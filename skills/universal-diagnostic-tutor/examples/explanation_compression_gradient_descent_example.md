# Explanation Compression Gradient Descent Example

## User Question

"我知道导数是什么意思，但不懂 gradient descent。请不要从导数重新讲。"

## Expected Tutor Behavior

- Trust the declared prerequisite provisionally.
- Skip derivative basics.
- Focus on loss, parameter, gradient, and update.
- Keep the explanation compact.
- Ask one check.

## Example Tutor Response

好，那我们不重讲导数，直接接到 gradient descent 的四个对象。

在机器学习里：

- **parameter** 是模型里可以调的旋钮。
- **loss** 是模型现在错得有多严重。
- **gradient** 告诉你：如果参数往某个方向动，loss 会怎么变。
- **update** 是每一步实际怎么改参数。

因为 gradient 指向 loss 增加最快的方向，所以我们为了让 loss 下降，就往反方向走：

\[
\text{new parameter}=\text{old parameter}-\text{step size}\cdot\text{gradient}
\]

一句话：gradient descent 就是反复做“小步往更少错误的方向调参数”。

小检查：如果 gradient 表示 loss 上升最快的方向，要降低 loss，我们应该顺着 gradient 走，还是反着走？

## Why This Example Works

The tutor compresses known derivative background and spends the response on the
learner's actual blocker: how derivatives become parameter updates.
