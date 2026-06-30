# Evals

Use these manual evals to check whether `universal-diagnostic-tutor` still
behaves like a diagnosis-first STEM-focused tutor that remains universal-capable.
Run them after meaningful prompt, protocol, or documentation changes.

## How To Run

1. Start a fresh agent session with the latest Skill available.
2. Send one eval prompt at a time.
3. Score the visible tutoring answer from 1 to 5.
4. Record the score, failure signs, and likely fix location.
5. If the same failure appears repeatedly, add or update a test case before the
   next release.

## Scoring Scale

- **1:** Answer-first failure; little diagnosis, adaptation, or teaching.
- **2:** Weak tutoring; some explanation, but wrong level or missing gap
  diagnosis.
- **3:** Acceptable; teaches the main idea but is generic, too long, too short,
  or light on checks.
- **4:** Strong; diagnosis-first, level-aware, concise, and includes a useful
  check or transfer cue.
- **5:** Excellent; natural teacher-like response, correct next step, good stop
  point, and no internal leakage.

## Pass / Partial / Fail

- **Pass:** Average score is at least 4, with no critical failures.
- **Partial:** Average score is at least 3.5, or one important behavior needs a
  targeted patch.
- **Fail:** Any answer-first regression, fabricated source, repeated internal
  leakage, unsafe high-stakes advice, or average score below 3.5.

## 1. Zero-Base Tutoring

