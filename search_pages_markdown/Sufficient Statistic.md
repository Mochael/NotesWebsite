# Sufficient Statistic

## Definition

If $Y_1,\ldots, Y_n$ are iid samples drawn from a distribution with parameter $\theta$ then a statistic $U = U(Y_1,\ldots, Y_n)$ is said to be sufficient for $\theta$ iff the conditional distribution of the data $Y_1,\ldots, Y_n|U$ does not depend on the parameter $\theta$.

## Method to Find Them

If the likelihood can be expressed as the following, then $U(Y_1,\ldots, Y_n)$ is a sufficient statistic

$$L\left(\theta ; y_{1}, y_{2}, \ldots, y_{n}\right)=g\left(U\left(y_{1}, y_{2}, \ldots, y_{n}\right), \theta\right) h\left(y_{1}, y_{2}, \ldots, y_{n}\right)$$

## Minimum Sufficient Statistic

A minimal sufficient statistic $T(Y_1,\ldots, Y_n)$ is a sufficient statistic that can be expressed as some function of any other sufficient statistic $\tilde{T}(Y_1,\ldots, Y_n)$:

$$T\left(y_{1}, y_{2}, \ldots, y_{n}\right)=g\left(\tilde{T}\left(y_{1}, y_{2}, \ldots, y_{n}\right)\right)$$

### Finding a minimal sufficient statistic

Let $x_1,\ldots, x_n \sim f(x;\theta)$ and $y_1,\ldots, y_n \sim f(x;\theta)$ be two samples from the same distribution and $T$ be a statistic. Suppose:

$$R=R\left(x_{1}, \ldots, x_{n}, y_{1}, \ldots, y_{n}, \theta\right)=\frac{f\left(x_{1}, \ldots, x_{n} ; \theta\right)}{f\left(y_{1}, \ldots, y_{n} ; \theta\right)}=\frac{L\left(\theta ; x_{1}, \ldots, x_{n}\right)}{L\left(\theta ; y_{1}, \ldots, y_{n}\right)}$$

If for all $\theta$ where $R$ is defined we have:

$$\text{R does not depend on } \theta \Longleftrightarrow T\left(x_{1}, \ldots, x_{n}\right)=T\left(y_{1}, \ldots, y_{n}\right)$$

then $T$ is a minimal sufficient statistic.

### Rao - Blackwell Theorem

Let $\hat{\theta}$ be an unbiased estimator for $\theta$ such that $V(\hat{\theta})<\infty$. If $U$ is a sufficient statistic for $\theta$, then for all $\theta$: 

$$E\left(E(\hat{\theta} | U)\right)=\theta \text { and } V\left(E(\hat{\theta} | U)\right) \leq V(\hat{\theta})$$