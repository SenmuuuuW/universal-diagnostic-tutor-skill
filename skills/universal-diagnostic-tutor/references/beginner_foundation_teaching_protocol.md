# Beginner Foundation Teaching Protocol

Use this protocol for true beginners, zero-base learners, or learners whose
confusion comes from missing vocabulary, notation, symbols, object types, or
the basic purpose of the task.

The core rule: explain "what is this object?" before "how do we solve?"

For STEM / AI-CS tutoring, begin with a short domain diagnosis when it helps
the learner orient: subject -> knowledge system -> subtopic -> core concept.
Keep it to one or two lines, then return to the learner's immediate blocker.

## Beginner Teaching Sequence

1. **Name the object.** Point to the thing being discussed: vector, equation,
   function, graph, edge, loop, memory address, signal, claim, grammar pattern,
   etc.
2. **Translate it into ordinary language.** Avoid jargon until the learner has
   a usable hook.
3. **Explain the object type.** Is it a number, vector, matrix, function,
   graph, edge, statement, rule, process, state, or signal?
4. **Use real-life or visual intuition.** Build a mental picture before
   formulas.
5. **Use a tiny numerical example.** Prefer one or two numbers before abstract
   symbols.
6. **Connect back to the original problem.** Show why the object matters.
7. **Ask one small check.** Do not pile on several questions. After the check,
   stop and wait.
8. **Stop before the full solution.** Confirm the learner understands the
   representation before calculation or proof.

Explain at most one or two new prerequisite concepts before the first check.
For proof or theorem questions, first explain what the statement is saying;
do not begin with the proof, theorem machinery, or full solution.

## STEM Plain-Language Object Glossary

Use these when needed; do not dump the whole list.

- **Scalar:** one number, such as a length, price, or temperature.
- **Vector:** a quantity with components, often representing movement,
  direction, features, or state.
- **Matrix:** a rectangular table of numbers that may represent data or a
  transformation.
- **Graph:** a set of objects and connections between them.
- **Complete graph:** a graph where every pair of vertices is connected.
- **Edge coloring:** assigning colors to edges so adjacent edges do not share a
  color when the rule requires it.
- **Edge chromatic number:** the minimum number of colors needed to edge-color
  a graph.
- **Function:** a rule that takes an input and gives an output.
- **Variable:** a symbol standing for a value that can change or is unknown.
- **Parameter:** a value that controls a model, formula, or system.
- **Equation:** a statement that two expressions are equal.
- **Derivative:** a measure of how fast something changes at an instant.
- **Series:** a sum of many terms, often infinitely many.
- **Probability:** a way to measure uncertainty or relative frequency.
- **Algorithm:** a step-by-step method for solving a problem.
- **Memory:** stored information a program or system can read or change.
- **State:** the current values or conditions of a system at a moment.
- **Signal:** a changing quantity that carries information, such as sound,
  voltage, or sensor readings.

## Beginner Mistakes To Watch For

- Copying formulas without knowing what the objects mean.
- Confusing a symbol with one fixed value.
- Not knowing what the question is asking.
- Not knowing why a method is chosen.
- Treating every problem as computation only.
- Manipulating symbols before understanding the representation.
- Continuing after a check question instead of waiting for the learner's
  answer.

## Good Beginner Moves

- "Before the formula, let's name the objects."
- "This symbol is not magic; it is a shorthand for..."
- "Let's use a walking example before numbers."
- "Tiny check: is this object a number, a vector, or a function?"
- "We will stop here, because the next step only makes sense if this picture is
  clear."

Graph theory example:

先判断领域：这是离散数学 -> 图论 -> 边染色。

在证明之前，先翻译符号：\(K_n\) 是有 \(n\) 个点、每两个点之间都连边的
完全图；\(\chi'(G)\) 表示给图 \(G\) 的边染色时最少需要几种颜色。

我先停在这里。小检查：这里研究的是给“点”染色，还是给“边”染色？

## Avoid

- Starting with the full theorem or formal proof.
- Starting a proof before translating the statement into plain language.
- Asking a guiding question that requires vocabulary the learner does not have.
- Solving the whole problem before the learner understands the representation.
- Explaining more than one or two new ideas before the first check.
- Asking a check question and then continuing to the next proof step.
- Adding several formulas to compensate for confusion.
- Treating beginner status as lack of ability. It is only missing setup.
