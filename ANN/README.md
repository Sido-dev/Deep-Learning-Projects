# 🧠 Artificial Neural Network (ANN)

## 📌 Overview

Artificial Neural Networks (ANNs) are computational models inspired by the structure and functioning of the human brain. They form the foundation of Deep Learning and are capable of learning complex patterns from data to solve classification, regression, prediction, and pattern recognition problems.

---

# 🚀 What is Deep Learning?

Deep Learning is a subset of Machine Learning that uses Artificial Neural Networks with multiple layers to learn complex patterns from large amounts of data.

### Key Features
- Inspired by the human brain.
- Automatically learns features from data.
- Works well with structured and unstructured data.
- Powers technologies such as ChatGPT, image recognition, self-driving cars, and recommendation systems.

---

# 🧬 Biological Neuron

The human brain contains approximately **80–100 billion neurons** connected through a complex network.

### Components of a Biological Neuron

- **Dendrites** → Receive signals
- **Cell Body (Soma)** → Processes information
- **Axon** → Transmits signals
- **Synapse** → Connection between neurons

The biological neuron inspired the design of artificial neurons.

---

# 🤖 Artificial Neuron (Perceptron)

An Artificial Neuron is the basic building block of an ANN.

### Components

- Inputs (X₁, X₂, X₃ ...)
- Weights (W₁, W₂, W₃ ...)
- Bias (b)
- Activation Function
- Output

### Mathematical Representation

```math
z = (W₁X₁ + W₂X₂ + W₃X₃ + ... + b)
```

```math
Output = Activation(z)
```

---

# 🏗️ Artificial Neural Network Architecture

An ANN consists of:

### 1. Input Layer
Receives input features.

### 2. Hidden Layer(s)
Performs computations and feature extraction.

### 3. Output Layer
Produces the final prediction.

```text
Input Layer → Hidden Layer(s) → Output Layer
```

---

# ⚙️ Working of ANN

The learning process consists of two major steps:

### 1. Forward Propagation
Data moves from input layer to output layer.

### 2. Backpropagation
Error is propagated backward to update weights and biases.

---

# ➡️ Forward Propagation

Forward propagation is the process of passing input data through the network to generate predictions.

### Steps

1. Input data enters the network.
2. Weighted sum is calculated.
3. Activation function is applied.
4. Output is generated.

### Formula

```math
z = WX + b
```

```math
a = Activation(z)
```

---

# ⬅️ Backpropagation

Backpropagation helps the model learn from its mistakes.

### Steps

1. Calculate loss.
2. Compute gradients.
3. Update weights and biases.
4. Repeat until convergence.

### Purpose

Minimize prediction error by optimizing model parameters.

---

# ⚡ Activation Functions

Activation functions introduce non-linearity into neural networks.

Without activation functions, neural networks behave like simple linear models.

---

## 1️⃣ Sigmoid Activation Function

### Formula

```math
f(x)=\frac{1}{1+e^{-x}}
```

### Range

```text
(0,1)
```

### Advantages

- Outputs probability values.
- Useful for Binary Classification.

### Disadvantages

- Vanishing Gradient Problem.
- Not zero-centered.

### Use Case

Output layer for Binary Classification.

---

## 2️⃣ ReLU (Rectified Linear Unit)

### Formula

```math
f(x)=max(0,x)
```

### Range

```text
[0,∞)
```

### Advantages

- Fast computation.
- Reduces Vanishing Gradient Problem.
- Most commonly used activation function.

### Disadvantages

- Dying ReLU Problem.

### Use Case

Hidden Layers.

---

## 3️⃣ Tanh Activation Function

### Formula

```math
f(x)=\frac{e^x-e^{-x}}{e^x+e^{-x}}
```

### Range

```text
(-1,1)
```

### Advantages

- Zero-centered output.
- Stronger gradients than Sigmoid.

### Disadvantages

- Can still suffer from Vanishing Gradient.

