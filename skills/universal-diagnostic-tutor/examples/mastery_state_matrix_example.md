# Mastery State Matrix Example

## Topic

A learner moves from not understanding `Ax = b` to explaining it and trying a
near-transfer problem.

## User Turns

```text
User: I keep seeing Ax = b. I don't even know what b is.
Tutor: [explains object types]
User: So A is a matrix and x and b are vectors?
Tutor: [checks meaning]
User: I think b is the output vector after A acts on x.
```

## Tutor Diagnosis

- Subject: Linear algebra.
- Initial blocker: notation and concept gap around matrix equation roles.
- Progress evidence: The learner can now identify `A`, `x`, and `b` and state
  the output role of `b`.

## Current Mastery State

Independent Explanation for the symbol roles, moving toward Guided Application.

## Tutor Decision

Do not reteach the symbol meanings. Move to a near-transfer check with a tiny
matrix equation.

## Example Tutor Response

Yes. That explanation has the key idea: `b` is the output vector, and `x` is
the input vector we are trying to find.

Let's try the same idea in a tiny case:

```text
A = [3]
x = [?]
b = [12]
```

Here `Ax = b` means `3 * x = 12`. What value of `x` would produce the output
`12`?

## Why The Tutor Reviews, Practices, Or Advances

The learner no longer needs the same notation explanation. They have explained
the roles, so the tutor advances one step to guided application without jumping
to row reduction or abstract vector spaces.

## What Mistake A Normal Answer Bot Would Make

It might start solving a full system immediately, even though the right next
step is a small application check.
