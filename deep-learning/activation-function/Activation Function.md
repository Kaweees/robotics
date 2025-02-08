- The **Activation Function** $\sigma$ is a function $\sigma: \mathbb{R} \to \mathbb{R}$ that applies a nonlinear transformation to the [pre-activation](Logits.md) $z$ to produce the neuron's output $a$, allowing the [model](Model.md) to learn complex patterns.
   - Without it, multi-layer neural networks compute nested linear transformations, which are equivalent to a single linear transformation.

The activation function $\sigma$ is applied elementwise to the pre-activation to produce the neuron's output, which is referred to as the **activation** $a$:
$$
a = \sigma(z)
$$
