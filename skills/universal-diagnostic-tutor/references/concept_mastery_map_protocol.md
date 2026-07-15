# Concept Mastery Map Protocol

Use this protocol when a learner is moving across related concepts and the
tutor needs to avoid assuming mastery too early.

A Concept Mastery Map is a small status view for important nodes. It can appear
inside a Learning State Card, Learning Task Card, or short progress summary.
It is not hidden memory, a gradebook, a database, or a rigid label system.

The status terms below are the preferred V1.9 terms for concept-level state.
Use them for compact state updates and readiness handoffs instead of inventing
a second status vocabulary.

## Status Terms

| Status | Meaning |
| --- | --- |
| explained | Tutor has explained the idea, but learner mastery is not proven |
| practiced | Learner attempted at least one task with the idea |
| checked | Tutor asked a check or near-transfer question |
| confirmed | Learner showed sound reasoning plus independent use or transfer evidence |
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

## Status Updates After Practice

- Mark an attempted concept `practiced`, even when the attempt is not correct.
- Mark it `checked` after the response has been evaluated against a targeted
  check or near-transfer task.
- Use `weak` when evidence is partial or unstable, and `blocked` when an
  unresolved prerequisite prevents progress.
- Use `confirmed` only when learner evidence supports the readiness gate. An
  explanation, exposure, completed example, or lucky answer is insufficient.
- Preserve `unconfirmed` for related nodes that were mentioned but not tested.

`answer_grading_protocol.md` supplies attempt evidence.
`readiness_gate_protocol.md` owns the explicit advance decision.

## Readiness Evidence

Useful readiness evidence includes whether the learner can:

- explain the concept in their own words
- use it independently in a near case
- identify a trap or misconception
- transfer the cue to a slightly changed problem

These are evidence types, not automatic pass conditions. Apply the readiness
gate and consider reasoning quality, independence, transfer, confidence, and
repeated errors together. If the learner can only repeat a phrase or follow one
worked example, keep the node as `practiced` or `checked`, not `confirmed`.

## Mistakes To Avoid

- Treating explanation as mastery.
- Treating one correct guess as confirmed mastery.
- Marking an entire chapter as learned after one subtopic.
- Showing too many status labels to the learner when natural wording would be
  clearer.
- Creating persistent learner labels that follow the user without consent.
