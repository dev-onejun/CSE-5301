# What Something Exists in Everyday Life: A Review of Probability and Statistics

$$
\mathbf{\text{Wonjun Park}} \\
\text{Computer Science} \\
\text{University of Texas at Arlington} \\
\text{Arlington, TX, United States} \\
\text{wxp7177@mavs.uta.edu}
$$

##### *Abstract*

$$
\mathbf{\text{Acronym and Abbreviation}} \\
\begin{array}{|c|c|}
\hline
\text{Probability Mass Function (PMF)} & \text{Cumulative Mass Function (CMF)} \\
\hline
\text{Probability Density Function (PDF)} & \text{Cumulative Distribution Function (CDF)} \\
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

### I. Introduction

### II. Literature Review

#### A. Basic Definition of Probability

Probability is observed as randomness and uncertainty in daily lives. *Relative Frequency* refers to the ratio of how often an event occurs relative to the total number of trials. However, situations occured in everyday seem that probabilities observed from *Relative Frequency* are not matched with the common sense. For example, two coins continously flipped are not always (Head, Tail) or (Tail, Head). *The law of large numbers* demonstrates that if the number of trials become higher, *Relative Frequency* will converge to this common sense. The probability of the flipped coin is $1 \over 2$ so that the result, flipped 100 times, may become 50 Head and 50 Tail.

The language that Probability uses is *Set theory*. The following table is a example of the *Set theory* language.

$$
\begin{array}{|c|}
\hline
\text{Universal set } \mathbf{S} = \{H, T\} \text{, when it comes to flipping a coin once} \\
\text{Integer set } \mathbf{Z} \text{ | 1 } \in Z, {1 \over 2} \notin Z \\
\hline
\text{1) When sets are disjoint AND } A_1 \cup A_2 \cup \cdots \cup A_n = A, \text{the sets is called as }\mathbf{\text{Partitions of a set}} \\
\text{2) If two or more sets do not have common elements (the intersections are empty), they are called }\mathbf{\text{Mutually exclusive sets}} \\
\hline
\end{array}
$$

*Venn Diagrams* are useful visualization tools, allowing to observe the relationship between sets.

Four *Set Operations* is enabled to *Set theory*; **1) Union** is a operation that makes a combined set from the targeted two sets without duplication. For instance, $A = \{1, 2\}, B = \{2, 3\} \to A \cup B = \{1, 2, 3\}$. **2) Intersection** emits a set which contains the only duplicated elements between the two sets. From the previous example, $A \cap B = \{ 2\}$. **3) Complement**, marked as $A^c$ or $\bar{A}$, derives a set which everything in $S$ but not in the set. **4) Difference** produces a set everything in the original set, but not in the minus set. Likewise with the above example, $A - B = A \cap B^c = \{ 1\}$.

*Cardinality* $\|A\|$ means the size of the set. If the set $A$ has its elements $\{2,4,6,8,10\}$, the value $\|A\| = 5$.

With these definition, three following rules are derived;

$$
\begin{array}{|c|c|}
\hline
\text{1) De Morgan's Law} & \text{For any sets } A_1, A_2, \cdots, A_n, \\
& (A_1 \cup A_2 \cup \cdots \cup A_n)^c = A_1^c \cap A_2^c \cap \cdots \cap A_n^c \\
& (A_1 \cap A_2 \cap \cdots \cap A_n)^c = A_1^c \cup A_2^c \cup \cdots \cup A_n^c \\
\hline
\text{2) Distributive Law} & \text{For any sets } A, B, C, \\
& A \cap (B \cup C) = (A \cap B) \cup (A \cap C) \\
& A \cup (B \cap C) = (A \cup B) \cap (A \cup C) \\
\hline
\text{3) Inclusion-exclusion Principle} & \text{The principle met the formula with its regular rule even if the number of the sets increases} \\
& |A \cup B| = |A| + |B| - |A \cap B|, \\
& |A \cup B \cup C| = |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C| \\
\hline
\end{array}
$$

A *random experiment* is a process that a result occurs uncertainly. Observing with the random experiment, all possible outcomes can be observed. These outcomes are called as the *sample space*. In other words, the *sample space* becomes *universal set* in the context of a *random experiment*. Take a fair coin for example. If a coin were flipped, the possible results of the flip are head and tail so that *sample space*, a *universal set* $S$, is $\{H, T \}$.

A subset of *sample space* is called an *event*. With this definition about *event*, the probability of the event can be calculated. Likewise with the example of the fair coin, a *event* $A$ can be defined as the result of the flip is head. In this case, the probability of the event $P(A)$ is $1 \over 2$.

*Random Variables* are informally defined as a quantity or object which depends on *random experiments*. For instance, a *random variable* $A$ can be defined as "True, if a randomly drawn person from our class is female."

Normally, *random variables* are categorized as four types: **1)** *Propositional* random variables, **2)** *Multivalued* random variables, **3)** *Discrete Real-valued* random variables, and **4)** *Continuous Real-valued* random variables.

*Propositional* random variables are the simplest type of *random variables*. It is defined as a *random variable* that can take only two values, true or false. For instance, whether it will rain tomorrow or not is a *propositional* random variable. This boolean type of *random variable* follows the axioms below.

$$
\begin{aligned}
& P(A) \in [0, 1] \\
& P(\text{true}) = 1, P(\text{false}) = 0 \\
& P(A \cup B) = P(A) + P(B) - P(A \cap B) \\
& P(A \cap B) = P(A) \cdot P(B|A) \\
& P(A) + P(\neg A) = 1
\end{aligned}
$$

*Multivalued* random variables are the *random variables* that can take more than two values. For example, the result of a dice roll is a *multivalued* random variable. The probability of the event that the result of the dice roll is 4 is $P(A) = {1 \over 6}$. The axioms of *multivalued* random variables are as follows.

$$
\begin{aligend}
& P(A = a_i) \in [0, 1] \\
& P(S) = 1, P(\emptyset) = 0 \\
& P(A \cup B) = P(A) + P(B) - P(A \cap B) \\
& P(A \cap B) = P(A) \cdot P(B|A) \\
& \sum_{i=1}^{n} P(A = a_i) = 1
\end{aligned}
$$

*Discrete (Real-valued)* random variables are the *random variables* that can take countable number of values. For example, the number of students in a class is a *discrete real-valued* random variable.
*PMF* is a function, used in *discrete* random variables, which maps the probability of each value. $RX$ is a countable set of values that the *discrete* random variable can take. The definition of the PMF is

$$
\begin{array}{c|cc}
px(x) = & P(X = x), & \text{if x in RX} \\
& 0, & \text{otherwise}
\end{array}
$$

