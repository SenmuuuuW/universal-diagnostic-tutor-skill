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
- Keep `SKILL.md` as a router, not a duplicate of every protocol.
- Put detailed subject guidance in `skills/universal-diagnostic-tutor/references/`.
- Prefer routing clarity over protocol sprawl.
- Update examples when behavior or answer formats change.
- Update `CHANGELOG.md` for user-visible changes.
- Add eval cases for repeated failures before broadening the Skill.
- Keep examples short, clear, and representative across subject areas.
- Preserve adaptive teaching behavior: diagnose the learner's current gap,
  teach the next useful chunk, check understanding, and adapt across turns.
- Do not solve by explaining more if a smaller intervention would work.
- Prefer the next best teaching step over a full lecture.
- Treat learner responses as mastery signals, not only right/wrong outcomes.
- Compress explanations when prerequisites are already known.
- Map mistake type to intervention type: notation, concept, method selection,
  setup, proof, calculation, transfer, overgeneralization, or memorized
  procedure.
- Keep README focused; the learning-efficiency loop is a selling point, not a
  complex technical diagram.
- Do not make README too long; link dedicated evaluation, rubric, taxonomy, and
  improvement docs instead of duplicating them.
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
- Normal tutoring answers should not expose internal Skill names, version
  numbers, repository files, protocol names, acceptance reports, or
  implementation details unless the user explicitly asks about the project.
- Do not expose internal gap labels such as "notation gap" or "concept gap"
  unless naming the label genuinely helps the learner.
- Prefer natural teacher language such as "The part that may be causing trouble
  is..." over diagnostic labels.
- For STEM tutoring, prefer a short domain diagnosis before teaching: subject
  -> knowledge system -> subtopic -> core concept.
- Keep domain diagnosis compact and useful; orient the learner, then teach.
- Use knowledge-system mapping to name the field, subtopic, core concept,
  prerequisites, and tested idea without creating a long roadmap.
- Use intuition or application bridges when they clarify abstract STEM
  concepts, but do not force applications when they distract.
- After a completed step, check, or misconception repair, add a transfer
  pattern when helpful: clue, method, trap, and tiny similar variation.
- Keep responses natural and teacher-like; do not make the learner watch the
  tutor execute protocols.
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
- Use Learning State Cards for cross-chat continuity, and do not imply hidden
  memory across chats.
- Context handoff should use user-visible cards or summaries, not persistent
  learner profiles.
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
- When editing old examples, migrate user-facing math from `$...$` / `$$...$$`
  to `\(...\)` / `\[...\]`, and keep intentional bad-formatting examples
  clearly labeled.
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
- Keep installation docs safe and conservative. Do not overclaim platform
  compatibility or imply native support where only manual adaptation is known.
- Distinguish native Skill use from manual prompt or project-instruction
  adaptation.
- Platform adapters must stay shorter than the full `SKILL.md` and should not
  duplicate the full reference system.
- Do not overclaim native compatibility for GPTs, Gemini Gems, Coze / Doubao,
  ordinary chat apps, API models, or local agents.
- Keep Lite Prompt usable without file references, repo access, or automatic
  loading of `references/` and `examples/`.
- Keep full Skill behavior in `skills/universal-diagnostic-tutor/`; platform
  adapters are downstream packaging.
- When core teaching behavior changes, update adapters only if the visible
  user-facing behavior changes.
- Ultra-Lite prompts may be short, but they should still avoid hidden-memory
  claims and ask for a Learning State Card when continuing prior study.
- API adapter wording should distinguish prompt guidance from actual API
  integration code and should not imply automatic context persistence.
- Do not add npm, npx, package setup, install scripts, path-detection scripts,
  or automated installers unless explicitly requested later.
- If installers are considered in the future, document risks, permissions,
  platform differences, and maintenance requirements first.
- Keep README concise; prefer replacing duplicated install/update text with
  links to `INSTALL.md` over appending long repeated sections.
- README can be polished and showcase-like, but must not overclaim, sound
  salesy, or imply benchmark results without real eval data.
- Showcase examples should live in root `EXAMPLES.md`, not as long blocks in
  README.
- README may include one short example preview and link to `EXAMPLES.md`.
- Keep showcase examples short, accurate, and aligned with actual Skill
  behavior: diagnosis-first, next best step, check-and-stop, and normal math
  formatting.
