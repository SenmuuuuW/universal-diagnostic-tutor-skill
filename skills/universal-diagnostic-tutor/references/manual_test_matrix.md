# Manual Test Matrix

Use this matrix after meaningful updates to check whether the skill still acts
like a universal, diagnosis-first tutor. Score each answer with the 1-5 rubric
in `evaluation_checklist.md`; target 4 or 5 unless a prompt intentionally tests
a failure mode.

## 1. Math

- **Prompt:** "Why do we divide by the coefficient when solving
  `3x + 5 = 20`?"
- **Expected routing:** Math; linear equations and inverse operations.
- **Expected depth:** Level 4.
- **Must include:** Identify isolating `x`, explain `3x` as three equal groups,
  then solve.
- **Failure:** Gives steps only: subtract 5, divide by 3, with no reason.
- **Target score:** 5.

## 2. Natural Science

- **Prompt:** "Why do antibiotics not work on viruses?"
- **Expected routing:** Biology; bacteria vs viruses; medicine education
  boundary.
- **Expected depth:** Level 3.
- **Must include:** Explain bacteria are living cells, viruses use host cells,
  and antibiotics target bacterial structures.
- **Failure:** Suggests treatment decisions or says only "viruses are
  different."
- **Target score:** 5.

## 3. History/Humanities

- **Prompt:** "Was the French Revolution caused by bad kings?"
- **Expected routing:** History; causation and structural factors.
- **Expected depth:** Level 4.
- **Must include:** Separate individual decisions, structural causes, and
  triggers.
- **Failure:** Reduces answer to one person or one cause.
- **Target score:** 4.

## 4. Literature

- **Prompt:** "How do I know if a poem line is literal or symbolic?"
- **Expected routing:** Literature; interpretation and textual evidence.
- **Expected depth:** Level 3.
- **Must include:** Start with literal sense, then repeated images, tone,
  context, and ambiguity.
- **Failure:** Claims one fixed meaning without evidence.
- **Target score:** 4.

## 5. Writing Revision

- **Prompt:** "Make this thesis stronger: `Social media is bad for teens.`"
- **Expected routing:** Writing; thesis specificity and arguability.
- **Expected depth:** Level 3.
- **Must include:** Diagnose broad claim, revise with scope/reason/stakes, and
  explain why the revision is stronger.
- **Failure:** Only rewrites the sentence without teaching the revision move.
- **Target score:** 5.

## 6. Coding/Debugging

- **Prompt:** "My loop prints values but my result list is empty. What am I
  missing?"
- **Expected routing:** Coding; printing vs appending/state.
- **Expected depth:** Level 3.
- **Must include:** Explain output vs stored data, check `append`, and check
  list initialization location.
- **Failure:** Gives code fix without explaining why the list stays empty.
- **Target score:** 5.

## 7. AI Concept

- **Prompt:** "What are embeddings and why do they matter?"
- **Expected routing:** AI concept; vector representations and similarity.
- **Expected depth:** Level 4.
- **Must include:** Explain representation as numbers, similarity, and uses
  such as search or retrieval.
- **Failure:** Uses jargon like "latent vector space" without intuition.
- **Target score:** 5.

## 8. Law/Civics

- **Prompt:** "What is the difference between a law, regulation, and court
  ruling?"
- **Expected routing:** Law/civics; institutions and authority.
- **Expected depth:** Level 4.
- **Must include:** Explain legislature, agency, and court roles; stay
  educational and jurisdiction-aware.
- **Failure:** Gives personalized legal advice or skips institutional structure.
- **Target score:** 5.

## 9. Economics/Business

- **Prompt:** "Why can a profitable company run out of cash?"
- **Expected routing:** Business; profit vs cash flow.
- **Expected depth:** Level 4.
- **Must include:** Explain timing, receivables, inventory, obligations, and the
  measurement difference.
- **Failure:** Says "cash flow" without teaching the mechanism.
- **Target score:** 5.

## 10. Health/Medical Boundary

- **Prompt:** "Should I take antibiotics for a cold?"
- **Expected routing:** Health education; viruses, antibiotics, care boundary.
- **Expected depth:** Level 2 or 3.
- **Must include:** Explain colds are usually viral, antibiotics target
  bacteria, and real decisions belong with a clinician.
- **Failure:** Gives personal medical instruction or dosage guidance.
- **Target score:** 5.

## 11. Finance Boundary

- **Prompt:** "Should I buy stocks because rates are going down?"
- **Expected routing:** Finance education; rates, valuation, uncertainty,
  advice boundary.
- **Expected depth:** Level 3.
- **Must include:** Explain possible mechanisms and risks; avoid personalized
  investment advice.
- **Failure:** Recommends buying or names an investment.
- **Target score:** 5.

## 12. Mixed-Subject Reasoning

- **Prompt:** "How does linear algebra connect to machine learning? I know
  vectors but not matrices."
- **Expected routing:** Math plus AI; matrices as transformations/features.
- **Expected depth:** Level 4.
- **Must include:** Bridge known vectors to matrices, transformations, data,
  and model layers.
- **Failure:** Teaches only abstract matrix algebra or only AI buzzwords.
- **Target score:** 5.

## 13. Resource-Augmented Calculus / Linear Algebra

- **Prompt:** "Why does matrix multiplication represent composition of
  transformations? Please include study resources."
- **Expected source behavior:** Use or request reliable linear algebra sources,
  preferably university notes, open courseware, or open textbooks. Cite or list
  sources if external search is available.
- **Expected diagnosis behavior:** Identify the gap between matrix formulas and
  linear maps/composition.
- **Expected teaching behavior:** Explain `A(Bx) = (AB)x`, basis-vector meaning,
  order of operations, and a practice direction.
- **Failure:** Gives only the multiplication formula, invents textbook links, or
  dumps source summaries without teaching.
- **Target score:** 5.

## 14. Resource-Augmented Data Structures

- **Prompt:** "How should I study stacks, queues, and trees for problem sets?"
- **Expected source behavior:** Prefer official problem sets, past exams,
  open courseware, or reputable data structures notes.
- **Expected diagnosis behavior:** Identify pattern-recognition and invariant
  gaps, not just definition gaps.
- **Expected teaching behavior:** Group practice by operations, invariants,
  complexity, traversal, recursion, and trap cases.
- **Failure:** Lists definitions or solved answers without study patterns.
- **Target score:** 5.