![img](https://upload.wikimedia.org/wikipedia/commons/thumb/8/85/Discrete_probability_distrib.svg/2880px-Discrete_probability_distrib.svg.png)
$\text{Fig 1. An example of PMF [}\href{#mjx-eqn-1}{1} \text{]}$

*Continuous (Real-valued)* random variables are the *random variables* that can take infinitely many values. For example, the height of a person is a *continuous real-valued* random variable. The one thing that needs to be cautious is that the probability of a single value in a *continuous* random variable is zero. For instance, if a *continuous* random variable $X \in [0, 10]$, uniformly distributed, the probability of the event $P(X = 5)$ is zero.

*CMF* is a function, used in *random variables*, which maps the probability of the event that the random variable is less than or equal to a certain values. The function is defined as $CMF(x) = P(X \le x)$.
*PDF* is used to specify the probability of the *continuous random variables* falling within a particular range of values. This probability is given by the integral of these variables over the range. In other words, the area under the density function but above the horizontal axis and between the lowest and the greatest variable values is the probability of the random variable. The valid *PDF* must satisfy the following conditions: **1)** $f(x) \ge 0$ for all $x$. **2)** $\int_{-\infty}^{\infty} f(x) dx = 1$.

![img](https://upload.wikimedia.org/wikipedia/commons/4/4f/4_continuous_probability_density_functions.png)
$\text{Fig 2. An Example of Four Continuous PDF functions [} \href{#mjx-eqn-2}{2} \text{]}$

*CDF* is a function, used in *continuous* random variables, which maps the probability of the event that the random variable is less than or equal to a certain values. The function is defined as $F(x) = P(X \le x)$.

With the definition of *random experiments* and *random variables*, three *axioms of probability* can be defined as follows: **1)** For any event $A$, $P(A) \ge 0$. **2)** The probability of the sample space $P(S)$ is always $1$. **3)** For disjoint events greater than or equal to 2, the probability of the union of these events is equal to the sum of the probabilities of these events. $P(A_1 \cup A_2 \cup \cdots) = P(A_1) + P(A_2) + \cdots$

*Conditional Probability* refers to the probability which has been considered after certain observations or facts. For instance, in poker cards, if a selected card were a black, then what is the probability of the card being a spade? The probability of the card being a spade is the *Conditional Probability*, and the answer is $P(\text{Spade} \| \text{Black}) = \frac{13}{26} = \frac{1}{2}$. The formula for *Conditional Probability* is given by

$$
P(A\|B) = \frac{P(A \cap B)}{P(B)} \\
\cdot \mathbf{\text{The Chain Rule: }} P(A \cap B) = P(A\|B)P(B) = P(B\|A)P(A)
$$

Two events $A$ and $B$ are independent if $P(A \cap B) = P(A)P(B)$. In other words, the occurrence of one event does not affect the probability of the other event. From the formula of *Conditional Probability*, if $A$ and $B$ are independent, then $P(A\|B) = P(A)$ and $P(B\|A) = P(B)$.

*Joint Probability* represents the probability of two events occurring simultaneously. Take the poker cards again as an example. The probability of selecting a black card and a spade card is $P(\text{Black} \cap \text{Spade}) = P(\text{Black}) \times P(\text{Spade}) = \frac{13}{52} = \frac{1}{4}$.

*Marginalization* is the process of obtaining the probability of a event by summing over all the possible values of the other event. For instance, the probability of selecting a black card is $P(\text{Black}) = P(\text{Black} \cap \text{Spade}) + P(\text{Black} \cap \text{Club}) = \frac{13}{52} + \frac{13}{52} = \frac{26}{52} = \frac{1}{2}$.

#### B. Bayes Theorem

*Bayes Theorem*, alternatively known as *Bayes'rule* or *Bayes' law*, is a formula that describes how to derive the probability of a hypothesis given the evidence. The formula is driven from the definition of *Conditional Probability* and given by

$$
P(A|B) = \frac{P(B|A)P(A)}{P(B)}
$$

#### C. Probability Distributions

*Probability Distributions* are the mathematical functions that provide the probabilities of occurrence of different possible outcomes in an experiment. *Probability Distributions* are categorized as **1)** *Discrete Probability Distributions* and **2)** *Continuous Probability Distributions*. *Discrete Probability Distributions*, known as PMF, are the distributions that can take only countable values. *Continuous Probability Distributions*, known as PDF, are the distributions that can take infinitely many values.

*Univariate Distributions* in *Probability Distributions*, unlike *Multivariate Distributions* which have more than one random variable, refers to the distribution that has only one random variable. the binomial distribution, the hypergeometric distribution, the normal distribution are the examples of *Univariate Distributions*. The multivariate normal distribution is a commonly encountered in *Multivariate Distributions*. For the summary simplification, the *Univariate Distributions* are discussed in this review.

*Mean* is the first moment of a distribution, which is the average value of the distribution and is denoted by $E(X)$ or $\mu$. *Variance* is the second moment of a distribution, which is the measure of the spread of the distribution and is denoted by $Var(X)$. *Standard Deviation* is the square root of the variance and is denoted by $SD(X)$ or $\sigma_x$. In **1)** *Discrete Probability Distributions*, the formulas of *Mean*, *Variance*, and *Standard Deviation* are given by

$$
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
$$

*Mean* is not enough to describe the distribution. Consider two random variables $X$ and $Y$ with the same mean. The distribution of $X$ can be more spread out than the distribution of $Y$. *Variance* is used to measure the spread of the distribution so that most moments of the distribution are utilized both *Mean* and *Variance* to describe the distribution. *Variance* is always non-negative, larger than or equal to zero, since it is the square of the difference between the *random variable* and the *mean*. The bigger the *Variance*, the more spread out the distribution is from the *mean* as well as the smaller the *Variance*, the more concentrated the distribution is around the *mean*.

The proof of the formula $(1)$ is as follows;

$$
\begin{array}{rcl}
Var(X) & = & E[(X - \mu)^2] \\
& = & E(X^2 - 2X\mu + \mu^2) \\
& = & E(X^2) - 2E(X)\mu + \mu^2 \\
& = & E(X^2) - 2\mu^2 + \mu^2 \\
& = & E(X^2) - \mu^2 \\
& = & E(X^2) - E(X)^2
\end{array}
$$

In **2)** *Continuous Probability Distributions*, the summation and the PMFs, in the formulas of *Mean*, *Variance*, and *Standard Deviation* above, are replaced by the integrals and the PDFs. The formula are given by

$$
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
$$

*Median* is the value that separates the higher half from the lower half of the data. It gives the advantage compared to the *Mean* that it is not affected by the outliers so that it may be more robust value to describe the distribution. If the number of the data is odd, the median is the middle value. If the number of the data is even, the median is the average of the two middle values. *Mode* is the value that appears most frequently in the data. The distribution can have more than one mode, not necessarily unique since the distribution can have more than one peak. The one peak distribution is called *Unimodal*, the two peak distribution is called *Bimodal*, and the more than two peak distribution is called *Multimodal*.

|![Visualization of Mean, Median, and Mode](https://upload.wikimedia.org/wikipedia/commons/3/33/Visualisation_mode_median_mean.svg)|
|:--:|

$\text{Fig 3. Geometric visualization of Mean, Median, and Mode in distributions}$

In symmetric unimodal distributions, the *Mean*, *Median*, and *Mode* are the same ($\text{Mean} = \text{Median} = \text{Mode}$). In the right-skewed distribution, the *Mean* is greater than the *Median*, and the *Median* is greater than the *Mode* ($\text{Mode} \lt \text{Median} \lt \text{Mean}$). In the left-skewed distribution, the *Mean* is less than the *Median*, and the *Median* is less than the *Mode* ($\text{Mode} \gt \text{Median} \gt \text{Mean}$).

#### D. Discrete Probability Distributions

Five discrete probability distributions are tackled in this review: **1)** **Binominal Distribution**, **2)** **Discrete Uniform Distribution**, **3)** **Poisson Distributions**, **4)** **Hypergeometric Distribution**, and **5)** **Geometric Distribution**.

**1) Binomial Distribution** is a distribution that describes the number of successes in a sequence of $n$ independent experiments. The distribution is characterized by two parameters: **1)** the number of trials $n$ and **2)** the probability of success $p$. The formula of the PMF of the Binomial Distribution is given by

$$
\begin{array}{c|ccc}
& \text{Mean} & = & np \\
P(X = k) = {n \choose k} p^k (1-p)^{n-k} & \text{Variance} & = & np(1-p) \\
& \text{Standard Deviation} & = & \sqrt{np(1-p)}
\end{array}
$$

where ${n \choose k} = \frac{n!}{k!(n-k)!}$ is the binomial coefficient. A coin tossed 5 times, A die rolled 25 times, and 50 chickens eggs examined are the examples of the Binomial Distribution.

The important thing is that the Binominal Distribution does not consider the order of the successes. The distribution that the order of the successes is considered is Geometric Distribution (5).

**2) Discrete Uniform Distribution** is a distribution that describes the probability of each value in the distribution is the same. The formula of the PMF of the Discrete Uniform Distribution is given by

$$
\begin{array}{c|ccc}
& \text{Mean} & = & \frac{a+b}{2} \\
P(X = k) = {1 \over n} \quad (k=[a,b], \; n=b-a+1)& \text{Variance} & = & \frac{n^2 - 1}{12} \\
& \text{Standard Deviation} & = & \sqrt{\frac{n^2 - 1}{12}}
\end{array}
$$

