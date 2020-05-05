# Bias Variance Decomposition

$$\begin{aligned} MSE(\hat{\theta}) &=E\left[(\hat{\theta}-\theta)^{2}\right]=E\left[(\hat{\theta}-E[\hat{\theta}]+E[\hat{\theta}]-\theta)^{2}\right] \\ &=E\left[(\hat{\theta}-E[\hat{\theta}])^{2}\right]+E\left[(E[\hat{\theta}]-\theta)^{2}\right]+2 E[(\hat{\theta}-E[\hat{\theta}])(E[\hat{\theta}]-\theta)] \\ &=\operatorname{Var}[\hat{\theta}]+(E[\hat{\theta}]-\theta)^{2}+2(E[\hat{\theta}]-\theta) E[(\hat{\theta}-E[\hat{\theta}])] \\ &=\operatorname{Var}[\hat{\theta}]+\operatorname{Bias}(\hat{\theta})^{2}+2(E[\hat{\theta}]-\theta)(E[\hat{\theta}]-E[\hat{\theta}]) \\ &=\operatorname{Var}[\hat{\theta}]+\operatorname{Bias}(\hat{\theta})^{2} \end{aligned}$$

