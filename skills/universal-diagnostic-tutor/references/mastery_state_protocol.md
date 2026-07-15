# Mastery State Protocol

Use this protocol to estimate what the learner has shown in the current
conversation and choose the next teaching move. Mastery state is evidence, not
a permanent label. Update it as the learner explains, solves, asks questions,
or makes mistakes.

This is the broader historical model for selecting a teaching posture, from
Unknown through Transfer or Overloaded. It does not override the preferred
concept-level status terms in `concept_mastery_map_protocol.md`: `explained`,
`practiced`, `checked`, `confirmed`, `unconfirmed`, `weak`, and `blocked`. Use
those terms for visible V1.9 state updates and readiness handoffs.

Do not announce state labels unless they help the learner. Prefer natural
language such as "You have the setup, but the reason behind the step is still
the part to strengthen."

## Unknown

- **Detect it:** The learner has not shown work, prior knowledge, confidence,
  or a specific stuck point yet.
- **Do next:** Start with compact diagnosis, ask one useful context question if
  needed, or give a foundation-first explanation.
- **Do not:** Assume beginner or expert status from the topic alone.
- **Example tutor move:** "Before we choose a method, the key question is
  whether you know what each symbol represents. Let me start there."

## Exposure

- **Detect it:** The learner has seen the term, formula, code pattern, source,
  or example but cannot yet explain it.
- **Do next:** Give a plain-language meaning, one concrete example, and one
  recognition check.
- **Do not:** Treat familiarity with a word as understanding.
- **Example tutor move:** "You've seen `gradient`, but let's make it usable: it
  is the direction that says how the loss changes when the parameters move."

## Recognition

- **Detect it:** The learner can identify the concept, method, bug type, or
  problem class when prompted.
- **Do next:** Ask why that method fits or move to a worked-example completion.
- **Do not:** Jump straight to hard transfer or mixed practice.
- **Example tutor move:** "Good, you recognized this as a base-case question.
  Now let's say why the base case stops the recursion."

## Guided Understanding

- **Detect it:** The learner can follow the explanation, answer small checks,
  or complete a step with support.
- **Do next:** Keep scaffolding but ask them to explain one reason or predict
  one next step.
- **Do not:** Mistake following along for independent mastery.
- **Example tutor move:** "You're following the idea. Try this next step: what
  does `A` do to the vector before we compare it with `b`?"

## Independent Explanation

- **Detect it:** The learner can explain the idea in their own words with the
  main relationship, reason, or mechanism intact.
- **Do next:** Move to guided application or near-transfer practice.
- **Do not:** Keep reteaching the same idea unless the learner asks.
- **Example tutor move:** "That explanation has the important part: a matrix can
  transform a vector. Let's use that on a tiny new equation."

## Guided Application

- **Detect it:** The learner can solve with hints, partial steps, a trace, or a
  worked example nearby.
- **Do next:** Give a near-transfer problem with fewer hints.
- **Do not:** Advance to mixed or project-style work too soon.
- **Example tutor move:** "You got it with the hint. Now try the same structure
  with one changed number and tell me the first step."

## Independent Application

- **Detect it:** The learner solves a similar problem without hints and can
  check the result.
- **Do next:** Ask for reasoning, give a trap case, or move to transfer.
- **Do not:** Declare full mastery from one correct answer.
- **Example tutor move:** "Nice. Since you solved that independently, let's see
  if you can spot when the same method applies in a slightly different form."

## Transfer

- **Detect it:** The learner applies the idea in a new wording, domain, data
  shape, proof context, or implementation situation.
- **Do next:** Summarize the transfer cue and optionally connect to a later
  topic or real application.
- **Do not:** Keep them on near-identical drills unless they want fluency.
- **Example tutor move:** "You transferred the recursion idea from factorial to
  tree traversal. The cue is still: solve a smaller version and stop at a base
  case."

## Misconception Detected

- **Detect it:** The learner uses a stable wrong model, repeats the same wrong
  step, or gives a plausible but false explanation.
- **Do next:** State the misconception gently, explain why it is tempting,
  repair the model, and give a near-match check.
- **Do not:** Say only "wrong" or continue practice without repair.
- **Example tutor move:** "The tempting idea is that virtual memory means extra
  RAM. The better model is address translation: it gives each process its own
  address view."

## Overloaded

- **Detect it:** The learner says they are lost, asks too many basic questions
  at once, mixes symbols, or shuts down under notation or steps.
- **Do next:** Reduce scope, lower abstraction, remove optional notation, and
  give one small success task.
- **Do not:** Add sources, formulas, edge cases, or a longer explanation before
  simplifying.
- **Example tutor move:** "Let's pause the full formula. We'll use one number,
  one direction, and one update first."

## Using Mastery States Well

- Treat state as local to the current concept and conversation.
- Track evidence separately for explanation, procedure, and transfer.
- Move up gradually after the learner explains why, not just after a correct
  answer.
- Move down quickly when confusion, repeated mistakes, or overload appears.
- Pass answer evidence through `mastery_signal_interpretation_protocol.md` and
  `readiness_gate_protocol.md` before deciding that the learner can advance.
- Summarize progress naturally when it helps: "So far, you have the meaning of
  the symbols; the next step is using them on a new problem."
