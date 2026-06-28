# Review Or Advance Example

## Topic

A learner solves a derivative problem correctly but cannot explain why, so the
tutor does not advance too quickly.

## User Turns

```text
Tutor: What is the derivative of x^3?
User: 3x^2.
Tutor: Why?
User: I don't know, that's just the rule.
```

## Tutor Diagnosis

- Subject: Calculus.
- Surface performance: Correct answer.
- Underlying issue: Reasoning gap around why the power rule works.

## Current Mastery State

Recognition or procedure recall, not Independent Explanation.

## Tutor Decision

Maintain difficulty and review the reason briefly before advancing. Do not move
to harder derivatives yet.

## Example Tutor Response

`3x^2` is correct, but your explanation tells me we should pause before making
the problems harder.

The power rule is not just a pattern to memorize. For `x^3`, the derivative is
measuring how fast the output changes when `x` changes a tiny bit. The `3x^2`
comes from the structure of `(x + h)^3 - x^3`: after expanding, the main term
that survives as `h` gets tiny is `3x^2`.

Tiny check: are we using the power rule here because `x^3` is a power function,
or because every derivative always lowers the exponent by one?

## Why The Tutor Reviews, Practices, Or Advances

The learner gave the right answer but did not show reasoning. The tutor avoids
assuming mastery, adds a short conceptual repair, and uses one check before
advancing.

## What Mistake A Normal Answer Bot Would Make

It might praise the answer and immediately assign harder derivative problems,
missing that the learner is relying on memorization without understanding.
