# Lesson Block Contract

Use this file only when the environment exposes a **structured lesson surface**:
a runtime that stores lesson blocks and offers a way to write them (for example
`udt_lesson_update`). The chat remains the classroom; the lesson surface is a
compact reference snapshot of the unit just taught. Never dump a whole lecture
into the block surface.

The teaching brain still decides what to teach, in what order, and what counts
as evidence. The runtime only validates, stores, renders and records. Never
invent a block type, a citation, or a runtime decision.

## Capability Detection

Look for capabilities, not a product name:

| Capability | Shape | Use |
| --- | --- | --- |
| Structured lesson write | A tool that accepts a lesson title and an ordered block list | Write the same unit you just taught in the chat |
| Source read | A tool that returns a stored source by id | Read before citing; never invent a source id |
| Source list | Metadata only, no body | Know what can be cited |
| Lesson surface | One block at a time, with learner-driven Continue | Keep each block small and self-contained |

If the capability is absent, teach exactly as before and do not mention the
absence or the runtime.

## Non-Negotiables

- **Chat teaches; blocks support.** The learner should be able to read the block
  surface as a short reference, not as a second lecture.
- **One small unit per write.** At most six blocks per `udt_lesson_update` call
  and 24 per lesson. Prefer four to six blocks for a real unit, including one
  check or quiz.
- **One screen, one idea.** Every block must be readable without scrolling far.
- **No arbitrary code or remote content.** Only the block types and fields
  below. SVG is sanitized; scripts, event handlers, external URLs, images and
  `foreignObject` are removed.
- **Append one complex block at a time.** A `figure` (inline SVG), or a mixed
  update containing several rich blocks, is more likely to exceed a model's
  tool-input budget and be rejected as malformed JSON. Write one such block per
  call, then verify it before appending the next. This is a delivery strategy,
  not a schema rule.
- **No source fabrication.** Every `sourceRefs` entry must point to a source
  that actually exists and was read.
- **No mastery claim.** A completed block, a moved slider or a view is not
  evidence of mastery.

## Block Selection

Choose for the teaching purpose, not for visual variety.

| Purpose | Block | Use it when | Avoid it when |
| --- | --- | --- | --- |
| Explain a concept in prose | `text` | A short explanation, definition, or worked reasoning | The prose is a full lecture |
| Show a worked process | `example` | A small multi-step worked example with a takeaway | A long solution dump |
| Show spatial/structural relations | `diagram` or `figure` | A shape, flow, graph, geometry, architecture, or labeled structure | Decoration or a picture that replaces reasoning |
| State a formula | `formula` | The formula is the object being taught | A formula is incidental |
| Show real code | `code` | Readable source with meaning | The learner should execute arbitrary code |
| Compare choices | `comparison` | Two or three designs, methods or interpretations | A long table that is not the lesson |
| Point to a source | `resource` | A cited reading or reference | Link dumping |
| Explore one parameter | `slider` | A visible result changes meaningfully with one safe parameter | The graph is decorative or the relationship is trivial |
| Pace a process | `step-through` | The learner needs to inspect one frame at a time | A short ordered list is enough |
| Check reasoning in chat | `check` | The tutor wants the learner to explain in the conversation | A recorded multiple-choice answer is the point |
| Record an inline answer | `quiz` | A quick multiple-choice or short answer should be recorded by the runtime | The answer needs qualitative teaching judgement |
| Schedule recall | `flashcard` | A fact should become a review card | The item is a full explanation |
| Safe custom visual | `figure` | A sanitized inline SVG makes the relation clearer | A text explanation is clearer |

### Slider

Use a slider only when one safe parameter produces a visibly meaningful change:

- the learner can form a prediction before dragging;
- the result is visible in the same block;
- the minimum, maximum and initial value are inside the teaching range;
- the expression is one variable, `x`, using only:
  `+ - * / ^`, parentheses, numbers, `x`, `pi`, `e`, and
  `sin cos tan sqrt abs exp log ln floor ceil round pow min max`;
- the block does not record an answer, grade the learner, or advance the lesson.

Do not use a slider for an animation that does not depend on a learner action.

### Step-Through

Use step-through for a process where the **order** carries meaning:

- 2–12 frames;
- each frame has one small idea and a short body;
- the learner controls previous/next;
- the runtime never auto-advances;
- do not hide the final result behind a cheat or an untracked action.

