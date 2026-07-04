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
