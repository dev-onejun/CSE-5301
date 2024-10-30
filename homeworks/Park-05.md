$$
\begin{array}{c}
\huge{\text{Homework #5}} \\
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

##### 1. Suppose that we have a sample of 100 people and the random variable Xi  is the Height of the ith person (in centimeters). Knowing that all  Xi's are identically distributed and  expected value of Xi is 150 and standard deviation is 25, find the probability that the average height of these people is smaller than 155 cm. (15 points)

$\qquad$ With the given values, $n = 100$, $\bar{X} = 150$, $\sigma = 25$,

$$
\begin{aligned}
P(\bar{X} \lt 155) & = P\left(\frac{\bar{X} - \mu}{\sigma/\sqrt{n}} \lt \frac{155 - 150}{25/\sqrt{100}}\right) \\
& = P\left(Z \lt \frac{155 - 150}{25/\sqrt{100}}\right) \\
& = P(Z \lt 2) \\
& = 0.9772
\end{aligned}
$$

##### 2.The height of female students in a sate college follows normal distribution with mean of 62 inches and standard deviation 8 inches. (10 points each)

$\qquad$ Let $X$ be the height of female students in a sate college. Then, $X \sim N(62, 8^2)$

$\quad$ **A. Find the height below which is the shortest 30% of the female students.** \
$\qquad$ Let $A$ be the targeted height. Then,

$$
\begin{aligned}
& P(X \lt A) = 0.3 \\
& P\left(Z \lt \frac{A - 62}{8}\right) = 0.3 \\
& \frac{A - 62}{8} = -0.525 \\
& A = 57.8 \text{ inches}
\end{aligned}
$$

$\quad$ **B. Find the height above which is the tallest 5% of the female student** \
$\qquad$ Let $B$ be the targeted height. Then,

$$
\begin{aligned}
& P(X \gt B) = 0.05 \\
& P\left(Z \gt \frac{B - 62}{8}\right) = 0.05 \to P\left(Z \lt \frac{B - 62}{8}\right) = 0.95 \\
& \frac{B - 62}{8} = 1.645 \\
& B = 75.16 \text{ inches}
\end{aligned}
$$

##### 3. Assuming that our random variable Y belongs to Binomial distribution and Y∼ Binomial (n = 64, p = 1/4). Find the probability that Y > 15. (15 points)

$\qquad$ With the given values, $E(Y) = np = 64 \times \frac{1}{4} = 16$, $\sigma = \sqrt{np(1-p)} = \sqrt{64 \times \frac{1}{4} \times \frac{3}{4}} = \sqrt{12}$ \
$\qquad$ Since $n$ is large enough ($n \geq 30$), without using continuity correction,

$$
\begin{aligned}
P(Y \gt 15) & = 1 - P(Y \leq 15) \\
& = 1 - P(Z \leq \frac{15 - 16}{\sqrt{12}}) \\
& = 1 - P(Z \leq -0.2887) \\
& \simeq 1 - P(Z \leq -0.285) \\
& = 1 - \frac{0.38974 + 0.38591}{2} \\
& = 1 - 0.3878 \\
& = 0.6122
\end{aligned}
$$


##### 4. A company makes semiconductor chips with a  failure rate of 6.3%. Assume that chip failures are independent , and you will be producing 2,000 chips tomorrow.

$\qquad$ Let $X$ be the number of defective chips produced. Then, $X \sim Binomial(2000, 0.063)$

$\quad$ **A. Find the expected number of defective chips produced. (5 points)**

$$
E(X) = np = 2000 \times 0.063 = 126
$$

$\quad$ **B. Find the standard deviation of the number of defective chips. (5 points)**

$$
\sigma = \sqrt{np(1-p)} = \sqrt{2000 \times 0.063 \times 0.937} = \sqrt{118.062} \simeq 10.8656
$$

$\quad$ **C. Find the probability (approximate) that you will produce less than 135 defects. (10 points)**

$\qquad$ Likewise `3`, the number of trials is large enough, without using continuity correction,

$$
\begin{aligned}
P(X \lt 135) & = P\left(Z \lt \frac{135 - 126}{10.8656}\right) \\
& = P(Z \lt 0.8283) \\
& \simeq \frac{0.79389 + 0.79673}{2} \\
& = 0.79531 \\
& \simeq 0.7953
\end{aligned}
$$

##### 5. The random variable Xi is the waiting time  (in seconds) for the elevator to arrive once the ith person push the button and expected value of Xi is 20 and standard deviation is 8. Find the probability that the waiting time for 50 people is between 900 & 1100 seconds? (15 points)

$\qquad$ With the given values, $X_i \sim N(20, 8^2)$, \
$\qquad$ $E(Y) = 50 \times 20 = 1000$, $\sigma = \sqrt{50 \times 8^2} = 40 \sqrt{2}$, when $Y$ is the waiting time for 50 people. \
$\qquad$ Therefore,

$$
\begin{aligned}
P(900 \lt Y \lt 1100) & = P\left(\frac{900 - 1000}{40\sqrt{2}} \lt \frac{Y - 1000}{40\sqrt{2}} \lt \frac{1100 - 1000}{40\sqrt{2}}\right) \\
& = P\left( -1.7678 \lt Z \lt 1.7678 \right) \\
& = P(Z \lt 1.7678) - P(Z \lt -1.7678) \\
& \simeq \frac{0.9608 + 0.96164}{2} - \frac{0.03920 + 0.03836}{2} \\
& = 0.96122 - 0.03878 \\
& = 0.92244 \\
& \simeq 0.9224
\end{aligned}
$$

##### 6. Suppose that the weight of people in a specific town are normally distributed with the mean of 150 pounds and standard deviation of 20 pounds. Answer the following questions: (7.5 points each)

$\qquad$ Given that $X \sim N(150, 20^2)$ when $X$ is the weight (pounds) of people in a specific town,

$\quad$ **A. Find the percentage of the people who weight less than 140 pounds.**

$$
\begin{aligned}
P(X \lt 140) & = P\left(Z \lt \frac{140 - 150}{20}\right) \\
& = P(Z \lt -0.5) \\
& = 0.30854 \\
& \to 30.854\%
\end{aligned}
$$

$\quad$ **B. Find the percentage of people who weight more than 170 pounds.**

$$
\begin{aligned}
P(X \gt 170) & = 1 - P(X \leq 170) \\
& = 1 - P(Z \leq \frac{170 - 150}{20}) \\
& = 1 - P(Z \leq 1) \\
& = 1 - 0.84134 \\
& = 0.15866 \\
& \to 15.866\%
\end{aligned}
$$

