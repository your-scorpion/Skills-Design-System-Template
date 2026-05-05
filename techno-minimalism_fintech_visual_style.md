---
version: 1.1
name: AXIOM
description: |
  A dual-canvas design system built on tension and precision. The void canvas
  (dark mode) runs near-black with electric chartreuse and hot coral weapons.
  The light canvas (day mode) runs white-to-stone with a cooled cobalt-signal
  and a warm clay cut — both accents shift hue when the surface flips, so they
  stay alive without burning the eye. Hard-cut editorial layout, industrial
  mono type, right angles everywhere. Typography is the architecture; surface
  mode is the register; accent color is the single weapon per viewport.

colors:
  # ─── VOID CANVAS (dark mode) ─────────────────────────────────────────────
  void: "#08080a"
  void-raised: "#111114"
  void-surface: "#16181b"
  void-edge: "#242428"
  void-muted: "#2e2e34"

  # ─── LIGHT CANVAS (day mode) ─────────────────────────────────────────────
  canvas: "#ffffff"
  canvas-parchment: "#f5f5f2"      # warm off-white — the default page bg
  canvas-soft: "#ededea"           # subtle band differentiation
  canvas-stone: "#e2e2de"          # hairline-weight fills, chip backgrounds

  # ─── INK SCALE (light surfaces) ──────────────────────────────────────────
  ink: "#191b1e"                   # primary text — warmer than pure black
  ink-secondary: "#3d4045"         # supporting body copy
  ink-muted: "#5c6068"             # captions, metadata
  ink-ghost: "#9098a0"             # disabled, placeholder
  ink-hairline: "#d8d8d4"          # 1px dividers at rest
  ink-hairline-strong: "#b8b8b4"   # emphasized dividers, active input borders

  # ─── CHALK SCALE (void surfaces) ─────────────────────────────────────────
  chalk: "#f0f0ec"
  chalk-dim: "#b8b8b2"
  chalk-ghost: "#6a6a65"
  chalk-hairline: "#2a2a2f"
  chalk-hairline-strong: "#3a3a40"

  # ─── SIGNAL — Accent I ───────────────────────────────────────────────────
  # Void canvas: electric chartreuse
  signal: "#c8ff00"
  signal-dim: "#8fb800"
  signal-flare: "#e0ff4d"
  signal-surface: "#1e2800"        # chip bg on void

  # Light canvas: deep cobalt-violet
  signal-day: "#4a50e0"
  signal-day-dim: "#3840c4"
  signal-day-bright: "#5c63f5"
  signal-day-pale: "#eeeffe"       # chip fill on light
  signal-day-mid: "#c4c6f8"        # chip border on light

  # ─── CUT — Accent II ─────────────────────────────────────────────────────
  # Void canvas: hot coral
  cut: "#ff3520"
  cut-dim: "#cc2918"
  cut-pale: "#ff6b57"
  cut-surface: "#280800"           # chip bg on void

  # Light canvas: clay-rose
  cut-day: "#c8352a"
  cut-day-dim: "#a02820"
  cut-day-pale: "#fdeeed"          # chip fill on light
  cut-day-mid: "#f0b0aa"           # chip border on light

  # ─── STRUCTURAL ──────────────────────────────────────────────────────────
  invert-ink: "#08080a"            # text on signal/chartreuse tile
  transparent: "transparent"

