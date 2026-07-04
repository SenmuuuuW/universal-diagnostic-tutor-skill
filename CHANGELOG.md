# Changelog

All notable changes to this project will be documented in this file.

## v1.7.0 - 2026-07-04

### Added In v1.7.0

- Added Matt-style Skill Pack invocation layer for `/tutor`, `/diagnose-gap`,
  `/study-plan`, `/exam-track`, `/state-card`, `/resource-scan`, `/visualize`,
  and `/mistake-review`.
- Added `GROUP_GUIDE.md` for ordinary users, students, and community sharing.
- Added Topic Scan + Trusted Resources protocol.
- Added Brief Study Plan protocol.
- Added STEM Exam Track / 理科备考 Track.
- Added learner profile and learning task card protocol.
- Added basic STEM visualization guidance.
- Added V1.7 examples for invocation flows, topic scan/resources, machine
  learning study planning, exam-track series review, learner/task cards, and
  vector visualization.

### Changed In v1.7.0

- Updated `SKILL.md` routing for V1.7 flows, cards, topic scan, study plans,
  exam track, and visualization.
- Updated README, Skill README, platform adapters, evals, rubric, failure
  taxonomy, feedback workflow, output formats, evaluation checklist, and manual
  test matrix for V1.7 behavior.

### Unchanged In v1.7.0

- No infrastructure, database, hidden memory, installer, source-pack, website,
  script, API integration code, package setup, npm/npx package, PDF, secret,
  copied-content, curriculum map, real RAG/vector DB, or account-system
  changes.

## v1.6.3 - 2026-06-30

### Changed In v1.6.3

- Added root `EXAMPLES.md` with concise answer-first vs diagnosis-first
  showcase examples.
- Restored and polished the README core reasoning / teaching flow diagram.
- Linked README and Skill README to `EXAMPLES.md` instead of keeping long
  showcase examples inside README.
- Cleaned README version/update layout so older version details live in Version
  Timeline / CHANGELOG.
- Kept README as a public-facing landing page without making it changelog-like.
- Collapsed Skill README historical notes into a compact version pointer.

### Unchanged In v1.6.3

- No core tutoring behavior, infrastructure, installer, source-pack, API
  integration code, package setup, database, persistent memory, real
  RAG/vector DB, PDF, secret, copied-content, curriculum map, platform adapter,
  or website changes.

## v1.6.2 - 2026-06-30

### Changed In v1.6.2

- Polished the root README first-screen positioning.
- Added a compact Core Learning Engine snapshot.
- Added a compact capability matrix.
- Clarified how diagnosis-first tutoring differs from answer-first style.
- Improved public-facing navigation to install, portability, adapters, evals,
  rubric, failure taxonomy, and feedback docs.

### Unchanged In v1.6.2

- No core tutoring behavior, infrastructure, installer, source-pack, API
  integration code, package setup, database, persistent memory, real
  RAG/vector DB, PDF, secret, copied-content, curriculum map, platform adapter,
  or website changes.

## v1.6.1 - 2026-06-30

### Changed In v1.6.1

- Clarified that the Ultra-Lite Prompt should not claim cross-chat memory and
  should ask for a Learning State Card when continuing prior study.
- Clarified that the DeepSeek/API adapter is usable for DeepSeek-compatible and
  OpenAI-compatible API-style usage.

### Unchanged In v1.6.1

- No core tutoring behavior, infrastructure, installer, source-pack, API
  integration code, package setup, database, persistent memory, real
  RAG/vector DB, PDF, secret, copied-content, curriculum map, or website
  changes.

## v1.6.0 - 2026-06-30

### Added In v1.6.0

- Added `PORTABILITY.md` for full Skill, custom bot, Lite Prompt, and API prompt
  usage guidance.
- Added platform-specific prompt adapters under `platforms/`.
- Added generic Lite and Ultra-Lite prompts for ordinary chat AIs.
- Added ChatGPT GPT, ChatGPT Project, Gemini Gem, Coze / Doubao, DeepSeek / API,
  Codex, and Claude Code-style usage notes.
- Clarified full Skill vs custom bot vs Lite Prompt vs API prompt usage.
- Added a small portability eval for adapter selection and overclaiming checks.

