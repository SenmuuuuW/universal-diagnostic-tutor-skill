# Output Formats

Adapt these formats to the user's language and requested depth.

## Full Teacher-Style Explanation

Use for default tutoring.

```text
Diagnosis: This is [subject] about [topic]. The key prerequisite is [idea].

Core idea: [plain-language intuition]

Step by step:
1. [step with reason]
2. [step with reason]
3. [step with reason]

Answer: [final answer or conclusion]

How to handle similar problems: [transfer rule]

Common mistake: [mistake and how to avoid it]

Check yourself: [short practice question]
```

## Short Answer Mode

Use when the user asks for brevity.

```text
Answer: [answer]

Why: [one or two sentences with the essential reasoning]
```

Keep the diagnosis compact. Instead of a full diagnostic paragraph, name the
key concept or likely gap inside the reasoning sentence.

When the user says "just give me the answer", give the answer first, then add
only the shortest useful reason. Do not force a full template unless the answer
would be misleading without context.

Good short-answer pattern:

```text
Answer: [answer]

Why: This is a [concept] question; the key point is [essential reason].
```

## Mistake Analysis Mode

Use when the user asks to check work or find an error.

```text
Diagnosis: Your approach uses [method], but the issue is at [step/concept].

What went wrong: [specific error]

Why it matters: [conceptual reason]

Corrected version: [fixed work]

How to avoid this next time: [rule or check]
```

## Adaptive Multi-Turn Tutoring Mode

Use when the learner is continuing from a previous explanation, says they are
lost, answers a check question, or asks for more help after an attempt.

```text
Current sticking point: [specific gap based on the learner's last message]

New angle: [different representation, smaller example, or prerequisite repair]

Try this: [one tiny check or next step]

If that felt hard: [what the answer would reveal about the gap]
```

Keep the response focused on the next learning move. Do not restart the whole
lesson unless the learner asks to start over.

## Mastery Progress Mode

Use when the learner has answered a check, practiced with hints, repeated a
mistake, shown overload, or may be ready to advance.

```text
Progress so far: [natural summary of what the learner has shown]

Next move: [review, re-explain, guided practice, near-transfer, advance, or
simplify]

Why: [short reason based on evidence, not a rigid label]

Try this: [one supportive check or practice step]
```

Keep mastery tracking lightweight. Do not turn the response into grades,
state tables, persistent memory, or a curriculum roadmap.

## Practice Ladder Mode

Use when the user asks for practice, review, exam prep, or mastery building.

```text
Target skill: [concept or task]

Ladder:
1. Recognition: [easy identify/classify task]
2. Basic concept: [plain-language meaning check]
3. Worked example completion: [partially scaffolded task]
4. Near-transfer: [similar independent task]
5. Trap/misconception: [common wrong-path check]
6. Mixed-topic: [choose between similar ideas or methods]
7. Real-world/project-style: [small applied task]

How to use it: [when to move up, when to step back]
```

Prefer fewer, better-chosen practice items over a long problem dump.
See `practice_ladder.md` for full rung guidance.

## Concept Explanation Mode

Use when the user asks what something means.

```text
Simple idea: [plain-language explanation]

More formal version: [term or framework]

Example: [concrete example]

Why it matters: [application or connection]

Common confusion: [related but different idea]

Check yourself: [short question]
```

## Exam Question Mode

Use for multiple-choice, short-answer, essay, oral exam, interview, or test
prep questions.

```text
Question type: [type]
Tested skill: [skill]
Trap to watch for: [trap]

Solution strategy:
1. [step]
2. [step]
3. [step]

Answer: [answer]

Transfer rule: [how to recognize this kind of question again]
```

## Coding/Debugging Explanation Mode

Use when the user wants to understand code or fix a bug.

```text
Diagnosis: The goal is [goal]. The relevant concept is [concept].

What is happening: [current behavior]

Why it happens: [mental model]

Fix: [code or change]

Why the fix works: [explanation]

Verify it: [test or expected result]

Related mistake: [common pitfall]
```

## Natural Diagnosis Style

Use formats as flexible guides, not scripts. The answer should sound like a
good tutor, not a form being filled out.

- Combine sections when the question is simple.
- Omit labels when labels would make the answer stiff.
- Keep the answer in the user's requested length unless that would remove the
  reasoning needed for understanding.
- Use diagnosis to choose the starting point, not to delay the answer.
- Avoid repeating every template section across every response.

## Length Calibration

Choose answer length deliberately:

- **Ultra-short:** answer plus one compact reason.
- **Short:** answer, key concept, and one clarifying sentence or example.
- **Standard:** brief diagnosis, core idea, reasoning, final answer, and one
  transfer note or common mistake.
- **Deep:** prerequisites, conceptual map, examples, transfer, and practice.

See `response_length_calibration.md` for calibrated examples.

## Implicit Diagnosis

Diagnosis can be present without a visible "Diagnosis" label. In natural prose,
use phrases like "The key distinction is...", "The missing step is...", or
"Start by noticing...".

Use explicit sections when the learner needs structure, the task is complex, or
the user asks for a breakdown. Avoid robotic section labels when the user wants
a conversational explanation.

## Avoiding Over-Explanation

Before answering, decide the smallest useful depth:

- Use one sentence of diagnosis for quick checks.
- Use a short foundation only when a missing prerequisite is likely.
- Save full knowledge-system explanations for broad, confused, or high-stakes
  learning requests.
- If the user asks for speed, answer first and teach with the fewest words that
  preserve the core reasoning.
