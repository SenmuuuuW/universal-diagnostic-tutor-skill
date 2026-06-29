# Difficulty Adjustment Protocol

Use this protocol to decide whether to decrease, maintain, or increase
difficulty during tutoring. Difficulty is not just hard versus easy; it can
come from abstraction, notation, steps, proof rigor, code complexity, system
layers, or too many sources at once.

The goal is a productive challenge: hard enough to build mastery, small enough
that the learner can make the next move.

Difficulty adjustment should serve the learning-efficiency loop: choose the
lowest sufficient difficulty for the next best teaching step, then adjust after
the learner's signal.

## Decrease Difficulty

Decrease when the learner shows confusion, repeated wrong answers, notation
issues, prerequisite gaps, overload, or inability to explain the current step.

Good moves:

- Use a smaller numerical example.
- Replace notation with words temporarily.
- Move from proof to intuition or invariant story.
- Move from full code to a trace table.
- Reduce the number of variables, layers, cases, or sources.
- Ask one recognition or confidence check.

Avoid making the same explanation longer. Step down by changing the
representation or reducing the cognitive load.

## Maintain Difficulty

Maintain when the learner follows the explanation but still needs guided
practice, a reasoning check, or one more scaffolded step.

Good moves:

- Ask the learner to complete the next step.
- Keep the same problem but remove one hint.
- Ask them to explain why a step is valid.
- Give a near-identical practice item.

Avoid jumping to transfer too soon.

## Increase Difficulty

Increase when the learner explains reasoning, solves without hints, catches a
mistake, or handles near-transfer.

Good moves:

- Give a near-transfer problem.
- Add one edge case or trap.
- Mix two similar methods and ask them to classify.
- Ask for a proof reason, code trace, unit check, or transfer cue.
- Move from guided application to independent application.

Avoid declaring full mastery after a single correct answer.

## Switch Representation When Stuck

If the learner is stuck after one explanation, keep the same core idea but
change the representation:

- Formula -> diagram.
- Diagram -> small numbers.
- Code -> trace table.
- Abstract definition -> concrete example.
- Proof -> invariant story.
- Dense notation -> object-role list.
- Source summary -> direct teaching path.

If the learner is stuck twice, switch representation rather than repeating or
adding more details.

## STEM / AI-CS Difficulty Dimensions

Adjust one dimension at a time when possible.

- **Abstraction level:** Concrete example, mental model, formal definition,
  general theorem, or architecture.
- **Notation density:** Few symbols, translated symbols, full formula, or dense
  derivation.
- **Number of steps:** One-step check, worked step, full procedure, or multi-
  stage problem.
- **Conceptual load:** One concept, contrast of two concepts, or several
  interacting concepts.
- **Computational load:** Small numbers, symbolic manipulation, larger
  calculation, or numerical/algorithmic workload.
- **Proof rigor:** Intuition, invariant, informal proof, formal proof, or edge
  case analysis.
- **Coding complexity:** Single line, trace, function, multiple functions,
  data structure, or system interaction.
- **System layers:** Program behavior, runtime, OS abstraction, hardware,
  network, or distributed system.
- **Amount of source material:** No source, one supporting source, a small
  curated set, or a longer study path.

## Quick Decision Cues

- Confused or overwhelmed: decrease.
- Following but dependent on hints: maintain.
- Correct answer without explanation: maintain and check reasoning.
- Correct explanation: increase gradually.
- Independent solution: increase to transfer or application.
- Same mistake repeats: decrease to prerequisite or misconception repair.
- Known prerequisite: compress it and focus on the new blocker.
