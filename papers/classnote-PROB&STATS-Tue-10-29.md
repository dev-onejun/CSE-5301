$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

* Review

    Example
    - A random sample $X_1, X_2, \ldots, X_100$ is given from a distribution with known variance Var($X_i$) = 16. For the observved sample, the sample mean $\bar{X} = 23.5$. Find an approximate 05% confidence interval for $\theta = E(X_i)$.

$$
Z_\frac{\alpha}{2} = Z_{0.025} = 1.96
\left[ \bar{X} - Z_\frac{\alpha}{2} \frac{\sigma}{\sqrt{n}}, \bar{X} + Z_\frac{\alpha}{2} \frac{\sigma}{\sqrt{n}} \right]
= \left[ 23.5 - 1.96 \frac{4}{10}, 23.5 + 1.96 \frac{4}{10} \right]
= \left[ 22.7, 24.3 \right]
$$

* Interval Estimation
    - If we do not know the value of $\sigma$, how can we approximate the confidence interval?

    1) Upper bound for $\sigma$ ($\sigma_\text{max}$) \
        example \
        - We would like to estimate the portion of people who plan to vote for candidate A in an upcoming election. it is assumed that the number of voters is large and $\theta$ is a portino of voters who plan to vote for candidate A. We define random variable $X$ as whether a randomly selected voter plan to vote for candidate A or not. $X=1$ represents yes and $X=0$ represents no. $X$ follows Bernouli($\theta$). We get $X_1, X_2, \ldots, X_n$ from this distribution and we want to find $\alpha (1-\alpha) 100$% confidence interval for $\theta = E(X)$. \

$$
\text{Var} = P(1-P) = \theta(1-\theta) \\
\text{which is maximized when } \theta = 0.5 \\
\to \sigma_\text{max} = \sqrt{0.5(1-0.5)} = 0.5 \\
\to \text{Confidence Interval} = \left[ \bar{X} - Z_\frac{\alpha}{2} \frac{\sigma_\text{max}}{\sqrt{n}}, \bar{X} + Z_\frac{\alpha}{2} \frac{\sigma_\text{max}}{\sqrt{n}} \right] \\
= \left[ \bar{X} - \frac{Z_\frac{\alpha}{2}}{2\sqrt{n}}, \bar{X} + \frac{Z_\frac{\alpha}{2}}{2\sqrt{n}} \right]
$$

    2) Estimate $\sigma$ \
        When it comes to Bernouli distribution, (위의 1과 같은 상황일 때),
            Confidence Interval is approximately as $\left[ \bar{X} - Z_\frac{\alpha}{2} \sqrt{\frac{\bar{X}(1-\bar{X})}{n}}, \bar{X} + Z_\frac{\alpha}{2} \sqrt{\frac{\bar{X}(1-\bar{X})}{n}} \right]$ \
        example \
        - A random sample $X_1, X_2, \ldots, X_{144}$ is given from Bernouli($\theta$). For the observed sample, $\bar{X} = 0.65$. Find a 99% confidence interval for $\theta = E(X_i)$.

$$
\begin{align*}
& \left[ \bar{X} - Z_\frac{\alpha}{2} \sqrt{\frac{\bar{X}(1-\bar{X})}{n}}, \bar{X} + Z_\frac{\alpha}{2} \sqrt{\frac{\bar{X}(1-\bar{X})}{n}} \right] \\
= & \left[ 0.65 - 2.575 \sqrt{\frac{0.65(1-0.65)}{144}}, 0.65 + 2.575 \sqrt{\frac{0.65(1-0.65)}{144}} \right] \\
\simeq & \left[ 0.65 - 0.1023, 0.65 + 0.1023 \right] \\
\simeq & \left[ 0.5476, 0.7504 \right]
\end{align*}
$$

    - What if the distribution is not Bernouli?

    * Calculating Sample Variance $S$ \
        - $S^2 = \frac{1}{n-1} \sum_{i=1}^{n} (X_i - \bar{X})^2$ = $\frac{1}{n-1} \left( \sum_{i=1}^{n} X_i^2 - n\bar{X}^2 \right)$

    Example
    - We have collected a random sample $X_1, X_2, \ldots, X_{100}$ from an unknown distribution. $\bar{X} = 15.6$ and $S^2 = 8.4$. Find a 99% confidence interval for $\theta = E(X_i)$.

$$
\begin{align*}
& \left[ \bar{X} - Z_\frac{\alpha}{2} \frac{S}{\sqrt{n}}, \bar{X} + Z_\frac{\alpha}{2} \frac{S}{\sqrt{n}} \right] \\
= & \left[ 15.6 - 2.575 \frac{\sqrt{8.4}}{10}, 15.6 + 2.575 \frac{\sqrt{8.4}}{10} \right] \\
\simeq & \left[ 14.85, 16.34 \right]
\end{align*}
$$

    - A random sample $X_1, X_2, \ldots, X_n$ is given from a distribution with unknown variance. How large $n$ should be such that $P(\bar{X} - 1.263 \leq \theta \leq \bar{X} + 1.263) \geq 0.99$ for the observed sample $S^2 = 34.5$?

$$
\begin{align*}
& P(\bar{X} - 1.263 \leq \theta \leq \bar{X} + 1.263) \geq 0.99 \\
\to & Z_\frac{\alpha}{2} \frac{S}{\sqrt{n}} = 1.263 \\
\to & n = 143.2 (144)
\end{align*}
$$

* Additional Practices

- Suppose you have 40 cards. Each has a color and a number. There are 10 pink cards, 10 orange cards, 10 green cards, and 10 purple cards. Cards of each color is numbered from 1 to 10. Two cards are picked at random. What is the probability that the two cards are not same color or not same number?

$$
\frac{27}{39}
$$

Since the first card is picked, the second card has 39 choices. Among them, 27 choices are not same color or not same number. (첫번째 카드가 무엇이든 상관 없음)

- A gambler presents you with an even-money wager. You will roll two dice and if the highest number showing is 1,2,3, or 4 you win. If it is 5 or 6, you lose. Should you take te bet?

$\frac{16}{36}$이 이길 확률이므로, 베팅하면 안됨























### References

$\tag*{}\label{n} \text{[n] }$
