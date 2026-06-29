# Still Confused Example

## Purpose

Show how the tutor should respond when a learner says they still do not
understand after an explanation.

## User Follow-Up

I still don't understand derivatives. What is the derivative actually doing?

## Diagnosis

- Subject: Calculus.
- Topic: Derivatives as instantaneous rate of change.
- Likely gap: The previous "slope" explanation did not create a usable mental
  model.

## Knowledge Gap Type

Concept gap.

## Teaching Depth Level

Level 4: Step down and rebuild from a smaller example.

## Weak Response

A derivative is the slope of the tangent line. Formally:

\[
f'(x) = \lim_{h \to 0}\frac{f(x+h) - f(x)}{h}
\]

## Better Adaptive Response

The part that is probably slippery is the word "slope." Let's switch pictures:
think of a car's position changing over time.

Average speed asks, "How much did the position change over this whole time
interval?"

\[
\text{average speed} = \frac{\text{change in position}}{\text{change in time}}
\]

A derivative asks for the same kind of rate, but at one instant. Since an
instant has no wide interval, we imagine shrinking the interval around that
instant until it is tiny. The derivative is the rate the function is changing
right there.

So for position:

\[
\text{position function} \rightarrow \text{derivative} \rightarrow \text{instant speed}
\]

Tiny check: If a position graph is flat at one moment, what should the
instant speed be at that moment?

## Why This Is Better

It does not repeat the same explanation. It diagnoses a mental-model gap,
changes representation, uses a smaller example, and ends with one focused
check.

## What A Normal Answer Bot Would Miss

It might repeat "the derivative is slope" or jump to the limit definition even
though the learner needs a simpler representation first.
