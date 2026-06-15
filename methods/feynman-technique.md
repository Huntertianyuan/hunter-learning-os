# Method: Feynman Technique

## Purpose

Test and strengthen understanding by asking the learner to explain an idea in simple, clear language.

This method exposes vague comprehension, hidden jargon, and places where the learner can recognize a term without truly understanding it.

## When to Use

- The user says they understand something but cannot explain it clearly.
- The system needs to test whether a concept has been internalized.
- The concept is abstract, technical, philosophical, or easily confused.
- The user wants to prepare to teach, speak, write, or apply the idea.

## When NOT to Use

- The user is still missing basic source context.
- The user wants emotional reflection rather than conceptual explanation.
- The idea is too early or fragile and forcing explanation would create frustration.
- A distinction or analogy is needed before explanation can become meaningful.

## Inputs

- Target concept.
- User's current explanation, if available.
- Source context or examples.
- Known misconceptions.

## Workflow

1. Ask the user to explain the concept as if speaking to a smart beginner.
2. Detect vague words, circular definitions, unexplained jargon, and skipped steps.
3. Ask for clarification at the weakest point.
4. Offer a simple version only after the user's attempt reveals the gap.
5. Ask the user to restate the improved version in their own words.
6. Optionally test the explanation with an example or counterexample.

## Outputs

- A plain-language explanation.
- Identified understanding gaps.
- A refined explanation in the user's own words.
- Candidate misconception records.

## Success Criteria

- The user can explain the idea without hiding behind jargon.
- The explanation is simple but not distorted.
- The user sees where their earlier understanding was incomplete.
- The explanation can survive at least one example or counterexample.

## Memory Integration

- Update Concept History with the user's current explanation.
- Update Misconception History when a gap is found and corrected.
- Save improved explanations as memory anchors for review.
- Track concepts that repeatedly fail Feynman testing.

## Compatible Skills

- Deep Dive
- Review
- Application
- Reflection

