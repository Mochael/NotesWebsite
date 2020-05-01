# Wake Sleep

## Hemholtz Machine

|                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="../search_pics/WakeSleep/Screen Shot 2020-04-30 at 8.22.32 PM.png" style="zoom:33%;"/> | <img src="../search_pics/WakeSleep/Screen Shot 2020-04-30 at 8.18.52 PM.png" alt="Screen Shot 2020-04-30 at 8.18.52 PM" style="zoom:40%;" /> |

We have two networks:

1. Recognition network with weights $\phi$ converts input data $\mathbf{x}$ into latent representations used in successive hidden states $\mathbf{z}$.
2. Generative network reconstructs data from the latent states using weights $\theta$.

The Hemholtz machine tries to learn $\phi$ and $\theta$ such that $q_{\phi}(\mathbf{z}|\mathbf{x}) \approx p_{\theta}(\mathbf{z}|\mathbf{x}) \propto p_{\theta}(\mathbf{z},\mathbf{x})$ 

- $q_{\phi}(\mathbf{z}|\mathbf{x})$ is the variational distribution approximating the posterior $p_{\theta}(\mathbf{z}|\mathbf{x})$ 



## Wake Phase

1. Feed $\mathbf{x}^{(i)}$ into the recognition network to get $\mu_{\phi}\left(\mathbf{x}^{(i)}\right)$ and $\Sigma_{\phi}\left(\mathbf{x}^{(i)}\right)$
2. Draw $L$ samples $\mathbf{z}_{1}^{(i)}, \ldots, \mathbf{z}_{L}^{(i)} \sim q_{\phi}\left(\mathbf{z} | \mathbf{x}^{(i)}\right)=N\left(\mathbf{z} ; \mu_{\phi}\left(\mathbf{x}^{(i)}\right), \Sigma_{\phi}\left(\mathbf{x}^{(i)}\right)\right)$
3. For each $l \in[L],$ feed $\mathbf{z}_{l}^{(i)}$ into the generative network to get $f_{\theta}\left(\mathbf{z}_{l}^{(i)}\right)$ for the likelihood $p_{\theta}\left(\mathbf{x} | \mathbf{z}_{l}^{(i)}\right)=$ Bernoulli(x; $\left.f_{\theta}\left(\mathbf{z}_{l}^{(i)}\right)\right)$
4. Optimize for $\max _{\theta} \sum_{i=1}^{N} \frac{1}{L} \sum_{l=1}^{L} \log p_{\theta}\left(\mathbf{x}^{(i)} | \mathbf{z}_{l}^{(i)}\right)$

- Simulate latent state by feeding input data to recognition network and maximize how well the generator's probabilities for the hidden state fit the actual data.

## Sleep Phase

1. Draw $\mathbf{z}^{l} \sim N(0, I)$
2. Sample $\mathbf{x}^{l}$ from the generative network $p_{\theta}\left(\mathbf{x} | \mathbf{z}^{l}\right)=\operatorname{Bernoulli}\left(f_{\theta}\left(\mathbf{z}^{l}\right)\right)$
3. Feed $\mathbf{x}^{l}$ into the recognition network to get $\mu\left(\mathbf{x}^{l}\right)$ and $\Sigma\left(\mathbf{x}^{l}\right)$
4. Compute $q_{\phi}\left(\mathbf{z}^{l} | \mathbf{x}^{l}\right)=N\left(\mathbf{z}^{l} ; \mu\left(\mathbf{x}^{l}\right), \Sigma\left(\mathbf{x}^{l}\right)\right)$
5. Optimize $\max _{\phi} \frac{1}{L} \sum_{l=1}^{L} \log q_{\phi}\left(\mathbf{z}^{l} | \mathbf{x}^{l}\right)$

- Simulate random $\mathbf{x}$ data by following the generator. Then maximize the probability that the recognition network suggests the correct latent states given the simulated $\mathbf{x}$.