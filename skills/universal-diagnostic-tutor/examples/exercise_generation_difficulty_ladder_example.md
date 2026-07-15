# 同一概念的三档练习生成

这个例子展示如何依据现有 Practice Ladder 为“链式法则”生成不同难度的单题。
三题是三种候选，不是在同一轮全部发给学习者。

## 共同目标

- **Target concept：** 识别并使用链式法则。
- **Prerequisite：** 基本幂函数求导，以及能区分外层函数和内层函数。
- **Likely trap：** 只求外层导数，漏乘内层导数。
- **Default stop：** 发出所选的一题后等待作答，不提前展示答案或下一题。

## Level 1：Recognition Check

- **Difficulty：** 基础识别。
- **Question：** 下列哪个函数需要链式法则：\(x^2+1\)、\((3x+1)^2\)、
  \(x^3\)？只需选出并说明“哪里发生了函数嵌套”。
- **Expected learner action：** 识别 \((3x+1)^2\) 的外层平方与内层线性函数。
- **Grading criteria：** 选对且能指出嵌套结构；只猜选项不能确认理解。
- **Hint policy：** 若卡住，只问“平方里面还是单独的 \(x\) 吗？”

## Level 3：Worked Example Completion

- **Difficulty：** 有脚手架的步骤完成。
- **Question：** 补全
  \[
  \frac{d}{dx}(2x+1)^3=3(2x+1)^2\cdot \underline{\qquad}.
  \]
  并说出空格对应哪个函数的导数。
- **Expected learner action：** 填 \(2\)，并指出它来自内层 \(2x+1\)。
- **Grading criteria：** 数值和来源都正确；只填 \(2\) 视为理由尚待检查。
- **Hint policy：** 先提示“现在只对括号里面求导”，不直接给出 \(2\)。

## Level 4：Near-Transfer Problem

- **Difficulty：** 相同结构的独立应用。
- **Question：** 求 \(g(x)=(5x-2)^4\) 的导数，并分别标出外层导数和内层导数。
- **Expected learner action：** 独立得到
  \(g'(x)=4(5x-2)^3\cdot 5\)，并解释两个因子的来源。
- **Grading criteria：** 方法、计算和解释一致；漏乘 \(5\) 表示仍需回到 Level 3。
- **Hint policy：** 首次作答前不提示；请求提示时只让学习者圈出内外层。

## 如何选择

无法看出复合结构时选 Level 1；能识别但常漏步骤时选 Level 3；有脚手架成功后选
Level 4。实际回复只生成当前最匹配的一题，批改后再决定升档、保持或降档。
