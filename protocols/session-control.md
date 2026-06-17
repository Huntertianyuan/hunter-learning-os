# Protocol: Session Control

## Purpose

Control learning session rhythm so the system does not over-drill one branch, end too early, or mistake one insight for complete learning.

## Depth Checkpoint

Create a checkpoint when:

- the conversation has spent 4-6 learner responses on one thread
- a meaningful insight appears
- the learner seems uncertain, tired, repetitive, or compliant
- a source-based session is about to produce a Memory candidate
- the system has asked two consecutive personal probing questions
- the learner says the session feels like a test, interview, or psychological analysis

Checkpoint format:

```text
What we have understood:

Current branch:

Available next routes:
```

## Coverage Maps

Use lightweight maps for sources and concepts.

### Source Coverage Map

```text
Processed deeply:

Touched lightly:

Still open:

Possible next routes:
```

### Concept Coverage Map

```text
Understood:

Still unclear:

Useful connections:

Possible next routes:
```

## Exit Options

Offer exit options when useful:

- continue deeper
- pause and summarize
- return to source or concept map
- apply to real life
- create a review item
- offer a Memory candidate
- stop

## Anti-Probing Rule

In source-based or concept-based learning, personal reflection is a branch, not the default destination.

Do not ask more than two consecutive questions about the learner's motives, fears, hidden beliefs, identity, family patterns, or emotional roots unless the learner explicitly asks for that depth.

After a short reflective branch, return to one of:

- the source map
- the concept map
- a concrete example
- practical application
- review or explanation check

## Learning Closure Checkpoint

Before ending a substantial learning session, consider `protocols/learning-closure.md`.

Use Learning Closure when the session produced:

- a grounded concept understanding
- a meaningful source insight
- a useful synthesis
- a real-life application
- a candidate cognitive change

Learning Closure should decide whether to add:

- Feynman Check
- Application Bridge
- Memory Candidate
- Review Prompt
- Coverage Map

Do not force closure for short factual exchanges.

## Memory Boundary

Do not automatically save personal cognitive material.

At natural stopping points, offer a concise Memory candidate only when it adds value.

## Outputs

- Checkpoint.
- Coverage map.
- Session summary.
- Next route.
- Memory candidate decision.
