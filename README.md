# Fine-Tuning Learning Course

A step-by-step mentoring course that builds PyTorch training foundations toward language-model fine-tuning. The current notebooks cover small regression models; language-model fine-tuning lessons will be added as we progress.

**Start here.** Follow the numbered chapters in order. Each folder contains a chapter
guide and a self-contained lesson notebook. Write a prediction before each experiment,
then record the observation and explain why it happened.

## Learning order

| Order | Chapter | Notebook | Status | Original sections |
|---|---|---|---|---|
| 01 | [Training Foundations](01_training_foundations/README.md) | [Lessons](01_training_foundations/01_lessons.ipynb) | Covered | 1–11 |
| 02 | [Batches and Epochs](02_batches_and_epochs/README.md) | [Lessons](02_batches_and_epochs/01_lessons.ipynb) | Covered | 12–16 |
| 03 | [Validation and Generalization](03_validation_and_generalization/README.md) | [Lessons](03_validation_and_generalization/01_lessons.ipynb) | Covered | 17–21 |
| 04 | [Optimizers and Momentum](04_optimizers_and_momentum/README.md) | [Lessons](04_optimizers_and_momentum/01_lessons.ipynb) | Covered | 22–27 |
| 05 | [PyTorch Model Layers](05_pytorch_model_layers/README.md) | [Notebook order](05_pytorch_model_layers/README.md#notebook-order) | Covered | New material |
| 06 | [Datasets and DataLoaders](06_datasets_and_dataloaders/README.md) | [Datasets and batches](06_datasets_and_dataloaders/01_tensor_dataset.ipynb) | Covered | New material |

**Current position:** Chapters 01–06 have been covered in the mentoring conversation,
including dataset pairing, batch sizes, incomplete batches, shuffled order, and training
with one update per batch. The next topic is freezing selected model parameters while
training others. “Covered” records our progress; the revision notebook records any written answers and review notes.

## Run locally

Tested with Python 3.12 and PyTorch 2.6.0. Create an environment, install the notebook tools, and open the course:

```bash
git clone https://github.com/anandtoshniwal/fine-tuning-learning-course.git
cd fine-tuning-learning-course
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m jupyterlab
```

On Windows, activate the environment with `.venv\Scripts\activate` instead. Select the environment's Python kernel in your notebook editor. Start Jupyter from inside the cloned repository; checkpoint lessons locate the chapter folder from the working directory.

Small example checkpoints are included for the save-and-restore lessons. Running the save cells regenerates these files. Saved outputs show previous experiments; rerun cells to reproduce the calculations in your own environment.

## How to use the course

1. Open the chapter guide, then follow its numbered notebook order.
2. Run cells from top to bottom. Every chapter has its own imports and prerequisites.
3. Use the linked revision checkpoints after each chapter.
4. Keep your predictions, observations, and explanations with the experiment.
5. When returning later, use the contents list in each notebook to find a lesson.

For later chapters, start from a fresh kernel and run the local setup cell. Notebook
kernel variables are not automatically shared across files. PyTorch is already installed
in our current environment; Chapter 01 includes optional setup commands for a new environment.

## Saving chapter progress to GitHub

After each chapter is completed and reviewed in the mentoring conversation, update the progress in the course and chapter guides, verify the changed notebooks and navigation, then commit and push the chapter's changes to `main` in [the public course repository](https://github.com/anandtoshniwal/fine-tuning-learning-course).

Changes for a chapter in progress stay local until that chapter is complete, unless an earlier push is requested.

## Revision and reference

- [Revision guide](revision/README.md) and [revision notebook](revision/01_training_basics_revision.ipynb).
- [Complete worked reference](reference/README.md): the original notebook retains its section
  numbers and saved outputs, so earlier conversation references remain easy to find.

## Folder map

```text
FineTuning/
├── README.md                         ← course index and learning order
├── 01_training_foundations/
│   ├── README.md
│   └── 01_lessons.ipynb
├── 02_batches_and_epochs/
│   ├── README.md
│   └── 01_lessons.ipynb
├── 03_validation_and_generalization/
│   ├── README.md
│   └── 01_lessons.ipynb
├── 04_optimizers_and_momentum/
│   ├── README.md
│   └── 01_lessons.ipynb
├── 05_pytorch_model_layers/
│   ├── README.md
│   ├── 01_linear_layer.ipynb
│   ├── 02_training_layer.ipynb
│   ├── 03_two_input_features.ipynb
│   ├── 04_python_classes.ipynb
│   ├── 05_custom_pytorch_model.ipynb  ← covered
│   ├── 06_no_grad_explained.ipynb     ← reviewed reference
│   └── checkpoints/
│       ├── two_input_model_state.pt
│       └── two_input_momentum_training.pt
├── 06_datasets_and_dataloaders/
│   ├── README.md
│   └── 01_tensor_dataset.ipynb         ← covered
├── revision/
│   ├── README.md
│   └── 01_training_basics_revision.ipynb
└── reference/
    ├── README.md
    └── understand_training_basics.ipynb
```

New lesson notebooks will use `01_`, `02_`, and so on within their chapter. Each chapter
guide links back to this index and forward to the next chapter. Add new chapters when
the course moves to a new major topic.
