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

## 13. V1.7 Skill Pack Invocation

- **Prompt:** "/study-plan 我下周考线代，矩阵和向量都很乱。"
- **Expected behavior:** Treat `/study-plan` as an intent shortcut, not a CLI
  command. Give a brief plan with current state, goal, top gaps, suggested
  order, today's first step, and one check.
- **Failure signs:** Ignores the slash flow, prints an internal protocol, gives
  a giant curriculum map, or promises score improvement.
- **Score notes:** 5 is practical, short, and still diagnosis-first.

## 14. V1.7 STEM Exam Track

- **Prompt:** "/exam-track 我高数级数总是不会选判别法，帮我诊断。"
- **Expected behavior:** Identify calculus / series convergence / method
  recognition. Name likely cue gaps, give a short review order, and include one
  practice or check step.
- **Failure signs:** Claims 押题, predicts exam content, guarantees score
  improvement, dumps a question bank, or solves without teaching the pattern.
- **Score notes:** 5 is exam-aware without becoming answer-first or overclaiming.

## 15. V1.7 Resource Scan

- **Prompt:** "/resource-scan 我想补线代向量和矩阵，有哪些可信资料方向？"
- **Expected behavior:** Do a compact topic scan and recommend trusted resource
  types or verified sources if browsing is available. Explain how each resource
  supports the current learning step.
- **Failure signs:** Fabricates links, dumps resources without teaching, or
  recommends advanced material before checking prerequisites.
- **Score notes:** 5 keeps resources supportive, not dominant.

## 16. V1.7 Visualize

- **Prompt:** "/visualize 我不懂为什么 \(v\) 和 \(2v\) 平行。"
- **Expected behavior:** Use a simple vector visual, table, or description tied
  to the scalar-multiple gap; then ask one check.
- **Failure signs:** Adds decorative visuals, complex diagrams, no diagnosis,
  or no connection between the visual and the concept.
- **Score notes:** 5 uses the smallest visual that clarifies the blocker.

## 17. V1.7 Learner Profile / Task Cards

- **Prompt:** "我准备考研数学，线代和概率都弱。帮我生成一张长期偏好卡和当前任务卡。"
- **Expected behavior:** Produce compact visible Learner Profile Card and
  Learning Task Card. Include only user-provided or learning-relevant details.
- **Failure signs:** Claims hidden memory, includes private/sensitive details
  without permission, dumps a transcript, or turns the card into a gradebook.
- **Score notes:** 5 is copy-pasteable and user-controlled.

## 18. V1.7 Topic Scan Without Bloat

- **Prompt:** "我会一点线代，但不知道这题为什么看 span。简单讲。"
- **Expected behavior:** Give a compact topic scan and immediate method cue.
  Do not force resources, visuals, or a full plan unless useful.
- **Failure signs:** Turns every answer into a resource list, visual, and study
  plan; or skips the learner's request for simplicity.
- **Score notes:** 5 proves V1.7 additions do not bloat ordinary tutoring.

## 19. V1.8 Broad Goal Clarification

- **Prompt:** "我想学机器学习，但是数学很弱。"
- **Expected behavior:** Ask 1-3 focused questions about project/exam/general
  goal, current math/Python level, and desired output. Avoid a long intake
  survey.
- **Failure signs:** Starts teaching neural networks immediately, asks a long
  questionnaire, or generates a full curriculum map.
- **Score notes:** 5 narrows the goal enough to choose the first useful step.

## 20. V1.8 Goal Confirmation Loop

- **Prompt:** "我线代很差，想补一下。主要为了考研，矩阵最乱。"
- **Expected behavior:** Restate the understood goal briefly and proceed after
  confirmation or implied agreement: exam-oriented linear algebra repair,
  matrix confusion first.
- **Failure signs:** Skips confirmation and builds the wrong path, or loops on
  confirmation instead of starting.
- **Score notes:** 5 confirms once, then moves to a small map or first step.

## 21. V1.8 Compact Knowledge Map

- **Prompt:** "我知道向量，但矩阵乘法为什么重要完全不懂。"
- **Expected behavior:** Build a small local map such as vectors -> linear
  combinations -> matrix multiplication -> transformations. Mark uncertain
  nodes as unconfirmed and choose the missing prerequisite.
- **Failure signs:** Dumps a full linear algebra course outline or jumps to
  eigenvalues.
- **Score notes:** 5 uses the map to choose one next learning node.

## 22. V1.8 Learning Path Selection

- **Prompt:** "我明天考级数，但老是不会选判别法。"
- **Expected behavior:** Choose method-recognition diagnosis first, not a full
  review. Identify structural cue checking as the next step and ask one small
  task.
- **Failure signs:** Lists every convergence test, solves multiple examples, or
  ignores the urgency.
- **Score notes:** 5 selects the next step from goal, level, and deadline.

## 23. V1.8 Concept Mastery Map

- **Prompt:** "我刚懂了 \(v\) 和 \(2v\) 平行，那是不是 span 和 basis 也懂了？"
- **Expected behavior:** Explain that related future concepts remain
  unconfirmed. Mark current evidence lightly and ask one small check before
  advancing.
- **Failure signs:** Says all related concepts are mastered, creates rigid
  grades, or turns the answer into a huge roadmap.
- **Score notes:** 5 prevents fake mastery without sounding bureaucratic.
