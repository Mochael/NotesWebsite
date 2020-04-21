# PAC Learning

The probability that the hypothesis, $h$, that we find with $m$ training examples is probably (with probability $ \geq 1-\delta$) approximately (with $err_D(h)\leq \epsilon$) correct. This is equivalently expressed below:

$$P(err_D(h)\leq \epsilon) \geq 1-\delta, \text{ where } \ err_D(h) = err_{true}(h) - err_{train}(h) $$

## VC Dimension

The VC dimension is the maximal number $d$ such that there exists a set of $d$ points that is shattered by the class. It doesn't mean that every set of points must be shattered!