## 15. Resource-Augmented Operating Systems

- **Prompt:** "Why do operating systems need virtual memory? Use sources if you
  can."
- **Expected source behavior:** Prefer OS course notes, open courseware, or
  official architecture references for address translation.
- **Expected diagnosis behavior:** Identify the misconception that virtual
  memory only means "more RAM."
- **Expected teaching behavior:** Teach address spaces, page tables, isolation,
  protection, and paging as system design ideas.
- **Failure:** Mentions only swapping or pretends to cite sources not checked.
- **Target score:** 5.

## 16. Resource-Augmented Machine Learning

- **Prompt:** "How do embeddings connect to linear algebra?"
- **Expected source behavior:** Prefer university ML/NLP notes, reputable
  tutorials, or official embedding documentation when implementation matters.
- **Expected diagnosis behavior:** Identify the missing bridge from vectors to
  learned representations and similarity.
- **Expected teaching behavior:** Explain vectors, geometry, cosine similarity,
  nearest-neighbor search, and later ML connections.
- **Failure:** Uses jargon without intuition or treats embeddings as magic.
- **Target score:** 5.

## 17. Resource-Augmented Physics Or Electronics

- **Prompt:** "Why does filtering a signal in frequency space change the time
  signal?"
- **Expected source behavior:** Prefer signal processing course notes, open
  textbooks, or reputable engineering tutorials.
- **Expected diagnosis behavior:** Identify the gap between time-domain and
  frequency-domain representations.
- **Expected teaching behavior:** Connect signals, decomposition, filters,
  transforms, physical meaning, and engineering use.
- **Failure:** Gives formulas only or ignores the conceptual representation gap.
- **Target score:** 5.

## 18. Source-Limited Answer

- **Prompt:** "I need sources for virtual memory, but the environment cannot
  access the web right now."
- **Expected source behavior:** State that external resources could not be
  verified. Do not invent links or source names.
- **Expected diagnosis behavior:** Identify the topic and source need.
- **Expected teaching behavior:** Give a foundations explanation and a checklist
  of source categories to verify later.
- **Failure:** Pretends to have searched or refuses to help at all.
- **Target score:** 5.

## 19. Exam-Pattern Analysis With Authoritative Sources

- **Prompt:** "Use official or university-style resources to help me recognize
  exam patterns for trees and graph traversal."
- **Expected source behavior:** Prefer official problem sets, past exams,
  open courseware, or instructor notes; reject answer-only sites.
- **Expected diagnosis behavior:** Identify the tested concepts and prerequisite
  gaps: traversal order, invariants, recursion, complexity, and edge cases.
- **Expected teaching behavior:** Extract recurring patterns, traps, recognition
  cues, and next practice priorities.
- **Failure:** Dumps solutions, uses copied answer sites, or ignores source
  reliability.
- **Target score:** 5.

## 20. V0.5 ML Foundation Learning Path Using Source Packs

- **Prompt:** "I'm starting machine learning. What math and CS foundations
  should I review first, and what sources should I use?"
- **Expected source pack behavior:** Use `source_packs/math_foundations.md`,
  `source_packs/programming_and_cs_foundations.md`, and
  `source_packs/ai_ml_data.md`; select a small set such as MIT OCW 6.100L, MIT
  OCW 18.06, MIT OCW 18.05, Google ML Crash Course, and Stanford CS229.
- **Expected diagnosis behavior:** Identify the prerequisite-chain gap across
  programming, linear algebra, calculus/optimization, probability/statistics,
  and ML concepts.
- **Expected teaching behavior:** Turn sources into an ordered learning path
  with practice goals, not a long link list.
- **Failure cases:** Lists sources without diagnosis, recommends advanced ML
  before prerequisites, cites unverified sources as checked, or implies ML is
  the whole skill.
- **Target score:** 5.

## 21. V0.5 Operating Systems Source Selection

- **Prompt:** "Why do operating systems need virtual memory? Give me reliable
  sources to keep studying."
- **Expected source pack behavior:** Use
  `source_packs/systems_networks_security.md` and optionally
  `source_packs/exam_problem_set_sources.md`; prefer OSTEP, MIT 6.S081, or MIT
  OS assignment/lab sources.
- **Expected diagnosis behavior:** Identify the misconception that virtual
  memory only means "more RAM"; diagnose gaps in address spaces, page tables,
  protection, isolation, and paging.
- **Expected teaching behavior:** Explain the concept first, then show which
  sources support foundations versus labs or practice.
- **Failure cases:** Mentions only swapping, dumps OS links, invents source
  names, or skips the protection/isolation purpose.
- **Target score:** 5.

## 22. V0.5 Linear Algebra Source Selection

- **Prompt:** "Matrices confuse me. Which sources should I use to understand
  why matrix multiplication matters?"
- **Expected source pack behavior:** Use `source_packs/math_foundations.md`;
  prefer MIT OCW 18.06 for formal study and 3Blue1Brown as visual intuition.
- **Expected diagnosis behavior:** Identify the gap between computation rules
  and transformations/composition.
- **Expected teaching behavior:** Explain matrix multiplication as composed
  transformations, then recommend source use and practice direction.
- **Failure cases:** Treats a visual tutorial as a complete formal course,
  gives only formula rules, or recommends too many links.
- **Target score:** 5.

## 23. V0.5 Data Structures Exam Prep Source Selection

- **Prompt:** "How should I study stacks, queues, trees, and graphs for problem
  sets and exams?"
- **Expected source pack behavior:** Use
  `source_packs/programming_and_cs_foundations.md` and
  `source_packs/exam_problem_set_sources.md`; prefer MIT 6.006, Princeton
  Algorithms, Princeton COS 226 assignments/exams, or Berkeley CS61B when
  appropriate.
- **Expected diagnosis behavior:** Identify gaps in operations, invariants,
  traversal, recursion, complexity, and choosing the right structure.
- **Expected teaching behavior:** Group practice by patterns and traps, then
  suggest official/university practice sources.
- **Failure cases:** Gives definitions only, dumps solved answers, or uses
  answer-only sites.
- **Target score:** 5.

## 24. V0.5 Physics And Signals Source Selection

- **Prompt:** "How does a real-world signal become something a computer can
  process? What should I study?"
- **Expected source pack behavior:** Use
  `source_packs/physics_electronics_signals.md`; choose sources such as
  OpenStax University Physics, MIT 6.002, MIT 6.003, and MIT 6.341 depending on
  level.
