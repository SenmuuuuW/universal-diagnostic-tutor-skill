# STEM Problem-Solving Protocol

Use this protocol when the learner asks to solve, understand, debug, derive,
model, or practice a STEM / AI-CS problem.

The goal is to teach the method, not merely finish the problem.

## General STEM Sequence

1. **Identify the target quantity or objective.** What are we solving for,
   proving, debugging, optimizing, predicting, or explaining?
2. **List known information.** Given values, constraints, code behavior,
   assumptions, diagrams, units, data, or system state.
3. **Identify the underlying concept.** Rate of change, conservation,
   recursion, conditioning, transformation, abstraction layer, etc.
4. **Choose a representation.** Equation, diagram, table, code trace, graph,
   vector, state machine, circuit, probability tree, or memory layout.
5. **Solve step by step.** Make each step small enough to follow.
6. **Explain why each step was chosen.** Tie moves to concepts, not just rules.
7. **Check the result.** Units, edge cases, complexity, reasonableness,
   dimensions, invariants, test case, or limiting behavior.
8. **Summarize the reusable method.** Name when to use it again.
9. **Give near-transfer practice.** Change one surface detail while preserving
   the structure.

## Coding And Debugging

Use this loop:

```text
observe -> hypothesize -> isolate -> test -> fix -> explain
```

- Observe actual vs expected behavior.
- Hypothesize the smallest likely cause.
- Isolate the line, state change, data flow, type, scope, or control path.
- Test the hypothesis with a small input or print/trace.
- Fix the cause.
- Explain why the fix changes the behavior.

## Algorithms

Use this progression:

```text
brute force -> pattern -> data structure -> complexity
```

- Start with the simple but possibly slow method.
- Find repeated work, ordering, search space, or invariant.
- Choose the data structure or algorithmic pattern that uses that structure.
- Explain time and space complexity from the operations performed.

## Machine Learning

Use this progression:

```text
data -> model -> loss -> optimization -> evaluation
```

- Identify inputs, labels, features, and distribution assumptions.
- Explain what the model computes.
- Explain what the loss measures.
- Explain how optimization changes parameters.
- Explain how evaluation checks generalization.

## Representation Choices

- Use equations for relationships between quantities.
- Use diagrams for geometry, physics, circuits, and systems.
- Use tables for states, cases, probabilities, or traces.
- Use code traces for programming behavior.
- Use graphs or vectors for structure and transformations.
- Use state machines for protocols, parsers, and control logic.

## Anti-Patterns

- Solving before naming the target.
- Plugging into formulas before explaining why that formula applies.
- Ignoring units, edge cases, complexity, or reasonableness.
- Fixing code without explaining the mental model.
- Ending without a transfer rule or practice step when the learner is studying.
