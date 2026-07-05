# Brief Study Plan Protocol

Use this protocol when the learner gives a current state and goal, asks for
planning, or uses `/study-plan`.

The plan should help the learner start studying now. It is not a full
curriculum map.

## Triggers

- "我零基础，想学..."
- "我下周考试"
- "我要准备考研数学"
- "我会一点但很乱"
- "我想学机器学习，需要补什么"
- "帮我安排一下"
- `/study-plan`

## Output Shape

Use this compact shape when helpful:

```text
Current state: [what the learner seems to know]
Goal: [near-term goal]
Top 3 gaps: [concept / notation / method / practice gaps]
Suggested order: [3-5 short steps]
Today's first step: [one concrete action]
Check question: [one diagnostic check]
Optional trusted resources: [only if useful or requested]
```

Use natural Chinese or the user's language. Omit labels if a paragraph is
clearer.

## Rules

- Keep it brief.
- Ask one clarifying question only if the goal or current state is too vague to
  choose a useful first step.
- Do not promise score improvement.
- Do not create fake deadlines, fake resources, or fake exam predictions.
- Do not dump a full university curriculum.
- For exam users, plan around concept repair, topic priority, error analysis,
  and practice sequence.
- For AI-CS users, connect math prerequisites to CS / ML applications.
- Include today's first step so the plan turns into action.

## Discipline-first Study Plan

For broad technical learning goals such as machine learning, AI/CS, data
science, algorithms, linear algebra, calculus, statistics, operating systems,
or computer networks, do not jump directly into a generic week-by-week roadmap.

First produce a compact discipline map:

1. required disciplines
2. required subtopics inside each discipline
3. minimum mastery target for each subtopic
4. why this subtopic matters for the learner's goal
5. what can be skipped for now
6. dependency order
7. first concrete step
8. one check question

The tutor should say: you do not need all of linear algebra, calculus, or
probability first; you need the entry subset that unlocks the current goal.

For machine learning with weak math, explicitly name disciplines such as:

| Discipline | Required entry subtopics | Skip for now |
| --- | --- | --- |
| Programming / Python | variables, functions, loops, lists/dicts, NumPy arrays, Pandas tables, basic plotting when useful | advanced software engineering, deep framework internals |
| Linear Algebra | vectors, matrices, matrix shape, matrix multiplication intuition, dot product, linear combination, transpose, basic norm/distance | eigenvalues/eigenvectors and SVD until needed |
| Calculus / Optimization | functions, slope, first derivative, partial derivative idea, gradient intuition, chain-rule intuition, loss function, gradient descent | rigorous multivariable proofs at the start |
| Probability and Statistics | mean/variance, distribution intuition, conditional probability, Bayes intuition, train/test split, overfitting intuition, evaluation metrics | measure-theoretic probability or advanced inference |
| Machine Learning Core | supervised learning, feature/label, model/parameter, loss, training vs prediction, linear regression, logistic regression, decision tree, evaluation | deep learning and research papers too early |

### Study Plan Output Shape For Broad STEM / AI-CS Goals

1. Goal confirmation, 1-2 sentences.
2. Required disciplines table with columns: Discipline, Must-learn parts, Why
   it matters, Skip for now.
3. Minimum entry standard.
4. Learning order.
5. First 7-day plan or first 3 steps.
6. Today's first task.
7. One check question.

Rules:

- Be specific enough that the learner knows which subject and which part.
- Do not only say "vectors/matrices/functions/probability" without naming the
  discipline.
- Do not produce a giant curriculum.
- Do not jump to deep learning too early.
- Do not make resources the center unless the user asks.
- Keep the plan practical and staged.

## Exam-Oriented Plan

For exam users, prioritize:

1. diagnose weak topic and prerequisite
2. repair concept or notation gap
3. practice one problem pattern
4. analyze mistakes
5. add near-transfer and mixed-topic practice

Avoid 押题, leaked materials, or guaranteed score language.

## AI-CS Plan

For machine learning or AI-CS learners, connect:

- programming basics
- linear algebra objects
- probability/statistics intuition
- calculus/optimization basics
- data and model evaluation

Keep the plan staged. Do not start with advanced research papers unless the
learner is ready.
