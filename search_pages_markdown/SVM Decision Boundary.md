# SVM Decision Boundary

Consider the equation below which has relation to the primal problem of SVMs:

$$h(\mathbf{w}, b)=\max _{\alpha_{i} \geq 0 \forall i} \sum_{i=1}^{N} \alpha_{i}\left(1-y_{i}\left(\left\langle\mathbf{w}, \phi\left(\mathbf{x}_{i}\right)\right\rangle+b\right)\right)$$

Specifically let's examine $y_{i}\left(\left\langle\mathbf{w}, \phi\left(\mathbf{x}_{i}\right)\right\rangle+b\right)$:

$$\left\langle\mathbf{w}, \phi\left(\mathbf{x}_{i}\right)\right\rangle+b = 0\text{ represents the decision boundary line}$$

$$\text{ For all } \phi\left(\mathbf{x}_{i}\right) \text{ lying on the same side of the line as the vector } \mathbf{w}, \left\langle\mathbf{w}, \phi\left(\mathbf{x}_{i}\right)\right\rangle+b>0$$

$$\text{ For all } \phi\left(\mathbf{x}_{i}\right) \text{ lying on the side of the line opposite the vector } \mathbf{w}, \left\langle\mathbf{w}, \phi\left(\mathbf{x}_{i}\right)\right\rangle+b<0$$

$$b \text{ shifts the location of the line and } w \text{ changes the slope} $$

Correct classification of a point:

$$y_{i}\left(\left\langle\mathbf{w}, \phi\left(\mathbf{x}_{i}\right)\right\rangle+b\right) > 0 \text{ for a point where } y_i \text{ is the same sign as } \left(\left\langle\mathbf{w}, \phi\left(\mathbf{x}_{i}\right)\right\rangle+b\right)$$

Incorrect classification:

$$y_{i}\left(\left\langle\mathbf{w}, \phi\left(\mathbf{x}_{i}\right)\right\rangle+b\right) < 0 \text{ for a point where } y_i \text{ is a different sign than } \left(\left\langle\mathbf{w}, \phi\left(\mathbf{x}_{i}\right)\right\rangle+b\right)$$