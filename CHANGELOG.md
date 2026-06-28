# Changelog

All notable changes to this project will be documented in this file.

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
