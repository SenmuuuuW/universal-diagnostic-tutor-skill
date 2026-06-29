# Mistake Analysis Example

## Purpose

Show how to treat an error as diagnostic evidence instead of only giving the
correct answer.

## User Question

I solved `2(x - 3) = 10` as `2x - 3 = 10`, so `x = 6.5`. What did I do wrong?

## Diagnosis

- Subject: Math.
- Topic: Distribution in linear equations.
- Likely gap: The learner distributed `2` to `x` but not to `-3`.

## Knowledge Gap Type

Procedure gap plus misconception gap.

## Teaching Depth Level

Level 3: Standard teacher-style mistake analysis.

## Example Answer

Your setup is close. The exact mistake happens here:

\[
2(x - 3) -> 2x - 3
\]

The `2` has to multiply the whole group inside the parentheses, not just the
`x`. So it should be:

\[
2(x - 3) = 2 \cdot x - 2 \cdot 3 = 2x - 6
\]

Now solve:

\[
\begin{aligned}
2x - 6 &= 10 \\
2x &= 16 \\
x &= 8
\end{aligned}
\]

Why your mistake is tempting: the `x` catches your eye, so it feels like the
outside number belongs only to the variable. But parentheses mean "treat this
whole group as one package."

Near-match practice: try `3(y - 4) = 15`. What should the left side become
after distributing?

## Why This Is Diagnosis-First

The answer locates the exact error, explains the mental model behind
parentheses, corrects the solution, and gives one targeted practice item.

## What A Normal Answer Bot Would Miss

It might only give `x = 8` or say "distribute correctly" without explaining why
the outside factor applies to the whole parenthesized group.
