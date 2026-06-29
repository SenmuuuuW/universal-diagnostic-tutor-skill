# Knowledge-System Mapping Protocol

Use this protocol when a learner would benefit from knowing what larger field a
problem belongs to and what prerequisite ideas make the method natural.

The goal is orientation, not a course roadmap.

## What To Map

At the beginning of substantial STEM / AI-CS tutoring, identify only the useful
parts:

- Subject area.
- Subtopic or knowledge system.
- Core concept.
- Prerequisite concepts.
- What the problem is really testing.

Keep this compact, usually one to three lines. Then begin teaching.

## When To Show The Map

Show a compact map when:

- The learner is zero-base or confused by symbols.
- The prompt asks what field, chapter, or knowledge point a problem belongs to.
- Method choice matters more than calculation.
- The problem is from STEM / AI-CS and has hidden prerequisites.
- The learner asks how to recognize similar problems later.

## When To Skip Or Shrink It

Skip or shrink the map when:

- The user asks for an urgent answer.
- The task is a tiny fact check.
- The domain is already obvious and repeating it would feel stiff.
- The learner is overloaded and needs one object or symbol explained first.
- A map would become a long prerequisite chain.

## Good Compact Maps

- "离散数学 -> 图论 -> 完全图的边染色。前置概念是点、边、完全图、边染色。"
- "线性代数 -> 向量方程 -> 标量倍数。核心是把文字条件翻译成向量等式。"
- "微积分 / 数学分析 -> 级数判敛 -> 方法识别。核心是看到结构后选择裂项、比较或交错判别法。"
- "机器学习 -> 优化 -> 梯度下降。前置是函数、导数/梯度、loss 和参数更新。"

## Use The Map To Choose The First Step

After the map, ask: what must the learner understand before the method can
work?

- If the blocker is notation, translate symbols first.
- If the blocker is method recognition, name the cue before solving.
- If the blocker is a proof, translate the statement before proving it.
- If the blocker is an application, give intuition before formalism.
- If the blocker is transfer, extract the reusable pattern after one step.

## Anti-Patterns

- Long curriculum roadmaps for a single problem.
- Listing every prerequisite in a course sequence.
- Starting with taxonomy instead of teaching the learner's blocker.
- Using formal labels that the learner cannot yet understand.
- Repeating the same map in every turn when the learner already knows the
  context.

## Natural Phrasing

Prefer:

```text
先定位一下：这是微积分里的级数判敛题，关键不是先算，而是先看结构。
```

Avoid:

```text
This problem belongs to Course Unit 3.2.1 and requires the following curriculum
sequence...
```
