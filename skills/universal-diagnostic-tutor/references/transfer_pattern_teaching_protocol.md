# Transfer-Pattern Teaching Protocol

Use this protocol after the learner has understood a step, completed a
subproblem, answered a check correctly, or asks how to recognize similar
problems later.

The goal is to teach the reusable pattern, not only the current solution.

## Core Transfer Questions

After teaching a problem, extract:

- **Clue:** What feature should the learner notice?
- **Method:** What method or representation does the clue suggest?
- **Trap:** What tempting wrong move should they avoid?
- **Variation:** What might change in the next similar problem?

Keep the transfer cue short. Usually one or two sentences plus one tiny
near-transfer question is enough.

## When To Use

Use transfer teaching when:

- The learner answers a check correctly.
- A subproblem is complete.
- The learner says they understand examples but cannot start new problems.
- The topic is exam prep, homework practice, debugging, proof, or method
  recognition.
- The learner has repeated a mistake and needs a prevention cue.

## When To Keep It Tiny

In early Zero-Base Mode, use very small transfer patterns:

```text
以后看到 \\(K_n\\)，先想到“完全图”：每两个点之间都有边。
```

Do not jump from symbol recognition to broad mixed-topic practice.

## Standard And Advanced Transfer

- **Standard Mode:** Emphasize method-recognition cues and near-transfer.
- **Advanced Mode:** Emphasize proof patterns, assumptions, invariants, edge
  cases, and when the method fails.

## Examples

- If you see \\(n(n+1)\\) in a denominator, consider telescoping or partial
  fractions.
- If a problem says one vector is a scalar multiple of another, translate it
  to \\(u = cv\\) and compare components.
- If a proof about binary search asks why it works, look for the invariant:
  the target, if present, stays inside the remaining search range.
- If a probability statement contains "given," check the denominator. It is
  usually the conditioned group, not the total sample space.
- If gradient descent appears, identify loss, parameters, gradient, and update
  rule before manipulating formulas.

## Transfer Cue Shape

```text
Reusable cue: When you see [clue], think [method].
Trap: Do not [tempting wrong move].
Try one tiny transfer: [small changed task].
```

Use this shape flexibly. In natural answers, one paragraph may be better than
visible labels.

## Anti-Patterns

- Ending after the final answer with no recognition cue.
- Giving many unrelated practice problems before naming the reusable pattern.
- Jumping to hard mixed practice after a learner barely followed one example.
- Making transfer sound like a rigid formula that works in every context.
- Giving a long course roadmap when the learner needs the next cue.
