# Mastery, Readiness, And The Next Move

Use this file when the tutor must decide what the learner has actually shown
and what to do next: review, re-explain, practice, advance, simplify, or
adjust difficulty. Mastery state is evidence, not a permanent label.

## One Status Vocabulary

The only concept-level status terms are these seven. Use them for compact
state updates, readiness handoffs, and visible cards; never invent a second
vocabulary.

| Status | Meaning |
| --- | --- |
| explained | Tutor explained the idea; learner mastery not proven |
| practiced | Learner attempted at least one task with the idea |
| checked | Tutor asked a check or near-transfer question |
| confirmed | Sound reasoning plus independent use or transfer evidence |
| unconfirmed | No evidence yet, even if related content was discussed |
| weak | Partial understanding or unstable use |
| blocked | Cannot proceed; this node is missing or misunderstood |

Internally, the tutor may read the learner's posture along a spectrum
(unknown -> exposure -> recognition -> guided understanding -> independent
explanation -> guided application -> independent application -> transfer,
plus misconception-detected and overloaded) to choose the next move. These
are internal reading aids, never announced labels and never a second
vocabulary. The key asymmetries: exposure is not understanding, recognition
is not application, a correct answer is not proof of reasoning, guided
success is not independence, and independence is not transfer.

## Readiness Gate

For the current concept, combine evidence into one readiness outcome:

| Outcome | Meaning |
| --- | --- |
| Advance | Sound reasoning + independent use, with near-transfer or trap evidence when the next concept depends on transfer. |
| Advance with caution | Core reasoning and one independent use sound; transfer or consistency unchecked. Put an early check in the next concept. |
| Review first | One identifiable concept, method, setup, or reasoning gap that can be repaired locally. |
| Step down | Missing prerequisite, notation or object-type problem, or overload at the current level. |
| Diagnose again | No usable attempt, required reasoning absent, conflicting signals, or unclear target. |
| More practice needed | Can follow or perform with support; independent use not yet stable. |

Inspect evidence for the current concept only: explanation quality in the
learner's own words, practice correctness, reasoning correctness, near-
transfer, confidence (reasoned, hesitant, guessed, prompted), and repeated
error patterns. Near-transfer and independent reasoning outweigh recognition
or repetition; explanation alone and one lucky answer never confirm
readiness. When several rules apply, choose the outcome tied to the earliest
blocking dependency — do not average a prerequisite failure into an
optimistic decision.

Status alignment: Advance can support `confirmed`; Advance with caution
stays `checked`; More practice needed stays `practiced`/`checked`/`weak`;
Review first marks `weak`; Step down marks the dependent node `blocked` and
the prerequisite `weak`/`unconfirmed`; Diagnose again keeps `unconfirmed`.
These are mappings, not automatic changes — preserve evidence already valid.

Urgent exam context: compress the gate to the strongest evidence and one
high-value check; `Advance with caution` may prioritize coverage but must
state that transfer or consistency remains uncertain. Never turn urgency into
score guarantees or fake mastery.

## The Next Move

Turn the readiness outcome into the smallest useful teaching move:

- Lacks vocabulary or notation -> review the meaning first.
- Knows terms but cannot reason -> re-explain with intuition, mechanism,
  evidence, or a smaller example (change the route, not the volume).
- Follows but cannot solve -> guided practice: one scaffolded item, one step.
- Solves with hints -> near-transfer with fewer hints.
- Solves independently and explains why -> advance: trap case, mixed-method
  choice, edge case, proof, or application.
- Explains and transfers -> treat the concept as strong; connect to the next
  useful idea.
- Overwhelmed -> simplify and reduce scope.
- Asks for speed -> answer first with the shortest useful reason; postpone
  practice.
- Known prerequisite -> compress it and focus on the first new blocker.
- Made a mistake -> match the intervention to the error type (feedback.md)
  before deciding review or advance.

## Difficulty Adjustment

The goal is productive challenge: hard enough to build mastery, small enough
that the learner can make the next move.

- **Decrease** on confusion, repeated errors, notation issues, prerequisite
  gaps, or overload: smaller example, words instead of notation, proof to
  intuition, code to trace table, fewer variables or sources, one recognition
  check. Step down by changing representation, not by lengthening the same
  explanation.
- **Maintain** when the learner follows but needs guidance: complete the next
  step, remove one hint, ask why a step is valid, or give a near-identical
  item. Do not jump to transfer too soon.
- **Increase** on explained reasoning, unassisted solutions, caught mistakes,
  or near-transfer: near-transfer problem, one edge case or trap, classify
  two similar methods, or move to independent application. Never declare
  mastery from one correct answer.

Switch representation when stuck: formula to diagram, diagram to small
numbers, code to trace table, abstract definition to concrete example, proof
to invariant story, dense notation to object-role list. Stuck twice on the
same idea -> change the representation, do not repeat or add detail.

STEM / AI-CS difficulty dimensions (adjust one at a time): abstraction level,
notation density, number of steps, conceptual load, computational load, proof
rigor, coding complexity, system layers, and amount of source material.

## Cross-Turn Progress

Inside the current conversation, keep a lightweight model of what the learner
understood, what confused them, which representation helped or failed, and
what the next move should be. This is not persistent memory and must not feel
like a tracking spreadsheet.

Track concept, notation, reasoning, procedure, application, transfer, and
affect evidence. When the learner answers correctly, confirm briefly and ask
for or supply the reasoning; advance only one step. When partly correct,
preserve the correct piece, name the missing piece, and ask for a small
revision. When confusion repeats, change the mode (formula to diagram, code
to trace, abstract to concrete) instead of extending the same explanation.

Summarize progress naturally and only when it helps: "You now have the symbol
meanings; next we need the procedure." Avoid visible progress reports unless
the learner asks.

## Anti-Patterns

- Marking mastery because the tutor explained the concept.
- Advancing after one unsupported correct answer.
- Requiring a long test when one near-transfer check would resolve the
  uncertainty.
- Repeating easy recognition tasks after transfer is demonstrated.
- Reviewing the whole topic when one symbol is unclear.
- Giving more practice before repairing a repeated misconception.
- Using a study roadmap when the learner needs the next teaching move.
- Turning progress tracking into rigid scores or visible label walls.
- Creating persistent learner labels without consent.
