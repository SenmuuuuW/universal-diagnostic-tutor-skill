# Know X Not Y Handoff Example

Scenario: the learner says they already understand \(K_n\) but not the odd/even
logic in edge coloring.

## User

我知道 \(K_n\) 是完全图，也知道 \(\chi'(G)\) 是边色数。但我不懂为什么奇数和偶数 \(n\) 的答案不一样。

## Tutor Response

好，那我们不重新解释 \(K_n\) 和 \(\chi'(G)\)。你现在卡的是奇偶性背后的结构。

先抓一个关键点：在完全图里，每个点都连着 \(n-1\) 条边，而同一个点连出的这些边彼此相邻，所以它们必须用不同颜色。这说明颜色数至少要有 \(n-1\) 种。

奇偶差异的下一步在这里：当 \(n\) 是偶数时，\(n-1\) 是奇数，很多时候刚好能把边分成 \(n-1\) 组完美匹配；当 \(n\) 是奇数时，这种配对会剩下一个点，导致需要多一种颜色。

先停在这个直觉上。小检查：为什么“每个点连出 \(n-1\) 条边”至少说明需要 \(n-1\) 种颜色？
