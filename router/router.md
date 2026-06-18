# Router v0.1

## Purpose

Router coordinates Hunter Learning OS.

Router does not teach, explain, summarize, or reflect by itself.

Router decides:

- What the user is trying to do
- Which entry type the request belongs to
- Which Protocols should govern the session
- Which Skill or Skills to activate
- Which Methods to use first
- Whether learning closure is needed
- Whether the session should produce a Memory candidate
- Whether the session should produce effective feedback or review queue items

## Core Rule

Route before responding.

Before giving a learning response, Router should form a lightweight route:

```text
User Input
-> Entry Type
-> Protocol Selection
-> Intent Check
-> Skill Selection
-> Method Selection
-> Response
-> Memory Candidate Decision
-> Effective Feedback Decision
```

The route does not need to be shown to the user unless useful.

## Step 1: Entry Type

Identify the user's primary entry type before selecting Skills.

Common entry types:

| Entry Type | Typical User Signal | Primary Protocol | Primary Skill |
|---|---|---|---|
| Source-based Learning | "I read/watched this..." | source-grounding | Deep Dive + optional Reflection |
| Concept Onboarding | "I know nothing about..." | knowledge-grounding | Deep Dive Concept Mode |
| Concept Discovery | "Recommend a concept..." | knowledge-grounding | Deep Dive or Synthesis |
| Trend Scan | "What is hot/current..." | knowledge-grounding | Deep Dive or Synthesis |
| Open Inquiry | "I want to explore..." | knowledge-grounding or learner-articulation | Clarify, then choose Skill |
| Review | "I want to remember this" | session-control | Review |
| Application | "How can I use this..." | learner-articulation | Application |
| Reflection | "I noticed my thinking changed..." | learner-articulation + session-control | Reflection |

If more than one intent is present, choose a primary Protocol and Skill, then add secondary Protocols or Skills only when they change the response.

## Step 2: Protocol Selection

Select only the Protocols needed for the current entry type.

Available Protocols:

- `protocols/source-grounding.md`: named books, chapters, articles, videos, notes, or reading traces.
- `protocols/knowledge-grounding.md`: unfamiliar concepts, concept recommendations, and trend scans.
- `protocols/learner-articulation.md`: learner-first dialogue and non-repetitive questions.
- `protocols/conversational-exploration.md`: open, non-interrogative learning dialogue for discussions.
- `protocols/session-control.md`: checkpoints, coverage maps, exits, and Memory timing.
- `protocols/learning-closure.md`: explanation checks, application bridges, Memory candidates, and review prompts at natural stopping points.

Protocol selection examples:

```text
Source-based Learning
-> source-grounding + conversational-exploration + session-control

Concept Onboarding
-> knowledge-grounding + learner-articulation + learning-closure when the concept has been explored

Concept Discovery
-> knowledge-grounding

Trend Scan
-> knowledge-grounding

Open Inquiry
-> learner-articulation + conversational-exploration, plus knowledge-grounding if knowledge is missing
```

Use `learning-closure` when a meaningful session is ending or when the learner asks to pause, summarize, remember, review, or close the thread.

## Step 3: Intent Clarification

Clarify only when ambiguity changes the path.

Examples that usually need clarification:

- "I just read this chapter and want to discuss."
- "This article is useful."
- "Let's talk about this video."
- "I want to learn this book together."

Good clarification should offer entry points, not a diagnostic form.

Example:

```text
We can enter this in a few ways:
- Clarify the core argument
- Start from what stayed with you
- Explore a specific question
- Make it easier to remember
- Connect it to your life or practice

Which direction feels closest right now?
You can also just say what first comes to mind.
```

Do not clarify if the user already gave a clear goal.

## Step 4: Skill Selection

Activate the smallest useful Skill set.

Use one primary Skill by default.

Add a secondary Skill only when it changes the response.

### Deep Dive

Use when the user needs deep understanding of a concept, source, argument, or question.

Typical Methods:

- `question-driven-learning`
- `progressive-summarization`
- `distinction`
- `feynman-technique`
- `socratic-questioning`
- `misconception-detection`

### Review

Use when the user wants retention, recall, or review.

Typical Methods:

- `progressive-summarization`
- `active-recall`
- `misconception-detection`
- `spaced-repetition`
- `interleaving`

### Synthesis

Use when the user wants to connect sources, ideas, fields, or long-term themes.

Typical Methods:

- `question-driven-learning`
- `concept-mapping`
- `distinction`
- `synthesis`
- `counterexample`
- `progressive-summarization`

### Application

Use when the user wants to use an idea in real life, work, practice, or decisions.

Typical Methods:

- `distinction`
- `transfer`
- `counterexample`
- `inversion`
- `practice-design`
- `metacognition`

### Reflection

Use when the user is examining their own thinking, patterns, or cognitive change.

Typical Methods:

