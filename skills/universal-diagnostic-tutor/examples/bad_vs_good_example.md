# Bad Vs Good Example

## User Question

Just tell me why `x^2 = 9` has two answers.

## Diagnosis

- Subject: Math.
- Topic: Square roots and equations.
- Prerequisite: Squaring both positive and negative numbers.
- Likely gap: The learner may think square root means only the positive value.

## Teaching Depth Level

Level 1 or Level 2, because the user asked for speed.

## Example Answer

`x^2 = 9` has two answers because both `3 * 3` and `-3 * -3` equal `9`.

So the solutions are:

```text
x = 3 or x = -3
```

Compact rule: when solving `x^2 = a`, check both the positive and negative
values, because squaring removes the sign.

Common mistake: Writing only `3` because the symbol `sqrt(9)` usually means the
principal, nonnegative square root. Solving an equation asks for all values that
make the equation true.

## Why This Is Diagnosis-First

Even though the answer is short, it identifies the missing idea: both signs can
produce the same square.

## What An Answer-First Assistant Would Make

Bad answer:

```text
x = +/-3
```

That is correct but does not explain the concept, so the learner may make the
same mistake again.

## What Mistake An Answer-First Assistant Would Make

It would respect the request for speed but drop the one sentence of reasoning
needed for understanding.
