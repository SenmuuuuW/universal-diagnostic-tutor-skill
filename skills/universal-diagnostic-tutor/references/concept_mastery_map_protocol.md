# Concept Mastery Map Protocol

Use this protocol when a learner is moving across related concepts and the
tutor needs to avoid assuming mastery too early.

A Concept Mastery Map is a small status view for important nodes. It can appear
inside a Learning State Card, Learning Task Card, or short progress summary.
It is not hidden memory, a gradebook, a database, or a rigid label system.

## Status Terms

| Status | Meaning |
| --- | --- |
| explained | Tutor has explained the idea, but learner mastery is not proven |
| practiced | Learner attempted at least one task with the idea |
| checked | Tutor asked a check or near-transfer question |
| confirmed | Learner showed understanding through explanation, independent use, or transfer |
| unconfirmed | No evidence yet, even if related content was discussed |
| weak | Evidence shows partial understanding or unstable use |
| blocked | Learner cannot proceed because this node is missing or misunderstood |

## Rules

- Do not mark a concept as mastered just because it was explained.
- Keep related future concepts unconfirmed unless checked.
- Before moving to the next node, ask a small mastery check when the step
  depends on the current node.
- Preserve correct evidence and repair weak evidence; do not restart from zero
  unnecessarily.
- Store important mastery status in a visible Learning State Card or Learning
  Task Card when the learner wants continuity.
- Avoid rigid scores unless the user explicitly asks for a rubric.

## Example: Parallel Vectors

```text
Concept Mastery Map:
- parallel vectors mean scalar multiples: explained, checked
- identifying \(v\) and \(2v\): confirmed
- proportional component test: unconfirmed
- relation to span: unconfirmed
- relation to linear combination: unconfirmed
- scalar multiple vs component equality: weak

Next step: repair scalar multiple vs component equality with one near-transfer
check.
```

## Advancement Rule

Advance when the learner can do one of these:

- explain the concept in their own words
- use it independently in a near case
- identify a trap or misconception
- transfer the cue to a slightly changed problem

If the learner can only repeat a phrase or follow one worked example, keep the
node as practiced or checked, not confirmed.

## Mistakes To Avoid

- Treating explanation as mastery.
- Treating one correct guess as confirmed mastery.
- Marking an entire chapter as learned after one subtopic.
- Showing too many status labels to the learner when natural wording would be
  clearer.
- Creating persistent learner labels that follow the user without consent.
