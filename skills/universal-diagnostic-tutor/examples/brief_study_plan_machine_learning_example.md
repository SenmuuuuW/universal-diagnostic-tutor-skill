# Brief Study Plan Machine Learning Example

## User

/study-plan 我想学机器学习，但数学很弱，会一点 Python。应该先补什么？

## Expected Tutor Behavior

Current state: 你有一点 Python，机器学习目标明确，但数学基础不稳。这里不要直接给
"Python -> 线代 -> 概率 -> scikit-learn" 这种泛路线，先说清楚每个学科到底要学哪一小部分。

Goal: 能看懂基础 ML 里的数据、模型、loss、训练和评估。

Required disciplines:

| Discipline | Must-learn parts | Skip for now |
| --- | --- | --- |
| Programming / Python | NumPy array shape, Pandas tables, basic plotting | large software projects |
| Linear Algebra | vectors, matrices, row/sample, column/feature, dot product, linear combination | eigenvalues and SVD |
| Calculus / Optimization | function, slope, derivative intuition, gradient, loss, gradient descent | rigorous multivariable proofs |
| Probability / Statistics | mean/variance, distribution intuition, conditional probability, train/test split, overfitting, metrics | advanced inference |
| ML Core | feature/label, model/parameter, training vs prediction, linear regression, evaluation | deep learning too early |

Minimum entry standard: 能把数据表看成矩阵，解释 row/sample 和 column/feature，
把 model 看成函数，把 loss 看成误差，把 gradient 看成让 loss 下降的方向提示。

Suggested order:

1. Python data handling: NumPy shape and simple table operations.
2. Linear algebra for data representation: vector, matrix, dot product.
3. Functions, loss, derivative / gradient intuition.
4. Probability / statistics for evaluation and overfitting.
5. First model: linear regression before deep learning.

Today's first step: 先学 NumPy array shape 和 sample / feature 含义。

Check question: 如果一张表有 100 个样本、每个样本 5 个特征，你觉得它更像一个向量，还是一个 \(100 \times 5\) 的矩阵？

Optional resources: 如果能搜索，优先找大学线性代数公开课、概率统计入门资料和官方 / 可信的 ML 入门课程；不要从高级论文开始。
