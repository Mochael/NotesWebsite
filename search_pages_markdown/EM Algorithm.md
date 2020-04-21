# EM Algorithm

## **E Step**

- **Compute the expected value of the sufficient statistics of the hidden variables given current estimations of the model parameters.**
- **In K-Means, it's where each datapoint is assigned to the closest cluster (think of this as the cluster centers are latent random variables because a point's assignment in a Gaussian Mixture Model follows a probability distribution).**
- **We close the gap, making the lower bound=likelihood.**

## **M Step**

- **Compute the parameters under current results of the expected value of the hidden variables.**
- **We optimize a lower bound on the likelihood.**
- **In K-Means, it's where the cluster centers are recomputed to minimize the distance for the expected cluster assignments found in the E step (think of this as a parameter, because cluster centers are fixed values and not random variables).**