- **Expected diagnosis behavior:** Identify the bridge from physical phenomena
  to circuits, sampling, quantization, digital representation, and processing.
- **Expected teaching behavior:** Build a staged path from physics to
  electronics to signals to DSP, with source roles explained.
- **Failure cases:** Gives formulas only, skips physical intuition, or treats
  DSP as the first step for a beginner.
- **Target score:** 5.

## 25. V0.5 Source Pack Unavailable Or Insufficient

- **Prompt:** "I need sources for a niche VR haptics topic, but your source
  packs do not cover it well and web access is unavailable."
- **Expected source pack behavior:** State that the packs have insufficient
  coverage and that external sources cannot be verified in the current
  environment.
- **Expected diagnosis behavior:** Identify the likely mixed domain: VR, HCI,
  sensors/actuators, signals, perception, and systems.
- **Expected teaching behavior:** Explain from foundations, name source
  categories to verify later, and avoid fake links or invented papers.
- **Failure cases:** Invents papers, pretends to have searched, or refuses to
  teach anything useful from foundations.
- **Target score:** 5.

## 26. V0.6 Beginner Networks Learning Path

- **Prompt:** "I want to learn computer networks from zero. What should I
  study first and which sources should I trust?"
- **Expected source-pack behavior:** Use `source_packs/networks_from_zero.md`
  before advanced networking sources; choose MDN, an open textbook, Wireshark
  labs, then Stanford CS144 or RFCs only when ready.
- **Expected diagnosis behavior:** Identify beginner gaps in layers, clients,
  servers, packets, DNS, HTTP, TCP/IP, routing, and reliability.
- **Expected teaching behavior:** Build a staged path from mental model to
  structured study to practical labs.
- **Failure cases:** Starts with RFCs, dumps advanced courses, or skips
  beginner mental models.
- **Target score:** 5.

## 27. V0.6 Cryptography And Number Theory

- **Prompt:** "Why does modern cryptography need number theory?"
- **Expected source-pack behavior:** Use
  `source_packs/crypto_security_addendum.md`; prefer Stanford CS255 or the
  applied cryptography book for learning, standards only for exact details.
- **Expected diagnosis behavior:** Identify modular arithmetic, primes,
  one-way operations, and easy-vs-hard computation as likely gaps.
- **Expected teaching behavior:** Keep the explanation educational and
  defensive; avoid implementation or exploit instructions.
- **Failure cases:** Says only "RSA uses primes," gives harmful cyber detail,
  or starts with TLS/AES standards before concepts.
- **Target score:** 5.

## 28. V0.6 Formal Languages And Automata

- **Prompt:** "Why do we study automata and formal languages in computer
  science?"
- **Expected source-pack behavior:** Use
  `source_packs/theory_formal_methods.md`; choose Stanford CS103 or MIT 6.042J
  for prerequisite repair and MIT 6.045J or UIUC CS374 for deeper theory.
- **Expected diagnosis behavior:** Identify the vocabulary gap: language as a
  set of strings and automaton as a recognition model.
- **Expected teaching behavior:** Explain motivation, examples, prerequisites,
  and how theory connects to parsers, regexes, protocols, and computability.
- **Failure cases:** Lists courses without explaining the model, or jumps to
  Turing machines before finite automata.
- **Target score:** 5.

## 29. V0.6 Numerical Analysis

- **Prompt:** "Why do computers sometimes get inaccurate answers in numerical
  calculations?"
- **Expected source-pack behavior:** Use
  `source_packs/numerical_hpc_control.md`; prefer MIT 18.335J or UIUC CS357
  before HPC resources.
- **Expected diagnosis behavior:** Identify floating-point representation,
  rounding, cancellation, conditioning, and stability gaps.
- **Expected teaching behavior:** Explain finite precision first, then connect
  to numerical methods and practice.
- **Failure cases:** Says only "floating point is imprecise" or dumps advanced
  numerical links without teaching error behavior.
- **Target score:** 5.

## 30. V0.6 HPC Or Parallel Computing

- **Prompt:** "How is high-performance computing different from just writing
  faster code?"
- **Expected source-pack behavior:** Use
  `source_packs/numerical_hpc_control.md`; choose LLNL HPC Tutorials, OpenMP,
  or MPI depending on shared-memory vs distributed-memory readiness.
- **Expected diagnosis behavior:** Identify gaps in parallelism, memory,
  communication, synchronization, and performance bottlenecks.
- **Expected teaching behavior:** Explain decomposition, coordination, and
  hardware/software tradeoffs before naming tools.
- **Failure cases:** Gives only tool names, skips prerequisites, or treats HPC
  as generic optimization.
- **Target score:** 5.

## 31. V0.6 Control Systems Or Signals/Control Connection

- **Prompt:** "How do signals and control systems connect?"
- **Expected source-pack behavior:** Use
  `source_packs/numerical_hpc_control.md` plus
  `source_packs/physics_electronics_signals.md`; choose MIT 16.30, Stanford
  EE263, or MIT 6.003 based on level.
- **Expected diagnosis behavior:** Identify gaps in systems, feedback,
  stability, transforms, and state-space thinking.
- **Expected teaching behavior:** Explain signals as inputs/outputs and control
  as shaping system behavior with feedback.
- **Failure cases:** Gives formulas only or recommends advanced EE263 before
  prerequisite checks.
- **Target score:** 5.

## 32. V0.6 Source Specificity

- **Prompt:** "Use MIT OCW to help me practice virtual memory."
- **Expected source-pack behavior:** Use
  `source_packs/source_specificity_guidelines.md`; prefer exact OS lecture,
  lab, or assignment pages over a broad MIT OCW homepage.
- **Expected diagnosis behavior:** Identify whether the learner needs concept
  explanation, lab practice, or exam-pattern practice.
- **Expected teaching behavior:** Explain why a specific page or lab is better
  than a generic source list.
- **Failure cases:** Cites only "MIT OCW" or a generic course homepage when a
  lab/assignment page is more useful.
- **Target score:** 5.

## 33. V0.6 Source Refresh Or Stale Source Behavior

- **Prompt:** "This course link looks stale. What should you do before using it
  as a source?"
- **Expected source-pack behavior:** Use
  `source_packs/source_refresh_maintenance.md`; verify, replace, mark stale, or
  omit rather than silently citing.
- **Expected diagnosis behavior:** Identify the source-maintenance task, not a
  subject-learning question.
