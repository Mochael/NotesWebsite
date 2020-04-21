# Confidence Intervals for Known Distributions and Pivotal Values (also Credible Intervals)

Created By: Michael Kronovet
Last Edited: Apr 13, 2020 2:45 AM

A $1-\alpha$ confidence interval for $\theta$ is an interval  $(L,U)$ where we have the following:

$$L=g_{L}\left(X_{1}, \ldots, X_{n}\right) \text{ and } U=g_{U}\left(X_{1}, \ldots, X_{n}\right) \text{ such that } P(\theta \in(L, U)) \geq 1-\alpha$$

- The confidence interval itself is random, since $L$ and $U$ are functions of random variables
- The parameter $\theta$ is not random.
- A confidence interval is a probability statement that a random interval captures a fixed parameter.

### Pivotal quantity

A random variable  $V = g(X_1,\ldots, X_n,\theta )$ is a pivotal quantity if its distribution does not depend on the unknown parameter $\theta$

### Finding Confidence Intervals

1. Find a pivotal quantity $V$
2. Choose $a$ and $b$ such that $P(a<V<b) \geq 1-\alpha$ 
    - This can be done by choosing $a$ and $b$ such that $P(V<a) = P(V>b) = \frac{\alpha}{2}$
3. Could also do something very similar for a one-sided confidence interval (just need either $a$ or $b$)

# Credible Interval

A credible interval is the Bayesian equivalent of the confidence interval where the estimated interval is dependent on the prior distribution

- In confidence intervals we treat the parameter as a fixed value and the bounds as random variables
- In credible intervals, the estimated parameter is treated as a random variable while the bounds are considered fixed

Any random variable following the posterior distribution $\pi(\theta|y_1,\ldots, y_n)$ will fall in the credible interval with probability $1-\alpha$

$$\int_{\mathcal{C}} \pi(\theta | y_1,\ldots, y_n) d \theta=1-\alpha \Longrightarrow P\left(a \leq \theta \leq b | y_{1}, \ldots, y_{n}\right)=1-\alpha$$