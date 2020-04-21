# Making Sense of a Betting Market with Probabilities

Consider a game you play with your friend where you get \$10 if you win and you pay your friend ​\$5 if you lose. How can you decide if you should play this game?

- Making a market comes down to expected value. In order for this to be a fair market, the expected value of playing this game (for either player) must be 0, otherwise the option with the lower expected value would not be picked.
- In the example, your expected value of playing the game $E(X) = 10p - 5(1-p)$ where $p$ is the probability that you win. For this game to be fair, $E(X) = 0 = 10p - 5(1-p)$ which implies that $p = 1/3$.
- In fact, for a Bernoulli random variable like in this game, the probability for a fair market generalizes to $p = (\text{money from losing})/\text{(money from winning + money from losing)}$. In the Bernoulli case, you should play the game if $p > (\text{money from losing})/\text{(money from winning + money from losing)}$ and not play if it is lower. In this example, you should play the game if you think that $p < 1/3$.
- You can also derive the fair betting probabilities for other distributions.
- The variance of this distribution $Var(X) = E(X^2)-E(X)^2 = 100p + 25(1-p) - (10p - 5(1-p)) = 70p + 20$.