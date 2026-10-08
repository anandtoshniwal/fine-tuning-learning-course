# Chapter 06: Datasets and DataLoaders

**Status: covered.** Start with [01_tensor_dataset.ipynb](01_tensor_dataset.ipynb).

**Current position:** All six lessons have been run and reviewed in the mentoring conversation. The [chapter recap](01_tensor_dataset.ipynb#chapter-06-review) records the main distinctions and the two-epoch training results.

## Mathematical view

Open [00_math_intuition.ipynb](00_math_intuition.ipynb) beside the programming lessons.
Paired indexes, shuffling permutations, rounded counts, and weighted means.

**Math status: prepared; mentoring review pending.** Start with words and worked numbers, then read the formula and run its matching code. Each related programming lesson links to the relevant section. The programming chapter's covered status records our earlier work.

## Notebook order

1. **[Datasets and batches](01_tensor_dataset.ipynb):** wrap our familiar inputs and targets in `TensorDataset`, count examples, and retrieve matching pairs, and then group examples into batches.

## Lessons in notebook 01

1. Keep inputs and targets together and retrieve one example by index.
2. Use `DataLoader` to create batches of two and inspect inputs, targets, and shapes.
3. Keep an incomplete final batch and compare its size and tensor shapes.
4. Compare `drop_last=False` with `drop_last=True` and count returned examples separately from dataset size.
5. Shuffle example order across loader passes while preserving matching targets.
6. Train with the loader, count one update per batch, and evaluate full training loss after each epoch.

## What comes next

Continue with [Chapter 07: Freezing Parameters](../07_freezing_parameters/README.md) to keep selected values fixed while training others.

Start in a fresh kernel and run the setup cell. The notebook has its own data; it does not depend on earlier notebook variables. Prerequisites: examples, features, targets, tensor shapes, batches, and epochs.

- [Previous: Chapter 05](../05_pytorch_model_layers/README.md)
- [Next: Chapter 07](../07_freezing_parameters/README.md)
- [Revision](../revision/README.md)
- [Course index](../README.md)
