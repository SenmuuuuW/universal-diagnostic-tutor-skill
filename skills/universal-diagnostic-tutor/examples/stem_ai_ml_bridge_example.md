# STEM AI / ML Bridge Example

## User Question

Why does gradient descent need calculus and linear algebra?

## Diagnosis

- Subject: AI / machine learning foundations.
- Topic: Gradient descent prerequisite bridge.
- Likely issue: The learner knows gradient descent as an ML phrase but does
  not see how derivatives, vectors, and parameters fit together.

## Likely Knowledge Gap Type

Concept gap plus prerequisite gap.

## Teaching Depth Level

Level 4: Foundation-first STEM bridge.

## Ask Or Explain First

Explain first, then ask a small check. The learner likely lacks the bridge
between math objects and ML training.

## Example Tutor Response

Gradient descent is an optimization method: it changes model parameters to make
the loss smaller.

Calculus enters because the derivative tells how a quantity changes. In ML, the
loss changes when the model parameters change. The gradient is the collection
of those derivative directions.

Linear algebra enters because models often have many parameters at once. We
store data, features, parameters, and gradients as vectors, matrices, or
tensors.

So the bridge is:

```text
data -> model parameters -> loss -> gradient -> parameter update
```

Calculus explains the direction of change. Linear algebra lets us represent
many changes at once.

## Follow-Up Check Or Practice

Tiny check: in gradient descent, is the gradient more like a single number, or
more like a vector of directions for many parameters?

## Why This Is Adaptive STEM Teaching

The tutor diagnoses the missing prerequisite bridge, connects calculus and
linear algebra to ML objects, and checks the learner's mental model of the
gradient.

## What Mistake A Normal Answer Bot Would Make

It might say "because gradients are derivatives" without explaining how loss,
parameters, vectors, and updates fit together.
