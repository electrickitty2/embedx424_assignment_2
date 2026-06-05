
# Edge AI Assignment: Neural Network from Scratch (Checkerboard Classification)

## Objective

Build a simple neural network **from scratch (no ML libraries)** to classify a 2D checkerboard pattern.

You will:
- Implement forward propagation
- Implement backpropagation
- Train a small neural network
- Visualize the decision boundary

---

## Dataset Concept

We generate (x, y) points and assign labels based on a checkerboard pattern.

This is a **non-linear classification problem** (like XOR, but extended to 2D).

---

## Activity

Analyze `assignment_02_claude.ipynb`. Any modifications should be written to `assignment_02_claude2.ipynb` with explanations for the changes. Document the behavior of the code for someone who is just learning neural networks so they can understand what is happening. Place all explanations in the Markdown cells of the notebook.

---

## Modifications for Exploration

### Plots per Run
- Keep the decision boundary plot per run.
- Add a plot for **Loss vs. Epochs** and **Learning Rate vs. Epochs** per run.

### Activation Functions

Add support for multiple activation functions (and their derivatives) so that each run configuration can specify a different activation function for the hidden layers.

### User Configuration

Restructure the user configuration section to allow the entire experiment to be run multiple times with different parameters. Use an array of configuration objects so that multiple runs can be defined and executed in sequence.

Each configuration object should support the following parameters:

| Parameter | Description |
|---|---|
| `HIDDEN_LAYERS` | Array defining the number of neurons per hidden layer. Example: `[32, 16, 8]` creates three hidden layers with 32, 16, and 8 neurons respectively. |
| `LEARNING_RATE` | Initial learning rate for gradient descent. |
| `EPOCHS` | Number of training epochs. |
| `LR_DECAY` | Learning rate decay factor applied per epoch. |
| `ACTIVATION` | Activation function to use (e.g., `relu`, `tanh`, `sigmoid`). |

Use this configuration for the initial pass:

'''python
# ─────────────────────────────────────────────────────────────────────────────
# USER CONFIGURATION  ← edit this section to define your experiments
# ─────────────────────────────────────────────────────────────────────────────
RUNS = [
    {
        "label":         "baseline (sigmoid, [64])",
        "hidden_layers": [64],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "sigmoid",
    },
    {
        "label":         "ReLU, lr decay, [64]",
        "hidden_layers": [64],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "relu",
    },
    {
        "label":         "leaky ReLU, [64]",
        "hidden_layers": [64],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "leaky_relu",
    },
    {
        "label":         "tanh, [64]",
        "hidden_layers": [64],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "tanh",
    },
    {
        "label":         "ReLU, [64,32,16,8]",
        "hidden_layers": [64,32,16,8],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "relu",
    },
    {
        "label":         "ReLU, [64,16,4]",
        "hidden_layers": [64,16,4],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "relu",
    },
    {
        "label":         "leaky ReLU, [128,64,32,16,8]",
        "hidden_layers": [128,64,32,16,8],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "leaky_relu",
    },
    {
        "label":         "leaky ReLU, [64,32,16,8]",
        "hidden_layers": [64,32,16,8],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "leaky_relu",
    },
    {
        "label":         "leaky ReLU, [64,16,4]",
        "hidden_layers": [64,16,4],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "leaky_relu",
    },
    {
        "label":         "leaky ReLU, [128,64,32,16,8]",
        "hidden_layers": [128,64,32,16,8],
        "learning_rate": 0.1,
        "epochs":        10000,
        "lr_decay":      0.9995,
        "activation":    "leaky_relu",
    },
]
# ─────────────────────────────────────────────────────────────────────────────
'''
