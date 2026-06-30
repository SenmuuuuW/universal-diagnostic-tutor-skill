# Feedback To Improvement

Use this workflow to turn real tutoring feedback into small, testable Skill
improvements.

## Workflow

1. **Collect real tutoring output.** Save the prompt, visible answer, and user
   feedback. Do not include private or sensitive details unless the user has
   explicitly approved doing so.
2. **Identify user intent and mode.** Note whether the request was zero-base,
   standard, advanced, speed mode, mistake analysis, resource-supported
   tutoring, or context handoff.
3. **Mark the failure type.** Use `FAILURE_TAXONOMY.md` to classify the most
   specific failure.
4. **Score the output.** Use `QUALITY_RUBRIC.md` to score the relevant
   dimensions from 1 to 5.
5. **Decide isolated vs repeated.** One weak answer may need only an example or
   wording patch. Repeated failures need an eval case.
6. **Find the smallest fix.** Prefer editing one protocol, example, or routing
   note. Avoid broad new features for a narrow failure.
7. **Add or update an eval case.** Every repeated failure should become a test
   in `EVALS.md` or `references/manual_test_matrix.md`.
8. **Re-test before release.** Run the relevant evals and at least one adjacent
   behavior test so the fix does not regress pacing, mode selection, math
   formatting, or resource integrity.
9. **Record the change.** Add a concise `CHANGELOG.md` entry that names the
   behavior improved and confirms no unwanted infrastructure was added.

## Improvement Principles

- Preserve STEM / AI-CS as the primary current use case while keeping the Skill
  universal-capable.
- Preserve concise, natural, student-facing tutoring.
- Keep `SKILL.md` as a router; put detailed behavior in references.
- Prefer routing clarity over protocol sprawl.
- Do not add scripts, databases, persistent memory, real RAG/vector DB,
  package setup, source packs, copied content, or infrastructure for a tutoring
  behavior issue.
- If a fix would make ordinary answers longer or more mechanical, rethink it.

## Minimal Patch Examples

- Repeated raw dollar math -> patch math formatting examples and add one eval.
- Repeated no-stop-point behavior -> patch stop-point wording and add a
  hints-only eval.
- Repeated context loss -> improve Learning State Card examples and add a
  handoff eval.
- Repeated fake source risk -> tighten source note checklist and add a
  resource-supported eval.
