$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

Practices

* A random variable $A$ takes the values 0 and 1 with equal probabilities. Find variance of $X$.

$$
E(X) = 0.5 \\
E(X^2) = 0.5 \\
Var(X) = E(X^2) - E(X)^2 = 0.5 - 0.25 = 0.25
$$

* Two random variables $X$ and $Y$ take values $X \in \{ 0, 1 \}$ and $Y \in \{ 0, 1 \}$. Their joint probability distribution can be written as $P(X, Y) = K \times (X + Y)$
    - Set up a table for joint P distribution
    $$
    \begin{array}{c|c|c|c}
    & Y = 0 & Y = 1 & Y = 2 \\
    \hline
    X = 0 & 0 & K & 2K \\
    \hline
    X = 1 & K & 2K & 3K \\
    \hline
    \end{array} \\
    K = \frac{1}{9}
    $$
    - Find $H(X)$ and $H(Y)$
    $$
    - \sum P(X) \log P(X) \\
    \begin{aligned}
    H(X) & = - \left( \frac{1}{3} \log \frac{1}{3} + \frac{2}{3} \log \frac{2}{3} \right) \\
    & = 0.9183 \\
    H(Y) & = . \\
    & = 1.3516
    \end{aligned}
    $$
    - Find $H(X, Y)$
    $$
    - \sum \sum P(X, Y) \log P(X, Y) \\
    \begin{aligned}
    H(X, Y) & = - \left( 2 ( \frac{1}{9} \log \frac{1}{9} ) + 2 ( \frac{2}{9} \log \frac{2}{9} ) + \frac{3}{9} \log \frac{3}{9} \right) \\
    & = 2.1971 \text{ bits}
    \end{aligned}
    $$
    - $I(X, Y)$
    $$
    I(X, Y) = H(X) + H(Y) - H(X, Y) \\
    0.9183 + 1.3516 - 2.1971 = 0.0728 \text{ bits}
    $$

* Suppose that an experiment has two outcomes A and B. Let P be the distribution with P(A) = $\frac{1}{3}$ and P(B) = $\frac{2}{3}$. Let Q be the distribution with q(A) = $\frac{2}{3}$ and q(B) = $\frac{1}{3}$.
    - Find relative entropy $D(P || Q)$
    $$
    D(P || Q) = \sum P(x) \log \frac{P(x)}{Q(x)} \\
    \begin{aligned}
    D(P || Q) & = \frac{1}{3} \log \frac{1/3}{2/3} + \frac{2}{3} \log \frac{2/3}{1/3} \\
    & = \frac{1}{3} \text{ bits}
    \end{aligned}
    $$

* Central limit theorem is $\bar{X}$ follows approximately normal distribution with mean $\mu$ and SD $\frac{\sigma}{\sqrt{n}}$, if sample size $leq$ 30, and sample is taken from a non normal distribution. Let $X$ be a random variable with $\mu = 10$ and $\sigma = 4$. A sample size 100 is taken from this distribution.
    - Find the probability that $\bar{X}$ of these 100 observations is less than 9.
    $$
    P(\bar{X} \lt 9) = P(Z \lt \frac{\bar{X} - \mu}{\sigma / \sqrt{n}}) \\
    = P(Z \lt \frac{9 - 10}{4 / \sqrt{100}}) = P(Z \lt -2.5) = 0.0062
    $$

* Suppose you have a sample of 100 values from a population with $\mu = 500, \sigma = 80$
    - What is the probability that the sample mean is between 490 and 510?
    $$
    \begin{aligned}
    P(490 \lt \bar{X} \lt 510) & = P(\frac{490 - 500}{80 / \sqrt{100}} \lt Z \lt \frac{510 - 500}{80 / \sqrt{100}}) \\
    & = P(-1.25 \lt Z \lt 1.25) = 0.7888
    \end{aligned}
    $$

* Point Estimation
- Case 1
    - When we are given a sample from a distribution with known variance and $n$ is large.
    $$
    \left[ \bar{X} - Z_{\alpha/2} \frac{\sigma}{\sqrt{n}}, \bar{X} + Z_{\alpha/2} \frac{\sigma}{\sqrt{n}} \right]
    $$
- Case 2
    - When we are given a sample from Bernouli distribution, Variance is unknown, and $n$ is large.
        - upper bound
        $$
        \left[ \bar{X} - \frac{Z_{\alpha/2}}{2 \sqrt{n}}, \bar{X} + \frac{Z_{\alpha/2}}{2 \sqrt{n}} \right]
        $$
        - estimation
        $$
        \left[ \bar{X} - Z_{\alpha/2} \sqrt{\frac{\bar{X}(1 - \bar{X})}{n}}, \bar{X} + Z_{\alpha/2} \sqrt{\frac{\bar{X}(1 - \bar{X})}{n}} \right]
        $$
