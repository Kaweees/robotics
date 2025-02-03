- A **loss function** measures how well a [model](Model.md)'s predictions match the true outputs.
Given a dataset:
$$
\{(\mathbf{x}_i, \mathbf{y}_i)\}_{i=1}^{N}
$$
The loss function $\mathcal{L}$ is:
$$
\mathcal{L} = \frac{1}{N} \sum_{i=1}^{N} \ell(f(\mathbf{x}_i), \mathbf{y}_i)
$$
where $ℓ(y,y^)\ell(y, \hat{y})$ is a per-example loss function.

Common choices:
1. **Mean Squared Error (Regression)**:
$$
\ell(x^i; w) = \frac{1}{2}(z^i-y^i)^2
$$
2. **Dot product Loss**:
$$
\ell(x^i; w) = -(z^{i} \cdot  y^{i})
$$
3. **Cross-Entropy Loss (Classification, Softmax Output)**:
$$
\ell(y, \hat{y}) = -\sum_{j} y_j \log \hat{y}_j
$$

where yjy_j is the true probability and y^j\hat{y}_j is the predicted probability.

### **Explanation**

- The loss function quantifies prediction error.
- The goal of training is to minimize L\mathcal{L} via optimization methods like gradient descent.