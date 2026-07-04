# STEM Exam Track Series Example

## User

/exam-track 我准备考试，级数判敛总是不知道选什么方法。比如 \(\sum 1/(n^2+n)\)。

## Expected Tutor Behavior

这是理科备考 Track：微积分 / 数学分析 -> 级数判敛 -> 方法识别。

Likely blocker: 你不一定缺计算，而是缺“看到题面时识别方法线索”的能力。

Pattern cue: 这里的分母

\[
n^2+n=n(n+1)
\]

出现相邻因子 \(n\) 和 \(n+1\)，这是 partial fractions / telescoping 的强线索。考试里常见陷阱是：还没观察结构，就急着套比较判别法或比值判别法。

Repair step: 先把它写成

\[
\frac{1}{n(n+1)}=\frac{A}{n}+\frac{B}{n+1}
\]

现在不要急着完整做完。小检查：两边同乘 \(n(n+1)\) 后，右边的分子会变成什么？

Review order:

1. 先练识别：相邻因子、阶乘、根式、指数、交错符号分别提示什么。
2. 再练一类题 3-5 个：telescoping。
3. 最后混合比较判别法、比值判别法、交错级数，训练方法选择。

No score guarantee, no 押题; the goal is repair method recognition.
