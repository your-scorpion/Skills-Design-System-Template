---
name: researcher-prompt-vocabulary
description: A glossary skill for LLMs that defines qualitative research terms and distinguishes commonly confused concepts when analyzing interviews, writing insights, conclusions, recommendations, and prompts.
---

# Researcher’s Vocabulary for Prompts

Definitions of research words that can be inserted into an AI prompt.

Each word has a short definition and an “Often confused with” line. This matters because it shows where a model may make terminology mistakes and confuse the term with similar-sounding words.

## When to use this skill

Use this skill when an LLM is asked to:

- analyze qualitative research data;
- write observations, patterns, insights, hypotheses, conclusions, or recommendations;
- create or improve research prompts;
- distinguish research terms that are often confused;
- avoid inventing insights or conclusions without sufficient data.

## LLM operating rules

- Use precise terms from this glossary when they fit the task.
- Do not upgrade an observation into an insight or conclusion without evidence.
- If the data lacks grounds for an insight or conclusion, label the statement as an observation or hypothesis.
- For patterns, state how many people show the pattern and who they are.
- For quotes, preserve the respondent’s exact words. Do not merge quotes from different people, shorten them, or “improve” them.
- For conclusions, state how many people the conclusion is based on and support it with quotes from those people.
- For recommendations, derive the action from a conclusion and specify what to do and for whom.
- Use only the glossary terms needed for the specific request. Do not insert the whole glossary into every prompt.

## Glossary

### 01 What we see in data

#### Observation

What a person said or did, recorded without interpretation. Example: “Opened the app three times during the evening and never reached checkout.”

Often confused with: conclusion.

#### Quote

The respondent’s verbatim words, without retelling, without merging quotes from different people into one, and without shortening.

Often confused with: paraphrase in quotation marks. The model likes to “improve” or trim quotes, so this should be stated separately.

#### Pattern

Behavior or reaction that repeats among several people in a similar situation. Always state how many such people there are and who they are.

Often confused with: a frequent answer to a guide question.

### 02 What drives a person

#### Need

What a person needs to obtain or change in their situation, regardless of a specific product. A need describes a state of needing something. It can be formulated through the result for the person: “to know that the order will definitely arrive by Friday.”

Often confused with: a wish or an idea to change something. “I want tracking” is already a solution.

#### Job

The progress a person wants to achieve in a specific situation. Formula: “When…, I want…, so that…”.

Often confused with: product functionality.

#### Motive

The reason a person begins to act right now; what impels them toward activity that can satisfy that need.

Often confused with: need. A need can live for years; a motive triggers it.

#### Pain

A difficulty a person already experiences and speaks about themselves.

Often confused with: barrier.

#### Barrier

What prevents a person from taking the next step: buying, starting, returning. It can be rational (price, complexity) or emotional (fear of making a mistake).

Often confused with: pain. Pain exists before encountering the product; a barrier appears on the path to it.

#### Expectation

A person’s idea of how things should be. Disappointment or contradiction appears where expectation diverges from reality.

#### Value

What a person considers important to receive and for which they are willing to pay with money, time, or effort.

Often confused with: benefit formulated by the business.

### 03 Context

#### Context

Circumstances: where, when, with whom, and in what state the person is.

#### Scenario

The sequence of actions a person takes to achieve a goal in a specific situation.

#### Trigger

The event after which a person begins to act.

#### Touchpoint

Any moment when a person encounters the product or company.

#### Workaround

The way a person solves the task themselves, without the product or by bypassing it. A strong signal of an unmet need.

#### Influencers

People or organizations that influence a person (their behavior, thinking) in a specific situation.

### 04 Analysis of results

#### Insight

A non-obvious explanation of why people do what they do. It relies on several observations, changes understanding of the task, and leads to action. It can also rely on contradictions when expectations and reality do not match.

Often confused with: observation (“users do not read instructions” is an observation) and any interesting finding.

#### Hypothesis

An assumption that still needs to be tested. It is formulated so it is clear what would confirm or refute it.

Often confused with: conclusion.

#### Conclusion

A statement supported by research data. When working with AI, it is better to ask it to state how many people the conclusion is based on and to support it with quotes from those people.

#### Recommendation

A concrete action for the team that follows from a conclusion: what to do and for whom.

Often confused with: a retelling of the conclusion in the imperative mood.

### 05 For working with business and the brief

#### Business task / business decision

The decision a company wants to make based on the research results.

#### Research question

What needs to be learned from people in order to make that decision.

Often confused with: an interview guide question.

#### Target audience

People for whom the product is created and who make decisions about it.

#### Segment

A group within the audience united by a similar situation and need. In qualitative research, use the word “segment” carefully: if it is not in the brief and the target audience has not been divided into segments in advance, you should not identify segments independently.

Often confused with: sociodemographic. In qualitative research, audiences are rarely divided by age and income.

#### Portrait / persona

A generalized image of a segment representative assembled from real interviews. A more characteristic concept for qualitative research.

Often confused with: an invented character.

#### Sample

Who and how many people participated, and by what criteria they were selected.

#### Research limitations

What the research cannot claim because of the sample, method, or timing.

## 06 How to insert the vocabulary into a prompt

- Take only the words that are needed in the specific request. The whole glossary dilutes the model’s attention and confuses you.
- Add the line: “If the data lacks grounds for an insight or conclusion, call it an observation or hypothesis.” This one phrase noticeably reduces the number of fabricated insights.

## Prompt snippet

```text
Use these research definitions: [insert only relevant terms from the glossary].

If the data lacks grounds for an insight or conclusion, call it an observation or hypothesis.

For patterns, state how many people show the pattern and who they are.
For quotes, preserve the respondent’s exact words and do not merge or shorten them.
For conclusions, state how many people the conclusion is based on and support it with quotes.
For recommendations, specify what to do and for whom.