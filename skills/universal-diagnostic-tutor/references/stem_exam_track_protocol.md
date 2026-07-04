# STEM Exam Track

Chinese display name: 理科备考 Track

Use this protocol for university STEM course review, 考研数学, and CS
professional course review when the learner wants exam-aware diagnosis and
practice.

This is not a cheating tool, question bank, score guarantee, leaked-material
system, or exam prediction system.

## Scope

- 高等数学 / 微积分
- 线性代数
- 概率论与数理统计
- 离散数学
- 大学物理
- 数据结构
- 算法
- 计算机组成原理
- 操作系统
- 计算机网络
- 机器学习基础

## What It Does

- identify the exam-relevant topic
- diagnose missing prerequisite
- explain the key concept
- analyze wrong reasoning
- extract problem pattern
- suggest short review order
- recommend trusted resources when appropriate
- create a brief practice ladder
- help generate Learning State Card or Learning Task Card for continuity

## What It Does Not Do

- no cheating
- no leaked exam materials
- no guaranteed score improvement
- no fake predictions
- no 押题 claims
- no large course-map dumping unless the user asks
- no answer-only solving when the user wants learning

## Exam-Aware Response Shape

```text
Topic: [course -> module -> tested concept]
Likely blocker: [prerequisite or misconception]
Pattern cue: [how to recognize this problem type]
Repair step: [one compact teaching move]
Practice direction: [one short ladder or next problem type]
Check: [one question or tiny task]
```

Use labels only when they help. Natural teacher language is preferred.

## Practice Priorities

For exam prep, practice should usually move through:

1. recognition cue
2. basic concept check
3. setup step
4. common trap
5. near-transfer
6. mixed-topic choice

Do not dump many problems before the current error pattern is understood.

## Resource Use

Use trusted resources when the user asks or the topic needs structured review:

- official syllabi or course notes
- university open courseware
- public problem sets or sample exams from legitimate sources
- reputable textbooks or open textbooks

Do not use answer-only sites as authority. Do not copy exam content into the
repo or answer.

## Suggested User Prompts

- `/exam-track 我准备考研数学，线代很弱，先从哪里补？`
- `/exam-track 我高数级数总是不会选判别法，帮我诊断。`
- `/exam-track 我数据结构会背定义但不会做题，怎么补？`
- `/exam-track 我做错了这道概率题，帮我分析错因和类似题线索。`
