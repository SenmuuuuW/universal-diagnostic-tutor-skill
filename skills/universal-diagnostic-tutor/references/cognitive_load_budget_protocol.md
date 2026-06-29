# Cognitive Load Budget Protocol

Use this protocol to keep tutoring responses productive rather than heavy. Each
response has a cognitive load budget: a limited amount of new terminology,
notation, reasoning, examples, and tasks the learner can process at once.

The tutor should spend that budget on the next best teaching step, not on a
complete lecture.

## Core Rule

Prefer a small complete step over a large incomplete lecture.

Do not include intuition, application, transfer, proof, and full solution all
in the same response unless the learner explicitly asks for that depth.

## Zero-Base Mode Budget

Use when the learner is new, confused by notation, or missing foundations.

- Introduce at most one or two new concepts per response.
- Use one simple example or one plain-language translation.
- Ask one check.
- Stop after the check when participation is intended.

Good budget use:

- Explain \(K_n\) and \(\chi'(G)\), then ask whether the problem colors points
  or edges.
- Explain what \(A\), \(x\), and \(b\) are in \(Ax=b\), then ask which object is
  unknown.

Bad budget use:

- Define graph, complete graph, coloring, edge chromatic number, theorem,
  parity proof, matching, lower bound, and construction in one response.

## Standard Mode Budget

Use when the learner has seen the topic but cannot choose or execute the method.

- Identify the method cue.
- Do one setup step.
- Ask one check.
- Stop before the full solution unless the learner requested the full answer.

Good budget use:

- For \(1/[n(n+1)]\), point out the adjacent-factor cue, set up partial
  fractions, and ask what numerator equality must hold.

Bad budget use:

- List every convergence test, solve the decomposition, prove convergence, add
  examples, and give a full practice set all at once.

## Advanced Mode Budget

Use when the learner has the basics and asks for rigor, proof, edge cases,
efficiency, or concise explanation.

- Skip obvious basics.
- Focus on the proof hinge, derivation, assumptions, invariant, edge case, or
  transfer boundary.
- Keep rigor concise.

Good budget use:

- For binary search correctness, state the invariant, preservation, and
  termination; ask one hinge check if useful.

Bad budget use:

- Re-explain arrays, loops, and comparison operators to a learner who already
  knows the code.

## Budget Signals

Decrease load when the learner:

- Says they are lost or overwhelmed.
- Confuses symbols or object types.
- Gives a wrong answer that reveals a prerequisite gap.
- Repeats the same mistake.

Increase or compress when the learner:

- Explains why a step works.
- Solves independently.
- Asks for rigor or speed.
- Correctly transfers the idea to a new case.

## Anti-Patterns

- Using many headings and labels when one natural explanation would do.
- Adding sources, applications, and practice before the core blocker is clear.
- Treating every learner as zero-base.
- Treating every advanced learner as needing a full formal proof.
- Continuing after a stop-point check because more content was prepared.
