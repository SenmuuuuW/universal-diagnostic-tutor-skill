# Cross-Turn Progress Protocol

Use this protocol when tutoring continues across multiple turns in the same
conversation. The goal is to carry forward the learner's progress without
making the answer feel like a tracking spreadsheet.

This is not persistent memory. Track only what is useful inside the current
conversation: what the learner understood, what confused them, which
representation already helped or failed, and what the next teaching move should
be.

## Core Progress Loop

1. **Recall the local learner model.** What has the learner shown in this
   conversation?
2. **Compare new evidence.** Did the latest answer show explanation,
   procedure, application, transfer, misconception, or overload?
3. **Update the likely mastery state.** Use `mastery_state_protocol.md` when
   the next move depends on readiness.
4. **Choose the next move.** Review, re-explain, practice, advance, simplify,
   or switch representation.
5. **Keep it natural.** Mention progress only when it helps orient the learner.

## Progress Rules

- Keep a lightweight mental note of what the learner has understood in this
  conversation.
- Do not assume mastery from one correct answer.
- Distinguish "answered correctly" from "understands why."
- If the learner explains correctly, advance gradually.
- If the learner answers correctly but cannot explain, give a reasoning check.
- If the learner is confused twice, change explanation mode instead of
  repeating.
- If the learner makes the same mistake again, return to the prerequisite or
  misconception repair.
- If the learner succeeds with hints, move to near-transfer practice.
- If the learner succeeds without hints, move to transfer or application.
- Summarize progress naturally when helpful.

## Evidence To Track

- **Concept evidence:** Can the learner explain the idea in plain language?
- **Notation evidence:** Can they say what the symbols, terms, units, code, or
  diagram parts mean?
- **Reasoning evidence:** Can they justify why a step is allowed?
- **Procedure evidence:** Can they choose and sequence the steps?
- **Application evidence:** Can they solve with fewer hints?
- **Transfer evidence:** Can they recognize the structure in a new context?
- **Affect evidence:** Are they confident, hesitant, overloaded, or rushing?

## When The Learner Answers Correctly

- Confirm the answer briefly.
- Ask for or supply the reasoning if the explanation was not shown.
- Advance only one step: from recognition to worked completion, from guided
  application to near-transfer, or from independent application to transfer.

Good move:

```text
Correct. To make sure this is understanding and not just the right number, what
reason lets us use that step?
```

## When The Learner Answers Partly Correctly

- Preserve the correct piece.
- Name the missing piece.
- Ask for a small revision instead of restarting the whole explanation.

Good move:

```text
You have the base case idea right. The missing part is the smaller input. What
input should the recursive call use so the problem actually shrinks?
```

## When Confusion Repeats

After two confused turns on the same idea, change the teaching mode:

- Formula to diagram.
- Diagram to numerical example.
- Code to trace table.
- Abstract definition to everyday analogy.
- Proof steps to invariant story.
- Source summary to direct explanation.

Do not keep extending the same explanation.

## Natural Progress Summaries

Use one sentence when it helps:

- "You now have the symbol meanings; next we need the procedure."
- "You can follow the trace with help, so let's try one line without hints."
- "The repeated error is the same misconception, so let's repair that before
  adding harder practice."
- "You solved that independently; now the goal is recognizing the method in a
  new wrapper."

Avoid visible progress reports unless the learner asks for a study plan or
status summary.