typography:
  hero:
    fontFamily: "'Clash Display', 'Syne', 'Cabinet Grotesk', Georgia, serif"
    fontSize: 80px
    fontWeight: 700
    lineHeight: 0.92
    letterSpacing: -3px
    textTransform: uppercase

  display:
    fontFamily: "'Clash Display', 'Syne', 'Cabinet Grotesk', Georgia, serif"
    fontSize: 52px
    fontWeight: 700
    lineHeight: 0.95
    letterSpacing: -1.5px
    textTransform: uppercase

  display-sm:
    fontFamily: "'Clash Display', 'Syne', 'Cabinet Grotesk', Georgia, serif"
    fontSize: 36px
    fontWeight: 600
    lineHeight: 1.05
    letterSpacing: -0.5px

  label-xl:
    fontFamily: "'DM Mono', 'Departure Mono', 'IBM Plex Mono', monospace"
    fontSize: 13px
    fontWeight: 500
    lineHeight: 1.0
    letterSpacing: 0.12em
    textTransform: uppercase

  label:
    fontFamily: "'DM Mono', 'Departure Mono', 'IBM Plex Mono', monospace"
    fontSize: 11px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.10em
    textTransform: uppercase

  body-editorial:
    fontFamily: "'Instrument Serif', 'Playfair Display', Georgia, serif"
    fontSize: 20px
    fontWeight: 400
    fontStyle: italic
    lineHeight: 1.55
    letterSpacing: 0.01em

  body:
    fontFamily: "'DM Mono', 'Departure Mono', 'IBM Plex Mono', monospace"
    fontSize: 15px
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: -0.01em

  body-sm:
    fontFamily: "'DM Mono', 'Departure Mono', 'IBM Plex Mono', monospace"
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: 0

  data:
    fontFamily: "'DM Mono', 'IBM Plex Mono', monospace"
    fontSize: 48px
    fontWeight: 300
    lineHeight: 1.0
    letterSpacing: -0.04em
    fontVariantNumeric: tabular-nums

  data-sm:
    fontFamily: "'DM Mono', 'IBM Plex Mono', monospace"
    fontSize: 24px
    fontWeight: 300
    lineHeight: 1.0
    letterSpacing: -0.02em
    fontVariantNumeric: tabular-nums

  fine:
    fontFamily: "'DM Mono', monospace"
    fontSize: 10px
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 0.06em
    textTransform: uppercase

rounded:
  none: 0px
  xs: 2px    # inline code chips only
  sm: 4px    # compact tags
  # Nothing above 4px. Right angles are the grammar.

spacing:
  micro: 2px
  xxs: 4px
  xs: 8px
  sm: 16px
  md: 24px
  lg: 40px
  xl: 64px
  xxl: 96px
  section: 128px
  section-sm: 80px

grid:
  columns: 12
  gutter: 24px
  margin: 40px
  max-width: 1600px
  editorial-max: 1200px

motion:
  duration-fast: 120ms
  duration-base: 200ms
  duration-slow: 400ms
  duration-crawl: 800ms
  ease-cut: "cubic-bezier(0.16, 1, 0.3, 1)"
  ease-snap: "cubic-bezier(0.87, 0, 0.13, 1)"
  ease-linear: "linear"

