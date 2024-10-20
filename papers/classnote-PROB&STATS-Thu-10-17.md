$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

* Statistical Inference


Example
* Let X be height of a randomly chosen individual from a population. In order to estimate the Mean and Variance of X, we observe a random sample (X1, X2, ..., X7). All X1 are independent and identically distributed and have same distribution as X. We obtain following data:
    166.8, 171.4, 169.1, 178.5, 168, 157.9, 170.1

    - Find sample mean, sample variance, and sample standard deviation.
$$
\bar{X} = \frac{\sum_{i=1}^{7} X_i}{7} = 168.8 \text{ cm}
S^2 = \frac{\sum (X_i - \bar{X})^2}{N - 1} = 37.7 \text{ cm}
S = \sqrt{S^2} = 6.1 \text{ cm}
$$

* Suppose weight of oranges are normally distributed with M = 8 oz and $\sigma$ = 1.5 oz.

    - What Proportional oranges weigh less than 8.7 oz?
$$
P(X \lt 8.7) = P\left(Z \lt \frac{8.7 - 8}{1.5}\right) = P(Z \lt 0.47) = 0.68082
$$
    - What Proportion weigh more than 11.5 oz?
$$
P(X \gt 11.5) = P\left(Z \gt \frac{11.5 - 8}{1.5}\right) = P(Z \gt 2.33) = 1 - \pi(2.33) = 0.0099
$$
    - What proportion weigh between 10.3 and 14 oz?
$$
P(10.3 \lt X \lt 14) = P\left(\frac{10.3 - 8}{1.5} \lt Z \lt \frac{14 - 8}{1.5}\right) = P(1.53 \lt Z \lt 4) = \pi(4) - \pi(1.53) = 0.063
$$

* Weights of chickens are normally distributed with M=3.8 lb and $\sigma$ = 0.6 lb. Farm created 3 categories: Petite (X < 3.5), Standard (3.5 $\le$ X $\le$ 4.9), and Large (X > 4.9).

    - What proportion of chickens will be in each category?
$$
\text{Petite} \\
P(X \lt 3.5) = P\left(Z \lt \frac{3.5 - 3.8}{0.6}\right) = P(Z \lt -0.5) = 0.30854 \\
\text{Standard} \\
P(3.5 \le X \le 4.9) = P\left(\frac{3.5 - 3.8}{0.6} \le Z \le \frac{4.9 - 3.8}{0.6}\right) = P(-0.5 \le Z \le 1.84) = \pi(1.84) - \pi(-0.5) = 0.96712 - 0.30854 = 0.6579 \\
\text{Large} \\
1 - \pi(1.84) = 1 - 0.96712 = 0.0336
$$
    - Find 60th percentile
$$
P(X \lt C) = 0.6 \\
\text{Since } \pi(0.255) \approx 0.6 \\
0.255 = \frac{C - 3.8}{0.6} \\
C = 3.953
$$
    - Suppose that 5 chickens are selected at random. What is probability that 3 of them will be petite
$$
P(\text{Petite}) = 0.30854 \\
\text{Answer} = \binom{5}{3} \times 0.30854^3 \times (1 - 0.30854)^2 = 0.1404
$$

* A television cable company receives phone calls from customers during the day. Most calls are put 'on hold' until an operator is free to help them. The length of hold time is normally distributed with $\mu = 3.1$ minutes and $\sigma = 0.9$ minutes.
    - The company experts decided it as many as 5% of the callers are put 'on hold' for more than 4.8 minutes, more operators need to be hired. Should they hire more operators?
$$
P(X \gt 4.8) = P\left(Z \gt \frac{4.8 - 3.1}{0.9}\right) = P(Z \gt 1.89) = 1 - \pi(1.89) = 0.0294
$$
Therefore, no need to hire more operators since it's 2%.
    - At another cable company with same distirubtion, 2.5% of callers are put 'on hold' for longer than X minutes. Find X.
$$
P(X \gt C) = 0.025 \\
\to P(X \lt C) = 0.975 \\
1.96 = \frac{C - 3.1}{0.9} \\
C = 4.86 \text{ minutes}
$$

* Suppose the height(X) in inches of a 25 year old man is normally distributed with M=70 inches. If $P(X \gt 79) = 0.025$, find $\sigma$.

$$
P(X \gt 79) = 0.025 \\
\to P(X \lt 79) = 0.975 \\
1.96 = \frac{79 - 70}{\sigma} \\
\sigma = 4.59
$$

* Suppose the weight(X) in lb of a 40 year old man is a normal random variable with $\sigma = 20$ lb. If 5% of this population weigh less than 160 lb, find M.

$$
P(X \lt 160) = 0.05 \\
-1.645 = \frac{160 - \mu}{20} \\
\mu = 192.9
$$


### References

$\tag*{}\label{n} \text{[n] }$