### Unchanged In v1.6.0

- No core teaching behavior, script, installer, API integration code,
  infrastructure, source-pack, website, package setup, npm/npx package,
  database, persistent memory, PDF, secret, curriculum map, real RAG/vector DB,
  or copied-content changes.

## v1.5.0 - 2026-06-30

### Added In v1.5.0

- Added Skill routing architecture.
- Added trigger and mode activation matrix.
- Added `EVALS.md` for manual Skill behavior evaluation.
- Added `QUALITY_RUBRIC.md` for 1-5 tutoring quality scoring.
- Added `FAILURE_TAXONOMY.md` for evidence-based failure classification.
- Added `FEEDBACK_TO_IMPROVEMENT.md` for turning repeated failures into small,
  testable Skill improvements.
- Added Learning State Card protocol.
- Added context handoff protocol.
- Added context compression checkpoint protocol.
- Added stateless recovery protocol.
- Added cross-chat continuity examples for graph theory, linear algebra,
  series, stateless recovery, and known-X-not-Y handoff.
- Updated README, Skill README, AGENTS, evaluation checklist, and manual test
  matrix for V1.5 reliability and context portability.

### Unchanged In v1.5.0

- No infrastructure, source-pack, installer, website, script, API, package
  setup, npm/npx package, database, persistent memory, PDF, secret,
  curriculum map, real RAG/vector DB, or copied-content changes.

## v1.4.0 - 2026-06-29

### Added In v1.4.0

- Added Learning Efficiency Optimization Loop.
- Added next-best-teaching-step protocol.
- Added cognitive-load budget protocol.
- Added mastery-signal interpretation protocol.
- Added explanation-compression protocol.
- Added error-to-intervention protocol.
- Added examples for graph theory, series, linear algebra, gradient descent,
  and binary search.
- Updated README to present the core loop as a stronger project principle.

### Unchanged In v1.4.0

- No infrastructure, source-pack, installer, website, script, API, package
  setup, npm/npx package, database, persistent memory, PDF, secret,
  curriculum map, real RAG/vector DB, or copied-content changes.

## v1.3.1 - 2026-06-29

### Changed In v1.3.1

- Added Chinese `INSTALL.md` for installation, update, and troubleshooting.
- Clarified what users should download and which folder is the actual Skill:
  `skills/universal-diagnostic-tutor/`.
- Added an agent-assisted installation prompt for Codex / Claude Code-style
  agents.
- Clarified platform / AI compatibility for Codex, Claude Code-style agents,
  instruction-based agents, ordinary chat, and local / IDE agents.
- Polished README structure by linking to `INSTALL.md` instead of repeating
  full installation details.

### Unchanged In v1.3.1

- No core Skill behavior, teaching protocol, source-pack, website, script, API,
  package setup, npm package, database, persistent memory, PDF, secret,
  curriculum map, real RAG/vector DB, or infrastructure changes.

## v1.3.0 - 2026-06-29

### Added In v1.3.0

- Student-facing response protocol for natural teacher-like tutoring answers.
- Knowledge-system mapping protocol for compact field, subtopic, prerequisite,
  and tested-concept orientation.
- Intuition/application bridge protocol for connecting abstract STEM concepts
  to concrete examples, real phenomena, technical systems, AI/CS applications,
  later courses, and common problem types.
- Transfer-pattern teaching protocol for extracting reusable clues, methods,
  traps, and near-transfer variations after a step or check.
- No-internal-tool-leakage protocol to prevent ordinary tutoring answers from
  mentioning Skill versions, repository files, internal protocols, or hidden
  implementation details.
- Examples for graph theory, series convergence, gradient descent, linear
  algebra transfer, and bad-vs-good internal leakage behavior.
- Chinese update guidance in the root README and a shorter Skill-level update
  note for users with cloned or copied Skill directories.

### Unchanged In v1.3.0

- No infrastructure, source-pack, database, roadmap, persistent memory,
  website, script, API, package setup, PDF, secret, or copied-content changes.

## v1.2.3 - 2026-06-29

### Changed In v1.2.3

- Cleaned up remaining raw dollar-sign math in older examples.
- Standardized user-facing math examples toward `\(...\)` and `\[...\]`.
- Replaced formula-only fenced code blocks in older examples with math displays.
- Preserved intentional bad-formatting examples only where clearly labeled.
- Made no behavior, protocol, infrastructure, or source-pack changes.