components:
  # ─── NAVIGATION ──────────────────────────────────────────────────────────
  global-nav-void:
    backgroundColor: "{colors.void}"
    textColor: "{colors.chalk}"
    typography: "{typography.label}"
    height: 52px
    borderBottom: "1px solid {colors.chalk-hairline}"

  global-nav-light:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    height: 52px
    borderBottom: "1px solid {colors.ink-hairline}"

  # ─── BUTTONS — VOID CANVAS ────────────────────────────────────────────────
  button-primary:
    backgroundColor: "{colors.signal}"
    textColor: "{colors.invert-ink}"
    typography: "{typography.label-xl}"
    rounded: "{rounded.none}"
    padding: "12px 28px"

  button-ghost:
    backgroundColor: "{colors.transparent}"
    textColor: "{colors.chalk}"
    typography: "{typography.label-xl}"
    rounded: "{rounded.none}"
    padding: "11px 27px"
    border: "1px solid {colors.void-edge}"

  button-cut:
    backgroundColor: "{colors.cut}"
    textColor: "{colors.chalk}"
    typography: "{typography.label-xl}"
    rounded: "{rounded.none}"
    padding: "12px 28px"

  button-void-utility:
    backgroundColor: "{colors.void-raised}"
    textColor: "{colors.chalk-dim}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "8px 16px"
    border: "1px solid {colors.chalk-hairline}"

  # ─── BUTTONS — LIGHT CANVAS ───────────────────────────────────────────────
  button-primary-day:
    backgroundColor: "{colors.signal-day}"
    textColor: "{colors.canvas}"
    typography: "{typography.label-xl}"
    rounded: "{rounded.none}"
    padding: "12px 28px"

  button-ghost-day:
    backgroundColor: "{colors.transparent}"
    textColor: "{colors.ink}"
    typography: "{typography.label-xl}"
    rounded: "{rounded.none}"
    padding: "11px 27px"
    border: "1px solid {colors.ink-hairline-strong}"

  button-cut-day:
    backgroundColor: "{colors.cut-day}"
    textColor: "{colors.canvas}"
    typography: "{typography.label-xl}"
    rounded: "{rounded.none}"
    padding: "12px 28px"

  button-soft-day:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.ink-secondary}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "8px 16px"
    border: "1px solid {colors.ink-hairline}"

  # ─── SECTION TILES ────────────────────────────────────────────────────────
  tile-void:
    backgroundColor: "{colors.void}"
    textColor: "{colors.chalk}"
    padding: "128px 40px"

  tile-raised:
    backgroundColor: "{colors.void-raised}"
    textColor: "{colors.chalk}"
    padding: "128px 40px"

  tile-signal:
    backgroundColor: "{colors.signal}"
    textColor: "{colors.invert-ink}"
    padding: "128px 40px"
    # ONCE PER PAGE. Non-negotiable.

  tile-canvas:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    padding: "128px 40px"

  tile-parchment:
    backgroundColor: "{colors.canvas-parchment}"
    textColor: "{colors.ink}"
    padding: "128px 40px"

  tile-soft:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.ink}"
    padding: "128px 40px"

  tile-signal-day:
    backgroundColor: "{colors.signal-day}"
    textColor: "{colors.canvas}"
    padding: "128px 40px"
    # Light-canvas equivalent of tile-signal. Same once-per-page rule.

  # ─── CARDS — VOID ─────────────────────────────────────────────────────────
  card-base:
    backgroundColor: "{colors.void-raised}"
    textColor: "{colors.chalk}"
    rounded: "{rounded.none}"
    padding: "32px"
    border: "1px solid {colors.chalk-hairline}"

  card-signal:
    backgroundColor: "{colors.void-raised}"
    textColor: "{colors.chalk}"
    rounded: "{rounded.none}"
    padding: "32px"
    borderLeft: "3px solid {colors.signal}"

  card-data:
    backgroundColor: "{colors.void-surface}"
    textColor: "{colors.chalk}"
    rounded: "{rounded.none}"
    padding: "24px"
    border: "1px solid {colors.chalk-hairline}"

  # ─── CARDS — LIGHT ────────────────────────────────────────────────────────
  card-base-light:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "32px"
    border: "1px solid {colors.ink-hairline}"

  card-signal-light:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "32px"
    borderLeft: "3px solid {colors.signal-day}"

  card-soft-light:
    backgroundColor: "{colors.canvas-parchment}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "32px"
    border: "1px solid {colors.ink-hairline}"

  card-data-light:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "24px"
    border: "1px solid {colors.ink-hairline}"

  # ─── TAGS & CHIPS ─────────────────────────────────────────────────────────
  tag:
    backgroundColor: "{colors.void-muted}"
    textColor: "{colors.chalk-dim}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "3px 8px"

  tag-signal:
    backgroundColor: "{colors.signal-surface}"
    textColor: "{colors.signal}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "3px 8px"

  tag-cut:
    backgroundColor: "{colors.cut-surface}"
    textColor: "{colors.cut-pale}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "3px 8px"

  tag-light:
    backgroundColor: "{colors.canvas-stone}"
    textColor: "{colors.ink-secondary}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "3px 8px"

  tag-signal-light:
    backgroundColor: "{colors.signal-day-pale}"
    textColor: "{colors.signal-day}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "3px 8px"
    border: "1px solid {colors.signal-day-mid}"

  tag-cut-light:
    backgroundColor: "{colors.cut-day-pale}"
    textColor: "{colors.cut-day}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "3px 8px"
    border: "1px solid {colors.cut-day-mid}"

  # ─── INPUTS ───────────────────────────────────────────────────────────────
  input-void:
    backgroundColor: "{colors.void-raised}"
    textColor: "{colors.chalk}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "12px 16px"
    border: "1px solid {colors.void-edge}"
    height: 48px

  input-light:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "12px 16px"
    border: "1px solid {colors.ink-hairline-strong}"
    height: 48px

  # ─── FOOTER ───────────────────────────────────────────────────────────────
  footer-void:
    backgroundColor: "{colors.void-raised}"
    textColor: "{colors.chalk-ghost}"
    typography: "{typography.body-sm}"
    padding: "64px 40px"
    borderTop: "1px solid {colors.chalk-hairline}"

  footer-light:
    backgroundColor: "{colors.canvas-parchment}"
    textColor: "{colors.ink-muted}"
    typography: "{typography.body-sm}"
    padding: "64px 40px"
    borderTop: "1px solid {colors.ink-hairline}"
---

## Overview

AXIOM v1.1 is a dual-canvas system built on tension, contrast, and precision. The void canvas stays near-black with electric chartreuse and hot coral, while the light canvas introduces warm whites, a five-stop ink scale, and accent shifts to cobalt-violet and clay-rose. Typography, spacing, motion, and zero-radius geometry remain shared across both modes.

