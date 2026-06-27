# STEM Teaching Sequence Example

## User Question

Teach me gradient descent from intuition to formula, then give me a practice
check.

## Diagnosis

- Subject: Math / AI / machine learning foundations.
- Topic: Gradient descent.
- Prerequisites: Functions, slope or derivative, and the idea of minimizing an
  error.
- Likely gap: The learner needs a bridge from "move downhill" intuition to the
  update rule.

## Knowledge Gap Type

Concept gap plus notation gap.

## Teaching Depth Level

Level 4: Foundation-first full explanation.

## Example Tutor Response

Start with the picture: imagine standing on a hilly surface where height means
error. Your goal is to move to a lower place.

In one dimension, the derivative tells you whether moving right increases or
decreases the function. In many dimensions, the gradient is the arrow pointing
in the direction of steepest increase.

So if the gradient points uphill, gradient descent moves the opposite way:

```text
new parameters = old parameters - learning_rate * gradient
```

The symbols mean:

- `parameters`: the adjustable numbers in the model.
- `gradient`: the direction that increases loss fastest at the current point.
- `learning_rate`: how large a step to take.

Why it works: for a small enough step, moving opposite the gradient usually
reduces the loss locally. The method can fail or behave badly if the step is
too large, the surface is very flat, or the loss has tricky local shapes.

Common mistake: thinking gradient descent knows the global best answer. It only
uses local slope information at the current point.

## Follow-Up Check Or Practice

If the gradient at the current point is `[2, -3]`, what direction does gradient
descent step before applying the learning rate?

## Why This Is Adaptive Teaching

The response follows the STEM path: intuition, concrete surface example,
formal update, notation, why it works, edge cases, common mistake, and a small
practice check.

## What A Normal Answer Bot Would Miss

It might start with the update formula and assume the learner already knows
what gradient, loss, and learning rate mean.
