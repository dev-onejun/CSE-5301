$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

추가 문제
1. We have 2 cards. card number 1 is red on both sided. card number 2 is red on one side and black on the other side. We randomly pick a card and see one side is red. What is the chance that the other side is also red?

$$
\frac{2}{3}
$$
It is similar to the problem 망한 문제. 경우의 수 따져서 (4 -> 3 중 ) 푸는 게 빠름

another solution
$$
P(rr \mid r) = \frac{P(r \mid rr) \times P(rr)}{P(r)} = \frac{\frac{1}{2}}{\frac{3}{4}} = \frac{2}{3} \\
\begin{aligned}
\from & P(r \mid rr) \times P(rr) + P(r \mid rb) \times P(rb) = P(r) \\
& 1 \times \frac{1}{2} + \frac{1}{2} \times \frac{1}{2} = \frac{3}{4}
\end{aligned}
$$

2. Alice and Bob can finish a job in 2 hours, Alice and Charlie can finish a job in 3 hours, Bob and Charlie can finish a job in 4 hours. If 3 of them work together, how long does it take to finish the job?

$$
A + B = \frac{1}{2} \\
A + C = \frac{1}{3} \\
B + C = \frac{1}{4} \\
\to 2A + 2B + 2C = \frac{13}{12} \\
\to A + B + C = \frac{13}{24} \\
\to \frac{24}{13} = \text{1 hour 51 minutes}
$$

3. You are a prisoner sentenced to death. Emperor gives you chance to live by playing a simple game. 50 black marbles and 50 white marbles are placed with 2 empty bowls. You can divide the marbles into 2 bowls as you like. Then you will be blindfolded and the bowls will be shuffled. You will choose one marble from one bowl. If the marble is white, you will be free. If the marble is black, you will be executed. How do you divide the marbles?

$$
\text{Equally distributing is only one half} \\
\text{one white ball in a jar and 49 white balls and 50 black balls in the other jar is the maximum probability to live} \\
$$

추가 문제
1.

$$
S = \{ 1,2,3,4,5,6,7,8,9,10 \}
A = {1,2,3,4,5}, B = {4,5,6,7,8}, C = {7, 9}
$$

A and B = {4, 5}, P(A and B) = 2/10

  - are A and B mutually exclusive?
    - No, because they have elements in common.
  - Are A and C mutually exclusive?
    - Yes, because they have no elements in common.

2. Let event C be taking an English class and event D be taking a speech class. P(C) = 0.75, P(D) = 0.3, P(C|D) = 0.75, P(C and D) = 0.225
    a. are C and D mutually exclusive?
        - No, because P(C and D) is not 0.
    b. are they independent?
        - yes, because P(C and D) = P(C)P(D)
    c. Find P(D|C)
        - P(D|C) = P(C and D) / P(C) = 0.225 / 0.75 = 0.3
        - or with bayes theorem
            - P(D|C) = P(C|D)P(D) / P(C) = 0.75 * 0.3 / 0.75 = 0.3

3. Suppose that three coins are tossed. Let X be the number of heads observed. We want to construct a probability distribution for X and find the mean and standard deviation of X

$$
R_x = \{ 0, 1, 2, 3 \} \\
$$

$$
P(X = 0) = \frac{1}{8} \\
P(X = 1) = {3 \choose 1} {\frac{1}{2}}^1 {\frac{1}{2}}^2 = \frac{3}{8} \\
P(X = 2) = {3 \choose 2} {\frac{1}{2}}^2 {\frac{1}{2}}^1 = \frac{3}{8} \\
P(X = 3) = \frac{1}{8} \\
$$

$$
\begin{aligned}
E[X] & = \sum_{i=0}^{3} x_i P(X = x_i) = 0 \cdot \frac{1}{8} + 1 \cdot \frac{3}{8} + 2 \cdot \frac{3}{8} + 3 \cdot \frac{1}{8} = 1.5 \\
Var(X) & = E[X^2] - E[X]^2 \\
& \qquad E[X^2] = 0 \cdot \frac{1}{8} + 1 \cdot \frac{3}{8} + 4 \cdot \frac{3}{8} + 9 \cdot \frac{1}{8} = 3 \\
& \qquad E[X]^2 = 1.5^2 = 2.25 \\
& = 0.75
\end{aligned}
$$

4. A restaurant's computer chooses orders at random to receive a free app. each order has 1/18 chance of receiving a free app. Let X be the number of orders the restaurant fills before giving away 1st free app. Find the probability that restaurant first gives away an app on 6th order of the day.

$\qquad$ This is a Geometric distribution. Therefore,

$$
\begin{aligned}
P(X = 6) & = (1 - \frac{1}{18})^5 \cdot \frac{1}{18} = \frac{17}{18}^5 \cdot \frac{1}{18} \\
& = 0.0417
\end{aligned}
$$

5. Hospital records show that the probability of dying from a certain disease is 75%. What is the probability that with 6 randomly selected patients , 4 will recover?

$\qquad$ This is a Binomial distribution. Therefore,

$$
\begin{aligned}
P(X = 4) & = {6 \choose 4} \cdot 0.25^4 \cdot 0.75^2 \\
& = 15 \cdot 0.0039 \cdot 0.5625 \\
& = 0.0329
\end{aligned}
$$

6. A life insurance salesman sells on the average 3 life insurance policies per week.
  a. What is the probability in a given week he will sell 2 or more policies but less than 5?

