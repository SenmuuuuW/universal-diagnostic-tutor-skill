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
- Preserve the diagnosis-first workflow in `SKILL.md`.
- Keep `SKILL.md` concise enough to load as a skill body.
- Put detailed subject guidance in `skills/universal-diagnostic-tutor/references/`.
- Update examples when behavior or answer formats change.
- Update `CHANGELOG.md` for user-visible changes.
- Keep examples short, clear, and representative across subject areas.
- Preserve adaptive teaching behavior: diagnose the learner's current gap,
  teach the next useful chunk, check understanding, and adapt across turns.
- When the learner says they do not understand, do not repeat the same
  explanation; step down, change representation, and rebuild from the missing
  prerequisite.
- Do not let source packs replace teaching. Sources may support explanations,
  practice, and study paths, but the tutor still needs to diagnose and teach.
- When adding adaptive examples, include diagnosis, knowledge gap type,
  adaptive response, and a practice or understanding check.
- Do not make every answer a rigid template. Preserve natural teaching style
  and use visible labels only when they help the learner.
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

## Editing Notes

- Use simple Markdown and portable plain text.
- Keep front matter in `SKILL.md` valid YAML with only `name` and
  `description` fields.
- Keep the skill name as `universal-diagnostic-tutor`.
- When adding subject-specific guidance, make sure it remains compatible with
  the universal tutoring model.
- Prefer small, focused updates over broad rewrites.
