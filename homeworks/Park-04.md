$$
\begin{array}{c}
\huge{\text{Homework #4}} \\
\hline
\text{Wonjun Park} \\
\text{Computer Science} \\
\href{mailto:wxp7177@mavs.uta.edu}{\text{wxp7177@mavs.uta.edu}} \\
\text{UTA ID: 1002237177} \\
\end{array}
$$

$\cdot$ Note that the problems are not intended to be realistic models for the corresponding situations but rather dramatically simplified scenarios. \
$\cdot$ This is individual work, and not a group project; do not share solutions. All work turned in must be your own work. \
$\cdot$ Also Include all the steps for calculating any part, Just the correct answer is not enough \
$\cdot$ Please round to the nearest 4 decimal places in your calculations.

##### 1. Given two random variables X and Y and their joint distribution P(X,Y):

| | X = 2 | X = 4 | X = 6 |
| --- | --- | --- | --- |
| Y = Red (2) | 0.02 | 0.15 | 0.08 |
| Y = Blue (4) | 0.2 | 0.08 | 0.12 |
| Y = Green (6) | 0.08 | 0.12 | 0.15 |

$\quad$ **Find:**

$\quad$ **1.a) H(X)  (7 points)**

$\qquad$ $P(X=2) = 0.3$, $P(X=4) = 0.35$, $P(X=6) = 0.35$. \
$\qquad$ Therefore,

$$
\begin{aligned}
H(X) &= - \sum_{x} P(X=x) \log_2 P(X=x) \\
&= - \left( 0.3 \log_2 0.3 + 0.35 \log_2 0.35 + 0.35 \log_2 0.35 \right) \\
&= 1.5813 \text{ bits}
\end{aligned}
$$

$\quad$ **1.b) H(Y)  (7 points)**

$\qquad$ $P(Y=\text{Red}) = 0.25$, $P(Y=\text{Blue}) = 0.4$, $P(Y=\text{Green}) = 0.35$. \
$\qquad$ Therefore,

$$
\begin{aligned}
H(Y) &= - \sum_{y} P(Y=y) \log_2 P(Y=y) \\
&= - \left( 0.25 \log_2 0.25 + 0.4 \log_2 0.4 + 0.35 \log_2 0.35 \right) \\
&= 1.5589 \text{ bits}
\end{aligned}
$$

$\quad$ **1.c.) D(X||Y)  (7 points)**

$\qquad$ The rewritten table of $X$ and $Y$ is as follows:

$$
\begin{array}{c|cc}
& X & Y \\
\hline
2 & 0.3 & 0.25 \\
4 & 0.35 & 0.4 \\
6 & 0.35 & 0.35 \\
\end{array}
$$

$\qquad$ Therefore,

$$
\begin{aligned}
D(X \mid\mid Y) &= 0.3 \log_2 \frac{0.3}{0.25} + 0.35 \log_2 \frac{0.35}{0.4} + 0.35 \log_2 \frac{0.35}{0.35} \\
&= 0.3 \log_2 1.2 + 0.35 \log_2 0.875 + 0.35 \log_2 1 \\
&= 0.3 \times 0.2630 + 0.35 \times -0.1926 + 0.35 \times 0 \\
&= 0.0789 - 0.0674 \\
&= 0.0115 \text{ bits}
\end{aligned}
$$

$\quad$ **1.d) D(Y||X)  (7 points)**

$\qquad$ According to the rewritten table in `1.c`, $D(Y \mid\mid X)$ is

$$
\begin{aligned}
D(Y \mid\mid X) &= 0.25 \log_2 \frac{0.25}{0.3} + 0.4 \log_2 \frac{0.4}{0.35} + 0.35 \log_2 \frac{0.35}{0.35} \\
&= 0.25 \log_2 0.8333 + 0.4 \log_2 1.1429 + 0.35 \log_2 1 \\
&= 0.25 \times -0.2631 + 0.4 \times 0.1927 + 0.35 \times 0 \\
&= -0.0658 + 0.0771 \\
&= 0.0113 \text{ bits}
\end{aligned}
$$

$\quad$ **1.e) H(X|Y)  (7 points)**

$\qquad$ From the result in `1.b`, $H(Y) = 1.5589$ bits, $H(X \mid Y)$ can be calculated as

$$
\begin{aligned}
H(X \mid Y) &= H(X,Y) - H(Y) \\
&= - \sum_{x} \sum_{y} P(X=x, Y=y) \log_2 P(X=x, Y=y) - 1.5589 \\
&= - ( 0.02 \log_2 0.02 + 0.15 \log_2 0.15 + 0.08 \log_2 0.08 + 0.2 \log_2 0.2 + 0.08 \log_2 0.08 + 0.12 \log_2 0.12 + \\
& \qquad\quad 0.08 \log_2 0.08 + 0.12 \log_2 0.12 + 0.15 \log_2 0.15 ) - 1.5589 \\
&= - \left( -0.1129 -0.4105 -0.2915 -0.4644 -0.2915 -0.3671 -0.2915 - 0.3671 -0.4105 \right) - 1.5589 \\
&= 3.0070 - 1.5589 \\
&= 1.4481 \text{ bits}
\end{aligned}
$$

$\quad$ **1.f) H(Y|X)  (7 points)**

$\qquad$ From the results in `1.a`, $H(X) = 1.5813$ bits, and `1.e`, $H(X,Y) = 3.007$ , $H(Y \mid X)$ can be calculated as

$$
\begin{aligned}
H(Y \mid X) &= H(X,Y) - H(X) \\
&= 3.007 - 1.5813 \\
&= 1.4257 \text{ bits}
\end{aligned}
$$

$\quad$ **1.g) H(X,Y)  (7 points)**

