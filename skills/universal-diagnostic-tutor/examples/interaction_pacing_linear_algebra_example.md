# Interaction Pacing Linear Algebra Example

## User Question

"I uploaded an image with two linear algebra questions. Please help, but don't
just give me the answers."

Question 1 asks whether `[3, 6]` is a scalar multiple of `[1, 2]`.
Question 2 asks whether `[2, 1]` and `[4, 2]` span `R^2`.

## Diagnosis

- **Subject routing:** Linear algebra.
- **Likely gap:** The learner may know vector arithmetic but not the method cue
  for scalar multiples and span.
- **Task:** Multiple subproblems from one image; start with the first.

## Expected Pacing Choice

Identify both questions, then solve only the first setup and stop before the
key comparison step. Do not complete both questions in one long answer.

## Autonomous Search

Not needed for this turn. The concept is small enough to teach directly. If the
learner later asks for practice sources, use university/open textbook linear
algebra resources.

## Source Selection Logic

No source is needed. Use internal teaching and one check question.

## Example Tutor Response

I see two questions here:

1. Check whether `[3, 6]` is a scalar multiple of `[1, 2]`.
2. Check whether `[2, 1]` and `[4, 2]` span `R^2`.

Let's start with the first one only.

Scalar multiple means: can one vector be made by multiplying the other vector
by one number?

So we ask:

```text
[3, 6] = k[1, 2]
```

That means:

```text
3 = k * 1
6 = k * 2
```

Stop here: the key learning step is checking whether the same `k` works for
both components.

Tiny check: from the first equation, what value of `k` do you get?

## Stop Point Or Check Question

"From `3 = k * 1`, what value of `k` do you get?"

## Why This Is Better Than A Generic AI Answer

A generic answer might solve both questions immediately. This response
identifies both subproblems but teaches one method cue at a time and leaves the
key comparison step for the learner.
