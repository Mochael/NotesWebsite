# Conjugate Priors

Suppose our prior follows a beta distribution $p(\theta) \sim Beta(\alpha,\beta)$ and we have a binomial likelihood $p(x|\theta)$.
$$
p(\theta | x) = p(x | \theta) p(\theta)
$$
Since the beta is a conjugate prior for the binomial likelihood, we can show that $p(\theta | x) \sim Beta(k+\alpha,n-k+\beta)$.

- We don't need to actually calculate this $p(\theta | x)$ with the computer since it just follows a known distribution and the MAP estimate for this distribution will be of the same form as the optimal estimate of $p(\theta)$, just with the adjusted $k+\alpha, \ n-k+\beta$ values.