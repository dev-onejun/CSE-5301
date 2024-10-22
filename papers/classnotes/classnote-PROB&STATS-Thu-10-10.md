$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

* Communication Theory (not included in the exam regarding this part)

$$
\text{Transmission} \leftrightarrow{\text{Channel}} \text{Reception}
$$

    - transmission: source of possible messages

    - The uncertainty of the receiver is closely related to the possible messages.
        ex1. Let's say source can only send 1 possible message, and the probability that receiver receives the message is 100%.
            $I = - \log_2 1 = 0$ (no uncertainty)
        ex2. Source can send 2 possible messages, and the probability that receiver receives the message is 0.5
            $I = - \log_2 0.5 = 1 \text{bit}$
        ex3. Source can only send 10 possible messages, and the probability that receiver receives the message is 0.1
            $I = - \log_2 0.1 = 3.3 \text{bits}$

    - Practice
    1. we have alphabets (26 letters) and a space as a symbol (27 symbols in total), and 27 cards.

    a. What is the amount of information for 1 letter?

    $$
    I = - \log_2 \frac{1}{27} = 4.76 \text{bits}
    $$

    2. With the previous setup, we want the number of bits of information for 3 letters?

    $$
    I = 3 \cdot 4.76 = 14.28 \text{bits}
    $$

    since the letters are independent, we can multiply the number of bits of information for each letter.

    3. Let's say the probability of each symbol is already given as space=0.2, E=0.105, T=0.072, etc. -> 9,679개의 카드가 필요하다고 하자. How to calculate the amount of information for 1 letter?

    by computing the average of the information for each symbol.

    $$
    = - \left( P_\text{space} \log_2 P_\text{space} + P_\text{E} \log_2 P_\text{E} + \cdots \right) = 3.9 \text{bits per letter}
    $$

    4. Let's say we want to calculate the number of bits of information for 3 letters in the setup at problem 3. and we want those letters to be 'X', 'F', 'O' in any order

    $$
    = - \left( P_\text{X} \log_2 P_\text{X} + P_\text{F} \log_2 P_\text{F} + P_\text{O} \log_2 P_\text{O} \right) = 2.23 \text{bits}
    $$

    5. the number of bits of informatino for 3 letters but we want them to be 'c', 'A', 'T' in this order

    $$
    = - \left( P_\text{c} \log_2 P_\text{c} + P_\text{A} \log_2 P_\text{A} + P_\text{T} \log_2 P_\text{T} \right) = 0.67 \text{bits}
    $$




### Practices

1. The probability of being male is 0.5 and 20% of males are tall (> 6 ft) and 6% of females are tall.
a. What is the P that if somebody is tall, the person is a male.

Given,
$$
P(T \mid M) = 0.2 \\
P(T \mid F) = 0.06 \\
$$

$$
P(M \mid T) = \frac{P (T \mid M) \cdot P(M)}{P(T)} \\
\quad P(T) = P(T \mid M) \cdot P(M) + P(T \mid F) \cdot P(F) \\
= \frac{0.2 \cdot 0.5}{0.13} = 0.769
$$

b. if you know somebody is male, how much information you gain by learning that he is also tall.

$$
P(T \mid M) = 0.2 \text{is given} \\
I = - \log_2 P(T \mid M) = - \log_2 0.2 = 2.32 ?
$$

c. How much information you gain by learning that a female is tall.

$$
P(T \mid F) = 0.06 \text{is given} \\
I = - \log_2 P(T \mid F) = - \log_2 0.06 = 4.06 \text{bits}
$$

d. how much information from learning that a tall person is female

$$
P(F \mid T) = \frac{P(T \mid F) \cdot P(F)}{P(T)} \\
= \frac{0.06 \cdot 0.5}{0.13} = 0.231 \\
I = - \log_2 P(F \mid T) = - \log_2 0.231 = 2.116 \text{bits}
$$

2. The input source to a noisy communication channel is random variable $X$ over 4 symbols (a, b, c, d). The output is a random variable $Y$ over 4 symbols (a, b, c, d).
The joint distribution of $X$ and $Y$, $P(X, Y)$ is given in the table below.

$$
\begin{array}{|c|c|c|c|c|}
\hline
\text{} & \text{a} & \text{b} & \text{c} & \text{d} \\
\hline
\text{Y=a} & \frac{1}{8} & \frac{1}{16} & \frac{1}{16} & \frac{1}{4} \\
\hline
\text{Y=b} & \frac{1}{16} & \frac{1}{8} & \frac{1}{16} & 0 \\
\hline
\text{Y=c} & \frac{1}{32} & \frac{1}{32} & \frac{1}{16} & 0 \\
\hline
\text{Y=d} & \frac{1}{32} & \frac{1}{32} & \frac{1}{16} & 0 \\
\hline
\end{array}
$$

