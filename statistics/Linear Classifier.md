- A **linear classifier** is a [linear model](Model.md) that maps an input vector $\mathbf{x} \in \mathbb{R}^n$ to a discrete class label using a linear decision boundary.
$$
z(\mathbf{x}) = \operatorname{sign}(\mathbf{w}^T \mathbf{x} + b)
$$
where:
- $\mathbf{x} \in \mathbb{R}^n$ is the input feature vector.
- $\mathbf{w} \in \mathbb{R}^n$ is the weight vector, which determines the orientation of the decision boundary.
- $b \in \mathbb{R}$ is the bias term, which shifts the decision boundary.
- $⁡\operatorname{sign}$ is the sign function, defined as:
$$
\operatorname{sign}(z) = \begin{cases} 1, & z \geq 0 \\ -1, & z < 0 \end{cases}
$$

### **3. Definition of a Neural Network**

A **neural network** is a composition of multiple neurons arranged in layers.

#### **Definition: Neural Network**

A neural network is a function F:Rn→RmF: \mathbb{R}^{n} \to \mathbb{R}^{m} with LL layers, where each layer consists of a collection of neurons. It is defined recursively:

h(l)=σ(W(l)h(l−1)+b(l)),∀l∈{1,2,…,L}\mathbf{h}^{(l)} = \sigma(W^{(l)} \mathbf{h}^{(l-1)} + \mathbf{b}^{(l)}), \quad \forall l \in \{1, 2, \dots, L\}

where:

- h(0)=x\mathbf{h}^{(0)} = \mathbf{x} is the input vector.
- W(l)∈Rdl×dl−1W^{(l)} \in \mathbb{R}^{d_{l} \times d_{l-1}} is the weight matrix for layer ll.
- b(l)∈Rdl\mathbf{b}^{(l)} \in \mathbb{R}^{d_l} is the bias vector for layer ll.
- h(l)∈Rdl\mathbf{h}^{(l)} \in \mathbb{R}^{d_l} is the output of layer ll (i.e., activations).
- σ\sigma is the activation function applied elementwise.

The final output h(L)\mathbf{h}^{(L)} represents either a class probability distribution (in classification) or a continuous value (in regression). If classification is required, a softmax function is often applied:

F(x)=softmax⁡(h(L))F(\mathbf{x}) = \operatorname{softmax}(\mathbf{h}^{(L)})

where:

softmax⁡(z)i=ezi∑j=1mezj\operatorname{softmax}(\mathbf{z})_i = \frac{e^{z_i}}{\sum_{j=1}^{m} e^{z_j}}

for i∈{1,…,m}i \in \{1, \dots, m\}.

---

### **Final Explanation of the Math Used**

1. **Dot Product wTx\mathbf{w}^T \mathbf{x}**  
    This computes a weighted sum of the input features, determining the decision boundary.
2. **Bias Term bb**  
    This allows shifting the decision boundary without affecting the weight vector.
3. **Activation Function σ\sigma**  
    It introduces non-linearity, allowing the model to learn more complex decision boundaries beyond linear separation.
4. **Layer-wise Transformation**  
    Each layer transforms its input using matrix multiplication and a non-linearity, enabling hierarchical feature learning.
5. **Softmax Function**  
    Converts the final layer’s outputs into a probability distribution for classification.

This mathematical framework forms the foundation of modern neural networks.


