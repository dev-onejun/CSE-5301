$$
\begin{array}{c}
\huge{\text{Homework #3}} \\
\hline
\text{Wonjun Park} \\
\text{Computer Science} \\
\href{mailto:wxp7177@mavs.uta.edu}{\text{wxp7177@mavs.uta.edu}} \\
\text{UTA ID: 1002237177} \\
\end{array}
$$

Note that the problems are not intended to be realistic models for the corresponding situations but rather dramatically simplified scenarios. This is individual work, and not a group project; do not share solutions. All work turned in must be your own work.

##### 1. The random variable X is given by the following PDF. (9 points each)

$$
f(x) = \frac{3}{2} (1 - x^2), \quad 0 \leq x \leq 1
$$

$\quad$ **1. Check that this is a valid PDF** \
$\qquad$ The integral of the function should be equal to 1 to be a valid PDF. \
$\qquad\qquad$ $\int_{0}^{1} \frac{3}{2} (1 - x^2) dx = \frac{3}{2} \int_{0}^{1} 1 - x^2 dx = \frac{3}{2} \left[ x - \frac{x^3}{3} \right]_{0}^{1} = \frac{3}{2} \left( 1 - \frac{1}{3} \right) = \frac{3}{2} \cdot \frac{2}{3} = 1$ \
$\qquad$ Therefore, the function is valid for PDF. \
$\quad$ **2. Calculate expected value of X** \
$\qquad$ $\int_{0}^{1} x \cdot \frac{3}{2} (1 - x^2) dx = \frac{3}{2} \int_{0}^{1} x - x^3 dx = \frac{3}{2} \left[ \frac{x^2}{2} - \frac{x^4}{4} \right]_{0}^{1} = \frac{3}{2} \left( \frac{1}{2} - \frac{1}{4} \right) = \frac{3}{2} \cdot \frac{1}{4} = \frac{3}{8}$ \
$\quad$ **3. Calculate the standard deviation of X** \
$\qquad$ To get the standard deviation, the variance is firstly needed. \
$\qquad\qquad$ $\int_{0}^{1} (x - \mu)^2 \cdot \frac{3}{2} (1 - x^2) dx = \int_{0}^{1} x^2 \cdot \frac{3}{2} (1 - x^2) dx - \mu^2 = \frac{3}{2} \int_{0}^{1} x^2 - x^4 dx - \mu^2 = \frac{3}{2} \left[ \frac{x^3}{3} - \frac{x^5}{5} \right]_{0}^{1} - \mu^2 = \frac{3}{2} \left( \frac{1}{3} - \frac{1}{5} \right) - \mu^2$ \
$\qquad\qquad\qquad = \frac{3}{2} \cdot \frac{2}{15} - \mu^2 = \frac{1}{5} - \mu^2$ \
$\qquad$ The $\mu$ is the expected value of X, which is derived as $\frac{3}{8}$ in the previous question so that the variance is $\frac{1}{5} - \left( \frac{3}{8} \right)^2 = \frac{19}{320}$ \
$\qquad$ Hence, the standard deviation is $\sqrt{\frac{19}{320}} \fallingdotseq 0.24367$

##### 2. A specific computer part lasts 10 years on average. The length of time the computer part lasts is exponentially distributed.

$\quad$ **1. What is the probability that a computer part lasts more than 6 years? (8 points)** \
$\qquad$ A continuous random variable X is exponentially distributed, and the mean of the distribution is given as $\mu = 10$. \
$\qquad$ From $\lambda = \frac{1}{\mu}$, the rate parameter is $\lambda = \frac{1}{10} = 0.1$. \
$\qquad$ The PDF of the exponential distribution $f(x) = \lambda e^{-\lambda x}$. Therefore, the probability that a computer part lasts more than 6 years is \
$\qquad\qquad$ $\int_{0}^{6} 0.1 e^{-0.1 x} dx = -e^{-0.1 x} \Big|_{0}^{6} = -e^{-0.1 \cdot 6} - (-e^{-0.1 \cdot 0}) = (-e^{-0.6}) - (-1) = 1 - e^{-0.6} \fallingdotseq 0.451188$ \
$\quad$ **2. On the average, how long would 3 computer parts last if they are used one after another? (5 points)** \
$\qquad$ Each computer part lasts 10 years on average independently so that the expected value of the sum of three computer parts is \
$\qquad\qquad$ $10 + 10 + 10 = 30$ years. \
$\quad$ **3. What is the probability that a computer part lasts between nine and 11 years? (8 points)** \
$\qquad$ The probability that a computer part lasts between 9 and 11 years is \
$\qquad\qquad$ $\int_{9}^{11} 0.1 e^{-0.1 x} dx = -e^{-0.1 x} \Big|_{9}^{11} = (-e^{-1.1}) - (-e^{-0.9}) = e^{-0.9} - e^{-1.1} \fallingdotseq 0.073699$

##### 3.You are given that random variable Y belongs to continuous uniform distribution between 100 and 300 (Y∼U(100,300)). Calculate  the following : (8 points each)

$\quad$ **1. P(Y>174)** \
$\qquad$ The PDF of the continuous uniform distribution is $f(y) = \frac{1}{300 - 100} = \frac{1}{200}$ for $100 \leq y \leq 300$. \
$\qquad$ Therefore, the probability that Y is greater than 174 is \
$\qquad\qquad$ $\int_{174}^{300} \frac{1}{200} dy = \frac{1}{200} \int_{174}^{300} 1 dy = \frac{1}{200} \left[ y \right]_{174}^{300} = \frac{1}{200} \left( 300 - 174 \right) = \frac{126}{200} = 0.63$ \
$\quad$ **2. P(100<Y<226)** \
$\qquad$ Aslike the previous question, the probability that Y is between 100 and 226 is \
$\qquad\qquad$ $\int_{100}^{226} \frac{1}{200} dy = \frac{1}{200} \int_{100}^{226} 1 dy = \frac{1}{200} \left[ y \right]_{100}^{226} = \frac{1}{200} \left( 226 - 100 \right) = \frac{126}{200} = 0.63$ \
$\quad$ **3. What is the expected value and standard deviation?** \
$\qquad$ The expected value of the continuous uniform distribution is $\frac{a+b}{2}$ and the standard deviation is $\frac{b-a}{\sqrt{12}}$. \
$\qquad$ Therefore, the expected value is $\frac{100+300}{2} = 200$ and the standard deviation is $\frac{300-100}{\sqrt{12}} = \frac{200}{\sqrt{12}} \fallingdotseq 57.735$

##### 4. Assume that an average of 30 customers per hour arrive at a store and the time between arrivals is exponentially distributed. (7 points each)

$\quad$ **1. On average, how many minutes elapse between two successive arrivals?** \
$\qquad$ A continuous random variable X is exponentially distributed, and the mean of the distribution is given as $\mu = \frac{30 \text{ customers}}{1 \text{ hour}} = 30$. \
$\qquad$ Converting the mean into the scale of minutes, $\mu = \frac{30 \text{ customers}}{60 \text{ minutes}} = 0.5$ customers per minute. \
$\qquad$ As a consequence, the average time between two successive arrivals is $\frac{1}{0.5} = 2$ minutes. \
$\quad$ **2. When the store first opens, how long on average does it take for three customers to arrive?** \
$\qquad$ The average time for three customers to arrive is $2 \times 3 = 6$ minutes. \
$\quad$ **3. After a customer arrives, find the probability that it takes less than one minute for the next customer to arrive.** \
$\qquad$ The rate parameter of the exponential distribution is $\lambda = \frac{1}{\mu} = \frac{1}{0.5} = 2$. \
$\qquad$ The probability that it takes less than one minute for the next customer to arrive is \
$\qquad\qquad$ $P(X < 1) = \int_{0}^{1} 2 e^{-2x} dx = -e^{-2x} \Big|_{0}^{1} = -e^{-2} - (-e^{-0}) = 1 - e^{-2} \fallingdotseq 0.86466 \quad (x \geq 0)$ \
$\quad$ **4. After a customer arrives, find the probability that it takes more than five minutes for the next customer to arrive.** \
$\qquad$ The probability that it takes more than five minutes for the next customer to arrive is \
$\qquad\qquad$ $P(X > 5) = \int_{5}^{\infty} 2 e^{-2x} dx = -e^{-2x} \Big|_{5}^{\infty} = 0 - (-e^{-10}) = e^{-10} \fallingdotseq 0.0000453999$
