# Next Best Teaching Step Protocol

Use this protocol when the tutor must decide what to teach next. The default is
not "explain all background" or "finish the problem." The default is to choose
the one concept, symbol, method, or reasoning hinge that blocks progress most.

## Core Rules

- Do not explain all possible background at once.
- Choose the one concept, symbol, method, or reasoning hinge that is blocking
  the learner now.
- If several gaps appear, choose the earliest blocking gap.
- Trust "I know X but not Y" provisionally. Focus on Y unless later evidence
  shows X is weak.
- Prefer a smaller complete step over a broad incomplete lecture.
- Preserve teacher-like stop points: if the next step should come from the
  learner, ask and stop.

## By Teaching Mode

### Zero-Base Mode

The next best step is usually object or symbol meaning before any formal
solution.

Ask:

- What object is the learner looking at?
- What does the symbol mean in ordinary language?
- What is the problem asking for?

### Standard Mode

The next best step is usually method recognition or setup.

Ask:

- What cue in the problem suggests this method?
- What equation, trace, diagram, invariant, or representation should be set up
  first?
- Where should the learner stop and do one step?

### Advanced Mode

The next best step is usually the proof hinge, invariant, assumption, edge case,
or concise derivation step.

Ask:

- What makes the theorem or method valid here?
- What condition, invariant, lower bound, construction, or assumption is doing
  the work?
- What can be skipped because the learner already knows it?

## Examples

### Graph Theory: \(\chi'(K_n)\)

Do not start with the parity proof. First confirm whether the learner knows
that \(\chi'(G)\) is about edge coloring, not vertex coloring.

Next best step: translate \(K_n\), \(\chi'(G)\), and edge coloring; then ask
whether the problem colors vertices or edges.

### Linear Algebra Scalar Multiple

If the problem says two vectors are parallel or one is a scalar multiple of
another, do not start with row reduction.

Next best step: translate the words to \(u=cv\), then compare components using
the same scalar \(c\).

### Series Convergence

For \(\sum 1/[n(n+1)]\), do not list every convergence test.

Next best step: identify the structural cue \(n(n+1)\), which suggests partial
fractions or telescoping.

### Gradient Descent

If the learner knows derivatives but not gradient descent, do not reteach the
derivative from scratch.

Next best step: identify the four objects: loss, parameter, gradient, and
update.

### Binary Search Proof

If the learner knows the code but not why it works, do not restate the code.

Next best step: identify the invariant: if the target exists, it remains inside
the current search interval.

## Mistakes To Avoid

- Solving the whole problem when the learner only needs the setup cue.
- Asking a guiding question before the learner knows the objects involved.
- Reteaching basics after the learner shows they know them.
- Jumping to transfer before the learner can complete the current hinge step.
- Treating the next best step as a rigid template rather than an evidence-based
  teaching decision.
