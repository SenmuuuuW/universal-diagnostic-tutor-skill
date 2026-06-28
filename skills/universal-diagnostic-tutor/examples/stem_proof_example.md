# STEM Proof Example

## User Question

Why is binary search correct? I know the code, but I do not see why it always
finds the target if it exists.

## Diagnosis

- Subject: Algorithms.
- Topic: Binary search correctness.
- Likely issue: The learner knows the procedure but not the invariant that
  makes it safe to discard half the search space.

## Likely Knowledge Gap Type

Reasoning gap plus procedure gap.

## Teaching Depth Level

Level 4: Proof with invariant.

## Ask Or Explain First

Explain first. The learner is asking for correctness, so the tutor should name
the invariant before asking for a proof step.

## Example Tutor Response

The key proof idea is an invariant: if the target is in the array, it is always
inside the current search interval.

Start with the whole sorted array. The target, if present, is somewhere inside
that interval.

At each step, compare the target with the middle element:

- If the middle equals the target, we are done.
- If the target is smaller, sorted order means it cannot be to the right of the
  middle.
- If the target is larger, sorted order means it cannot be to the left of the
  middle.

So when binary search discards half the array, it discards only positions where
the target cannot be. That preserves the invariant.

The loop stops when the interval is empty. At that point, if we have not found
the target, the invariant says there is nowhere left it could be.

## Follow-Up Check Or Practice

Tiny check: what assumption lets us safely discard the right half when the
target is smaller than the middle element?

## Why This Is Adaptive STEM Teaching

The tutor focuses on the proof goal, identifies the invariant, explains why
each discard step is allowed, and checks the key assumption.

## What Mistake A Normal Answer Bot Would Make

It might restate the algorithm or show code without explaining the invariant
that proves correctness.
