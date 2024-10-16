$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

* Standard Normal Distribution
- Review the previous concept
    - D(x) is a CDF

    - For the average of a sample size of n

    - example
        - Suppose a diameter of a certain car component follows a normal distribution with $\mu = 10$ and $\sigma = 3$. Find the proportion of these components that have the diameter smaller than 5.1 mm.

$$
P(X \lt 5.1) = P left(\frac{X - \mu}{\sigma} \lt \frac{5.1 - 10}{3}\right) = P(Z \lt -1.63) = 0.05155
$$
            - Find the proportion that have diameters larger than 13.4 mm.
$$
P(X \gt 13.4) = P left(\frac{X - \mu}{\sigma} \gt \frac{13.4 - 10}{3}\right) = P(Z \gt 1.13) = 1 - P(Z \lt 1.13) = 1 - 0.87076 = 0.12924
$$

* Limit Theorem

1. Law of Large Numbers (LLN)
    - The average of a large number of independent and identically distributed random variables approaches the expected value of the distribution.

    - For independent and identically distributed random variables $X_1, X_2, \cdots X_n$, the sample mean $\bar{X}$ is defined as
$$
\bar{X} = \frac{X_1 + X_2 + \cdots + X_n}{n}
$$
    - The expected value of the sample mean is
$$
E(\bar{X}) = \frac{E(X_1) + E(X_2) + \cdots + E(X_n)}{n} = \mu
$$
    - The variance of the sample mean is
$$
Var(\bar{X}) = \frac{Var(X_1) + Var(X_2) + \cdots + Var(X_n)}{n} = \frac{\sigma^2}{n}
$$


2. Central Limit Theorem (CLT)

    - example
        - Assume $X_i$ ~ Bernoulli(p), and $\mu = p$, $\text{Var}(X) = p(1-p)
$$
Z_n = \frac{\bar{X} - \mu}{\frac{\sigma}{\sqrt{n}}} = \frac{X_1 + X_2 + \cdots + X_n - np}{\sigma \sqrt{n}} \\
\text{Let} Y = X_1 + X_2 + \cdots + X_n \\
= \frac{Y - np}{\sqrt{n \cdot p(1-p)}} \\
\\
Z_1 = \frac{X_1 - p}{\sqrt{p(1-p)}} \\
Z_2 = \frac{X_1 + X_2 - 2p}{\sqrt{2p(1-p)}} \\
\cdots \\
Z_30 = \frac{X_1 + X_2 + \cdots + X_{30} - 30p}{\sqrt{30p(1-p)}} \\
\text{where the PDF is similar to bell curve in } Z_30
$$
        - Assume $X_i$ ~ Uniform(0,1), and $\mu = \frac{a+b}{2} = \frac{1}{2}$, $\text{Var}(X) = \frac{(b-a)^2}{12} = \frac{1}{12}$
$$
Z_n = \frac{Y - \frac{n}{2}}{\sqrt{\frac{n}{12}}} \\
\\
Z_1 = \frac{X_1 - \frac{1}{2}}{\sqrt{\frac{1}{12}}} \\
Z_2 = \frac{X_1 + X_2 - 1}{\sqrt{\frac{1}{6}}} \\
\cdots \\
Z_{30} = \frac{X_1 + X_2 + \cdots + X_{30} - 15}{\sqrt{\frac{30}{12}}} \\
\text{where the PDF is similar to bell curve (normal distribution) in } Z_{30}
$$

So if n is large enough, the sample mean $\bar{X}$ is approximately normally distributed.

...

    - example
        - A bank teller serves customers standing in a queue one by one. Suppose service time $X_i$ for customer $i$ has $E X_i = 2$ minutes and $\text{Var}(X_i) = 1$. We assume service time for different customers are independent. Let $Y$ be total wait time bank teller spends serving 50 customers. Find $P( 90 \lt Y \lt 110 )$.
