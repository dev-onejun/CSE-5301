$$
\begin{aligned}
& \text{1) When sets are disjoint AND } A_1 \cup A_2 \cup \cdots \cup A_n = A, \text{the sets is called as }\mathbf{\text{Partitions of a set}} \\
& \text{2) If two or more sets do not have common elements (the intersections are empty), they are called }\mathbf{\text{Mutually exclusive sets}}
\end{aligned}
$$

$$
\begin{array}{cc}
\begin{array}{|ccc|}
\hline
E(X) & = & \sum_{i=1}^{n} x_i \cdot p(x_i) \\
\hline
Var(X) & = & E[(X - \mu)^2] \\
& = & E(X^2) - E(X)^2 & \cdots (1)\\
\hline
SD(X) & = & \sqrt{Var(X)} \\
\hline
\end{array}
&
\begin{array}{|ccc|}
\hline
E(X) & = & \int_{-\infty}^{\infty} x \cdot f(x) dx \\
\hline
Var(X) & = & \int_{-\infty}^{\infty} (x - \mu)^2 \cdot f(x) \; dx \\
& = & \int_{-\infty}^{\infty} x^2 \cdot f(x) \; dx - \mu^2 \\
\hline
SD(X) & = & \sqrt{Var(X)} \\
\hline
\end{array}
\end{array}
$$

$$
\begin{array}{|c|}
\hline
\mathbf{\text{Binomial Distribution}} \\
\hline
\begin{array}{c|ccc}
& \text{Mean} & = & np \\
P(X = k) = {n \choose k} p^k (1-p)^{n-k} & \text{Variance} & = & np(1-p) \\
& \text{Standard Deviation} & = & \sqrt{np(1-p)}
\end{array} \\
\hline
\mathbf{\text{Discrete Uniform Distribution}} \\
\hline
\begin{array}{c|ccc}
& \text{Mean} & = & \frac{a+b}{2} \\
P(X = k) = {1 \over n} \quad (k=[a,b], \; n=b-a+1)& \text{Variance} & = & \frac{n^2 - 1}{12} \\
& \text{Standard Deviation} & = & \sqrt{\frac{n^2 - 1}{12}}
\end{array} \\
\hline
\mathbf{\text{Poisson Distribution}} \\
\hline
\begin{array}{c|ccc}
& \text{Mean} & = & \lambda \\
P(X = k) = \frac{e^{-\lambda} \lambda^k}{k!} & \text{Variance} & = & \lambda \\
& \text{Standard Deviation} & = & \sqrt{\lambda}
\end{array} \\
\hline
\mathbf{\text{Hypergeometric Distribution}} \\
\hline
\begin{array}{c|ccc}
& \text{Mean} & = & \frac{nK}{N} \\
P(X = k) = \frac{ {K \choose k} {N-K \choose n-k} }{ {N \choose n} } & \text{Variance} & = & n \frac{K}{N} \frac{N-K}{N} \frac{N-n}{N-1} \\
& \text{Standard Deviation} & = & \sqrt{n \frac{K}{N} \frac{N-K}{N} \frac{N-n}{N-1}}
\end{array} \\
\hline
\mathbf{\text{Geometric Distribution}} \\
\hline
\begin{array}{c|ccc}
& \text{Mean} & = & \frac{1}{p} \\
P(X = k) = (1-p)^{k-1} p & \text{Variance} & = & \frac{1-p}{p^2} \\
& \text{Standard Deviation} & = & \sqrt{\frac{1-p}{p^2}}
\end{array} \\
\hline
\end{array}
$$

$$
\begin{array}{|c|}
\hline
\mathbf{\text{Normal (Gaussian) Distribution}} \\
\hline
f(x) = \frac{1}{\sqrt{2\pi}\sigma} e^{-\frac{(x-\mu)^2}{2\sigma^2}} \\
\hline
\mathbf{\text{Exponential Distribution}} \\
\hline
\begin{array}{c|c}
\text{PDF} & \text{CDF} \\
\hline
f(x; \lambda) = \begin{cases}
\lambda e^{-\lambda x} & \text{if } x \ge 0 \\
0 & \text{if } x < 0
\end{cases} & F(x; \lambda) = \begin{cases}
1 - e^{-\lambda x} & \text{if } x \ge 0 \\
0 & \text{if } x < 0
\end{cases}
\end{array} \\
\\
(\text{Mean} = \frac{1}{\lambda} \quad \text{Variance} = \frac{1}{\lambda^2} \quad \text{Standard Deviation} = \frac{1}{\lambda}) \\
\hline
\mathbf{\text{Uniform Distribution}} \\
\hline
\begin{array}{c|c}
\text{PDF} & \text{CDF} \\
\hline
f(x; a, b) = \begin{cases}
\frac{1}{b-a} & \text{if } a \le x \le b \\
0 & \text{otherwise}
\end{cases} & F(x; a, b) = \begin{cases}
0 & \text{if } x < a \\
\frac{x-a}{b-a} & \text{if } a \le x \le b \\
1 & \text{if } x > b
\end{cases}
\end{array} \\
\\
(\text{Mean} = \frac{a+b}{2} \quad \text{Variance} = \frac{(b-a)^2}{12} \quad \text{Standard Deviation} = \frac{b-a}{\sqrt{12}}) \\
\hline
\mathbf{\text{Gamma Distribution}} \\
\hline
\begin{array}{c|c}
\text{Condition} & \text{Gamma Function} \\
\hline
\begin{aligned}
& \text{1. } \Gamma(\alpha) = \int_{0}^{\infty} x^{\alpha-1}e^{-x}dx, \quad \alpha > 0 \\
& \text{2. } \int_{0}^{\infty} x^{\alpha-1}e^{- \lambda x}dx = \frac{\Gamma(\alpha)}{\lambda^{\alpha}}, \quad \alpha > 0, \lambda > 0 \\
& \text{3. } \Gamma(\alpha + 1) = \alpha \Gamma(\alpha), \quad \alpha > 0 \\
& \text{4. } \Gamma(n) = (n-1)!, \quad n \in \mathbb{N} \\
& \text{5. } \Gamma(\frac{1}{2}) = \sqrt{\pi}
\end{aligned}
&
f(x) = \begin{cases}
\frac{\lambda^\alpha x^{\alpha-1} e^{-\lambda x}}{\Gamma(\alpha)}, & x > 0 \\
0, & \text{otherwise}
\end{cases}
\end{array} \\
\\
(\text{Mean} = \frac{\alpha}{\lambda} \quad \text{Variance} = \frac{\alpha}{\lambda^2} \quad \text{Standard Deviation} = \frac{\sqrt{\alpha}}{\lambda}) \\
\hline
\end{array}
$$


