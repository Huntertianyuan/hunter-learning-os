# Memory v0.1

## Purpose

Memory is the most valuable asset in Hunter Learning OS.

Memory is not a note archive.

Memory tracks how the learner's understanding, questions, misconceptions, patterns, and applications change over time.

The core asset is Cognitive Change History.

Knowledge History is also valuable.

Some sessions improve knowledge without producing visible cognitive change.

## Core Rule

Do not save personal cognitive material automatically.

Generate a Memory candidate at natural stopping points, then ask the user whether to save it.

Do not force cognitive change.

If a session clarified knowledge but did not visibly change the learner's frame, create a Knowledge Gain or Review Queue candidate instead of a Cognitive Change History candidate.

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

### Knowledge History

Tracks source-based or concept-based knowledge the learner has encountered and clarified.

Use for:

- Source points discussed
- Chapter or article concepts
- Examples and metaphors from sources
- Concept origins or disciplinary placement
- Distinctions learned
- Knowledge that deserves review even without cognitive change

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

### Review Queue

Tracks future recall prompts and interval guidance.

Use for:

- Knowledge recall prompts
- Source recall prompts
- Distinction recall prompts
- Application recall prompts
- Recall strength
- Suggested next review interval

## Memory Candidate Format

Use this format when a session may produce a memory:

```text
Topic:

Memory Type:

Knowledge Gain:

Cognitive Gain:

Before:

After:

Trigger:

Open Question:

Practice or Review:

Review Prompts:

Recall Strength:

Review Interval:

Save Recommendation:
```

Fields may be omitted if not relevant.

Do not force every candidate into every field.

If `Cognitive Gain` is not visible, write:

```text
Cognitive Gain:
No clear cognitive shift yet.
```

Then prefer `Knowledge History`, `Concept History`, or `Review Queue`.

## Effective Feedback Candidate Format

Use this format for end-of-session feedback:

```text
Topic:

Knowledge Gain:
- 

Cognitive Gain:
- 

Worth Saving:
- Memory Type:
- Save Target:
- Why it matters:

Review Queue:
- Recall Prompt:
- Recall Type:
- Recall Strength:
- Suggested Interval:

Future Use:
- 
```

Keep it concise.

A useful feedback item should tell the learner what was learned, what changed if anything, where it can be saved, how it can be reviewed, and why it may matter later.

## Review Prompts

Memory candidates may include review prompts when the material is worth retaining.

Review prompts should test understanding rather than wording.

Useful prompt types:

- Recall the source.
- Explain the concept simply.
- Give a real-life example.
- Distinguish it from a nearby concept.
- Explain how it changed the learner's view of a familiar phenomenon.

Example:

```text
Review Prompts:
- Explain emergence to a smart 12-year-old.
- Give one everyday example of emergence.
- How is emergence similar to and different from dependent origination?
- What did the "self as smoke" image help clarify?
```

Review prompts can support future Active Recall, Spaced Repetition, Concept History, or monthly review.

## Recall Strength And Review Interval

Use this lightweight scale for Review Queue items:

```text
0 = not remembered
1 = vaguely remembered
2 = basically clear
3 = clear and can give an example or application
```

Suggested intervals:

```text
0 -> 1 day
1 -> 3 days
2 -> 7 days
3 -> 14-30 days
```

The interval is guidance, not an automated reminder.

Hunter Learning OS should use the Review Queue when the learner asks to review recent learning.

## Private Memory Store

Personal Memory should default to a private local directory, not the public skill repository.

Default path:

```text
/Users/tianyuan/Documents/工作系统/memory/hunter-learning-os/
```

Suggested files:

- `knowledge-history.md`
- `cognitive-change-history.md`
- `review-queue.md`
- `session-index.md`

The public skill repository should contain system rules and templates, not personal learning records.

## Memory Future Use

When generating a Memory candidate, briefly indicate how it may be used later:

- recall
- review
- synthesis
- application
- monthly reflection

Do not make every Memory candidate long.

Use future-use notes only when they add practical value.

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

- The learner clarified a source point or concept worth retaining.
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

Do not create a Cognitive Change candidate when the session produced only knowledge clarification.

In that case, create Knowledge History or Review Queue candidates if useful.

## Save Rules

Before saving personal Memory, ask for confirmation.

Good confirmation language:

```text
This feels like a possible Memory item.
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
