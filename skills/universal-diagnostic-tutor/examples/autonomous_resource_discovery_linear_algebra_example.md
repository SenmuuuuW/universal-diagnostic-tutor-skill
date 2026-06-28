# Autonomous Resource Discovery Linear Algebra Example

## User Question

"What does `Ax = b` mean? I don't know if `b` is a point or a vector. Use good
resources if you can."

## Diagnosis

- **Subject routing:** Linear algebra.
- **Likely gap:** Notation and object-type gap.
- **Task:** Explain symbols before solving.

## Expected Pacing Choice

Teach the object roles first, then pause with a check before row reduction or
solving.

## Autonomous Search

Use autonomous search if web/search access is available because the user asks
for good resources and the topic benefits from stable linear algebra sources.

## Source Selection Logic

Prefer exact university/open textbook sources such as:

- A linear algebra course lecture or chapter on matrix-vector multiplication.
- An open textbook section on matrix equations or linear transformations.
- A visual intuition source only as an intuition builder, not as the sole
  formal reference.

Avoid broad homepages, pirated textbook PDFs, or answer-only sites.

## Example Tutor Response

The sticking point is the type of each object, not row reduction yet.

If search is available, I would look for a reliable linear algebra source on
matrix-vector multiplication or matrix equations, preferably a university note
or open textbook section. The source's role would be to confirm the formal
definition; I will still teach the meaning directly.

In `Ax = b`:

- `A` is a matrix.
- `x` is usually the unknown vector.
- `b` is also a vector.
- The expression `Ax` means "apply the transformation `A` to the vector `x`."

So `Ax = b` means:

```text
Find the input vector x that A transforms into the output vector b.
```

You can picture `b` as a point position if you are drawing vectors in the
plane, but mathematically it is a vector: an object with components such as
`[4, 7]`.

Tiny check before solving: in `Ax = b`, which object is unknown: `A`, `x`, or
`b`?

## Stop Point Or Check Question

"Which object is unknown: `A`, `x`, or `b`?"

## Why This Is Better Than A Generic AI Answer

A generic answer may jump to row reduction or list links. This answer first
diagnoses the notation gap, explains object roles, uses source search only when
useful, and pauses before solving.
