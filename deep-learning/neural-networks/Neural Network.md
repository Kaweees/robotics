- A **neural network (nn)** $F: \mathbb{R}^{n} \to \mathbb{R}^{m}$ is a composition of [neurons](Neuron.md) arranged in layers $L$, to [model](../../statistics/Model.md) complex patterns in data.
![neural network.png](../../images/neural%20network.png)

$$
F^L(\ldots F^1(F^0(x)))
$$

A sequence of layer dimensions:
$$
d_0, d_1, d_2, \dots, d_L
$$
where:
- $d_0 \in \mathbb{N}$ is the dimension of the input layer
- $d_L \in \mathbb{N}$ is the dimension of the output layer


A set of weight matrices and bias vectors:
$$
W^{(l)} \in \mathbb{R}^{d_l \times d_{l-1}}, \quad b^{(l)} \in \mathbb{R}^{d_l}, \quad \text{for } l = 1, 2, \dots, L
$$
where:
- each $ W^{(l)} $ represents the transformation of the activations from the previous layer, and $ b^{(l)} $ is a bias term.

3. A set of activation functions $ \sigma^{(l)}: \mathbb{R}^{d_l} \to \mathbb{R}^{d_l} $, which are element-wise nonlinear functions applied after each affine transformation.

Thus, the neural network function $ f(x) $ is given recursively as:
$$
a^{(0)} = x
$$
$$
z^{(l)} = W^{(l)} a^{(l-1)} + b^{(l)}, \quad \forall l = 1, \dots, L
$$
$$
a^{(l)} = \sigma^{(l)}(z^{(l)}), \quad \forall l = 1, \dots, L-1
$$
$$
f(x) = a^{(L)} = z^{(L)}.
$$
where:
- $ a^{(l)} $ are the activations (outputs of each layer),
- $ z^{(l)} $ are the pre-activation values (before applying activation functions),
- $ \sigma^{(l)} $ is the activation function (such as ReLU or sigmoid).



Given a neural network $F: \mathbb{R}^n \to \mathbb{R}^m$ with $L$ layers, the output of the $l$-th layer is given by:
$$
\mathbf{h}^{(l)} = \sigma(W^{(l)} \mathbf{h}^{(l-1)} + \mathbf{b}^{(l)}), \quad \forall l \in \{1, 2, \dots, L\}
$$
where:
- $\mathbf{h}^{(l)} \in \mathbb{R}^{d_l}$ is the output of the $l$-th layer
- $W^{(l)} \in \mathbb{R}^{d_l \times d_{l-1}}$ is the weight matrix for the $l$-th layer
- $\mathbf{b}^{(l)} \in \mathbb{R}^{d_l}$ is the bias vector for the $l$-th layer
- $\sigma$ is the activation function

### **Definition of a Neural Network**
A **Neural Network** can be rigorously defined as a function $ f: \mathbb{R}^{d_0} \to \mathbb{R}^{d_L} $ parameterized by a sequence of weight matrices and bias vectors, where the function is computed as a composition of layer-wise affine transformations followed by nonlinear activation functions.



2.
---

### **Definition of Forward Propagation**
**Forward propagation** is the process of computing the output $ f(x) $ for a given input $ x $ by applying the sequence of transformations defined above.

Mathematically, forward propagation is performed iteratively using the equations:

1. **Input Layer:**
   $$
   a^{(0)} = x
   $$
   The input to the network is simply the given data point.

2. **Hidden Layers (for $ l = 1 $ to $ L-1 $):**
   $$
   z^{(l)} = W^{(l)} a^{(l-1)} + b^{(l)}
   $$
   $$
   a^{(l)} = \sigma^{(l)}(z^{(l)})
   $$
   where:
   - $ W^{(l)} $ applies a linear transformation to the previous layer’s activations,
   - $ b^{(l)} $ shifts the transformation,
   - $ \sigma^{(l)} $ introduces nonlinearity.

3. **Output Layer:**
   $$
   z^{(L)} = W^{(L)} a^{(L-1)} + b^{(L)}
   $$
   $$
   f(x) = z^{(L)}
   $$
   Here, typically, no activation function is applied (or a specific function such as softmax is used in classification problems).

---

### **Explanation of the Math**
- The **weight matrix** $ W^{(l)} $ represents the learnable parameters that determine how much influence each neuron in layer $ l-1 $ has on the neurons in layer $ l $.
- The **bias vector** $ b^{(l)} $ accounts for an additional degree of freedom that shifts the activation independently of the input.
- The **affine transformation** $ z^{(l)} = W^{(l)} a^{(l-1)} + b^{(l)} $ represents a linear mapping from one layer to the next.
- The **activation function** $ \sigma^{(l)}(z^{(l)}) $ introduces nonlinearity, ensuring that the network can approximate complex functions.
- The **output layer** may use an identity function (for regression) or a specialized function like softmax (for classification).

Would you like me to add derivations for specific activation functions like ReLU, sigmoid, or softmax?
