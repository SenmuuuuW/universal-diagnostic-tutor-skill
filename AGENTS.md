# AGENTS.md

Guidance for future Codex maintenance work on this repository.

## Project Intent

This repository contains a reusable Codex Agent Skill for universal,
diagnosis-first tutoring across all subjects.

Future changes must preserve the core identity of the skill:

- It is universal across subjects.
- It is diagnosis-first, not answer-first.
- It supports mastery, not just task completion.
- It teaches from the learner's likely starting point.

## Maintenance Rules

- Do not narrow this skill into a SAT-only, math-only, coding-only, or
  single-subject tutor.
- Keep STEM / science / AI-CS as the clearest public positioning while
  preserving universal-capable diagnosis-first tutoring.
- Do not describe the Skill primarily as a generic all-subject assistant.
- Preserve the diagnosis-first workflow in `SKILL.md`.
- Keep `SKILL.md` concise enough to load as a skill body.
- Put detailed subject guidance in `skills/universal-diagnostic-tutor/references/`.
- Update examples when behavior or answer formats change.
- Update `CHANGELOG.md` for user-visible changes.
- Keep examples short, clear, and representative across subject areas.
- Preserve adaptive teaching behavior: diagnose the learner's current gap,
  teach the next useful chunk, check understanding, and adapt across turns.
- Preserve teacher-like pacing: teach one useful chunk, check, then continue.
- Preserve learner mode calibration: Auto, Zero-Base, Standard, and Advanced
  should be chosen from learner evidence, not treated as rigid labels.
- Do not assume a beginner knows notation, symbols, object types, or
  prerequisites.
- In Zero-Base Mode, explain symbols and objects before proof, theorem use, or
  full solution.
- After a check question, stop and wait for the learner instead of continuing
  to the next proof step, subproblem, theorem idea, or final result.
- Do not slow down advanced learners unnecessarily; if they ask for rigor,
  proof, derivation, edge cases, or concise explanation, keep the answer
  efficient unless a gap appears.
- Allow mode switching based on learner response. Step down for notation or
  prerequisite gaps; step up when the learner shows readiness.
- Do not expose mode labels too often if natural phrasing is better.
- Do not let the tutor solve too much at once.
- If the learner requests no direct answer, preserve at least one meaningful
  step for the learner unless they are stuck or ask for the final answer.
- Prefer one problem or subproblem at a time unless the user explicitly asks
  for a complete multi-question solution.
- When the learner says they do not understand, do not repeat the same
  explanation; step down, change representation, and rebuild from the missing
  prerequisite.
- Do not let source packs replace teaching. Sources may support explanations,
  practice, and study paths, but the tutor still needs to diagnose and teach.
- Do not assume users will upload materials. When web/search access is
  available and resources would improve teaching, verification, practice
  design, or exam-pattern analysis, the tutor may actively search for
  authoritative learning resources.
- When resources are used, integrate them into teaching instead of dumping
  links.
- Do not fabricate resources, citations, exams, course pages, authors,
  institutions, page numbers, or links.
- Make the Skill's difference from generic AI visible in examples and docs:
  diagnosis, pacing, stop points, resource discovery, resource orchestration,
  mistake analysis, checks, difficulty adjustment, and transfer.
- When adding adaptive examples, include diagnosis, knowledge gap type,
  adaptive response, and a practice or understanding check.
- Do not make every answer a rigid template. Preserve natural teaching style
  and use visible labels only when they help the learner.
- V0.8 focuses on STEM / AI-CS teaching calibration while preserving universal
  scope.
- Do not make adaptive STEM teaching overly robotic or over-labeled.
- Do not expose internal gap labels such as "notation gap" or "concept gap"
  unless naming the label genuinely helps the learner.
- Prefer natural teacher language such as "The part that may be causing trouble
  is..." over diagnostic labels.
- For STEM tutoring, prefer a short domain diagnosis before teaching: subject
  -> knowledge system -> subtopic -> core concept.
- For STEM examples, include diagnosis, gap type, ask-vs-explain choice,
  adaptive response, and a practice or understanding check.
