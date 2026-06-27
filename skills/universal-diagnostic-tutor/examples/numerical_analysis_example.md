# Numerical Analysis Example

## User Question

"Why do computers sometimes get inaccurate answers in numerical calculations?"

## Diagnosis

This is a numerical analysis question about representation, approximation, and
error propagation. The learner probably expects computers to calculate exact
real numbers.

## Prerequisite Gap

The likely gap is floating-point representation: computers store finite
approximations of many decimal or real values, and operations can amplify small
errors.

## Source-Pack Behavior

Use `source_packs/numerical_hpc_control.md`. For foundations, start with MIT
18.335J or UIUC CS357. Use HPC sources only if the learner asks about parallel
scientific computing or performance.

## Teaching Depth Level

Level 4: foundation-first full explanation.

## Example Answer

Computers can be very fast and still be approximate. The key issue is that many
real numbers cannot be stored exactly in a finite number of bits. A computer
stores a rounded version, then performs operations on those rounded versions.

That usually works well, but errors can grow. Subtracting two nearly equal
numbers can erase meaningful digits. Repeating a calculation many times can
accumulate rounding error. Solving a poorly conditioned system can make a tiny
input error produce a large output error.

Numerical analysis studies how to choose methods that control those errors. It
asks not only "what is the formula?" but "is this formula stable when computed
with finite precision?"

## Source List Behavior

- MIT OCW 18.335J Numerical Methods: formal numerical analysis path.
- UIUC CS357 Numerical Methods: undergraduate practical path.
- LLNL HPC Tutorials: only when parallel scientific computing becomes relevant.

## Common Mistakes

- Assuming computer arithmetic is the same as exact algebra.
- Blaming programming language syntax instead of representation and stability.
- Using a formula without checking whether it is numerically stable.

## Why This Is Diagnosis-First And Resource-Augmented

The answer diagnoses the learner's hidden assumption, teaches representation
and error first, then selects numerical sources by level.

## Answer-First Or Source-Dumping Mistake

A weak assistant would say "because floating point is imprecise" and stop, or
dump numerical methods links without explaining rounding, cancellation, and
stability.
