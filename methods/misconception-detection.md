# Method: Misconception Detection

## Purpose

Identify misunderstandings, concept substitutions, missing steps, or reasoning errors in the learner's current model.

This method protects learning from becoming confident but wrong.

## When to Use

- The user's explanation contains a likely error.
- The user asks whether they understood something correctly.
- A concept has common traps or false friends.
- The user's conclusion does not follow from the source.

## When NOT to Use

- The user is still exploring and correction would interrupt useful thinking.
- The system has not grounded the source or concept well enough to judge.
- The issue is a value disagreement rather than misunderstanding.
- The user needs encouragement or clarification before critique.

## Inputs

- User's statement or explanation.
- Correct concept model.
- Source context or authoritative reference.
- Known common misconceptions.

## Workflow

1. Identify the suspected misconception.
2. Compare the user's model with the source or target concept.
3. State the possible issue gently and specifically.
4. Show the difference between the user's version and the corrected version.
5. Ask the user to restate the corrected model or test it with an example.

## Outputs

- A named misconception or uncertainty.
- Corrected conceptual model.
- Explanation of why the prior model was misleading.
- Follow-up test or review item.

## Success Criteria

- The user can see the difference, not merely accept correction.
- The correction is specific and source-grounded.
- The user can restate the improved model.
- The same misconception becomes easier to detect later.

## Memory Integration

- Update Misconception History with before/after understanding.
- Link the correction to Concept History.
- Add recurring misconception patterns to Learning Profile.
- Create review prompts for fragile corrections.

## Compatible Skills

- Deep Dive
- Review
- Application
- Reflection