- Ask guiding questions only when they help learning and the learner has enough
  foundation to reason one step.
- Explain directly when the learner lacks the vocabulary, notation, concept, or
  technical background needed to answer.
- V0.9 focuses on teaching progress within the current conversation, not on
  curriculum roadmaps or university course maps.
- Do not turn V0.9 into a roadmap, planner, persistent learner profile,
  database, or memory system.
- Do not assume mastery from one correct answer. Check whether the learner can
  explain why, apply with less help, or transfer the idea.
- Preserve teaching-progress focus: learner state, tutor decision, next
  teaching move.
- Keep mastery tracking lightweight and conversational; avoid rigid labels,
  scores, or visible state tables unless the user asks for a progress summary.
- Future mastery/progress examples should show learner state, tutor decision,
  example response, and why the tutor reviews, practices, simplifies, or
  advances.
- Do not add persistent memory, databases, telemetry, accounts, or storage
  unless explicitly requested.
- Do not add scripts, test harnesses, package managers, websites, or other
  infrastructure unless there is a clear recurring need.
- Do not add fake sources, invented citations, invented exams, or invented
  course materials.
- Do not commit copyrighted textbooks, scraped books, copied course packs, or
  large copied source materials.
- Do not add pirated textbooks, unofficial textbook uploads, copied PDFs, or
  downloaded course archives.
- In source packs, add only source metadata, links, coverage notes, usage notes,
  and cautions.
- Do not copy large source content into the repository.
- Verify links lightly when possible, and mark stale or unreachable sources
  instead of silently keeping them.
- Prefer specific course pages, lecture pages, official documentation pages,
  and problem-set pages over generic homepages.
- Prefer exact source pages over broad homepages when updating source packs.
- Mark links as stale, term-specific, or unverified when needed.
- Preserve the source trust hierarchy when adding or changing source packs.
- Keep source packs maintainable; do not turn them into huge dumps.
- Do not add offensive cybersecurity instructions or exploit walkthroughs.
- Keep security and cryptography content educational and defensive.
- Keep source entries lightweight and maintainable.
- Distinguish source-backed claims from general explanation when updating
  resource-augmented guidance.
- Preserve the universal identity while supporting the STEM / AI-CS primary use
  case.
- Do not add API keys, credentials, or secrets to the repository.
- Do not add external-search scripts unless explicitly requested.
- Do not put math formulas in code blocks. Use Markdown/LaTeX math for ordinary
  algebra, calculus, linear algebra, probability, and proof steps.
- In user-facing tutoring responses, prefer `\(...\)` and `\[...\]` for math;
  avoid raw `$...$` inline formulas because some chat environments render them
  badly.
- Use code blocks only for actual code, commands, paths, or literal text where
  spacing is essential.
- V1.0 is a stable consolidation release. Keep future V1.0 maintenance focused
  on clarity, consistency, documentation quality, and acceptance checks rather
  than feature expansion.
- Keep the root README and `skills/universal-diagnostic-tutor/README.md`
  professional, Chinese-friendly, not too dry, and aligned with the universal
  diagnosis-first identity.
- Keep the root README as the polished GitHub landing page and
  `skills/universal-diagnostic-tutor/README.md` as the Skill usage guide.
- Use emojis in README files sparingly and consistently as visual anchors;
  keep the tone serious, trustworthy, and not childish.
- Do not let README polish alter core Skill behavior, teaching protocols,
  source-pack scope, or repository infrastructure.
- If an external `quick_validate.py` check is used, note that it may require
  PyYAML in the local environment. Do not add package setup or dependency files
  only for that validator unless explicitly requested.

## Editing Notes

- Use simple Markdown and portable plain text.
- Keep front matter in `SKILL.md` valid YAML with only `name` and
  `description` fields.
- Keep the skill name as `universal-diagnostic-tutor`.
- When adding subject-specific guidance, make sure it remains compatible with
  the universal tutoring model.
- Prefer small, focused updates over broad rewrites.
