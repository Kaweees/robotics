- A **model** $f$ is a [function](Function.md) that **approximates the relationship** between a dataset of input-output pairs and output predictions.
Given a dataset $\mathcal{D}$ of input-output pairs:
$$
\mathcal{D} = \{(\mathbf{x}_i, y_i) \mid \mathbf{x}_i \in \mathbb{R}^N, y_i \in \mathcal{Y}, i = 1, \dots, \mathcal{m}\}
$$
where:
- $N \in \mathbb{N}$ is the number of [features](Feature.md) the input data has
- $\mathcal{m} \in \mathbb{N}$ is the size of the dataset
- $\mathcal{Y}$ is the set of possible outputs (e.g., real numbers for regression, class labels for classification).
- $\mathbf{x}_i \in \mathbb{R}^N$ is the $i$-th input (feature vector)
- $y_i \in \mathcal{Y}$ is the $i$-th target (label or output)

A **model** $f$ is a function $f: \mathbb{R}^N \to \mathcal{Y}$ that maps an input $\mathbf{x}$ to an output prediction $\hat{y}$:
$$
\hat{y} = f(\mathbf{x}; \theta)
$$
where:
- $\theta \in \mathbb{R}^p$ is the model parameters, which are intrinsic characteristics of the model used to make predictions.
- $\mathbf{x} \in \mathbb{R}^N$ is the input (feature vector)
- $\hat{y} \in \mathcal{Y}$ is the predicted output
