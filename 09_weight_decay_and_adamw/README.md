# Chapter 09: Weight Decay and AdamW

**Status: covered.** Start with [01_weight_decay.ipynb](01_weight_decay.ipynb).

**Current position:** All six lessons have been run and reviewed in the mentoring conversation. The [chapter recap](01_weight_decay.ipynb#chapter-09-review) records decay calculations, AdamW, optimizer memories, and validation-based selection.

## Notebook order

1. **[Meet weight decay](01_weight_decay.ipynb):** compare an update with and without weight decay using one example and one weight.

## Lessons in notebook 01

1. Observe weight decay with a zero prediction-loss gradient.
2. Trace the decay contribution and check the update for positive and negative weights.
3. Combine a nonzero prediction-loss gradient and decay in one SGD update.
4. Meet AdamW and compare its decay update with Adam.
5. Inspect which optimizer memories include the decay contribution.
6. Combine a nonzero prediction-loss gradient and decay with Adam and AdamW.

## What comes next

Introduce learning-rate schedules: observe what changes when we adjust the learning rate during training, then let a scheduler manage that setting. The next chapter will be added as we progress.

Start in a fresh kernel and run Setup. Prerequisites: `Linear`, mean squared loss, gradients, plain SGD, and `torch.no_grad()`.

- [Previous: Chapter 08](../08_adam_optimizer/README.md)
- [Revision](../revision/README.md)
- [Course index](../README.md)
