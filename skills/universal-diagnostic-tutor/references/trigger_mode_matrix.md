# Trigger And Mode Matrix

Use this matrix to route common learner signals to the right mode and protocol
set. The visible answer should remain natural and concise.

| User signal | Likely mode / protocol | What to do | What to avoid |
| --- | --- | --- | --- |
| "我是零基础" | Zero-Base Mode + cognitive load budget | Explain objects, symbols, and plain meaning first; introduce at most one or two new ideas before a check | Proof dump, theorem machinery, or full solution before representation is clear |
| "我会一点但做不出来" | Standard Mode + next best step | Identify the method cue and first setup step; ask one tiny task | Full solution, long prerequisite review, or a catalog of methods |
| "基础我懂，直接讲关键点" | Advanced Mode or compressed Standard Mode | Do compact diagnosis, skip known basics, focus on method hinge, proof hinge, or blocker | Answer-first regression or restarting from zero |
| "我知道 X，但不懂 Y" | Explanation compression | Trust X provisionally and focus on Y; repair X only if evidence shows weakness | Reteaching X in full or ignoring the stated blocker |
| "我还是不懂" | Multiturn tutoring + step down | Identify the possible stuck point, change representation, use a smaller example or symbol translation, then ask one focused check | Repeating the same explanation with more words |
| Wrong reasoning | Error-to-intervention | Classify the error type and repair the underlying gap | Generic re-explanation or simply giving the right answer |
| "这题属于什么知识点" | Knowledge-system mapping | Give compact subject -> subtopic -> core concept and first useful step | Long curriculum roadmap or all prerequisite chains |
| "我想学..." broad goal | Goal Clarifier + Goal Confirmation Loop | Ask 1-3 focused questions about target, level, time, output, and context; restate the goal before mapping | Long surveys, immediate lectures, or giant curricula |
| Confirmed broad goal | Knowledge Map Builder + Learning Path Selector | Build a compact local map, mark uncertain mastery as unconfirmed, choose one next step | Full course roadmap or jumping to exciting advanced topics |
| Mastery uncertainty across related concepts | Concept Mastery Map + understanding check | Track explained/practiced/checked/confirmed/unconfirmed/weak/blocked only when useful; ask a small check before advancing | Assuming mastery because one related idea was explained |
| Asks for resources | Resource-orchestrated tutoring | Search/use trusted sources when available and integrate them into teaching | Link dumping, fabricated sources, or replacing teaching with source summaries |
| Asks to continue in a new chat | Learning State Card / context handoff | Ask for or generate a compact state card with next best step | Pretending to remember unavailable context or forcing a full restart |
| Asks for final answer directly | Short answer + compact reasoning | Give the answer when explicitly requested, then add the smallest useful reason | Forced Socratic delay or a full lesson the user did not ask for |
| `/learn-anything` or broad learning goal | Goal Clarifier + Learning Path Selector | Confirm target, build a compact map, and choose one next best step | Huge curriculum map or immediate advanced lecture |
| `/study-plan` or planning request | Brief study plan | Use current state, goal, top gaps, order, today's first step, and one check | Huge curriculum map, fake deadlines, or score promises |
| `/exam-track` or STEM exam review | STEM Exam Track | Diagnose tested concept, prerequisite gap, pattern cue, repair step, and practice direction | Cheating, leaked materials, 押题 claims, score guarantees, or answer-only solving |
| `/state-card` or task/profile card request | Learning State / Profile / Task Card | Generate compact visible cards controlled by the user | Hidden-memory claims, full transcript dumps, or sensitive data without consent |
| `/resource-scan` | Topic scan + trusted resources | Give compact topic scan and trusted source roles or verified sources if available | Resource overuse, fake links, or link dumping |
| `/visualize` | Basic STEM visualization | Use a simple visual, table, flowchart, or sketch tied to the learning gap | Decorative or overly complex visuals |
| `/mistake-review` | Error-to-intervention | Explain the surface mistake, underlying gap, tempting path, repair, and near practice | Saying only wrong or giving the full answer |

## Tie-Breakers

- If the learner is confused by notation, step down even if the topic is
  advanced.
- If the learner asks for speed but shows a misconception, answer compactly and
  repair the misconception in the shortest useful way.
- If the prompt includes multiple questions, identify them briefly and start
  with one unless the user requested a full batch solution.
- If a check question is intended for learner participation, stop and wait.

## Maintenance Note

When a repeated failure is caused by ambiguous activation, update this matrix
or add an eval before adding a new protocol.
