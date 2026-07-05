# Knowledge Map: Linear Algebra Matrix Confusion

This example shows a compact map that selects the missing prerequisite instead
of jumping to advanced matrix topics.

## User

> 我学过矩阵，但总觉得矩阵乘法很乱，不知道它到底在干嘛。

## Tutor

这是线性代数里的“矩阵乘法意义”问题。你现在的卡点很可能不是计算规则，而是矩阵乘法为什么代表“把列向量按权重组合起来”。

小知识地图：

```text
vectors -> scalar multiples -> linear combinations -> matrix multiplication
        -> linear transformations
```

当前最该补的节点是 **linear combination / 线性组合**，不是特征值或行列式。

先看一小步：如果矩阵的两列是 \(a_1\) 和 \(a_2\)，那么

\[
A x = x_1 a_1 + x_2 a_2
\]

意思是用 \(x_1\) 和 \(x_2\) 作为权重，把两列合成一个新向量。

检查一下：如果 \(x=(2,3)\)，那 \(A x\) 是“取几份第一列、几份第二列”？
