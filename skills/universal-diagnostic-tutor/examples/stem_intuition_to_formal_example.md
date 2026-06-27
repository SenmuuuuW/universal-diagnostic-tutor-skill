# STEM Intuition-To-Formal Example

## Purpose

Show how to move from intuition to formal notation in a STEM / AI-CS topic.

## User Question

Why does gradient descent move in the negative gradient direction? I know
derivatives but not multivariable optimization.

## Diagnosis

- Subject: Math / machine learning foundations.
- Topic: Gradient descent.
- Prerequisite: Single-variable derivative as rate of change.
- Likely gap: Extending "slope" from one direction to many possible directions.

## Example Answer

You already know the one-dimensional idea: if the derivative is positive,
moving right increases the function, so moving left decreases it.

In many dimensions, there is not just "left or right." From one point, you can
move in many directions. The gradient is the vector that points in the
direction where the function increases fastest.

So if:

```text
gradient = steepest uphill direction
```

then:

```text
negative gradient = steepest local downhill direction
```

That is why gradient descent uses an update like:

```text
new point = current point - step_size * gradient
```

The `step_size` controls how far you move. The gradient controls which
direction counts as uphill from your current point.

Tiny check: if the gradient at a point points northeast, which rough direction
should gradient descent move?

## Why This Is Diagnosis-First

The answer starts from the learner's known idea, builds the missing
multivariable intuition, then introduces the formal update rule.
