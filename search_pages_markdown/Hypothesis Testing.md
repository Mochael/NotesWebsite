# Hypothesis Testing

## Hypothesis Testing Framework

$$H_0 : \theta \in \Theta_0 \text{ and } H_a : \theta \in \Theta_1 \text{ where } \Theta_0 \cap \Theta_1 = \emptyset$$

1. Calculate a test statistic  $T(X_1,...,X_n)$
2. Select a rejection region $R$ where if $T(X_1,...,X_n) \in R$ then we reject the null, otherwise we retain it

$$power(θ^*) = P(T(X_1,...,X_n) \in R \text{ if } θ=θ^*)$$

$$\text{ where } \theta \text{ is the parameter of interest and } \theta^* \text{ is a potential value of the parameter.}$$

We want $power(\theta^*)$ to be small when $\theta^* \in \Theta_0$  (to minimize the chance of a false positive) and large when $\theta^* \in \Theta_1$ (to minimize the chance of a false negative).

$$\text{Significance level } \alpha = \max_{\theta^* \in \Theta_0} power(\theta^*)$$

- We can select a value of alpha and then solve for a rejection region that would satisfy that alpha or vice versa

## P-Value

The definition of the p-value is often expressed as “the probability of observing data as or more extreme than what was observed, if the null hypothesis is true.”

Suppose we have a test that rejects when $T(X_1,...,X_n) \geq c$ and we observe a sample of data $(x_1,...,x_n)$ then we define the p-value as follows:

$$p(x_1,...x_n) = \max_{\theta^* \in \Theta_0} P(T(X_1,...X_n) \geq T(x_1,...,x_n) \text{ if } \theta = \theta^*)$$

### How p-values can be used to test hypotheses

$$\max_{\theta^* \in \Theta_0} P(T(X_1,...X_n) \geq c \text{ if } \theta = \theta^*) \text{ is a decreasing function of } c$$

Let $c_{\alpha}$ be the cutoff at which we reject the null for an $\alpha$-level test, i.e. reject the null if $T(X_1,...X_n) \geq c_{\alpha}$ and $\max_{\theta^* \in \Theta_0} P(T(X_1,...X_n) \geq c_{\alpha} \text{ if } \theta = \theta^*)=\alpha$. Then, if we observe $(x_1,...x_n)$ we reject the null if $T(x_1,...,x_n) \geq c_{\alpha}$.

$$\implies p(x_1,...x_n) = \max_{\theta^* \in \Theta_0} P(T(X_1,...X_n) \geq T(x_1,...,x_n) \text{ if } \theta = \theta^*)$$

$$\leq \max_{\theta^* \in \Theta_0} P(T(X_1,...X_n) \geq c_{\alpha} \text{ if } \theta = \theta^*)$$

$$= \alpha$$

Therefore $p(x_1,...,x_n) \leq \alpha \iff T(x_1,...,x_n) \geq c_{\alpha}$ and these rejection conditions are equivalent.

- We can interpret the p-value as the smallest alpha for which we would reject the null.

### Explaining How P-Value is Area under the curve from critical point

Suppose we have that $z = T(x_1,...x_n)$ and $\theta^*$ is the max value for the power in the null set.

$$\max_{\theta^* \in \Theta_0} P(T(X_1,...X_n) \geq z \text{ if } \theta = \theta^*) = 1 - F_{T(X_1,...,X_n)}(z) \text{ where } F_{R} \text{ is the cdf of } R$$

Tests such as the Z-test, T-test, and F-test assume the distribution of our test statistic, which allows us to calculate the cdf to determine p-values.

**Example**

$$H_0: \theta = \theta_0, H_1: \theta < \theta_0,$$

$$p(x_1,...,x_n) = P(T(X_1,...,X_n) < T(x_1,...,x_n) \text{ where } \theta=\theta_0)$$

Intuition: Assuming the null is true, what is the probability of getting a test statistic that equivalently or more extremely supports the alternative hypothesis?

![](/Users/michaelkronovet/Downloads/download (1).png)

