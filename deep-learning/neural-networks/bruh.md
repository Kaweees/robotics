


$$
\mathbf{h}^{(l)} = \sigma(W^{(l)} \mathbf{h}^{(l-1)} + \mathbf{b}^{(l)}), \quad \forall l \in \{1, 2, \dots, L\}
$$
$$
a_0^{(1)} = \sigma(w_{0,0} a_0^{(0)} + w_{0,1} a_1^{(0)} + \cdots + w_{0,n} a_n^{(0)} + b_0)
$$
$$
\begin{bmatrix}
w_{0,0} & w_{0,1} & \cdots & w_{0,n} \\
w_{1,0} & w_{1,1} & \cdots & w_{1,n} \\
\vdots & \vdots & \ddots & \vdots \\
w_{k,0} & w_{k,1} & \cdots & w_{k,n}
\end{bmatrix}
\begin{bmatrix}
a_0^{(0)} \\
a_1^{(0)} \\
\vdots \\
a_n^{(0)}
\end{bmatrix}
+
\begin{bmatrix}
b_0 \\
b_1 \\
\vdots \\
b_n
\end{bmatrix}
$$

$$
X = \begin{bmatrix}
k_1 \\
k_2 \\
\vdots \\
k_n
\end{bmatrix}

W = \begin{bmatrix}
w_{11} & w_{12} & \dots & w_{1n} \\
w_{21} & w_{22} & \dots & w_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
w_{m1} & w_{m2} & \dots & w_{mn}
\end{bmatrix}
$$

$$
\begin{bmatrix} w^1_{11} & w^1_{12} & w^1_{13} \\ w^1_{21} & w^1_{22} & w^1_{23} \\ w^1_{31} & w^1_{32} & w^1_{33} \\ w^1_{41} & w^1_{42} & w^1_{43} \\ w^1_{51} & w^1_{52} & w^1_{53} \end{bmatrix}
$$

A neural network is a function \( F: \mathbb{R}^{n} \to \mathbb{R}^{m} \) with \( L \) layers, where each layer consists of a collection of neurons. It is defined recursively:



where:
- $F^L$ is the last layer
- $F^1$ is the first layer
- $F^0$ is the input layer
- $x$ is the input data

### **1. Definition of a Linear Classifier**

A **linear classifier** is a function that maps an input vector \( \mathbf{x} \in \mathbb{R}^n \) to a discrete class label using a linear decision boundary. Formally, we define a linear classifier as follows:

#### **Definition: Linear Classifier**
A linear classifier is a function \( f: \mathbb{R}^n \to \{-1, 1\} \) of the form:

\[
f(\mathbf{x}) = \operatorname{sign}(\mathbf{w}^T \mathbf{x} + b)
\]

where:
- \( \mathbf{x} \in \mathbb{R}^n \) is the input vector.
- \( \mathbf{w} \in \mathbb{R}^n \) is the weight vector, which determines the orientation of the decision boundary.
- \( b \in \mathbb{R} \) is the bias term, which shifts the decision boundary.
- \( \operatorname{sign} \) is the sign function, defined as:

  \[
  \operatorname{sign}(z) =
  \begin{cases}
  1, & z \geq 0 \\
  -1, & z < 0
  \end{cases}
  \]

### **2. Definition of a Neuron in a Neural Network**

A **neuron** in a neural network is a generalization of a linear classifier, incorporating a nonlinear activation function.

#### **Definition: Neuron**
A neuron is a function \( g: \mathbb{R}^n \to \mathbb{R} \) of the form:

\[
g(\mathbf{x}) = \sigma(\mathbf{w}^T \mathbf{x} + b)
\]

where:
- \( \mathbf{x} \in \mathbb{R}^n \) is the input vector.
- \( \mathbf{w} \in \mathbb{R}^n \) is the weight vector.
- \( b \in \mathbb{R} \) is the bias term.
- \( \sigma: \mathbb{R} \to \mathbb{R} \) is a **nonlinear activation function**, such as:
  - **Sigmoid function:** \( \sigma(z) = \frac{1}{1 + e^{-z}} \)
  - **ReLU (Rectified Linear Unit):** \( \sigma(z) = \max(0, z) \)
  - **Hyperbolic tangent (Tanh):** \( \sigma(z) = \tanh(z) \)

Unlike the linear classifier, which directly maps to a class label, the neuron’s output is continuous, making it suitable for deeper compositions.

### **3. Definition of a Neural Network**

A **neural network** is a composition of multiple neurons arranged in layers.

#### **Definition: Neural Network**

\[
\mathbf{h}^{(l)} = \sigma(W^{(l)} \mathbf{h}^{(l-1)} + \mathbf{b}^{(l)}), \quad \forall l \in \{1, 2, \dots, L\}
\]

