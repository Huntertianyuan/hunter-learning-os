# Hunter Learning OS

Vision & Architecture Specification v0.1

## 1. Vision

Hunter Learning OS is a personal cognitive operating system.

It is designed to help a learner transform information into understanding, understanding into insight, and insight into long-term cognitive growth.

The system is not primarily a reading assistant, note-taking tool, or study planner.

Its purpose is to support lifelong learning and cognitive development.

## 2. Mission

Most people consume information.

Few people internalize it.

Hunter Learning OS exists to help users:

- Understand deeply
- Remember effectively
- Connect ideas across domains
- Apply knowledge to real life
- Track cognitive growth over time

The goal is not knowledge accumulation.

The goal is cognitive transformation.

## 3. Success Criteria

The system should help the user progress through five levels:

### Level 1: Understanding

Can explain an idea clearly.

### Level 2: Connection

Can connect an idea to previous knowledge.

### Level 3: Application

Can apply an idea in real situations.

### Level 4: Transformation

Mental models change.

The user begins to think differently.

### Level 5: Identity Integration

The idea becomes part of how the user naturally thinks and acts.

## 4. Core Design Principles

### Principle 1: Active Learning

Learning is not passive consumption.

The system should continuously ask questions, challenge assumptions, test understanding, and provoke reflection.

### Principle 2: Depth Over Coverage

Deep understanding of one chapter is preferable to superficial exposure to ten chapters.

### Principle 3: User Thinking Over Source Material

Books, articles, courses, podcasts, and videos are inputs.

The user's evolving understanding is the primary focus.

### Principle 4: Modular Learning

Methods should be reusable.

Skills should be stable workflows.

The system should separate:

- What to do
- How to do it

### Principle 5: Memory First

The user's cognitive history is the most valuable asset in the system.

The system should remember:

- What the user learned
- What the user misunderstood
- What changed over time

## 5. System Architecture

Hunter Learning OS consists of five layers.

```text
Learning OS
|-- Router
|-- Protocols
|-- Skills
|-- Methods
`-- Memory
```

## 6. Router Layer

Purpose:

Coordinate learning activity.

Router does not teach.

Router does not explain.

Router decides:

- Which entry type the request belongs to
- Which Protocols should govern the session
- Which Skill to activate
- Which Methods to invoke
- Which Memory to retrieve
- Which Memory to update

Router acts as the learning coordinator.

## 7. Protocols Layer

Purpose:

Define system-level operating rules for common learning situations.

Protocols are not Skills.

Protocols are not Methods.

They do not teach by themselves.

They specify how a learning route should be grounded and controlled before and during Skill execution.

Current V1 Protocols:

### Source Grounding

Purpose:

Ground named books, chapters, articles, videos, notes, or reading traces before interpretation.

### Knowledge Grounding

Purpose:

Orient unfamiliar concepts, recommend concepts for discovery, and ground trend scans with external sources when needed.

### Learner Articulation

Purpose:

Keep the learner actively producing understanding without forcing empty repetition.

### Session Control

Purpose:

Manage depth checkpoints, coverage maps, exits, and Memory candidate timing.

### Learning Closure

Purpose:

Close meaningful sessions with explanation checks, application bridges, Memory candidates, review prompts, or coverage maps.

Layer responsibilities:

```text
Router = choose route
Protocol = route rules
Skill = learning workflow
Method = cognitive operation
Memory = long-term cognitive record
```

## 8. Skills Layer

Skills are user-facing learning workflows.

The number of skills should remain small and stable.

Current V1 Skills:

### Deep Dive

Purpose:

Achieve deep understanding of a concept, idea, chapter, argument, or problem.

### Review

Purpose:

Strengthen memory, retention, and recall.

### Synthesis

Purpose:

Connect ideas across books, disciplines, and domains.

### Application

Purpose:

Translate knowledge into real-world decisions and behavior.

### Reflection

Purpose:

Track cognitive growth, mental model changes, and learning progress.

## 9. Methods Layer

Methods are reusable cognitive algorithms.

Methods are not workflows.

Methods are tools used by Skills.

A Skill may invoke multiple Methods.

Example:

Deep Dive may invoke:

- Feynman
- Socratic Questioning
- Analogy
- Distinction

Methods are organized into categories.

### Input Methods

Purpose:

Acquire knowledge effectively.

Examples:

- Active Reading
- Question-Driven Learning
- SQ3R

### Understanding Methods

Purpose:

Build deep comprehension.

Examples:

- Feynman Technique
- Socratic Questioning
- Analogy
- Distinction
- Counterexample

### Knowledge Organization Methods

Purpose:

Create structure.

Examples:

- Zettelkasten
- Concept Mapping
- Progressive Summarization

### Memory Methods

Purpose:

Improve retention.

Examples:

- Active Recall
- Spaced Repetition
- Interleaving
- Retrieval Practice

### Application Methods

Purpose:

Transfer knowledge into practice.

Examples:

- Transfer
- Scenario Testing
- Case Application

### Reflection Methods

Purpose:

Improve self-awareness.

Examples:

- Metacognition
- Reflective Journaling
- Double Loop Learning
- After Action Review

### Creation Methods

Purpose:

Generate insight and new ideas.

Examples:

- First Principles
- Inversion
- Synthesis

## 10. Memory Layer

Memory is a first-class system component.

The competitive advantage of the system is not its methods.

Modern AI systems can all perform Feynman explanations and Socratic questioning.

The unique asset is the user's cognitive history.

Memory should capture:

### Reading History

What was read.

When it was read.

### Concept History

Concepts encountered.

Concepts mastered.

Concepts still unclear.

### Misconception History

Previous misunderstandings.

Corrections.

Evolution of understanding.

### Cognitive Profile

Current interests.

Current strengths.

Current weaknesses.

Recurring themes.

Learning patterns.

### Idea Network

Connections between concepts.

Connections across books.

Connections across disciplines.

## 11. Cognitive Profile

The system should maintain a continuously evolving model of the learner.

Possible fields:

- Interests
- Frequently revisited concepts
- Persistent misconceptions
- Strong domains
- Weak domains
- Preferred learning styles
- Cognitive growth milestones

The profile should evolve continuously.

## 12. Example Learning Flow

User:

> What is impermanence?

Router:

Determine goal:

Understanding

Skill:

Deep Dive

Methods:

- Feynman
- Analogy
- Socratic Questioning

Memory:

Retrieve:

- Previous discussions about impermanence
- Related concepts

After completion:

Update:

- Concept History
- Cognitive Profile

## 13. What This System Is NOT

This system is not:

- A note-taking application
- A flashcard application
- A reading tracker
- A productivity system
- A generic chatbot

It is a cognitive growth system.

## 14. Long-Term Vision

The system should eventually become a personal learning partner that understands:

- What the user knows
- What the user misunderstands
- How the user thinks
- How the user's thinking changes over time

The final goal is not knowledge acquisition.

The final goal is cognitive transformation.

## 15. Current Development Stage

Current focus:

Phase 1

Vision and Architecture

Next phase:

Methods Specification

Future phases:

- Skills Specification
- Router Specification
- Memory Specification
- Implementation for Codex/Hermes

Status:

Version 0.1

Architecture under active design.
