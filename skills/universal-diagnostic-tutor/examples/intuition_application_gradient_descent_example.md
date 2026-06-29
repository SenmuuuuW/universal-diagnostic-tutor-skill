# Intuition Application Gradient Descent Example

## User Question

"我知道一点导数，但不懂 gradient descent 为什么重要。它在机器学习里到底干什么？"

## Expected Tutor Behavior

- Use a compact AI/ML knowledge map.
- Explain loss, parameters, and gradient with an intuition bridge.
- Connect the idea to model training without over-formalizing.
- Stop with one small check.

## Example Tutor Response

先定位一下：这是机器学习 -> 优化 -> 梯度下降。核心问题是：模型怎么一步步把错误变小。

先不用复杂公式。你可以把模型想成有很多“旋钮”的机器：这些旋钮就是 **parameters（参数）**。模型预测错多少，用一个数来衡量，这个数叫 **loss（损失）**。

训练就是不断调整参数，让 loss 变小。

gradient 可以理解成一个方向提示：如果你朝 gradient 的方向调参数，loss 增加得最快；所以 gradient descent 反过来走，朝负梯度方向移动，想让 loss 下降。

用一句话写就是：

\[
\text{new parameters} = \text{old parameters} - \text{step size} \cdot \text{gradient}
\]

它重要是因为很多 AI / ML 模型训练，本质上都是在做这件事：看预测错多少，然后一点点调整参数，让错误越来越小。

小检查：如果 gradient 指向“loss 上升最快”的方向，那我们为了降低 loss，应该顺着它走，还是反着它走？

## Why This Example Works

The response bridges derivative intuition to ML training, explains why the
concept matters, and stops with one check instead of launching into full
optimization theory.
