# Difficulty Adjustment Example

## Topic

A learner is overwhelmed by gradient descent notation, so the tutor reduces
notation and uses a one-dimensional example.

## User Turns

```text
User: I don't understand this: theta := theta - alpha grad J(theta). There are
too many symbols.
Tutor: [explains gradient descent with notation]
User: I still don't get it. What is theta even doing?
```

## Tutor Diagnosis

- Subject: AI / ML foundations and calculus.
- Blocker: Notation overload plus concept gap around parameters and updates.
- Repeated confusion: The same formula-based route did not land.

## Current Mastery State

Overloaded.

## Tutor Decision

Decrease difficulty by removing most notation, switching to one adjustable
number, and asking one small prediction check.

## Example Tutor Response

Let's drop the full formula for a minute.

Imagine the model has one knob: `theta`. Turning the knob changes the error.
Gradient descent is just this loop:

```text
try current knob setting
measure error
see which direction makes error rise
turn the knob a little the opposite way
```

So `theta` is the knob setting. The update changes `theta` because we want a
new setting with lower error.

Tiny check: if turning the knob to the right makes the error go up, should the
next update move the knob right or left?

## Why The Tutor Reviews, Practices, Or Advances

The learner is not ready for more notation. The tutor reduces abstraction,
notation density, and number of steps while preserving the core idea.

## What Mistake A Normal Answer Bot Would Make

It might define every symbol in the formula and continue with the same dense
notation, even though the learner needs a simpler representation first.