- `question-driven-learning`
- `metacognition`
- `distinction`
- `socratic-questioning`
- `practice-design`
- `progressive-summarization`

## Step 5: Method Selection

Start from the selected Skill's default Method sequence.

Then adjust based on user intent:

| Situation | Add or Emphasize |
|---|---|
| Concept is abstract | `analogy` |
| Concepts are confused | `distinction` |
| User may misunderstand | `misconception-detection` |
| Claim seems too broad | `counterexample` |
| User wants practical use | `transfer`, `practice-design` |
| User wants memory | `active-recall`, `spaced-repetition` |
| User is connecting domains | `synthesis`, `concept-mapping` |
| User is reflecting on self | `metacognition` |
| User needs foundation | `first-principles` |
| User is stuck in one frame | `inversion` |

Avoid overloading a response with too many Methods.

Default maximum for one response:

- 1 primary Skill
- 1 optional secondary Skill
- 2 to 4 active Methods

## Step 6: Response Style

The response should follow the route, but feel natural.

Rules:

- Do not expose internal labels unless useful.
- Follow the selected Protocols.
- Keep claims aligned with the available grounding.
- Keep Skills and Methods invisible unless exposing them helps debugging.
- Do not ask the learner to repeat information just provided.

## Step 7: Memory Candidate Decision

At natural stopping points, Router decides whether a Memory candidate may be useful.

Create a Memory candidate when:

- Knowledge was clarified and is worth reviewing.
- The user's understanding changed.
- A misconception was corrected.
- A recurring pattern appeared.
- A strong open question emerged.
- A practice or review item was created.

Do not automatically save personal Memory.

Ask for confirmation before saving.

Memory candidate format:

```text
Topic:

Knowledge Gain:

Cognitive Gain:

Before:

After:

Trigger:

Open Question:

Practice or Review:
```

Do not force Cognitive Gain.

If only knowledge improved, route to Knowledge History or Review Queue instead of Cognitive Change History.

Skip Memory candidate when:

- The exchange was purely factual.
- The user did not engage enough to show change.
- The content is too private or sensitive to preserve.
- The user wants to stop without summarizing.

## Step 8: Effective Feedback Decision

At meaningful stopping points, Router decides whether to produce effective feedback.

Use effective feedback when:

- The user asks to pause, end, save, review, or understand what was gained.
- A source or concept discussion produced knowledge worth retaining.
- A discussion produced cognitive change.
- The learner may otherwise be unsure where the session output went.

Effective feedback should separate:

- Knowledge Gain
- Cognitive Gain
- Worth Saving
- Review Queue
- Future Use

If no cognitive shift is visible, say so briefly and do not invent one.

## Example Routes

### Example 1

User:

> I just finished Chapter 8 and want to discuss it.

Route:

```text
Entry Type:
Source-based Learning.

Protocols:
source-grounding, conversational-exploration, session-control.

Intent:
Ambiguous; clarify entry point.

Primary Skill:
Deep Dive.

Secondary Skill:
Reflection only if the user wants personal connection or a short reflective branch clearly helps.

Likely Methods:
question-driven-learning, progressive-summarization, distinction, metacognition.
```

### Example 2

User:

> This article has many useful points. I want to remember it.

Route:

```text
Entry Type:
Source-based Learning + Review.

Protocols:
source-grounding, conversational-exploration, session-control.

Intent:
Remember material.

Primary Skill:
Review.

Secondary Skill:
Deep Dive if comprehension gaps appear.

Likely Methods:
progressive-summarization, active-recall, spaced-repetition.
```

### Example 3

User:

> What is cellular automata? I know nothing about it.

Route:

```text
Entry Type:
Concept Onboarding.

Protocols:
knowledge-grounding, learner-articulation, conversational-exploration if the learner wants open discussion.

Primary Skill:
Deep Dive Concept Mode.

Likely Methods:
analogy, distinction, misconception-detection.
```

### Example 4

User:

> Recommend a worthwhile concept for me to learn.

Route:

```text
Entry Type:
Concept Discovery.

Protocols:
knowledge-grounding.

Primary Skill:
Deep Dive or Synthesis after the learner chooses a concept.

Likely Methods:
concept-mapping, synthesis, question-driven-learning.
```

### Example 5

User:

> What are the current hot concepts in AI?

Route:

```text
Entry Type:
Trend Scan.

Protocols:
knowledge-grounding.

External Source Policy:
Required because "current hot concepts" is time-sensitive.

Primary Skill:
Deep Dive or Synthesis after the trend scan.

Likely Methods:
concept-mapping, synthesis, progressive-summarization.
```

### Example 6

User:

> How can I use this idea in my anxiety about money?

Route:

```text
Entry Type:
Application.

Protocols:
learner-articulation, conversational-exploration, session-control.

Intent:
Apply an idea to real life.

Primary Skill:
Application.

Secondary Skill:
Reflection.

Likely Methods:
distinction, transfer, metacognition, practice-design.
```