The reference point is deliberate: fintech-grade tonal discipline and editorial pacing, but without soft consumer polish. Pill shapes, heavy shadows, and gradient haze are rejected outright.

### System Snapshot

| Axis | Decision | Effect |
|---|---|---|
| Core model | Dual-canvas system | Pages switch between void and light bands in hard cuts |
| Dark mode register | Near-black with chartreuse and hot coral | Tactical, nocturnal, high-contrast energy |
| Light mode register | White-to-stone with cobalt and clay | Analytical, premium, controlled clarity |
| Type system | Display serif plus industrial mono | Editorial hierarchy over systems rigor |
| Geometry | Zero-radius or near-zero-radius | Hard-cut, industrial silhouette |
| Accent logic | One weapon per viewport | Accent color stays rare and high-value |
| Depth model | Surface stepping and hairlines only | No shadow-based softness |

### Core Convictions

| Principle | Rule |
|---|---|
| Type is structure | Headlines are architectural, never decorative |
| Color is ammunition | One weapon per viewport, deployed once |
| Borders are load-bearing | 1px hairlines carry separation and hierarchy |
| Geometry stays hard | Right angles dominate both canvases |
| Motion is informational | Animate state change, not ambience |

---

## Canvas System

AXIOM operates in two full-bleed band modes. Pages switch between them using hard cuts only. No fades and no gradient transitions are allowed; the cut itself is the divider.

### Canvas Comparison

| Canvas | Core Surface | Supporting Surfaces | Text System | Accent Weapon | Best Used For |
|---|---|---|---|---|---|
| Void | `{colors.void}` / #08080a | `{colors.void-raised}`, `{colors.void-surface}` | `{colors.chalk}`, `{colors.chalk-dim}`, `{colors.chalk-ghost}` | `{colors.signal}` and `{colors.cut}` | Hero sections, flagship product moments, technical editorial bands |
| Light | `{colors.canvas}` / #ffffff | `{colors.canvas-parchment}`, `{colors.canvas-soft}`, `{colors.canvas-stone}` | Five-stop ink scale | `{colors.signal-day}` and `{colors.cut-day}` | Catalogue sections, comparison bands, forms, support documentation |

### Band Rhythm

| Sequence Step | Recommended Pattern |
|---|---|
| 1 | `tile-void` |
| 2 | `tile-canvas` or `tile-parchment` |
| 3 | `tile-void` or `tile-raised` |
| 4 | `tile-parchment` |
| 5 | `tile-signal` or `tile-signal-day` |
| 6 | `footer-void` or `footer-light` |

Signal tile rule: the signal tile appears exactly once per page.

---

## Color Philosophy

### Palette Roles

| Group | Primary Tokens | Role |
|---|---|---|
| Void surfaces | `{colors.void}`, `{colors.void-raised}`, `{colors.void-surface}` | Dark-mode floors, cards, nested containers |
| Light surfaces | `{colors.canvas}`, `{colors.canvas-parchment}`, `{colors.canvas-soft}`, `{colors.canvas-stone}` | Day-mode page bands, cards, chips |
| Light text | `{colors.ink}` through `{colors.ink-hairline-strong}` | Headline, body, metadata, and border hierarchy |
| Void text | `{colors.chalk}` through `{colors.chalk-hairline-strong}` | Text and border hierarchy on dark surfaces |
| Signal accents | `{colors.signal}` and `{colors.signal-day}` families | Primary CTA and active-state weapon by canvas |
| Cut accents | `{colors.cut}` and `{colors.cut-day}` families | Destructive or sharp edge accent by canvas |

### The Ink Scale (light surfaces)

| Token | Hex | Use |
|---|---|---|
| `{colors.ink}` | #191b1e | Headlines, primary labels |
| `{colors.ink-secondary}` | #3d4045 | Body copy, card descriptions |
| `{colors.ink-muted}` | #5c6068 | Captions, metadata |
| `{colors.ink-ghost}` | #9098a0 | Disabled, placeholder text |
| `{colors.ink-hairline}` | #d8d8d4 | 1px dividers at rest |
| `{colors.ink-hairline-strong}` | #b8b8b4 | Active input borders, emphasized rules |

The ink tones stay warm-gray to avoid the sterile register of neutral grayscale. `{colors.ink}` is intentionally warmer than pure black, reducing optical vibration against white at large sizes.

### Light Canvas Surface Steps

