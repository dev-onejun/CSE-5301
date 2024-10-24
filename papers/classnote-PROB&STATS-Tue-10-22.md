$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

* Point Estimation
- Invovles the use of sample data to estimate a single value..?
    ex. Mean value

- How can we make sure that we have a good estimator? (Estimating Estimators)
    - Bias
$$
B(\hat{\theta}) = E(\hat{\theta}) - \theta
$$

...

* Mean Squared Error
$$
MSE(\hat{\theta}) = E \left[ (\hat{\theta} - \theta) \right]^2
$$

**Example**

* Suppose we have an algorithm that predicts the pries of a particular stock on a daily basis

$$
\begin{array}{c|c|c}
& \text{Estimation} & \text{Actual} \\
\hline
\text{Monday} & 5.5 & 4.75 \\
\text{Tuesday} & 6.0 & 5.35 \\
\text{Wednesday} & 6.0 & 6.25 \\
\text{Thursday} & 7.5 & 7.25 \\
\text{Friday} & 8.0 & 8.5
\end{array}
$$

Find the MSE

**Solution**
$$
\hat{\theta} = \text{Estimation} \\
\theta = \text{Actual} \\
\\
\frac{0.75^2 + 0.65^2 + -0.25^2 + 0.25^2 + -0.5^2}{5}
$$

* Maximum Likelihood Estimation
...
    - The difference between likelihood and probability
        $L(\mu, \theta; \text{data}) = P(\text{data}; \mu, \theta)$
        + Probability is about the value of the data knowing its distribution ($\mu$ and $\sigma$) $\to$ the population distribution
        + Likelihood is about the $\mu$ and $\sigma$ that we observed in the data $\to$ the sample distribution
        - In other words, one is asking about the data, and the other is asking about the parameters (mu and sigma)
            - For the case of maximum likelihood, we are asking about the parameters 모집단의 분포가 궁금한거자너

**Example**

* I have a bag containing 3 balls. Each ball is either blue or red, but we do not have any further information. the number of blue balls ($\theta$) might be 0,1,2, or 3. I am allowed to choose 4 balls at random from the bag with replacement sequentially. A random variable X is defined as

$$
X_i = \begin{cases} 1 & \text{if the ball is blue} \\ 0 & \text{if the ball is red} \end{cases} \\
i \text{ is the index of the ball}
$$

$X_i$ is identically distributed and $X_i \sim Bernoulli(\theta)$. After doing this experiment, I observe the following values for $X_i$

$$
X_1 = 1, X_2 = 0, X_3 = 1, X_4 = 1
$$

Which value of $\theta$ is the most likely to generate the observed data?


$$
\begin{aligned}
L(X_1, X_2, X_3, X_4; \theta) & = P_{X_1, X_2, X_3, X_4}(X_1, X_2, X_3, X_4) \\
& = P_{X_1}(X_1) \cdot P_{X_2}(X_2) \cdot P_{X_3}(X_3) \cdot P_{X_4}(X_4) \\
& = \frac{\theta}{3} \cdot (1 - \frac{\theta}{3}) \cdot \frac{\theta}{3} \cdot \frac{\theta}{3} \\
& = \frac{\theta}{3}^3 \cdot (1 - \frac{\theta}{3})
\end{aligned}
$$

$$
\begin{array}{c|c}
\theta & \\
\hline
0 & 0 \\
1 & 0.0247 \\
2 & 0.0988 \\
3 & 0
\end{array}
$$

so that 2 is the maximum likelihood estimation for number of blue balls is 2.
확률이 어떻게 나온건데? -> 후보군인 0,1,2,3 을 확률식에 대입해본거지

* Suppose we want to determine how biased an unfair coin is. Let the probability of tossing a Head be $P$. Determine $P(\theta}$, supposing the coin is tossed 80 times.

    - Sample -> X_1 = H, X_2 = T, ..., X_80 = H) => 49 heads and 31 tails

    Suppose coin was taken from a box containing 3 coins:
        1. give Head with P = 1/3
        2. give head with P = 1/2
        3. give head with P = 2/3
        (coins lost their labels which one it was)

$$
P(\text{49 heads} \mid P = \frac{1}{3}) = \choose{80}{49} \frac{1}{3}^49 \frac{2}{3}^31 = 0.0000 \\
P(\text{49 heads} \mid P = \frac{1}{2}) = \choose{80}{49} \frac{1}{2}^49 \frac{1}{2}^31 = 0.012 \\
P(\text{49 heads} \mid P = \frac{2}{3}) = \choose{80}{49} \frac{2}{3}^49 \frac{1}{3}^31 = 0.054
$$

Therefore, $\frac{2}{3}$ is the maximum likelihood estimation for P of head

* A coin is flipped 100 times. Given that there were 55 heads, find the maximum likelihood estimation for probability of head on a single toss. (직관적으로 p가 0.55임을 추정해야 한다?)

$$
P(\text{head}) = \theta \\
f = \choose{100}{55} \cdot P^55 (1-p)^45
$$

To find the maximum point of the $f$, find the point that the first derivative of $f$ becomes 0.

$$
\choose{100}{55} \left( 55p^54(1-p)^45 - 45p^55 (1-p)^44) = 0 \\
p = 0.55
$$

* For the following random samples, find the likelihood function

    + a. $X_i \sim \text{Binominal}(3, \theta)$ and we observe $(X_1, X_2, X_3, X_4) = (1, 3, 2, 2)$

$$
L(X_1, X_2, X_3, X_4; \theta) = P_{X_1, X_2, X_3, X_4}(X_1, X_2, X_3, X_4) \\
= \choose{3}{x} \theta^x (1-\theta)^{3-x} \\
= \choose{3}{1} \theta^1 (1-\theta)^2 \cdot \choose{3}{3} \theta^3 (1-\theta)^0 \cdot \choose{3}{2} \theta^2 (1-\theta)^1 \cdot \choose{3}{2} \theta^2 (1-\theta)^1 \\
= 27 \theta^8 (1-\theta)^4 \\
\to \\
\frac{dL}{d\theta} = 27(8\theta^7(1-\theta)^4 - 4\theta^8(1-\theta)^3) = 0 \\
\to \theta = \frac{2}{3}
$$

세타 후보가 있으면, 세타에 대입해 어떤 게 최대인지 찾으면 됨 (discrete case)

    + b. $X_i \sim \text{Exponnential}(\theta$ and we observed $(X_1, X_2, X_3, X_4) = (1.23, 3.32, 1.98, 2.12)$

cf. $f_\text{exponential}(x) = \theta e^{-\theta x}$
$$
L(X_1, X_2, X_3, X_4; \theta) = P_{X_1, X_2, X_3, X_4}(X_1, X_2, X_3, X_4) \\
= \theta e^{-\theta -1.23} \cdot \theta e^{-\theta -3.32} \cdot \theta e^{-\theta -1.98} \cdot \theta e^{-\theta -2.12} \\
= \theta^4 e^{-\theta -8.65} \\
$$






























### References

$\tag*{}\label{n} \text{[n] }$
