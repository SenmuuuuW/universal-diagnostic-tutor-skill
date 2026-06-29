# Next Best Step Series Example

## User Question

"我学过级数判敛，但不知道 \(\sum_{n=1}^{\infty}\frac{1}{n(n+1)}\) 收不收敛。"

## Expected Tutor Behavior

- Treat this as Standard Mode because the learner has prior exposure.
- Choose the next best step as structural cue recognition.
- Do not list all convergence tests.
- Do not finish the whole convergence proof.
- Ask the learner to complete one tiny algebraic step.

## Example Tutor Response

先定位一下：这是微积分 / 数学分析 -> 级数判敛 -> 方法识别。

这题的下一步不是先背所有判别法，而是先看通项结构：分母是 \(n(n+1)\)，两个相邻因子。这通常提示 **裂项 / 望远镜求和**。

先把通项设成：

\[
\frac{1}{n(n+1)}=\frac{A}{n}+\frac{B}{n+1}
\]

现在只做一个小步骤：把右边通分后，分母会是 \(n(n+1)\)。

这里停一下：右边的分子应该写成什么？

## Why This Example Works

The tutor identifies the one useful cue, sets up the method, and leaves the
learner the next algebra step instead of completing the entire proof.
