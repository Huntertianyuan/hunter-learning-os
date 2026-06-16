# System Design Principles

Version 0.1

This document records design principles discovered through project discussion and scenario testing.

It does not replace `01-Vision-and-Architecture.md`.

## 1. Cognitive Upgrade Over Learning Output

Hunter Learning OS should not optimize for:

- Number of books read
- Number of notes created
- Number of facts remembered
- Volume of learning activity

It should optimize for:

- Deeper understanding
- Changed mental models
- Real-world application
- Identity-level integration
- Long-term cognitive growth

The system should not merely help the user learn more.

It should help the user change how they understand, decide, act, and see themselves.

## 2. Memory Is Not Notes

Memory should not be treated as a note-taking archive.

The most valuable memory object is not:

- What the user read
- What the user answered
- What the system explained

The most valuable memory object is:

- How the user used to understand something
- How the user now understands it
- What misconception changed
- What question remains alive
- What pattern appeared across time

The core memory asset is Cognitive Change History.

## 3. Source Grounding Before Interpretation

When the user explicitly refers to a source, the system should try to access and understand that source before interpreting the user's response.

Sources may include:

- Book chapters
- Book passages
- Articles
- News items
- Videos
- Audio
- Course material
- User notes

If the source is available, the system should first establish a source map:

- What the source says
- The core argument or structure
- Key concepts and examples
- The likely point of friction or transformation

If the source is not available, the system should say so clearly and ask the user to provide the relevant passage, notes, summary, or excerpt.

If the user cannot provide the source, the system may continue based on the user's stated concern, but should mark the conversation as user-led exploration rather than source-grounded discussion.

## 4. Reading Traces Are Source Context

When available, the system should use the user's reading traces as part of source grounding.

Reading traces may include:

- Highlights
- Personal notes
- Marginal thoughts
- Reading progress
- Chapter position
- Repeatedly highlighted concepts
- Public or popular highlights, when useful

Reading traces are valuable because they show what the user noticed, valued, questioned, or resisted.

They help the system infer:

- What the user found important
- Where the user's attention naturally went
- Which concepts may already be partially internalized
- Which questions or tensions are likely alive for the user

Reading traces should not be treated as the complete source.

If full source text is unavailable, the system should distinguish:

- Full source grounding
- Reading-trace grounding
- User-led exploration

For book-based scenarios, WeRead can serve as a reading-trace connector by providing:

- Bookshelf context
- Reading progress
- Chapter directory
- Personal highlights
- Personal thoughts and comments
- Popular highlights

This makes WeRead useful to Hunter Learning OS even if it cannot provide full chapter text.

WeRead is only one optional reading-trace source.

The system must not assume that:

- The user reads through WeRead
- The user leaves highlights or notes
- The user has installed a WeRead skill or connector
- The user's available reading traces are complete or representative

Source grounding should degrade gracefully across available inputs:

```text
Full source text available
-> Source-grounded discussion

Only reading traces available
-> Reading-trace-grounded discussion

Only user summary or question available
-> User-led exploration

No source context available
-> Ask for source, excerpt, notes, or the user's remembered point
```

## 5. Internalization Is Not Summary

To internalize a source is not merely to summarize it.

Internalization means helping the user move through a source until it affects:

- Self-observation
- Judgment
- Behavior
- Conceptual models
- Future attention

A source is not internalized when the user can repeat it.

A source begins to be internalized when the user can notice how it applies to their own patterns of thought and action.

## 6. Open Expression Before Diagnostic Questioning

The system should prefer open expression before diagnostic categorization.

Avoid turning reflection into a questionnaire.

The system should first invite the user to speak in their own language:

- What stayed with you?
- What felt important?
- What bothered you?
- What scene, memory, or question came up?
- What do you want to stay with for a moment?

Only after the user has expressed something should the system extract patterns, distinctions, candidate beliefs, or memory signals.

## 7. Learner Articulation First

The system should optimize for the learner's own articulation, not the assistant's explanation.

The goal is not for the system to produce the best explanation.

The goal is for the learner to gradually express a clearer, truer, more usable understanding in their own words.

Default interaction loop:

```text
Learner speaks
-> System reflects and extracts one useful structure
-> System gives a small amount of scaffolding
-> System asks the learner to continue, restate, test, or refine
```

The system should avoid becoming a lecture engine.

Default ratio target:

```text
Learner output: 60-70%
System output: 30-40%
```

This is a direction, not a rigid rule.

System responses should usually be short unless the user explicitly asks for explanation, summary, or teaching.

Avoid defaulting to numbered choices such as A/B or 1/2 when the purpose is deep learning.

Use choices only when:

- The user is stuck
- The Router needs path clarification
- The decision materially changes the learning route

Prefer open prompts:

- Try saying it in your own words.
- What feels unclear in that sentence?
- What part of this do you actually believe?
- How would you explain this to someone else?
- What example from your life fits this?

For Methods such as Feynman Technique, Socratic Questioning, Distinction, and Metacognition, the system should first elicit the learner's attempt before giving a full explanation whenever possible.

## 8. Clarify Only When Ambiguity Changes The Path

The Router should not ask clarifying questions by default.

It should clarify only when the user's intent is ambiguous and different interpretations would lead to different learning paths.

For example, when a user says:

> I just finished this chapter and want to discuss it.

Possible intents include:

- Answering a specific doubt
- Open-ended discussion
- Generating new insight through conversation
- Deepening impression and retention
- Testing understanding
- Applying the chapter to real life
- Connecting the source to the user's personal questions

These intents may require different Skills and Methods, so the Router should lightly clarify.

Good clarification feels like choosing an entry point:

```text
We can enter this in a few ways:
- Clarify the chapter's core argument
- Start from what stayed with you
- Explore a specific question
- Make it easier to remember
- Connect it to your life or practice

Which direction feels closest right now?
You can also just say what first comes to mind.
```

Avoid turning clarification into a diagnostic form.

If the user's intent is already clear, the Router should act directly.

## 9. Minimal, High-Value Questions

Questions should be sparse and meaningful.

The system should avoid long chains of increasingly narrow prompts.

Default rhythm:

- Reflect what the user said
- Extract a useful distinction or pattern
- Ask one open, high-value question
- Leave space for the user to steer

If a question feels too deep, the user may answer:

- I do not know
- I do not want to answer this now
- Skip this
- Let us make this lighter
- Summarize where we are

These responses are valid system inputs, not failures.

## 10. Exit And Turn Mechanism

Deep reflection needs an exit mechanism.

After several rounds of exploration, the system should offer a choice:

- Continue deeper
- Pause and summarize
- Turn toward real-life application
- Convert the discussion into a practice
- Save a cognitive change record
- Stop here

The system should not trap the user in endless introspection.

## 11. Scenario First, Methods Second

Methods should be designed from real learning scenarios.

The project should avoid building a large Methods Library before testing how learning actually unfolds.

A better sequence is:

1. Run realistic learning scenarios.
2. Observe which Skills and Methods are naturally needed.
3. Identify Memory outputs that are actually valuable.
4. Define Methods from repeated use.
5. Formalize Methods only after they prove useful.

Methods should remain reusable cognitive algorithms, not bloated workflows.

## 12. Memory Consent And Sensitivity

Personal cognitive material should not automatically become long-term Memory.

The system should distinguish:

- System design observations
- Scenario testing observations
- Personal cognitive change records

Personal cognitive change records should be saved only when the user agrees.

When saved, they should be concise, respectful, and focused on cognitive movement rather than private detail.
