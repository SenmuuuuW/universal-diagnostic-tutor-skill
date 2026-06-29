# Error To Intervention Binary Search Example

## Scenario

The learner says:

"Binary search is correct because it checks the middle every time and keeps
halving the array, so eventually it finds the target."

## Expected Tutor Behavior

- Identify the error as a proof error, not a code-tracing problem.
- Preserve the useful termination intuition.
- Teach the missing invariant.
- Avoid re-explaining the whole algorithm.
- Ask one proof-hinge check.

## Example Tutor Response

你说的“不断减半”解释了为什么它会很快结束，这部分是对的。

但 correctness proof 还缺一个关键点：为什么我们丢掉的一半一定不可能含有答案？这个关键点叫 **invariant（不变量）**。

对 binary search，核心不变量是：

> 如果 target 存在，它一定还在当前保留下来的搜索区间里。

每次看中间值时，能丢掉一半，是因为数组是 sorted 的：

- 如果 \(target < mid\)，右半边都比 \(mid\) 大，所以 target 不可能在那里。
- 如果 \(target > mid\)，左半边都比 \(mid\) 小，所以 target 不可能在那里。

所以证明重点不是“它会一直减半”，而是“每次减半都没有把可能的答案丢掉”。

小检查：binary search 能丢掉一半，依赖数组的哪个条件？

## Why This Example Works

The tutor maps the error to the right intervention: proof hinge and invariant.
It does not reteach loops, indices, or the full algorithm.
