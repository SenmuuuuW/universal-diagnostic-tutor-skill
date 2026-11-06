# Evidence and Interaction Contract

This file defines what the runtime records and what you, the teaching brain, may
conclude. The short rule:

> **Recording an answer is not judging it. Completing an interaction is not
> mastery. Only the tutor makes a teaching judgement.**

## 1. Interaction vs Evidence

| Event | Runtime record | Does it become evidence automatically? |
| --- | --- | --- |
| Learner opens a lesson / moves a slider / views a step-through | Presentation state (`attempt.study`) | **No** |
| Learner answers a `quiz` | `attempt.responses[]` (quiz) | **Yes — one neutral `practice` observation** on the bound node, never correctness |
| Learner submits a `flashcard` self-report | `attempt.responses[]` (flashcard) | **Yes — one neutral `practice` observation**; it also feeds the review queue |
| Learner answers a `check` in the chat | No block response exists; the tutor observes it in conversation | **Only if the tutor records it** with `udt_map_update` `op: "add-evidence"`, `evidenceKind: "check"`, with the active `attemptId` |
| Learner explains/uses a concept in conversation | No automatic record | **Only if the tutor records** `explanation` / `check` / `transfer` evidence |

A repeated quiz/flashcard submission updates the response snapshot but does not
duplicate the practice evidence. Still, treat re-submission as one interaction,
not as a new proof.

## 2. What Each Kind Means

- `goal-stated` — the learner stated the goal.
- `diagnosis` — a gap, prerequisite or blocker was identified.
- `explanation` — the learner explained something in their own words.
- `practice` — the learner attempted a task; **never enough alone to confirm**.
- `check` — a check or near-transfer question was asked and answered; may support
  `checked`, but is not a mastery verdict.
- `transfer` — independent use or transfer; may support `confirmed` only after the
  tutor's own readiness judgement.

`confirmed` still requires the tutor's judgement and the runtime's structural
floor. The runtime does not calculate it from answers.

## 3. The Check Gap

A `check` block has no input box. When the learner answers it in the chat, the
answer exists only in conversation until the tutor records it.

After a real learner answer, if it is useful evidence, call:

```json
{
  "op": "add-evidence",
  "attemptId": "<active attempt>",
  "nodeId": "<bound node>",
  "evidenceKind": "check",
  "evidenceNote": "Explained why the derivative sign selects the descent direction.",
  "readiness": "advance-with-caution"
}
```

Do this **only after the learner actually answered**. Never record a check from
the fact that the block was displayed, and never record a correct answer as
`transfer` without independent use.

## 4. Avoiding Duplicates

- Do not add a second `check` evidence for the same answer just because the UI
  re-rendered.
- Do not add evidence when you merely re-read a previous answer.
- A quiz/flashcard response already produced one practice observation; do not
  add another generic practice entry for the same block.
- If you need to record a new observation, use a concrete note about what the
  learner actually did.

## 5. What You May Conclude

| Observation | May support | Must not claim |
| --- | --- | --- |
| Correct MCQ | one check / practice observation | "mastered", "confirmed", "understands everything" |
| Correct quiz after explanation | `checked` at most | automatic `confirmed` |
| Flashcard self-report "got it" | scheduling + practice | mastery |
| Learner explains a new example | `explanation` / `check` | automatic `transfer` |
| Independent new-context success | `transfer`, then your judgement | runtime-generated confirmed |

The runtime never advances the route because an interaction happened. You decide
the next step; the learner chooses whether to act.

## 6. Image and PDF Boundaries

- An `image` block is learner material. The runtime can display it, but this
  model interface does not receive its pixels. Do not claim to have read it.
- PDF text is extracted page by page. Empty pages may be scanned images; this
  version does not OCR them. Say so rather than inventing page content.
