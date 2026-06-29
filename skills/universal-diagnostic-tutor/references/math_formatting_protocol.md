# Math Formatting Protocol

Use this protocol whenever tutoring includes mathematical expressions,
derivations, formulas, equations, probability notation, linear algebra,
calculus, proofs, or symbolic reasoning.

Mathematics should look like mathematics, not code.

## Core Rules

- Do not put mathematical formulas in fenced code blocks.
- Do not use code blocks for ordinary algebra, calculus, linear algebra,
  probability, or proof steps.
- In user-facing tutoring responses, prefer `\(...\)` for inline math and
  `\[...\]` for display math.
- Avoid `$...$` inline math in normal tutoring text because some chat
  environments show raw dollar signs.
- Do not show raw dollar-sign formulas such as `$K_n$`, `$G$`, `$n$`, or
  `$A+B=0$` in ordinary teaching responses.
- Use inline math for short expressions, such as `\(A+B=0\)`.
- Use display math for important formulas.
- Use aligned display math for multi-line derivations.
- Use clean paragraphs plus LaTeX formulas for math tutoring.
- Keep formulas readable on GitHub and in chat.
- Avoid excessive boxed or code-card style formatting.
- In GitHub documentation, dollar-delimited math may appear only when
  discussing formatting itself or showing an intentionally bad example.
- If the host renderer has weak LaTeX support, use plain text formulas inline,
  but still avoid fenced code blocks.

## Preferred Formatting

Inline math:

\(A+B=0\)

Display math:

\[
\frac{1}{n(n+1)} = \frac{A}{n} + \frac{B}{n+1}
\]

Piecewise display math:

\[
\chi'(K_n)=
\begin{cases}
n, & n \text{ is odd} \\
n-1, & n \text{ is even}
\end{cases}
\]

Aligned derivation:

\[
\begin{aligned}
A(n+1)+Bn &= 1 \\
(A+B)n + A &= 1
\end{aligned}
\]

Short proof steps can be written as paragraphs with inline math:

Since \(h \neq 0\) during the simplification step, we can divide by \(h\)
before taking the limit as \(h \to 0\).

## When Code Blocks Are Appropriate

Use fenced code blocks only for:

- Actual programming code.
- Terminal commands.
- File paths or repository commands.
- Literal text where spacing is essential.
- A deliberately bad formatting example in documentation or examples.

## Bad Math Formatting

Avoid this for ordinary math:

```text
(x+h)^2 - x^2
----------------
       h
```

Use display math instead:

\[
\frac{(x+h)^2 - x^2}{h}
\]

## Mixed Code And Math

For programming explanations, use code blocks for code and math formatting for
math:

```python
theta = theta - alpha * gradient
```

Then explain the update as math:

\[
\theta \leftarrow \theta - \alpha \nabla L(\theta)
\]

Do not format the mathematical update as code unless discussing the literal
program text.
