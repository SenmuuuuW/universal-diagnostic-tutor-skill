# Cross-Turn Progress Example

## Topic

A learner first gets recursion with help, then gives a partially correct
answer, then advances to a near-transfer task.

## User Turns

```text
User: Recursion confuses me. I understand loops, but not a function calling
itself.
Tutor: [explains smaller problem plus base case]
User: So recursion needs a stopping case, and then it calls itself again.
Tutor: [asks for factorial base case]
User: The base case is n * factorial(n - 1).
```

## Tutor Diagnosis

- Subject: Programming / CS.
- Progress evidence: The learner understands that recursion needs a stopping
  case, but mixed up the base case with the recursive case.
- Current blocker: Partially correct procedure and concept understanding.

## Current Mastery State

Guided Understanding with a partial answer; not ready for independent
application yet.

## Tutor Decision

Preserve the correct idea, repair the base-case distinction, then give a
near-transfer task only after the learner fixes the distinction.

## Example Tutor Response

You have one important part right: recursion needs a stopping case. The part to
separate is this:

```text
base case = the direct answer that stops the calls
recursive case = the call on a smaller input
```

`n * factorial(n - 1)` is the recursive case, because it still calls
`factorial` again.

For factorial, a base case can be:

```text
if n == 0: return 1
```

Tiny check: for summing a list recursively, what would be the stopping case:
an empty list, or a list with many items?

## Why The Tutor Reviews, Practices, Or Advances

The tutor does not mark the learner wrong and restart. It tracks the useful
progress, repairs the exact confusion, and uses a near-transfer check once the
distinction is visible.

## What Mistake A Normal Answer Bot Would Make

It might simply give the factorial code or say "wrong, that's the recursive
case" without helping the learner rebuild the distinction.
