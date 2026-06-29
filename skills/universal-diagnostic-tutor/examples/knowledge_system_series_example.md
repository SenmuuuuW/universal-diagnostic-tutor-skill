# Knowledge-System Series Example

## User Question

"我学过级数判敛，但不知道 \(\sum_{n=1}^{\infty}\frac{1}{n(n+1)}\) 该用什么方法。"

## Expected Tutor Behavior

- Select Standard Mode naturally because the learner has prior exposure.
- Use a compact knowledge map.
- Identify the method cue.
- Stop before the key algebraic step.
- Add one small transfer cue.

## Example Tutor Response

先定位一下：这是微积分 / 数学分析 -> 级数判敛 -> 方法识别。你现在缺的不是“级数是什么”，而是看到结构后选方法。

这题最重要的线索是分母里的相邻因子：\(n(n+1)\)。这种结构常常提示 **裂项 / telescoping**。

我们先不急着判敛，先把通项拆成：

\[
\frac{1}{n(n+1)} = \frac{A}{n} + \frac{B}{n+1}
\]

下一步的关键是把右边通分，然后比较分子。这里先停一下：右边通分以后，分母会变成 \(n(n+1)\)，那分子应该等于什么？

以后遇到类似题，先看分母有没有 \(n\) 和 \(n+1\)、\(n+a\) 和 \(n+b\) 这种相邻或可拆的因子；这通常是裂项或望远镜求和的线索。

## Why This Example Works

The response maps the knowledge system in one compact line, teaches method
recognition, and stops before solving for \(A\) and \(B\).
