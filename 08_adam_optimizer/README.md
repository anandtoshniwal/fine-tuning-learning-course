# Chapter 08: Adam Optimizer

**Status: covered.** Start with [01_adam_basics.ipynb](01_adam_basics.ipynb).

**Current position:** All eight lessons have been run and reviewed in the mentoring conversation. The [chapter recap](01_adam_basics.ipynb#chapter-08-review) records Adam's memories, gradient clearing, and optimizer comparisons at matching update budgets.

## Notebook order

1. **[Meet Adam](01_adam_basics.ipynb):** compare the first SGD and Adam updates from identical model values and gradients.

## Lessons in notebook 01

1. Compare one plain-SGD update and one Adam update with the same learning-rate setting.
2. Explain the first Adam step sizes using the observed gradients and small arithmetic calculations.
3. Inspect Adam's two running averages and confirm that clearing gradients preserves its history.
4. Explain the gradient average with the default 90% old and 10% fresh contributions.
5. Explain the squared-gradient average using its separate weighting setting.
6. Perform the actual second Adam update and inspect its fresh gradients and changed memories.
7. Trace the first-step correction and size scaling to reconstruct the observed weight increase.
8. Compare training and validation outcomes at several equal update budgets and inspect loss increases.

## What comes next

Introduce weight decay with a small programming experiment, then explore how AdamW uses it. The next chapter will be added as we work through those lessons.

Use the programming-led mentoring approach: one idea in words, one small experiment, its output, and one understanding check. Start in a fresh kernel and run Setup. Prerequisites: `Linear`, mean squared loss, gradients, SGD, and the familiar training sequence.

- [Previous: Chapter 07](../07_freezing_parameters/README.md)
- [Revision](../revision/README.md)
- [Course index](../README.md)
