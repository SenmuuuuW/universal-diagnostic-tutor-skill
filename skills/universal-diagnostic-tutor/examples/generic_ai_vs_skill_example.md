# Generic AI Vs Skill Example

## User Question

"Solve `2x + y = 7` and `x - y = 2`, but don't just give me the answer. I want
to understand elimination."

## Diagnosis

- **Subject routing:** Algebra / linear systems.
- **Likely gap:** Procedure and reasoning gap around elimination.
- **Task:** Teach method without finishing too early.

## Expected Pacing Choice

Set up elimination and stop before the key operation so the learner chooses the
next step.

## Autonomous Search

Not needed. This is a small procedural concept. If the learner later asks for
practice, search for open algebra practice only if useful.

## Source Selection Logic

No source required; use teacher-like stop points.

## Bad Generic AI Answer

Add the equations:

```text
2x + y = 7
x - y = 2
---------
3x = 9
x = 3
```

Then plug in:

```text
3 - y = 2
y = 1
```

Answer: `x = 3`, `y = 1`.

## Good Diagnosis-First Skill Answer

You are trying to understand elimination, so I will stop before the key move.

Elimination means: combine equations so one variable disappears.

Here are the equations:

```text
2x + y = 7
x - y = 2
```

Look at the `y` terms:

```text
+y
-y
```

That is the useful cue. If we combine the equations in the right way, those two
terms cancel.

Stop here: should we add the equations or subtract them to make `y` disappear?

## Stop Point Or Check Question

"Should we add the equations or subtract them to make `y` disappear?"

## Why This Is Better Than A Generic AI Answer

The generic answer finishes the problem. The Skill answer identifies the method
cue, leaves the key decision to the learner, and checks whether they understand
why elimination works before calculating.