- **Expected teaching behavior:** Explain link-state labeling and replacement
  preference for official/current pages.
- **Failure cases:** Pretends the link is current, invents a replacement, or
  keeps broken links without caution.
- **Target score:** 5.

## 34. V0.7 "I Still Don't Understand" Follow-Up

- **Prompt:** After an explanation of derivatives as slope, the learner says:
  "I still don't understand. What is the derivative actually doing?"
- **Expected diagnosis behavior:** Identify a concept or mental-model gap around
  what "slope" means in context.
- **Expected adaptive behavior:** Do not repeat the same slope explanation.
  Identify the likely mental-model gap and switch to a smaller example such as
  position changing over time.
- **Expected teaching behavior:** Explain derivative as instant rate of change,
  contrast average vs instant change, and ask one tiny check question.
- **Failure cases:** Restarts a full calculus lecture, gives only the formal
  limit definition, or says "it is just slope" again.
- **Target score:** 5.

## 35. V0.7 Mistake Analysis

- **Prompt:** "I solved `2(x - 3) = 10` as `2x - 3 = 10`, so `x = 6.5`.
  What did I do wrong?"
- **Expected diagnosis behavior:** Identify a procedure and misconception gap
  around distributing across a parenthesized group.
- **Expected adaptive behavior:** Locate the exact distribution mistake and
  explain why it is tempting.
- **Expected teaching behavior:** Show that `2` multiplies both `x` and `-3`,
  correct the work, and give one near-match practice item.
- **Failure cases:** Only gives the correct answer or says "distribute
  properly" without teaching the underlying operation.
- **Target score:** 5.

## 36. V0.7 Wrong Answer Response

- **Prompt:** After being asked "What is the base case for factorial?" the
  learner answers: "The base case is `n * factorial(n - 1)`."
- **Expected diagnosis behavior:** Identify that the learner gave the recursive
  case instead of the stopping condition; classify this as a procedure and
  concept gap.
- **Expected adaptive behavior:** Preserve the useful part, separate recursive
  case from base case, and ask for the stopping value.
- **Expected teaching behavior:** Explain that the base case prevents infinite
  recursion and usually returns a direct value such as `1` for `0!` or `1!`.
- **Failure cases:** Says only "wrong" or gives full code without repairing the
  base-case distinction.
- **Target score:** 5.

## 37. V0.7 Explain Simpler

- **Prompt:** "Explain matrix eigenvectors simpler. I got lost."
- **Expected diagnosis behavior:** Identify abstraction overload and likely
  notation or concept gap.
- **Expected adaptive behavior:** Step down one level, avoid heavy notation,
  use a visual or physical analogy, and ask one recognition check.
- **Expected teaching behavior:** Explain that an eigenvector keeps its
  direction under a transformation, while its length may scale.
- **Failure cases:** Starts with `Av = lambda v` without plain-language meaning,
  or repeats the same formal explanation.
- **Target score:** 5.

## 38. V0.7 Deeper Explanation Request

- **Prompt:** "I get that supply shifts affect price, but why does the graph
  model work at all? Give me the deeper reasoning."
- **Expected diagnosis behavior:** Identify a reasoning gap about model purpose,
  assumptions, and equilibrium logic.
- **Expected adaptive behavior:** Increase depth by explaining mechanism and
  assumptions, not by adding unrelated facts.
- **Expected teaching behavior:** Explain buyers, sellers, incentives,
  equilibrium, ceteris paribus assumptions, and limits of the model.
- **Failure cases:** Repeats only "supply left means price up" or gives a long
  economics lecture without answering why the model works.
- **Target score:** 5.

## 39. V0.7 Practice Ladder

- **Prompt:** "I understand recursion when you explain it, but I freeze when I
  need to write a recursive function. Give me practice."
- **Expected diagnosis behavior:** Identify procedure and transfer gaps around
  base case, smaller input, and recursive case.
- **Expected adaptive behavior:** Use a ladder rather than random exercises.
- **Expected teaching behavior:** Include recognition, concept check, worked
  completion, near-transfer, trap/misconception, mixed-topic, and project-style
  rungs.
- **Failure cases:** Dumps many recursion problems or reteaches only the
  definition.
- **Target score:** 5.

## 40. V0.7 Mistake Analysis With Misconception Repair

- **Prompt:** "A medical test is 99% accurate, so I said a positive result
  means 99% chance of disease. What did I do wrong?"
- **Expected diagnosis behavior:** Identify a conditional-probability and
  base-rate misconception, not just a calculation error.
- **Expected adaptive behavior:** Explain why the wrong path felt tempting and
  use a concrete-count example before formulas.
- **Expected teaching behavior:** Separate sensitivity/false positives from
  probability given a positive test, then give a near-match practice item.
- **Failure cases:** Says only "use Bayes' theorem" or gives a formula without
  repairing the intuition.
- **Target score:** 5.

## 41. V0.7 STEM Intuition-To-Formal Sequence

- **Prompt:** "Why does gradient descent move in the negative gradient
  direction? I know derivatives but not multivariable optimization."
- **Expected diagnosis behavior:** Identify a prerequisite bridge from
  single-variable derivatives to multivariable direction of steepest change.
- **Expected adaptive behavior:** Bridge from single-variable slope to
  multivariable steepest increase before formal notation.
- **Expected teaching behavior:** Start with terrain intuition, define gradient
  as direction of steepest increase, explain why negative gradient decreases
  fastest locally, then show the update rule and a tiny check.
- **Failure cases:** Starts with formulas only, assumes linear algebra mastery,
  or skips the intuition-to-formal bridge.
- **Target score:** 5.

## 42. V0.7 Transfer To Similar Problems

- **Prompt:** "I can solve `3x + 5 = 20`, but word problems with the same idea
  confuse me. How do I recognize them?"
- **Expected diagnosis behavior:** Identify a recognition and transfer gap, not
  an algebra-procedure gap.
- **Expected adaptive behavior:** Extract the underlying equation structure and
  compare symbolic and word-problem versions.
- **Expected teaching behavior:** Teach cues such as total, fixed amount,
  repeated amount, unknown quantity, and give a near-transfer word problem.
- **Failure cases:** Solves one word problem without teaching recognition cues.
- **Target score:** 5.

## 43. V0.7 Universal Mastery Beyond STEM

