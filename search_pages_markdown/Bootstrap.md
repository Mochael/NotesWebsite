# Bootstrap

**How Bootstrap Works:** 

Take n samples with replacement (you could also use other data simulation methods such as estimating parameters from the data and then simulating data using these parameters) and compute your test statistic using the simulated data. Repeat this resampling process $B$ times to get a distribution for your test statistic.

**Hypothesis Testing**: 

Simulate data $B$ times and calculate your test statistic $t^*$ for each simulation. A common example test:

$$p − value \cong \frac{ \text{count} \{t^* > t^*_{obs}\}}{B}$$

In original case (no bootstrapping), if we observe a test statistic that is very different from what we would expect under the null, then observing this value would have a very low probability, hence a low p-value, and therefore we would likely reject the null.

In the bootstrap case, we simulate the data under the assumption that the null hypothesis is true. So if we take a random sample via bootstrap and compute a test statistic, we would expect to see those values of the test statistic if the null were true. If these simulated test statistics are more extreme than the originally observed test statistic, then the observed test statistic must not be too extreme and there would be a high probability of that observed test statistic occurring. This means that from the equation above, we would have a high p-value and we would not reject the null.

**Bootstrapping to Check Model Specification:**

Suppose we wanted to test the null hypothesis that a certain estimator f(x) followed a linear model (the alternative hypothesis is just that the model is not linear).

$$\text{test statistic} = \text{difference in MSEs}$$

- If a linear model is correct it will perform at least as well as a nonparametric model.
- If a linear model is incorrect, then eventually a nonparametric model will beat it (as samples increase).

[Here is a Useful Link that Explains it in more detail](https://towardsdatascience.com/an-introduction-to-the-bootstrap-method-58bcb51b4d60)