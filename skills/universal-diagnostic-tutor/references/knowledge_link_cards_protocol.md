# Knowledge Link Cards Protocol

Use Knowledge Link Cards when a strongly related concept is necessary to
resolve the learner's current gap. A card should make the connection usable for
a beginner instead of mentioning a required concept in one vague sentence.

Cards support teaching, practice, grading, and readiness. They do not replace
the current task, become a textbook chapter, or create a broad curriculum map.

## Use A Card When

- a beginner needs a prerequisite concept to follow the current explanation
- a beginner explicitly asks why required concepts appear together or says a
  one-line mention is not enough
- a broad-topic learner needs one strong connection made explicit
- the tutor has mentioned a related concept that is required for the next step
- the learner cannot proceed without understanding how two concepts connect
- grading reveals a missing prerequisite
- a study plan names a required subtopic whose role is unclear to the learner

Before creating a card, ask: "Would understanding this connection change the
learner's next attempt?" If not, omit it.

When the learner explicitly asks for beginner-friendly explanation of several
required concepts, use the card shape and one check in the first turn. Do not
add a formal derivation in that turn unless the learner explicitly requests
one, and do not replace the cards with a longer equation-first lecture.

## Do Not Use A Card When

- the concept is only weakly related or merely interesting
- the learner asked for a quick answer and the connection is not required
- a one-sentence definition is already sufficient
- the cards would turn the response into a wiki or course map
- more than three cards would be required to explain the branch

If more than three concepts appear essential, identify the earliest blocker
and card only that node first.

## Card Shape

Each card contains:

- **Knowledge point:** The related concept.
- **What it is:** A short, beginner-usable meaning.
- **Why it matters here:** Why the current task depends on it.
- **How it connects to the current topic:** The direct relationship, not a
  broad association.
- **Minimum mastery needed now:** What the learner must be able to recognize,
  explain, or do before returning.
- **Skip for now:** Advanced details that are not needed for the current task.
- **Small example:** One concrete example that exposes the connection.

Use one to three cards at most. Keep each card short but more informative than
a one-line name drop.

## Integration With The Practice Loop

1. Identify the current task and the strong blocking connection.
2. Explain only the minimum needed through the card.
3. Ask one tiny check when the connection needs learner evidence.
4. Stop and wait if the check requires an answer.
5. Return explicitly to the original explanation, exercise, correction, or
   readiness decision after the check.

When grading exposes the blocker, first classify the mistake through the
mistake and intervention protocols. Use a card only when the repair requires a
related concept; do not turn every error into a card.

## Example

**Knowledge point:** Matrix

- **What it is:** A rectangular table of numbers arranged in rows and columns.
- **Why it matters here:** Machine-learning datasets are often represented as
  matrices.
- **How it connects to the current topic:** Rows can represent samples and
  columns can represent features.
- **Minimum mastery needed now:** Understand row, column, shape, and simple
  matrix-vector multiplication.
- **Skip for now:** Eigenvalues, SVD, and rigorous proofs.
- **Small example:** Data for 3 people with 2 measured features forms a
  \(3 \times 2\) matrix.

Return to the current machine-learning task after checking that the learner can
identify the samples and features.

## Style Rules

- Use the learner's language and current notation level.
- Explain the link directly; do not dump resources unless requested.
- Keep optional history, proofs, edge cases, and adjacent topics out of the
  card unless they are required now.
- Use a small visual only when `basic_stem_visualization_protocol.md` indicates
  it would clarify the relationship.
- Preserve math formatting with `\(...\)` and `\[...\]`.

## Anti-Patterns

- Listing related terms without explaining their role.
- Adding cards for every node in a knowledge map.
- Using a card as a detour that never returns to the learner's task.
- Hiding a full lecture inside `Minimum mastery needed now`.
- Treating card exposure as mastery without a learner check.
