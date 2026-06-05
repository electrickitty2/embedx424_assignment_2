
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

## activity

Analyze assignment_02.ipynb any modifications should be written to the file assignment_02_claud.ipyn with explianations for the changes.  Document the behavior of the code for someone who is just learning neural networks so they can understand what is happening in the code.  Make the comments in the markdown sections.

## Modifications for exploration

Keep the decision boundary layer plot per run, and add a plot for Loss and Learning rate  vs epochs per run.

In the user configuration, change the structure to allow the entire test to be run mulitple times with different parameters for HIDDEN_LAYERS, LEARNING_RATE, EPOCHS, LR_DECAY.  Set this up as an array so mulitple runs can easily be generated.

The HIDDEN_LAYERS is actually an array that defines multiple hidden layers with the number of neurons per hidden layer.  Ex, [32, 16, 8]


Also allow for different activation functions.