- **Prompt:** "I can identify metaphors in poems when someone points them out,
  but I miss them on my own. How do I practice?"
- **Expected diagnosis behavior:** Identify a recognition and transfer gap in a
  literature task.
- **Expected adaptive behavior:** Diagnose a recognition and transfer gap in a
  literature task.
- **Expected teaching behavior:** Build a non-STEM practice ladder: literal
  meaning, odd word choice, repeated image, evidence check, contrast with
  non-metaphor, and a short teach-back.
- **Failure cases:** Treats the skill as STEM-only or gives a generic "read
  more poems" answer.
- **Target score:** 5.

## 44. V0.8 Matrix Notation Confusion

- **Prompt:** "I keep seeing `Ax = b`. What are `A`, `x`, and `b` actually
  supposed to mean?"
- **Expected diagnosis behavior:** Identify notation and concept gaps around
  object types and matrix equation roles.
- **Expected ask-vs-explain choice:** Explain first; the learner lacks the
  notation foundation needed for a useful guiding question.
- **Expected adaptive tutor behavior:** Translate each symbol, identify matrix
  and vector object types, explain what the equation means, and use a tiny
  numerical example.
- **Expected check/practice behavior:** Ask which object is unknown or what `A`
  does to `x`.
- **Failure cases:** Starts row reduction, treats all symbols as scalars, or
  gives only formal notation.
- **Target score:** 5.

## 45. V0.8 Derivative Derivation

- **Prompt:** "Why is the derivative of `x^2` equal to `2x`?"
- **Expected diagnosis behavior:** Identify a reasoning gap around why the
  power rule works.
- **Expected ask-vs-explain choice:** Explain first because the user asks for a
  derivation.
- **Expected adaptive tutor behavior:** State the derivation goal, use the
  derivative definition, explain expansion/cancellation, and interpret `2x` as
  rate of change.
- **Expected check/practice behavior:** Ask why `h` can be canceled before the
  limit or ask for the next step in a similar derivation.
- **Failure cases:** Cites the power rule only, gives equation steps without
  reasons, or skips the meaning after the derivation.
- **Target score:** 5.

## 46. V0.8 Binary Search Correctness Proof

- **Prompt:** "Why is binary search correct? I know the code, but not the
  proof."
- **Expected diagnosis behavior:** Identify a reasoning gap around invariants
  and sorted-order assumptions.
- **Expected ask-vs-explain choice:** Explain first by naming the invariant;
  then ask a proof check.
- **Expected adaptive tutor behavior:** State the invariant, explain why each
  discard step preserves it, mention termination, and connect correctness to
  sorted order.
- **Expected check/practice behavior:** Ask which assumption allows discarding
  half the array.
- **Failure cases:** Restates code, skips invariant, or asserts correctness
  without proof reasoning.
- **Target score:** 5.

## 47. V0.8 Python Loop/List Debugging

- **Prompt:** "My Python loop prints values but my result list is empty. What
  am I missing?"
- **Expected diagnosis behavior:** Identify a state/data-flow gap between
  printing and storing, and check list initialization location.
- **Expected ask-vs-explain choice:** Ask one guiding question if code is
  visible; otherwise explain likely causes directly.
- **Expected adaptive tutor behavior:** Use observe, hypothesize, isolate,
  test, fix, explain; teach why `print` does not mutate a list.
- **Expected check/practice behavior:** Ask where `result = []` should be or
  where `append` occurs.
- **Failure cases:** Gives only a patched snippet, ignores state, or treats it
  as a syntax-only problem.
- **Target score:** 5.

## 48. V0.8 Virtual Memory Abstraction

- **Prompt:** "Why is virtual memory not just more RAM?"
- **Expected diagnosis behavior:** Identify a systems abstraction-layer
  misconception about virtual vs physical addresses.
- **Expected ask-vs-explain choice:** Explain first; the learner lacks the
  layer distinction.
- **Expected adaptive tutor behavior:** Explain address translation, program
  view vs physical memory, isolation, protection, and paging as secondary.
- **Expected check/practice behavior:** Ask whether two processes using the
  same virtual address must share the same physical address.
- **Failure cases:** Mentions only swapping, starts with page-table details too
  early, or says simply "it extends RAM."
- **Target score:** 5.

## 49. V0.8 Physical Signal To Digital Data

- **Prompt:** "How does a physical signal become digital data?"
- **Expected diagnosis behavior:** Identify a bridge gap from physical
  phenomenon to sensor, analog signal, sampling, quantization, and numbers.
- **Expected ask-vs-explain choice:** Explain first; the learner needs the
  pathway before equations.
- **Expected adaptive tutor behavior:** Start with measurable quantity, then
  sensor voltage, sampling, quantization, digital representation, and limits.
- **Expected check/practice behavior:** Ask whether sampling or quantization
  turns a continuous signal into time-separated measurements.
- **Failure cases:** Dumps ADC jargon, starts with transform formulas, or skips
  physical meaning and units.
- **Target score:** 5.

## 50. V0.8 Gradient Descent Math Bridge

- **Prompt:** "Why does gradient descent need calculus and linear algebra?"
- **Expected diagnosis behavior:** Identify prerequisite bridge gaps across
  loss, parameters, derivatives, gradients, vectors, and matrices.
- **Expected ask-vs-explain choice:** Explain first, then ask a small check.
- **Expected adaptive tutor behavior:** Connect data, model, loss,
  optimization, gradient, and parameter update without starting from formal
  notation.
- **Expected check/practice behavior:** Ask whether the gradient is a single
  number or a vector of directions for many parameters.
- **Failure cases:** Says only "gradients are derivatives," assumes advanced
  linear algebra, or skips the ML objects.
- **Target score:** 5.

## 51. V0.8 When To Ask A STEM Guiding Question

- **Prompt:** "I know derivatives and vectors. For gradient descent, should the
  update move with the gradient or against it?"
- **Expected diagnosis behavior:** Identify that prerequisites are probably
  present and the learner needs a one-step direction check.
- **Expected ask-vs-explain choice:** Ask a guiding question first, such as
  "Which direction increases the loss fastest?"
- **Expected adaptive tutor behavior:** Use the learner's known prerequisites
  to prompt reasoning, then confirm and explain briefly.
- **Expected check/practice behavior:** Ask a tiny vector-direction check.
- **Failure cases:** Gives a full lecture, withholds confirmation too long, or
  asks a question requiring unstated background.
- **Target score:** 5.

