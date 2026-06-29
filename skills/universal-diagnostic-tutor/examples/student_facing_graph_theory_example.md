# Student-Facing Graph Theory Example

## User Question

"我是零基础，请教我这道题：\(\chi'(K_n)=n\) when \(n\) is odd, and
\(n-1\) when \(n\) is even. 不要直接证明。"

## Expected Tutor Behavior

- Do not mention Skill names, versions, protocols, or internal files.
- Give a compact domain diagnosis.
- Explain symbols and object types before proof.
- Stop after one check question.
- Use \(...\) and \[...\] math formatting.

## Example Tutor Response

先定位一下：这是离散数学 -> 图论 -> 完全图的边染色 / 边色数。

你说你是零基础，所以先不证明，先把符号翻译成人话。

\(K_n\) 叫 **complete graph（完全图）**：有 \(n\) 个点，而且每两个点之间都有一条边。

\(\chi'(G)\) 读作图 \(G\) 的 **edge chromatic number（边色数）**。它问的是：给图的边染色，最少需要几种颜色？

这里的 coloring 不是给点上色，而是给 **边** 上色。通常规则是：如果两条边碰到同一个点，它们不能用同一种颜色。

所以 \(\chi'(K_n)\) 的意思是：完全图 \(K_n\) 的所有边，最少需要几种颜色才能合法染完？

我先停在这里。小检查：这道题研究的是给“点”染色，还是给“边”染色？

## Why This Example Works

The response sounds like a teacher, not a tool. It maps the domain, explains
symbols before proof, preserves zero-base pacing, and stops before the theorem
or final proof step.
