- A **model** is a [function](Function.md) that **approximates the relationship** between input data and output predictions.

Given a dataset:
$$
\mathcal{D} = \{(\mathbf{x}_i, y_i) \mid \mathbf{x}_i \in \mathbb{R}^n, y_i \in \mathcal{Y}, i = 1, \dots, m\}
$$
where:
- $\mathcal{x_i}$ is an input (feature vector)
- $\mathcal{y_i}$ is the target (label or output)
- $\mathcal{m}$ is the number of training examples (dataset size)
- $\mathcal{Y}$ is the set of possible outputs (e.g., real numbers for regression, class labels for classification).
a **model** is a function $f: \mathbb{R}^n \to \mathcal{Y}$ that maps an input $\mathcal{x}$ to an output prediction $\hat{y}$:
$$
\hat{y} = f(\mathbf{x}; \theta)
$$
where:
- $\theta$ is the model parameters, which are intrinsic characteristics of the model.