$\qquad$ $H(X,Y)$ was derived in `1.e` as $3.007$ bits.

$\quad$ **1.h) H(Y) - H(Y|X)  (7 points)**

$\qquad$ From the results in `1.b`, $H(Y) = 1.5589$ bits, and `1.f`, $H(Y \mid X) = 1.4257$ bits, \
$\qquad\qquad$ $H(Y) - H(Y \mid X) = 1.5589 - 1.4257 = 0.1332$ bits

$\quad$ **1.i)  I(X;Y)  (7 points)**

$\qquad$ Mutual Information $I(X;Y)$ \
$\qquad\qquad$ = $H(X) - H(X \mid Y)$ \
$\qquad\qquad$ = $H(Y) - H(Y \mid X)$ \
$\qquad\qquad$ = $H(X) + H(Y) - H(X,Y)$

$\qquad$ Therefore,

$$
\begin{aligned}
I(X;Y) &= 1.5813 - 1.4481 \\
&= 1.5589 - 1.4257 \\
&= 1.5813 + 1.5589 - 3.007 \\
&= 0.1332 \text{ bits}
\end{aligned}
$$

$\quad$ **1.j) If X is the number of wheels on a vehicle and Y is the color of the vehicle, what does I(X;Y) tell us? (Let’s say we can observe the number of wheels easily but not the color)   (7 points)**

$\qquad$ The mutual information $I(X;Y)$ tells the amount of uncertainty between the number of wheels and the color of the vehicle. Since the number of wheels is easily observed, the mutual information value $0.1332$ bits indicates that they are not independent but have a small relationship between them.

##### 2. Using a standard (balanced) die, the following sequence of numbers is rolled : 5, 4, 2. Compute the amount of information in bits for this event (i.e. the minimal amount of information required to store this sequence). (10 points)

$\qquad$ The probability of each number on a balanced die is $\frac{1}{6}$ so that the probability of the given sequence $5, 4, 2$ is $\left( \frac{1}{6} \right)^3 = \frac{1}{216}$. \
$\qquad$ Therefore, the amount of information in bits for this event is

$$
\begin{aligned}
I &= - \log_2 P \\
&= - \log_2 \frac{1}{216} \\
&= \log_2 216 \\
&= 7.7549 \text{ bits}
\end{aligned}
$$

##### 3. Consider two die, one being balanced, i.e. the probability of each of the 6 numbers is equal, and one which is loaded where the probability of 1 is 0.25, the probability of 5 is 0.35, and the probability of the other numbers are equal. Compute the entropy an event produced by each of the two dice. (10 points)

$\qquad$ Let $X$ be the random variable representing the outcome of the balanced die and $Y$ be the random variable representing the outcome of the loaded die. The tables of $X$ and $Y$ are

$$
\begin{array}{cc}
\textrm{Balanced Die} & \textrm{Loaded Die} \\
\begin{array}{c|cccccc}
X & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
P(X) & \frac{1}{6} & \frac{1}{6} & \frac{1}{6} & \frac{1}{6} & \frac{1}{6} & \frac{1}{6}
\end{array}
&
\begin{array}{c|cccccc}
Y & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
P(Y) & 0.25 & 0.1 & 0.1 & 0.1 & 0.35 & 0.1
\end{array}
\end{array}
$$

$\qquad$ Since $X$ and $Y$ are independent, the joint probability of them is

$$
\begin{array}{c|cccccc}
Y\text{\\}X & 1 & 2 & 3 & 4 & 5 & 6 \\
\hline
1 & 0.0417 & 0.0417 & 0.0417 & 0.0417 & 0.0417 & 0.0417 \\
2 & 0.0167 & 0.0167 & 0.0167 & 0.0167 & 0.0167 & 0.0167 \\
3 & 0.0167 & 0.0167 & 0.0167 & 0.0167 & 0.0167 & 0.0167 \\
4 & 0.0167 & 0.0167 & 0.0167 & 0.0167 & 0.0167 & 0.0167 \\
5 & 0.0583 & 0.0583 & 0.0583 & 0.0583 & 0.0583 & 0.0583 \\
6 & 0.0167 & 0.0167 & 0.0167 & 0.0167 & 0.0167 & 0.0167 \\
\end{array}
$$

$\qquad$ Therefore, the joint entropy of $X$ and $Y$ is

$$
\begin{aligned}
H(X,Y) &= - \sum_{x} \sum_{y} P(X=x, Y=y) \log_2 P(X=x, Y=y) \\
&= - \left( 6 \times 0.0417 \log_2 0.0417 + 24 \times 0.0167 \log_2 0.0167 + 6 \times 0.0583 \log_2 0.0583 \right) \\
&= - \left( -1.1469 -2.3663 -1.4343 \right) \\
&= 4.9475 \text{ bits}
\end{aligned}
$$

##### 4.  The entropy of a probability distribution is 3.6 bits. Is this enough information to calculate how many Hartleys the entropy of the same distribution is? If it can be calculated, how many Hartleys is it? How would the answer change if we were asking about nat-s? (10 points)

$\qquad$ The given information is enough to calculate Hartleys and nats. \
$\qquad$ With the feature of the logarithm, the entropy in bits is converted as follows:

$$
3.6 \text{ bits} = \sum_{x \in X} x \log_2 x = \log_2 y^y \qquad \text{where y is the multiplication of } x^x \text{ for all } x \in X \\
\to y^y = 2^{3.6}
$$

$\qquad$ Therefore, the entropies in Hartleys and nats are

$$
\begin{aligned}
(1) \log_{10} y^y &= \log_{10} 2^{3.6} &= 1.0837 \text{ Hartleys} \\
(2) \log_{e} y^y &= \log_{e} 2^{3.6} &= 2.4953 \text{ nats}
\end{aligned}
$$
