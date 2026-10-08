# Chapter 03: Validation and Generalization

Separate training, validation, and test roles; investigate incorrect targets and choose checkpoints.

## Mathematical view

[00_math_intuition.ipynb](00_math_intuition.ipynb) is an optional reference for later.
Separate data averages, targets, checkpoint minima, and early stopping.

**Math status: optional reference, not yet reviewed.** Continue the programming lessons without requiring this notebook first. Use a short arithmetic explanation only when it helps the current experiment; revisit formal notation later. Each related programming lesson links to the reference section. The programming chapter's covered status records our earlier work.

## Start here

Open [01_lessons.ipynb](01_lessons.ipynb) and run its cells from top to bottom.
Run the local setup cell first; the notebook is self-contained.

## Lessons in order

1. Training loss and validation loss
2. Track training and validation loss over epochs
3. Fit the supplied targets: original versus noisy data
4. Early stopping and patience
5. Evaluate selected checkpoints on a held-out test set

## Revision

Use checkpoints **6–8** in
[01_training_basics_revision.ipynb](../revision/01_training_basics_revision.ipynb).

## Navigation

- [Course index](../README.md)
- [Previous: Chapter 02](../02_batches_and_epochs/README.md)
- [Next chapter](../04_optimizers_and_momentum/README.md)