Do not use step-through for a simple three-item list; use `example` or `text`.

### Figure

Use inline SVG only for a relation that is genuinely visual:

- geometry, vectors, curves, flow, architecture, matrices, labeled systems;
- include `alt` text that says what the figure teaches;
- keep shapes and labels legible at sidebar width;
- no scripts, event handlers, external URLs, `<image>`, `<use>`, `<a>`,
  `foreignObject`, `style` attributes, or remote references;
- allowed tags are `svg`, `g`, `defs`, `title`, `desc`, `linearGradient`,
  `radialGradient`, `stop`, `path`, `circle`, `ellipse`, `rect`, `line`,
  `polyline`, `polygon`, `text`, `tspan`;
- allowed attributes include `viewBox`, `width`, `height`, `fill`, `stroke`,
  `stroke-width`, `d`, `cx`, `cy`, `r`, `x`, `y`, `points`, `transform`,
  `opacity`, font attributes, gradient attributes and local `url(#id)`;
- animation is limited to `none`, `fade`, `pulse` or `draw`.

### `check` vs `quiz`

- `check` is an invitation to answer in the chat. It has `prompt`, optional
  `expect` (`reasoning` or `answer`) and optional `hint`. It does not record a
  machine answer.
- `quiz` is an inline recorded submission. It has 1–8 questions, each with an
  id, kind (`mcq` or `short`), prompt, and either 2–8 options or a short-answer
  field. `answer`, `rubric` and `explanation` may be stored for the tutor but
  must never be rendered before judgement.
- Use `quiz` only when recording the response is pedagogically useful. Use
  `check` when the tutor needs the learner's own words in the conversation.

## Envelope

Every block has the same envelope:

```json
{
  "id": "stable-block-id",
  "type": "one-of-the-supported-types",
  "content": {},
  "sourceRefs": [{ "sourceId": "existing-source-id", "locator": "section or page" }]
}
```

- `id`: unique within the lesson, 1–120 characters.
- `sourceRefs`: optional, at most 6; omit rather than invent. `locator` is a
  page, heading, line range or URL fragment, at most 300 characters.
- Unknown fields are rejected by the runtime. Use only the fields below.

## Content Shapes and Limits

All limits are hard runtime limits; stay well inside them.

### `text`

```json
{ "md": "Short markdown. Math as \\(...\\) or \\[...\\]." }
```

- `md` required, 1–6000 characters.
- Prefer 1–3 short paragraphs. Do not write a chapter.

### `example`

```json
{ "title": "A small worked example", "steps": ["First step", "Second step"], "takeaway": "One sentence." }
```

- `title` 1–200; `steps` 1–12 entries, each 1–400; optional `takeaway` 1–400.

### `diagram`

```json
{ "format": "ascii", "spec": "...", "caption": "Optional." }
```

- `format` `ascii` or `mermaid`; `spec` 1–4000; `caption` 1–200.
- Mermaid may be carried but a client without a renderer shows source text; do
  not rely on it for essential meaning.

### `formula`

```json
{ "tex": "x^2 + 1", "display": true, "caption": "Optional." }
```

- `tex` 1–2000; `display` optional; `caption` 1–200.
- Use TeX without `$` delimiters.

### `code`

```json
{ "language": "python", "source": "print(1)", "caption": "Optional." }
```

- `language` 1–40 optional; `source` 1–6000; `caption` 1–200.
- Code is displayed as text; the runtime does not execute it.

### `quiz`

```json
{
  "title": "Quick check",
  "questions": [
    {
      "id": "q1",
      "kind": "mcq",
      "prompt": "Which shape?",
      "options": ["(4, 3)", "(3,)"],
      "answer": "(4, 3)",
      "rubric": "Optional",
      "explanation": "Optional"
    }
  ]
}
```

- 1–8 questions; IDs unique; MCQ needs 2–8 unique options; prompt 1–1000;
  stored answer/rubric/explanation 1–2000. Never reveal stored answers before
  the learner submits.

### `flashcard`

```json
{ "front": "Question", "back": "Answer", "tags": ["optional"] }
```

- `front` and `back` 1–2000; at most 8 tags, each 1–40.

### `resource`

