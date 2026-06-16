# Memory v0.1

## Purpose

Memory is the most valuable asset in Hunter Learning OS.

Memory is not a note archive.

Memory tracks how the learner's understanding, questions, misconceptions, patterns, and applications change over time.

The core asset is Cognitive Change History.

## Core Rule

Do not save personal cognitive material automatically.

Generate a Memory candidate at natural stopping points, then ask the user whether to save it.

## Memory Types

### Cognitive Change History

Records how the learner's understanding changed.

Use for:

- Before/after understanding
- Changed mental models
- New self-observations
- Identity-level or behavior-relevant shifts

Example:

```text
Before:
I thought higher income would make all problems disappear.

After:
I see that income may support responsibility and safety, but it cannot guarantee inner ease.
```

### Concept History

Tracks concepts the learner has encountered, clarified, mastered, or still finds unclear.

Use for:

- Concept definitions
- Current explanation level
- Key distinctions
- Open questions
- Related examples

### Misconception History

Tracks misunderstandings and corrections.

Use for:

- Incorrect prior understanding
- Corrected model
- What triggered the correction
- Whether the correction is stable or fragile

### Learning Profile

Tracks the learner's evolving learning patterns.

Use for:

- Interests
- Preferred learning styles
- Strong domains
- Weak domains
- Recurring questions
- Repeated cognitive patterns
- Methods that work well or poorly

### Idea Network

Tracks relationships among ideas, sources, domains, and recurring themes.

Use for:

- Concept links
- Cross-book connections
- Cross-domain analogies
- Tensions between ideas
- Long-term inquiry threads

### Practice and Review Items

Tracks follow-up actions, observations, and recall prompts.

Use for:

- Small practices
- Review questions
- Spaced repetition candidates
- Real-life experiments
- Future check-ins

## Memory Candidate Format

Use this format when a session may produce a memory:

```text
Topic:

Memory Type:

Before:

After:

Trigger:

Open Question:

Practice or Review:

Save Recommendation:
```

Fields may be omitted if not relevant.

Do not force every candidate into every field.

## Source Session Coverage

When the Memory candidate comes from a chapter, article, lecture, video, or other source-based session, include a short coverage note when useful.

Coverage is not ordinary note-taking.

It helps prevent the system from treating one cognitive change as complete source internalization.

Suggested format:

```text
Source Coverage:
Processed deeply:

Touched lightly:

Still open:

Possible next routes:
```

Use this when:

- The user discussed a whole source but the session focused on one branch.
- A Memory candidate emerges before the source has been broadly covered.
- The user may want to continue the source later.

Keep coverage brief.

Do not make it the main memory unless the user's goal was review or source mapping.

## When to Create a Memory Candidate

Create a candidate when:

- The user's understanding changed.
- A misconception was corrected.
- A strong open question emerged.
- A recurring cognitive pattern appeared.
- A source became connected to the user's life.
- A practice or review item was created.
- The user explicitly asks to remember or save something.

## When NOT to Create a Memory Candidate

Do not create a candidate when:

- The exchange was purely factual.
- The user did not engage enough to show change.
- The topic is too private or sensitive and the user has not invited preservation.
- The user wants to stop immediately.
- The response was only a quick clarification.
- Saving would turn a passing emotion into an overfixed identity claim.

## Save Rules

Before saving personal Memory, ask for confirmation.

Good confirmation language:

```text
This feels like a possible Cognitive Change record.
Would you like me to save it, revise it, or leave it unsaved?
```

If the user says yes:

- Save the shortest accurate version.
- Prefer cognitive movement over private detail.
- Preserve uncertainty when the user is unsure.

If the user says no:

- Do not save.
- Continue normally.

If the user wants revision:

- Let the user adjust wording.
- Save only the user-approved version.

## Writing Principles

Memory should be:

- Concise
- Specific
- Respectful
- Revisable
- Focused on change
- Written in the user's language when possible

Memory should avoid:

- Overdiagnosis
- Excessive personal detail
- Permanent labels
- Claims stronger than the evidence
- Turning speculation into fact

## Memory Quality Levels

### Low Quality

```text
User read Chapter 8 of The Joy of Living.
```

This is reading history, not cognitive memory.

### Medium Quality

```text
User discussed why people chase material things even if material things do not guarantee happiness.
```

This records topic, but not cognitive movement.

### High Quality

```text
The user moved from asking "If material abundance does not remove suffering, why pursue material things?" toward distinguishing material resources as conditions for responsibility and safety from material resources as a fantasy of complete inner security.
```

This records cognitive change.

## Example: Chapter 8 Scenario

Source:

*The Joy of Living*, Chapter 8, "Why Are We Unhappy?"

Possible Memory Candidate:

```text
Topic:
Material conditions and happiness

Memory Type:
Cognitive Change History

Before:
The user questioned whether pursuing material resources has meaning if material abundance does not guarantee happiness.

After:
The user began distinguishing material resources as support for family responsibility and safety from the belief that higher income can make all problems disappear.

Trigger:
Chapter 8's discussion of external conditions, attachment, and the fading of stimulation.

Open Question:
How can the user pursue material responsibility without turning income into a guarantee of inner peace?

Practice or Review:
When "If only I had more income" appears, distinguish:
- What responsibility am I actually trying to meet?
- What inner discomfort am I hoping money will permanently remove?

Save Recommendation:
Ask the user before saving because this is personal cognitive material.
```

## Interaction With Router

Router decides whether a Memory candidate may be useful.

Memory decides:

- What type of memory it is
- Whether it is worth saving
- How it should be written
- Whether user consent is required

Router should not save personal Memory directly.

## Interaction With Skills

### Deep Dive

Often updates:

- Concept History
- Misconception History
- Cognitive Change History

### Review

Often updates:

- Practice and Review Items
- Concept History
- Learning Profile

### Synthesis

Often updates:

- Idea Network
- Learning Profile
- Cognitive Change History

### Application

Often updates:

- Practice and Review Items
- Cognitive Change History
- Learning Profile

### Reflection

Often updates:

- Cognitive Change History
- Learning Profile
- Practice and Review Items
