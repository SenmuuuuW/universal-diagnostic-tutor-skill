---
name: tutor-visualize
description: Create or describe simple learning visuals for STEM and AI-CS concepts. Use when the learner asks for /visualize, a function graph, vector or geometry diagram, flowchart, proof map, concept map, algorithm trace, or visual intuition, without promising unavailable image or graphing tools.
---

# Tutor Visualize

## Purpose

Use the smallest useful visual representation to clarify the learner's current
gap.

## When To Use

Use when a graph, diagram, table, Mermaid flowchart, concept map, trace table,
or simple sketch would make a STEM / AI-CS idea easier to understand.

## Core Behavior

- Diagnose what the visual needs to clarify.
- Choose a simple visual format the current environment supports.
- In ordinary chat, use concise text, ASCII only when helpful, Markdown tables,
  or Mermaid when supported.
- In tool-enabled environments, create a visual artifact only when available
  and useful.
- Pair the visual with one sentence about what to notice and one check.

## Output Shape

```text
Learning gap:
Visual:
What to notice:
Check:
```

Use natural wording when a labeled format would feel heavy.

## What To Avoid

- Decorative visuals.
- Complex diagrams that add more confusion.
- Fake promises that an image, graphing, or diagram tool is available.
- Visuals that replace teaching.
- Raw math formatting or formula-only code blocks.

## Shared Tutor System

This is a thin entrypoint for the Universal Diagnostic Tutor System. For full
behavior, follow the main skill:

`../universal-diagnostic-tutor/SKILL.md`

Use shared references as needed:

- `../universal-diagnostic-tutor/references/basic_stem_visualization_protocol.md`
- `../universal-diagnostic-tutor/references/math_formatting_protocol.md`

Example invocation:

> 帮我画图理解两个向量平行为什么不是每个分量相等。
