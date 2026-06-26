# Source Pack Usage Example

## User Question

"I'm starting to learn machine learning. What math and CS foundations should I
review first, and what sources should I use?"

## Diagnosis

This is an AI / machine learning learning-path question. The likely gap is not
one missing fact; it is the prerequisite chain. The learner probably needs to
know which foundations matter, what order to study them in, and which sources
support each stage without becoming overwhelming.

## Prerequisite Chain

1. Programming basics: variables, functions, loops, data structures, debugging.
2. Linear algebra: vectors, matrices, dot products, matrix multiplication, and
   geometric meaning.
3. Calculus and optimization: derivatives, gradients, and why training means
   changing parameters to reduce loss.
4. Probability and statistics: random variables, distributions, estimation,
   uncertainty, train/test evaluation.
5. Algorithms and data handling: complexity, arrays/lists/maps, graph basics,
   and clean implementation habits.

## Resource Selection From Source Packs

- From `source_packs/programming_and_cs_foundations.md`: MIT OCW 6.100L for
  Python programming and computational thinking.
- From `source_packs/math_foundations.md`: MIT OCW 18.06 for linear algebra,
  MIT OCW 18.05 for probability/statistics, and OpenStax Calculus Volume 1 for
  calculus refreshers.
- From `source_packs/ai_ml_data.md`: Google Machine Learning Crash Course for
  a beginner-friendly ML on-ramp, then Stanford CS229 for a more rigorous path.
- From `source_packs/exam_problem_set_sources.md`: MIT OCW 6.006 assignments
  only if the learner needs algorithm practice before ML implementation.

## Example Answer

You do not need to learn every math topic before touching ML. The better path
is to learn the pieces that explain what models are doing.

Start with programming, because ML ideas become real through data and code. If
loops, functions, lists, dictionaries, and debugging still feel shaky, use MIT
OCW 6.100L first. Your practice goal is simple: load data, transform it, write
functions, and debug mistakes without guessing.

Then learn linear algebra. In ML, a data point is often represented as a vector,
and a dataset can be viewed as a matrix. Matrix multiplication is not just a
formula; it is how models combine features, weights, and transformations. MIT
OCW 18.06 is the best formal starting point here. If the formulas feel abstract,
use 3Blue1Brown's Essence of Linear Algebra as visual support, but do not treat
it as the whole course.

Next, review calculus for gradients. You mainly need derivatives, partial
derivatives, and the idea that a gradient points in the direction of fastest
increase. Gradient descent uses that idea in reverse: change parameters in a
direction that reduces loss. OpenStax Calculus Volume 1 is enough for a
refresh, while optimization can come later.

After that, study probability and statistics. ML is full of uncertainty:
training data is sampled, models make errors, and evaluation estimates how well
the model may generalize. MIT OCW 18.05 is a good source for probability,
estimation, and inference.

Once those foundations are moving, use Google Machine Learning Crash Course to
connect the pieces quickly: features, labels, loss, training, validation, and
classification. Then use Stanford CS229 when you want the university-level
mathematical version.

## Suggested Learning Path

1. Week 1-2: Python and debugging with MIT OCW 6.100L.
2. Week 3-5: vectors, matrices, dot products, projections, and eigen ideas with
   MIT OCW 18.06.
3. Week 6: derivative and gradient refresh with OpenStax Calculus.
4. Week 7-8: probability, distributions, estimation, and evaluation with MIT
   OCW 18.05.
5. Week 9+: ML overview with Google ML Crash Course, then deeper study with
   Stanford CS229.

## How To Use The Sources

- Use MIT and OpenStax sources for foundations and practice, not just reading.
- Use Google ML Crash Course to see how the pieces fit together.
- Use Stanford CS229 after you can explain vectors, gradients, probability, and
  train/test evaluation in plain language.
- Keep a "mistake log" for concepts you confuse: matrix multiplication,
  gradient, loss, overfitting, and evaluation are common early friction points.

## What To Practice

- Turn a small table into feature vectors.
- Compute dot products and explain what similarity means.
- Sketch how changing a model parameter changes loss.
- Split a dataset conceptually into train and test parts.
- Explain overfitting without using jargon.

## Source List Behavior

When answering with current web access, list source labels and links:

- MIT OCW 6.100L Python Programming:
  https://ocw.mit.edu/courses/6-100l-introduction-to-cs-and-programming-using-python-fall-2022/
- MIT OCW 18.06 Linear Algebra:
  https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/
- MIT OCW 18.05 Probability And Statistics:
  https://ocw.mit.edu/courses/18-05-introduction-to-probability-and-statistics-spring-2022/
- OpenStax Calculus Volume 1:
  https://openstax.org/details/books/calculus-volume-1
- Google Machine Learning Crash Course:
  https://developers.google.com/machine-learning/crash-course
- Stanford CS229 Machine Learning:
  https://cs229.stanford.edu/

If web access is unavailable, say that the sources could not be verified in the
current environment and present them as source categories or previously curated
pack entries rather than pretending to have checked them live.

## Why This Is Diagnosis-First And Resource-Augmented

The answer starts by diagnosing the learner's real need: a prerequisite chain
for ML, not a random source list. It orders resources around the learner's
likely gaps, explains how each source helps, and keeps teaching at the center.
The sources support the path; they do not replace the tutor's explanation.