```json
{ "title": "Reading", "sourceId": "existing-source-id", "locator": "section 2.1", "url": "optional text", "note": "Why read it." }
```

- `title` 1–200; `sourceId`/`locator` optional; `url` is display text only and
  is not fetched; `note` 1–500.
- A `resource` with a `sourceId` must reference a source that exists.

### `comparison`

```json
{ "columns": ["A", "B"], "rows": [["1", "2"]], "caption": "Optional." }
```

- 1–8 columns; 1–20 rows; every row has one cell per column; each cell at most
  500 characters; `caption` 1–200.

### `slider`

```json
{
  "title": "Explore the loss",
  "prompt": "Drag x and watch the value.",
  "expression": "(x - 3)^2",
  "min": 0,
  "max": 6,
  "step": 0.1,
  "initial": 1.5,
  "unit": "optional",
  "caption": "Optional."
}
```

- `expression` required, 1–240, safe single-variable `x` expression;
- `min`, `max`, `step`, `initial` required finite numbers; `max > min`;
  `initial` inside the range; `step > 0`;
- `title` 1–200; `prompt` 1–1000; `unit` 1–40; `caption` 1–200.
- Never use arbitrary JavaScript, property access, assignments, or `eval`.

### `step-through`

```json
{
  "title": "Follow one update",
  "prompt": "Advance one frame at a time.",
  "frames": [
    { "title": "Start", "body": "First frame." },
    { "title": "Move", "body": "Second frame." }
  ],
  "caption": "Optional."
}
```

- 2–12 frames; frame `body` 1–2000; frame `title` 1–200; optional `math`
  fragments are host-rendered; `title`/`prompt` 1–200/1000; `caption` 1–200.

### `figure`

```json
{
  "title": "A line through points",
  "alt": "A straight line fitted through observed points.",
  "svg": "<svg viewBox=\"0 0 360 180\"><line x1=\"30\" y1=\"150\" x2=\"330\" y2=\"150\" stroke=\"#ddd\"/><path d=\"M30 130 L330 50\" fill=\"none\" stroke=\"#2563eb\"/></svg>",
  "caption": "A prediction is not a causal claim.",
  "animation": "draw"
}
```

- `alt` required, 1–300; `svg` required, 1–20,000; `title`/`caption` 1–200;
  `animation` `none`, `fade`, `pulse` or `draw`.
- The SVG is sanitized. Do not use external resources, scripts or handlers.

## Complete Lesson Examples

These are lesson blocks, not full chat lectures. Each is a reference snapshot
for a unit the tutor already taught in the conversation. They are complete
arrays for review, not a recommendation to send every block in one tool call:
for a real lesson, append one block (and especially one `figure`) at a time.

### Mathematics — derivative as a local rate

```json
[
  { "id": "m1", "type": "text", "content": { "md": "For \\(L(w)=(w-3)^2\\), the derivative \\(2(w-3)\\) tells you the direction and sensitivity of a small change." } },
  { "id": "m2", "type": "slider", "content": { "title": "Loss near the minimum", "prompt": "Move w and watch both the value and the slope.", "expression": "(x - 3)^2", "min": 0, "max": 6, "step": 0.1, "initial": 1.5, "caption": "The minimum is at w = 3." } },
  { "id": "m3", "type": "step-through", "content": { "title": "One descent step", "frames": [{ "title": "Read the slope", "body": "At w = 1.5, the derivative is negative, so increasing w lowers the loss." }, { "title": "Take a step", "body": "Subtract a fraction of the derivative: a small step moves toward w = 3." }, { "title": "Check the result", "body": "The new loss is smaller; a too-large step could overshoot." }] } },
  { "id": "m4", "type": "check", "content": { "prompt": "At w = 4, which direction should a small descent step move? What in the derivative tells you that?", "expect": "reasoning", "hint": "Look at the sign of 2(w − 3)." } }
]
```

### Physics — a falling object and velocity

