# STEM Ask-Vs-Explain Calibration

Use this guide for university-level STEM, AI, computer science, mathematics,
physics, engineering foundations, and related technical subjects. The goal is
to choose whether the next teaching move should be a guiding question or a
direct explanation.

Questions should help learning. They should not stall, test a confused learner,
or turn every answer into a Socratic exercise.

## Core Choice

Ask a guiding question when the learner likely has enough prerequisite
knowledge to reason one step.

Explain directly when the learner lacks vocabulary, notation, concept
foundation, or the required mathematical or technical background.

After a direct explanation, use a tiny check question to see whether the idea
landed.

## Ask A Guiding Question When

- The learner has already shown the needed prerequisite.
- One small prompt can reveal whether they recognize the structure.
- The learner is practicing method selection or transfer.
- The next step is narrow enough to answer without guessing.
- You need to diagnose a specific uncertainty before explaining more.

Good question shape:

```text
Before we compute, what kind of object is this: scalar, vector, matrix, or
function?
```

## Explain Directly When

- The learner is missing a definition, symbol meaning, or notation convention.
- The learner has not seen the prerequisite concept.
- The topic depends on background math, code behavior, system layers, or
  physical intuition they likely do not have.
- The learner says they are lost, overwhelmed, or still do not understand.
- The user asks for an urgent short answer.

In urgent short-answer mode, answer first, then give one compact reason.

## STEM-Specific Question Types

### Math

Ask questions that reveal recognition of structure, not just computation.

- Good: "Is this asking for a rate of change, an accumulated amount, or a
  solved value?"
- Weak: "What is the derivative?" when the learner does not know what a
  derivative means.

### Programming

Ask questions that reveal mental model, not just syntax.

- Good: "Where is the list created, and where is it appended to?"
- Weak: "What line should you write?" when the learner does not understand
  state or control flow.

### AI / ML

Ask questions that reveal prerequisite gaps in linear algebra, probability,
calculus, optimization, or programming.

- Good: "Do you see the gradient as one derivative or as a vector of partial
  derivatives?"
- Weak: "Why does the optimizer converge?" before the learner understands loss.

### Systems

Ask questions that reveal whether the learner understands abstraction layers.

- Good: "Is this address the program sees, or the physical address in RAM?"
- Weak: "What does the MMU do?" before virtual and physical addresses are
  distinguished.

### Physics / Electronics / Signals

Ask questions that reveal whether the learner understands the phenomenon before
the equation.

- Good: "What physical quantity is changing over time here?"
- Weak: "Which transform should we apply?" before the signal meaning is clear.

## Anti-Patterns

- Do not turn every STEM answer into Socratic questioning.
- Do not make a confused learner feel tested.
- Do not ask questions whose answer requires knowledge the learner has not been
  taught.
- Do not use questions to delay giving the needed explanation.
- Do not hide the final answer in a long chain of hints when the user asked for
  speed.

## Good STEM Rhythm

1. Diagnose the likely gap.
2. Explain directly if the prerequisite is missing.
3. Ask one tiny check question.
4. If the learner succeeds, ask a guiding transfer question.
5. If not, step down and explain with a smaller example.
