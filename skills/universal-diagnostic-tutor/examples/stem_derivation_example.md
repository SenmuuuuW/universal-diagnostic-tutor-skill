# STEM Derivation Example

## User Question

Why is the derivative of `x^2` equal to `2x`?

## Diagnosis

- Subject: Calculus.
- Topic: Derivative derivation from first principles.
- Likely issue: The learner may know the power rule but not why it works.

## Likely Knowledge Gap Type

Reasoning gap plus concept gap.

## Teaching Depth Level

Level 4: Foundation-first derivation.

## Ask Or Explain First

Explain first. The learner is asking why the formula works, so the tutor should
state the goal and show why each step is allowed.

## Example Tutor Response

Goal: show why the slope of `f(x) = x^2` at input `x` is `2x`.

The derivative means the limit of average rate of change over a tiny interval:

```text
f'(x) = lim h->0 (f(x + h) - f(x)) / h
```

For `f(x) = x^2`, substitute into the definition:

```text
((x + h)^2 - x^2) / h
```

Expand the square:

```text
(x^2 + 2xh + h^2 - x^2) / h
```

The `x^2` terms cancel:

```text
(2xh + h^2) / h = 2x + h
```

Now let `h` shrink to `0`:

```text
2x + h -> 2x
```

So the derivative is `2x`. Meaning: at the point `x`, the graph of `x^2` is
changing at a rate of `2x`.

## Follow-Up Check Or Practice

Tiny check: in the derivation, why are we allowed to cancel `h` before setting
`h` to zero?

## Why This Is Adaptive STEM Teaching

The tutor states the derivation goal, separates the derivative idea from the
algebra, explains each legal step, and returns to the meaning of the result.

## What Mistake A Normal Answer Bot Would Make

It might cite the power rule directly and skip the reason the formula works.
