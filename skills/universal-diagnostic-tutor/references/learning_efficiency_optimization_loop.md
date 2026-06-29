# Learning Efficiency Optimization Loop

Use this protocol when a tutoring turn could become too broad, too slow, or too
answer-heavy. It upgrades the adaptive teaching loop by asking the tutor to
maximize learning gain per response while minimizing unnecessary cognitive
load.

This does not mean shorter at all costs. It means choosing the smallest useful
teaching move that changes what the learner can understand or do next.

Silent tutor question:

```text
What is the smallest next step that will most improve this learner's understanding right now?
```

## Optimized Loop

1. **Diagnose the current knowledge system and immediate gap.** Identify the
   subject, subtopic, prerequisite, and the one blocker most likely to stop the
   learner now.
2. **Select the next best teaching step.** Choose the concept, symbol, method
   cue, reasoning hinge, or misconception repair that unlocks the next move.
3. **Choose the lowest sufficient explanation depth.** Use enough explanation
   to make the step usable, but do not expand into a full lesson by default.
4. **Teach one compact unit.** Give one idea, one representation, or one
   worked micro-step.
5. **Ask one diagnostic check.** The check should reveal whether the learner
   can use the compact unit.
6. **Interpret the learner's response as a mastery signal.** Do not only mark
   right or wrong; infer what the response shows about understanding.
7. **Decide the next move.** Advance, transfer, compress, re-explain, or step
   down based on the signal.

## What Counts As Learning Gain

- The learner understands one symbol that was blocking the problem.
- The learner can identify the method cue before solving.
- The learner can explain why a step is allowed.
- The learner repairs one misconception.
- The learner completes one step with less help than before.
- The learner recognizes how the pattern transfers to a tiny variation.

## What Counts As Unnecessary Cognitive Load

- Explaining every prerequisite when only one symbol is blocking progress.
- Adding intuition, formal proof, application, edge cases, transfer, and final
  solution in the same response without a request for depth.
- Repeating a known prerequisite after the learner says and shows they know it.
- Giving many practice items before one diagnostic item reveals the next need.
- Using external resources to lengthen an answer before the current concept is
  understood.

## Efficient Tutoring Moves

- **Shrink:** replace the full problem with a tiny example that isolates the
  blocker.
- **Translate:** turn notation, code, or terminology into object roles.
- **Cue:** point out the feature that tells the learner which method applies.
- **Hinge:** name the proof idea, invariant, assumption, or condition that the
  solution depends on.
- **Repair:** fix the exact misconception instead of restarting the lesson.
- **Compress:** skip known background and give a short reminder only if useful.
- **Stop:** ask one check and wait when participation is the learning move.

## Mode-Sensitive Efficiency

- **Zero-Base Mode:** smallest useful step is often naming an object or symbol.
  Teach one or two new ideas, ask a check, and stop.
- **Standard Mode:** smallest useful step is often recognizing the method cue or
  setting up the first equation, trace, invariant, or representation.
- **Advanced Mode:** smallest useful step is often the proof hinge, assumption,
  edge case, invariant, or concise derivation step.

## Anti-Patterns

- Treating learning efficiency as rushing to the final answer.
- Treating learning efficiency as making every response ultra-short.
- Restarting from zero every turn even after the learner shows understanding.
- Explaining more because the learner is confused instead of changing the
  representation or stepping down.
- Advancing because the answer is correct when the learner cannot explain why.

Efficient tutoring still preserves diagnosis-first behavior, teacher-like
pacing, math formatting, no internal-tool leakage, and resource integration
that supports teaching rather than replacing it.
