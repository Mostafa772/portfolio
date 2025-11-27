---
layout: default
title: Neural Network From Scratch
parent: Projects
---

[← Back to Home](../README.md)

# Neural Network From Scratch in NumPy

**Tech Stack:** Python, NumPy, Matplotlib  
**Status:** Completed (Nov 2024 -- May 2025)  
**Repository:** [View Code on GitHub](YOUR_GITHUB_LINK_HERE)

## 📌 Overview
Understanding modern Deep Learning frameworks (like PyTorch) requires a deep grasp of the underlying mathematics. This project implements a Feed-Forward Neural Network entirely from scratch using **NumPy**, avoiding any auto-differentiation libraries.

## ⚙️ Key Technical Features
1.  **Forward Propagation:** Implemented matrix multiplications for weighted sums and bias additions.
2.  **Activation Functions:** Manually coded Sigmoid, ReLU, and Tanh, along with their derivatives.
3.  **Backpropagation:** Calculated gradients using the Chain Rule to update weights and biases.
4.  **Optimization:** Implemented Stochastic Gradient Descent (SGD).

## 📊 Results
I tested the model on the MONK benchmark datasets.
* **MONK1:** 99% Test Accuracy
* **MONK2:** 95% Test Accuracy

## 💻 Code Snippet (Backpropagation Logic)
```python
def backward(self, output_gradient, learning_rate):
    weights_gradient = np.dot(output_gradient, self.input.T)
    input_gradient = np.dot(self.weights.T, output_gradient)
    
    self.weights -= learning_rate * weights_gradient
    self.bias -= learning_rate * output_gradient
    return input_gradient