## 52. V0.8 When To Explain Directly In STEM

- **Prompt:** "I do not know what the gradient symbol means. Why does gradient
  descent use it?"
- **Expected diagnosis behavior:** Identify a vocabulary/notation prerequisite
  gap.
- **Expected ask-vs-explain choice:** Explain directly before asking questions.
- **Expected adaptive tutor behavior:** Define gradient as a vector of partial
  derivatives, connect it to steepest increase, then explain why the negative
  gradient is used.
- **Expected check/practice behavior:** Ask whether negative gradient points
  uphill or downhill locally.
- **Failure cases:** Starts with a Socratic question, assumes notation mastery,
  or gives only the update formula.
- **Target score:** 5.

## 53. V0.9 Correct Answer But Cannot Explain

- **Prompt:** After being asked for the derivative of `x^3`, the learner says:
  "It is `3x^2`, but I don't know why. I just memorized the rule."
- **Expected mastery-state diagnosis:** Recognition or procedure recall, not
  independent explanation.
- **Expected tutor decision:** Maintain difficulty and review the reasoning
  before advancing.
- **Expected adaptive response:** Confirm the correct answer, explain that the
  reasoning is the part to strengthen, give a compact intuition or derivation
  cue, and avoid harder derivatives for the moment.
- **Expected practice/check behavior:** Use one reasoning check, such as why a
  power function uses the power rule or what the derivative is measuring.
- **Failure cases:** Treats the correct answer as mastery, gives harder
  problems immediately, or says only "memorize the rule."
- **Target score:** 5.

## 54. V0.9 Learner Succeeds With Hints

- **Prompt:** The learner completes a recursive factorial function after two
  hints about the base case and smaller input, then asks: "What should I try
  next?"
- **Expected mastery-state diagnosis:** Guided application; the learner solved
  with support but has not shown independent application.
- **Expected tutor decision:** Move to near-transfer with fewer hints.
- **Expected adaptive response:** Briefly summarize what the learner now has,
  then give a similar recursion task such as summing a list or counting items.
- **Expected practice/check behavior:** Ask for the base case and recursive
  case, with fewer scaffolds than before.
- **Failure cases:** Gives a full project, repeats the same factorial problem,
  or assumes independent mastery.
- **Target score:** 5.

## 55. V0.9 Confused Twice

- **Prompt:** After two explanations of matrix multiplication as rows times
  columns, the learner says: "I still don't understand why this operation means
  composition."
- **Expected mastery-state diagnosis:** Misconception or concept gap with
  repeated confusion; current explanation mode failed.
- **Expected tutor decision:** Re-explain by switching representation, not by
  repeating row-column computation.
- **Expected adaptive response:** Use transformations or basis vectors as the
  new representation, connect `A(Bx)` to `(AB)x`, and keep the example small.
- **Expected practice/check behavior:** Ask which transformation happens first
  in `ABx` or give one tiny composition check.
- **Failure cases:** Gives a longer row-column lecture, dumps formulas, or
  implies the learner should understand by now.
- **Target score:** 5.

## 56. V0.9 Overwhelmed By Notation

- **Prompt:** "This gradient descent formula has too many symbols. I don't
  know what theta or alpha are and now I'm lost."
- **Expected mastery-state diagnosis:** Overloaded with notation and concept
  prerequisites missing.
- **Expected tutor decision:** Decrease difficulty and simplify.
- **Expected adaptive response:** Remove dense notation, explain one adjustable
  parameter and one step size in plain language, then return to symbols only
  after the intuition lands.
- **Expected practice/check behavior:** Ask one confidence or prediction check,
  such as which direction to move if error rises to the right.
- **Failure cases:** Defines all symbols in a dense list, adds sources, or
  continues the full vector formula.
- **Target score:** 5.

## 57. V0.9 Learner Solves Independently

- **Prompt:** The learner solves a near-transfer linear equation without hints
  and explains why each inverse operation preserves equality.
- **Expected mastery-state diagnosis:** Independent application with reasoning
  evidence.
- **Expected tutor decision:** Increase difficulty one step toward transfer or
  a trap case.
- **Expected adaptive response:** Confirm the reasoning, name the reusable
  method, and give a slightly different word problem or trap involving the same
  equation structure.
- **Expected practice/check behavior:** Ask the learner to identify the method
  in the new wording before solving.
- **Failure cases:** Keeps drilling identical equations, declares total mastery,
  or jumps to unrelated advanced algebra.
- **Target score:** 5.

## 58. V0.9 Learner Transfers Method To New Problem

- **Prompt:** After learning recursion with factorial, the learner explains how
  the same base-case/smaller-input idea applies to walking a folder tree.
- **Expected mastery-state diagnosis:** Transfer for the recursion concept.
- **Expected tutor decision:** Mark strong understanding naturally and connect
  to the next useful application or edge case.
- **Expected adaptive response:** Summarize the transfer cue, then offer a
  small edge case such as an empty folder or a folder with nested folders.
- **Expected practice/check behavior:** Ask how the base case changes for the
  edge case.
- **Failure cases:** Reteaches factorial, ignores the transfer, or starts a
  broad data-structures roadmap.
- **Target score:** 5.

## 59. V0.9 Review Vs Advance Decision

- **Prompt:** "I can plug numbers into Bayes' theorem, but I don't know when I
  should use it. Can we do harder problems?"
- **Expected mastery-state diagnosis:** Procedure familiarity with recognition
  gap; not ready for harder mixed problems yet.
- **Expected tutor decision:** Review recognition cues before advancing.
- **Expected adaptive response:** Explain that the next progress step is
  identifying conditional-probability structure, then contrast a Bayes case
  with a non-Bayes case.
- **Expected practice/check behavior:** Use a classify-the-method check before
  solving.
- **Failure cases:** Gives harder Bayes calculations, starts a probability
  curriculum map, or ignores the recognition gap.
- **Target score:** 5.

## 60. V0.9 One-Question Understanding Check

- **Prompt:** After explaining virtual memory address translation, the tutor
  needs to check understanding without making the learner feel tested.
- **Expected mastery-state diagnosis:** Guided understanding after explanation;
  needs one signal before advancing.
- **Expected tutor decision:** Use one supportive understanding check.
- **Expected adaptive response:** Frame the check naturally, such as "Tiny check
  so I know where to aim next," then ask whether two processes using the same
  virtual address must share the same physical RAM.
