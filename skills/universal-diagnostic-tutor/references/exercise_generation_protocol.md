# Exercise Generation Protocol

Use this protocol to create a targeted practice item from the learner's current
concept, gap, mastery evidence, and selected rung in `practice_ladder.md`.
This is not a generic worksheet generator.

`practice_ladder.md` owns the difficulty framework. This protocol turns the
chosen rung into an answerable exercise. `answer_grading_protocol.md` evaluates
the learner's response, and `learning_task_loop_protocol.md` decides what
happens around the exercise.

## Plan The Exercise

Before showing the item, establish these fields:

- **Target concept:** The one idea or skill the learner should use.
- **Prerequisite being tested:** The earlier idea that must work for this item,
  or `none` when prerequisites are already supported by evidence.
- **Practice-ladder level:** Use one named level from `practice_ladder.md`.
- **Difficulty:** Easy, moderate, or challenging relative to this learner's
  current evidence, not relative to the whole subject.
- **Expected learner action:** For example, identify, explain, calculate,
  derive, trace, justify, compare, or implement.
- **Answer key or grading criteria:** Keep the expected result and essential
  reasoning available for later grading.
- **Likely misconception trap:** Name the tempting wrong path the item can
  reveal. Do not add a trap when it would make a beginner item needlessly
  tricky.
- **Hint policy:** Decide whether to offer no hint, a cue, a scaffolded step,
  or a stronger hint after an attempt.
- **Stop point:** End after the item and wait for the learner's answer.

Verify that the question contains enough information, fits the intended level,
and can be graded against the key or criteria. For open-ended work, define the
required ideas rather than pretending there is one exact answer.

## Match Evidence To The Ladder

- For `unconfirmed` or newly `explained` concepts, prefer recognition or basic
  concept checks.
- For `practiced` concepts or guided understanding, prefer worked-example
  completion or a close concept check.
- For `checked` concepts with stable guided work, prefer near-transfer with
  fewer hints.
- For `weak` concepts, target the exact unstable step. Do not raise difficulty
  merely because the learner has already seen the topic.
- For `blocked` concepts, step down to the missing prerequisite before testing
  the dependent concept again.
- For `confirmed` concepts, use a trap, mixed-topic, or applied item only when
  the learner's goal benefits from deeper transfer or fluency.

These are defaults, not automatic promotions. Use the learner's latest
reasoning and confidence evidence to select the lowest rung that can answer the
current learning question.

## Quantity And Sequencing

- Generate one small exercise at a time by default.
- Generate two or three only when the learner explicitly asks for a practice
  set.
- Keep a requested set coherent: vary one intended feature at a time and state
  whether the learner should answer all items together or one by one.
- If comparison is the target skill, keep the comparison inside one focused
  question unless the learner requested a set.
- Do not dump a full ladder, a large worksheet, or several unrelated concepts
  into one turn unless the learner explicitly requests that format.
- Do not jump to advanced transfer before concept and near-transfer evidence
  support it.

## Hint And Answer Policy

- Start without a hint when the goal is independent evidence.
- Offer a small cue when a beginner needs a supported attempt or when the
  selected rung is worked-example completion.
- Reveal hints progressively. A hint should preserve a meaningful learner
  action instead of giving away the answer.
- Keep the answer key internal unless the learner asks for it, asks for a
  worked solution, or has made a meaningful attempt and needs resolution.
- Do not show a full solution before the learner answers unless explicitly
  requested.

## Learner-Facing Shape

Use labels only when they improve clarity. A compact practice turn may contain:

1. **Target concept**
2. **Practice level**
3. **Question**
4. **What this checks**
5. **Optional hint**
6. **Stop and wait for the learner's answer**

The final line should invite the answer, not continue into grading, another
concept, or the solution.

## Example

- **Target concept:** Parallel vectors as scalar multiples
- **Practice level:** Basic concept check
- **Question:** Are \(u=(2,4)\) and \(v=(1,2)\) parallel? Explain why.
- **What this checks:** Whether one scalar ratio works across every component.
- **Optional hint:** Ask whether the same number turns both components of
  \(v\) into the corresponding components of \(u\).

Stop here and wait for the learner's explanation.

## Exam And Advanced Contexts

- Exam practice may use the style and time pressure of a known exam, but do
  not claim prediction, leaked content, guaranteed scores, or 押题.
- For beginners, prefer plain concept checks with minimal notation.
- For advanced learners, prefer near-transfer, method selection, mixed
  context, proof hinges, or edge cases that match their demonstrated level.
- Preserve correct math formatting with `\(...\)` and `\[...\]`.

## Anti-Patterns

- Generating a generic item that does not test the current gap.
- Choosing difficulty from the topic label instead of learner evidence.
- Asking several new concepts in one supposedly focused item.
- Including an accidental answer in the hint or question wording.
- Treating more questions as better evidence than one well-chosen response.