- Case 3
    - When we are given a sample from a distribution, Variance is unknown, and $n$ is large.
    $$
    \left[ \bar{X} - Z_{\alpha/2} \frac{S}{\sqrt{n}}, \bar{X} + Z_{\alpha/2} \frac{S}{\sqrt{n}} \right]
    $$

* Distribution of people who are following Atkin's diet is normal distribution with $\sigma = 7.1$. A sample of 29 was chosen their average weight gain was 6.7 lb.
    - Test the hypothesis that the average weight gain is 5 lb.
    $$
    \text{Z-test} \\
    \begin{array}{rl}
    1 & \begin{aligned}
    H_0 & : \mu = 5 \\
    H_1 & : \mu \lt 5
    \end{aligned} \\
    2 & \text{...}
    \end{array}
    $$

* A professor wants to know if her statistics class has a good grasp of math. 6 students are chosen at random and they were given a math test. The results were 62, 92, 75, 68, 83, 95.
    - Can she have 90% confidence that the average score of the class is above 70?
    $$
    \text{one sample T-test} \\
    \begin{array}{rl}
    1 & \begin{aligned}
    H_0 & : \mu = 70 \\
    H_1 & : \mu \gt 70
    \end{aligned} \\
    2 & \text{right tail test with 90% confidence and 5 degree of freedom} \to 1.476 \\
    3 & t_5 = \frac{\bar{X} - \mu}{S / \sqrt{n}} = \frac{79.17 - 70}{13.17 / \sqrt{6}} = 1.71 \\
    4 & \text{Reject } H_0
    \end{array}
    $$

* The question being answered is whether there is a significant difference in average cycle time to deliver pizza from company A versus company B. The sample of deliveres from both companies is
$$
\begin{array}{c|c}
\text{Company A} & \text{Company B} \\
\hline
20.4 & 20.2 \\
24.2 & 16.9 \\
15.4 & 18.5 \\
21.4 & 17.3 \\
20.2 & 20.5 \\
18.5 & \\
21.5 &
\end{array}
$$
    - Test the hypothesis that there is significant difference between two companies
    $$
    \text{Two sample T-test} \\
    \bar{X}_A = 20.23, \bar{X}_B = 18.68, S_A = 2.74, S_B = 1.64 \\
    \begin{array}{rl}
    1 & \begin{aligned}
    H_0 & : \mu_A = \mu_B \\
    H_1 & : \mu_A \neq \mu_B
    \end{aligned} \\
    2 & \text{two-sided test with 95% confidence and 10 degree of freedom} \to 2.228 \\
    3 & t_{10} = \frac{\bar{X}_A - \bar{X}_B}{\sqrt{\frac{S_A^2}{n_A} + \frac{S_B^2}{n_B}}} = \frac{20.23 - 18.68}{\sqrt{\frac{2.74^2}{7} + \frac{1.64^2}{5}}} = 1.221 \\
    4 & \text{Accept } H_0
    \end{array}
    $$


* This example shows matched-pairs data with tire wear for right and left tire of same car.
$$
\begin{array}{c|c|c}
\text{Car} & \text{Left Tire} & \text{Right Tire} \\
\hline
1 & 42 & 54 \\
2 & 75 & 73 \\
3 & 24 & 22 \\
4 & 56 & 59 \\
5 & 52 & 51 \\
6 & 56 & 45
\end{array}
$$
    - Test the hypothesis that there is significant difference between left and right tires of the same car
    $$
    \text{Paired Sample T-test} \\
    \begin{array}{rl}
    1 & \begin{aligned}
    H_0 & : \mu_d = 0 \\
    H_1 & : \mu_d \neq 0
    \end{aligned} \\
    2 & \text{two-sided test with 95% confidence and 5 degree of freedom} \to 2.571 \\
    3 & \bar{X_d} = 0.833, S_d = 6.306 \\
    & t_5 = \frac{\bar{X}_d}{S_d / \sqrt{n}} = \frac{0.833}{6.306 / \sqrt{6}} = 0.3235 \\
    4 & \text{Accept } H_0
    \end{array}
    $$

* a
``` mermaid
graph TD;
    A --> C
    B --> C
    B --> D
    C --> E
    D --> E
    E --> F
```

$$
\begin{array}{cc}
\begin{array}{c|c}
P(A) & P(!A) \\
\hline
0.2 & 0.8
\end{array} &
\begin{array}{c|c}
P(B) & P(!B) \\
\hline
0.4 & 0.6
\end{array} \\
\begin{array}{c|c|c|c}
A & B & P(C) & P(!C) \\
\hline
T & T & 0.55 & 0.45 \\
T & F & 0.5 & 0.5 \\
F & T & 0.45 & 0.55 \\
F & F & 0.1 & 0.9
\end{array} &
\begin{array}{c|c|c}
B & P(D) & P(!D) \\
\hline
T & 0.6 & 0.4 \\
F & 0.55 & 0.45
\end{array} &
...
\end{array}
$$














### References

$\tag*{}\label{n} \text{[n] }$
