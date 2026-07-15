<div align="center">

# 🧠 Universal Diagnostic Tutor Skill

**A diagnosis-first STEM / AI-CS tutor skill that finds the learner's current knowledge gap before teaching.**

English | [中文](README.zh-CN.md)

[User Guide](USER_GUIDE.md) · [Command Surface](COMMAND_SURFACE.md) · [Examples](EXAMPLES.md) · [Changelog](CHANGELOG.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-2f6f4e.svg)](LICENSE)
![Markdown only](https://img.shields.io/badge/Markdown-only-555555.svg)
![Focus: STEM and AI-CS](https://img.shields.io/badge/Focus-STEM%20%2F%20AI--CS-1f6feb.svg)
![V1.9 Practice and Mastery](https://img.shields.io/badge/V1.9-Practice%20%26%20Mastery-b78300.svg)
[![GitHub stars](https://img.shields.io/github/stars/SenmuuuuW/universal-diagnostic-tutor-skill?style=flat)](https://github.com/SenmuuuuW/universal-diagnostic-tutor-skill/stargazers)

</div>

Universal Diagnostic Tutor Skill is a Markdown-only AI tutor behavior layer for
STEM, mathematics, programming, AI/CS, and exam review. It diagnoses the
learner's gap, chooses the next best teaching step, and checks evidence before
advancing.

> **The difference:** it is not answer-first. It identifies the subject,
> concept, prerequisite, notation, method, or reasoning gap before choosing a
> compact teaching move. It is not a course platform, database, RAG system, or
> hidden-memory service.

## 🚀 Quick Start

| Where you use AI | Start here |
| --- | --- |
| Ordinary ChatGPT, Gemini, DeepSeek, Doubao, Kimi, or Qwen chat | Copy the [Lite Prompt](platforms/generic-chat/TUTOR_LITE_PROMPT.md) |
| Codex or Claude Code-style agent | Use the [Full Skill](skills/universal-diagnostic-tutor/) and follow the [install guide](INSTALL.md) |
| Codex with visible Skill entrypoints | Choose the most relevant `tutor-*` entrypoint |
| Custom bot or API prompt | Choose an adapter in [Portability](PORTABILITY.md) |

New to the project? Read the [User Guide](USER_GUIDE.md). Installation and
updates live in [INSTALL.md](INSTALL.md), while entrypoint details live in
[COMMAND_SURFACE.md](COMMAND_SURFACE.md).

## ✨ Core Capabilities

| Capability | What it does |
| --- | --- |
| Diagnosis-first tutoring | Locates the subject, concept, prerequisite, notation, method, or reasoning gap |
| Learning Architecture | Clarifies broad goals, builds a compact knowledge map, and selects one next step |
| Practice & Mastery Loop | Generates targeted practice, waits for an answer, grades qualitatively, repairs mistakes, and checks readiness |
| Skill entrypoints | Exposes focused `tutor-*` doors into one shared Tutor system |
| STEM Exam Track | Supports university STEM, postgraduate math, and CS review without prediction or score promises |
| Topic Scan + Trusted Resources | Uses reliable learning resources when they improve the current teaching step |
| Knowledge Link Cards | Explains one to three strongly related concepts when they block the current task |
| Learning State Cards | Creates visible, copyable checkpoints for continuation without hidden memory |
| Cross-platform adapters | Packages smaller prompt versions for custom bots, ordinary chat, and API-style use |

The strongest current coverage is university-level STEM and AI-CS: calculus,
linear algebra, probability, discrete mathematics, programming, algorithms,
machine learning, systems, networks, physics, signals, and engineering
foundations. The Tutor remains useful across other learning domains, but it is
not positioned as a generic answer bot.

## 🧭 Skill Entrypoints

| Need | Use |
| --- | --- |
| General tutoring | `universal-diagnostic-tutor` |
| Broad learning goal | `tutor-learn-anything` |
| Study plan | `tutor-study-plan` |
| Practice / grading / readiness | `tutor-practice` |
| Exam review | `tutor-exam-track` |
| Gap diagnosis | `tutor-diagnose-gap` |
| Mistake analysis | `tutor-mistake-review` |
| State cards | `tutor-state-card` |
| Resources | `tutor-resource-scan` |
| Visual learning | `tutor-visualize` |

These are thin entrypoints into the same canonical Tutor system. Slash-style
text such as `/practice` and `/study-plan` expresses intent; it is not a
guaranteed native command in every host. See the
[Command Surface](COMMAND_SURFACE.md) for practical examples.

## 🔍 How It Works

```text
Goal clarification -> Knowledge map -> Teach one concept -> Practice
-> Learner answer -> Qualitative grading -> Mistake repair
-> Visible state update -> Readiness decision -> Next step
```

The full chain is used only when the learner needs it. A quick factual question
does not trigger a giant workflow, and a practice turn normally stops after one
targeted exercise to wait for the learner's answer.

## ✅ V1.9 Practice & Mastery Loop

V1.9 closes the gap between explanation and demonstrated understanding. The
Tutor can generate one targeted exercise, wait for the learner's attempt,
preserve correct reasoning, identify the earliest meaningful mistake, select a
focused repair, update visible learning state when useful, and decide whether
to advance, review, step down, diagnose again, or continue practicing.

Readiness is evidence-based. An explanation or one lucky correct answer does
not establish mastery. Knowledge Link Cards are limited to strongly related
blocking concepts and usually contain only one to three compact cards.

## Example

Instead of immediately solving a vector problem, the Tutor first distinguishes
"parallel" from "equal components," identifies scalar multiples as the missing
idea, teaches one compact step, and asks the learner to apply it before moving
on. See [EXAMPLES.md](EXAMPLES.md) for concise comparisons and teaching flows.

## ⭐ Star History

<a href="https://www.star-history.com/?repos=SenmuuuuW%2Funiversal-diagnostic-tutor-skill&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=date&theme=dark&legend=top-left&sealed_token=Q0X6xvOavsuyd8bdKza51o_UGJTUU1wlNVQuskf64hOMbT6bVMWEsD4NadjLyoMj5r7MYrppwPZuLgsk3p_qyC_eytVA3AfYFdbGRG3cTqrLBMlSbhqGHAEAT4xIeEvAuAYae7hLQRTOCPzp1KHR2F56WLs3b6tPNZWxnZTcb25l8EAUCqrK1LJLK0U_" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=date&legend=top-left&sealed_token=Q0X6xvOavsuyd8bdKza51o_UGJTUU1wlNVQuskf64hOMbT6bVMWEsD4NadjLyoMj5r7MYrppwPZuLgsk3p_qyC_eytVA3AfYFdbGRG3cTqrLBMlSbhqGHAEAT4xIeEvAuAYae7hLQRTOCPzp1KHR2F56WLs3b6tPNZWxnZTcb25l8EAUCqrK1LJLK0U_" />
   <img alt="Star History Chart" src="https://api.star-history.com/chart?repos=SenmuuuuW/universal-diagnostic-tutor-skill&type=date&legend=top-left&sealed_token=Q0X6xvOavsuyd8bdKza51o_UGJTUU1wlNVQuskf64hOMbT6bVMWEsD4NadjLyoMj5r7MYrppwPZuLgsk3p_qyC_eytVA3AfYFdbGRG3cTqrLBMlSbhqGHAEAT4xIeEvAuAYae7hLQRTOCPzp1KHR2F56WLs3b6tPNZWxnZTcb25l8EAUCqrK1LJLK0U_" />
 </picture>
</a>


## 📚 Documentation

| Document | Purpose |
| --- | --- |
| [User Guide](USER_GUIDE.md) | Beginner-friendly setup and usage tutorial |
| [Command Surface](COMMAND_SURFACE.md) | Tutor entrypoints and text shortcuts |
| [Install](INSTALL.md) | Installation, updates, and copied-Skill synchronization |
| [Portability](PORTABILITY.md) | Full Skill, custom bot, Lite Prompt, and API prompt choices |
| [Examples](EXAMPLES.md) | Short public examples of diagnosis-first tutoring |
| [Evaluations](EVALS.md) | Behavioral evaluation cases |
| [Quality Rubric](QUALITY_RUBRIC.md) | Scoring criteria for tutoring quality |
| [Failure Taxonomy](FAILURE_TAXONOMY.md) | Known failure classes and repair targets |
| [Changelog](CHANGELOG.md) | Release history |

The root READMEs are landing pages. Detailed tutorials belong in the linked
documents, and implementation guidance remains in
[`skills/universal-diagnostic-tutor/`](skills/universal-diagnostic-tutor/).

## 🛡️ Boundaries

- No hidden memory, automatic learner profile, database, RAG/vector store, or backend infrastructure.
- No official grading claims, score guarantees, exam prediction, leaked materials, cheating, or 押题.
- No claim that every platform natively supports Skills or slash commands.
- No replacement for professional medical, legal, financial, tax, or safety advice.
- No copied textbooks, answer bank, course platform, or persistent gradebook.

Learning continuity uses visible, user-controlled Learning State, Profile, and
Task Cards. Platform adapters are prompt packaging and may be less capable than
the Full Skill.

## 📄 License

Released under the [MIT License](LICENSE).
