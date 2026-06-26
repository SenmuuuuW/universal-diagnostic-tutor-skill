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
- Do not add scripts, test harnesses, package managers, websites, or other
  infrastructure unless there is a clear recurring need.

## Editing Notes

- Use simple Markdown and portable plain text.
- Keep front matter in `SKILL.md` valid YAML with only `name` and
  `description` fields.
- Keep the skill name as `universal-diagnostic-tutor`.
- When adding subject-specific guidance, make sure it remains compatible with
  the universal tutoring model.
- Prefer small, focused updates over broad rewrites.
