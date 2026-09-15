# DeepSeek Harness (DSH)

DSH loads the Skill folder natively. There is no DSH prompt to paste and no
DSH-specific tutoring instructions — this page covers installation, update,
verification, and limits only.

## What It Is

DSH's local skill provider scans project and user skill roots, parses each
`<name>/SKILL.md` frontmatter into the session catalog, and loads the body plus
`references/` only when the model needs them. `universal-diagnostic-tutor`
therefore runs as a first-class Skill:

```text
Universal Diagnostic Tutor Core
        ↓
DeepSeek Harness Skill Loader
```

The canonical behavior lives only in
[`skills/universal-diagnostic-tutor/`](../../skills/universal-diagnostic-tutor/).

## Installation

Skill roots are scanned in this order:

| Rank | Scope | Path |
| --- | --- | --- |
| 100 | project | `<projectRoot>/.dsh/skills` |
| 200 | project | `<projectRoot>/.agents/skills` |
| 300 | custom | provider `customSkillDirs` |
| 400 | user | `$DSH_HOME/skills` (default `~/.dsh/skills`) |
| 500 | user | `$DSH_AGENTS_HOME/skills` (default `~/.agents/skills`) |

`<projectRoot>` is the nearest ancestor containing `.git`; without one the
current working directory is used. Discovery is one level deep, so the linked
or copied entry must be the bundle directory itself.

User-level symlink (recommended — one source of truth, updates flow through):

```bash
git clone https://github.com/SenmuuuuW/universal-diagnostic-tutor-skill.git
cd universal-diagnostic-tutor-skill
mkdir -p ~/.agents/skills
ln -s "$(pwd)/skills/universal-diagnostic-tutor" ~/.agents/skills/universal-diagnostic-tutor
```

Project-level symlink (scopes the Skill to one repository):

```bash
mkdir -p /path/to/your-project/.agents/skills
ln -s /path/to/universal-diagnostic-tutor-skill/skills/universal-diagnostic-tutor \
  /path/to/your-project/.agents/skills/universal-diagnostic-tutor
```

Copy instead of symlink (simplest, needs re-copying on update):

```bash
mkdir -p ~/.agents/skills
cp -R skills/universal-diagnostic-tutor ~/.agents/skills/universal-diagnostic-tutor
```

The entry name must stay `universal-diagnostic-tutor`, matching the
frontmatter `name`.

## Update

- **symlink install:** `git pull` in the repository is enough; no reinstall.
- **copy install:** re-copy after `git pull` —
  `cp -R skills/universal-diagnostic-tutor ~/.agents/skills/universal-diagnostic-tutor`
- **confirm the version:** `git log --oneline -1` against the top of
  [`CHANGELOG.md`](../../CHANGELOG.md); for symlink installs you can also diff
  `SKILL.md` between the repository and the installed path.
- **reload:** DSH watches the roots, so added, renamed, deleted, or
  frontmatter-edited skills refresh the catalog before the next model step, and
  every load re-reads the current body. Opening a new session is the reliable
  way to confirm.

## Verification

In a new DSH session, ask naturally:

```text
教我一下梯度下降
```

```text
我为什么这里错了？我的答案是 \(3(2x+1)^2\)
```

```text
给我一道类似题
```

Confirm: `universal-diagnostic-tutor` appears in the skill catalog; loading it
returns a base directory at the installed path; no slash command is needed;
`references/` are read on demand rather than all at once; "我还是不懂" changes
the representation instead of repeating the same explanation; and a pasted
Learning State Card still continues earlier study.

## Known Limitations

- **One level deep.** Only `<root>/<name>/SKILL.md` and `<root>/<name>.md` are
  discovered. Pointing a root at the whole repository does not work, because
  `SKILL.md` would sit two levels down.
- **Frontmatter decides visibility.** `name` and `description` are required;
  `disable-model-invocation` and `user-invocable` control the model and user
  surfaces. A malformed value drops the skill with a warning rather than
  failing loudly in the catalog.
- **Copy installs drift.** Only a symlink keeps the repository as the single
  source of truth after `git pull`.
- **Reset policies differ per deployment.** Project and user roots can be
  disabled or reordered by provider config, so confirm the effective roots in
  your own DSH configuration when discovery fails.

## Difference From Ordinary DeepSeek Chat And API

- **DeepSeek Chat** — no Skill discovery. Paste the
  [Lite Prompt](../generic-chat/TUTOR_LITE_PROMPT.md) manually.
- **DeepSeek API** — you send the system prompt yourself; see
  [SYSTEM_PROMPT.md](../deepseek-api/SYSTEM_PROMPT.md). No automatic loading of
  `references/`.
- **DeepSeek Harness** — discovers and loads the Skill folder, including
  `references/`, with no prompt copy and no manual context management.

Chat and API are prompt-packaging surfaces; DSH is the native loading surface.
None of them get a second copy of the tutor's rules.
