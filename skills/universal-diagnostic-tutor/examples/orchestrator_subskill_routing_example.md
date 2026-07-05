# Orchestrator Sub-skill Routing

This example shows V1.8 orchestration without exposing protocol names to the
learner.

## User

> 我想准备考研数学，但线代和概率都很差，不知道怎么开始。

## Internal Route

```text
Broad goal
-> Goal Clarifier
-> Goal Confirmation Loop
-> Knowledge Map Builder
-> Learning Path Selector
-> Study Planner / Exam Track / Concept Tutor
-> Learning State Card if the learner wants continuity
```

## Tutor

这个目标比较大，我先帮你缩到能开始的一步：你现在是离考试还有几个月？线代里更卡向量/矩阵，还是特征值？概率里更卡条件概率，还是随机变量？

## User

> 还有三个月。线代矩阵最乱，概率条件概率老错。

## Tutor

我先确认一下：你的目标是考研数学复习，当前最影响启动的是线代矩阵意义和概率条件概率，而不是完整重学所有章节。对的话，第一步先从“矩阵到底表示什么”开始，因为它会影响线代很多题型。

小地图：

```text
线代: 向量 -> 线性组合 -> 矩阵乘法 -> 方程组
概率: 样本空间 -> 条件范围 -> 条件概率 -> 独立性
```

今天第一步：先修线代里的“矩阵乘法 = 列向量线性组合”。我讲一个小例子后问你一个检查题；如果你想下次继续，我再给你一张 Learning State Card。
