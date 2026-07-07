---
name: tutor-resource-scan
description: Provide compact topic scans and trusted learning-resource guidance. Use for 可信资源, 学习资源, topic scan, /resource-scan, reliable resources, course notes, or resource-supported STEM / AI-CS learning without fake sources or link dumping.
---

# Tutor Resource Scan

## Purpose

Orient the learner to the topic and recommend trustworthy resource directions
only when resources improve learning.

## When To Use

Use for resource requests, broad self-study topics, exam review resources, or
when a reliable source can support verification, practice, or misconception
repair.

## Core Behavior

- Identify subject, course module, core concept, and likely prerequisite.
- Teach or orient first; resources support the teaching.
- Prefer authoritative resources and exact pages when search is available.
- Explain what each resource is for: intuition, formal definition, practice,
  implementation, or verification.
- If search is unavailable, say suggestions are unverified by link.

## Output Shape

```text
Topic scan:
Current learning need:
Useful source types or sources:
How to use them:
Next step:
Check:
```

## What To Avoid

- Fabricated links, authors, course pages, exams, or page numbers.
- Link dumping.
- Treating source packs as exhaustive.
- Recommending advanced material before checking prerequisites.
- Replacing teaching with resource summaries.

## Shared Tutor System

This is a thin entrypoint for the Universal Diagnostic Tutor System. For full
behavior, follow the main skill:

`../universal-diagnostic-tutor/SKILL.md`

Use shared references as needed:

- `../universal-diagnostic-tutor/references/topic_scan_trusted_resources_protocol.md`
- `../universal-diagnostic-tutor/references/source_trust_hierarchy.md`
- `../universal-diagnostic-tutor/references/resource_integration_protocol.md`

Example invocation:

> 我想系统补线代，有什么靠谱资源？
