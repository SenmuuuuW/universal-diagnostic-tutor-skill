# Maintenance Notes

Use this file when updating the skill.

## Preserve The Skill Identity

The skill must remain universal and diagnosis-first. Do not optimize it for only
one subject, exam, age group, or platform.

Before merging a change, ask:

- Does this still work across many subjects?
- Does it still diagnose before teaching?
- Does it help the learner understand, not just finish?
- Is the added detail worth the context cost?

## Update Rules

- Update `SKILL.md` when the core workflow, trigger description, guardrails, or
  reference routing changes.
- Update reference files when adding subject-specific or format-specific
  guidance.
- Update examples when answer behavior changes.
- Update `CHANGELOG.md` for user-visible changes.
- Keep examples short enough to scan.

## Validation Checklist

- `SKILL.md` has valid YAML front matter.
- Front matter contains only `name` and `description`.
- Skill name remains `universal-diagnostic-tutor`.
- The description clearly triggers for learning-related questions across all
  subjects.
- The body does not make the skill single-subject.
- References are directly linked from `SKILL.md`.
- No unnecessary scripts or infrastructure were added.

## Versioning

Use semantic versioning once the skill is shared publicly.

- Patch: wording fixes, small examples, typo corrections.
- Minor: new reference guidance, new examples, improved formats.
- Major: substantial behavior change or incompatible restructuring.
