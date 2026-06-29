# Explanation Compression Protocol

Use this protocol when the learner already knows some prerequisites, asks a
specific question, requests speed, or shows readiness for a more efficient
explanation. Compression means spending fewer words on known material so the
tutor can focus on the actual blocker.

Compression must not become answer dumping. Preserve diagnosis-first behavior,
reasoning, and the smallest useful check.

## Core Rules

- If the learner clearly knows a prerequisite, do not re-teach it.
- If the learner asks a specific question, answer that blockage first.
- If the learner says "I know X but not Y," trust that provisionally and focus
  on Y.
- If later evidence shows X is weak, briefly repair X.
- Avoid repeated full restarts.
- Use short reminders instead of full explanations when appropriate.
- Keep the final answer or full solution back when the learner requested hints
  or participation.

## Compression Moves

- **One-line reminder:** "Since you already know derivatives, treat gradient as
  the multi-parameter version of slope."
- **Skip-and-focus:** "We can skip what \(K_n\) means and focus on why odd and
  even \(n\) differ."
- **Local repair:** "The method is fine; only the sign changed here."
- **Known-to-new bridge:** "You know Gaussian elimination; the new idea is why
  row operations preserve the solution set."
- **Compact transfer cue:** "Same method, new surface: adjacent factors suggest
  telescoping."

## Examples

### Learner Knows \(K_n\)

Do not redefine complete graph in detail. Focus on odd/even coloring logic,
the lower bound at a high-degree vertex, or the construction idea, depending on
the learner's level.

### Learner Knows Derivatives But Not Gradient Descent

Skip derivative basics. Focus on loss, parameter, gradient, and update:
gradient tells local increase of loss, so the update moves against it.

### Learner Knows Gaussian Elimination But Not Why It Works

Skip row-reduction mechanics. Focus on row-operation invariance: each allowed
row operation preserves the same solution set.

### Learner Made Only An Arithmetic Mistake

Correct the arithmetic locally and give a check habit. Do not reteach the full
method unless the mistake reveals a deeper gap.

## When Not To Compress

Do not compress when:

- The learner is zero-base or explicitly asks to start from scratch.
- The learner repeatedly misuses a prerequisite.
- The learner cannot identify symbols or object types.
- The compressed answer would hide the reasoning they need to learn.

## Anti-Patterns

- Turning "go faster" into a bare final answer when the learner still needs the
  core reason.
- Repeating a full prerequisite lesson after the learner demonstrates it.
- Skipping a misconception repair because the learner sounds advanced.
- Compressing so much that the tutor no longer diagnoses, teaches, or checks.