$$
\begin{aligned}
P(2 \leq X \lt 5) & = P(X = 2) + P(X = 3) + P(X = 4) \\
& = e^{-3} \cdot \frac{3^2}{2!} + e^{-3} \cdot \frac{3^3}{3!} + e^{-3} \cdot \frac{3^4}{4!} \\
& = 0.6161
\end{aligned}
$$

  b. What is the probability that in a given week he will sell some policies?

$$
\begin{aligned}
1 - P(X = 0) & = 1 - e^{-3} \cdot \frac{3^0}{0!} \\
& = 0.9502
\end{aligned}
$$

  c. Assuming that there are 5 working days per week. What is the probability that in a given day he will sell 1 policy?

  $\qquad$ With adjusting $\lambda$ to 3/5,

$$
\begin{aligned}
P(X = 1) & = e^{-3/5} \cdot \frac{3/5}{1!} \\
& = 0.3293
\end{aligned}
$$

7. Consider two random variables X and Y with their joint PMF given in the table below.

| | Y = 0 | Y = 2 | Y = 3 |
|:---:|:---:|:---:|:---:|
| X = 1 | $\frac{1}{18}$ | $\frac{1}{9}$ | $\frac{1}{6}$ |
| X = 2 | $\frac{1}{6}$ | $\frac{1}{18}$ | $\frac{1}{9}$ |
| X = 3 | $\frac{1}{9}$ | $\frac{1}{9}$ | $\frac{1}{9}$ |

  a. Find P(X = 2, Y <= 2)
    - 1/6 + 1/18 = 2/9

  b. Find Marginal PMFs

$$
\begin{array}{cc}
P_X(x) = \begin{cases} \frac{1}{3} & x = 1 \\ \frac{1}{3} & x = 2 \\ \frac{1}{3} & x = 3 \\ 0 & \text{otherwise} \end{cases} & P_Y(y) = \begin{cases} \frac{1}{3} & y = 0 \\ \frac{5}{18} & y = 2 \\ \frac{7}{18} & y = 3 \\ 0 & \text{otherwise} \end{cases}
\end{array}
$$

  c. P(Y=2|X=1)
    - $\frac{ P(Y=2, X=1) }{ P(X=1) } = \frac{1/9}{1/3} = 1/3$

  d. Are X and Y independent?
    - No. Because $P(X=1, Y=0) \neq P(X=1)P(Y=0)$

8. Consider two random variables X and Y with the joint PMF given in the table below. and let Z = E[X|Y]

$$
\begin{array}{c|c|c}
X \backslash Y & 0 & 1 \\
\hline
0 & \frac{1}{5} & \frac{2}{5} \\
\hline
1 & \frac{2}{5} & 0 \\
\hline
\end{array}
$$

  a. Find Marginal PMF of X and Y

$$
\begin{array}{cc}
P_X(x) = \begin{cases} \frac{3}{5} & x = 0 \\ \frac{2}{5} & x = 1 \\ 0 & \text{otherwise} \end{cases} & P_Y(y) = \begin{cases} \frac{3}{5} & y = 0 \\ \frac{2}{5} & y = 1 \\ 0 & \text{otherwise} \end{cases}
\end{array}
$$

  b. Find Conditional PMF of X given that Y=0 and Y=1

$$
\begin{array}{cc}
P_{X|Y}(x|0) =
\begin{cases} P(X = 0 \mid Y = 0) = \frac{P(X = 0, Y = 0)}{P(Y = 0)} = \frac{1/5}{3/5} = \frac{1}{3} & x = 0 \\
P(X = 1 \mid Y = 0) = \frac{P(X = 1, Y = 0)}{P(Y = 0)} = \frac{2/5}{3/5} = \frac{2}{3} & x = 1
\end{cases}
&
P_{X|Y}(x|1) =
\begin{cases} P(X = 0 \mid Y = 1) = \frac{P(X = 0, Y = 1)}{P(Y = 1)} = \frac{2/5}{2/5} = 1 & x = 0 \\
P(X = 1 \mid Y = 1) = \frac{P(X = 1, Y = 1)}{P(Y = 1)} = \frac{0}{2/5} = 0 & x = 1
\end{cases}
\end{array}
$$

  c. Find PMF of the random variable $Z$ 잘모르겠담..

$$
E[X|Y] = \sum_{i} x_i P_{X|Y}(x_i|y) ??
$$

$$
\begin{aligned}
E[X \mid Y = 0] & = 0 \cdot \frac{1}{3} + 1 \cdot \frac{2}{3} & = \frac{2}{3} \\
E[X \mid Y = 1] & = 0 \cdot 1 + 1 \cdot 0 & = 0
\end{aligned}
$$

$$
P_Z(z) = \begin{cases} \frac{3}{5} & z = \frac{2}{3} \\ \frac{2}{5} & z = 0 \\ 0 & \text{otherwise} \end{cases}
$$

  d. Find the mean and variance of Z

$$
\begin{aligned}
E[Z] & = \frac{3}{5} \cdot \frac{2}{3} + \frac{2}{5} \cdot 0 = \frac{2}{5} \\
Var(Z) & = E[Z^2] - E[Z]^2 \\
& = \frac{3}{5} \cdot \frac{4}{9} + \frac{2}{5} \cdot 0 - \frac{4}{25} \\
& = \frac{8}{75}
\end{aligned}
$$










### References

$\tag*{}\label{n} \text{[n] }$
