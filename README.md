<div align="center">

# Universal Diagnostic Tutor

**A diagnosis-first AI tutor that decides what the learner needs next — without making them choose modes or commands.**

English | [简体中文](README.zh-CN.md)

[![Version](https://img.shields.io/badge/version-2.0.0-1f6feb.svg)](CHANGELOG.md)
![Markdown only](https://img.shields.io/badge/Markdown-only-555555.svg)
[![DeepSeek Harness](https://img.shields.io/badge/DeepSeek%20Harness-native%20skill-2f6f4e.svg)](platforms/deepseek-harness/README.md)
![Focus: STEM and AI-CS](https://img.shields.io/badge/Focus-STEM%20%2F%20AI--CS-1f6feb.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-2f6f4e.svg)](LICENSE)

[User Guide](USER_GUIDE.md) · [Command Surface](COMMAND_SURFACE.md) · [Install](INSTALL.md) · [Portability](PORTABILITY.md) · [Examples](EXAMPLES.md) · [Changelog](CHANGELOG.md)

</div>

---

## What It Is

Universal Diagnostic Tutor is a Markdown-only tutor behavior layer for
university-level STEM, mathematics, programming, AI/CS, and exam review.

The difference from an ordinary AI answer is one sentence:

> **It does not answer first. It works out where you are stuck first.**

It locates the subject, concept, prerequisite, notation, method, or reasoning
gap, then chooses the smallest step that actually unlocks progress. Before
advancing it checks real evidence — one correct answer is not mastery.

It is not a course platform, question bank, database, RAG system, or hidden
memory service.

---

## New: Native DeepSeek Harness Skill

**DeepSeek Harness (DSH) now loads this Skill natively.** No prompt to paste,
and no DSH-specific second set of instructions.

```text
Universal Diagnostic Tutor Core
        ↓
DeepSeek Harness Skill Loader
```

DSH scans its skill roots, parses `universal-diagnostic-tutor/SKILL.md` into the
session catalog, and loads the body plus `references/` only when the model needs
them. Recommended install (user-level symlink):

```bash
git clone https://github.com/SenmuuuuW/universal-diagnostic-tutor-skill.git
cd universal-diagnostic-tutor-skill
mkdir -p ~/.agents/skills
ln -s "$(pwd)/skills/universal-diagnostic-tutor" ~/.agents/skills/universal-diagnostic-tutor
```

Full install, update, and verification steps live in
[INSTALL.md](INSTALL.md#deepseek-harness--dsh); the platform notes live in
[platforms/deepseek-harness/](platforms/deepseek-harness/README.md).

Three different DeepSeek surfaces, three different loading models:

| Surface | Loading | What you do |
| --- | --- | --- |
| DeepSeek **Chat** | Not native | Paste the Lite Prompt manually |
| DeepSeek **API** | Not native | Send the system prompt yourself |
| **DeepSeek Harness** | **Native Skill** | Install once, then use natural language |

---

## One Tutor, No Feature Menu

V2.0 collapsed the public surface into one tutor. Practice, grading, mistake
review, planning, exam review, resources, visualization, and continuity are no
longer separate entrypoints — the tutor routes to them from natural language.

| Before | Now |
| --- | --- |
| Choose a feature or sub-entrypoint | Just say what you need |
| Memorize slash commands | Not needed; legacy forms stay silently recognized |
| Decide whether to practice or be taught | The tutor decides |
| Multiple learning cards | One Learning State Card (optional fields) |
| Mode menu (Zero-Base / Standard / Advanced) | Inferred from your own wording |

You only have to speak plainly:

```text
教我这个
我为什么错了
我还是不懂
给我练习
推荐资料
画一下
我准备考试
继续上次的学习
```

Legacy slash text (`/practice`, `/study-plan`, `/mistake-review`, and others)
is still recognized silently for backward compatibility, but it is no longer
required or advertised.

---

## Core Loop

```text
Clarify → Diagnose → Intervene → Check → Decide → Carry
```

| Stage | What happens |
| --- | --- |
| Clarify | Only for vague broad goals: one to three focused questions, then wait |
| Diagnose | Subject → knowledge system → subtopic → core concept, plus the blocking gap |
| Intervene | Teach one compact unit: object meaning, method cue, setup, proof hinge, or misconception repair |
| Check | One focused check or tiny task; stop and wait when participation is the point |
| Decide | Read the answer as a mastery signal: advance, transfer, compress, re-explain, step down, or keep practicing |
| Carry | Light tracking in-conversation; a visible Learning State Card across chats |

Not every question runs the whole chain. A quick factual question does not
trigger a giant workflow, and a practice turn normally stops after one targeted
exercise to wait for the learner's answer.

---

## Quick Start

| Where you use AI | Start here |
| --- | --- |
| **DeepSeek Harness (DSH)** | **Native / first-class Skill support** — install `skills/universal-diagnostic-tutor/` into a DSH skill root; see [DSH install](INSTALL.md#deepseek-harness--dsh) |
| Ordinary ChatGPT, Gemini, Doubao, Kimi, or Qwen chat | Copy the [Lite Prompt](platforms/generic-chat/TUTOR_LITE_PROMPT.md) |
| Codex or Claude Code-style agent | Use the [Full Skill](skills/universal-diagnostic-tutor/) and follow the [install guide](INSTALL.md) |
| Custom bot or **DeepSeek API** prompt | Choose an adapter in [Portability](PORTABILITY.md) |

New to the project? Read the [User Guide](USER_GUIDE.md). Installation and
updates live in [INSTALL.md](INSTALL.md), while the single entrypoint is
explained in [COMMAND_SURFACE.md](COMMAND_SURFACE.md).

---

## What The Tutor Does

These are behaviors the tutor performs automatically from what the learner
says — not features to choose from a menu.

| Behavior | What it does |
| --- | --- |
| Diagnosis-first tutoring | Locates the subject, concept, prerequisite, notation, method, or reasoning gap |
| Broad-goal planning | Clarifies broad goals, builds a compact knowledge map, and selects one next step |
| Practice and mastery | Generates targeted practice, waits for an answer, grades qualitatively, repairs mistakes, and checks readiness |
| Natural-language routing | One tutor; practice, planning, resources, visuals, and continuity trigger from what the learner says |
| Exam-aware review | Supports university STEM, postgraduate math, and CS review without prediction or score promises |
| Resource-supported teaching | Uses reliable learning resources when they improve the current teaching step |
| Related-concept cards | Explains one to three strongly related concepts when they block the current task |
| Learning State Card | A visible, copyable checkpoint for continuation, never hidden memory |
| Cross-platform adapters | Packages smaller prompt versions for chat, custom bots, and API use |

The strongest coverage is university-level STEM and AI-CS: calculus, linear
algebra, probability, discrete mathematics, programming, algorithms, machine
learning, systems, networks, physics, signals, and engineering foundations. The
tutor stays useful across other domains, but it is not positioned as a generic
answer bot.

---

## One Tutor, One Learning State Card

Continuing across chats needs exactly one visible artifact:

```text
Learning State Card:
- Subject:
- Topic:
- Already understood:
- Still weak:
- Next best step:
- Optional — preferred language / pace:
- Optional — active goal or exam target:
```

Preferences, the active goal, and the latest practice are **optional fields of
the same card**. No parallel card types exist, and the card never implies hidden
persistence, accounts, or a database.

---

## Evaluation (project-frozen harness)

In this repository's fixed 29-case evaluation harness, v2.0.0 against the
v1.9.2 baseline:

| Metric | v1.9.2 | v2.0.0 |
| --- | --- | --- |
| Identity group | 4.622 | 4.819 |
| Quality group | 4.135 | 4.619 |
| Over-teaching control | 3.62 | 4.62 |
| Mistake diagnosis | 3.75 | 4.50 |
| Next-best teaching step | 4.03 | 4.55 |
| Naturalness | 4.53 | 4.76 |
| Critical failures / leakage | 0 / 0 | 0 / 0 |

Runtime context in the same harness dropped from about 11,388 to about 6,678
tokens (roughly −41%).

These numbers come from this repository's own frozen harness. They are **not**
universal performance claims across every model or environment.

---

## Documentation

| Document | Purpose |
| --- | --- |
| [User Guide](USER_GUIDE.md) | Beginner-friendly setup and usage tutorial |
| [Command Surface](COMMAND_SURFACE.md) | Single-tutor usage and natural-language examples |
| [Install](INSTALL.md) | Installation, updates, copied-Skill synchronization, and the DSH section |
| [Portability](PORTABILITY.md) | Full Skill, custom bot, Lite Prompt, and API prompt choices |
| [Examples](EXAMPLES.md) | Short diagnosis-first tutoring examples |
| [Evaluations](EVALS.md) | Behavioral evaluation cases |
| [Quality Rubric](QUALITY_RUBRIC.md) | Scoring criteria for tutoring quality |
| [Failure Taxonomy](FAILURE_TAXONOMY.md) | Known failure classes and repair targets |
| [Changelog](CHANGELOG.md) | Release history |

Root READMEs are landing pages. Detailed tutorials live in the linked
documents, and implementation guidance lives in
[`skills/universal-diagnostic-tutor/`](skills/universal-diagnostic-tutor/).

---

## Boundaries

- No hidden memory, automatic learner profile, database, RAG/vector store, or backend infrastructure.
- No official grading claims, score guarantees, exam prediction, leaked materials, cheating, or 押题.
- No claim that every platform natively supports Skills or slash commands.
- No replacement for professional medical, legal, financial, tax, or safety advice.
- No copied textbooks, answer bank, course platform, or persistent gradebook.

Learning continuity uses one visible, user-controlled Learning State Card.
Platform adapters are prompt packaging and may be less capable than the Full
Skill.

---

## Star History

<a href="https://www.star-history.com/?repos=SenmuuuuW%2Funiversal-diagnostic-tutor-skill&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=date&theme=dark&legend=top-left&sealed_token=Q0X6xvOavsuyd8bdKza51o_UGJTUU1wlNVQuskf64hOMbT6bVMWEsD4NadjLyoMj5r7MYrppwPZuLgsk3p_qyC_eytVA3AfYFdbGRG3cTqrLBMlSbhqGHAEAT4xIeEvAuAYae7hLQRTOCPzp1KHR2F56WLs3b6tPNZWxnZTcb25l8EAUCqrK1LJLK0U_" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=date&legend=top-left&sealed_token=Q0X6xvOavsuyd8bdKza51o_UGJTUU1wlNVQuskf64hOMbT6bVMWEsD4NadjLyoMj5r7MYrppwPZuLgsk3p_qyC_eytVA3AfYFdbGRG3cTqrLBMlSbhqGHAEAT4xIeEvAuAYae7hLQRTOCPzp1KHR2F56WLs3b6tPNZWxnZTcb25l8EAUCqrK1LJLK0U_" />
   <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=date&legend=top-left&sealed_token=Q0X6xvOavsuyd8bdKza51o_UGJTUU1wlNVQuskf64hOMbT6bVMWEsD4NadjLyoMj5r7MYrppwPZuLgsk3p_qyC_eytVA3AfYFdbGRG3cTqrLBMlSbhqGHAEAT4xIeEvAuAYae7hLQRTOCPzp1KHR2F56WLs3b6tPNZWxnZTcb25l8EAUCqrK1LJLK0U_" />
 </picture>
</a>

---

## License

Released under the [MIT License](LICENSE).