$$
P(\frac{90 - n \mu}{\sqrt{n} \sigma} \leq Z \leq \frac{110 - n \mu}{\sqrt{n} \sigma}) \\
= P(\frac{90 - 100}{\sqrt{50}} \leq Z \leq \frac{110 - 100}{\sqrt{50}}) \\
= P(-1.414 \leq Z \leq 1.414) \\
= P(Z \leq 1.414) - P(Z \leq -1.414) \\
\quad \text{make 3rd digit to (get rid of if 1,2,3), average if (4,5,6), round up if (7,8,9)} \\
= \pi (\frac{1.41 + 1.42}{2}) - \pi (\frac{-1.41 - 1.42}{2}) \\
= \frac{0.92073 + 0.92222){2} - \frac{0.07927 + 0.07778}{2} \\
= 0.842
$$

        - In a communication systems, each data packet consists of 1,000 bits. Due to noise, each bit may be received in error with $P=0.1$. It is assumed that bit errors occur independently. Find P that there are more than 120 errors in a certain data packet.
$$
\text{Each bit } X_i ~ Bernoulli(0.1) \text{with } \mu = 0.1, \text{Var}(X_i) = 0.1(1-0.1) = 0.09 \\
P(Y \gt 120) = P(Z \gt \frac{120 - n \mu}{\sqrt{n} \sigma}) \\
= P(Z \gt \frac{120 - 100}{\sqrt{90}}) \\
= P(Z \gt 2.11) = 1 - pi(2.11) = 0.0175
$$

cf. $\frac{\bar{X} - \mu}{\frac{\sigma}{\sqrt{n}}} = \frac{Y - n \mu}{\sqrt{n} \sigma}$

- Continuity Correction for Discrete Random Variables

    - example
        - Assume that $Y$ ~ Binomial(20, 1/2) and we are interested in $P(8 \leq Y \leq 10)$.

$$
\text{방법 1} \\
\text{Each } X_i ~ Bernoulli(1/2) \text{with } \mu = 1/2, \text{Var}(X_i) = 1/2(1-1/2) = 1/4 \\
P(8 \leq Y \leq 10) = P(\frac{8 - n \mu}{\sqrt{n} \sigma} \leq Z \leq \frac{10 - n \mu}{\sqrt{n} \sigma}) \\
= P(\frac{8 - 10}{\sqrt{5}} \leq Z \leq \frac{10 - 10}{\sqrt{5}}) \\
= P(-0.894 \leq Z \leq 0) \\
= P(Z \leq 0) - P(Z \leq -0.894) \\
= \pi(0) - \pi(\frac{-0.89 - 0.90}{2}) \\
= 0.5 - \frac{0.18673 + 0.18406}{2} = 0.3146
$$

$$
\text{방법 2} \\
\sum_{k=8}^{10} \binom{20}{k} \left(\frac{1}{2}\right)^k \left(\frac{1}{2}\right)^{20-k} \\
= \binom{20}{8} \left(\frac{1}{2}\right)^8 \left(\frac{1}{2}\right)^{12} + \binom{20}{9} \left(\frac{1}{2}\right)^9 \left(\frac{1}{2}\right)^{11} + \binom{20}{10} \left(\frac{1}{2}\right)^{10} \left(\frac{1}{2}\right)^{10} \\
= 0.4565
\text{n이 충분히 크면(30이상) 두 방법의 결과가 비슷해진다.}
$$

$$
\text{방법 3} \\
P(7.5 \leq Y \leq 10.5) = P(\frac{7.5 - 10}{\sqrt{5}} \leq Z \leq \frac{10.5 - 10}{\sqrt{5}}) \\
= P(-1.118 \leq Z \leq 0.22) \\
= \pi(0.22) - \pi(-1.12) \\
= 0.58706 - 0.13136 \\
= 0.455
\text{Continuity Correction을 방법 1에 적용해야 한다(30 미만)}
$$






























### References

$\tag*{}\label{n} \text{[n] }$
