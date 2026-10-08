# Chapter 05: PyTorch Model Layers

**Status: covered.** Start with [01_linear_layer.ipynb](01_linear_layer.ipynb).

**Current position:** All six notebooks have been covered in the mentoring conversation, including notebook 05, Lesson 13. Restoring model and optimizer state reproduced uninterrupted training in our fixed-data momentum experiment. Continue with [Chapter 06: Datasets and DataLoaders](../06_datasets_and_dataloaders/README.md).

## Mathematical view

Open [00_math_intuition.ipynb](00_math_intuition.ipynb) beside the programming lessons.
Weighted sums, matrix shapes, per-feature gradients, and model state.

**Math status: prepared; mentoring review pending.** Start with words and worked numbers, then read the formula and run its matching code. Each related programming lesson links to the relevant section. The programming chapter's covered status records our earlier work.

## Notebook order

1. **Our model as a PyTorch layer:** inspect parameters, arrange examples and features,
   make familiar predictions, and calculate the same loss.
2. **[Training the layer](02_training_layer.ipynb):** calculate gradients, pass the layer's parameters to SGD, perform one complete training step, and repeat it in a loop.
3. **[Two input features](03_two_input_features.ipynb):** inspect two weights and one bias, predict for one and four examples, inspect each weight's gradient, and train all three parameters.
4. **[Python classes from scratch](04_python_classes.ipynb):** learn objects, attributes, initialization, and methods using our prediction formula.
5. **[Our own PyTorch model class](05_custom_pytorch_model.ipynb):** inherit from `Module`, store a layer, define `forward`, and train through the model's parameters.
6. **[torch.no_grad explained](06_no_grad_explained.ipynb):** focused review of recording, evaluation, initialization, and parameter updates. Study this after Notebook 05, Lesson 03, then return to its Lesson 04.

## Lessons in notebook 01

1. Create `torch.nn.Linear(1, 1)` and inspect its weight and bias.
2. Arrange four examples with one feature each as a tensor of shape `[4, 1]`.
3. Assign weight 1 and bias 0, then compare `model(x)` with the manual calculation.
4. Measure mean squared loss and confirm that predictions alone do not train parameters.

## Lessons in notebook 02

1. Calculate gradients and confirm that backward leaves parameters unchanged.
2. Use `model.parameters()` with SGD to update weight and bias.
3. Recreate our familiar complete training step and compare loss before and after.
4. Repeat ten full-batch updates and compare them with the manual training rule.
5. Compare our handwritten loss with `torch.nn.MSELoss()`.

## Lessons in notebook 03

1. Inspect `Linear(2, 1)` and count its three scalar parameter values.
2. Predict 12 from one example with two features using known parameter values.
3. Predict for four examples while sharing the same parameters.
4. Inspect both weight gradients when one input feature is zero.
5. Compare gradients when the other input feature is active.
6. Apply one SGD update and measure the new prediction and loss.
7. Combine two examples into a batch and interpret the mean-loss gradients.
8. Apply the batch update to all three parameters and remeasure predictions and loss.
9. Train on all four examples for 100 full-batch epochs.
10. Measure loss on unseen validation examples without updating parameters.

## Lessons in notebook 04

1. Define a class and create two separate objects.
2. Store each object's weight and bias using `__init__` and `self`.
3. Call a prediction method using the object's stored values.
4. Change one object's weight and compare both predictions.

## Lessons in notebook 05

1. Inherit model features from `torch.nn.Module` in an empty class.
2. Initialize a layer and define the forward calculation.
3. Call the model with known weights and bias.
4. Reproduce our familiar two-example SGD update through the model class.
5. Inspect the model's named state values with `state_dict()`.
6. Load those values into another model and compare predictions.
7. Save the current state to a `.pt` checkpoint file in the chapter's `checkpoints` folder.
8. Read that file and restore a compatible model, using only the class definition and saved state.
9. Inspect momentum buffers and optimizer settings for resuming training.
10. Save a checkpoint containing the model, optimizer, and completed-update count.
11. Restore the model, optimizer memory and settings, and progress counter from that file.
12. Continue with a fresh gradient calculation and the next momentum update.
13. Compare full restoration with a fresh optimizer at the same total update budget.

## Lessons in notebook 06

1. Compare the same numerical calculation with and without gradient recording.
2. Separate forward recording, backward, and clearing stored gradients.
3. Assign initial parameter values without recording assignments.
4. Perform a manual update inside no-grad and confirm that values can change.
5. Keep training tracked and evaluate afterward without recording.
6. Revisit the differences between no-grad, zero-grad, detach, and evaluation mode.

Run each notebook from top to bottom in a fresh kernel. Each lesson has prediction and
explanation fields. Prerequisites: parameters, loss, gradients, batches, and plain SGD.

- [Previous: Chapter 04](../04_optimizers_and_momentum/README.md)
- [Next: Chapter 06](../06_datasets_and_dataloaders/README.md)
- [Revision](../revision/README.md)
- [Course index](../README.md)
