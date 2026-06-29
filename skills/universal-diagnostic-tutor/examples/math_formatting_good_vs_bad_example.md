# Math Formatting Good Vs Bad Example

## User Question

"我是零基础。老师写了 \(\chi'(K_n)\)，我完全不知道这是什么意思。不要直接证明。"

## Selected Mode

Zero-Base Mode with formatting guidance.

## Diagnosis

- **Subject routing:** Discrete math -> graph theory -> edge coloring.
- **Likely gap:** The learner needs symbol, object-type, and formatting
  support before proof.
- **Starting point:** Explain the symbols and stop after one check.

## Expected Pacing Choice

Use one short domain diagnosis, explain the two or three symbols, show the
right math delimiters, then stop with a check question.

## Example Tutor Response

先判断领域：这是离散数学 -> 图论 -> 边染色。

先不要证明，先把符号翻译成人话。

Bad formatting in a tutoring answer: raw dollar signs may show up literally in
some chat environments, and code blocks make math look like terminal text.

`$K_n$ 是完全图，$\chi'(G)$ 是边色数。`

```text
chi'(K_n) = minimum number of edge colors
```

Good formatting: use \(...\) for inline math and \[...\] for display math.

\(K_n\) 是 **complete graph（完全图）**：有 \(n\) 个点，而且每两个点之间都有一条边。

**Edge coloring（边染色）** 是给边上色，不是给点上色。规则通常是：如果两条边碰到同一个点，它们不能用同一种颜色。

\(\chi'(G)\) 读作图 \(G\) 的 **edge chromatic number（边色数）**，意思是“给图 \(G\) 的边染色，最少需要几种颜色”。

所以 \(\chi'(K_n)\) 问的是：完全图 \(K_n\) 的边最少要用几种颜色。

也可以把“边色数”的意思用 display math 写清楚：

\[
\chi'(G)=\text{minimum number of edge colors needed for }G
\]

Use fenced code blocks for actual code, commands, paths, or literal text where
spacing matters. Use math formatting for algebra, calculus, linear algebra,
probability, and proofs.

我先停在这里。小检查：这里研究的是给“点”染色，还是给“边”染色？

## Stop Point Or Check Question

"这里研究的是给点染色，还是给边染色？"

## Why This Mode Fits The Learner

The learner is zero-base and asks about graph-theory notation. The tutor starts
with domain diagnosis, explains symbols before proof, demonstrates reliable
math delimiters, and stops after one check question.

## Formatting Note

The code block and raw dollar-sign snippet appear only as intentionally bad
formatting examples. The correct tutoring response uses \(...\) and \[...\].
