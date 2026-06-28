# STEM Physics Signal Example

## User Question

How does a physical signal become digital data?

## Diagnosis

- Subject: Physics / electronics / signals.
- Topic: Measurement, sampling, quantization, and digital representation.
- Likely issue: The learner needs the bridge from physical phenomenon to
  sensor voltage to numbers.

## Likely Knowledge Gap Type

Concept gap plus notation/measurement gap.

## Teaching Depth Level

Level 4: Foundation-first physical-to-digital explanation.

## Ask Or Explain First

Explain first. The learner is asking for the pathway, so start with the
phenomenon before asking about equations.

## Example Tutor Response

Start with the physical thing: temperature, sound pressure, light intensity, or
motion. A sensor converts that physical quantity into an electrical signal,
usually a changing voltage.

Then the computer needs two steps:

1. **Sampling:** measure the signal at separate moments in time.
2. **Quantization:** round each measurement to one of the allowed digital
   values.

So the path is:

```text
physical phenomenon -> sensor -> analog voltage -> samples -> digital numbers
```

The important idea is that digital data is not the physical signal itself. It
is a sequence of measured, rounded values that represents the signal.

Common mistake: thinking higher sampling always fixes everything. Sampling rate
helps with time detail, but sensor quality, noise, filtering, and quantization
also matter.

## Follow-Up Check Or Practice

Tiny check: which step turns a continuous changing voltage into values measured
at separate times: sampling or quantization?

## Why This Is Adaptive STEM Teaching

The tutor starts with the phenomenon, then connects sensor behavior,
measurement, sampling, quantization, and representation before using technical
terms heavily.

## What Mistake A Normal Answer Bot Would Make

It might jump straight to formulas or ADC jargon without explaining what is
being measured and represented.
