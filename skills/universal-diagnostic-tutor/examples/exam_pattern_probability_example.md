# Exam Pattern Probability Example

## User Question

"I keep getting conditional probability wrong. I divided by the total number of
outcomes again. How is this usually tested?"

## Diagnosis

- **Subject routing:** Probability and exam prep.
- **Likely gap:** Misconception plus recognition gap.
- **Task:** Repair denominator reasoning and identify exam trap.

## Expected Pacing Choice

Repair the concept with one small example, identify the exam cue, then give one
near-match practice item.

## Autonomous Search

Use search if available and the learner wants exam-style practice. Prefer
university probability problem sets, open textbook exercises, or public sample
exams. Search is not needed to explain the core concept.

## Source Selection Logic

Look for resources with conditional probability exercises, not answer-only
solution dumps. Use them to identify patterns such as "given that," restricted
sample space, and independence traps.

## Example Tutor Response

Your repeated mistake is a very common exam trap: after the condition is given,
the denominator is no longer the whole sample space.

Conditional probability means:

```text
P(A | B) = outcomes where A and B both happen / outcomes where B happens
```

The phrase "given B" means "we are already inside group B." So the denominator
is only the conditioned group.

Tiny example:

```text
10 students total
6 studied
4 studied and passed
```

If the question asks "What is the probability a student passed given that they
studied?", the denominator is `6`, not `10`, because we are only looking among
students who studied.

Exam pattern:

- **Cue:** "given that," "among those who," "if we know."
- **Trap:** divide by everyone.
- **Prevention rule:** after reading the condition, redraw the sample space.

If search is available, I would look for a university probability problem set
or open textbook exercise section on conditional probability and use it for
practice patterns, not copied answers.

Practice check: In the example above, what should the denominator be: `10` or
`6`?

## Stop Point Or Check Question

"What should the denominator be: `10` or `6`?"

## Why This Is Better Than A Generic AI Answer

A generic answer might only give the formula. This response identifies the
repeated misconception, explains why the wrong denominator is tempting, names
the exam cue, and gives one small check.
