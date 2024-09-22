$$
\begin{array}{c}
\huge{\text{Homework #2}} \\
\hline
\text{Wonjun Park} \\
\text{Computer Science} \\
\href{mailto:wxp7177@mavs.uta.edu}{\text{wxp7177@mavs.uta.edu}} \\
\text{UTA ID: 1002237177} \\
\end{array}
$$

Please round to the nearest 4 digits after decimal point in your calculations.

Note that the problems are not intended to be realistic models for the corresponding situations but rather dramatically simplified scenarios.  This is individual work, and not a group project; do not share solutions. All work turned in must be your own work.

##### 1. Given the following data sets. Compute their mean,  variance  and median: (5 point each)

**a) { 5, 3, 2, 6, 7, 1, 2, 9, 5}** \
$\quad$ Mean = 4.4444, Variance = 6.2469, Median = 5 \
**b) { 4, 2, 3, 1 , 2 , 9 , 3,  5 , 4 , 1 , 4 , 5 , 8 }** \
$\quad$ Mean = 3.9231, Variance = 5.4556, Median = 4 \
**c) { 3, 2 , -8 ,  0 , 4 ,5 , -4 , 5,  8 ,  3, -1 }** \
$\quad$ Mean = 1.5455, Variance = 18.7934, Median = 3

##### 2. Suppose that we investigate the effects of some drug on Alzheimer disease and the probability of each drug being effective is 15%. Calculate the following (5 point each):

**The probability that the first effective drug is the 5th one that we examine.** \
$\quad$ $({85 \over 100})^4 \times {15 \over 100} = 0.0783$ \
**The probability that we find the first effective drug in the first 3 experiments( each experiment is with a new drug).** \
$\quad$ The effective drub can be found in the first, second, or third experiment so that the probability is \
$\quad\quad$ $\frac{15}{100} + (\frac{85}{100})^1 \times \frac{15}{100} + (\frac{85}{100})^2 \times \frac{15}{100} = 0.3859$ \
**Name the distribution.** \
$\quad$ Geometric Distribution

##### 3. Suppose that we investigate an apple store shop and saw on average that out of 20 customer, 15 of them want to buy the newest iPhone. We select 50 customer randomly, find the probability that (5 point each):

**More than 48 customers want to buy the newest iPhone.** \
$\quad$ According to the observation of the problem, the probability of the customer who wants to buy the newest iPhone is $\frac{15}{20} = 0.75$. Let $X$ be the random variable that represents the number of customers who want to buy the newest iPhone. The probability that more than 48 customers want to buy the newest iPhone is \
$\quad\quad$ $P(X > 48) = p(X = 49) + p(X = 50) = {50 \choose 49} \times 0.75^{49} \times 0.25^1 + {50 \choose 50} \times 0.75^{50} \times 0.25^0 = 0.00001$ \
**Exactly 36 customers want to buy the newest iPhone.** \
$\quad$ $P(X = 36) = {50 \choose 36} \times 0.75^{36} \times 0.25^{14} = 0.1110$ \
**What is the variance on the number of purchased iPhone.** \
$\quad$ This is a binomial distribution, the answer of the below question, so that the the variance is \
$\quad\quad$ $npq = 50 \times 0.75 \times 0.25 = 9.375$ \
**Name the distribution.** \
$\quad$ Binomial Distribution

##### 4. Suppose that we saw thunderstorm on average rate of 5 per month during Fall. Calculate the following(5 point each):

**The probability that during 2 months we see at most 6 thunderstorm.** \
$\quad$ The random variable $X$ follows a Poisson distribution. Adjusting the lambda value to 10, since the unit is 2 months, the probability that at most 6 thunderstorm is \
$\quad\quad$ $Pois(0; 10) + Pois(1; 10) + Pois(2; 10) + Pois(3; 10) + Pois(4; 10) + Pois(5; 10) + Pois(6; 10)$ \
$\quad\quad$ $= \frac{e^{-10} \times 10^0}{0!} + \frac{e^{-10} \times 10^1}{1!} + \frac{e^{-10} \times 10^2}{2!} + \frac{e^{-10} \times 10^3}{3!} + \frac{e^{-10} \times 10^4}{4!} + \frac{e^{-10} \times 10^5}{5!} + \frac{e^{-10} \times 10^6}{6!}$ \
$\quad\quad$ $= 0.1301$ \
**The probability that during 3 months we see exactly 10 thunderstorms.** \
$\quad$ Adjusting the lambda value to 15, since the unit is 3 months, the probability that exactly 10 thunderstorm is \
$\quad\quad$ $Pois(10; 15) = \frac{e^{-15} \times 15^{10}}{10!} = 0.0486$ \
**What is the expected value on the number of the thunderstorms?** \
$\quad$ The expected value of the Poisson distribution is $\lambda$. Therefore, the expected value per month is 5. \
**Name the distribution.** \
$\quad$ Poisson Distribution

##### 5. We have a four sided die and the die is not fair meaning that the probability of getting "1" is 3 times (*3) the probability of getting other values (2,3,4) but the probability of the other possibilities are equal. We define the random variable Z which shows the number when we roll the die. Calculate the following(5 point each):

$\quad$ In summary, the probability of getting "1" is $\frac{1}{2}$ and the probability of getting "2", "3", "4" is $\frac{1}{6}$.

**What is the expected value of Z?** \
$\quad$ The expected value of the random variable Z is \
$\quad\quad$ $E(Z) = 1 \times \frac{1}{2} + 2 \times \frac{1}{6} + 3 \times \frac{1}{6} + 4 \times \frac{1}{6} = 2$ \
**What is the probability mass function for the random variable Z?** \
$\quad$ The probability mass function for the random variable Z is \
$$
\begin{array}{cc}
P(Z = x) = & \begin{cases}
\frac{1}{2} & \text{if } x = 1 \\
\frac{1}{6} & \text{if } x = 2, 3, 4 \\
0 & \text{otherwise}
\end{cases}
\end{array}
$$
**Is it Uniform distribution? Explain your answer.** \
$\quad$ No, it is not a uniform distribution. The probability of getting "1" is $\frac{1}{2}$ and the probability of getting "2", "3", "4" is $\frac{1}{6}$. The uniform distribution is a distribution where the probability of each value is equal.

##### 6. We have a bag containing 7 red marbles and 8 blue marbles. we draw 5 marbles randomly without replacement. Calculate the following(5 point each):

**The probability that 3 of these balls are blue.** \
$\quad$ The probability that 3 of these balls are blue is \
$\quad\quad$ $\frac{ {8 \choose 3} \times {7 \choose 2} }{{15 \choose 5}} = 0.3916$ \
**The probability that at most 4 of them are blue marbles.** \
$\quad$ The probability that at most 4 of them are blue marbles is eqaul to the probability of (1 - the probability that 5 of them are blue marbles) \
$\quad\quad$ $1 - \frac{ {8 \choose 5} \times {7 \choose 0} }{{15 \choose 5}} = 0.9814$ \
**Name the distribution** \
$\quad$ Hypergeometric Distribution
