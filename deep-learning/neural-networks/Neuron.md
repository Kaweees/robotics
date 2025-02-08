- A **neuron (aka perceptron)** $a: \mathbb{R}^n \to \mathbb{R}$ is a generalization of a [linear classifier](Linear%20Classifier.md), incorporating a nonlinear activation function.

The [pre-activation (aka logits)](Logits.md) $z$ is the linear combination of the input and the weights, plus the bias.
$$
z = \mathbf{w}^T\mathbf{x} + b
$$
The pre-activation $z$ is then passed through the [activation function](Activation%20Function.md) $\sigma$ to produce the neuron's **activation** $a$:
$$
a = \sigma(z)
$$
Unlike the linear classifier, which directly maps to a class label, the neuron’s output is continuous, making it suitable for deeper compositions.
