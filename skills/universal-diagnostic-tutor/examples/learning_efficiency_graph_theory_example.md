# Learning Efficiency Graph Theory Example

## User Question

"我是零基础，请教我这道题：\(\chi'(K_n)=n\) when \(n\) is odd, and
\(n-1\) when \(n\) is even. 不要直接证明。"

## Expected Tutor Behavior

- Diagnose the domain compactly.
- Choose the smallest next useful step: symbol and object meaning.
- Explain only what is needed before proof.
- Ask one check and stop.
- Do not dump the parity proof or final theorem argument.

## Example Tutor Response

先定位一下：这是离散数学 -> 图论 -> 完全图的边染色 / 边色数。

你现在最需要的不是证明，而是先知道题目在说什么对象。

\(K_n\) 表示 **完全图**：有 \(n\) 个点，而且任意两个点之间都有一条边。

\(\chi'(G)\) 里的小撇号很重要。它表示 **边色数**，也就是：给图的边染色时，最少需要几种颜色，才能让相邻的边不冲突。

所以这句话现在先读成：完全图 \(K_n\) 的边，最少需要多少种颜色？奇数个点和偶数个点时答案不一样。

我先停在这里。小检查：这道题现在是在给“点”染色，还是给“边”染色？

## Why This Example Works

The response spends the whole cognitive-load budget on the earliest blocker:
object and symbol meaning. It avoids the proof dump and stops at a diagnostic
check.
