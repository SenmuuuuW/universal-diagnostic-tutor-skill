# Readiness Gate Protocol

Use this protocol to decide whether a learner should move beyond the current
concept. It formalizes readiness from observed evidence; it does not assign a
permanent label or predict exam performance.

`mastery_signal_interpretation_protocol.md` interprets individual learner
signals. `concept_mastery_map_protocol.md` records the compact concept status.
This protocol combines the available evidence into a readiness outcome.
`review_or_advance_decision.md` then chooses the concrete teaching move.

## Readiness Outcomes

| Outcome | Meaning |
| --- | --- |
| Advance | Evidence supports moving to the next dependent concept or a higher practice rung. |
| Advance with caution | Core understanding is usable, but transfer, consistency, or confidence evidence is limited; move on with an early check. |
| Review first | A specific current-concept gap should be repaired before advancing. |
| Step down | A prerequisite, notation, object-type, or overload problem requires a simpler level first. |
| Diagnose again | The target or evidence is missing, ambiguous, contradictory, or does not reveal the actual blocker. |
| More practice needed | The concept is understood enough to keep working at this level, but independent use is not stable yet. |

## Evidence To Inspect

Inspect evidence for the current concept, not general impressions of the
learner:

- **Explanation quality:** Can the learner state the main relationship or
  reason in their own words?
- **Practice answer correctness:** Does the response satisfy the targeted
  criteria?
- **Reasoning correctness:** Is the method valid, complete enough, and used for
  the right reason?
- **Near-transfer:** Can the learner use the idea when wording, numbers, data,
  or context changes slightly?
- **Confidence signal:** Was the response reasoned, hesitant, guessed, or
  heavily prompted? Self-reported confidence supports but does not replace
  performance evidence.
- **Repeated error pattern:** Does the same concept, method, notation, or setup
  error recur after repair?

Near-transfer and independent reasoning are stronger evidence than recognition
or repetition. Explanation alone and one lucky correct answer are not enough
to confirm readiness.

## Decision Rules

- Choose **Advance** when the learner gives sound reasoning and independent
  application, with near-transfer or trap evidence when the next concept
  depends strongly on transfer. No unresolved repeated blocker should remain.
- Choose **Advance with caution** when the core reasoning and an independent
  use are sound, but transfer or consistency has not been fully checked. Put a
  small check early in the next concept.
- Choose **Review first** when the evidence reveals one identifiable concept,
  method, setup, or reasoning gap that can be repaired locally.
- Choose **Step down** when the current task depends on a missing prerequisite,
  misunderstood notation or object type, or the learner is overloaded by the
  current representation.
- Choose **Diagnose again** when there is no usable attempt, reasoning is
  required but absent, signals conflict, or the current target is unclear.
- Choose **More practice needed** when the learner can follow or perform with
  support but independent use remains inconsistent. Keep practice targeted to
  the unstable step.

When several rules apply, choose the outcome tied to the earliest blocking
dependency. Do not average a prerequisite failure into an optimistic overall
decision.

## Concept Status Alignment

Use the preferred status terms from `concept_mastery_map_protocol.md`:

- `Advance` can support `confirmed` when the required evidence is present.
- `Advance with caution` usually remains `checked` until the missing evidence
  is observed; do not force `confirmed`.
- `More practice needed` remains `practiced`, `checked`, or `weak` according to
  the actual evidence.
- `Review first` commonly marks the current node `weak`.
- `Step down` commonly marks the dependent node `blocked` and the prerequisite
  `weak` or `unconfirmed`.
- `Diagnose again` keeps the node `unconfirmed` unless earlier evidence
  supports another status.

These are mappings, not automatic state changes. Preserve evidence that is
already valid.

## Urgent Exam Context

When time is short, compress the gate to the strongest available evidence and
one high-value check. The tutor may choose `Advance with caution` to prioritize
coverage, but must state that transfer or consistency remains uncertain. Do not
turn urgency into score guarantees, exam prediction, or fake mastery.

## Output Shape

1. **Current concept**
2. **Evidence observed**
3. **Readiness decision**
4. **Reason**
5. **Next step**
6. **State update note**

Keep the learner-facing wording natural. Record the readiness status in a
visible Learning State Card or Learning Task Card when continuity, an active
task, or a learner request makes that useful.

## Anti-Patterns

- Marking mastery because the tutor explained the concept.
- Advancing after one unsupported correct answer.
- Requiring a long test when one near-transfer check would resolve the
  uncertainty.
- Repeating easy recognition tasks after transfer is already demonstrated.
- Hiding uncertainty behind a rigid score or permanent learner label.
