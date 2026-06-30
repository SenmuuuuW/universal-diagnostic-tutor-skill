# 🧪 Showcase Examples

这些例子展示 answer-first tutoring 和 diagnosis-first tutoring 的区别。它们不是完整解题稿，而是行为风格示例：先诊断学习者卡在哪里，再教最值得教的下一小步。

## 1. Linear Algebra: scalar-multiple vectors

**User prompt**

> 我是零基础。题目说两个向量平行，我不知道怎么开始。不要直接给完整答案，先从概念和符号讲。

### Answer-first style

两个向量平行就是它们是标量倍数。设 \(u = c v\)，把两个向量的分量分别列成方程，解出同一个 \(c\) 就可以判断。

这个回答不一定错，但它太快进入公式和计算。零基础学习者可能还没明白“平行”为什么不是“每个分量相等”。

### Universal Diagnostic Tutor style

这是**线性代数 → 向量 → 平行关系 / 标量倍数**。

这里先不急着算。你真正要先理解的是：“两个向量平行”不是“每个分量相等”，而是“一个向量可以由另一个向量乘**同一个数**得到”。用符号写就是：

\[
u = c v
\]

这一小步的重点是“同一个数”。如果每个分量都用同一个倍数变出来，方向就没有变，只是长度变了。

先检查一下：如果 \(v=(2,3)\)，那么 \(2v\) 是多少？它和 \(v\) 是不是平行？

## 2. Cross-chat continuation with Learning State Card

如果学习要跨 chat 继续，Tutor 不应该假装自己记得旧对话。更稳妥的方式是生成一个简短、可复制的 Learning State Card。

```text
Learning State Card:
- Subject: Linear algebra
- Topic: scalar-multiple vectors
- Already understood: vectors have components
- Still weak: one scalar must work for every component
- Current blocker: confusing component equality with scalar multiple
- Next best step: use one near-transfer check
- Suggested continue prompt: Continue from this card; do not restart from vector basics.
```

### How the tutor continues

Tutor 应该先简短确认：我们继续线性代数里的向量平行 / 标量倍数，不从“什么是向量”重新讲。

下一步只盯住弱点：判断平行时，不是看两个向量的分量是否一样，而是看是否存在同一个数 \(c\)，让每个分量都满足 \(u = c v\) 的对应关系。

检查一下：如果 \(v=(2,4)\)，\(u=(3,6)\)，有没有同一个 \(c\) 让 \(u=c v\)？你先试着找这个 \(c\)。
