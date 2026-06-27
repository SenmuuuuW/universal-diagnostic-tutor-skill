# Mistake Analysis Teaching Example

## User Question

A test for a disease is 99% accurate. I said that if someone tests positive,
there is a 99% chance they have the disease. Why is that wrong?

## Diagnosis

- Subject: Probability / statistics.
- Topic: Conditional probability and base rates.
- Likely gap: The learner is using intuition about test accuracy instead of
  conditioning on all people who tested positive.

## Knowledge Gap Type

Misconception gap plus reasoning gap.

## Teaching Depth Level

Level 4: Foundation-first full explanation.

## Example Tutor Response

Your answer is tempting because "99% accurate" sounds like it should directly
become "99% chance." The hidden issue is that the test result is not the only
information that matters. We also need to know how common the disease is.

Imagine 10,000 people and the disease is rare: 1% have it.

```text
100 people have the disease
9,900 people do not have it
```

If the test catches 99% of sick people, about 99 sick people test positive. If
the test also has a 1% false-positive rate, about 99 healthy people test
positive too.

So among positive tests:

```text
99 true positives / (99 true positives + 99 false positives) = 1/2
```

In this example, a positive test means about a 50% chance, not 99%. The wrong
path felt reasonable because it ignored the healthy people who can also test
positive.

Prevention rule: when you see "probability after evidence," ask "out of all
cases with this evidence, how many come from each group?"

## Follow-Up Check Or Practice

Near-match practice: If a disease affects 10% of people and the same test has
99% sensitivity and a 1% false-positive rate, would the chance after a positive
test be higher or lower than 50%? Why?

## Why This Is Adaptive Teaching

The response identifies the surface mistake, repairs the base-rate
misconception with concrete counts, explains why the wrong intuition was
tempting, and gives a similar but changed practice item.

## What A Normal Answer Bot Would Miss

It might only say "use Bayes' theorem" or provide a formula, leaving the
learner with the same intuition problem.
