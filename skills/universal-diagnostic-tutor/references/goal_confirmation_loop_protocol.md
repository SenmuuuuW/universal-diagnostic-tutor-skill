# Goal Confirmation Loop Protocol

Use this protocol after clarifying a broad learning goal and before building a
knowledge map or learning path.

The loop keeps the tutor aligned with the learner without trapping them in
endless confirmation.

## Lightweight Loop

1. Learner gives a goal.
2. Tutor asks 1-3 focused clarifying questions if needed.
3. Tutor restates the understood goal.
4. Learner confirms or corrects.
5. Tutor proceeds to a compact knowledge map, first teaching step, plan, or
   sub-skill route.

## When To Use

Use for:

- broad learning goals
- exam or project goals with unclear scope
- study-plan requests
- weak-foundation repair
- multi-week or cross-chat learning tasks

Usually skip for:

- one-off concept questions
- a single problem with clear context
- urgent final-answer requests
- cases where the learner already gave a precise target, level, and desired
  output

## Confirmation Template

```text
我先确认一下：你现在的目标是 [goal]，当前基础大概是 [state]，
你希望先解决 [priority]。如果对，我会先给你一个小知识地图，
再选第一步开始。
```

For urgent exam mode, compress it:

```text
我先按这个目标走：先修复 [priority]，目标是 [exam/task]。对的话我们马上从第一步开始。
```

## Correction Rule

- If the user says "yes", "对", "就是这个", or similar, proceed.
- If the user corrects the goal, update it and restate once.
- If the user keeps changing the target, ask which target matters first today.
- Do not require formal agreement when the learner is clearly ready to begin.

## Examples

### Machine Learning Goal

Tutor:

> 我先确认一下：你想为了做小项目入门机器学习，Python 会一点，但数学基础不稳。所以我们先不从神经网络开始，而是先补向量、函数和 loss 的直觉。对吗？

### Linear Algebra Exam Goal

Tutor:

> 我先按考试目标理解：你要尽快补线代做题能力，当前最卡的是矩阵和向量关系，不是完整重学整门课。对的话，我先给一个很小的知识地图，再从矩阵乘法意义开始。

### Concept-Only Question

User:

> 什么是 \(K_n\)？

Tutor should not run a confirmation loop. Explain the symbol directly, then
ask one small check if useful.

## Mistakes To Avoid

- Asking for confirmation after every small question.
- Turning confirmation into a formality that delays urgent help.
- Proceeding with a broad plan when the learner corrected the goal.
- Repeating the whole clarification after one small correction.
