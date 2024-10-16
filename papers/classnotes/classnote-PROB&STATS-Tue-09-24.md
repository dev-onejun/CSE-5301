$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

**Conditioning for Continuous Random Variables**

**Conditional CDF**

(여기 서술 뭔가 틀린듯)
Suppose a continuous random variable $X$ has a PDF $F_X(x)$ and the event X = [a,b] has occurred. The conditional CDF of $X$ given the event X = [a,b] is defined as

$$
F_{X|X \in [a,b]}(x) = \begin{cases} 0
\frac{}{}
$$

**Conditional PDF**

$$
f_{X \mid A} (X) = \begin{cases} \frac{f_{X}(x)}{P(A)} & \text{if } a \leq x \leq b \\ 0 & \text{otherwise} \end{cases}
$$

Practices

Let X ~ Exponential(1). $\lambda e^{-\lambda x} = e^{-x}$.
    - a) Find Conditional PDF of X given X > 1.

$$
f_{X \mid A} (X) = \frac{f_X(x)}{P(A)} \\
\\
P(A) = = \int_{1}^{\infty} e^{-x} dx = \left. -e^{-x} \right|_{1}^{\infty} = e^{-1}
\to f_{X \mid A} (X) = \frac{e^{-x}}{e^{-1}} = e^{-x+1}
$$

    - b) Find E[X | X > 1]
$$
\text{From} \int_{- \infty}^{\infty} x f_{X \mid A} (x) dx
E[X \mid X > 1] = \int_{1}^{\infty} x e^{-x+1} dx = e \int_{1}^{\infty} x e^{-x} dx = ... = 2
$$

    - c) Find Var(X | X > 1) ( = E[X^2 | X > 1] - E[X | X > 1]^2)
$$
e \int_{1}^{\infty} x^2 e^{-x} dx = e \left| -2 e^{-x} -2 x e^{-x} - x^2 e^{-x} \right|_{1}^{\infty} = ...
$$

**Conditioning by another random variable**

Practices

Let X and Y be two jointly continous random variables with the joint PDF given below.

$$
f_{XY}(x,y) = \begin{cases} \frac{x^2}{4} + \frac{y^2}{4} + \frac{xy}{6} & 0 \leq x \leq 1, 0 \leq y \leq 2 \\ 0 & \text{otherwise} \end{cases}
$$

a) Find conditional PDF of X given Y=y.

$$
f_{X \mid Y} (x \mid y) = \frac{f_{XY}(x,y)}{f_Y(y)} \\
f_Y(y) = \int_{0}^{1} \left( \frac{x^2}{4} + \frac{y^2}{4} + \frac{xy}{6} \right) dx = \frac{x^3}{12} + \frac{y^2}{4} + \frac{xy}{6} \right|_{0}^{1} = \frac{1}{12} + \frac{y^2}{4} + \frac{y}{6} = \frac{3y^2 + y + 1}{12} \\
\to f_Y(y) = \begin{cases} \frac{3y^2 + y + 1}{12} & 0 \leq y \leq 2 \\ 0 & \text{otherwise} \end{cases} \\
\to f_{X \mid Y} (x \mid y) = \frac{\frac{x^2}{4} + \frac{y^2}{4} + \frac{xy}{6}}{\frac{3y^2 + y + 1}{12}} = \frac{3x^2 + 3y^2 + 2xy}{3y^2 + y + 1}
$$

b) Find $P(X \lt \frac{1}{2} \mid Y = y)$

$$
\int_{0}^{\frac{1}{2}} f_{X \mid Y} (x \mid y) dx = \int_{0}^{\frac{1}{2}} \frac{3x^2 + 3y^2 + 2xy}{3y^2 + y + 1} dx = \frac{1}{3y^2 + y + 1} \int_{0}^{\frac{1}{2}} 3x^2 + 3y^2 + 2xy dx \\
= \frac{1}{3y^2 + y + 1} \left| x^3 + 3y^2 x + x^2 y \right|_{0}^{\frac{1}{2}} = \frac{1}{3y^2 + y + 1} (\frac{1}{8} + \frac{3y^2}{2} + \frac{y}{4}) = \frac{\frac{3}{2} y^2 + \frac{y}{4} + \frac{1}{8}}{3y^2 + y + 1}
$$

