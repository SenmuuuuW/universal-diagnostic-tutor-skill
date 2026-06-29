# Error To Intervention Protocol

Use this protocol when a learner makes a mistake and the tutor needs to choose
the most efficient repair. Different error types need different interventions;
do not answer every mistake with the same generic re-explanation.

## Error Type To Intervention

| Error Type | Typical Signal | Efficient Intervention |
| --- | --- | --- |
| Notation error | Misreads a symbol, variable, graph mark, code token, or object role | Translate symbols into object roles |
| Concept error | Uses the wrong mental model | Build an intuition bridge or concrete example |
| Method selection error | Chooses the wrong test, theorem, algorithm, or formula | Compare problem cues side by side |
| Setup error | Cannot turn words into equations, code state, diagrams, or variables | Translate words into mathematical or computational objects |
| Proof error | Gives examples or code behavior but no reason it always works | Identify missing hinge, invariant, lower bound, construction, or assumption |
| Calculation error | Arithmetic, sign, algebra, syntax, or copying slip | Correct locally and add a check habit |
| Transfer error | Can solve the example but misses similar problems | Name reusable pattern and give near-transfer |
| Overgeneralization | Applies one pattern where it does not hold | Give counterexample or edge case |
| Memorized procedure without understanding | Gives rule or answer but cannot explain why | Ask a why-step check or teach the mechanism |

## Intervention Shapes

### Notation Error -> Symbol Translation

> Before solving, let's translate the symbols. In \(Ax=b\), \(b\) is not a
> point; it is the output vector we want \(Ax\) to equal.

### Concept Error -> Intuition Bridge

> The tempting model is that virtual memory means extra RAM. The better model
> is address translation: each process gets its own address view.

### Method Selection Error -> Cue Comparison

> Comparison test looks tempting, but the adjacent factors \(n(n+1)\) are a cue
> for telescoping. The first move is to try partial fractions.

### Setup Error -> Object Translation

> The phrase "parallel vectors" means one vector is a scalar multiple of the
> other, so translate it to \(u=cv\) before comparing components.

### Proof Error -> Hinge Or Invariant

> Your proof says what binary search does, but the missing invariant is: if the
> target exists, it stays inside the remaining interval after each cut.

### Calculation Error -> Local Correction

> The concept is right; the sign changed in this line. Fix that local step,
> then check by substituting back.

### Transfer Error -> Reusable Pattern

> You solved the example. The transfer cue is: when the same unknown is
> repeated in equal groups plus a fixed amount, set up a linear equation.

### Overgeneralization -> Counterexample

> That pattern works for this special case, but not always. A quick
> counterexample is enough to show where it breaks.

### Memorized Procedure -> Why-Step Check

> The formula is right. Tiny check: what does the denominator count in a
> conditional probability problem?

## Anti-Patterns

- Responding to every wrong answer with a full solution.
- Treating notation confusion as laziness or lack of effort.
- Correcting calculation slips by reteaching the entire topic.
- Giving more practice before repairing a stable wrong model.
- Skipping the reason why the wrong path felt tempting.
