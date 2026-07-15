# Answer Grading Protocol

Use this protocol when a learner submits an answer, solution, explanation,
proof, trace, or other attempt. Grade for learning: preserve what is correct,
locate what is unstable, choose a targeted repair, and provide evidence for the
next readiness decision.

This is qualitative educational grading. It is not official exam scoring,
exact point calculation, exam prediction, or a promise of score improvement.

## Grade Labels

Choose one primary label:

| Label | Use When |
| --- | --- |
| Correct | The result and essential reasoning are correct and the response satisfies the exercise criteria. |
| Mostly correct | The core method and result are sound, but reasoning, justification, notation, or completeness is fragile. |
| Partially correct | A meaningful part is correct, but an important step, condition, or conclusion is wrong or missing. |
| Incorrect | The response does not satisfy the core concept or method being checked. |
| Cannot grade yet / missing reasoning | The task requires reasoning, but the response is absent, too ambiguous, or gives only an unsupported result. |

When the exercise legitimately asks only for a short result, do not invent a
reasoning requirement after the fact. Grade against the criteria established
when the exercise was generated.

## STEM Reasoning Classifications

Add a secondary classification when it explains the learning signal:

- final answer correct but reasoning weak
- reasoning correct but calculation error
- concept correct but notation wrong
- method correct but incomplete
- guessed correct
- copied answer / no reasoning

Use `copied answer / no reasoning` only when the learner says the answer was
copied or provides no original reasoning. Do not accuse a learner of copying
from style alone.

## Grading Sequence

1. Reconstruct what the learner is claiming and which criteria the answer
   addresses.
2. Compare the result, reasoning, conditions, notation, and requested form
   with the answer key or grading criteria.
3. Select one primary grade label and, when useful, one secondary reasoning
   classification.
4. Name the exact correct part before discussing the gap.
5. Identify the first consequential error or omission. Do not list every small
   flaw when one underlying issue explains them.
6. Classify the mistake through `mistake_analysis_protocol.md`, then select the
   smallest repair through `error_to_intervention_protocol.md`.
7. Pass the observed evidence to `readiness_gate_protocol.md`. A grade alone
   does not prove readiness.
8. Update the concept status through `concept_mastery_map_protocol.md` when a
   visible state update is useful.

## Required Grading Output

Adapt the labels to natural learner-facing language, but preserve these seven
decisions:

1. **Verdict:** Primary grade label, with uncertainty when applicable.
2. **What is correct:** The specific reasoning, setup, method, or result that
   should be kept.
3. **What is wrong or missing:** The earliest important gap and why it matters.
4. **Mistake type:** The learning-relevant error class, not a character
   judgment.
5. **Targeted fix:** The smallest explanation, correction, check habit, or
   prerequisite repair that addresses the error.
6. **Whether the learner can advance:** Apply a readiness outcome and state the
   evidence limit. Do not infer this from the verdict alone.
7. **Next step or next practice question:** Choose one action and stop if it
   asks for a learner response.

For a simple answer, these can be combined into a few natural paragraphs. Do
not force a seven-heading report when it would make the tutoring robotic.

## Partial Credit Principles

- Explain exactly which idea earns qualitative credit.
- Preserve a correct setup even when later calculation fails.
- Distinguish a local mechanics error from a wrong mental model.
- Do not upgrade an unsupported correct result to `Correct` when reasoning is
  part of the target; use `Mostly correct` or `Cannot grade yet / missing
  reasoning` according to the available evidence.
- Do not downgrade sound reasoning to `Incorrect` because of one local
  arithmetic, sign, syntax, or notation slip.
- Do not convert these labels into invented percentages or official exam
  points.

## Missing Or Unusable Evidence

Ask for one narrow piece of work when the response cannot be graded reliably:

- the step where the learner chose a method
- one sentence explaining why the answer follows
- the missing calculation or code trace
- the original question when context is absent

If the learner does not want to provide reasoning, state what can be checked
from the final answer and keep mastery unconfirmed.

## Tone And Stop Point

- Be direct, specific, and non-shaming.
- Explain why a wrong path was tempting when that helps repair the model.
- Do not respond with only `right` or `wrong`.
- Do not bury the verdict under a full new lecture.
- When the next step is a question or exercise, ask only that step and wait.

## Anti-Patterns

- Claiming an official score without an official rubric and authority.
- Treating one correct guess as confirmed mastery.
- Erasing a learner's correct reasoning because the final value is wrong.
- Giving the full solution before isolating the learner's actual error.
- Advancing automatically after any `Correct` verdict.
