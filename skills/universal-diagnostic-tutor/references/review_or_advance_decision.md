# Review Or Advance Decision

Use this guide when deciding whether the next tutor move should be review,
re-explanation, guided practice, near-transfer, advancement, or simplification.
The decision should follow evidence from the learner, not the tutor's desire to
finish the topic quickly.

For V1.4, choose the action that produces the highest learning gain for the
smallest reasonable explanation cost.

`readiness_gate_protocol.md` owns the explicit readiness outcome: Advance,
Advance with caution, Review first, Step down, Diagnose again, or More practice
needed. This file turns that outcome into the smallest useful teaching move. Do
not use this guide to bypass the gate when progression to a dependent concept
matters.

## Decision Rules

- If the learner lacks vocabulary or notation, review the meaning first.
- If the learner knows terms but cannot reason, re-explain with intuition,
  mechanism, evidence, or a smaller example.
- If the learner follows the explanation but cannot solve, give guided
  practice.
- If the learner solves with hints, give near-transfer with fewer hints.
- If the learner solves independently, advance to a harder variation, trap
  case, or transfer task.
- If the learner can explain and transfer, treat the current concept as strong
  understanding and connect to the next useful idea.
- If the learner is overwhelmed, simplify and reduce scope.
- If the learner asks for speed, answer first and postpone practice.
- If the learner knows a prerequisite, compress that part and focus on the
  first new blocker.
- If the learner makes a mistake, match the intervention to the error type
  before deciding whether to review or advance.

## Review

Choose review when the blocker is terminology, notation, prerequisite facts,
or a prior concept.

Example:

```text
Before solving `Ax = b`, let's review what kind of objects `A`, `x`, and `b`
are. Otherwise row reduction will feel like symbol pushing.
```

## Re-Explain

Choose re-explanation when the learner has heard the content but cannot state
why it works.

Good re-explanation changes the route:

- Use intuition instead of the formula.
- Use a concrete case instead of the abstract rule.
- Use a trace instead of code.
- Use an invariant story instead of formal proof steps.

## Guided Practice

Choose guided practice when the learner can follow but not yet do the method.
Give one scaffolded item and ask for one step.

Example:

```text
I'll set up the base case; you choose the smaller recursive input.
```

## Near-Transfer

Choose near-transfer when the learner succeeded with hints or completed a
worked example. Change one surface detail while preserving the structure.

Example:

```text
You solved factorial with help. Now try summing a list: what is the base case?
```

## Advance

Choose advance when the learner solves independently and can explain the main
reason. Advancement can mean a trap case, mixed-method choice, edge case,
formal proof, or real application.

Example:

```text
You can solve the derivative. Now let's check whether you can explain when the
same limit-definition idea applies to a different function.
```

## Simplify

Choose simplification when the learner is overwhelmed, mixing several ideas, or
missing a prerequisite. Reduce scope before adding practice.

Example:

```text
Let's drop the matrix notation for one minute and use one input, one slope, and
one update. Then we will return to the full gradient formula.
```

## Speed Mode

When the learner asks for speed, give the answer first with the shortest useful
reason. Do not force practice in that turn. You may add a compact offer such as
"I can walk through why afterward."

## Avoid These Decisions

- Advancing because the learner got one answer right but gave no reason.
- Reviewing the whole topic when only one symbol is unclear.
- Re-explaining a known prerequisite instead of compressing and moving to the
  current blocker.
- Giving more practice before repairing a repeated misconception.
- Using a study roadmap when the learner needs the next teaching move.
- Turning progress tracking into rigid scores or unnecessary visible state
  labels.
