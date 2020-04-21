# Gaussian Process

[Here is a very detailed explanation](https://towardsdatascience.com/understanding-gaussian-process-the-socratic-way-ba02369d804)

- A Gaussian Process (GP) is a collection of random variables of any finite number which have a joint Gaussian distribution
- Using a Gaussian Process we can generate data from the prior distribution as well as the posterior
- In the case below, $f$ is a Gaussian process with mean function $m(x)$ and covariance kernel $k(x_i,x_j)$

$$f(x) \sim GP(m,k) \\ \implies \text{we generate } \begin{bmatrix} f(x_1) \\  \vdots \\ f(x_n) \end{bmatrix} \sim N(\boldsymbol{\mu}, \mathbf{K}) \\ \text{where } \boldsymbol{\mu}_i = m(x_i) \text{ and } \mathbf{K}_{ij} = k(x_i,x_j)$$

[10-708 Lecture](../search_pics/lecture21-GP-compressed.pdf)

