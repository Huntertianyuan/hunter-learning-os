# Skill: Deep Dive

## Purpose

Help the learner deeply understand a concept, chapter, argument, question, or problem.

Deep Dive is for moving from surface familiarity to clear, testable understanding. It can operate in three modes:

- Concept Mode: understand one concept or distinction.
- Source Mode: understand a chapter, article, passage, video, or argument.
- Discussion Mode: discuss a source or idea after the learner has already engaged with it.

## When to Use

- The user says they do not understand something.
- The user wants to discuss a chapter, article, video, concept, or argument.
- The user asks a "why", "what does this mean", or "what is the difference" question.
- The user needs conceptual clarity before review, synthesis, application, or reflection.
- The user has reading traces or notes that show unresolved questions.

## When NOT to Use

- The user's primary goal is memorization and the concept is already understood.
- The user mainly wants to apply an idea to a real decision or action.
- The user wants to compare multiple sources or domains.
- The user is primarily reflecting on their own cognitive change rather than understanding the source.
- The source has not been grounded enough for source-specific claims.

## Default Method Sequence

1. `question-driven-learning`: identify the live question or learning focus.
2. `progressive-summarization`: establish the core source or concept structure when source material is involved.
3. `distinction`: separate concepts that are being mixed together.
4. `feynman-technique`: test whether the learner can explain the idea simply.
5. `socratic-questioning`: examine assumptions, reasoning, and implications.
6. `misconception-detection`: detect and repair misunderstandings.
7. `progressive-summarization`: close with a compact understanding.

## Source And Discussion Mode Rules

When Deep Dive is used for a chapter, article, lecture, video, or other source, it should balance depth with coverage.

### Source Mode

Use when the learner wants to understand the source itself.

Default rhythm:

1. Establish or infer a lightweight source map.
2. Identify the learner's live question or point of friction.
3. Connect the learner's words back to one relevant source point.
4. Add a compact conceptual scaffold.
5. Invite the learner to restate, test, or extend the idea.
6. After 4-6 learner responses on one branch, create a depth checkpoint.
7. End with both a compact understanding and a coverage map when useful.

### Discussion Mode

Use when the learner has read or watched the source and wants open discussion.

The system should not assume open discussion means unlimited deep drilling into the first topic.

Default rhythm:

1. Start from what the learner naturally brings up.
2. Deepen that thread enough to produce clearer understanding.
3. Add short source, concept, or tradition-level scaffolding as the discussion unfolds.
4. Create a checkpoint when one insight has emerged.
5. Offer to continue the current thread or return to the wider source.

### Depth Versus Coverage

One successful insight does not mean the whole source has been internalized.

When discussing a source, Deep Dive should track:

- Processed deeply
- Touched lightly
- Still open
- Possible next routes

This should be brief and used as a navigation aid, not as a full summary.

## Concept Mode Rules

Use Concept Mode when the learner wants to understand a concept, theory, model, or technical term.

If the learner is completely new to the concept, begin with orientation before testing articulation.

### Novice Concept Orientation

Minimum orientation:

1. Plain definition: what the concept means.
2. Field: which discipline or area uses it.
3. Origin: who introduced or popularized it, if relevant.
4. Core mechanism: how it works.
5. Importance: why anyone cares.
6. Concrete example: one simple case.
7. Boundaries: what it is not.

After orientation, ask a question that requires application, comparison, or boundary testing.

Avoid asking the learner to merely repeat the previous explanation.

### Concept Mode Rhythm

Default rhythm for a new concept:

```text
Orient
-> Give one concrete example
-> Check for the learner's real point of confusion
-> Deepen through analogy, distinction, or counterexample
-> Ask the learner to apply the concept to a new case
-> Summarize the concept in the learner's words
```

Use Feynman Technique only after the learner has enough material to explain something in their own words.

## Optional Method Add-ons

- `analogy`: when the idea is abstract and needs a familiar structure.
- `counterexample`: when a claim needs boundary testing.
- `concept-mapping`: when several concepts must be related.
- `first-principles`: when the user needs foundational rebuilding.
- `metacognition`: when the discussion reveals the user's own thinking pattern.
- `practice-design`: when the understanding should become a small real-life observation or exercise.

## Memory Outputs

- Updated Concept History.
- Misconception History entries when misunderstanding is corrected.
- Open questions that remain alive.
- Candidate Cognitive Change History when the user's understanding shifts.
- Useful explanations, distinctions, or analogies for future review.
- Source coverage maps for chapter, article, lecture, or video sessions.

## Exit Conditions

- The user can explain the concept or argument in their own words.
- The user's original question has a clear answer or a better follow-up question.
- A misconception has been identified and repaired.
- The discussion reaches a natural landing point and should shift to Review, Application, or Reflection.
- A depth checkpoint shows the learner wants to pause, shift, or return to source coverage.
- The user chooses to pause, summarize, or stop.

## Example Scenarios

- "I do not understand what emptiness means."
- "What is the difference between emptiness and no-self?"
- "I just read Chapter 8 and want to discuss it."
- "This video mentioned Nash equilibrium, but I do not understand it."
- "The author says material abundance does not create happiness. Why do people still pursue material things?"