## v1.2.2 - 2026-06-29

### Changed In v1.2.2

- Clarified STEM / science / AI-CS-first positioning while preserving
  universal-capable diagnosis-first tutoring.
- Added and strengthened compact domain diagnosis guidance for substantial
  STEM tutoring: subject -> knowledge system -> subtopic -> core concept.
- Tightened Zero-Base Mode pacing so the tutor explains objects and symbols
  before proof or solution, introduces only one or two new concepts, asks a
  check, then stops.
- Improved math rendering guidance to prefer `\(...\)` and `\[...\]` in
  user-facing tutoring responses and avoid raw dollar-sign formulas.
- Polished README and Skill README prompt examples around domain diagnosis,
  stop-after-check behavior, and math formatting.
- Updated evaluation checklist, manual test matrix, and existing examples for
  V1.2.2 acceptance coverage.

### Unchanged In v1.2.2

- No new major teaching features, source packs, websites, scripts, APIs,
  package setup, databases, persistent memory, PDFs, secrets, copied content,
  curriculum maps, real RAG/vector DB, or infrastructure.

## v1.2.1 - 2026-06-28

### Changed In v1.2.1

- Polished the Chinese GitHub README for a stronger first impression and more
  readable open-source landing page.
- Improved visual structure, tasteful emoji anchors, section hierarchy, and
  new-user onboarding.
- Added clearer learning mode presentation for Zero-Base, Standard, Advanced,
  and Auto Mode.
- Added a clearer Skill-vs-generic-AI comparison and core teaching loop.
- Clarified quick-start instructions, copyable Chinese prompts, example topic
  areas, limitations, and repository structure.
- Kept V1.2.1 as documentation polish only: no core Skill behavior changes,
  new teaching protocols, source packs, scripts, websites, APIs, package setup,
  databases, persistent memory, PDFs, secrets, curriculum maps, real RAG/vector
  DB, or infrastructure.

## v1.2.0 - 2026-06-28

### Added In v1.2.0

- Teaching mode selection protocol for Auto, Zero-Base, Standard, and Advanced
  tutoring modes.
- Beginner foundation teaching protocol for true zero-base learners who need
  concepts, symbols, object types, and prerequisites before solving.
- Standard and advanced mode protocol for balancing normal method recognition
  and guided practice against concise rigorous derivation, proof, assumptions,
  edge cases, efficiency, and transfer.
- Math formatting protocol requiring Markdown/LaTeX math for formulas and
  reserving code blocks for actual code, commands, paths, or literal text.
- User mode onboarding guide with Chinese copyable prompts.
- Examples for zero-base vector teaching, standard series convergence,
  advanced derivative proof, mode switching, and math formatting good-vs-bad
  behavior.

### Changed In v1.2.0

- Updated `SKILL.md`, README files, evaluation checklist, and manual test
  matrix to route V1.2 teaching modes and math-formatting behavior.
- Preserved V1.1 teacher-like pacing and stop points while adding learner-level
  calibration.

## v1.1.0 - 2026-06-28

### Added In v1.1.0

- Interaction pacing protocol for one-subproblem-at-a-time tutoring,
  teach-check-continue rhythm, and avoiding over-solving.
- Teacher-like stop point protocol for pausing after translation, target
  identification, method choice, misconception repair, new representations, or
  before final calculations.
- Autonomous resource discovery protocol for actively searching authoritative
  learning resources when web/search access is available and useful.
- Resource-orchestrated tutoring protocol for turning searched resources,
  curated source packs, or user-provided materials into teaching rather than
  link lists.
- Exam-pattern resource analysis for tested concepts, common traps,
  recognition cues, and short practice ladders.
- Skill-vs-generic-AI advantage guidance to clarify the Skill's unique
  diagnosis, pacing, resource, and mastery behavior.
- Examples for interaction pacing, autonomous resource discovery, probability
  exam traps, and generic-AI-vs-Skill comparison.

### Changed In v1.1.0

- Updated `SKILL.md`, README files, evaluation checklist, and manual test
  matrix to route V1.1 pacing and resource-discovery behavior.