```json
[
  { "id": "p1", "type": "text", "content": { "md": "Under constant acceleration, velocity changes linearly with time while position changes quadratically." } },
  { "id": "p2", "type": "figure", "content": { "title": "Velocity over time", "alt": "A straight line rising from the origin, showing constant positive acceleration.", "svg": "<svg viewBox=\"0 0 360 180\"><line x1=\"30\" y1=\"150\" x2=\"330\" y2=\"150\" stroke=\"#d7dbe2\"/><line x1=\"30\" y1=\"150\" x2=\"30\" y2=\"20\" stroke=\"#d7dbe2\"/><path d=\"M30 140 L300 35\" fill=\"none\" stroke=\"#2563eb\" stroke-width=\"3\"/><text x=\"40\" y=\"28\" font-size=\"11\" fill=\"#6b7280\">v = at</text></svg>", "caption": "The slope is acceleration; the area under the line is displacement." } },
  { "id": "p3", "type": "step-through", "content": { "title": "Read the motion graph", "frames": [{ "title": "Start at rest", "body": "At t = 0, v = 0 and the object starts to speed up." }, { "title": "Equal time, equal change", "body": "Each second adds the same amount to velocity." }, { "title": "Area matters", "body": "Area under the velocity graph gives displacement, not velocity." }] } },
  { "id": "p4", "type": "quiz", "content": { "title": "Graph reading", "questions": [{ "id": "q1", "kind": "mcq", "prompt": "What does the slope of a v–t graph represent?", "options": ["Acceleration", "Displacement", "Mass"], "answer": "Acceleration", "explanation": "Slope is change in velocity over time." }] } }
]
```

### Computer science — binary search bounds

```json
[
  { "id": "c1", "type": "text", "content": { "md": "Binary search keeps a half-open interval `[lo, hi)` and discards the half that cannot contain the target." } },
  { "id": "c2", "type": "code", "content": { "language": "python", "source": "lo, hi = 0, len(a)\nwhile lo < hi:\n    mid = (lo + hi) // 2\n    if a[mid] < target:\n        lo = mid + 1\n    else:\n        hi = mid\nreturn lo" } },
  { "id": "c3", "type": "step-through", "content": { "title": "One comparison", "frames": [{ "title": "Choose mid", "body": "The interval is half-open; `hi` is not included." }, { "title": "Discard a half", "body": "If `a[mid]` is too small, the answer cannot be at or below `mid`." }, { "title": "Stop", "body": "When `lo == hi`, the interval is empty and `lo` is the insertion point." }] } },
  { "id": "c4", "type": "quiz", "content": { "title": "Boundary check", "questions": [{ "id": "q1", "kind": "mcq", "prompt": "Why use `hi = mid` rather than `hi = mid - 1`?", "options": ["Because `hi` is exclusive", "Because the array is sorted", "Because Python indexes from zero"], "answer": "Because `hi` is exclusive", "rubric": "Explain the half-open invariant." }] } }
]
```

## Source Citations

- Read the source with the runtime's source-read capability before citing it.
- `sourceRefs` must use the real `sourceId` and a useful `locator`:
  ```json
  { "sourceRefs": [{ "sourceId": "src_...", "locator": "chapter 3, page 42" }] }
  ```
- Cite only what supports the block's claim. Do not cite a source merely to make
  the block look researched.
- If no source is available, omit `sourceRefs`; never invent a source id,
  title, author or URL.

## Failure Repair

- A schema error names the block and field. Fix that field and resend; do not
  send the same malformed block again.
- If a visual is rejected or cannot be made safe, fall back to `text`,
  `example`, or `formula`. Do not replace a teaching idea with a decorative
  block.
- Do not reduce a whole lesson to a single text block merely because one block
  failed. Keep the unit small and re-write only the failed block.
- If the runtime reports that a source is unknown, remove that citation or
  read the source first; do not fabricate an id.
- If the runtime reports an unknown block type, use only the types listed here.
- If a rich multi-block update is rejected as malformed JSON, do not retry the
  same payload. Split it: one small block per call, figure/SVG alone. Keep the
  chat and block surface consistent while appending the rest.
- Keep the chat and the block surface consistent: if the chat teaches a
  correction, rewrite or append the relevant block rather than leaving a
  contradictory reference.

## Boundary

- The Skill decides the teaching sequence, block choice, wording, check and
  readiness.
- The Runtime validates, stores, renders and records. It never decides that a
  learner is ready, never marks mastery, and never advances the lesson.
- A slider drag, a step-through view, or a completed block is **not** evidence
  of mastery. Only the learner's actual answers, explanations or transfers can
  become evidence.
- Never narrate the block write, tool names, schema or runtime internals to the
  learner. The learner sees teaching and a reference surface, not the machinery.
