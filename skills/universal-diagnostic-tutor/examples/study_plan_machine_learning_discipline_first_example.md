# Study Plan: Machine Learning Discipline-first Example

This example shows how `/study-plan` should avoid a generic roadmap for a broad
AI-CS goal.

## User

> /study-plan 我想系统入门机器学习，但是数学基础比较弱。我会一点 Python，不是为了考试，是为了以后能看懂基础模型并做小项目。请给我一个学习计划。

## Tutor

我先按这个目标理解：你想为了看懂基础模型并做小项目来入门机器学习；Python
有一点基础，但数学需要补到 ML-entry level。你不需要先学完整的线代、微积分和概率论，
只需要先补能支撑基础模型的那一部分。

## Required Disciplines

| Discipline | Must-learn parts | Why it matters | Skip for now |
| --- | --- | --- | --- |
| Programming / Python | variables, functions, loops, lists/dicts, NumPy array shape, Pandas tables | 能把数据读成表、数组和特征 | 大型工程结构、框架源码 |
| Linear Algebra | vectors, matrices, row/sample, column/feature, matrix shape, dot product, linear combination, basic norm/distance | 数据表、特征向量、线性模型都靠这些对象表达 | eigenvalues, SVD |
| Calculus / Optimization | function, slope, derivative intuition, partial derivative idea, gradient as direction, loss function, gradient descent | 训练模型就是让 loss 下降 | 严格多元微积分证明 |
| Probability & Statistics | mean/variance, distribution intuition, conditional probability, train/test split, overfitting, evaluation metrics | 理解数据波动、泛化和模型好坏 | 测度论、复杂统计推断 |
| Machine Learning Core | supervised learning, feature/label, model/parameter, training vs prediction, linear regression, logistic regression, decision tree, evaluation | 建立第一个完整 ML mental model | deep learning 和论文 |

## Minimum Entry Standard

你可以开始第一个基础模型前，至少要能做到：

- 把一张数据表看成矩阵：row = sample，column = feature。
- 解释一个样本为什么可以看成向量。
- 把 model 理解成从 features 到 prediction 的函数。
- 把 loss 理解成 prediction error 的数字化。
- 把 gradient 理解成让 loss 下降的方向提示。
- 在这些概念稳定后，再训练一个基础 sklearn model。

## Learning Order

1. Python data handling: NumPy array shape, Pandas table, sample / feature.
2. Linear algebra for representation: vector, matrix, dot product, linear combination.
3. Functions, loss, and derivative / gradient intuition.
4. Probability and statistics for data split, overfitting, and evaluation.
5. First model: linear regression, then logistic regression or decision tree.

## First 7 Days

1. Days 1-2: NumPy shape and table-as-matrix.
2. Days 3-4: vectors, dot product, and linear combination.
3. Days 5-6: model as function and loss as error.
4. Day 7: small linear regression walkthrough without deep learning.

Today's first task: learn NumPy array shape and sample / feature meaning.

Check question: 如果数据有 100 个房子，每个房子有面积、卧室数、楼龄 3 个特征，
这张数据表的 shape 应该更像 \(100 \times 3\)，还是 \(3 \times 100\)？为什么？
