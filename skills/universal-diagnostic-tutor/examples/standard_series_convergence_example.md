# Standard Series Convergence Example

## User Question

"我学过级数判别法，但看到题目还是不知道用哪个。比如这个：判断 \(\sum_{n=1}^{\infty} \frac{1}{n(n+1)}\) 是否收敛。"

## Selected Mode

Standard Mode.

## Diagnosis

- **Subject routing:** Calculus / series convergence.
- **Likely gap:** Method recognition gap.
- **Starting point:** Identify the cue before applying a test.

## Expected Pacing Choice

Briefly name the pattern, show the first rewrite target, and stop before the
key algebraic decomposition.

## Example Tutor Response

先判断领域：这是微积分 -> 级数 -> 判敛方法识别。

你不是没学过级数；卡点是“看到题目怎么判断方法”。

这个题的关键 cue 是分母：

\[
n(n+1)
\]

它由两个相邻因子组成，这常常提示 **telescoping（裂项相消）**。我们想把它拆成：

\[
\frac{1}{n(n+1)} = \frac{A}{n} + \frac{B}{n+1}
\]

先别急着求和。关键步骤是找到 \(A\) 和 \(B\)。

把右边通分：

\[
\frac{A}{n} + \frac{B}{n+1}
= \frac{A(n+1)+Bn}{n(n+1)}
\]

停在这里：为了让它等于 \(\frac{1}{n(n+1)}\)，分子 \(A(n+1)+Bn\) 应该等于什么？

## Stop Point Or Check Question

"分子 \(A(n+1)+Bn\) 应该等于什么？"

## Why This Mode Fits The Learner

The learner has seen convergence tests, so the tutor does not re-teach what a
series is. It focuses on the recognition cue and one guided algebra step.

## Formatting Note

The series and decomposition use LaTeX display math for readability.
