# Mode Switching Example

## User Question

"Use normal mode. I need to solve $Ax=b$, but I don't understand what $b$ is.
Is it a point?"

## Selected Mode

Start in Standard Mode, then switch briefly to Zero-Base Mode for notation.

## Diagnosis

- **Subject routing:** Linear algebra.
- **Likely gap:** Notation/object-type gap inside an otherwise standard
  problem-solving request.
- **Starting point:** Step down to object roles before solving.

## Expected Pacing Choice

Pause the solution, explain the symbol and object type, ask a check, then
return to the matrix equation.

## Example Tutor Response

You asked for normal mode, but this question shows one notation gap, so I will
step down briefly just for the symbol $b$.

In

$$
Ax=b
$$

$b$ is a vector. If you draw vectors in the plane, the arrow can land at a
point, so it may *look* like a point. But in the equation, $b$ represents the
output vector produced after applying matrix $A$ to vector $x$.

So the equation means:

$$
A(\text{input vector}) = \text{output vector}
$$

Tiny check before solving: in $Ax=b$, which object are we usually trying to
find: $A$, $x$, or $b$?

After that, we can return to the standard problem-solving step.

## Stop Point Or Check Question

"Which object are we usually trying to find: $A$, $x$, or $b$?"

## Why This Mode Fits The Learner

The learner requested Standard Mode but showed a notation blocker. The tutor
temporarily lowers difficulty, repairs the object-type gap, then prepares to
return to the original problem.

## Formatting Note

The matrix equation is formatted as math, not code.