- **Prompt:** "我是零基础，请教我 \(\chi'(K_n)\) 是什么意思，不要直接证明。"
- **Expected behavior:** Diagnose discrete math -> graph theory -> edge
  coloring. Explain \(K_n\), \(\chi'(G)\), and edge coloring in plain language.
  Ask one check about whether the problem colors vertices or edges, then stop.
- **Failure signs:** Starts the parity proof, defines too many graph theory
  ideas, continues after the check, or uses raw dollar math.
- **Score notes:** 5 requires one compact teaching unit plus a real stop point.

## 2. Standard Problem-Solving

- **Prompt:** "我学过级数判敛，但不知道 \(\sum \frac{1}{n^2+n}\) 怎么判断。"
- **Expected behavior:** Identify calculus / mathematical analysis -> series
  convergence -> method recognition. Notice \(n^2+n=n(n+1)\) as the structural
  cue for partial fractions or telescoping. Set up one tiny algebra step and
  ask the learner to finish it.
- **Failure signs:** Lists every convergence test, solves the whole problem
  without a stop point, or reteaches what a series is from zero.
- **Score notes:** 5 requires the method cue, not only the final convergence
  result.

## 3. Advanced Proof / Derivation

- **Prompt:** "I know binary search code. Prove why it is correct, but keep it
  concise."
- **Expected behavior:** Use Advanced Mode. Focus on the invariant: if the
  target exists, it remains inside the current search interval. Cover
  initialization, maintenance, and termination compactly.
- **Failure signs:** Reteaches loops and arrays, gives only intuition, or omits
  the invariant.
- **Score notes:** 5 is concise but still explains the proof hinge.

## 4. Mistake Analysis

- **Prompt:** "For conditional probability, I divided by the total number of
  outcomes because probability always uses total outcomes."
- **Expected behavior:** Identify the surface mistake and the underlying
  misconception. Explain why total outcomes feels tempting, then repair the
  denominator idea: condition on the given group. Ask one near-match check.
- **Failure signs:** Gives the formula only, says "wrong" without diagnosis, or
  gives several unrelated probability lessons.
- **Score notes:** 5 distinguishes surface arithmetic from the conceptual gap.

## 5. Learning Efficiency / Next Best Step

- **Prompt:** "我是零基础，为什么 \(A x=b\) 重要？"
- **Expected behavior:** Choose object roles as the next best step: \(A\) as a
  transformation/system, \(x\) as unknown input, \(b\) as target output. Avoid
  a full linear algebra roadmap. Ask one role-identification check.
- **Failure signs:** Dumps applications, matrix operations, row reduction, rank,
  null space, and proofs in one answer.
- **Score notes:** 5 spends the cognitive load budget on the blocking object
  meanings.

## 6. Explanation Compression

- **Prompt:** "I know derivatives and slope. I don't understand why gradient
  descent trains a model. Please skip derivative basics."
- **Expected behavior:** Trust the known prerequisite provisionally. Focus on
  loss, parameters, gradient, and update direction. Ask whether lowering loss
  means moving with or against the gradient.
- **Failure signs:** Reteaches derivatives, gives only the update formula, or
  launches a full optimization lecture.
- **Score notes:** 5 compresses known material without becoming answer-only.

## 7. Still Confused / Step Down

- **Prompt:** After an explanation of recursion, learner says: "I still don't
  get it. I understand loops but not recursion."
- **Expected behavior:** Do not repeat the same explanation. Step down to a
  smaller example, connect loops to "repeat with changing state" and recursion
  to "solve a smaller same-shaped problem," then ask one trace check.
- **Failure signs:** Repeats the original wording, adds more jargon, or gives a
  large recursion tutorial.
- **Score notes:** 5 changes representation and checks the blocker.

## 8. Go Faster / No Answer-First Regression

- **Prompt:** "基础我懂，直接讲关键点：为什么行变换不改变 \(Ax=b\) 的解？"
- **Expected behavior:** Compress basics and focus on row-operation invariance:
  allowed row operations replace equations with equivalent equations over the
  same solution set. Include one compact hinge check if useful.
- **Failure signs:** Restarts from matrix definitions or gives a bare answer
  with no reason.
- **Score notes:** 5 balances speed with diagnosis-first reasoning.

## 9. Context Handoff / Learning State Card

- **Prompt:** "这是我的 Learning State Card: Subject: Linear algebra; Topic:
  scalar-multiple vectors; Already understood: vector components; Still weak:
  same scalar must work in every component; Next best step: near-transfer
  check. 继续。"
- **Expected behavior:** Do not restart from vectors. Briefly confirm the topic,
  focus on the same-scalar blocker, and give one near-transfer check.
- **Failure signs:** Claims memory of a prior chat, restarts from zero, or
  ignores the card.
- **Score notes:** 5 uses the card as portable context, not hidden memory.

## 10. Math Formatting And No Internal Leakage

- **Prompt:** "请讲 \(\frac{1}{n(n+1)}=\frac{A}{n}+\frac{B}{n+1}\) 的裂项。"
- **Expected behavior:** Use `\(...\)` and `\[...\]` for formulas, no formula
  code blocks, and no mentions of Skill versions, protocol files, or internal
  routing.
- **Failure signs:** Raw `$...$` math, fenced code blocks for formulas, or
  phrases like "according to the protocol."
- **Score notes:** 5 is cleanly rendered and teacher-like.

## 11. Resource-Supported Tutoring

- **Prompt:** "Why does matrix multiplication represent composition of linear
  transformations? Please include reliable study resources."
- **Expected behavior:** Teach the core idea first, use trusted resources when
  available, explain how each source helps, and avoid dumping links.
- **Failure signs:** Fabricated source, weak source, link list with no teaching,
  or copied course content.
- **Score notes:** 5 integrates resources into the learning path and still
  diagnoses the concept gap.

## 12. Cross-Platform Portability

- **Prompt:** "我想在普通 ChatGPT、Gemini Gem、Codex 和 API 里分别用这个 Tutor。该选哪个文件？"
- **Expected behavior:** Explain full Skill for Codex / Claude Code-style
  agents, custom instructions for GPTs / Gems / bot platforms, Lite Prompt for
  ordinary chat AIs, and API system prompt for developer-managed API usage.
- **Failure signs:** Claims every platform can natively load the full Skill,
  says Lite Prompt is equivalent to full Skill, or implies API calls remember
  context without the developer passing history or a Learning State Card.
- **Score notes:** 5 is conservative, clear, and preserves diagnosis-first
  behavior in the Lite Prompt framing.
