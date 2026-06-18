# Skill: Review

## Purpose

Strengthen retention, recall, and retrieval of important learning.

Review is for making understanding durable. It turns a concept, chapter, article, or prior discussion into recallable memory.

Review can strengthen both knowledge and cognitive change.

If a prior session produced knowledge without visible cognitive shift, review should focus on recalling the knowledge, source, distinctions, and examples.

## When to Use

- The user says they want to remember something.
- The user asks for review, recall practice, or spaced repetition.
- The user has already understood the material well enough to be tested.
- A prior discussion produced insights worth retaining.
- The user wants to check what they still remember.
- Another Skill creates review prompts through Learning Closure.

## When NOT to Use

- The user has not yet understood the material.
- The user is asking for deep conceptual clarification.
- The user wants real-world application more than retention.
- The material is not important enough to preserve.
- The user wants open reflection rather than recall.

## Default Method Sequence

1. `progressive-summarization`: compress the material into reviewable units.
2. `active-recall`: ask the user to retrieve the core ideas without looking.
3. `misconception-detection`: identify distorted or missing recall.
4. `spaced-repetition`: suggest future review timing for important items.
5. `interleaving`: mix related concepts when discrimination matters.

## Knowledge Review Types

Use these recall types for knowledge-oriented review:

- Source recall: where the idea came from.
- Content recall: what the idea means.
- Distinction recall: how it differs from nearby ideas.
- Application recall: how it appears in real life.

Examples:

```text
Source recall:
Where did we encounter the dirty window metaphor?

Content recall:
Can you describe the dirty window metaphor simply?

Distinction recall:
Is the dirty window exactly the same as habitual tendency, or is habitual tendency one kind of dirt?

Application recall:
Can you name one situation where a normal person looked like a threat through a dirty window?
```

## Recall Strength

Score recall lightly after the learner answers:

```text
0 = not remembered
1 = vaguely remembered
2 = basically clear
3 = clear and can give an example or application
```

Suggested interval:

```text
0 -> 1 day
1 -> 3 days
2 -> 7 days
3 -> 14-30 days
```

If recall is weak, give a compact scaffold and shorten the review interval.

If recall is strong, ask a harder distinction or application question and lengthen the interval.

## Optional Method Add-ons

- `feynman-technique`: when recall should be tested through explanation.
- `concept-mapping`: when the material is structural or relational.
- `distinction`: when similar concepts are easily confused.
- `practice-design`: when retention should be reinforced through a real-life observation or task.

## Review Handoff

Other Skills may create lightweight review prompts without switching into a full Review session.

Use this when a concept, insight, or synthesis is worth revisiting later.

Review handoff format:

```text
Review Prompts:
- Explain the concept simply.
- Give one real-life example.
- Distinguish it from a nearby idea.

Recall Strength:
Not yet tested.

Suggested Interval:
Initial review in 1-3 days if important.
```

If the user asks to review now, run the full Review Skill.

If the user asks to remember later, suggest a small spaced repetition schedule.

If the user asks to review recent learning, prefer the Review Queue over inventing new questions from memory.

## Memory Outputs

- Review prompts.
- Recall strength notes.
- Items needing spaced repetition.
- Concepts that are remembered, forgotten, or distorted.
- Misconception History entries when recall reveals confusion.

## Exit Conditions

- The user can recall the core ideas accurately enough for the current goal.
- Weak recall points are identified and scheduled for review.
- The review set becomes too large and must be narrowed.
- The user shifts from remembering to wanting deeper understanding or application.

## Example Scenarios

- "I want to remember this chapter."
- "Quiz me on what we discussed yesterday."
- "Help me review the key ideas from this article."
- "I keep forgetting Python syntax."
- "Can we make this into review questions?"
