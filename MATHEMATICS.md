# From a Problem Statement to Mathematics

[Course index](README.md)

**Optional reference for later.** Continue the programming-led mentoring course, including Adam, without completing these notes first. Introduce a little arithmetic when it explains the current code; formal notation and derivations can wait. The existing programming chapters are covered, while these reference notes have not been reviewed in the mentoring conversation.

The teaching sequence is: one idea in everyday words → a small code example → observe the output → discuss one question. When mathematics helps, first use actual numbers and familiar words. Introduce a symbol only after its meaning is understood. No formal mathematics background is assumed.

Mathematics gives precise names to the quantities and relationships in a problem. Turning a problem into equations still requires decisions: what information is available, what outcome matters, which relationships we assume, and what errors we want to penalize. An equation is useful only if those choices match the problem.

The `00_math_intuition.ipynb` files are companions beside the existing lessons. The `00` prefix makes them easy to find; it does not mean you must finish an entire mathematics course before running the programming lessons. Every companion starts with words, explains its symbols, works through familiar numbers, and provides short runnable code.

## A worked translation

**Toy problem:** use delivery distance to predict delivery time. Our made-up observations are distances `[0, 1, 2, 3]` and times `[2, 5, 8, 11]`.

| Question to ask | Choice in our toy problem | Mathematical view |
|---|---|---|
| What will be known when predicting? | Distance | Input $x$ |
| What do we want to predict? | Recorded delivery time | Target $y$ |
| How are observations organized? | Matching distance–time pairs | $(x_i,y_i)$; $i$ identifies an example |
| What prediction rule will we try? | Multiply distance by a weight, then add a bias | $\hat y=wx+b$ |
| Which values can training change? | Weight and bias | Parameters $w,b$ |
| What counts as a miss? | Prediction minus recorded time | Error $e=\hat y-y$ |
| How do we score several misses? | Average their squared errors | Loss $L=\frac{1}{n}\sum_i e_i^2$ |
| How do we change parameters? | Use local loss slopes and a learning rate | SGD subtracts learning rate times gradient |
| How do we judge a selected model? | Evaluate held-out examples | Separate validation and test losses |

The hat on $\hat y$ means “prediction”; it is not a new target. The sum symbol $\sum$ means add across examples, and $n$ is the example count for this single-output loss.

In this story, weight has units of minutes per kilometre and bias has units of minutes. That makes $wx+b$ a quantity measured in minutes. Units can help check whether a proposed formula is sensible. Squared loss has units of minutes squared.

The straight-line rule and squared loss are modeling choices. Real measurements may not follow a straight line; other prediction tasks may need other outputs and losses. We will introduce the mathematics for language-model outputs when those lessons arrive.

## Mathematical companions in chapter order

| Chapter | What the mathematics explains | Companion |
|---|---|---|
| 01 | Prediction functions, errors, means, local slopes, and gradient updates | [Training foundations](01_training_foundations/00_math_intuition.ipynb) |
| 02 | Mean gradients in batches, sequential updates, and epoch counts | [Batches and epochs](02_batches_and_epochs/00_math_intuition.ipynb) |
| 03 | Loss on separate datasets, supplied targets, checkpoint selection, and patience | [Validation](03_validation_and_generalization/00_math_intuition.ipynb) |
| 04 | Parameter vectors, gradient history, momentum buffers, and training state | [Optimizers and momentum](04_optimizers_and_momentum/00_math_intuition.ipynb) |
| 05 | Weighted sums, dot products, matrices, shapes, and feature-wise gradients | [PyTorch layers](05_pytorch_model_layers/00_math_intuition.ipynb) |
| 06 | Matching pairs, permutations, rounded batch counts, and weighted loss averages | [Datasets and loaders](06_datasets_and_dataloaders/00_math_intuition.ipynb) |
| 07 | Fixed-parameter constraints, the bias-only loss floor, and non-unique fits | [Freezing parameters](07_freezing_parameters/00_math_intuition.ipynb) |

## Read notation in small steps

| Notation | Read it in plain language |
|---|---|
| $x$, $y$, $\hat y$ | Input, target, predicted target |
| $w$, $b$ | Weight, bias |
| $L$ | Loss, our error score |
| $i$ | Which example; its starting index depends on the notation or code |
| $n$, $N$ | Example count; the surrounding section says which data is counted |
| $\eta$ | Eta: learning rate |
| $g_w$, $g_b$ | Gradients for weight and bias |
| $\partial L/\partial w$ | How loss changes locally when just the weight changes |
| $\theta$ | Theta: a collection of parameter values |
| $\mu$, $v$ | Mu: momentum coefficient; $v$: remembered update-direction buffer |
| $\sum$, $\min$ | Add the terms; find the smallest value |
| $\operatorname{argmin}$ | The position or parameter choice where the smallest value occurs |
| $\mathbf x$, $X$ | A feature vector; a matrix of input rows |
| $W^T$ | Weight matrix with rows and columns swapped |
| $\pi$ | Pi: a permutation, or rearranged example order |

This table is a reference, not a memorization test. Start with $x,y,\hat y,w,b$ and add the rest when their sections use them. We will develop derivative and matrix intuition gradually.

## A worksheet for a new problem

1. Write the desired prediction in one sentence.
2. Name the available inputs and the correct target, including their units or categories.
3. Write two or three concrete input–target examples.
4. Choose a prediction rule and identify the parameters that can change.
5. Define what a good or bad prediction means; choose a loss that reflects it.
6. Identify any fixed values or constraints, such as frozen parameters.
7. Work through one prediction and one loss calculation by hand.
8. Check how training can change the parameters, then evaluate on held-out data.

We will fill this in together using small examples. For each section, connect the formula to the corresponding code before moving on.