- The Core Reasoning Flow diagram is a public-facing selling point; keep it
  accurate, compact, and not overcomplicated.
- Prefer concrete examples, diagrams, capability matrices, and navigation
  tables over vague marketing claims.
- Keep README concise by linking to dedicated docs for installation,
  portability, evals, rubrics, failure taxonomy, and feedback workflow.
- Do not claim every platform has full native support; distinguish Full Skill,
  Custom Bot, Lite Prompt, and API Prompt usage.
- README should not duplicate `CHANGELOG.md`; keep only the latest major
  release highlight in the main body and send detailed history to the compact
  Version Timeline plus `CHANGELOG.md`.
- Put older versions in a compact Version Timeline and link to
  `CHANGELOG.md` for details.
- Describe current capabilities as present capabilities, not repeated
  historical release notes.
- Use emojis in README files sparingly and consistently as visual anchors;
  keep the tone serious, trustworthy, and not childish.
- Do not let README polish alter core Skill behavior, teaching protocols,
  source-pack scope, or repository infrastructure.
- Slash-style flows such as `/tutor`, `/study-plan`, `/exam-track`,
  `/state-card`, `/resource-scan`, and `/visualize` are user-facing intent
  shortcuts, not actual shell commands.
- Keep cards visible and user-controlled. Learner Profile Cards, Learning Task
  Cards, and Learning State Cards must never imply hidden persistence,
  databases, accounts, or automatic memory.
- STEM Exam Track must not promise score gains, predict exams, claim 押题, use
  leaked materials, or help with cheating.
- Topic Scan should stay compact and should not force resources into every
  answer.
- Visualizations must serve learning, not decoration. Do not add graphing
  scripts, image pipelines, or diagram infrastructure unless explicitly
  requested later.
- Keep Lite Prompt short enough for ordinary chat platforms; it should carry
  V1.7 intent shortcuts without duplicating the full Skill reference system.
- `skills/universal-diagnostic-tutor/` is canonical. `skills/tutor-*` folders
  are thin V1.8.1 entrypoints for discoverability, not separate Tutor systems.
- Do not duplicate the full Tutor Skill, reference system, or long protocol
  text inside each `tutor-*` sub-skill.
- Keep entrypoint `description` fields short, unique, and discoverable.
- If adding a new user-facing capability later, decide whether it needs a
  protocol reference, prompt shortcut, sub-skill entrypoint, and README /
  `COMMAND_SURFACE.md` documentation.
- README should only summarize the command surface. `COMMAND_SURFACE.md` is
  the canonical detailed Chinese tutorial for visible Codex Tutor entrypoints.
- Keep Chinese user-facing entrypoint explanations practical: what the user
  sees, when to choose it, and one example prompt.
- Do not promise exact Codex UI slash command behavior. `/study-plan` and
  similar names remain Tutor text shortcuts unless the host UI exposes them.
- Keep `tutor-*` entrypoints as thin wrappers around the main Tutor system.
- V1.8 is a learning architecture layer, not a new tool, assignment generator,
  grading system, course generator, graphing tool, database, or hidden-memory
  system.
- For broad goals, clarify the target and confirm it lightly before building a
  path.
- Knowledge maps should be compact, goal-specific, and used to choose the next
  step; do not build massive curriculum maps.
- Do not assume mastery of future concepts because a related concept was
  explained. Use checks and visible cards when status matters.
- Route to existing sub-skills instead of putting every behavior in
  `SKILL.md` or applying every protocol in one answer.
- If V1.8 behavior fails, patch the smallest relevant protocol, trigger row,
  example, or eval before adding new features.
- `USER_GUIDE.md` is the canonical beginner tutorial for non-technical users.
- `GROUP_GUIDE.md` should stay short and shareable; link to `USER_GUIDE.md`
  instead of duplicating the full tutorial.
- Generated PDFs should come from Markdown source and should not become the
  canonical source.
- Do not duplicate full tutorial content across README, INSTALL, PORTABILITY,
  or GROUP_GUIDE. Link to `USER_GUIDE.md` for step-by-step instructions.
- Keep non-technical user instructions simple: choose platform, copy the right
  prompt, ask a first learning question, and use Learning State Card to
  continue later.
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
