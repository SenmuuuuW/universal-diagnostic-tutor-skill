# Internal Tool Leakage Bad Vs Good Example

## Purpose

Show how to avoid exposing Skill names, versions, file names, or protocol names
inside ordinary tutoring answers.

## User Question

"我是零基础，\(Ax=b\) 到底是什么意思？请像老师一样讲。"

## Bad Response

This is bad because it exposes internal implementation details instead of just
teaching:

```text
I will use the updated universal-diagnostic-tutor V1.3 student-facing response
protocol and STEM symbol notation protocol to explain this in Zero-Base Mode.
```

## Good Tutor Response

可以，我们按零基础来。先定位一下：这是线性代数里的矩阵方程，核心是理解 \(A\)、\(x\)、\(b\) 分别是什么。

先不要解方程，先把它翻译成人话：

\[
Ax=b
\]

- \(A\) 是一个 matrix（矩阵），可以看成一个会改变向量的规则。
- \(x\) 是我们想找的 input vector（输入向量）。
- \(b\) 是得到的 output vector（输出向量）。

所以这句话的意思是：找到一个输入 \(x\)，让矩阵 \(A\) 作用在它身上以后，结果变成 \(b\)。

这里先停一下：在 \(Ax=b\) 里，我们通常要找的是 \(A\)、\(x\)，还是 \(b\)？

## Why The Good Response Works

It uses the same internal teaching judgment but expresses it naturally. The
learner sees domain diagnosis, symbol translation, and a stop point, not the
project machinery behind the answer.
