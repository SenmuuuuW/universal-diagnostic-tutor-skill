# Codex Usage

Use the full Skill directory:

```text
skills/universal-diagnostic-tutor/
```

This is the best experience for Codex-style workflows because Codex can use the
main `SKILL.md`, selected references, and examples as needed.

## Recommended Setup

- Clone or update the repository.
- Point Codex at `skills/universal-diagnostic-tutor/` according to your local
  Skill workflow.
- Keep `skills/tutor-*` alongside the main Skill if you want focused entrypoints
  such as Tutor Learn Path and Tutor Practice. V1.9.2 exposes six canonical
  entries in total.
- Read the root `INSTALL.md` for installation, update, and copied-directory
  troubleshooting.

## Tutor Practice

If Codex exposes focused Skill entrypoints, choose Tutor Practice /
`tutor-practice` for exercises, answer checking, qualitative grading, mistake
diagnosis, or readiness decisions. It normally gives one targeted exercise,
waits for the learner's answer, and then decides whether to advance or review.
One to three Knowledge Link Cards may be used only when a strongly related
concept blocks the current task.

`/practice` is a Tutor text shortcut and is not guaranteed to be a native
Codex slash command.

## Simplified Entrypoints

The public surface is Universal Diagnostic Tutor, Tutor Learn Path, Tutor
Practice, Tutor State Card, Tutor Resource Scan, and Tutor Visualize. Older
shortcut intents remain supported as text aliases rather than separate Skill
folders.

## Notes

- The full Skill gives the strongest behavior: routing, references, examples,
  evaluation docs, and Learning State Cards.
- If you copied the Skill directory into another location, `git pull` updates
  only the repo copy. Sync the copied `skills/universal-diagnostic-tutor/`
  directory too.
- Open a new Codex session after updating if the old session still uses cached
  instructions.

Do not duplicate `INSTALL.md` here; keep this file as a short Codex orientation.
