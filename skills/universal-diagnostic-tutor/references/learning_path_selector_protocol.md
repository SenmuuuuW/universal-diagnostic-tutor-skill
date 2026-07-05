# Learning Path Selector Protocol

Use this protocol after the learner's goal is confirmed and the tutor has
enough evidence to choose what to study next.

The selector chooses the next best learning step, not the entire path.

## Inputs

Consider:

- confirmed goal
- current level and teaching mode
- prerequisite gaps
- urgency or deadline
- exam, project, concept, or general-learning context
- mastery signals from the current conversation
- available time

## Output Shape

Use this shape when useful:

```text
Current goal: [goal]
Current blocker: [blocker]
Next best step: [one learning step]
Why this step: [reason]
Not yet: [advanced topic or broad branch to postpone]
Check: [one focused question or tiny task]
```

In ordinary tutoring, this can be expressed naturally without visible labels.

## Selection Rules

- Pick the earliest blocking prerequisite.
- Explain why this step comes first.
- Avoid jumping to advanced topics before prerequisites are stable.
- If the learner needs exam review, choose high-yield repair and method cues.
- If the learner needs project ability, choose concepts that unlock
  implementation.
- If the learner needs conceptual understanding, start with intuition,
  notation, and object roles.
- If mastery is unconfirmed, check before advancing.
- Keep the plan reversible: learner evidence can change the next step.

## Examples

### Machine Learning With Weak Math

Next best step: vectors and functions, not neural networks.

Why: linear regression, gradients, and model parameters all rely on these
objects. A neural-network overview would add vocabulary before the learner can
use it.

### Linear Algebra Matrices Are Confusing

Next best step: linear combination / matrix multiplication meaning, not
eigenvalues.

Why: eigenvalues depend on understanding matrices as transformations or column
combinations.

### Series Convergence Exam

Next best step: classify the series type before choosing a test.

Why: the learner's blocker is method recognition, so listing tests will not
help until the cue is visible.

## Mistakes To Avoid

- Presenting the whole learning path as if it must be followed rigidly.
- Choosing the exciting advanced topic instead of the unlocking prerequisite.
- Advancing after one correct answer when the "why" is still unconfirmed.
- Ignoring time pressure or project context.
