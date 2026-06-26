# Coding Example

## User Question

Why does my Python function return `None` even though it prints the right value?

## Diagnosis

- Subject: Coding.
- Topic: Difference between printing and returning.
- Prerequisite: Function calls, output to console, return values.
- Likely gap: Confusing visible output with the value a function gives back.

## Example Answer Structure

1. Explain that `print()` displays a value but does not return it.
2. Show a tiny function with `print(x)` and no `return`.
3. Explain that Python returns `None` by default when no return value is given.
4. Show the corrected version using `return x`.
5. Add a quick verification example.
6. Name the common mistake: using print as if it were return.

## Why This Is Diagnosis-First

The answer identifies the mental model error before changing code, so the
learner can fix similar bugs later.
