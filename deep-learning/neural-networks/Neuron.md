- A **neuron (aka perceptron)** $a$ is a generalization of a [linear classifier](Linear%20Classifier.md), incorporating a nonlinear activation function.

The [pre-activation (aka logits)](Logits.md) $z$ is the linear combination of the input and the weights, plus the bias.
$$
z = \mathbf{w}^T\mathbf{x} + b
$$
The pre-activation $z$ is then passed through the [activation function](Activation%20Function.md) $\sigma$ to produce the neuron's output:
$$
a = \sigma(z)
$$
Unlike the linear classifier, which directly maps to a class label, the neuron’s output is continuous, making it suitable for deeper compositions.

where:
A neuron is a function $g:Rn→Rg$: $\mathbb{R}^n \to \mathbb{R}$ of the form:

g(x)=σ(wTx+b)g(\mathbf{x}) = \sigma(\mathbf{w}^T \mathbf{x} + b)



- x∈Rn\mathbf{x} \in \mathbb{R}^n is the input vector.
- w∈Rn\mathbf{w} \in \mathbb{R}^n is the weight vector.
- b∈Rb \in \mathbb{R} is the bias term.
- σ:R→R\sigma: \mathbb{R} \to \mathbb{R} is a **nonlinear activation function**, such as:

