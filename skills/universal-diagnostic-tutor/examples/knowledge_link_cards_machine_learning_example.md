# Knowledge Link Cards：机器学习入门

## 学习者

> 我刚开始学线性回归。讲义同时出现了数据矩阵 \(X\)、loss 和 gradient。
> loss 我大概知道是预测误差，但矩阵和 gradient 为什么会出现在这里？

## Tutor 判断

当前任务是理解“训练线性回归时各对象做什么”。loss 已有初步认识；数据矩阵和
梯度是现在无法跳过的两个强连接概念，因此只补两张卡。

## 卡 1：数据矩阵 \(X\)

- **Knowledge point：** 矩阵。
- **What it is：** 按行、列排列的数值表。
- **Why it matters here：** 机器学习需要同时表示许多样本和每个样本的特征。
- **How it connects：** 在线性回归中，\(X\) 的每一行通常是一个样本，每一列
  通常是一个特征；\(Xw\) 会为所有样本生成预测。
- **Minimum mastery needed now：** 能辨认行、列、shape，并知道
  \(X\in\mathbb{R}^{n\times d}\) 常表示 \(n\) 个样本、\(d\) 个特征。
- **Skip for now：** 特征值、SVD 和严格线性代数证明。
- **Small example：** 100 套房子、每套 3 个特征，可以写成
  \(100\times 3\) 的矩阵。

## 卡 2：梯度

- **Knowledge point：** gradient。
- **What it is：** loss 对各个模型参数的变化方向和敏感程度的汇总。
- **Why it matters here：** 训练要调整参数 \(w\)，使 loss 变小。
- **How it connects：** \(X\) 和 \(w\) 产生预测，预测产生 loss；梯度再告诉我们
  参数应朝哪个方向调整。梯度下降通常沿负梯度更新。
- **Minimum mastery needed now：** 知道梯度是“参数空间中的方向提示”，并能区分
  参数、预测和 loss。
- **Skip for now：** 多元微积分的严格证明、Hessian 和高级优化算法。
- **Small example：** 若某个参数增大时 loss 上升，沿相反方向小幅调整通常会让
  loss 下降。

## 回到当前任务

先检查数据表示，不扩展更多概念：如果有 100 个样本、每个样本 3 个特征，
\(X\) 的 shape 更可能是 \(100\times 3\) 还是 \(3\times 100\)？为什么？

## 为什么只用两张卡

两张卡都直接解除当前线性回归任务的阻塞，并明确了最低掌握要求与暂缓内容；回答
随后回到当前检查题，没有展开成机器学习百科或资源列表。
