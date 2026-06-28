# Math Formatting Good Vs Bad Example

## User Question

"Show me how to format a derivation nicely. Sometimes math looks like code."

## Selected Mode

Formatting guidance mode with Standard Mode teaching.

## Diagnosis

- **Subject routing:** Math communication / formatting.
- **Likely gap:** The learner needs to distinguish mathematical notation from
  literal code or terminal text.
- **Starting point:** Show bad formatting, then the corrected version.

## Expected Pacing Choice

Show one bad example and one good example, then ask the learner to identify why
the good version is more readable.

## Example Tutor Response

Bad formatting: this makes the math look like code or terminal output.

```text
f'(x) = lim h->0 ((x+h)^2 - x^2) / h
      = lim h->0 (2xh + h^2) / h
      = 2x
```

Good formatting: use Markdown/LaTeX math for formulas.

$$
\begin{aligned}
f'(x)
&= \lim_{h\to 0}\frac{(x+h)^2-x^2}{h} \\
&= \lim_{h\to 0}\frac{2xh+h^2}{h} \\
&= 2x
\end{aligned}
$$

Use fenced code blocks for actual code, commands, paths, or literal text where
spacing matters. Use math formatting for algebra, calculus, linear algebra,
probability, and proofs.

Tiny check: which version makes the fraction structure easier to see?

## Stop Point Or Check Question

"Which version makes the fraction structure easier to see?"

## Why This Mode Fits The Learner

The learner is not asking for a proof; they are asking how to communicate math
cleanly. The tutor teaches one formatting contrast and checks the visual
reason.

## Formatting Note

The code block appears only as an intentionally bad example. The correct math
uses aligned display math.
