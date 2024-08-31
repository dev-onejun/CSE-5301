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

**Basic Definition of Probability**

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

*Cardinality* $|A|$ means the size of the set. If the set $A$ has its elements $\{2,4,6,8,10\}$, the value $|A| = 5$.

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
*PDF* is used to specify the probability of the *continuous random variables* falling within a particular range of values. This probability is given by the integral of these variables over the range. In other words, the area under the density function but above the horizontal axis and between the lowest and the greatest variable values is the probability of the random variable.

![img](https://upload.wikimedia.org/wikipedia/commons/4/4f/4_continuous_probability_density_functions.png)
$\text{Fig 2. An Example of Four Continuous PDF functions [} \href{#mjx-eqn-2}{2} \text{]}$

*CDF* is a function, used in *continuous* random variables, which maps the probability of the event that the random variable is less than or equal to a certain values. The function is defined as $F(x) = P(X \le x)$.

With the definition of *random experiments* and *random variables*, three *axioms of probability* can be defined as follows: **1)** For any event $A$, $P(A) \ge 0$. **2)** The probability of the sample space $P(S)$ is always $1$. **3)** For disjoint events greater than or equal to 2, the probability of the union of these events is equal to the sum of the probabilities of these events. $P(A_1 \cup A_2 \cup \cdots) = P(A_1) + P(A_2) + \cdots$

*Conditional Probability* refers to the probability which has been considered after certain observations or facts. For instance, in poker cards, if a selected card were a black, then what is the probability of the card being a spade? The probability of the card being a spade is the *Conditional Probability*, and the answer is $P(\text{Spade}|\text{Black}) = \frac{13}{26} = \frac{1}{2}$. The formula for *Conditional Probability* is given by

$$
P(A|B) = \frac{P(A \cap B)}{P(B)} \\
\cdot \mathbf{\text{The Chain Rule: }} P(A \cap B) = P(A|B)P(B) = P(B|A)P(A)
$$

Two events $A$ and $B$ are independent if $P(A \cap B) = P(A)P(B)$. In other words, the occurrence of one event does not affect the probability of the other event. From the formula of *Conditional Probability*, if $A$ and $B$ are independent, then $P(A|B) = P(A)$ and $P(B|A) = P(B)$.

*Joint Probability* represents the probability of two events occurring simultaneously. Take the poker cards again as an example. The probability of selecting a black card and a spade card is $P(\text{Black} \cap \text{Spade}) = P(\text{Black}) \times P(\text{Spade}) = \frac{13}{52} = \frac{1}{4}$.

*Marginalization* is the process of obtaining the probability of a event by summing over all the possible values of the other event. For instance, the probability of selecting a black card is $P(\text{Black}) = P(\text{Black} \cap \text{Spade}) + P(\text{Black} \cap \text{Club}) = \frac{13}{52} + \frac{13}{52} = \frac{26}{52} = \frac{1}{2}$.

**Bayes Theorem**

*Bayes Theorem*, alternatively known as *Bayes'rule* or *Bayes' law*, is a formula that describes how to derive the probability of a hypothesis given the evidence. The formula is driven from the definition of *Conditional Probability*. The formula is given by

$$
P(A|B) = \frac{P(B|A)P(A)}{P(B)}
$$


#### References

[1] "Probability mass function", Wikipedia, [Online] Available: https://en.wikipedia.org/wiki/Probability_mass_function, accessed in Aug. 28th, 2024. \
[2] "Probability density function", Wikipedia, [Online] Available: https://en.wikipedia.org/wiki/Probability_density_function, accessed in Aug. 28th, 2024.


