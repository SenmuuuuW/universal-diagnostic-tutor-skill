# Exam Pattern Resource Analysis

Use this protocol when the learner asks about exam prep, repeats a mistake, is
trying to recognize problem types, or asks how a knowledge point is commonly
tested. Do not overuse it when the learner only needs a concept explanation.

The goal is to teach the reusable pattern, not to turn the answer into a course
roadmap or solution dump.

## Core Sequence

1. **Identify the tested concept.** What idea is the question really checking?
2. **Identify prerequisites.** What definitions, notation, facts, or procedures
   must be in place?
3. **Identify common question forms.** How does this topic usually appear?
4. **Identify common traps.** What tempting wrong methods appear often?
5. **Explain why the wrong method feels tempting.** Connect it to a plausible
   but incomplete cue.
6. **Name the method-recognition cue.** What tells the learner this method
   applies?
7. **Name the minimal transferable skill.** What should the learner be able to
   do on a similar problem?
8. **Recommend a short practice ladder.** Use one or two rungs, not a long
   worksheet.
9. **Use resources when useful.** Public past exams, problem sets, open
   textbooks, official docs, or reputable exercise sources can reveal patterns.

## Resource Use

When web/search access is available and exam-pattern analysis would improve the
answer:

- Prefer official or university problem sets, labs, assignments, sample exams,
  and public course materials.
- Use exercise sources to identify patterns and traps, not to copy solutions.
- Cite or name only sources actually checked.
- Avoid pirated PDFs, answer-only sites, SEO farms, and uncited solution dumps.
- If source access is unavailable, say so and teach from foundations.

## STEM Pattern Examples

### Linear Algebra

- **Concepts:** scalar multiples, vector equations, span, basis, matrix
  transformations.
- **Question forms:** "Is this vector in the span?", "Are these vectors
  independent?", "Find coefficients," "Interpret `Ax = b`."
- **Traps:** Treating vectors as unrelated lists of numbers; solving for the
  wrong object; confusing point, vector, and transformation.
- **Recognition cue:** The question asks whether one object can be built from
  others using linear combinations.

### Calculus

- **Concepts:** derivative rules, limit definition, optimization.
- **Question forms:** "Find the derivative," "Explain the rate of change,"
  "Optimize under a constraint."
- **Traps:** Applying a memorized rule without conditions; confusing average
  and instantaneous rate; differentiating before identifying the variable.
- **Recognition cue:** The question asks about changing quantity, slope, or
  best value.

### Probability

- **Concepts:** conditioning, independence, expectation.
- **Question forms:** "Given that...", "Are events independent?", "Find the
  expected value."
- **Traps:** Dividing by the total sample space after a condition is given;
  treating independence as mutually exclusive; using intuition without a
  denominator check.
- **Recognition cue:** A phrase such as "given," "among," or "if we know"
  changes the denominator.

### Programming

- **Concepts:** loops, recursion, state mutation, debugging.
- **Question forms:** trace output, fix a bug, identify base case, explain why
  state did not change.
- **Traps:** Confusing printing with storing, mutating a local copy, missing
  the base case, or assuming one loop iteration represents the whole program.
- **Recognition cue:** The question asks what changes over time or when the
  repeated process stops.

### Algorithms

- **Concepts:** invariants, complexity, data structures.
- **Question forms:** prove correctness, choose data structure, analyze runtime,
  handle edge cases.
- **Traps:** Choosing by surface words rather than operations; ignoring the
  invariant; counting lines instead of operations.
- **Recognition cue:** The input structure and required operations point to the
  algorithmic pattern.

### AI / ML

- **Concepts:** loss, gradient, overfitting, evaluation.
- **Question forms:** explain training update, choose metric, diagnose
  overfitting, interpret validation results.
- **Traps:** Treating loss as accuracy, treating a gradient as one ordinary
  slope, evaluating on training data only.
- **Recognition cue:** The question asks what the model is optimizing or how it
  generalizes.

### Systems

- **Concepts:** memory, process, network layers.
- **Question forms:** explain virtual memory, trace a system call, map layers,
  diagnose packet flow.
- **Traps:** Treating virtual memory as only extra RAM; mixing process view
  with hardware view; skipping layers.
- **Recognition cue:** The question asks which abstraction layer is responsible
  for a behavior.

## Compact Output Pattern

```text
This is testing [concept], not just [surface task].
The trap is [tempting wrong cue].
The recognition cue is [how to know the method applies].
Try one rung: [short practice item].
```