| Token | Hex | Role |
|---|---|---|
| `{colors.canvas}` | #ffffff | Primary page surface, cards |
| `{colors.canvas-parchment}` | #f5f5f2 | Alternating bands, footer |
| `{colors.canvas-soft}` | #ededea | Inset cards, data tile backgrounds |
| `{colors.canvas-stone}` | #e2e2de | Chip fills, rule backgrounds |

Each step is perceptually ~8% darker than the previous. The four steps create depth without shadow.

### Accent Behavior

| Accent | Void Canvas | Light Canvas | Rule |
|---|---|---|---|
| Signal | `{colors.signal}` / #c8ff00 | `{colors.signal-day}` / #4a50e0 | One CTA, one accent block, one active state |
| Signal support | `{colors.signal-surface}`, `{colors.signal-dim}`, `{colors.signal-flare}` | `{colors.signal-day-pale}`, `{colors.signal-day-mid}`, `{colors.signal-day-bright}` | Support chips and borders without overpowering the page |
| Cut | `{colors.cut}` / #ff3520 | `{colors.cut-day}` / #c8352a | Reserved for destructive or urgent states |
| Cut support | `{colors.cut-surface}`, `{colors.cut-pale}`, `{colors.cut-dim}` | `{colors.cut-day-pale}`, `{colors.cut-day-mid}`, `{colors.cut-day-dim}` | Keeps urgency legible at different contrast levels |

### No Gradient Rule

| Rule | Meaning |
|---|---|
| Gradient tokens | None |
| Depth on light surfaces | Achieved through surface stepping and border-color shifts |
| Imagery overlays | No atmospheric gradient overlays |

---

## Typography

All typography tokens, weights, sizes, and tracking rules from v1.0 apply identically on both canvases.

### Typographic Role Map

| Layer | Primary Tokens | Visual Purpose |
|---|---|---|
| Hero / display | `hero`, `display`, `display-sm` | Architectural headlines and section anchors |
| Labels | `label-xl`, `label`, `fine` | Navigation, controls, metadata, compact UI language |
| Editorial body | `body-editorial` | Select narrative or art-directed passages |
| System body | `body`, `body-sm` | Product copy, UI prose, technical text |
| Numeric display | `data`, `data-sm` | Metrics, KPIs, tabular numerics |

### Color Rules by Canvas

| Canvas | Headlines | Body | Metadata | Active / Link | Error Text |
|---|---|---|---|---|---|
| Void | `{colors.chalk}` | `{colors.chalk-dim}` | `{colors.chalk-ghost}` | `{colors.signal}` sparingly | `{colors.cut-pale}` |
| Light | `{colors.ink}` | `{colors.ink-secondary}` | `{colors.ink-muted}` | `{colors.signal-day}` | `{colors.cut-day}` |

---

## Layout

### Spacing Reference

| Area | Standard Value | Note |
|---|---|---|
| Section spacing | 128px | Default full-band rhythm |
| Section minimum | 80px | Do not go lower on light surfaces |
| Card padding | 32px | Default content-card interior |
| Button padding | 12px x 28px | Shared primary action rhythm |
| Light adaptation increase | +16px vertical | Add when converting `tile-void` to `tile-canvas` |

### Layout Rules

| Rule | Guidance |
|---|---|
| Light-canvas compression | Light surfaces need roughly 15% more internal padding to feel equally open |
| Card grid treatment | `card-base-light` and `card-soft-light` rely on 1px `{colors.ink-hairline}` borders only |
| Signal card hierarchy | `card-signal-light` uses a 3px cobalt left border as the only hierarchy cue |
| Elevation behavior | No shadow, no outer glow, no scale trickery |

---

## Elevation & Depth

### Void Canvas

| Level | Treatment | Use |
|---|---|---|
| Flat | No shadow, no border | Full-bleed tiles |
| Surface | `{colors.void-raised}` | Cards, nav |
| Nested | `{colors.void-surface}` | Containers within cards |
| Scrim | `rgba(0,0,0,0.8)` | Modal overlays only |

### Light Canvas

| Level | Treatment | Use |
|---|---|---|
| Base | `{colors.canvas}` | Primary page surface |
| Raised | `{colors.canvas-parchment}` | Alternating bands, footer |
| Inset | `{colors.canvas-soft}` | Cards within parchment bands |
| Chip | `{colors.canvas-stone}` | Chip fills, rule backgrounds |

No shadows on either canvas. Elevation is entirely surface-color stepping.

