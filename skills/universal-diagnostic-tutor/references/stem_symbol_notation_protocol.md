# STEM Symbol And Notation Protocol

Use this protocol when a learner is stuck on symbols, formulas, notation,
definitions, diagrams, code-like math, or technical vocabulary.

When notation is the blocker, pause the problem. Translate before manipulating.

## Core Sequence

1. **Name the notation.** Say what expression, symbol, or definition is causing
   trouble.
2. **Translate into plain language.** Explain what it says before using it.
3. **Identify each symbol's role.** Say what each part stands for.
4. **Name the object type.** Scalar, vector, matrix, function, set, graph,
   probability, random variable, parameter, tensor, process, pointer, register,
   state, signal, or another relevant object.
5. **Separate what it is from what it does.** A matrix may be an array of
   numbers; it may also represent a transformation.
6. **Use a small numerical or concrete example.** Only then return to the
   general formula.
7. **Connect meaning.** Link notation to geometry, computation, physical
   measurement, data flow, or system behavior.
8. **Check.** Ask one small question about the role or object type.

## What It Is Vs What It Does

Distinguish these explicitly:

- **What it is:** the type of mathematical, computational, or physical object.
- **What it does:** the operation, relationship, transformation, measurement,
  or role it has in the task.

Example:

```text
`A` is a matrix. In `Ax = b`, it acts like a transformation that turns vector
`x` into vector `b`.
```

## Domain Calibration

### Math

Connect notation to quantity, geometry, transformations, sets, functions,
proof roles, and constraints.

### Programming / CS

Connect notation to data structures, memory, runtime behavior, state, pointers,
references, scope, control flow, and implementation.

### AI / ML

Connect notation to data, features, labels, model parameters, loss, gradients,
embeddings, tensors, batches, and evaluation metrics.

### Systems

Connect notation to layers: program view, OS abstraction, hardware mechanism,
memory address, register, page, packet, process, thread, file descriptor, or
protocol field.

### Physics / Electronics / Signals

Connect notation to measurable quantities, units, dimensions, time-varying
signals, frequency, voltage, current, energy, force, state, and uncertainty.

## Anti-Patterns

- Manipulating symbols before explaining what they represent.
- Treating all symbols as numbers when some are functions, vectors, matrices,
  distributions, tensors, processes, or states.
- Explaining only the formal definition when the learner needs object type and
  role.
- Using a large general formula when a small numerical example would reveal the
  meaning faster.
