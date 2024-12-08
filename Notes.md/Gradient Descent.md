### Gradient Descent
Used to minimize the $(error|difference)$ between actual value and predicted value. It is used to train Neural Networks.
> Formula:

$$ w = w - lr.\frac {\partial{L}} {\partial{w}}$$

- $w$ : Weights
- $lr$: Learning Rate
- $L$: Loss function $(MSE)$

Note :\
If $\frac {\partial{L}} {\partial{w}}$ is positive the cost functions is going Up.

If $\frac {\partial{L}} {\partial{w}}$ is negative the cost functions is going down.

#### Types of Gradient Descent
- Batch
- Stochastic 
- Mini-Batch
