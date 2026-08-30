# Agent Operating Rules: State Design & Testing Discipline

## Part 1 — State Properties Checklist

Before writing or modifying any code that touches persistent or shared state, explicitly work out these properties for each state/component involved. Write the answer down (comment, design note, PR description) before implementing — don't guess and find out later.

- **SSOT (Single Source of Truth)** — which store or service owns this data. Everything else is a cache or a copy, never a second owner.
- **Transactionality** — does the operation commit fully or not at all, or can it leave a half-done state behind?
- **Idempotency** — running the same operation twice (accidental retry, duplicate message) must produce the same result as running it once.
- **Concurrency** — what happens when two callers touch the same data at the same time? Name the lock, version check, or isolation level.
- **Ordering guarantees** — can events/requests arrive out of order, and does that matter here?
- **Retries and deduplication** — how is a retried request recognized so it isn't processed twice?
- **Partial failure** — what state is left if the operation dies halfway through?
- **Timeouts** — how long do you wait before giving up, and what does "giving up" do to the state?
- **Cancellation** — can an in-flight operation be stopped without corrupting state?
- **Recovery** — how does the system return to a known-good state after a crash or restart?
- **Observability** — can the actual behavior be reconstructed after the fact from logs/metrics/traces?

**Minimize failure points.** Don't add a queue, cache, service, or abstraction layer unless the requirements above actually demand it. Choose each technology against real requirements, maturity, performance, and long-term maintainability — never because it's familiar (**inertia**) or because it's new (**novelty**).

## Part 2 — The Fix-It Loop

Apply this sequence for every defect or behavior change, in order — don't skip steps:

1. **Identify** the observable defect or new requirement precisely.
2. **Trace** the affected execution path to the actual root cause, not the first place the symptom shows up.
3. **Reproduce** the defect with a regression test, a **property-based test** (a test that checks a rule holds across many generated inputs instead of one hand-picked example), or another independent check.
4. **Document the invariant** that must hold — the rule the fix is actually enforcing.
5. **Implement the minimal general rule** that enforces it. Not a special case, not a patch — the rule.
6. **Remove** the replaced code path, duplicated logic, and any assertions that are now stale.
7. **Refactor only while every test stays green.**
8. **Verify boundaries** — hostile inputs, error paths, failure scenarios.
9. **Review the diff** as its own artifact, separate from the narrative of what was done.
10. **Independently re-review** the final state — don't just trust the first pass.
11. **Re-review the affected area** after corrections land.
12. **Provide reproducible evidence** the issue is resolved — a failing-then-passing test, a log, a before/after.

## Part 3 — Test Taxonomy

### By level
- **Unit** — a single function/module's contract in isolation.
- **Integration** — how modules behave together with real adapters (real DB, real API client — not mocks).
- **Contract** — whether a boundary (API, schema, event) stays compatible with what consumers expect.
- **Smoke** — the fastest check that the assembled system is minimally alive.
- **E2E (End-to-End)** — a full real user journey, start to finish.

### Against regression
- **Regression tests** — lock in a bug staying fixed.
- **Characterization tests** — pin down current behavior so any change to it is visible, even before you know if it's "correct."
- **Reference vectors** — known input/output pairs from a spec or external authority.
- **Golden tests** — compare output against a saved known-good file.
- **Snapshots** — only when the snapshot represents a stable contract, not just whatever the code currently happens to do.

### Beyond hand-picked examples
- **Property-based testing** — generate many random inputs and assert a general rule holds, instead of writing one example at a time.
- **Fuzz testing** — throw malformed/random input at the system to find crashes or unexpected states.
- **Differential testing** — run two implementations (or old vs. new) on the same input and compare.
- **Metamorphic testing** — check a relationship between outputs holds (e.g. "sorting twice gives the same result as sorting once") when there's no ground-truth answer to check against.
- **Fault injection** — deliberately break a dependency (network, disk, downstream service) to test failure handling.
- **Concurrency testing** — deliberately race conditions to check locking/ordering logic actually holds.
- **Load, stress, and soak testing** — behavior under expected load, above expected load, and over long duration.

### Validating the tests themselves
- **Mutation testing** — deliberately introduce small bugs into the code and confirm the test suite catches them. A suite that stays green through a mutation isn't testing anything.
- **Deliberate sabotage** — manually break the implementation and confirm the tests fail.
- **Independent oracle** — a second, independently-derived way of computing the expected answer (not copy-pasted from the implementation).
- **Proven counterexample** — a concrete case that would fail without the fix.
- **Anti-vacuity assertions** — confirm the test can actually fail — it isn't asserting something trivially true.

**Rule of thumb:** a test that claims to catch a specific defect must demonstrate it would go red without the fix — via mutation testing, deliberate sabotage, or an equivalent method. A green suite that's never been shown capable of failing proves nothing.