**Conditional Expectation and Variance**

Practices

Let X and Y be the same as previious example. Find E[X | Y = 1] and Var(X | Y = 1).

$$
E[X \mid Y = 1] = \int_{0}^{1} x f_{X \mid Y} (x \mid 1) dx = \int_{0}^{1} x \frac{3x^2 + 3y^2 + 2xy}{3y^2 + y + 1} \right|_{y=1} dx = \int{0}^{1} x \frac{3x^2 + 3 + 2x}{5} dx = \frac{1}{5} \int_{0}^{1} 3x^3 + 3x + 2x^2 dx = \frac{1}{5} \left| \frac{3}{4} x^4 + \frac{3}{2} x^2 + \frac{2}{3} x^3 \right|_{0}^{1} = \frac{1}{5} \times \frac{9 + 18 + 8}{12} = \frac{35}{60} = \frac{7}{12} \\
$$

$$
\begin{aligned}
Var(X \mid Y = 1) & = E[X^2 \mid Y = 1] - E[X \mid Y = 1]^2 \\
& \text{I. } E[X^2 \mid Y = 1] = \int_{0}^{1} x^2 \frac{3x^2 + 3 + 2x}{5} dx = \frac{1}{5} \int_{0}^{1} 3x^4 + 3x^2 + 2x^3 dx = \frac{21}{50} \\
& \text{II. } Var(X | Y = 1) = \frac{21}{5} - \frac{7}{12}^2 = \frac{287}{3600}
\end{aligned}
$$

**Independent Random Variables**

Practices

Determine if X and Y are independent if their joint PDF is given below.

$$
f_{XY}(x,y) = \begin{cases} 8xy & 0 \leq x \leq y \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

$$
\text{Find } f_X(x) \text{ and } f_Y(y) \\
f_X(x) = \int_{x}^{1} 8xy dy = 4x - 4x^3 \\
\to f_X(x) = \begin{cases} 4x - 4x^3 & 0 \leq x \leq 1 \\ 0 & \text{otherwise} \end{cases} \\
f_Y(y) = \int_{0}^{y} 8xy dx = 4y^3 \\
\to f_Y(y) = \begin{cases} 4y^3 & 0 \leq y \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

$$
\text{is it independent?} \\
f_{XY}(x,y) = f_X(x) \times f_Y(y) ? \\
8xy = (4x - 4x^3) \times 4y^3 ?
$$
No. Not independent.

**Functions of two continuous random variables**

$$
E[g(X,Y)] = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x,y) f_{XY}(x,y) dx dy
$$

Practices

1. Let X and Y be two jointly continuous random variables with the joint PDF given below.

$$
f_{XY}(x,y) = \begin{cases} x + y & 0 \leq x, y \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

a) Find $E[XY^2]$

$$
E[XY^2] = \int_{- \infty}^{\infty} \int_{- \infty}^{\infty} x y^2 f_{XY}(x,y) dx dy = \int_{0}^{1} \int_{0}^{1} x y^2 (x + y) dx dy = \int_{0}^{1} \int_{0}^{1} x^2 y^2 + xy^3 dx dy \\
\int_{0}^{1} \left| \frac{x^3 y^2}{3} + \frac{x^2 y^3}{3} \right|_{0}^{1} dy = \int_{0}^{1} \frac{y^2}{3} + \frac{y^3}{2} dy = \left| \frac{y^3}{9} + \frac{y^4}{8} \right|_{0}^{1} = \frac{1}{9} + \frac{1}{8} = \frac{17}{72}
$$




### References

$\tag*{}\label{n} \text{[n] }$

### Practices