where $a$ and $b$ are the minimum and the maximum values of the distribution. The examples of the Discrete Uniform Distribution are the roll of a fair die, the selection of a card from a deck of cards, and the selection of a number from a set of numbers.

**3) Poisson Distribution** is a distribution that describes the number of events occurring in a fixed interval of time or space. The distribution is characterized by one parameter: the average number of events $\lambda$. The formula of the PMF of the Poisson Distribution is given by

$$
\begin{array}{c|ccc}
& \text{Mean} & = & \lambda \\
P(X = k) = \frac{e^{-\lambda} \lambda^k}{k!} & \text{Variance} & = & \lambda \\
& \text{Standard Deviation} & = & \sqrt{\lambda}
\end{array}
$$

The Poisson Distribution is used in the number of phone calls received by a call center in an hour, the number of emails received in a day, and the number of customers arriving at a store in an hour. The Poisson Distribution is a special case of the Binomial Distribution when the number of trials $n$ is large and the probability of success $p$ is small.

**If you confused about the lambda and mean of Poisson Distribution, just remember that the unit of the mean is a time.**

**4) Hypergeometric Distribution** is a distribution that describes the number of successes in a sequence of $n$ draws without replacement from a finite population of size $N$ that contains $K$ successes. The distribution is characterized by three parameters: the population size $N$, the number of available successes in the population $K$, the number of draws $n$, and the number of observed (curious) success $k$. The formula of the PMF of the Hypergeometric Distribution is given by

$$
\begin{array}{c|ccc}
& \text{Mean} & = & \frac{nK}{N} \\
P(X = k) = \frac{ {K \choose k} {N-K \choose n-k} }{ {N \choose n} } & \text{Variance} & = & n \frac{K}{N} \frac{N-K}{N} \frac{N-n}{N-1} \\
& \text{Standard Deviation} & = & \sqrt{n \frac{K}{N} \frac{N-K}{N} \frac{N-n}{N-1}}
\end{array}
$$

The distribution is simply considered as the probability of the possible cases with the combinations without replacements.

Finally, **5) Geometric Distribution** is a distribution that describes the number of trials needed to get the first success in a sequence of independent experiments. The distribution is characterized by one parameter: the probability of success $p$. The formula of the Geometric Distribution PMF is given by

$$
\begin{array}{c|ccc}
& \text{Mean} & = & \frac{1}{p} \\
P(X = k) = (1-p)^{k-1} p & \text{Variance} & = & \frac{1-p}{p^2} \\
& \text{Standard Deviation} & = & \sqrt{\frac{1-p}{p^2}}
\end{array}
$$

#### E. Continuous Probability Distributions

Four continuous probability distributions are addressed in this review: **1)** **Normal(Gaussian) Distribution**, **2)** **Exponential Distribution**, **3)** **Continuous Uniform Distribution**, and **4)** **Gamma Distribution**.

**1) Normal(Gaussian) Distribution** is a distribution that describes the probability of the continuous random variable whose distribution is symmetric and bell-shaped. The distribution is characterized by two parameters: the mean $\mu$ and the standard deviation $\sigma$. The formula of the Normal Distribution PDF is given by

$$
f(x) = \frac{1}{\sqrt{2\pi}\sigma} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

68% of the data falls within one standard deviation of the mean, 95% of the data falls within two standard deviations of the mean, and 99.7% of the data falls within three standard deviations of the mean.

The standard normal distribution, also known as Bell Curve, is a special case of the normal distribution when the mean $\mu = 0$ and the standard deviation $\sigma = 1$. The PDF of the standard normal distribution is always $f(x) = \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}}$. The standard normal distribution is also used to calculate the z-score, which is the number of standard deviations a data point is from the mean. The z-score is calculated by $z = \frac{x - \mu}{\sigma}$. The standardization of the normal distribution is helpful to compare the data points among different normal distributions.

**2) Exponential Distribution** is a distribution that explains the waiting time between events in a process that occurs continuously and independently at a constant average rate. The distribution is characterized by one parameter: the rate parameter $\lambda$. The formula of the Exponential Distribution PDF and CDF are given by (CDF is an integral of PDF) [[Practice](#mjx-eqn-AA)]

$$
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
(\text{Mean} = \frac{1}{\lambda} \quad \text{Variance} = \frac{1}{\lambda^2} \quad \text{Standard Deviation} = \frac{1}{\lambda})
$$

The moment of Mean means that if the number of the trials is $\lambda$, the average waiting time between each trial is $\frac{1}{\lambda}$. For instance, if the bus arrives at the bus stop 2 times per hour, the average waiting time for the bus is $\frac{1}{2} = 0.5$ hour. This concept is similar to the Poisson Distribution.

**3) Continuous Uniform Distribution** is a distribution that tells the probability of the continuous random variable whose distribution is uniform. The distribution is characterized by two parameters: the minimum value $a$ and the maximum value $b$. The PDF and CDF of the Continuous Uniform Distribution are given by

$$
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
(\text{Mean} = \frac{a+b}{2} \quad \text{Variance} = \frac{(b-a)^2}{12} \quad \text{Standard Deviation} = \frac{b-a}{\sqrt{12}})
$$

**4) Gamma Distributions**

The gamma distribution is a two-parameter family of continuous probability distributions, particularly useful when dealing with waiting times. The gamma distribution is a generalization of the exponential distribution. In other words, they have same purpose, to predict the wait time until future events, but while the exponential distribution predicts the wait time until the first event, the gamma distribution predicts the wait time until the k-th event.

In order to define the gamma distribution, the gamma function is priorly needed. The gamma function $\Gamma(x)$ is defined with the following five characteristics for any positive real number $\alpha$:

$\text{1. } \Gamma(\alpha) = \int_{0}^{\infty} x^{\alpha-1}e^{-x}dx, \quad \alpha > 0$ \
$\text{2. } \int_{0}^{\infty} x^{\alpha-1}e^{- \lambda x}dx = \frac{\Gamma(\alpha)}{\lambda^{\alpha}}, \quad \alpha > 0, \lambda > 0$ \
$\text{3. } \Gamma(\alpha+1) = \alpha\Gamma(\alpha), \quad \alpha > 0$ \
$\text{4. } \Gamma(n) = (n-1)!, \quad n \in \mathbb{N}$ \
$\text{5. } \Gamma\left(\frac{1}{2}\right) = \sqrt{\pi}$

With these characteristics, the gamma distribution, $X$~Gamma($\alpha$, $\lambda$) followed by a continuous random variable $X$ with parameters $\alpha \gt 0$ and $\lambda \gt 0$, is defined as follows:

$$
f(x) = \begin{cases}
\frac{\lambda^\alpha x^{\alpha-1} e^{-\lambda x}}{\Gamma(\alpha)}, & x > 0 \\
0, & \text{otherwise}
\end{cases}
$$

The specific case, Exponential Distribution, can be checked by setting $\alpha = 1 \rightarrow f(x) = \lambda e^{-\lambda x}$. In other words, Gamma(1, $\lambda$) = Exponential($\lambda$).

The moments of the gamma distribution are as follows:

$\text{1. } E(X) = \frac{\alpha}{\lambda}$ \
$\text{2. } Var(X) = \frac{\alpha}{\lambda^2}$ \
$\text{3. } SD(X) = \sqrt{\frac{\alpha}{\lambda^2}}$

#### F. Joint Distributions

