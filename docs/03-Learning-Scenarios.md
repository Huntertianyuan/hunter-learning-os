# Learning Scenarios

Version 0.1

This document records scenario-first testing for Hunter Learning OS.

The purpose of scenario testing is to validate whether Router, Skills, Methods, and Memory can work together in realistic learning situations.

## 1. Scenario-First Design

Hunter Learning OS should be tested through real user learning moments before its Methods Library is finalized.

Each scenario should observe:

- What the user is really asking for
- Which Skill should be activated
- Which Methods are naturally needed
- What source context must be retrieved
- What kind of Memory would be valuable
- Where the interaction feels useful or uncomfortable
- Whether a cognitive change actually occurred

## 2. Priority Scenario Types

Initial scenario types:

- Reading and discussing a chapter from a contemplative or philosophical book
- Reading and discussing an English literary text
- Understanding a difficult concept
- Applying a concept to daily life or work
- Learning AI, Python, or another technical skill
- Reviewing a previously discussed idea after time has passed

## 3. Scenario Test Template

Each scenario test should record:

### Scenario

What the user asked for.

### Source Context

Whether a source was named, whether it was available, and how it was grounded.

### Router Judgment

The user's likely learning intent.

### Skill Selection

The Skill or combination of Skills used.

### Methods Used

The Methods that were actually useful.

### Interaction Observations

What felt natural, useful, too narrow, too fast, or uncomfortable.

### Memory Candidate

What could be saved, if the user consents.

### Design Implication

What the system should change or preserve.

## 4. Scenario Test 001

### Scenario

The user said:

> I just finished Chapter 8, "Why Are We Unhappy?", from *The Joy of Living*, and I want to discuss it.

### Source Context

The user had placed the EPUB file in:

`/Users/tianyuan/Documents/Codex工作台/学习系统/books/`

The system located the book and confirmed that Chapter 8 maps to `index_split_008.html` inside the EPUB.

The chapter was source-grounded before restarting the discussion.

Future runs of this scenario may also use WeRead reading traces if the user read the chapter in WeRead.

WeRead can provide:

- Whether the book is on the user's shelf
- Reading progress
- Personal highlights from the book
- Personal thoughts and comments
- Popular highlights
- Chapter directory and chapter identifiers

These traces help the system understand what the user noticed and valued.

They do not replace full chapter text.

If the EPUB or full text is unavailable but WeRead traces are available, the scenario should be marked as reading-trace grounded.

WeRead must remain optional.

Some users do not read through WeRead.

Some users read through WeRead but leave no highlights or thoughts.

Some users leave traces but do not install or authorize the WeRead skill.

The scenario should therefore support a graceful grounding ladder:

```text
Full text + reading traces
-> Best grounding

Full text only
-> Source-grounded

Reading traces only
-> Reading-trace-grounded

User notes or summary only
-> User-led with explicit limitation

No source, traces, or notes
-> Ask for a passage, summary, remembered point, or desired discussion direction
```

### Chapter Map

The chapter's central movement:

```text
Material abundance does not guarantee happiness
-> People chase new stimulation
-> Stimulation fades
-> People misidentify external objects as stable sources of happiness
-> Emotional and neural conditioning reinforce reactive patterns
-> Buddhism describes these patterns as kleshas: ignorance, attachment, aversion
-> The way forward is to recognize and settle the mind
```

Important chapter concepts:

- External stimulation fades.
- The mind confuses temporary pleasure with lasting happiness.
- Emotional reactions are shaped by body, brain, and conditioning.
- Temporary emotional states can become stable traits.
- Ignorance creates the sense of a separate, vulnerable self.
- Attachment turns external objects into imagined sources of completion.
- Aversion resists change and intensifies fear.
- Afflictive emotions can become opportunities for observing the mind.

### Router Judgment

The user was not asking for a simple summary.

However, the initial phrasing was still underspecified:

> I just finished Chapter 8 and want to discuss it.

This could mean:

- I have a specific question.
- I want to casually discuss the chapter and see what comes up.
- I want the system's response to spark new insight.
- I want to deepen my impression and remember the chapter.
- I want to connect the chapter to my own life.
- I want to test whether I understood it.

Because these paths lead to different Skills and Methods, the Router should lightly clarify the user's preferred entry point before going deep.

A better first response after source grounding:

```text
I have the chapter map now. We can enter it in a few ways:
- Clarify the chapter's core argument
- Start from the part that stayed with you
- Explore a specific question you have
- Make the chapter easier to remember
- Connect it to your real life or practice

Which direction feels closest right now?
You can also just say what first comes to mind.
```

If the user chooses open discussion, the likely intent becomes:

- Discuss the chapter
- Identify what touched the user
- Understand the chapter's relevance to personal life
- Move from reading comprehension toward internalization

### Skill Selection

Primary Skill:

- Deep Dive

Secondary Skill:

- Reflection

Potential later Skill:

- Application

### Methods Used Or Needed

Methods that appeared necessary:

- Source Grounding
- Reading Trace Grounding
- Chapter Mapping
- Open Reflection
- Self-Connection
- Socratic Questioning
- Distinction
- Cognitive Change Capture
- Exit And Turn

### Initial Failure

The system first responded without confirming the chapter's content.

It used the user's stated point as the entry and began a useful but insufficiently source-grounded discussion.

### Correction

When a user names a specific source, the system should first attempt to access and understand the source.

If the source cannot be accessed, the system should ask the user to provide:

- A passage
- Notes
- A summary
- The key point they want to discuss

Only then should the system continue based on the user's own material.

### Interaction Observation

The discussion surfaced a second issue:

Repeated diagnostic questions can make the user feel like they are completing a questionnaire.

When the user does not want to continue answering, they may choose from the system's options without genuine reflection.

This creates false clarity.

### Correction

The system should prefer:

- Open prompts
- User-led language
- Reflection from the user's own words
- Fewer questions
- Explicit pause and exit options

The system should periodically offer:

- Continue
- Pause
- Summarize
- Shift to application
- Save a cognitive change record
- Stop

### Memory Candidate

This scenario suggested a possible cognitive change, but it should not be saved as personal Memory without user consent.

If the user chooses to save it later, it could be compressed into a respectful record such as:

```text
Topic:
External stimulation and happiness

Cognitive Movement:
The user connected the chapter's idea of chasing external stimulation with the possibility that some personal future-oriented goals may be attempts to secure inner ease through outer conditions.

Open Question:
When a new goal appears, is it a clear desire or an attempt to avoid discomfort, comparison, or self-judgment?

Practice:
When "If only I had X" appears, observe:
- What do I expect X to give me?
- Is this a grounded wish or a conditioned chase?
```

### Design Implication

This scenario establishes several system requirements:

- Source Grounding should be a core Method.
- Chapter Mapping should be available for book-based scenarios.
- Open Reflection should precede diagnostic questioning.
- Cognitive Change Capture should happen only after the user feels the discussion has reached a natural landing point.
- Exit And Turn should be treated as a required interaction mechanism, not an optional courtesy.
