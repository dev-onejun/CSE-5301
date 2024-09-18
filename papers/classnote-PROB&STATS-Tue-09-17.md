**Joint Cumulative Distribution Function**

~

Marginal CDFs

$$
$$

$$
F_{XY}(\infty, \infty) = 1
F_{XY}(-\infty, y) = 0 \text{for any y}
F_{XY}(x, -\infty) = 0 \text{for any x)
$$

Examples

LEt X~Bernouli(p) and Y~Bernouli(q) are independent. Find joint PMF and joint CDF for x and y

R_XY = {(0,0), (0,1), (1,0), (1,1)}, R_X = {0,1}, R_Y = {0,1}

P_XY(x,y) = P_X(x)P_Y(y)

P_XY(0,0) = P_X(0)P_Y(0) = (1-p)(1-q)
P_XY(0,1) = P_X(0)P_Y(1) = (1-p)q
P_XY(1,0) = P_X(1)P_Y(0) = p(1-q)
P_XY(1,1) = P_X(1)P_Y(1) = pq

F_XY(x,y) = F_X(X) * F_Y(y)

F_XY(x,y) = 1 (x > 1, y>1)
F_XY(x,y) = 0 (x < 0 or y<0) x = 0, y>1)
F_XY(x,y) = (1-p) * 1 (y=0, x>=1)
F_XY(x,y) = (1-q) * 1 (x=0, y=0)?

in the 2 dimensional coordinate,
1사분면을 제외하면 모두 0. x=1,y=1을 기점으로 각 확률을 가짐. (위에 x,y 범위 틀렸을 가능성 높음)

**Conditioning and Independence**

Example

I roll a fair die. Let X be the observed number. Find the conditinoal PMF of X given that we know the number was less than 5.

A $\to$ {1,2,3,4} P(A) = 4/6 = 2/3

$P_{X|A}^{(1)} = \frac{P(X=1, X<5)}{P(X<5)} = \frac{1/6} / \frac{2/3} = 1/4$
$P_{X|A}^{(2)} = P_{X|A}^{(3)} = P_{X|A}^{(4)} = 1/4$
$P_{X|A}^{(5)} = P_{X|A}^{(6)} = 0$

**Conditional CDF**

**Independent Random Variables**

Example

Consider set of points in the grid shown below. These are points in set G = {(x,y) | x,y \in Z, |x|+|y| \leq 2}. Suppose we pick a point randomly. (P = 1/13)

a) Find marginal PMF of X, Y and their joint PMF

$$
P_{XY}(x,y) = \begin{cases} \frac{1}{13} & \text{if } (x,y) \in G \\ 0 & \text{otherwise} \end{cases} \\
\\
P_X(x) = \begin{cases} \frac{1}{13} & \text{for (-2,0)} \\ \frac{3}{13} & \text{for (-1,-1), (=1,0), (-1, 1)} \\ \frac{5}{13} & \text{for (0,-2), (0,-1), (0,0), (0,1), (0,2)} \end{cases} \\ \frac{3}{13} & \text{for (1,-1), (1,0), (1,1)} \\ \frac{1}{13} & \text{for (2,0)} \end{cases} \\
P_Y(y) = \begin{cases} \frac{1}{13} & \text{for (0,-2)} \\ \frac{3}{13} & \text{for (-1,-1), (0,-1), (1,-1)} \\ \frac{5}{13} & \text{for (-2,0), (-1,0), (0,0), (1,0), (2,0)} \end{cases} \\ \frac{3}{13} & \text{for (-1,1), (0,1), (1,1)} \\ \frac{1}{13} & \text{for (0,2)} \end{cases}
$$

b) Find conditional PMF of X given Y=1

$$
P_{X|Y}(x_i} = \frac{P(X=X_i, Y=1)}{P(Y=1)} = \frac{P(-1, 1)}{P_Y(1)} = \frac{1/13}{3/13} = 1/3
$$

c) Are X and Y independent?

No. since they are subjected to the constraint $|x|+|y| \leq 2$

**Conditional Expectation**

Example

Let X and Y be the same as in the previous example.

a) Find $E[X|Y=1]$

$$
E[X|Y=1] = \sum_{x_i} x_i P_{X_i|Y=1} = -1 * 1/3 + 0 * 1/3 + 1 * 1/3 = 0
$$

b) Find $E[X| -1 \leq Y \leq 2]$

$$
E[X| -1 \leq Y \leq 2] = \sum_{x_i} x_i P_{X_i| -1 \leq Y \leq 2} = \\
\\
P_{X|A}(-2) = \frac{P(X=-2, A)}{P(Y=0) + P(Y=1)} = \frac{1 \over 13}{8 \over 13} = {1 \over 8} \\
P_{X|A}(-1) = \frac{P(X=-1, A)}{P(Y=-1) + P(Y=0) + P(Y=1)} = \frac{2 \over 13}{8 \over 13} = {1 \over 4} \\
P_{X|A}(0) = \frac{P(X=0, A)}{P(Y=-1) + P(Y=0) + P(Y=1)} = \frac{2 \over 13}{8 \over 13} = {1 \over 4} \\
P_{X|A}(1) = \frac{P(X=1, A)}{P(Y=-1) + P(Y=0) + P(Y=1)} = \frac{2 \over 13}{8 \over 13} = {1 \over 4} \\
P_{X|A}(2) = \frac{P(X=2, A)}{P(Y=0) + P(Y=1)} = \frac{1 \over 13}{8 \over 13} = {1 \over 8} \\
\\
E[X | -1 \leq Y \leq 2] = -2 * 1/8 + -1 * 1/4 + 0 * 1/4 + 1 * 1/4 + 2 * 1/8 = 0
$$

c) Find E[ |X| | -1 \leq Y \leq 2]

$$
E[|X| | -1 \leq Y \leq 2 ] = (|-2| \times \frac{1}{8}) + (|-1| \times \frac{1}{4}) + (|0| \times \frac{1}{4}) + (|1| \times \frac{1}{4}) + (|2| \times \frac{1}{8}) = 1
$$

**Law of Total Probability**

If A_1, A_2, ... is a partition of the sample space S, then for any event B.

$$
P(B) = \sum_{i} P(A \cap B_i) = \sum_{i} P(A_i)P(B|A_i)
$$

Remember that the partition is a set of events that are mutually exclusive.

Example

Let X~Geometric(P). Find E[X] by conditioning on the result of the first coin toss.

$$
E[X] = E[X|H] \times P(H) + E[X|T] \times P(T) = 1 \times P + (1 + E[X]) \times (1-P) \\
E[X] = P + (1 - P) \cdot E[X] + (1 - P) \\
E[x] - (1-P)E[X] = P + 1 - P = 1 \\
E[X] = \frac{1}{P}
$$
식정리 한거네?
