# Feedback: Grading, Mistakes, And Interventions

Use this file when a learner submits an answer, solution, explanation, proof,
or trace, or when a check answer reveals an error. Treat mistakes as
diagnostic evidence, never as a reason to simply reveal the solution.

The pipeline: grade qualitatively -> analyze the mistake (surface error,
underlying gap, why the wrong path felt tempting) -> map the error type to the
smallest repair -> interpret the signal into the next teaching move. The
focused practice loop lives in `learning_task_loop_protocol.md`.

## Grade Labels

Choose one primary label. This is qualitative educational grading — not
official exam scoring, exact points, exam prediction, or score promises.

| Label | Use when |
| --- | --- |
| Correct | Result and essential reasoning satisfy the exercise criteria. |
| Mostly correct | Core method and result sound; reasoning, justification, notation, or completeness fragile. |
| Partially correct | A meaningful part is correct, but an important step, condition, or conclusion is wrong or missing. |
| Incorrect | The response does not satisfy the core concept or method being checked. |
| Cannot grade yet | Reasoning required but absent, ambiguous, or only an unsupported result. |

Add a secondary classification when it explains the signal: final answer
correct but reasoning weak; reasoning correct but calculation error; concept
correct but notation wrong; method correct but incomplete; guessed correct;
copied answer / no reasoning (only when the learner says so or provides no
original reasoning — never from style alone).

Partial-credit principles: name exactly which idea earns credit; preserve a
correct setup even when a later calculation fails; distinguish a local
mechanics slip from a wrong mental model; never upgrade an unsupported result
to Correct, never downgrade sound reasoning to Incorrect over one local slip;
never convert labels into percentages or official points.

When evidence is missing, ask for one narrow piece: the step where the method
was chosen, one sentence of reasoning, the missing calculation or trace, or
the original question. If the learner declines, state what can be checked
from the final answer and keep mastery unconfirmed.

## Mistake Analysis

1. Identify the surface mistake — the exact line, assumption, calculation, or
   choice that changed the path.
2. Identify the underlying gap — vocabulary, concept, notation, procedure,
   reasoning, recognition, transfer, misconception, confidence, or resource
   selection.
3. Separate careless from conceptual: a slip needs a check habit; a conceptual
   error needs model repair. (Careless: learner can explain the idea but made
   an arithmetic, sign, typo, copying, unit, or syntax slip. Conceptual: same
   wrong move repeated, step unjustified, or a false model.)
4. Explain why the wrong path felt tempting — this lowers shame and reveals
   the faulty cue.
5. Repair the misconception or missing prerequisite with the smallest idea
   that prevents the error.
6. Give a similar but slightly changed practice task.
7. Summarize one prevention rule the learner can reuse.

Common mistake types: misread question (restate the task, underline the
demanded output); memorized formula without meaning (translate every symbol
before plugging in); applied wrong rule (contrast the rule's valid case with
this one); skipped prerequisite (rebuild it with a smaller example); answer
by intuition only (respect the guess, test it against structure);
confused similar concepts (two-column contrast with recognition cues);
calculation or syntax error (local correction plus a check habit);
overgeneralized from one example (counterexample, then the real boundary).

## Error To Intervention

| Error type | Typical signal | Efficient intervention |
| --- | --- | --- |
| Notation | Misreads a symbol, variable, graph mark, code token, or object role | Translate symbols into object roles |
| Concept | Uses the wrong mental model | Build an intuition bridge or concrete example |
| Method selection | Chooses the wrong test, theorem, algorithm, or formula | Compare problem cues side by side |
| Setup | Cannot turn words into equations, code state, diagrams, or variables | Translate words into objects |
| Proof | Gives examples or behavior but no reason it always works | Identify missing hinge, invariant, or assumption |
| Calculation | Arithmetic, sign, algebra, syntax, or copying slip | Correct locally and add a check habit |
| Transfer | Solves the example but misses similar problems | Name the reusable pattern; give near-transfer |
| Overgeneralization | Applies one pattern where it does not hold | Give counterexample or edge case |
| Memorized procedure | Gives rule or answer but cannot explain why | Ask a why-step check or teach the mechanism |

## Signal To Action

| Learner signal | Likely meaning | Tutor action |
| --- | --- | --- |
| Correct and can explain why | Understanding stabilizing | Pass evidence to readiness; give near-transfer |
| Correct but guessed | Recognition without reasoning | Ask for reasoning or give short intuition |
| Correct but cannot explain why | Procedure recall, weak concept | Maintain difficulty; repair the why |
| Partially correct | Some structure present | Preserve correct part; repair missing part |
| Wrong concept | Model mismatch | Intuition or application bridge |
| Wrong symbol | Notation or object-type gap | Return to symbol translation |
| Wrong method | Recognition gap | Compare method cues side by side |
| Calculation-only error | Local mechanics issue | Correct locally; do not reteach the method |
| Cannot explain why | Reasoning gap | One why-step check or compact mechanism |
| Asks a deeper question | Ready for rigor or context | Temporarily switch to advanced depth |
| Asks to go faster | Background or urgency | Compress and focus on the blocker |
| Asks to go slower / overwhelmed | Cognitive overload | Step down and reduce load |

## Learner-Facing Output

Adapt the labels to natural language but preserve the decisions: the verdict,
what is correct and should be kept, the earliest important gap and why it
matters, the mistake type, the smallest targeted fix, whether the learner can
advance (with the evidence limit — never from the verdict alone), and one
next step or practice question. Stop and wait when that step asks for a
learner response. Be direct, specific, non-shaming; never answer with only
"right" or "wrong"; never bury the verdict under a full new lecture.

Near-match practice after a repair: change numbers but keep structure for
procedure errors; change surface but keep concept for recognition errors; add
a tempting trap for misconception errors; ask for a short explanation for
reasoning errors. The goal is transfer, not volume — use
`exercise_generation_protocol.md` to build the item.

## Anti-Patterns

- Claiming an official score without an official rubric and authority.
- Treating one correct guess as confirmed mastery.
- Erasing correct reasoning because the final value is wrong.
- Giving the full solution before isolating the learner's actual error.
- Advancing automatically after any Correct verdict.
- Restarting from zero after a partial answer.
- Treating calculation slips as conceptual failure, or conceptual errors as
  mere slips.
- Reteaching the whole method when one local step failed.
