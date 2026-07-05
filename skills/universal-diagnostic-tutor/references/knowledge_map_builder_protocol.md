# Knowledge Map Builder Protocol

Use this protocol after a broad goal is confirmed or when a learner asks where
a concept fits in a larger subject.

The output is a compact, goal-specific knowledge map. It is not a full course
outline, textbook table of contents, or curriculum map.

## Map Contents

Include only what helps choose the next step:

- **Target area:** the larger subject or course module.
- **Prerequisite nodes:** ideas needed before the focus node.
- **Current focus node:** the concept or skill to work on now.
- **Next possible nodes:** nearby concepts that may come after a check.
- **Dependencies:** which node depends on which prerequisite.
- **Mastery status:** confirmed, unconfirmed, weak, or blocked when evidence is
  available.
- **First learning path:** the first one to three nodes to attempt.

## Supported Formats

- compact bullet tree
- small Markdown table
- Mermaid flowchart when the host can render it
- plain text map for ordinary chat

## Rules

- Keep the map small enough to read in one glance.
- Use the learner's goal to decide map depth.
- Mark uncertain mastery as unconfirmed, not learned.
- Do not assume that because one concept was explained, related concepts are
  mastered.
- Use a Learning State Card or Learning Task Card when the map should persist
  across chats.

## Example: Machine Learning With Weak Math

```text
Machine Learning Entry Map:
- Python basics: unconfirmed
- Linear algebra
  - vectors: first check
  - matrices: later
  - matrix multiplication: later
- Calculus
  - functions: first check
  - derivatives: later
  - gradients: later
- Probability/statistics
  - probability: later
  - distributions: later
  - expectation: later
- Optimization
  - loss: later
  - gradient descent: later
- First ML model
  - linear regression: after vectors/functions/loss

Current first step: vectors and functions, not neural networks.
```

## Example: Linear Algebra Matrix Confusion

```text
Small map:
vectors -> linear combinations -> matrix multiplication -> linear transformation

Likely missing node: linear combination.
First step: explain one column combination before using matrix notation.
```

## Mistakes To Avoid

- Generating a full semester plan when the learner needs a first step.
- Marking a node as mastered after an explanation only.
- Listing every prerequisite chain in the subject.
- Using a beautiful map that does not guide the next tutoring action.