---

## Component Reference

### Button Pairs by Canvas

| Void | Light | Role |
|---|---|---|
| `button-primary` (chartreuse) | `button-primary-day` (cobalt) | Primary CTA |
| `button-ghost` (chalk border) | `button-ghost-day` (ink border) | Secondary CTA |
| `button-cut` (hot coral) | `button-cut-day` (clay-rose) | Destructive |
| `button-void-utility` | `button-soft-day` | Tertiary / utility |

Same shape grammar on both: zero border-radius, label-xl type, 12px × 28px padding.

### Card Grammar

| Void | Light | Role |
|---|---|---|
| `card-base` | `card-base-light` | Default content card |
| `card-signal` | `card-signal-light` | Featured / recommended |
| `card-data` | `card-data-light` | Metric / numeric display |
| — | `card-soft-light` | Subdued card on parchment |

### Tag Grammar

| Void | Light | Role |
|---|---|---|
| `tag` | `tag-light` | Neutral label |
| `tag-signal` | `tag-signal-light` | Positive / active |
| `tag-cut` | `tag-cut-light` | Warning / error |

Light tags gain explicit border tokens (`signal-day-mid`, `cut-day-mid`) — a tint alone on white fails to define the chip edge without shadow. The border replaces shadow.

### Signal Tile Rule
`tile-signal` (chartreuse) and `tile-signal-day` (cobalt) are both governed by the once-per-page maximum. A page cannot contain both. Choose the one that matches the dominant canvas of the page.

### Structural Components

| Void Component | Light Component | Role |
|---|---|---|
| `global-nav-void` | `global-nav-light` | Navigation matched to page canvas |
| `tile-void`, `tile-raised`, `tile-signal` | `tile-canvas`, `tile-parchment`, `tile-soft`, `tile-signal-day` | Full-band page sections |
| `input-void` | `input-light` | Form input field system |
| `footer-void` | `footer-light` | Footer matched to dominant canvas |

---

## Do's and Don'ts

| Do | Don't |
|---|---|
| Switch full bands in hard cuts | Fade between canvas modes |
| Use `{colors.signal}` on void and `{colors.signal-day}` on light | Swap accent weapons across canvases |
| Use `{colors.ink}` for headlines and `{colors.ink-secondary}` for body on light | Collapse all light text to `{colors.ink}` |
| Keep one weapon per viewport | Spread accent color across multiple competing elements |
| Match footer and nav to dominant canvas | Use light nav on void pages or void footer on light pages |
| Add 16px vertical padding when adapting void tiles to light tiles | Shrink light sections below 80px padding |
| Keep radius at `{rounded.sm}` or below | Introduce soft rounded corners |
| Use border and surface stepping for elevation | Add `box-shadow` |
| Use `{colors.cut-pale}` or `{colors.cut-day}` for error text | Use raw `{colors.cut}` as body text |
| Keep disabled text to `{colors.ink-ghost}` only | Reuse ghost tone for active content |

---

## Responsive Behavior

All breakpoints and collapsing strategies from v1.0 hold.

| Condition | Adjustment |
|---|---|
| Mobile under 640px | `canvas-parchment` bands reduce vertical padding from 128px to 64px |
| Reason | Parchment surfaces feel optically larger than void surfaces at the same spacing |

---

## Iteration Guide

| Step | Decision | Validation Check |
|---|---|---|
| 1 | Decide canvas first | Every subsequent token should inherit from void or light mode |
| 2 | Choose the correct signal weapon | Chartreuse only on void, cobalt only on light |
| 3 | Apply the ink hierarchy on light | Headlines use `{colors.ink}`, body uses `{colors.ink-secondary}` |
| 4 | Enforce the signal tile rule | Use `tile-signal` or `tile-signal-day`, never both |
| 5 | Use border, not fill, for signal cards | Featured cards get a 3px left border rather than a full accent fill |
| 6 | Validate canvas-matched chrome | `global-nav-light` on a void-heavy page is a design error |

---

## Known Gaps

| Gap | Current State |
|---|---|
| Mixed-canvas hero | Architecturally possible, not yet formalized as a component |
| Light-canvas data viz palette | Third and fourth series colors remain undecided |
| Photography on light canvas | Dark-backdrop renders perform poorly on parchment surfaces |
| Focus rings on light canvas | 2px signal-day outline passes AA, 3px is preferred for production |
| Forced dark mode override | `color-scheme` handling is still undocumented in implementation tokens |
