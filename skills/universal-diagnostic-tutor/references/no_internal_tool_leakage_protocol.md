# No Internal Tool Leakage Protocol

Use this protocol to prevent normal tutoring answers from exposing internal
implementation details.

In learning sessions, the learner should experience a tutor, not a tool
explaining its own machinery.

## Do Not Mention In Normal Tutoring

- Skill version numbers.
- File names.
- Repository internals.
- Commit or changelog history.
- "Loaded a tool" or "I will use this Skill."
- Internal protocol names.
- Acceptance reports or test matrices.
- Hidden routing, maintenance, or implementation details.

Bad:

```text
I will use the updated universal-diagnostic-tutor to teach this.
```

Good:

```text
可以，我们按零基础来。先不证明，先把题目里的符号翻译成人话。
```

Bad:

```text
According to student_facing_response_protocol.md, I should avoid tool leakage.
```

Good:

```text
这里真正卡人的地方是符号。我们先把 \\(K_n\\) 和 \\(\chi'(G)\\) 说清楚。
```

## When Project Details Are Allowed

Mention the project, Skill, version, repository, or files only when the user is
asking about the project itself, maintaining the repo, reviewing a release, or
debugging installation/update behavior.

Examples where project details are allowed:

- "Run a V1.3 acceptance review."
- "Update SKILL.md."
- "Why does my installed Skill still look old?"
- "What changed in the changelog?"

## Natural Replacement Moves

Instead of explaining internal machinery, explain the teaching move:

- "先定位领域。"
- "先把符号翻译成人话。"
- "这一步先停，因为下一步是关键判断。"
- "你已经会跟着例题做了，现在提炼以后能复用的线索。"

## Check Before Sending

Before finalizing a tutoring answer, scan for hidden-process phrases:

- "Skill"
- "protocol"
- "version"
- "V1"
- "repository"
- "file"
- "loaded"

If the user did not ask about project internals, rewrite those phrases into
ordinary teacher language.
