# Mastery Signal Interpretation Protocol

Use this protocol when the learner answers a check, gives work, reacts to an
explanation, asks to go faster or slower, or makes a mistake. The tutor should
interpret what the response reveals about mastery, not merely mark it right or
wrong.

For submitted work, `answer_grading_protocol.md` owns the grade label and
specific feedback. Use this file to interpret the resulting learning signal,
then pass the combined evidence to `readiness_gate_protocol.md`. Do not treat a
single signal as an automatic readiness decision.

## Signal To Action Map

| Learner Signal | Likely Meaning | Tutor Action |
| --- | --- | --- |
| Correct and can explain why | Understanding is becoming stable | Pass evidence to the readiness gate or give near-transfer |
| Correct but guessed | Recognition without reasoning | Ask for reasoning or give short intuition |
| Correct but cannot explain why | Procedure recall, weak concept | Maintain difficulty and repair why |
| Partially correct | Some structure is present | Preserve correct part, repair missing part |
| Wrong concept | Model mismatch | Use intuition or application bridge |
| Wrong symbol interpretation | Notation or object-type gap | Return to symbol translation |
| Wrong method | Recognition gap | Compare method cues side by side |
| Calculation-only error | Local mechanics issue | Correct locally; do not reteach the whole method |
| Cannot explain why | Reasoning gap | Ask one why-step check or give compact mechanism |
| Asks a deeper question | Ready for more rigor or context | Temporarily switch to advanced depth |
| Asks to go faster | Existing background or urgency | Compress and focus on the blocker |
| Asks to go slower or seems overwhelmed | Cognitive overload | Step down and reduce load |

## How To Respond

### Correct And Can Explain Why

Confirm the reasoning, not just the answer. If transfer is not yet supported,
give a near-transfer, trap, or edge-case check. Otherwise pass the evidence to
the readiness gate for an advancement decision.

### Correct But Cannot Explain Why

Do not treat the answer as mastery. Say naturally that the answer is right but
the reason is the part to strengthen. Ask one reasoning check or give one short
intuition before advancing.

### Partially Correct

Name the part that works first. Then isolate the missing piece.

> That first part is right: you noticed the scalar multiple idea. The missing
> piece is that the same scalar must work for every component.

### Wrong Symbol

Return to notation before method. If \(b\) in \(Ax=b\) is mistaken for a point,
explain it as an output vector in the equation's object roles.

### Wrong Method

Do not just solve. Show the cue that distinguishes methods.

> This looks like comparison at first, but the adjacent factors \(n(n+1)\) are
> the cue for telescoping.

### Overwhelmed

Remove optional notation, reduce the example, and ask one small confidence or
recognition check. Do not add sources, formulas, edge cases, or long roadmaps.

## Interpretation Principles

- A correct answer is evidence, not proof of mastery.
- A wrong answer often reveals the next best teaching step.
- A repeated mistake usually needs misconception repair before more practice.
- A vague answer needs one narrow diagnostic question, not a lecture.
- Learner confidence matters: guessed correctness and confident reasoning need
  different next moves.
- Supplemental grading signals such as correct reasoning with a calculation
  error, correct concept with wrong notation, or a guessed correct answer
  should change the intervention and readiness evidence without creating a new
  mastery vocabulary.

## Anti-Patterns

- Saying only "correct" or "wrong" with no teaching decision.
- Advancing after a correct answer when the learner cannot explain why.
- Restarting from zero after a partial answer.
- Treating calculation slips as conceptual failure.
- Treating conceptual errors as mere arithmetic slips.
