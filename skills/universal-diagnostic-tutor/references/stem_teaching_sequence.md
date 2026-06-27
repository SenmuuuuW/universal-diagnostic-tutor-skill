# STEM Teaching Sequence

Use this sequence for STEM and AI-CS topics when the learner needs intuition,
formal reasoning, algorithms, proofs, code, or problem-solving transfer.

This is a STEM default, not the whole skill. For non-STEM subjects, use the
same teaching principle in discipline-appropriate form: context before claim,
evidence before interpretation, rule before application, audience before
revision, or usage before grammar label.

## Ideal Path

1. **Intuition:** Start with the mental picture, mechanism, or purpose.
2. **Concrete example:** Use a small case the learner can inspect.
3. **Formal definition:** State the precise idea after intuition exists.
4. **Notation or symbols:** Translate each symbol, variable, unit, data
   structure, or diagram element.
5. **Procedure or algorithm:** Show the repeatable steps.
6. **Why it works:** Explain the invariant, proof idea, physical mechanism,
   computational reason, or model assumption.
7. **Edge cases:** Show where the method fails, changes, or needs care.
8. **Common mistakes:** Name the tempting wrong moves.
9. **Practice:** Give a small item at the right ladder rung.
10. **Later connection:** Connect to later courses, projects, or real
    applications when useful.

Do not force every answer through all ten steps. Use the sequence to choose a
good path and stop when the learner has enough for the current turn.

## Math Example

- **Topic:** Matrix multiplication.
- **Intuition:** One transformation happens after another.
- **Concrete example:** Rotate a point, then scale it.
- **Formal definition:** The product `AB` represents applying `B` first, then
  `A`.
- **Notation:** Explain rows, columns, entries, and vector coordinates.
- **Procedure:** Compute dot products only after the composition meaning is
  clear.
- **Why it works:** Each column shows where a basis vector ends up after the
  composed transformation.
- **Edge case:** Order matters; usually `AB != BA`.
- **Practice:** Ask which transformation happens first in `ABx`.
- **Later connection:** Linear maps, graphics transforms, neural-network
  layers, and systems of equations.

## Programming Example

- **Topic:** Recursion.
- **Intuition:** A function solves a smaller version of the same problem.
- **Concrete example:** Count files inside a folder tree.
- **Formal definition:** Recursive functions call themselves and require a base
  case.
- **Notation:** Explain function call, argument, return value, stack frame, and
  base case.
- **Procedure:** Identify base case, recursive case, smaller input, and how
  results combine.
- **Why it works:** Each call reduces the problem until the base case stops the
  chain.
- **Edge case:** Missing base case or non-shrinking input causes infinite
  recursion.
- **Practice:** Ask the learner to mark the base case in a factorial function.
- **Later connection:** Trees, search, divide-and-conquer, parsing, and dynamic
  programming.

## AI/ML Example

- **Topic:** Gradient descent.
- **Intuition:** Move downhill on an error surface.
- **Concrete example:** Adjust one knob to reduce prediction error.
- **Formal definition:** Iteratively update parameters in the negative gradient
  direction to reduce a loss locally.
- **Notation:** Explain parameter, loss, gradient, learning rate, and update
  rule.
- **Procedure:** Predict, measure loss, compute gradient, update, repeat.
- **Why it works:** The gradient points toward steepest local increase, so the
  negative gradient points toward steepest local decrease.
- **Edge case:** Learning rate too large can overshoot; non-convex loss may
  have local minima or flat regions.
- **Practice:** Ask which way to move if the gradient points northeast.
- **Later connection:** Neural-network training, optimization, regularization,
  and numerical methods.

## Computer Systems Example

- **Topic:** Virtual memory.
- **Intuition:** Each process gets the illusion of its own private address
  space.
- **Concrete example:** Two programs both use address `0x1000` but map to
  different physical memory.
- **Formal definition:** A hardware/software mechanism translates virtual
  addresses to physical addresses using page tables and protection metadata.
- **Notation:** Explain virtual address, physical address, page, frame, page
  table entry, and fault.
- **Procedure:** CPU issues virtual address, MMU translates, permission is
  checked, memory is accessed or a fault occurs.
- **Why it works:** Indirection lets the OS isolate processes, control access,
  and move pages without changing program addresses.
- **Edge case:** Page faults are not always errors; they can load missing pages.
- **Practice:** Ask why virtual memory is not merely "more RAM."
- **Later connection:** Operating systems, architecture, security, performance,
  and memory debugging.

## Physics / Electronics / Signals Example

- **Topic:** Filtering a signal.
- **Intuition:** A filter keeps some patterns of change and reduces others.
- **Concrete example:** Smooth a noisy temperature reading by reducing rapid
  fluctuations.
- **Formal definition:** A filter changes a signal's frequency components or
  time-domain behavior according to a system response.
- **Notation:** Explain signal, amplitude, frequency, time domain, frequency
  domain, cutoff, and response.
- **Procedure:** Represent the signal, choose filter behavior, apply the filter,
  inspect output and distortion.
- **Why it works:** Many signals can be understood as combinations of slower
  and faster variations; filters weight those variations differently.
- **Edge case:** Filtering can remove useful detail or introduce delay.
- **Practice:** Ask whether a low-pass filter keeps slow trends or sharp noise.
- **Later connection:** DSP, communications, control systems, audio, sensors,
  and instrumentation.
