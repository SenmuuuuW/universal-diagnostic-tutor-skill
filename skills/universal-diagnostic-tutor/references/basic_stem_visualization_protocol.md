# Basic STEM Visualization Protocol

Use this protocol when a simple visual would clarify the learner's current gap.

This project does not add image-generation code, graphing scripts, or diagram
infrastructure. The protocol only tells the tutor when and how to use visuals
available in the host environment, or how to describe a simple visual in text.

## Supported Visual Types

- function graph
- geometry diagram
- vector relationship diagram
- matrix transformation sketch
- number line
- flowchart
- concept map
- proof structure map
- algorithm trace table
- state transition diagram
- probability tree
- signal/sampling sketch

## When To Use A Visual

Use a visual when it helps with:

- direction, shape, or transformation
- symbol-to-object meaning
- algorithm state changes
- probability branches
- proof structure
- time/frequency or signal intuition
- overloaded notation that needs a simpler representation

Do not use visuals just to look polished.

## How To Visualize By Environment

- **Ordinary chat:** describe the visual, use ASCII sparingly, or use Markdown
  tables.
- **Markdown platforms:** use Mermaid for flowcharts or concept maps when it is
  supported.
- **Agent environments with image, HTML, or diagram tools:** create a small
  educational visual artifact only if it materially helps.

Always connect the visual to the current learning gap.

## Visual Rules

- Keep the visual simple.
- Label the key objects.
- Use correct notation.
- Avoid complex graphs when a small sketch works.
- Pair the visual with one sentence explaining what to notice.
- Ask one check after the visual when learning participation matters.
- If asking an AI image tool to create a visual, request a clean educational
  diagram with labels, not decorative art.

## Examples

- Function graph: show slope / derivative intuition.
- Geometry: label angles, sides, known relations, and unknowns.
- Vector: show \(v\), \(2v\), and direction preservation.
- Flowchart: show binary search invariant or recursion base/recursive cases.
- Concept map: connect gradient descent to loss, parameter, gradient, and
  update.
- Algorithm trace table: show variable changes per loop iteration.

## Anti-Patterns

- Creating a visual before diagnosing the learning gap.
- Using a diagram that contains more new terms than the explanation.
- Treating a visual as a replacement for teaching.
- Making a polished artifact when a two-line sketch would teach better.
