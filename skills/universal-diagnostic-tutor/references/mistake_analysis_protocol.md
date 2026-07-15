# Mistake Analysis Protocol

Use this protocol when the learner shows work, gives an answer, asks what went
wrong, or repeats an error. Treat mistakes as diagnostic evidence, not as a
reason to simply reveal the solution.

## Protocol Boundary

`answer_grading_protocol.md` owns the qualitative verdict and the accounting
of what is correct or missing. This protocol explains the mistake and its
underlying gap. After diagnosis, use `error_to_intervention_protocol.md` to
choose the smallest repair, then return to `learning_task_loop_protocol.md` for
practice, state update, and readiness. Do not repeat the full grading output
here.

## Core Sequence

1. **Identify the surface mistake.** Point to the exact line, word, assumption,
   calculation, code behavior, interpretation, or choice that changed the path.
2. **Identify the underlying gap.** Decide whether the issue is vocabulary,
   concept, notation, procedure, reasoning, recognition, transfer,
   misconception, confidence, or resource selection.
3. **Separate careless from conceptual.** A slip needs a check habit; a
   conceptual error needs model repair.
4. **Explain why the wrong path felt tempting.** This lowers shame and reveals
   the faulty cue.
5. **Repair the misconception or missing prerequisite.** Teach the smallest
   idea needed to prevent the error.
6. **Give a similar but slightly changed practice task.** Keep it close enough
   to target the same gap.
7. **Summarize a prevention rule.** Give the learner a reusable check.

## Careless Error Or Conceptual Error?

- **Likely careless:** The learner explains the correct idea but made an
  arithmetic, sign, typo, copying, unit, syntax, or attention slip.
- **Likely conceptual:** The same wrong move is repeated, the learner cannot
  justify the step, or the error reveals a false model.

For careless errors, teach a check strategy. For conceptual errors, repair the
model before giving more practice.

## Common Mistake Types

### Misread Question

- **Signal:** The learner answers a different task than the one asked.
- **Tutor move:** Restate the task in simpler words and underline the demanded
  output.
- **Prevention rule:** "Before solving, name what the question is asking for."

### Memorized Formula Without Meaning

- **Signal:** The learner uses a formula correctly shaped but cannot explain
  what its parts represent.
- **Tutor move:** Translate each symbol into the story, unit, object, or role.
- **Prevention rule:** "Do not plug in until every symbol has a meaning."

### Applied Wrong Rule

- **Signal:** A familiar rule appears in a context where its conditions do not
  hold.
- **Tutor move:** Contrast the rule's valid case with the current case.
- **Prevention rule:** "Check the conditions before using the rule."

### Skipped Prerequisite

- **Signal:** The learner jumps into a procedure but misses an earlier concept
  needed for the step.
- **Tutor move:** Pause the solution and rebuild the missing prerequisite with a
  smaller example.
- **Prevention rule:** "If a step feels magical, find the earlier idea it uses."

### Chose Answer By Intuition Only

- **Signal:** The learner picks a plausible answer without evidence, formula,
  proof, code trace, or explicit reasoning.
- **Tutor move:** Respect the intuition, then test it against the relevant
  structure or data.
- **Prevention rule:** "Use intuition to guess, then use reasoning to check."

### Confused Similar Concepts

- **Signal:** The learner mixes demand/supply, correlation/causation,
  syntax/semantics, average/instant rate, or similar pairs.
- **Tutor move:** Make a two-column contrast with recognition cues.
- **Prevention rule:** "Ask which concept fits the cue in the problem."

### Calculation Or Syntax Error

- **Signal:** The concept is right but the arithmetic, algebra, code syntax,
  punctuation, or grammar form breaks the result.
- **Tutor move:** Show the local correction and add a check habit.
- **Prevention rule:** "Verify the small mechanics before trusting the final
  answer."

### Overgeneralized From One Example

- **Signal:** The learner treats a pattern from one case as a universal rule.
- **Tutor move:** Give a counterexample or edge case, then state the real
  boundary of the pattern.
- **Prevention rule:** "Ask where this pattern stops working."

## Near-Match Practice

After the repair, use one similar problem with a small change:

- Change numbers but keep structure for procedure errors.
- Change surface story but keep concept for recognition errors.
- Add a tempting trap for misconception errors.
- Ask for a short explanation for reasoning errors.

The goal is not volume. The goal is to see whether the repaired idea transfers.
Use `exercise_generation_protocol.md` to construct that item against the
selected rung and grading criteria.
