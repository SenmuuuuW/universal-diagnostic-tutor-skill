# Skill Pack Invocation Example

These slash-style names are prompt conventions, not CLI commands. They help the
learner state intent quickly.

## Example Inputs And Expected Behavior

| User input | Expected behavior |
| --- | --- |
| `/tutor 我是零基础，\(Ax=b\) 到底是什么意思？` | Start diagnosis-first tutoring: topic scan, explain object roles, ask one check. |
| `/diagnose-gap 我会背 Bayes 公式但总不会用。` | Diagnose recognition and conditioned-sample-space gaps before teaching. |
| `/study-plan 我想学机器学习，但线代和概率都弱。` | Give a brief plan: current state, top gaps, order, today's first step, one check. |
| `/state-card 帮我生成下次继续用的学习卡。` | Produce a compact Learning State Card or task card, no hidden-memory claim. |
| `/exam-track 级数判敛总不会选方法。` | Identify exam-relevant topic, method cue gap, review order, and one practice step. |
| `/resource-scan 我想系统补线代，有什么靠谱资料？` | Topic scan, trusted resource types or verified sources if browsing is available. |
| `/visualize 向量平行我看文字不懂。` | Use a simple vector diagram or description tied to the current gap. |
| `/mistake-review 我把条件概率分母写成总样本数了。` | Analyze surface mistake, underlying misconception, tempting path, and repair. |

## Short Expected Response Shape

For `/tutor 我是零基础，\(Ax=b\) 到底是什么意思？`:

这是线性代数 -> 矩阵方程 -> 对象角色。你现在最可能卡在符号代表什么。

先看三个对象：A 是一个变换或方程组，x 是未知输入向量，b 是目标输出向量。\(Ax=b\) 的意思是：找一个 \(x\)，让 \(A\) 作用后得到 \(b\)。

小检查：这三个里面，通常哪个是未知的？

The visible answer stays natural. It does not announce internal protocol names.
