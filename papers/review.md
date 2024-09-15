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

#### I. Introduction

#### II. Literature Review

##### A. Basic Definition of Probability

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

*Cardinality* $| A |$ means the size of the set. If the set $A$ has its elements $\{2,4,6,8,10\}$, the value $| A | = 5$.

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
P(A) \in [0, 1] \\
P(\text{true}) = 1, P(\text{false}) = 0 \\
P(A \cup B) = P(A) + P(B) - P(A \cap B) \\
P(A \cap B) = P(A) \cdot P(B|A) \\
P(A) + P(\neg A) = 1
$$

*Multivalued* random variables are the *random variables* that can take more than two values. For example, the result of a dice roll is a *multivalued* random variable. The probability of the event that the result of the dice roll is 4 is $P(A) = {1 \over 6}$. The axioms of *multivalued* random variables are as follows.

$$
P(A = a_i) \in [0, 1] \\
P(S) = 1, P(\emptyset) = 0 \\
P(A \cup B) = P(A) + P(B) - P(A \cap B) \\
P(A \cap B) = P(A) \cdot P(B|A) \\
\sum_{i=1}^{n} P(A = a_i) = 1
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

*Conditional Probability* refers to the probability which has been considered after certain observations or facts. For instance, in poker cards, if a selected card were a black, then what is the probability of the card being a spade? The probability of the card being a spade is the *Conditional Probability*, and the answer is $P(\text{Spade} | \text{Black}) = \frac{13}{26} = \frac{1}{2}$. The formula for *Conditional Probability* is given by

$$
P(A|B) = \frac{P(A \cap B)}{P(B)} \\
\cdot \mathbf{\text{The Chain Rule: }} P(A \cap B) = P(A|B)P(B) = P(B|A)P(A)
$$

Two events $A$ and $B$ are independent if $P(A \cap B) = P(A)P(B)$. In other words, the occurrence of one event does not affect the probability of the other event. From the formula of *Conditional Probability*, if $A$ and $B$ are independent, then $P(A|B) = P(A)$ and $P(B|A) = P(B)$.

*Joint Probability* represents the probability of two events occurring simultaneously. Take the poker cards again as an example. The probability of selecting a black card and a spade card is $P(\text{Black} \cap \text{Spade}) = P(\text{Black}) \times P(\text{Spade}) = \frac{13}{52} = \frac{1}{4}$.

*Marginalization* is the process of obtaining the probability of a event by summing over all the possible values of the other event. For instance, the probability of selecting a black card is $P(\text{Black}) = P(\text{Black} \cap \text{Spade}) + P(\text{Black} \cap \text{Club}) = \frac{13}{52} + \frac{13}{52} = \frac{26}{52} = \frac{1}{2}$.

##### B. Bayes Theorem

*Bayes Theorem*, alternatively known as *Bayes'rule* or *Bayes' law*, is a formula that describes how to derive the probability of a hypothesis given the evidence. The formula is driven from the definition of *Conditional Probability* and given by

$$
P(A|B) = \frac{P(B|A)P(A)}{P(B)}
$$

##### C. Probability Distributions

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

##### D. Discrete Probability Distributions

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

**4) Hypergeometric Distribution** is a distribution that describes the number of successes in a sequence of $n$ draws without replacement from a finite population of size $N$ that contains $K$ successes. The distribution is characterized by three parameters: the population size $N$, the number of available successes in the population $K$, the number of draws $n$, and the number of observed (curious) success $k$. The formula of the PMF of the Hypergeometric Distribution is given by

$$
\begin{array}{c|ccc}
& \text{Mean} & = & \frac{nK}{N} \\
P(X = k) = \frac{{K \choose k} {N-K \choose n-k}}{{N \choose n}} & \text{Variance} & = & n \frac{K}{N} \frac{N-K}{N} \frac{N-n}{N-1} \\
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

##### E. Continuous Probability Distributions

Four continuous probability distributions are addressed in this review: **1)** **Normal(Gaussian) Distribution**, **2)** **Exponential Distribution**, **3)** **Continuous Uniform Distribution**, and **4)** **Gamma Distribution**.

**1) Normal(Gaussian) Distribution** is a distribution that describes the probability of the continuous random variable whose distribution is symmetric and bell-shaped. The distribution is characterized by two parameters: the mean $\mu$ and the standard deviation $\sigma$. The formula of the Normal Distribution PDF is given by

$$
f(x) = \frac{1}{\sqrt{2\pi}\sigma} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

68% of the data falls within one standard deviation of the mean, 95% of the data falls within two standard deviations of the mean, and 99.7% of the data falls within three standard deviations of the mean.

The standard normal distribution, also known as Bell Curve, is a special case of the normal distribution when the mean $\mu = 0$ and the standard deviation $\sigma = 1$. The PDF of the standard normal distribution is always $f(x) = \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}}$. The standard normal distribution is also used to calculate the z-score, which is the number of standard deviations a data point is from the mean. The z-score is calculated by $z = \frac{x - \mu}{\sigma}$. The standardization of the normal distribution is helpful to compare the data points among different normal distributions.

**2) Exponential Distribution** is a distribution that explains the waiting time between events in a process that occurs continuously and independently at a constant average rate. The distribution is characterized by one parameter: the rate parameter $\lambda$. The formula of the Exponential Distribution PDF and CDF are given by (CDF is an integral of PDF)

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
$\text{2. } \int_{0}^{\infty} x^{\alpha-1}e^{\lambda x}dx = \frac{\Gamma(\alpha)}{\lambda^{\alpha}}, \quad \alpha > 0, \lambda > 0$ \
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

##### F. Joint Distributions

Joint distributions are used to describe the probability of two or more random variables simultaneously. The PMF of joint distribution is defined as $P(x, y) = P(X = x, Y = y) = P((X = x) \text{ and } (Y = y)$.

For two discrete random variables $X$ and $Y$ which the sum of their probabilities is equal to 1, the joint PMF is written as $P(x, y) = P(X = x, Y = y) = P((X = x) \cap P(Y = y))$.

Marginal PMF is the probability of a single random variable without considering the other random variable. The marginal PMF of $X$ is defined as $P(x) = P(X = x) = \sum_{y_i \in R_Y} P(x_i, y_i)$ and the marginal PMF of $Y$ is defined as $P(y) = P(Y = y) = \sum_{x_i \in R_X} P(x_i, y_i)$. In order to $X$ and $Y$ are independent, the independent condition $P(x, y) = P(x)P(y)$ must be satisfied in all $x$ and $y$ cases. For instance, if two discrete random variables $X \in \{1, 2\}$ and $Y \in \{1\}$ are independent, the condition $P(x, y) = P(x)P(y)$ must be satisfied for $x=1, y=1$, and $x=2, y=1$.

#### References

$$\tag*{}\label{1} \text{[1] "Probability mass function", Wikipedia, [Online] Available: https://en.wikipedia.org/wiki/Probability_mass_function, accessed in Aug. 28th, 2024.}$$
$$\tag*{}\label{2} \text{[2] "Probability density function", Wikipedia, [Online] Available: https://en.wikipedia.org/wiki/Probability_density_function, accessed in Aug. 28th, 2024.}$$

#### Appendix

##### Practices


