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

The language that Probability uses is *Set theory*. The following elements are example of the *Set theory* language.

$$
\begin{array}{|c|}
\hline
\text{Universal set } \mathbf{S} = \{H, T\} \text{, when it comes to flipping a coin once} \\
\text{Integer set } \mathbf{Z} \text{ | 1 } \in Z, {1 \over 2} \notin Z \\
\hline
\text{When sets are disjoint && } A_1 \cup A_2 \cup \cdots \cup A_n = A, \text{the sets is called as }\mathbf{\text{Partitions of a set}} \\
\text{If two or more sets do not have common elements (the intersections are empty), they are called }\mathbf{\text{Mutually exclusive sets}} \\
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
