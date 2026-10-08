# Chapter 01: Training Foundations

Understand parameters, predictions, loss, gradients, learning rate, and repeated updates.

## Mathematical view

[00_math_intuition.ipynb](00_math_intuition.ipynb) is an optional reference for later.
Prediction, mean squared error, gradients as local slopes, and update rules.

**Math status: optional reference, not yet reviewed.** Continue the programming lessons without requiring this notebook first. Use a short arithmetic explanation only when it helps the current experiment; revisit formal notation later. Each related programming lesson links to the reference section. The programming chapter's covered status records our earlier work.

## Start here

Open [01_lessons.ipynb](01_lessons.ipynb) and run its cells from top to bottom.
The package-installation cell is optional when PyTorch already imports.

## Lessons in order

1. Install PyTorch (optional)
2. Import PyTorch
3. Create four training examples
4. Make predictions with weight and bias
5. Measure prediction error with mean squared loss
6. Calculate gradients without changing parameters
7. Apply one parameter update
8. Compare learning rates from the same starting point
9. Recalculate gradients after an update
10. Repeat the full-batch training loop for 10 steps
11. Check what happens over 100 steps

## Revision

Use checkpoints **1–4** in
[01_training_basics_revision.ipynb](../revision/01_training_basics_revision.ipynb).

## Navigation

- [Course index](../README.md)
- [Previous: Course index](../README.md)
- [Next chapter](../02_batches_and_epochs/README.md)