Joint distributions are used to describe the probability of two or more random variables simultaneously. The PMF of joint distribution is defined as $P(x, y) = P(X = x, Y = y) = P((X = x) \text{ and } (Y = y)$.

For two discrete random variables $X$ and $Y$ which the sum of their probabilities is equal to 1, the joint PMF is written as $P(x, y) = P(X = x, Y = y) = P((X = x) \cap P(Y = y))$.

Marginal PMF is the probability of a single random variable without considering the other random variable. The marginal PMF of $X$ is defined as $P(x) = P(X = x) = \sum_{y_i \in R_Y} P(x_i, y_i)$ and the marginal PMF of $Y$ is defined as $P(y) = P(Y = y) = \sum_{x_i \in R_X} P(x_i, y_i)$. In order to $X$ and $Y$ are independent, the independent condition $P(x, y) = P(x)P(y)$ must be satisfied in all $x$ and $y$ cases. For instance, if two discrete random variables $X \in \{1, 2\}$ and $Y \in \{1\}$ are independent, the condition $P(x, y) = P(x)P(y)$ must be satisfied for $x=1, y=1$, and $x=2, y=1$.

**Joint Cumulative Distribution Function** ([Practice](#mjx-eqn-A))

A joint cumulative distribution function is a function of two random variables that gives the probability of them jointly. Aslike the CDF of a single random variable was defined as $F_X(x) = P(X \leq x)$, the joint CDF of two random variables is defined as $F_{XY}(x, y) = P(X \leq x, Y \leq y)$. The common for joint distributions is also applied about comma so that

$$
\begin{aligned}
F_{XY}(x, y) & = P(X \leq x, Y \leq y) \\
& = P(X \leq x \text{ and } Y \leq y) \\
& = P(X \leq x \cap Y \leq y)
\end{aligned}
$$

Marginal CDFs, which are the CDFs of individual random variables obtained from the joint CDFs, are defined as

$$
\begin{aligned}
F_X(x) & = F_{XY}(x, \infty) & = P(X \leq x, Y \leq \infty) & = P(X \leq x) & = \lim_{y \to \infty} F_{XY}(x, y) \text{, for any x} \\
F_Y(y) & = F_{XY}(\infty, y) & = P(X \leq \infty, Y \leq y) & = P(Y \leq y) & = \lim_{x \to \infty} F_{XY}(x, y) \text{, for any y}
\end{aligned}
$$

When it comes to joint CDFs, the following formulas are always true:

$$
\begin{aligned}
F_{XY}(\infty, \infty) & = 1 \\
F_{XY}(-\infty, y) & = 0 \text{ for any y} \\
F_{XY}(x, -\infty) & = 0 \text{ for any x}
\end{aligned}
$$

**Conditioning and Independence of Joint Functions** ([Practice](#mjx-eqn-B))

A formula regarding conditional probability about joint random variables is derived from the basic conditional probability $P(A \mid B) = \frac{P(A \cap B)}{P(B)}$:

$$
P_(X \in A \mid Y \in B) = \frac{P(X \in A, Y \in B)}{P(Y \in B)}, \text{where } C,D \subset R \\
\begin{array}{c|c}
\text{Condtional PMF} & \text{Condtional CDF} \\
\hline
P_{X \mid A}(x_i) = P(X = x_i \mid A) = \frac{P(X = x_i, A)}{P(A)} & F_{X \mid A}(x) = P(X \leq x \mid A) = \frac{P(X \leq x, A)}{P(A)}
\end{array}
$$

Likewise, an independence of joint random variables is derived from the basic independence of events $P(A \cap B) = P(A)P(B)$:

$$
F_{XY}(x, y) = F_X(x)F_Y(y)
$$

Conditional expectation is also similari to ordinary expectation. The only difference is that the expectation is taken with respect to the conditional PMF from the PMF. Specifically,

$$
\begin{aligned}
& E(X \mid A) = \sum_{x_i \in R_X} x_i P_{X \mid A}(x_i) \\
& E(X \mid Y = y_i) = \sum_{x_i \in R_X} x_i P_{X \mid Y}(x_i \mid y_i) \text{ given that the probability of } Y \text{ is observed, the conditional expectation of } X \text{ is calculated}
\end{aligned}
$$

**Law of Total Probability** ([Practice](#mjx-eqn-C))

Recall that the partition is a set of events that are mutually exclusive. The law of total probability is a formula that gives the probability of an event A by summing the probabilities of the event A intersected with the partitioned events. The law is fitted to expectation as well. To be specific,

$$
\begin{aligned}
& P(A) = \sum_{i} P(A \cap B_i) = \sum_{i} P(A \mid B_i)P(B_i) \\
& E(X) = \sum_{i} E(X \mid A_i)P(A_i)
\end{aligned}
$$

**Joint Probability Density Function** ([Practice](#mjx-eqn-D))

When random variables are moved from discrete to continuous, the PMF is replaced by the PDF, and the sum is replaced by the integral. The joint PDF is defined as $f(x, y)$ with the following properties:

- $f(x, y) \geq 0$
- $\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(x, y) \, dx \, dy = 1$
- $P(a \leq X \leq b, c \leq Y \leq d) = \int_{c}^{d} \int_{a}^{b} f(x, y) \, dx \, dy$

**Marginal Probability Density Function** ([Practice](#mjx-eqn-E))

The marginal PDF is obtained from the joint PDF by integrating the joint PDF over the other variable. For example,

$$
\begin{aligned}
f_X(x) & = \int_{-\infty}^{\infty} f(x, y) \, dy \\
f_Y(y) & = \int_{-\infty}^{\infty} f(x, y) \, dx
\end{aligned}
$$

**Joint Cumulative Distribution Function** ([Practice](#mjx-eqn-F))

The joint CDF is defined as $F_{XY}(x, y) = P(X \leq x, Y \leq y)$ with the following 6 properties:

- $F_X(x) = F_{XY}(x, \infty)$ for any $X$
- $F_Y(y) = F_{XY}(\infty, y)$ for any $Y$
- $F_{XY}(\infty, \infty) = 1$
- $F_{XY}(-\infty, y) = F_{XY}(x, -\infty) = 0$ for any $x, y$
- $P( X1 \leq x \leq X2, Y1 \leq y \leq Y2) = F_{XY}(x2, y2) - F_{XY}(x1, y2) - F_{XY}(x2, y1) + F_{XY}(x1, y1)$
- If $X$ and $Y$ are independent, then $F_{XY}(x, y) = F_X(x) \cdot F_Y(y)$

##### G. Conditioning for Continuous Random Variables

Conditional probability for discrete random variables was discussed in the previous section *A*. Similar to other transition from discrete to continuous random variables, the concept of conditional probability for continuous random variables also work with PDFs from PMFs.

**Conditional PDFs and CDFs in Continuous Random Variables** ([Practice](#mjx-eqn-G))

Suppose an event $A$ is defined with a continuous random variable $X$ in the interval $[a,b]$. A conditional PDF and CDF of $X$ and $X$'s conditional expectation and variance are as follows:

$$
\begin{array}{c|c}
\text{Conditional PDF} & \text{Conditional CDF} \\
\hline
f_{X \mid A} (x) = \begin{cases} \frac{f_{X}(x)}{P(A)} & \text{if } a \leq x \leq b \\ 0 & \text{otherwise} \end{cases}
&
F_{X \mid A}(x) = \begin{cases} 0 & \text{if } x < a \\ \int_{a}^{b} f_{X \mid A}(x) dx = \frac{F_X(x) - F_X(a)}{F_X(b) - F_X(a)} & \text{if } a \leq x \leq b \\ 1 & \text{if } x > b \end{cases}
\end{array}
$$

$$
\begin{array}{c|c}
\text{Expectation} & \text{Variance} \\
\hline
E[X \mid A] = \int_{- \infty}^{\infty} x f_{X \mid A} (x) dx & Var(X \mid A) = E[X^2 \mid A] - \left( E[X \mid A] \right)^2 \\
E[g(X) \mid A] = \int_{- \infty}^{\infty} g(x) f_{X \mid A} (x) dx
\end{array}
$$

**Conditioning by Another Random Variable** ([Practice](#mjx-eqn-H))

For two jointly continuous random variables $X$ and $Y$ with their joint PDF $f_{XY}(x,y)$, the conditional PDF and CDF of $X$ given $Y = y$ are as follows:

$$
\begin{array}{c|c}
\text{Conditional PDF} & \text{Conditional CDF} \\
\hline
f_{X \mid Y} (x \mid y) = \frac{f_{XY}(x,y)}{f_Y(y)} & F_{X \mid Y}(x \mid y) = P(X \leq x \mid Y = y) = \int_{-\infty}^{x} f_{X \mid Y}(x \mid y) dx
\end{array}
$$

**Conditional Expectation and Variance in Continuous Random Variables** ([Practice](#mjx-eqn-I))

For two jointly continuous random variables $X$ and $Y$ with their joint PDF $f_{XY}(x,y)$, the conditional expectation and variance of $X$ given $Y = y$ are:

$$
\begin{array}{c|c}
\text{Expectation} & \text{Variance} \\
\hline
E[X \mid Y = y] = \int_{- \infty}^{\infty} x f_{X \mid Y} (x \mid y) dx & Var(X \mid Y = y) = E[X^2 \mid Y = y] - \left( E[X \mid Y = y] \right)^2
\end{array}
$$

**Independent Random Variables in Continuous Random Variables** ([Practice](#mjx-eqn-J))

When two jointly continuous random variables $X$ and $Y$ are independent, the following formulas are true:

$$
f_{X,Y}(x,y) = f_X(x) f_Y(y) \quad \text{for all } x,y \\
E[XY] = E[X]E[Y]
$$

**Involved Functions in Continuous Random Variables** ([Practice](#mjx-eqn-K))

When it comes to the expectation and variance of the function which involves two rando variables $X$ and $Y$, the following formulas are true:

$$
E[g(X,Y)] = \int \int g(x,y) f_{X,Y}(x,y) dx dy \\
Var(g(X,Y)) = E[g(X,Y)^2] - \left( E[g(X,Y)] \right)^2
$$

#### References

$$\tag*{}\label{1} \text{[1] "Probability mass function", Wikipedia, [Online] Available: https://en.wikipedia.org/wiki/Probability_mass_function, accessed in Aug. 28th, 2024.}$$
$$\tag*{}\label{2} \text{[2] "Probability density function", Wikipedia, [Online] Available: https://en.wikipedia.org/wiki/Probability_density_function, accessed in Aug. 28th, 2024.}$$

#### Appendix

#### Practices

$$\tag*{}\label{A} \mathbf{\text{A. Joint Cumulative Distribution Function}}$$

**a. Let $X$~Bernoulli($p$) and $Y$~Bernoulli($q$) are independent. Find joint PMF and joint CDF for $X$ and $Y$.**

Note that $P(X=0) = 1-p, P(X=1) = p, P(Y=0) = 1-q, P(Y=1) = q$.

$$
R_{XY} = \{(0,0), (0,1), (1,0), (1,1)\}, R_X = \{0,1\}, R_Y = \{0,1\} \\
F_{XY}(x, y) = F_X(x) \cdot F_Y(y)
$$

$$
\begin{array}{c|c}
\text{Joint PMF} & \text{Joint CDF} \\
\hline
P_{XY}(x, y) = \begin{cases} (1-p)(1-q) & \text{if } x=0, y=0 \\ (1-p)q & \text{if } x=0, y=1 \\ p(1-q) & \text{if } x=1, y=0 \\ pq & \text{if } x=1, y=1 \\ 0 & \text{otherwise} \end{cases}
&
P_{XY}(x, y) = \begin{cases} 0 & \text{if } x < 0,  y < 0 \\ (1-p)(1-q) & \text{if } 0 \leq x, y \lt 1 \\ (1-p) & \text{if } 0 \leq x \lt 1, y \geq 1 \\ (1-q) & \text{if } x \geq 1, 0 \leq y \lt 1 \\ 1 & \text{if } x \geq 1, y \geq 1 \end{cases}
\end{array}
$$

$$\tag*{}\label{B} \mathbf{\text{B. Conditioning and Independence of Joint Functions}}$$

**a. I roll a fair die. Let $X$ be the observed number. Find the conditional PMF of $X$ given that we know the number was less than 5.**

$$
\begin{array}{cc}
I. & A \to \{1,2,3,4\} \quad P(A) = \frac{4}{6} = \frac{2}{3} \\
II. & P_{X|A}^{(1)} = \frac{P(X=1, X<5)}{P(X<5)} = \frac{\frac{1}{6}}{\frac{2}{3}} = \frac{1}{4} \\
& P_{X|A}^{(2)} = P_{X|A}^{(3)} = P_{X|A}^{(4)} = \frac{1}{4} \\
& P_{X|A}^{(5)} = P_{X|A}^{(6)} = 0
\end{array}
$$

**b. Consider a set of points in the grid shown below. These are points in set $G = \{(x,y) \| x,y \in Z, \|x\| + \|y\| \leq 2\}$. Suppose we pick a point randomly.** (P = $1 \over 13$) \
**b-1. Find the marginal PMF of $X$, $Y$ and their joint PMF.**

$$
\begin{array}{c|c|c}
\text{joint PMF} & \text{marginal PMF of X} & \text{marginal PMF of Y} \\
\hline
P_{XY}(x, y) = \begin{cases} \frac{1}{13} & \text{if } (x,y) \in G \\ 0 & \text{otherwise} \end{cases}
&
P_X(x) = \begin{cases} \frac{1}{13} & \text{for } (-2,0) \\ \frac{3}{13} & \text{for } (-1,-1), (1,0), (-1, 1) \\ \frac{5}{13} & \text{for } (0,-2), (0,-1), (0,0), (0,1), (0,2) \\ \frac{3}{13} & \text{for } (1,-1), (1,0), (1,1) \\ \frac{1}{13} & \text{for } (2,0) \end{cases}
&
P_Y(y) = \begin{cases} \frac{1}{13} & \text{for } (0,-2) \\ \frac{3}{13} & \text{for } (-1,-1), (0,-1), (1,-1) \\ \frac{5}{13} & \text{for } (-2,0), (-1,0), (0,0), (1,0), (2,0) \\ \frac{3}{13} & \text{for } (-1,1), (0,1), (1,1) \\ \frac{1}{13} & \text{for } (0,2) \end{cases}
\end{array}
$$

**b-2. Find the conditional PMF of $X$ given $Y=1$.**

$$
P_{X|Y}(x_i \| Y = 1) = \frac{P(X=x_i, Y=1)}{P(Y=1)} = \frac{P(-1, 1)}{P_Y(1)} = \frac{1/13}{3/13} = \frac{1}{3}
$$

**b-3. Are $X$ and $Y$ independent?**

$\qquad$ No, they are not independent since they are subjected to the constraint $\|x\| + \|y\| \leq 2$

**c. Let X and Y be the same as in b.** \
**c-1. Find $E[X \| Y = 1]$.**

$$
E[X \| Y = 1] = \sum_{x_i} x_i P_{X|Y}(x_i \| Y = 1) = \sum_{x_i} x_i \frac{1}{3} = -1 \cdot \frac{1}{3} + 0 \cdot \frac{1}{3} + 1 \cdot \frac{1}{3} = 0
$$

**c-2. Find $E[X \| -1 \leq Y \leq 2]$.**

$$
E[X \| -1 \leq Y \leq 2] = \sum_{x_i} x_i P_{X|Y}(x_i \| -1 \leq Y \leq 2) = \begin{cases} P(X \| A)(-2) = \frac{P(X = -2, A)}{P(Y = 0) + P(Y = 1)} = \frac{1 \over 13}{8 \over 13} = \frac{1}{8} \\ P(X \| A)(-1) = \frac{P(X = -1, A)}{P(Y = -1) + P(Y = 0) + P(Y = 1)} = \frac{2 \over 13}{8 \over 13} = \frac{1}{4} \\ P(X \| A)(0) = \frac{P(X = 0, A)}{P(Y = -1) + P(Y = 0) + P(Y = 1)} = \frac{2 \over 13}{8 \over 13} = \frac{1}{4} \\ P(X \| A)(1) = \frac{P(X = 1, A)}{P(Y = -1) + P(Y = 0) + P(Y = 1)} = \frac{2 \over 13}{8 \over 13} = \frac{1}{4} \\ P(X \| A)(2) = \frac{P(X = 2, A)}{P(Y = 0) + P(Y = 1)} = \frac{1 \over 13}{8 \over 13} = \frac{1}{8} \end{cases}
$$

**c-3. Find $E[ \|X\| \| -1 \leq Y \leq 2]$.**

$$
E[ \|X\| \| -1 \leq Y \leq 2] = (\|-2\| \cdot \frac{1}{8}) + (\|-1\| \cdot \frac{1}{4}) + (\|0\| \cdot \frac{1}{4}) + (\|1\| \cdot \frac{1}{4}) + (\|2\| \cdot \frac{1}{8}) = 1
$$

$$\tag*{}\label{C} \mathbf{\text{C. Law of Total Probability}}$$

**a. Let $X$~Geometric($p$). Find $E[X]$ by conditioning on the result of the first coin toss.**

$$
\begin{aligned}
& E[X] = E[X \| H]P(H) + E[X \| T]P(T) = 1 \cdot p + (1 + E[X]) \cdot (1-p) = 1 + (1-p)E[X] \\
& \to E[X] = p + (1-p)E[X] + (1-p) \\
& \to E[X] - (1-p)E[X] = p + (1-p) \\
& \to E[X] = \frac{p + (1-p)}{p} = \frac{1}{p}
\end{aligned}
$$

$\qquad$ From a point of view, this is a process of finding the expectation of a geometric random variable.

$$\tag*{}\label{D} \mathbf{\text{D. Joint Probability Density Function}}$$

**a. Let $X$ and $Y$ be two jointly continuous random variables with joint PDF given below.** \

$$
f_{XY}(x, y) = \begin{cases} X + C y^2 & 0 \leq x, y \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

**a-1. Find the value of $C$ that makes $f_{XY}(x, y)$ a valid joint PDF.**

$$
\begin{aligned}
& \int_{0}^{1} \int_{0}^{1} (x + C y^2) \, dx \, dy = 1 \\
& \int_{0}^{1} \left[ \frac{1}{2} x^2 + C y^2 x \right]_{0}^{1} \, dy = 1 \\
& \int_{0}^{1} \left( \frac{1}{2} + C y^2 \right) \, dy = 1 \\
& \left[ \frac{1}{2} y + \frac{C}{3} y^3 \right]_{0}^{1} = 1 \\
& \frac{1}{2} + \frac{C}{3} = 1 \\
& \to C = \frac{3}{2}
\end{aligned}
$$

**a-2. Find $P(0 \leq X \leq 1/2, 0 \leq Y \leq 1/2)$.**

$$
\begin{aligned}
& P(0 \leq X \leq 1/2, 0 \leq Y \leq 1/2) = \int_{0}^{1/2} \int_{0}^{1/2} (x + \frac{3}{2} y^2) \, dx \, dy \\
& = \int_{0}^{1/2} \left[ \frac{1}{2} x^2 + \frac{3}{2} y^2 x \right]_{0}^{1/2} \, dy \\
& = \int_{0}^{1/2} \left( \frac{1}{8} + \frac{3}{4} y^2 \right) \, dy \\
& = \left[ \frac{1}{8} y + \frac{3}{12} y^3 \right]_{0}^{1/2} \\
& = \frac{1}{8} \frac{1}{2} + \frac{3}{12} \left( \frac{1}{2} \right)^3 \\
& = \frac{3}{32}
\end{aligned}
$$

$$\tag*{}\label{E} \mathbf{\text{E. Joint Probability Density Function}}$$

**a. In the previous problem `D.a`, find the marginal PDFs of $X$ and $Y$.**

$$
\begin{aligned}
f_X(x) & = \int_{- \infty}^{\infty} f(x, y) \, dy \\
& = \int_{0}^{1} (x + \frac{3}{2} y^2) \, dy \\
& = \left[ x y + \frac{3}{2} y^3 \right]_{0}^{1} \\
& = x + \frac{1}{2} \\
f_Y(y) & = \int_{- \infty}^{\infty} f(x, y) \, dx \\
& = \int_{0}^{1} (x + \frac{3}{2} y^2) \, dx \\
& = \left[ \frac{1}{2} x^2 + \frac{3}{2} y^2 x \right]_{0}^{1} \\
& = \frac{1}{2} + \frac{3}{2} y^2
\end{aligned}
\\
\begin{array}{cc}
f_X(x) = \begin{cases} x + \frac{1}{2} & 0 \leq x \leq 1 \\ 0 & \text{otherwise} \end{cases} & f_Y(y) = \begin{cases} \frac{1}{2} + \frac{3}{2} y^2 & 0 \leq y \leq 1 \\ 0 & \text{otherwise} \end{cases}
\end{array}
$$

**b. Let $X$ and $Y$ be two random variables with the joint PDF given below.** \

$$
f_{XY}(x, y) = \begin{cases} C x^2 y & 0 \leq x \leq 1, 0 \leq y \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

**b-1. Find $R_{xy}$ and show it in $X$ and $Y$ planes.**

$$
R_{xy} = \{ (x, y) \in \mathbb{R}^2 | 0 \leq y \leq x \leq 1 \}
$$

<details> <summary>summary</summary> y=x 그래프에서 하단 삼각형 영역 그리면 됨 </details>

**b-2. Find constant $C$ that makes $f_{XY}(x, y)$ a valid joint PDF.**

$$
\begin{array}{c|c}
\text{Integrate y first} & \text{Integrate x first} \\
\hline
\begin{aligned}
\int_{0}^{1} \int_{0}^{x} C x^2 y \, dy \, dx & = 1 \\
\int_{0}^{1} \left[ C x^2 \frac{1}{2} y^2 \right]_{0}^{x} \, dx & = 1 \\
\int_{0}^{1} \left( C x^2 \frac{1}{2} x^2 \right) \, dx & = 1 \\
\int_{0}^{1} \left( C \frac{1}{2} x^4 \right) \, dx & = 1 \\
\left[ C \frac{1}{10} x^5 \right]_{0}^{1} & = 1 \\
C \frac{1}{10} & = 1 \\
C & = 10
\end{aligned}
&
\begin{aligned}
\int_{0}^{1} \int_{y}^{1} C x^2 y \, dx \, dy & = 1 \\
\int_{0}^{1} \left[ \frac{1}{3} C x^3 y \right]_{y}^{1} \, dy & = 1 \\
\int_{0}^{1} \left( \frac{1}{3} C y (1 - y^3) \right) \, dy & = 1 \\
\frac{1}{3} C \int_{0}^{1} \left( y - y^4 \right) \, dy & = 1 \\
\frac{1}{3} C \left[ \frac{1}{2} y^2 - \frac{1}{5} y^5 \right]_{0}^{1} & = 1 \\
\frac{1}{3} C \left( \frac{1}{2} - \frac{1}{5} \right) & = 1 \\
C & = 10
\end{aligned}
\end{array}
$$

**b-3. Find Marginal PDFs of $X$ and $Y$.**

$$
\begin{array}{c|c}
\begin{aligned}
f_X(x) & = \int_{0}^{x} 10 x^2 y \, dy \\
& = 10 x^2 \left[ \frac{1}{2} y^2 \right]_{0}^{x} \\
& = 10 x^2 \frac{1}{2} x^2 \\
& = 5 x^4
\end{aligned}
&
\begin{aligned}
f_Y(y) & = \int_{y}^{1} 10 x^2 y \, dx \\
& = 10 y \left[ \frac{1}{3} x^3 \right]_{y}^{1} \\
& = 10 y \left( \frac{1}{3} - \frac{1}{3} y^3 \right) \\
& = 10 y \left( \frac{1}{3} - \frac{1}{3} y^3 \right) \\
& = \frac{10}{3} y - \frac{10}{3} y^4
\end{aligned} \\
\hline
f_X(x) = \begin{cases} 5 x^4 & 0 \leq x \leq 1 \\ 0 & \text{otherwise} \end{cases} & f_Y(y) = \begin{cases} \frac{10}{3} y - \frac{10}{3} y^4 & 0 \leq y \leq 1 \\ 0 & \text{otherwise} \end{cases}
\end{array}
$$

**b-4. Find $P(Y \leq 1/2)$.**

$$
\begin{aligned}
P(Y \leq 1/2) & = \int_{- \infty}^{\infty} \int_{0}^{x/2} f_{xy}(x, y) \, dy \, dx \\
& = \int_{0}^{1} \int_{0}^{x/2} 10 x^2 y \, dy \, dx \\
& = \int_{0}^{1} \left[ 10 x^2 \frac{1}{2} y^2 \right]_{0}^{x/2} \, dx \\
& = \int_{0}^{1} \left( \frac{5}{4} x^4 \right) \, dx \\
& = \left[ \frac{5}{4} \frac{1}{5} x^5 \right]_{0}^{1} \\
& = \frac{1}{4}
\end{aligned}
$$

**b-5. Find $P(Y \leq \frac{X}{4} \mid Y \leq \frac{X}{2})$.**

$$
\begin{aligned}
P(Y \leq X/4 | Y \leq X/2) & = \frac{P(Y \leq X/4, Y \leq X/2)}{P(Y \leq X/2)} \\
& = \frac{\int_{0}^{1} \int_{0}^{x/4} 10 x^2 y \, dy \, dx}{\frac{1}{4}} \\
& = 4 \times P(Y \leq X/4) \\
& = 4 \times \int_{0}^{1} \int_{0}^{x/4} 10 x^2 y \, dy \, dx \\
& = 4 \times \int_{0}^{1} \left[ 10 x^2 \frac{1}{2} y^2 \right]_{0}^{x/4} \, dx \\
& = 4 \times \int_{0}^{1} \left( 10 x^2 \frac{1}{2} \frac{1}{16} x^2 \right) \, dx \\
& = 4 \times \int_{0}^{1} \left( \frac{5}{16} x^4 \right) \, dx \\
& = 4 \times \left[ \frac{5}{16} \frac{1}{5} x^5 \right]_{0}^{1} \\
& = 4 \times \frac{5}{16} \frac{1}{5} \\
& = \frac{1}{4}
\end{aligned}
$$

**c. Let $X$ and $Y$ be two jointly contious random variables with joint PDF given below.** \

$$
f_{xy}(x, y) = \begin{cases} C x + 1 & x,y \leq 0, x + y \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

**c-1. Show the range $R_{xy}$ in $X$ and $Y$ planes.**

<details> <summary>summary</summary> y=-x+1 그래프에서 음수 영역 그리면 됨 </details>

**c-2. Find constant $C$ that makes $f_{xy}(x, y)$ a valid joint PDF.**

$$
\begin{array}{c|c}
\begin{aligned}
\int_{0}^{1} \int_{0}^{1-x} C x + 1 \, dy \, dx & = 1 \\
\int_{0}^{1} \left[ C x y + y \right]_{0}^{1-x} \, dx & = 1 \\
\int_{0}^{1} \left( C x (1-x) + (1-x) \right) \, dx & = 1 \\
\int_{0}^{1} \left( C x - C x^2 + 1 - x \right) \, dx & = 1 \\
\left[ \frac{1}{2} C x^2 - \frac{1}{3} C x^3 + x - \frac{1}{2} x^2 \right]_{0}^{1} & = 1 \\
\frac{1}{2} C - \frac{1}{3} C + 1 - \frac{1}{2} & = 1 \\
C & = 3
\end{aligned}
&
\begin{aligned}
\int_{0}^{1} \int_{0}^{1-y} C x + 1 \, dx \, dy & = 1 \\
\int_{0}^{1} \left[ \frac{C}{2} x^2 + x \right]_{0}^{1-y} \, dy & = 1 \\
\int_{0}^{1} \left( \frac{C}{2} (1-y)^2 + 1 - y \right) \, dy & = 1 \\
\int_{0}^{1} \left( \frac{C}{2} (1 - 2y + y^2) + 1 - y \right) \, dy & = 1 \\
\int_{0}^{1} \left( \frac{C}{2} - C y + \frac{C}{2} y^2 + 1 - y \right) \, dy & = 1 \\
\left[ \frac{C}{2} y - \frac{C}{2} y^2 + \frac{C}{6} y^3 + y - \frac{1}{2} y^2 \right]_{0}^{1} & = 1 \\
\frac{C}{2} - \frac{C}{2} + \frac{C}{6} + 1 - \frac{1}{2} & = 1 \\
C & = 3
\end{aligned}
\end{array}
$$

**c-3. Find Marginal PDFs of $X$ and $Y$.**

$$
\begin{array}{c|c}
\begin{aligned}
f_X(x) & = \int_{0}^{1-x} 3 x + 1 \, dy \\
& = 3 x y + y \, \Big|_{0}^{1-x} \\
& = 3 x (1-x) + (1-x) \\
& = 3 x - 3 x^2 + 1 - x \\
& = 2 x - 3 x^2 + 1
\end{aligned}
&
\begin{aligned}
f_Y(y) & = \int_{0}^{1-y} 3 x + 1 \, dx \\
& = \frac{3}{2} x^2 + x \, \Big|_{0}^{1-y} \\
& = \frac{3}{2} (1-y)^2 + 1-y \\
& = \frac{3}{2} (1 - 2 y + y^2) + 1 - y \\
& = \frac{3}{2} - 3 y + \frac{3}{2} y^2 + 1 - y \\
& = \frac{5}{2} - 4 y + \frac{3}{2} y^2
\end{aligned} \\
\hline
f_X(x) = \begin{cases} - 3 x^2 + 2 x + 1 & 0 \leq x \leq 1 \\ 0 & \text{otherwise} \end{cases} & f_Y(y) = \begin{cases} \frac{3}{2} y^2 - 4 y + \frac{5}{2} & 0 \leq y \leq 1 \\ 0 & \text{otherwise} \end{cases}
\end{array}
$$

$$\tag*{}\label{F} \mathbf{\text{F. Joint Cumulative Distribution Function}}$$

**a. Let $X$ and $Y$ be two independent uniform random variables on $[0,1]$. Find $F_{XY}(x, y)$.**

$$
F_{XY}(x, y) = F_X(x) \cdot F_Y(y) \\
\begin{aligned}
\hline
F_X(x) & = \begin{cases} 0 & x \lt 0 \\ x & 0 \leq x \leq 1 \\ 1 & x \gt 1 \end{cases} \\
F_Y(y) & = \begin{cases} 0 & y \lt 0 \\ y & 0 \leq y \leq 1 \\ 1 & y \gt 1 \end{cases} \\
\hline
F_{XY}(x, y) & = \begin{cases} 0 & x \lt 0, y \lt 0 \\ x \cdot y & 0 \leq x, y \leq 1 \\ x & 0 \leq x \leq 1, y \gt 1 \\ y & x \gt 1, 0 \leq y \leq 1 \\ 1 & x \gt 1, y \gt 1 \end{cases}
\end{aligned}
$$

$$\tag*{}\label{G} \mathbf{\text{G. Conditional PDFs and CDFs in Continuous Random Variables}}$$

**a. Let $X$ ~ Exponential(1). ($\lambda e^{-\lambda x} = e^{-x}$)** \
**a-1. Find Conditional PDF of $X$ given $X > 1$.**

$$
\begin{array}{c|c}
f_{X \mid A} (x) = \frac{f_X(x)}{P(A)}
&
\begin{aligned}
& P(A) = \int_{1}^{\infty} e^{-x} dx = \left. -e^{-x} \right|_{1}^{\infty} = e^{-1} \\
& \to f_{X \mid A} (x) = \frac{e^{-x}}{e^{-1}} = e^{-x+1}
\end{aligned}
\end{array}
$$

**a-2. Find $E[X \mid X > 1]$.**

$$
\begin{array}{c|c}
\int_{- \infty}^{\infty} x f_{X \mid A} (x) dx
&
\begin{aligned}
E[X \mid X > 1] & = \int_{1}^{\infty} x e^{-x+1} dx = e \int_{1}^{\infty} x e^{-x} dx \\
& = e \left| -x e^{-x} + e^{-x} \right|_{1}^{\infty} \\
& = 2
\end{aligned} \\
\hline
\end{array} \\
\int f(x)g(x) dx = f(x)G(x) - \int f'(x)G(x) dx + C
$$

**a-3. Find $Var(X \mid X > 1)$ = $E[X^2 \mid X > 1] - \left( E[X \mid X > 1] \right)^2$**

$$
\begin{aligned}
\int_{1}^{\infty} x^2 e^{-x+1} dx & = e \int_{1}^{\infty} x^2 e^{-x} dx \\
& = e \left| x^2 (-e^{-x}) - \int 2x (-e^{-x}) dx \right|_{1}^{\infty} \\
& \left( \begin{aligned}
& \int 2x (-e^{-x}) dx = 2x e^{-x} - 2 \int e^{-x} dx \\
& \int e^{-x} dx = \left| -e^{-x} \right|_{1}^{\infty} \\
\end{aligned} \right) \\
& = e \left| x^2 (-e^{-x}) - 2x e^{-x} - 2e^{-x} \right|_{1}^{\infty} \\
& = 5 \\
Var(X \mid X > 1) & = 5 - 2^2 = 1
\end{aligned}
$$

$$\tag*{}\label{H} \mathbf{\text{H. Conditioning by Another Random Variable}}$$

**a. Let $X$ and $Y$ be two jointly continuous random variables with the joint PDF given below.** \

$$
f_{XY}(x,y) = \begin{cases} \frac{x^2}{4} + \frac{y^2}{4} + \frac{xy}{6} & 0 \leq x \leq 1, 0 \leq y \leq 2 \\ 0 & \text{otherwise} \end{cases}
$$

**a-1. Find conditional PDF of $X$ given $Y=y$.**

$$
\begin{array}{c|c}
f_{X \mid Y} (x \mid y) = \frac{f_{XY}(x,y)}{f_Y(y)}
&
\begin{aligned}
f_Y(y) & = \int_{0}^{1} f_{XY}(x,y) dx \\
& = \int_{0}^{1} \left( \frac{x^2}{4} + \frac{y^2}{4} + \frac{xy}{6} \right) dx \\
& = \left. \frac{x^3}{12} + \frac{y^2}{4}x + \frac{xy}{6} \right|_{0}^{1} \\
& = \frac{1}{12} + \frac{y^2}{4} + \frac{y}{6} \\
& = \frac{3y^2 + y + 1}{12}
\end{aligned} \\
\hline
\end{array} \\
\begin{aligned}
& f_Y(y) = \begin{cases} \frac{3y^2 + y + 1}{12} & 0 \leq y \leq 2 \\ 0 & \text{otherwise} \end{cases} \\
\to & f_{X \mid Y} (x \mid y) = \frac{\frac{x^2}{4} + \frac{y^2}{4} + \frac{xy}{6}}{\frac{3y^2 + y + 1}{12}}
\end{aligned}
$$

**a-2. Find $P(X \lt \frac{1}{2} \mid Y = y)$.**

$$
\begin{aligned}
P(X \lt \frac{1}{2} \mid Y = y) & = \int_{0}^{\frac{1}{2}} f_{X \mid Y} (x \mid y) dx \\
& = \int_{0}^{\frac{1}{2}} \frac{\frac{x^2}{4} + \frac{y^2}{4} + \frac{xy}{6}}{\frac{3y^2 + y + 1}{12}} dx \\
& = \frac{1}{3y^2 + y + 1} \int_{0}^{\frac{1}{2}} \frac{x^2}{4} + \frac{y^2}{4} + \frac{xy}{6} dx \\
& = \frac{1}{3y^2 + y + 1} \left. x^3 + 3y^2 x + x^2 y \right|_{0}^{\frac{1}{2}} \\
& = \frac{1}{3y^2 + y + 1} \left( \frac{1}{8} + \frac{3y^2}{2} + \frac{y}{4} \right) \\
& = \frac{\frac{3}{2} y^2 + \frac{y}{4} + \frac{1}{8}}{3y^2 + y + 1}
\end{aligned}
$$

$$\tag*{}\label{I} \mathbf{\text{I. Conditional Expectaion and Variance in Continuous Random Variables}}$$

**a. Let $X$ and $Y$ be the same as the previous problem H.a.** \
**a-1. Find $E[X \mid Y = 1]$ and $Var(X \mid Y = 1)$.**

$$
\begin{array}{c|c}
\begin{aligned}
E[X \mid Y = 1] & = \int_{0}^{1} x f_{X \mid Y} (x \mid 1) dx \\
& = \int_{0}^{1} x \left| \frac{3x^2 + 3y^2 + 2xy}{3y^2 + y + 1} \right|^{y=1} dx \\
& = \int_{0}^{1} x \left( \frac{3x^2 + 3 + 2x}{5} \right) dx \\
& = \frac{1}{5} \left| \frac{3}{4} x^4 + \frac{3}{2} x^2 + \frac{2}{3} x^3 \right|_{0}^{1} \\
& = \frac{1}{5} \times \frac{9 + 18 + 8}{12} \\
& = \frac{7}{12}
\end{aligned}
&
\begin{aligned}
Var(X \mid Y = 1) & = E[X^2 \mid Y = 1] - \left( E[X \mid Y = 1] \right)^2 \\
\\
\qquad \text{i. } E[X^2 \mid Y = 1] & = \int_{0}^{1} x^2 \left( \frac{3x^2 + 3 + 2x}{5} \right) dx \\
& = \frac{21}{50} \\
\qquad \text{ii. } Var(X \mid Y = 1) & = \frac{21}{50} - \left( \frac{7}{12} \right)^2 \\
& = \frac{287}{3600}
\end{aligned}
\end{array}
$$

$$\tag*{}\label{J} \mathbf{\text{J. Independent Random Variables}}$$

**a. Determine if $X$ and $Y$ are independent if their joint PDF is given below.**

$$
f_{XY}(x,y) = \begin{cases} 8xy & 0 \leq x \leq y \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

**a-1. Find $f_X(x)$ and $f_Y(y)$.**

$$
\begin{array}{c|c}
\begin{aligned}
f_X(x) & = \int_{x}^{1} 8xy dy \\
& = 4x - 4x^3
\end{aligned}
&
\begin{aligned}
f_Y(y) & = \int_{0}^{y} 8xy dx \\
& = 4y^3
\end{aligned} \\
\hline
f_X(x) = \begin{cases} 4x - 4x^3 & 0 \leq x \leq 1 \\ 0 & \text{otherwise} \end{cases}
&
f_Y(y) = \begin{cases} 4y^3 & 0 \leq y \leq 1 \\ 0 & \text{otherwise} \end{cases}
\end{array}
$$

**a-2. Is it independent?**

$$
8xy \neq (4x - 4x^3)(4y^3) \quad \text{for all } x,y
$$

$\qquad$ No, they are not independent.

$$\tag*{}\label{K} \mathbf{\text{K. Independent Random Variables}}$$

**a. Let $X$ and $Y$ be two jointly continuous random variables with the joint PDF given below.** \

$$
f_{XY}(x,y) = \begin{cases} x + y & 0 \leq x, y \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

**a-1. Find $E[XY^2]$.**

$$
\begin{aligned}
E[XY^2] & = \int_{- \infty}^{\infty} \int_{- \infty}^{\infty} x y^2 f_{XY}(x,y) dx dy \\
& = \int_{0}^{1} \int_{0}^{1} x y^2 (x + y) dx dy \\
& = \int_{0}^{1} \int_{0}^{1} x^2 y^2 + xy^3 dx dy \\
& = \int_{0}^{1} \left| \frac{x^3 y^2}{3} + \frac{x^2 y^3}{3} \right|_{0}^{1} dy \\
& = \int_{0}^{1} \frac{y^2}{3} + \frac{y^3}{2} dy \\
& = \left| \frac{y^3}{9} + \frac{y^4}{8} \right|_{0}^{1} \\
& = \frac{17}{72}
\end{aligned}
$$
