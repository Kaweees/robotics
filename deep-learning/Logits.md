- A **logit** (aka pre-activation) represents how strongly a [model](Model) believes a particular datapoint $\mathbf{x}$ from a dataset $\mathcal{D}$ belongs to each possible outcome.
$$
z = w_1 x_1 + w_2 x_2 + \dots + w_n x_n + b = \sum_{n=1}^{N} w_n x_n + b
$$
where:
- $N$ is the number of [features](Feature.md) (aka dimensions) of the input vector
- $w_n$ is the [weight](Weight.md) for the $n$-th feature
- $x_n$ is the value of the datapoint's $n$-th feature
- $b$ is the [bias](Bias.md)