where:
- \( \mathbf{h}^{(0)} = \mathbf{x} \) is the input vector.
- \( W^{(l)} \in \mathbb{R}^{d_{l} \times d_{l-1}} \) is the weight matrix for layer \( l \).
- \( \mathbf{b}^{(l)} \in \mathbb{R}^{d_l} \) is the bias vector for layer \( l \).
- \( \mathbf{h}^{(l)} \in \mathbb{R}^{d_l} \) is the output of layer \( l \) (i.e., activations).
- \( \sigma \) is the activation function applied elementwise.

The final output \( \mathbf{h}^{(L)} \) represents either a class probability distribution (in classification) or a continuous value (in regression). If classification is required, a softmax function is often applied:

\[
F(\mathbf{x}) = \operatorname{softmax}(\mathbf{h}^{(L)})
\]

where:

\[
\operatorname{softmax}(\mathbf{z})_i = \frac{e^{z_i}}{\sum_{j=1}^{m} e^{z_j}}
\]

for \( i \in \{1, \dots, m\} \).

---

### **Final Explanation of the Math Used**
1. **Dot Product \( \mathbf{w}^T \mathbf{x} \)**
   This computes a weighted sum of the input features, determining the decision boundary.
2. **Bias Term \( b \)**
   This allows shifting the decision boundary without affecting the weight vector.
3. **Activation Function \( \sigma \)**
   It introduces non-linearity, allowing the model to learn more complex decision boundaries beyond linear separation.
4. **Layer-wise Transformation**
   Each layer transforms its input using matrix multiplication and a non-linearity, enabling hierarchical feature learning.
5. **Softmax Function**
   Converts the final layer’s outputs into a probability distribution for classification.

This mathematical framework forms the foundation of modern neural networks.


- A **Neural Network (NN)** is an interconnected layers of [neurons](Neuron.md) that perform mathematical operations to detect patterns in data

$$
a_0^{(1)} = \sigma(w_{0,0} a_0^{(0)} + w_{0,1} a_1^{(0)} + \cdots + w_{0,n} a_n^{(0)} + b_0)
$$
$$
\begin{bmatrix}
w_{0,0} & w_{0,1} & \cdots & w_{0,n} \\
w_{1,0} & w_{1,1} & \cdots & w_{1,n} \\
\vdots & \vdots & \ddots & \vdots \\
w_{k,0} & w_{k,1} & \cdots & w_{k,n}
\end{bmatrix}
\begin{bmatrix}
a_0^{(0)} \\
a_1^{(0)} \\
\vdots \\
a_n^{(0)}
\end{bmatrix}
+
\begin{bmatrix}
b_0 \\
b_1 \\
\vdots \\
b_n
\end{bmatrix}
$$

$$
X = \begin{bmatrix}
k_1 \\
k_2 \\
\vdots \\
k_n
\end{bmatrix}

W = \begin{bmatrix}
w_{11} & w_{12} & \dots & w_{1n} \\
w_{21} & w_{22} & \dots & w_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
w_{m1} & w_{m2} & \dots & w_{mn}
\end{bmatrix}
$$

The matrix-vector dot product in neurons comes from the way artificial neurons process inputs using linear algebra. This operation originates from the **weighted sum** computation in biological and artificial neural networks.

### **Derivation from the Neuron Model**
A simple artificial neuron takes multiple inputs, weights them, applies a bias, and then passes the result through an activation function.

1. **Inputs and Weights**
   Consider a neuron with \( n \) inputs, represented as a vector:
   \[
   \mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}
   \]
   Each input has an associated weight:
   \[
   \mathbf{w} = \begin{bmatrix} w_1 \\ w_2 \\ \vdots \\ w_n \end{bmatrix}
   \]

2. **Weighted Sum**


3. **Activation Function**
   The output is then passed through a non-linear activation function \( f(z) \), such as ReLU or sigmoid:
   \[
   y = f(z)
   \]

### **Extending to Multiple Neurons (Matrix Form)**
When dealing with multiple neurons in a **layer**, each neuron has its own set of weights. If there are \( m \) neurons and \( n \) inputs, we represent all neuron weights as a **weight matrix**:

\[
W =
\begin{bmatrix}
w_{11} & w_{12} & \dots & w_{1n} \\
w_{21} & w_{22} & \dots & w_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
w_{m1} & w_{m2} & \dots & w_{mn}
\end{bmatrix}
\]

The inputs are still represented as a column vector:

\[
\mathbf{x} =
\begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}
\]

The weighted sum for all neurons can be computed as:

\[
\mathbf{z} = W \mathbf{x} + \mathbf{b}
\]

where \( \mathbf{b} \) is a bias vector. This is a **matrix-vector multiplication**, which generalizes the dot product operation to multiple neurons.

### **Why Use This Form?**
- **Efficiency:** Matrix-vector operations are highly optimized in hardware (e.g., GPUs).
- **Scalability:** It naturally extends to multiple neurons and layers in deep learning.
- **Compact Representation:** Using linear algebra simplifies expressing neural network operations.

Thus, the matrix-vector dot product in neurons comes from the fundamental **weighted sum** operation in artificial neurons and is generalized to matrix form for multiple neurons in a layer.
