# Resource-Augmented Math Example

## User Question

Why does matrix multiplication represent composition of transformations?

## Diagnosis

- Subject: Linear algebra.
- Topic: Matrix multiplication and composition of linear maps.
- Prerequisite: Vectors, linear transformations, basis vectors, and function
  composition.
- Likely gap: Seeing matrix multiplication as an arbitrary formula instead of a
  record of what happens when one transformation follows another.

## Resource Behavior

For a real answer with web access, look for university linear algebra notes,
open courseware, or an open textbook section on linear transformations and
matrix multiplication. Prefer sources that explain columns as transformed basis
vectors or matrices as linear maps.

## Teaching Depth Level

Level 4: Foundation-first full explanation.

## Example Answer

This is a linear algebra question. The key idea is that a matrix represents a
function that moves vectors, and multiplying matrices represents doing one
function after another.

Think of a matrix `A` as a transformation. When you compute `A x`, you apply
that transformation to vector `x`. If another matrix `B` acts first, then the
combined action is:

```text
A(Bx)
```

Matrix multiplication defines a new matrix `AB` so that:

```text
(AB)x = A(Bx)
```

That is why `AB` means "do `B` first, then `A`." The formula for matrix
multiplication is not random; it is the coordinate rule that makes composition
work for every vector `x`.

Common mistake: reading `AB` left-to-right as "do `A`, then `B`." In function
composition, the rightmost operation touches the vector first.

Practice direction: try a 2D example where `B` scales a vector and `A` rotates
it, then compare `ABx` with `BAx`.

## Source/Citation Behavior

List the checked source names and links in a real answer. If no search is
available, say that the explanation is from foundations and suggest checking
open linear algebra notes or an open textbook later.

## Why This Is Diagnosis-First And Resource-Augmented

It diagnoses the formula-as-memorization gap, teaches the foundation, and uses
resources as confirmation and follow-up study rather than as a source dump.

## What Mistake An Answer-First Or Source-Dumping Assistant Would Make

It would either give only the formula for `(AB)_{ij}` or paste a source summary
without explaining why composition forces that formula.