a. Find H(X) and H(Y)

$$
P(X) = \begin{cases} \frac{1}{4} & \text{if } X = a \\ \frac{1}{4} & \text{if } X = b \\ \frac{1}{4} & \text{if } X = c \\ \frac{1}{4} & \text{if } X = d \\ 0 & \text{otherwise} \end{cases} \\
P(Y) = \begin{cases} \frac{1}{2} & \text{if } Y = a \\ \frac{1}{4} & \text{if } Y = b \\ \frac{1}{8} & \text{if } Y = c \\ \frac{1}{8} & \text{if } Y = d \\ 0 & \text{otherwise} \end{cases} \\
\\
H(X) = - \left( 4 (\frac{1}{4} \log_2 \frac{1}{4}) \right) = 2 \text{bits} \\
H(Y) = - \left( \frac{1}{2} \log_2 \frac{1}{2} + \frac{1}{4} \log_2 \frac{1}{4} + 2 \cdot \frac{1}{8} \log_2 \frac{1}{8} \right) = 1.75 \text{bits}
$$

b. Find $D(X \mid\mid Y)$

$$
D(X \mid\mid Y) = \sum P(X) \log_2 \frac{P(X)}{P(Y)} \\
= \frac{1}{4} \log_2 \frac{1/4}{1/2} + \frac{1}{4} \log_2 \frac{1/4}{1/4} + \frac{1}{4} \log_2 \frac{1/4}{1/8} + \frac{1}{4} \log_2 \frac{1/4}{1/8} \\
= 0.25 \text{bits}
$$

c. Find the joint entropy $H(X, Y)$

$$
H(X, Y) = - \sum\sum P(X, Y) \log_2 P(X, Y) \\
= - \left( 2 \cdot \frac{1}{8} \log_2 \frac{1}{8} + 6 \cdot \frac{1}{16} \log_2 \frac{1}{16} + 4 \cdot \frac{1}{32} \log_2 \frac{1}{32} + \frac{1}{4} \log_2 \frac{1}{4} \right) \\
= 3.375 \text{bits}
$$

d. Find $H(X \mid Y)$ and $H(Y \mid X)$

$$
H(X \mid Y) = H(X, Y) - H(Y) = 3.375 - 1.75 = 1.625 \text{bits} \\
H(Y \mid X) = H(X, Y) - H(X) = 3.375 - 2 = 1.375 \text{bits}
$$

e. Find $I(X, Y)$

$$
I(X, Y) = H(X) - H(X \mid Y) = 2 - 1.625 = 0.375 \text{bits} \\
= H(Y) - H(Y \mid X) = 1.75 - 1.375 = 0.375 \text{bits} \\
= H(X) + H(Y) - H(X, Y) = 2 + 1.75 - 3.375 = 0.375 \text{bits}
$$

3. The joint distribution of $X$ and $Y$ is given in the table below.

$$
\begin{array}{|c|c|c|}
\hline
\text{} & \text{X=0} & \text{X=1} \\
\hline
\text{Y=0} & \frac{1}{3} & \frac{1}{3} \\
\hline
\text{Y=1} & 0 & \frac{1}{3} \\
\hline
\end{array}
$$

a. Find $H(X)$ and $H(Y)$

$$
H(X) = - \left( \frac{2}{3} \log_2 \frac{2}{3} + \frac{1}{3} \log_2 \frac{1}{3} \right) = 0.918 \text{bits} \\
H(Y) = - \left( \frac{1}{3} \log_2 \frac{1}{3} + \frac{2}{3} \log_2 \frac{2}{3} \right) = 0.918 \text{bits}
$$

b. Find $H(X, Y)$

$$
H(X, Y) = - \left( 3 \cdot \frac{1}{3} \log_2 \frac{1}{3} \right) = 1.585 \text{bits}
$$

c. Find $H(X \mid Y)$

$$
H(X \mid Y) = H(X, Y) - H(Y) = 1.585 - 0.918 = 0.667 \text{bits}
$$

d. Find $I(X, Y)$

$$
I(X, Y) = H(X) - H(X \mid Y) = 0.918 - 0.667 = 0.251 \text{bits}
$$







































### References

$\tag*{}\label{n} \text{[n] }$