- Clarified that V1.1 is still Markdown-only teaching behavior: no website,
  scripts, APIs, package setup, databases, persistent memory, real RAG/vector
  database, PDFs, copied materials, curriculum map, or new source packs.

## v1.0.0 - 2026-06-28

### Added In v1.0.0

- Stable consolidation release for the `universal-diagnostic-tutor` Skill.
- Rewritten Chinese GitHub README explaining project identity, intended users,
  capabilities, usage, repository structure, quality principles, limitations,
  and license.
- Skill-level Chinese README for `skills/universal-diagnostic-tutor/`, covering
  when to use the Skill, when not to use it, STEM / AI-CS strengths, prompt
  examples, reference-file roles, and maintenance notes.

### Changed In v1.0.0

- Clarified that the project is a reusable diagnosis-first teaching behavior
  layer, not a website, app, database, course platform, curriculum roadmap, or
  persistent learner-memory system.
- Documented the optional `quick_validate.py` PyYAML requirement without adding
  dependency files or package setup.
- Kept V1.0 as documentation polish and stable consolidation only; no new
  teaching protocols, source packs, scripts, APIs, PDFs, secrets, or
  infrastructure were added.

## v0.9.0 - 2026-06-28

### Added In v0.9.0

- Mastery state protocol for tracking local learner evidence such as exposure,
  recognition, guided understanding, independent explanation, guided or
  independent application, transfer, misconception, and overload.
- Cross-turn progress protocol for carrying forward what the learner has shown
  within the current conversation without assuming mastery too early.
- Understanding check protocol for supportive one-question, explain-it-back,
  method-classification, prediction, error-spotting, near-transfer, and
  confidence checks.
- Difficulty adjustment protocol for decreasing, maintaining, or increasing
  abstraction, notation density, number of steps, proof rigor, coding
  complexity, system layers, and source load.
- Review-or-advance decision guidance for choosing whether to review,
  re-explain, guide practice, give near-transfer, advance, simplify, or answer
  first in speed mode.
- Mastery and progress examples for matrix notation, recursion across turns,
  gradient-descent overload, and derivative review-versus-advance decisions.

### Changed In v0.9.0

- Updated `SKILL.md` and the adaptive teaching engine to route cross-turn
  tutoring through mastery-state, difficulty, understanding-check, and
  review-or-advance guidance.
- Expanded the manual test matrix and evaluation checklist with V0.9 teaching
  progress criteria.

## v0.8.0 - 2026-06-28

### Added In v0.8.0

- STEM ask-vs-explain calibration for choosing between guiding questions and
  direct explanation in technical learning.
- STEM natural adaptive style guidance for keeping gap diagnosis teacher-like
  and minimally labeled.
- Symbol and notation teaching protocol for formulas, object types, code-like
  notation, systems notation, ML tensors, and physical quantities.
- Proof and derivation protocol for explaining why formulas, theorems, and
  algorithms work.
- STEM problem-solving protocol for equations, diagrams, code traces,
  algorithms, debugging, systems, and ML workflows.
- STEM adaptive teaching examples for matrix notation, derivative derivation,
  binary search proof, Python debugging, virtual memory, physical signals, and
  AI/ML prerequisite bridges.

## v0.7.0 - 2026-06-28

### Added In v0.7.0

- Adaptive teaching engine reference for multi-turn tutoring, knowledge-gap
  diagnosis, "I still don't understand" handling, practice ladders, mistake
  analysis, STEM intuition-to-formal teaching, and mastery signals.
- Knowledge gap taxonomy for vocabulary, concept, notation, procedure,
  reasoning, recognition, transfer, misconception, confidence, and resource
  gaps.
- Multiturn tutoring protocol for confused learners, wrong or partially correct
  answers, simpler or deeper explanations, practice requests, overwhelmed
  learners, and subject changes.
- Practice ladder reference from recognition checks through real-world or
  project-style application.
- Mistake analysis protocol for distinguishing careless and conceptual errors,
  repairing misconceptions, and assigning near-match practice.
- STEM teaching sequence for math, programming, AI/ML, computer systems,
  physics, electronics, and signals.
