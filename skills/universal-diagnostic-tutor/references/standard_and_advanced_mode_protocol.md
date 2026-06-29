# Standard And Advanced Mode Protocol

Use this protocol to calibrate answers for learners who are not zero-base:
standard learners with classroom exposure and advanced learners seeking rigor,
efficiency, derivation, proof, assumptions, edge cases, or transfer.

Both modes remain diagnosis-first and preserve V1.1 stop-point behavior.

## Standard Mode

Standard Mode balances explanation, method recognition, guided steps, and
exam-style practice.

Use it when the learner has seen the topic but cannot reliably solve or choose
the method.

Do:

- Briefly review only the prerequisite needed now.
- Name the method cue before solving.
- Explain why the method applies.
- Work one subproblem at a time.
- Stop before key transformations.
- Give one short check or near-transfer practice item.

Avoid:

- Re-teaching obvious basics.
- Jumping straight to proof rigor.
- Dumping a full solution without method recognition.

## Advanced Mode

Advanced Mode prioritizes rigor, proof, derivation, assumptions, edge cases,
efficiency, and transfer.

Use it when the learner already knows the basics or explicitly asks for proof,
derivation, rigor, comparison, optimization, or concise explanation.

Do:

- State assumptions.
- Use formal notation appropriately.
- Explain the proof or derivation hinge.
- Discuss edge cases and failure conditions.
- Generalize the method.
- Connect to transfer, exam patterns, or later topics.

Avoid:

- Slowing down for basic vocabulary unless evidence shows a gap.
- Hiding the main idea behind too much notation.
- Giving a bare final answer when the learner requested understanding.

## STEM Examples

### Series Convergence

- **Standard:** Identify cues such as telescoping, alternating signs, ratio
  structure, comparison shape, or p-series form. Stop before the algebraic
  rewrite or test choice.
- **Advanced:** State convergence criteria, justify test conditions, discuss
  absolute vs conditional convergence, and note edge cases.

### Derivative Derivation

- **Standard:** Use the derivative definition with a small expansion and stop
  before cancellation.
- **Advanced:** Use the limit definition efficiently, justify algebraic
  simplification for \(h \neq 0\), then take the limit and interpret local linear
  behavior.

### Matrix Equation

- **Standard:** Identify object types in \(Ax=b\), explain method cue, then ask
  what is unknown.
- **Advanced:** Discuss linear map, solvability, rank, null space, uniqueness,
  and geometric interpretation.

### Recursion

- **Standard:** Ask for base case and smaller input, then trace one call.
- **Advanced:** State invariant or induction proof, termination measure, stack
  complexity, and edge cases.

### Algorithm Proof

- **Standard:** Name the invariant and ask which step preserves it.
- **Advanced:** Prove initialization, maintenance, termination, complexity, and
  boundary conditions.

### Gradient Descent

- **Standard:** Connect slope to loss decrease, then ask whether to move with
  or against the gradient.
- **Advanced:** Use first-order Taylor approximation, step-size assumptions,
  local descent condition, convex vs nonconvex caveats, and transfer to
  stochastic gradients.

### Virtual Memory

- **Standard:** Distinguish virtual address, physical address, page table, and
  process isolation.
- **Advanced:** Discuss address translation, TLB, page faults, protection bits,
  replacement policy, and performance tradeoffs.

## Preserve Stop Points In Both Modes

Standard stop points are usually about method choice or the next algebra/code
step. Advanced stop points are usually about assumptions, proof hinge, edge
case, or generalization.

Even in Advanced Mode, pause when the learner requested participation or when
one key step is the learning target.
