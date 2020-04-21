# Indian Buffet Process

## Motivation

- Dirichlet Process can give us clusters for data points, but it cannot cluster data into overlapping clusters.
- In many applications, data points exhibit properties of multiple latent features:
    - Images contain multiple objects, movies contain aspects of multiple genres, etc.
- Can we model a system where:
    - we allow each data point to exhibit multiple latent features, to varying degrees
    - we make the number of features unbounded a posteriori (like with the Dirichlet Process)

## The Process

![Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_12.11.00_PM.png](Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_12.11.00_PM.png)

- $m_{k}$ is the number of previous customers who have sampled the dish.

$$\text{ If } Z \text{ follows this process then } Z \sim IBP(\alpha)$$

## Beta Bernoulli Model

- The Beta-Bernoulli model where we take the limit as the number of latent features goes to infinity describes the Indian Buffet Process

![Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.33.34_PM.png](Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.33.34_PM.png)

![Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.33.41_PM.png](Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.33.41_PM.png)

## Infinite Gamma-Poisson Process

![Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.22.16_PM.png](Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.22.16_PM.png)

![Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.22.26_PM.png](Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.22.26_PM.png)

![Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.21.52_PM.png](Indian%20Buffet%20Process/Screen_Shot_2020-04-15_at_1.21.52_PM.png)