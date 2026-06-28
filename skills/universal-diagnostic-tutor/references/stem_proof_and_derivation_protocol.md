# STEM Proof And Derivation Protocol

Use this protocol when the learner asks why a formula works, how to prove a
claim, where an equation comes from, or why an algorithm is correct.

The goal is not just to show legal steps. The goal is to make the reason behind
the result visible.

## Core Sequence

1. **State the goal.** What are we trying to prove, derive, or justify?
2. **List assumptions and known facts.** Name definitions, conditions, prior
   theorems, model assumptions, units, or invariants.
3. **Explain the key idea before formal steps.** Give the proof intuition or
   derivation strategy.
4. **Separate conceptual reasoning from algebraic manipulation.** Say whether a
   step follows from a definition, assumption, algebra rule, invariant, or
   physical model.
5. **Show why each step is allowed.** Do not hide the main reason in notation.
6. **Use a small example when abstract.** A tiny case can reveal the structure.
7. **Explain what the result means.** Return from symbols to interpretation.
8. **Check.** Ask one question about the key idea or a nearby case.

## Domain Calibration

### Calculus

Connect derivative formulas to change and local rate. Connect integral formulas
to accumulation, area, total change, or limiting sums.

### Linear Algebra

Connect proofs to spaces, transformations, rank, independence, span, basis,
projection, orthogonality, eigenvectors, and dimension.

### Probability / Statistics

Connect formulas to sample space, conditioning, distributions, uncertainty,
counting, assumptions, and what information is being updated.

### Algorithms

Connect proof to invariants, induction, correctness, termination, and
complexity. For search or sorting, name what remains true after each step.

### Physics / Engineering

Connect derivations to assumptions, models, conservation laws, units,
dimensions, idealizations, and measurement limits.

## Step Explanation Patterns

- "This step uses the definition of..."
- "This equality is algebra; the important idea is..."
- "The invariant is..."
- "The assumption that makes this legal is..."
- "This small case shows why the general rule has this shape..."
- "After the derivation, the result means..."

## Anti-Patterns

- Starting with formal notation before stating the goal.
- Presenting a derivation as a chain of equations with no reason for each step.
- Treating algebraic manipulation as understanding.
- Skipping assumptions, units, boundary cases, or invariants.
- Ending at the formula without explaining what it means.