- **Expected practice/check behavior:** One focused question only; adapt based
  on the answer.
- **Failure cases:** Gives a quiz list, skips the check and advances, or asks a
  question requiring page-table details not yet taught.
- **Target score:** 5.

## 61. V1.1 Multi-Question Image Pacing

- **Prompt:** "This image has two linear algebra questions. Help me, but don't
  just give the answers."
- **Expected diagnosis behavior:** Identify a multi-subproblem linear algebra
  task and likely method-recognition gap.
- **Expected pacing behavior:** Identify both questions, then start with the
  first one rather than solving both.
- **Expected stop/check behavior:** Stop before the key scalar comparison,
  elimination, or method-choice step and ask one focused check.
- **Expected source behavior:** Do not search unless resources would improve
  practice or the user asks for sources.
- **Failure cases:** Solves all visible questions in one long response,
  completes the final answer despite the learner's request, or skips the check.
- **Target score:** 5.

## 62. V1.1 Hints-Only Algebra Stop Point

- **Prompt:** "Solve `2x + y = 7` and `x - y = 2`, but don't give me the final
  answer. I want to understand elimination."
- **Expected diagnosis behavior:** Identify a procedure/reasoning gap around
  elimination.
- **Expected pacing behavior:** Explain the cue that `+y` and `-y` can cancel,
  then pause.
- **Expected stop/check behavior:** Ask whether to add or subtract the
  equations before carrying out the elimination.
- **Expected source behavior:** No source needed.
- **Failure cases:** Gives `x = 3, y = 1`, hides the answer in a hint, or
  teaches elimination as a memorized rule only.
- **Target score:** 5.

## 63. V1.1 Autonomous Resource Discovery

- **Prompt:** "What does `Ax = b` mean? Use good sources if you can."
- **Expected diagnosis behavior:** Identify a notation/object-type gap around
  matrix equations.
- **Expected resource behavior:** If web/search access is available, actively
  search for authoritative university/open textbook resources or exact course
  sections; do not wait for uploaded materials.
- **Expected teaching behavior:** Use sources to support object-role teaching,
  not to dump links; explain `A`, `x`, and `b` directly.
- **Expected stop/check behavior:** Ask which object is unknown before solving.
- **Failure cases:** Does not search despite useful available search, invents
  sources, cites broad homepages only, dumps links, or starts row reduction.
- **Target score:** 5.

## 64. V1.1 Resource-Orchestrated Programming

- **Prompt:** "My Python list stays empty even though the loop prints values.
  Can you use official docs if needed?"
- **Expected diagnosis behavior:** Identify a state/data-flow gap: printing is
  not storing, and list mutation must happen in the right scope.
- **Expected resource behavior:** If search is useful and available, prefer
  official Python documentation for list methods or language behavior.
- **Expected teaching behavior:** Explain the mental model first, then use the
  official source as implementation verification.
- **Expected stop/check behavior:** Ask where `append` happens or where the
  list is initialized.
- **Failure cases:** Gives only patched code, lists docs without teaching,
  fabricates documentation links, or ignores state mutation.
- **Target score:** 5.

## 65. V1.1 Exam Pattern Conditional Probability

- **Prompt:** "I keep dividing by the total outcomes in conditional
  probability. How is this tested?"
- **Expected diagnosis behavior:** Identify a repeated misconception and
  recognition gap around the conditioned sample space.
- **Expected exam-pattern behavior:** Name common cues such as "given,"
  "among," or "if we know"; identify the denominator trap and why it feels
  tempting.
- **Expected resource behavior:** If search is available and useful, prefer
  reputable public problem sets, open textbook exercises, or sample exams.
- **Expected practice/check behavior:** Give one near-match denominator check
  or short practice rung.
- **Failure cases:** Gives only Bayes' formula, dumps problem links, copies
  solutions, or skips the misconception repair.
- **Target score:** 5.

## 66. V1.1 Generic AI Contrast

- **Prompt:** "Show me why your tutoring style is different from just asking a
  generic AI to solve this derivative problem."
- **Expected diagnosis behavior:** Identify that the request is about tutoring
  behavior and method understanding, not only the derivative answer.
- **Expected pacing behavior:** Contrast a too-fast answer with a
  diagnosis-first answer that stops at a meaningful step.
- **Expected teaching behavior:** Emphasize prerequisite diagnosis, intuition,
  stop points, checks, and transfer.
- **Expected source behavior:** Search only if the learner asks for external
  resources or practice; otherwise no source needed.
- **Failure cases:** Self-promotional claims without a concrete teaching
  contrast, or a generic full solution with no pacing.
- **Target score:** 5.

## 67. V1.2 Zero-Base Vector Foundation

- **Prompt:** "我是零基础。vector = endpoint - start point 是什么意思？"
- **Expected mode behavior:** Select Zero-Base Mode from explicit learner
  wording.
- **Expected diagnosis behavior:** Identify vocabulary, notation, and
  object-type gaps around points, vectors, and displacement.
- **Expected teaching behavior:** Explain point vs vector before calculation,
  use a real-world movement or visual analogy, and avoid formalism overload.
- **Expected pacing/check behavior:** Stop before calculation and ask whether a
  vector means location or movement.
- **Expected formatting behavior:** Use inline/display math, not code blocks.
- **Failure cases:** Starts subtracting coordinates immediately, assumes vector
  knowledge, or formats the formula as code.
- **Target score:** 5.

## 68. V1.2 Standard Series Convergence

- **Prompt:** "I learned series tests, but I cannot tell which one to use for
  $\sum 1/(n(n+1))$."
- **Expected mode behavior:** Select Standard Mode because the learner has
  class exposure but needs method recognition.
- **Expected diagnosis behavior:** Identify recognition gap around telescoping
  or related convergence-test cues.
- **Expected teaching behavior:** Name the cue in $n(n+1)$, set up partial
  fraction or telescoping reasoning, and avoid re-teaching what a series is.
- **Expected pacing/check behavior:** Stop before the key algebraic
  decomposition and ask what numerator equality must hold.
- **Expected formatting behavior:** Use LaTeX math, not code blocks.
- **Failure cases:** Gives a full convergence proof without a stop point,
  reteaches series from zero, or dumps a list of tests without cue diagnosis.
- **Target score:** 5.

## 69. V1.2 Advanced Derivative Proof

- **Prompt:** "I know the power rule. Give me a concise rigorous proof that the
  derivative of $x^2$ is $2x$."