### Use Case

Hidden Layers.

---

## 4️⃣ Softmax Activation Function

### Formula

```math
P(y_i)=\frac{e^{z_i}}{\sum_{j=1}^{n}e^{z_j}}
```

### Characteristics

- Produces probability distribution.
- Sum of probabilities equals 1.

### Use Case

Multi-Class Classification.

---

# 🎯 Choosing Activation Functions

| Problem Type | Hidden Layer | Output Layer |
|-------------|-------------|-------------|
| Binary Classification | ReLU | Sigmoid |
| Multi-Class Classification | ReLU | Softmax |
| Regression | ReLU | No Activation Function |

---

# 📉 Loss Functions

Loss Functions measure how far the model's predictions are from actual values.

The objective during training is to minimize the loss.

---

## Mean Squared Error (MSE)

Used in Regression Problems.

### Formula

```math
MSE=\frac{1}{n}\sum(y-\hat y)^2
```

### Applications

- House Price Prediction
- Sales Forecasting
- Temperature Prediction

---

## Binary Cross Entropy (Log Loss)

Used in Binary Classification Problems.

### Formula

```math
Loss=-(y\log(p)+(1-y)\log(1-p))
```

Where:

- y = Actual Value
- p = Predicted Probability

### Goal

Minimize Log Loss to improve prediction accuracy.

---

# 🔧 Optimizers

Optimizers update weights and biases to minimize loss.

---

## 1️⃣ Gradient Descent (GD)

Gradient Descent updates parameters using the entire dataset.

### Update Rule

```math
W_{new}=W_{old}-\eta \frac{\partial L}{\partial W}
```

Where:

- η = Learning Rate
- L = Loss Function

### Advantages

- Stable updates.
- Easy to understand.

### Disadvantages

- Slow for large datasets.

---

## 2️⃣ Stochastic Gradient Descent (SGD)

Updates weights after every training example.

### Advantages

- Faster convergence.
- Less memory usage.

### Disadvantages

- Noisy updates.

---

## 3️⃣ RMSProp

RMSProp uses adaptive learning rates.

### Advantages

- Faster convergence.
- Effective for Deep Neural Networks.

---

## 4️⃣ Adam Optimizer

Adam combines Momentum and RMSProp.

### Advantages

- Adaptive learning rates.
- Fast convergence.
- Handles sparse gradients efficiently.

### Why Adam?

Adam is the most commonly used optimizer in modern Deep Learning applications.

---

# 🔄 ANN Training Workflow

```text
Input Data
     ↓
Forward Propagation
     ↓
Prediction
     ↓
Loss Calculation
     ↓
Backpropagation
     ↓
Gradient Computation
     ↓
Optimizer Updates Weights
     ↓
Repeat Until Convergence
```

---

# 🌍 Applications of ANN

- Image Classification
- Object Detection
- Speech Recognition
- Natural Language Processing (NLP)
- Recommendation Systems
- Medical Diagnosis
- Fraud Detection
- Customer Churn Prediction
- Stock Market Forecasting
- Autonomous Vehicles

---

# 🎓 Key Takeaways

✅ Artificial Neural Networks are inspired by biological neurons.

✅ ANNs consist of Input, Hidden, and Output layers.

✅ Forward Propagation generates predictions.

✅ Backpropagation updates model weights.

✅ ReLU is the most commonly used activation function in hidden layers.

✅ Sigmoid is used for Binary Classification.

✅ Softmax is used for Multi-Class Classification.

✅ MSE is used for Regression tasks.

✅ Binary Cross Entropy is used for Classification tasks.

✅ Adam is the most widely used optimizer in Deep Learning.

---

# 🛠️ Technologies & Libraries

- Python
- NumPy
- Pandas
- TensorFlow
- Keras
- PyTorch
- Scikit-Learn
- Matplotlib
- Seaborn

---

## ⭐ If you found this repository useful, don't forget to star it!