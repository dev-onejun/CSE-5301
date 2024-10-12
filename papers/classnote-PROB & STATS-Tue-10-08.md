$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

* Information Theory
    - Information can not be negative. $I(p) \geq 0$
    - . $I(1) = 0$

    - $I(p) = -\log_b(p)$
        - $b=2$: bits, the most common base (default)
        - $b=3$: trits
        - $b=e$: nats
        - $b=10$: Hartleys

    - Entropy
        - The expected of information of an experiment
            - $H(X) = -\sum_{i=1}^{n} p(x_i) \log_b(p(x_i))$

    Example

        - Maximum Entropy
            - When the probability distribution is uniform, the entropy is maximized.

* Coding Theory
- Usage: Data compression, cryptography, error detection/correction, data transmission/storage
- Goal: Remove redundancy in data,

    1) Data Compression (Source Coding)
        - Lossless: No information loss (Complete recovery)
            ex. zip, rar
        - Lossy: Some information loss (Partial recovery)
            ex. jpeg, mpeg
    2) Error Control (Channel Coding): Add redundent data
    3) Cryptographic Coding
    4) i? Coding

* Relative Entropy (Kullback-Leibler Distance) Divergence?

$$
D(p||q) = E_p \left[ \log \frac{p(x)}{q(x)} \right] = \sum_{x} p(x) \log_b \frac{p(x)}{q(x)}
$$

Example

* Joint Entropy

$$
H(X,Y) = E \left[ -\log_b P(X,Y) \right] = -\sum_x \sum_y P(X=x,Y=y) \log_b P(X=x,Y=y)
$$

- $H(X,Y) \geq max(H(X), H(Y))$
- $H(X,Y) \leq H(X) + H(Y)$
- $H(X,Y) = H(X) + H(Y)$ if and only if X and Y are independent.

    - Conditional Entropy

    $$
    \begin{aligned}
    H(X|Y) & = H(X,Y) - H(Y)
    & = -\sum_x \sum_y P(X=x,Y=y) \log_b P(X=x|Y=y)
    & = -\sum_x \sum_y P(X=x,Y=y) \log_b P(x_i, y_i) + \sum_y P(Y=y) \log_b P(Y=y)
    \end{aligned}
    $$

    - Mutual Information
    .

Example




### Practices <!-- 강의자료로 올라오면 정리 안해도 되지 않을까..?-->

a. Suppose P of being stopped by cops is 0.1. Find entropy.

$$
\begin{aligned}
P(S) & = 0.1, P(\bar{S}) = 0.9 \\
H(S) & = -0.1 \log_2(0.1) - 0.9 \log_2(0.9) = 0.469 \text{ bits}
\end{aligned}
$$

b-1. What is $D(P||Q)$?

||P|Q|
|:--:|:--:|:--:|
|X = 1|0.5|0.25|
|X = 2|0.4|0.25|
|X = 3|0.07|0.25|
|X = 4|0.03|0.25|

$$
\begin{aligned}
D(P||Q) & = 0.5 \log_2 \frac{0.5}{0.25} + 0.4 \log_2 \frac{0.4}{0.25} + 0.07 \log_2 \frac{0.07}{0.25} + 0.03 \log_2 \frac{0.03}{0.25} \\
& = 0.5 \log_2 2 + 0.4 \log_2 1.6 + 0.07 \log_2 0.28 + 0.03 \log_2 0.12 \\
& = 0.5 + 0.271 - 0.128 - 0.0917 \\
& = 0.5513 \text{ bits}
\end{aligned}
$$

b-2. What is $D(Q||P)$?

$$
\begin{aligned}
D(Q||P) & = 0.25 \log_2 \frac{0.25}{0.5} + 0.25 \log_2 \frac{0.25}{0.4} + 0.25 \log_2 \frac{0.25}{0.07} + 0.25 \log_2 \frac{0.25}{0.03} \\
& = -0.25 - 0.17 + 0.458 + 0.764 \\
& = 0.802 \text{ bits}
\end{aligned}
$$

c. $P$ of sunny weather is 0.5. $M$ is an event of riding a motorcycle. We have a probability $P(S) = 0.5, P(M|S) = 0.96, P(M|\bar{S}) = 0.1$. Find mutual information of $S$ and $M$.

From conditions,

$$
\begin{aligned}
P(S) = 0.5 & \to P(\bar{S}) = 0.5 \\
P(M|S) = 0.96 & \to P(\bar{M}|S) = 0.04 \\
P(M|\bar{S}) = 0.1 & \to P(\bar{M}|\bar{S}) = 0.9 \\
\end{aligned}
$$

Therefore,

$$
I(M, S) = H(M) - H(M|S) \\
\quad H(M) = -(P(M) \log_2 P(M) + P(\bar{M}) \log_2 P(\bar{M})) \\
\quad\quad P(M) = P(M|S)P(S) + P(M|\bar{S})P(\bar{S}) = 0.96 \times 0.5 + 0.1 \times 0.5 = 0.53 \\
\quad = - (0.53 \log_2 0.53 + 0.47 \log_2 0.47) \\
\quad = 0.9974 \text{ bits} \\
\quad H(M|S) = - \sum \sum P(m_i, s_i) \log_2 P(m_i|s_i) \\
\quad = - (P(\bar{M}, \bar{S}) \log_2 P(\bar{M}|\bar{S}) + P(\bar{M}, S) \log_2 P(\bar{M}|S) + P(M, \bar{S}) \log_2 P(M|\bar{S}) + P(M, S) \log_2 P(M|S)) \\
\quad\quad P(\bar{M}, \bar{S}) = P(\bar{M}|\bar{S})P(\bar{S}) = 0.9 \times 0.5 = 0.45 \\
\quad\quad P(\bar{M}, S) = P(\bar{M}|S)P(S) = 0.04 \times 0.5 = 0.02 \\
\quad\quad P(M, \bar{S}) = P(M|\bar{S})P(\bar{S}) = 0.1 \times 0.5 = 0.05 \\
\quad\quad P(M, S) = P(M|S)P(S) = 0.96 \times 0.5 = 0.48 \\
\quad = - (0.45 \log_2 0.9 + 0.02 \log_2 0.04 + 0.05 \log_2 0.1 + 0.48 \log_2 0.96) \\
\quad = 0.355 \text{ bits} \\
= 0.9974 - 0.355 = 0.6424 \text{ bits}
$$

### References

$\tag*{}\label{n} \text{[n] }$
