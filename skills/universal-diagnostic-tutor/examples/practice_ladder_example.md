# Practice Ladder Example

## Purpose

Show how to build mastery practice instead of giving a random list of
exercises.

## User Question

I understand recursion when you explain it, but I freeze when I need to write a
recursive function. Give me practice.

## Diagnosis

- Subject: Programming / computer science foundations.
- Topic: Recursion.
- Likely gap: Procedure and transfer. The learner can follow recursive examples
  but struggles to identify the base case and recursive step independently.

## Knowledge Gap Type

Procedure gap plus transfer gap.

## Teaching Depth Level

Level 4: Foundation-first practice toward mastery.

## Example Tutor Response

You probably do not need the definition again. The missing skill is turning a
problem into two parts: the base case and the smaller same problem.

Practice ladder:

1. **Recognition:** Is this a recursion-shaped problem? Example: "sum all
   numbers in a list." Can it be reduced to the first item plus the sum of the
   rest?
2. **Basic concept check:** What is the base case for an empty list?
3. **Worked example completion:** Fill in the missing line:
   `sum_list(xs) = xs[0] + ______`.
4. **Near-transfer:** Write `count_items(xs)` using the same structure.
5. **Trap/misconception:** What goes wrong if the recursive call uses `xs`
   instead of a smaller list like `xs[1:]`?
6. **Mixed-topic:** Decide whether factorial, binary search, and printing a
   menu are recursion, iteration, or either.
7. **Project-style application:** Sketch a function that counts files in a
   folder tree. Name the base case and recursive case.

How to move up: if you can explain the base case, recursive case, and why the
input gets smaller, go to the next rung. If you only guessed correctly, stay on
that rung and explain the structure in one sentence.

## Follow-Up Check Or Practice

Start with rung 2: for `sum_list([])`, what should the function return, and why?

## Why This Is Adaptive Teaching

The answer identifies the procedure/transfer gap and organizes practice from
recognition to project-style application instead of dumping random recursion
exercises.

## What A Normal Answer Bot Would Miss

It might give several recursion problems without diagnosing whether the learner
needs recognition, base-case practice, near-transfer, or mixed-method practice.