- **Expected mode behavior:** Select Advanced Mode.
- **Expected diagnosis behavior:** Identify a reasoning/proof gap, not a
  zero-base derivative gap.
- **Expected teaching behavior:** Use the limit definition efficiently, justify
  the $h \neq 0$ simplification, state the assumption, and interpret the
  result.
- **Expected pacing/check behavior:** May include one concise proof-hinge check
  but should not slow down unnecessarily.
- **Expected formatting behavior:** Use aligned display math, not a code block.
- **Failure cases:** Re-explains slope from scratch, gives only the power rule,
  or renders the derivation as monospaced code.
- **Target score:** 5.

## 70. V1.2 Mode Switching For Notation Gap

- **Prompt:** "Use normal mode for $Ax=b$, but I don't understand what $b$ is.
  Is it a point?"
- **Expected mode behavior:** Start Standard, then step down briefly to
  Zero-Base explanation for the notation blocker.
- **Expected diagnosis behavior:** Identify notation/object-type gap around
  $b$ as output vector.
- **Expected teaching behavior:** Explain $A$, $x$, and $b$ roles without
  solving; then return to the original problem.
- **Expected pacing/check behavior:** Ask which object is unknown before row
  reduction or solving.
- **Expected formatting behavior:** Use math formatting for $Ax=b$.
- **Failure cases:** Stays in standard mode and manipulates symbols, labels the
  learner rigidly, or never returns to the original problem.
- **Target score:** 5.

## 71. V1.2 Concise Advanced Explanation

- **Prompt:** "I understand recursion. Be concise and explain the proof idea
  for why this recursive algorithm is correct."
- **Expected mode behavior:** Select Advanced Mode from declared background and
  concise proof request.
- **Expected diagnosis behavior:** Identify proof/invariant or induction need.
- **Expected teaching behavior:** State invariant or induction structure,
  assumptions, base case, inductive step, termination, and edge case compactly.
- **Expected pacing/check behavior:** Ask one proof-hinge check if useful, but
  do not force beginner scaffolding.
- **Expected formatting behavior:** Use code blocks only if actual code is
  shown.
- **Failure cases:** Explains what recursion is from scratch, gives a generic
  correctness claim, or ignores termination.
- **Target score:** 5.

## 72. V1.2 Math Formatting

- **Prompt:** "Show the derivation of the derivative of $x^2$."
- **Expected mode behavior:** Use Standard or Advanced based on learner wording;
  if unclear, infer from context or ask if rigor level matters.
- **Expected diagnosis behavior:** Identify derivation/proof task.
- **Expected teaching behavior:** Use the derivative definition and explain the
  key simplification.
- **Expected pacing/check behavior:** Stop before cancellation if the learner
  asked to participate; otherwise finish with a concise check.
- **Expected formatting behavior:** Use display or aligned LaTeX math for the
  derivation; do not put formulas in fenced code blocks.
- **Failure cases:** Formats algebra as code, uses ASCII fractions in a code
  fence, or hides the proof inside a monospaced block.
- **Target score:** 5.

## 73. V1.2 Auto Mode Calibration

- **Prompt:** "Can you help me understand this matrix equation?"
- **Expected mode behavior:** Use Auto Mode; infer from available context or
  ask "你希望我按零基础、普通还是进阶方式讲？" if the level would change the
  answer.
- **Expected diagnosis behavior:** Identify likely matrix-equation topic and
  unknown learner level.
- **Expected teaching behavior:** If not asking, start with a compact Standard
  explanation and adapt quickly if notation confusion appears.
- **Expected pacing/check behavior:** Ask one small object-role or method cue
  check.
- **Expected formatting behavior:** Use math formatting for matrix equations.
- **Failure cases:** Assumes advanced knowledge, launches a long zero-base
  lecture without evidence, or never calibrates.
- **Target score:** 5.

## 74. V1.2 Beginner Real-World Analogy

- **Prompt:** "我是初学者，能不能用生活中的例子解释什么是 derivative?"
- **Expected mode behavior:** Select Zero-Base or beginner-friendly mode from
  explicit beginner wording.
- **Expected diagnosis behavior:** Identify vocabulary/concept gap around
  derivative as instant rate of change.
- **Expected teaching behavior:** Use a real-world analogy such as speed at one
  instant before introducing formal notation; explain why the idea matters.
- **Expected pacing/check behavior:** Ask one small check, such as whether the
  speedometer shows a whole-trip average or a moment-by-moment rate.
- **Expected formatting behavior:** Use math formatting only if a formula is
  needed; avoid code blocks for math.
- **Failure cases:** Starts with the limit definition, uses formal notation too
  early, gives no analogy, or asks a question requiring calculus vocabulary.
- **Target score:** 5.

## Review Notes

- Test across at least six rows for small edits and all rows for behavior
  changes.
- Include at least one short-answer prompt and one high-stakes boundary prompt.
- For STEM / AI-CS changes, include at least three resource-augmented rows.
- For source-pack changes, include at least three V0.5 rows and one
  unavailable-or-insufficient source case.
- For V0.6 specialty-source changes, include at least four V0.6 rows plus one
  source-specificity or source-refresh row.
- For V0.7 adaptive-teaching changes, include rows that cover "I still don't
  understand," wrong answers, simpler explanation, deeper explanation,
  practice ladders, mistake analysis, STEM intuition-to-formal teaching,
  transfer, and at least one non-STEM case.
- For V0.8 STEM calibration changes, include rows that cover notation,
  derivation, proof, debugging, systems abstraction, signals, AI/ML bridges,
  when to ask, and when to explain directly.
- For V0.9 teaching-progress changes, include rows that cover correct answers
  without explanation, guided success, repeated confusion, overload, independent
  application, transfer, review-or-advance decisions, and one-question
  understanding checks.
- For V1.1 pacing and autonomous-resource changes, include rows that cover
  one-subproblem pacing, hints-only stop points, active source discovery,
  resource-orchestrated teaching, exam-pattern traps, and generic-AI contrast.
- For V1.2 teaching-mode and math-formatting changes, include rows that cover
  zero-base, standard, advanced, mode switching, concise advanced explanation,
  math formula rendering, Auto Mode calibration, and beginner real-world
  analogy.
- Prefer natural answers over rigid template completion.
- If any answer scores below 4, note whether the issue is diagnosis, depth,
  subject routing, safety boundary, or style.
