# Advanced Derivative Proof Example

## User Question

"I know the power rule. Give me a more rigorous concise explanation of why the
derivative of $x^2$ is $2x$."

## Selected Mode

Advanced Mode.

## Diagnosis

- **Subject routing:** Calculus / derivative proof.
- **Likely gap:** Reasoning behind a known rule, not basic derivative meaning.
- **Starting point:** Use the limit definition efficiently.

## Expected Pacing Choice

Give the proof hinge concisely, justify the algebraic step, and include the
interpretation. A stop point is optional because the learner requested concise
advanced explanation.

## Example Tutor Response

Use the derivative definition:

$$
f'(x)=\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}
$$

For $f(x)=x^2$:

$$
\begin{aligned}
f'(x)
&= \lim_{h\to 0}\frac{(x+h)^2-x^2}{h} \\
&= \lim_{h\to 0}\frac{x^2+2xh+h^2-x^2}{h} \\
&= \lim_{h\to 0}\frac{2xh+h^2}{h} \\
&= \lim_{h\to 0}(2x+h) \\
&= 2x
\end{aligned}
$$

The key assumption in the simplification step is that while forming the
difference quotient, $h \neq 0$, so dividing by $h$ is valid. Only after
simplifying do we take the limit as $h \to 0$.

Interpretation: the local slope of $x^2$ at input $x$ is $2x$.

## Stop Point Or Check Question

"Which step would fail if we substituted $h=0$ before simplifying?"

## Why This Mode Fits The Learner

The learner already knows the rule and asks for rigor, so the tutor uses formal
notation, states the key assumption, and avoids re-explaining basic slope.

## Formatting Note

The derivation uses aligned display math instead of a code block.
