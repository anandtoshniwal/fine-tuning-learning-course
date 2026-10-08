# Chapter 04: Optimizers and Momentum

Use SGD, inspect momentum, compare learning rates at fixed budgets, and load selected checkpoints.

## Mathematical view

Open [00_math_intuition.ipynb](00_math_intuition.ipynb) beside the programming lessons.
Parameter vectors, momentum recurrence, and saved optimizer history.

**Math status: prepared; mentoring review pending.** Start with words and worked numbers, then read the formula and run its matching code. Each related programming lesson links to the relevant section. The programming chapter's covered status records our earlier work.

## Start here

Open [01_lessons.ipynb](01_lessons.ipynb) and run its cells from top to bottom.
Run the local setup cell first; the notebook is self-contained.

## Lessons in order

1. Replace manual updates with the SGD optimizer
2. Train for 10 steps using SGD
3. Inspect how momentum changes SGD updates
4. Compare momentum settings at a fixed training budget
5. Learning rate and momentum interact
6. Select and load the best validation checkpoint

## Revision

Use checkpoints **9 (plain SGD)** in
[01_training_basics_revision.ipynb](../revision/01_training_basics_revision.ipynb).
The revision notebook covers plain SGD; lessons 03–06 here remain the worked
reference for momentum and its interaction with learning rate.

## Navigation

- [Course index](../README.md)
- [Previous: Chapter 03](../03_validation_and_generalization/README.md)
- [Next chapter](../05_pytorch_model_layers/README.md)
