# Chapter 07: Freezing Parameters

**Status: covered.** Start with [01_freeze_weights.ipynb](01_freeze_weights.ipynb).

**Current position:** All five lessons have been run and reviewed in the mentoring conversation. The [chapter recap](01_freeze_weights.ipynb#chapter-07-review) records gradient flags, optimizer registration, and the limits of bias-only training.

## Mathematical view

Open [00_math_intuition.ipynb](00_math_intuition.ipynb) beside the programming lessons.
Constrained optimization, the bias-only minimum, and non-unique fitting parameters.

**Math status: prepared; mentoring review pending.** Start with words and worked numbers, then read the formula and run its matching code. Each related programming lesson links to the relevant section. The programming chapter's covered status records our earlier work.

## Notebook order

1. **[Freeze weights and train the bias](01_freeze_weights.ipynb):** inspect which parameters receive gradients when the two weights are frozen and the bias remains trainable.

## Lessons in notebook 01

1. Freeze the weights and calculate a bias gradient without updating any parameter values.
2. Give SGD only the bias, apply its stored gradient, and measure updated predictions and loss.
3. Repeat bias-only training with fresh gradients and investigate the loss that remains.
4. Unfreeze weights and compare a bias-only optimizer with one that includes all parameters.
5. Continue training all parameters and compare the remaining error with the bias-only limit.

## What comes next

Next, introduce Adam and study how gradient history changes the scaling of parameter updates.

Start in a fresh kernel and run Setup. Prerequisites: `Linear`, parameters, gradient calculation, SGD, and `torch.no_grad()`.

- [Previous: Chapter 06](../06_datasets_and_dataloaders/README.md)
- [Revision](../revision/README.md)
- [Course index](../README.md)
