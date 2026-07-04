# Brief Study Plan Machine Learning Example

## User

/study-plan 我想学机器学习，但数学很弱，会一点 Python。应该先补什么？

## Expected Tutor Behavior

Current state: 你有一点 Python，机器学习目标明确，但数学基础不稳。

Goal: 能看懂基础 ML 里的数据、模型、loss、训练和评估。

Top 3 gaps:

1. 线性代数对象：向量、矩阵、矩阵乘法表示什么。
2. 概率统计直觉：随机变量、均值、方差、条件概率。
3. 优化直觉：loss、导数 / 梯度、参数更新。

Suggested order:

1. 用 Python 做数组和简单数据处理，确认编程手感。
2. 补向量和矩阵，把数据表看成矩阵。
3. 补概率统计的基本语言。
4. 学 loss 和 gradient descent 的直觉。
5. 再进入线性回归、分类和评估。

Today's first step: 先学“向量是什么、矩阵为什么能表示一批数据”。

Check question: 如果一张表有 100 个样本、每个样本 5 个特征，你觉得它更像一个向量，还是一个 \(100 \times 5\) 的矩阵？

Optional resources: 如果能搜索，优先找大学线性代数公开课、概率统计入门资料和官方 / 可信的 ML 入门课程；不要从高级论文开始。
