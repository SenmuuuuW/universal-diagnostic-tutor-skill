# Context Compression Checkpoint: Series Example

Scenario: after working on \(\sum \frac{1}{n^2+n}\), the learner wants to stop
and continue later.

## Tutor Response

可以，我们把现在的进度压缩一下，方便下次继续。

- **What you learned:** 这题是微积分 / 数学分析里的级数判敛，关键线索是 \(n^2+n=n(n+1)\)。相邻因子通常提示裂项或望远镜求和。
- **What is still weak:** 你能看出结构，但还不稳地把
  \(\frac{1}{n(n+1)}\) 写成 \(\frac{A}{n}+\frac{B}{n+1}\)。
- **Mistake to watch:** 不要先把所有判别法都试一遍；先看分母结构有没有能裂开的线索。
- **Next best step:** 练习把等式两边同乘 \(n(n+1)\)，得到关于 \(A\) 和 \(B\) 的关系。
- **Continue prompt:** "继续这道级数题。我已经知道 \(n(n+1)\) 是裂项线索，但还不会求 \(A\) 和 \(B\)。请从同乘分母那一步继续。"

下次贴最后一句就够了；如果要换聊天，可以贴整段 checkpoint。
