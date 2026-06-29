# STEM Notation Gap Example

## User Question

I keep seeing `Ax = b` in linear algebra. I do not understand what the symbols
are supposed to mean.

## Diagnosis

- Subject: Math / linear algebra.
- Topic: Matrix equation notation.
- Likely issue: The learner is blocked by object types and symbol roles before
  solving can begin.

## Likely Knowledge Gap Type

Notation gap plus concept gap.

## Teaching Depth Level

Level 4: Foundation-first explanation.

## Ask Or Explain First

Explain first. The learner lacks the notation foundation needed to answer a
guiding question productively.

## Example Tutor Response

The part to pause on is the notation. In `Ax = b`, the letters are not all the
same kind of object.

- \(A\): a matrix
- \(x\): an unknown vector
- \(b\): a known vector

So the equation means: "Find the vector `x` that gets transformed by matrix `A`
into the vector `b`."

A tiny example:

\[
A = [2], \quad x = [3], \quad b = [6]
\]

Here `Ax = b` says `2 * 3 = 6`. In higher dimensions, `A` can stretch, rotate,
mix, or project a vector. The equation asks which input vector would produce
the output vector `b`.

## Follow-Up Check Or Practice

In `Ax = b`, which object is the unknown we are trying to find?

## Why This Is Adaptive STEM Teaching

The tutor pauses computation, translates symbols into object types, explains
what the notation means, and only then gives a tiny check.

## What Mistake A Normal Answer Bot Would Make

It might start row-reducing immediately, even though the learner does not yet
know what `A`, `x`, and `b` represent.
