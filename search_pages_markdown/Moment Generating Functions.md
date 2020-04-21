# Moment Generating Functions

The moment-generating function $m(t)$ for a random variable $Y$ is defined as the following:

$$m(t)=E\left(e^{t Y}\right)$$

If $m(t)$ exists, then for any positive integer $k$, the $k$-th derivative of $m(t)$ is:

$$\left.\frac{d^{k} m(t)}{d t^{k}}\right|_{t=0}=m^{(k)}(0)=E\left(Y^{k}\right)$$

This is true because of the following:

$$\begin{aligned} e^{t Y} &=1+\frac{t Y}{1 !}+\frac{t^{2} Y^{2}}{2 !}+\frac{t^{3} Y^{3}}{3 !}+\ldots+\frac{t^{n} Y^{n}}{n !}+\ldots \\ m(t)=E\left[e^{t Y}\right] &=1+t E[Y]+\frac{t^{2}}{2 !} E\left[Y^{2}\right]+\frac{t^{3}}{3 !} E\left[Y^{3}\right]+\ldots+\frac{t^{n}}{n !} E\left[Y^{n}\right]+\ldots \end{aligned}$$

## MGF Determines Distribution

Suppose $m_X(t), \  m_Y(t)$ are mgfs of the random variables $X$and $Y$ respectively. If both mgfs exist and $m_X(t) = m_Y(t)$ for all values of $t$, then $X$ and $Y$ have the same probability distribution