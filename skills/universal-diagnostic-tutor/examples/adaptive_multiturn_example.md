# Adaptive Multiturn Example

## User Question

I still do not understand matrix multiplication. You said it is rows times
columns, but I do not see what it means.

## Diagnosis

- Subject: Math / linear algebra.
- Topic: Matrix multiplication.
- Known idea: The learner has heard the row-times-column procedure.
- Likely gap: They do not understand the meaning of the operation.

## Knowledge Gap Type

Concept gap plus notation gap. The learner knows the procedure words but not
the transformation or composition model behind them.

## Teaching Depth Level

Level 4: Foundation-first full explanation.

## Example Tutor Response

Good, that tells me the row-times-column rule is not the part to repeat. The
stuck point is what multiplication of matrices is for.

Think of a matrix as a machine that moves or changes a vector. If matrix `B`
changes a vector first, and matrix `A` changes the result after that, then
`AB` means "one combined machine that does `B` first, then `A`."

So the meaning is:

```text
ABx = A(Bx)
```

The row-times-column calculation is just the bookkeeping that builds the
combined machine.

Smaller example: if `B` stretches a point and `A` rotates it, then `AB` is the
single transformation that stretches first and rotates second.

## Follow-Up Check Or Practice

Tiny check: In `ABx`, which matrix touches the vector `x` first: `A` or `B`?

## Why This Is Adaptive Teaching

The response does not repeat the same row-times-column explanation. It
diagnoses a concept gap, changes representation to transformations, uses a
smaller example, and asks one focused check question.

## What A Normal Answer Bot Would Miss

It would likely restate the multiplication formula or compute another example
without repairing the missing meaning behind the notation.
