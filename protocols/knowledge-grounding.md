# Protocol: Knowledge Grounding

## Purpose

Provide reliable knowledge orientation before deeper learning when the learner brings an unfamiliar concept, asks for concept recommendations, or asks what is currently trending.

Knowledge Grounding is not a Skill and not a Method.

It prepares the ground for Skills such as Deep Dive, Synthesis, Review, or Application.

## Modes

### Known Target

Use when the learner names a concept, theory, model, field, person, or technical term.

Examples:

- "What is cellular automata?"
- "I know nothing about game theory."
- "What does predictive processing mean?"

Default concept map:

- What it is
- What it is not
- Field or discipline
- Origin or key figures, if relevant
- Core mechanism
- Canonical example
- Why it matters
- Real-world applications
- Common misconceptions or boundaries
- Good next questions

### Discovery

Use when the learner wants a worthwhile concept but does not name one.

Examples:

- "Recommend a concept for me to learn."
- "I want to learn something new."
- "Give me a concept connected to what we have been discussing."

Default behavior:

- Recommend 3-5 concepts.
- Base suggestions on Learning Profile, recent learning context, and long-term themes.
- Do not claim a concept is currently trending unless external sources were checked.
- For each concept, include:
  - concept name
  - one-line meaning
  - why it is worth learning
  - likely next Skill path

### Trend Scan

Use when the learner asks what is current, popular, new, or trending.

Examples:

- "What AI concepts are hot right now?"
- "What are the current popular psychology concepts?"
- "What should I know about recent AI?"

Trend Scan requires external sources because current popularity is time-sensitive.

Default behavior:

- Search current external sources.
- Prefer primary or authoritative sources when possible.
- Group concepts by domain when useful.
- Distinguish trend signal from long-term importance.
- Provide source links or clear source attribution.

## External Source Policy

Default: use external sources on demand.

Internal knowledge is acceptable for stable basic orientation when it is enough to begin learning.

Prefer external sources when discussing:

- history
- originators
- disciplinary placement
- canonical examples
- professional or technical details

Require external sources when:

- the learner asks for citations or sources
- the topic is current, trending, recent, or time-sensitive
- the topic is disputed
- the topic is high-risk
- the system is uncertain

## Transition To Learning

Knowledge acquisition should not end as encyclopedia output.

After orientation, route to the next learning move:

- Deep Dive: understand mechanism or boundaries.
- Synthesis: connect the concept to other domains.
- Application: use the concept in a real context.
- Review: retain the concept.
- Reflection: notice whether the concept changes the learner's mental model.

Useful transition questions:

- What does this concept explain that you previously found confusing?
- Which part of the concept feels most useful or questionable?
- Does this concept change how you think about a familiar phenomenon?

## Outputs

- Concept map or concept recommendation set.
- External source status.
- Reliability note when useful.
- Next Skill path.
- Candidate Concept History or Idea Network update.
