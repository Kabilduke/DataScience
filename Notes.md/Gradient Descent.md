### Gradient Descent
Used to minimize the $(error|difference)$ between actual value and predicted value. It is used to train Neural Networks. This helps to find the gobal minimum in higher dimensions more efficiently.

> Formula:

$$ w = w - lr.\frac {\partial{L}} {\partial{w}}$$

- $w$ : Weights
- $lr$: Learning Rate
- $L$: Cost function $(MSE)$

Note :\
If $\frac {\partial{L}} {\partial{w}}$ is positive the cost functions is going $Up$.

If $\frac {\partial{L}} {\partial{w}}$ is negative the cost functions is going $Down$.

#### Types of Gradient Descent
- Batch
- Stochastic $(Non-Convex)$
- Mini-Batch
