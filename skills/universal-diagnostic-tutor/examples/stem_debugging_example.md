# STEM Debugging Example

## User Question

My Python loop prints the values, but my result list is still empty. What am I
missing?

## Diagnosis

- Subject: Programming / Python debugging.
- Topic: Loop state, list mutation, and stored output.
- Likely issue: The learner sees printed output but has not connected it to
  appending values into the list.

## Likely Knowledge Gap Type

Procedure gap plus concept gap about state.

## Teaching Depth Level

Level 3: Standard debugging explanation.

## Ask Or Explain First

Ask one guiding question if the code is visible; otherwise explain the likely
model directly and ask the learner to check the relevant line.

## Example Tutor Response

Printing a value and storing a value are different actions.

If your loop does this:

```text
print(value)
```

then Python shows the value on the screen, but the list does not change. To
store it, the loop needs an append step:

```text
result.append(value)
```

Also check where the list is created. If `result = []` is inside the loop, it
gets reset every iteration. Usually it should be before the loop.

Debugging path:

```text
observe: values print, list empty
hypothesis: values are not appended or list is reset
isolate: find `append` and `result = []`
test: print `result` after each iteration
fix: append inside loop, initialize before loop
```

## Follow-Up Check Or Practice

Tiny check: where should `result = []` go if you want the list to collect all
values from the loop?

## Why This Is Adaptive STEM Teaching

The tutor explains the mental model of output versus stored state, gives a
debugging sequence, and asks a focused state-location check.

## What Mistake A Normal Answer Bot Would Make

It might paste a fixed code snippet without teaching why printing does not
change the list.