- Output formats for adaptive multi-turn tutoring and practice ladder mode.
- Examples for matrix-multiplication follow-up tutoring, still-confused
  derivative handling, algebra mistake analysis, conditional-probability
  misconception repair, recursion practice ladders, and gradient-descent
  STEM teaching.
- Manual test rows for V0.7 adaptive teaching behavior across STEM and
  non-STEM learning scenarios.

### Changed In v0.7.0

- Updated `SKILL.md` to route confused learners, practice requests, mistake
  analysis, and multi-turn tutoring through the adaptive teaching engine.
- Expanded the evaluation checklist with adaptive teaching criteria.
- Clarified depth adaptation so deeper answers change teaching strategy rather
  than merely adding more detail.

## v0.6.0 - 2026-06-27

### Added In v0.6.0

- Specialty source addendums for theory/formal methods, cryptography/security,
  numerical analysis, HPC/control, and VR/multimedia.
- Networks-from-zero source pack for beginner-friendly networking study.
- Source specificity guidelines for preferring exact pages over broad
  homepages.
- Source refresh maintenance guidance for stale, unverified, and term-specific
  sources.
- Examples for networks, cryptography, numerical analysis, and formal
  languages.

### Changed In v0.6.0

- Updated the source checklist with specificity, source count, beginner-vs-
  advanced, and stale-link checks.
- Expanded the manual test matrix with V0.6 specialty source-pack tests.

## v0.5.0 - 2026-06-26

### Added In v0.5.0

- Curated STEM / AI-CS source packs for math foundations, programming and CS,
  systems, networks, security, AI/ML/data, physics/electronics/signals,
  graphics/HCI/software, and exam or problem-set practice.
- Source pack usage guide for choosing source packs without narrowing the
  universal tutor identity.
- Source note checklist for safer citation and source-list behavior.
- Source pack usage example for building an ML foundations learning path.

### Changed In v0.5.0

- Improved source selection for resource-augmented tutoring.
- Expanded the manual test matrix with V0.5 source-pack behavior tests.

## v0.4.0 - 2026-06-26

### Added In v0.4.0

- Resource integration protocol for resource-augmented learning answers.
- Source trust hierarchy for choosing reliable learning resources.
- STEM / AI-CS scope reference for university-level science and engineering
  study.
- Resource-augmented output formats for concept explanations, problem solving,
  exam-pattern analysis, learning paths, and source-limited answers.
- Resource-augmented STEM, AI, CS, and exam-pattern examples.
- Source-limited answer example for environments without web access.

### Changed In v0.4.0

- Strengthened citation, source-listing, and no-hallucinated-source rules.
- Expanded the manual test matrix with resource-augmented STEM / AI-CS tests.

## v0.3.0 - 2026-06-26

### Added In v0.3.0

- Manual test matrix covering 12 subject and boundary scenarios.
- Response length calibration reference for ultra-short, short, standard, and
  deep answers.
- Health and finance educational boundary examples.
- Humanities evidence example focused on support, proof, and uncertainty.
- Natural style example showing robotic vs natural diagnosis-first teaching.

### Changed In v0.3.0

- Improved output format guidance for answer length, implicit diagnosis, and
  natural section use.

## v0.2.0 - 2026-06-26

### Added In v0.2.0

- Manual V0.2 evaluation checklist with pass/fail criteria and a 1-5 rubric.
- Realistic full-answer examples for law/civics, economics/business, writing
  revision, AI concepts, and mixed-subject tutoring.
- Bad-vs-good example showing compact diagnosis for a short-answer request.

### Changed In v0.2.0

- Improved compact diagnosis guidance for short-answer mode.
- Strengthened high-stakes educational boundaries for law, finance, and other
  professional domains.
- Expanded subject teaching guidance for writing, AI concepts, law/civics,
  economics/business, and mixed-subject questions.

## v0.1.0 - 2026-06-26

### Added In v0.1.0

- Initial `universal-diagnostic-tutor` Codex Skill.
- Diagnosis-first tutoring workflow for all learning-related questions.
- Subject teaching modes for math, science, humanities, language, writing,
  coding, law, economics, business, and exam prep.
- Five teaching depth levels.
- Reusable output formats for common tutoring situations.
- First example set across math, science, humanities, coding, language and
  literature, and exam prep.
