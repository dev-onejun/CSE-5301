$$
\begin{array}{|c|c|}
\hline
\text{} & \text{} \\
\hline
\text{} & \text{} \\
\hline
\end{array}
$$

**Joint Continuous Random Variables**

- **Joint Probability Density Function (pdf)**
  - $f(x, y)$
  - $f(x, y) \geq 0$
  - $\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(x, y) \, dx \, dy = 1$
  - $P(a \leq X \leq b, c \leq Y \leq d) = \int_{c}^{d} \int_{a}^{b} f(x, y) \, dx \, dy$

  Practice
    - Let X and Y be two jointly continuous random variables with joint PDF given below

    $$
    f_{xy}(x, y) = \begin{cases} X + C y^2 & 0 \leq x, y \leq 1 \\ 0 & \text{otherwise} \end{cases}
    $$

        a) Find the value of C that makes $f_{xy}(x, y)$ a valid joint PDF.

$$
\begin{aligned}
\int_{0}^{1} \int_{0}^{1} (x + C y^2) \, dx \, dy & = 1 \\
\int_{0}^{1} \left[ \frac{1}{2} x^2 + C y^2 x \right]_{0}^{1} \, dy & = 1 \\
\int_{0}^{1} \left( \frac{1}{2} + C y^2 \right) \, dy & = 1 \\
\left[ \frac{1}{2} y + \frac{C}{3} y^3 \right]_{0}^{1} & = 1 \\
\frac{1}{2} + \frac{C}{3} & = 1 \\
--recalculate \\
\frac{1}{2} + \frac{C}{3} & = 1 \\
\frac{3}{6} + \frac{2}{6} & = 1 \\
\frac{5}{6} & = 1 \\
--recarculate \\
C & = \frac{3}{2}
\end{aligned}
$$

        b) Find P(0 <= X <= 1/2, 0 <= Y <= 1/2)

$$
\begin{aligned}
P(0 \leq X \leq 1/2, 0 \leq Y \leq 1/2) & = \int_{0}^{1/2} \int_{0}^{1/2} (x + \frac{3}{2} y^2) \, dx \, dy \\
& = \int_{0}^{1/2} \left[ \frac{1}{2} x^2 + \frac{3}{2} y^2 x \right]_{0}^{1/2} \, dy \\
--recalculate \\
& = \int_{0}^{1/2} \left( \frac{1}{8} + \frac{3}{8} y^2 \right) \, dy \\
& = \left[ \frac{1}{8} y + \frac{3}{24} y^3 \right]_{0}^{1/2} \\
& = \frac{1}{16} + \frac{3}{24} \left( \frac{1}{2} \right)^3 \\
& = \frac{1}{16} + \frac{3}{24} \left( \frac{1}{8} \right) \\
& = \frac{1}{16} + \frac{3}{192} \\
& = \frac{1}{16} + \frac{1}{64} \\
& = \frac{4}{64} + \frac{1}{64} \\
--recalculate \\
& = \frac{3}{32}
\end{aligned}
$$


- **Marginal Probability Density Function**
  - $f_X(x) = \int_{-\infty}^{\infty} f(x, y) \, dy$
  - $f_Y(y) = \int_{-\infty}^{\infty} f(x, y) \, dx$

  Practice
    - In previous example, find the marginal PDFs of X and Y.

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

    - Let X and Y be two jointly continuous random variables with joint PDF given below

$$
f_{xy}(x, y) = \begin{cases} C x^2 y & 0 \leq y \leq x \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

        a) Find $R_{xy}$ and show it in X and Y planes.

$$
R_{xy} = \{ (x, y) \in \mathbb{R}^2 | 0 \leq y \leq x \leq 1 \}
$$
<!-- y=x 그래프에서 하단 삼각형 영역 그리면 됨-->

        b) Find constant C that makes $f_{xy}(x, y)$ a valid joint PDF.

$$
\begin{array}{c|c}
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
--recalculate \\
\int_{0}^{1} \left[ C \frac{1}{3} x^3 y \right]_{y}^{1} \, dy & = 1 \\
\int_{0}^{1} \left( C \frac{1}{3} - C \frac{1}{3} y^3 \right) \, dy & = 1 \\
\int_{0}^{1} \left( C \frac{1}{3} - C \frac{1}{3} y^3 \right) \, dy & = 1 \\
\left[ C \frac{1}{3} y - C \frac{1}{12} y^4 \right]_{0}^{1} & = 1 \\
C \frac{1}{3} - C \frac{1}{12} & = 1 \\
--recalculate \\
C & = 10
\end{aligned}
\end{array}
$$
<!-- integral range를 0~x 해도 되고, y를 바깥에 dy할경우 y to 1 해도 됨-->

        c) Find Marginal PDFs of X and Y.

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

        d) Find P(Y <= 1/2)

$$
\begin{aligned}
P(Y \leq 1/2) & = \int_{- \infty}^{\infty} \int_{0}^{x/2} f_{xy}(x, y) \, dy \, dx \\
& = \int_{0}^{1} \int_{0}^{x/2} 10 x^2 y \, dy \, dx \\
& = \int_{0}^{1} \left[ 10 x^2 \frac{1}{2} y^2 \right]_{0}^{x/2} \, dx \\
--recalculate \\
& = \int_{0}^{1} \left( 10 x^2 \frac{1}{2} \frac{1}{4} x^2 \right) \, dx \\
& = \int_{0}^{1} \left( \frac{5}{2} x^4 \right) \, dx \\
& = \left[ \frac{5}{2} \frac{1}{5} x^5 \right]_{0}^{1} \\
& = \frac{5}{2} \frac{1}{5} \\
--recalculate \\
& = \frac{1}{4}
\end{aligned}
$$

        e) Find P(Y <= X/4 | Y <= X/2)

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
<!-- 검산 필요 -->

    - Let X and Y be two jointly continuous random variables with joint PDF given below

$$
f_{xy}(x, y) = \begin{cases} C x + 1 & x,y \leq 0, x + y \leq 1 \\ 0 & \text{otherwise} \end{cases}
$$

        a) Show the range $R_{xy}$ in X and Y planes.

$$
R_{xy} = \{ (x, y) \in \mathbb{R}^2 | x, y \leq 0, x + y \leq 1 \}
$$
<!-- y=-x+1 그래프에서 0-1 x구간 아래 삼각형 영역 그리면 됨-->

        b) Find constant C that makes $f_{xy}(x, y)$ a valid joint PDF.

$$
\begin{array}{c|c}
\begin{aligned}
\int_{0}^{1} \int_{0}^{1-x} C x + 1 \, dy \, dx & = 1 \\
\int_{0}^{1} \left[ C x y + y \right]_{0}^{1-x} \, dx & = 1 \\
--recalculate \\
\int_{0}^{1} \left( C x (1-x) + 1 - 0 \right) \, dx & = 1 \\
\int_{0}^{1} \left( C x - C x^2 + 1 \right) \, dx & = 1 \\
\left[ \frac{C}{2} x^2 - \frac{C}{3} x^3 + x \right]_{0}^{1} & = 1 \\
\frac{C}{2} - \frac{C}{3} + 1 & = 1 \\
\frac{C}{2} - \frac{C}{3} & = 0 \\
\frac{3C}{6} - \frac{2C}{6} & = 0 \\
--recalculate \\
1 = \frac{C}{6} + \frac{1}{2} \\
C & = 3
\end{aligned}
&
\begin{aligned}
\int_{0}^{1} \int_{0}^{1-x} C x + 1 \, dx \, dy & = 1 \\
--recalculate \\
\int_{0}^{1} \left[ C x^2 + x \right]_{0}^{1-x} \, dy & = 1 \\
\int_{0}^{1} \left( C (1-x)^2 + 1 - 0 \right) \, dy & = 1 \\
\int_{0}^{1} \left( C (1-2x+x^2) + 1 \right) \, dy & = 1 \\
\int_{0}^{1} \left( C - 2C x + C x^2 + 1 \right) \, dy & = 1 \\
\left[ C y - 2C x y + C x^2 y + y \right]_{0}^{1-x} & = 1 \\
C (1-x) - 2C x (1-x) + C x^2 (1-x) + 1-x & = 1 \\
C - C x - 2C x + 2C x^2 + C x^2 - C x^3 + 1 - x & = 1 \\
C - 3C x + 3C x^2 - C x^3 & = 0 \\
C - 3C x + 3C x^2 - C x^3 & = 0 \\
C (1 - 3x + 3x^2 - x^3) & = 0 \\
C (1 - x)^3 & = 0 \\
C & = 0
--recalculate \\
\end{aligned}
\end{array}
$$

        c) Find Marginal PDF of X and Y

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

* **Joint Cumulative Distribution Function (CDF)**
  - $F(x, y) = P(X \leq x, Y \leq y)$
  - Properties
    - $\text{1. } F_X(x) = F(x, \infty) \text{, for any x}$
    - $\text{2. } F_Y(y) = F(\infty, y) \text{, for any y}$
    - $\text{3. } F_{XY}(\infty, \infty) = 1$
    - $\text{4. } F_{XY}(-\infty, y) = F_{XY}(x, -\infty) = 0$
    - $\text{5. } P( X1 \leq X \leq X2, Y1 \leq Y \leq Y2) = F_{XY}(x2, y2) - F_{XY}(x1, y2) - F_{XY}(x2, y1) + F_{XY}(x1, y1)$
    - $\text{6. If } X \text{ and } Y \text{ are independent, then } F_{XY}(x, y) = F_X(x) \cdot F_Y(y)$

    Practice

    - Let X and Y be two indepedent uniform (0,1) continuous random variables. Find $F_{XY}(x, y)$.

$$
F_{XY}(x, y) = F_X(x) \cdot F_Y(y) \\
\\
F_X(x) = \begin{cases} 0 & x \lt 0 \\ x & 0 \leq x \leq 1 \\ 1 & x \gt 1 \end{cases} & F_Y(y) = \begin{cases} 0 & y \lt 0 \\ y & 0 \leq y \leq 1 \\ 1 & y \gt 1 \end{cases} \\
\\
F_{XY}(x, y) = \begin{cases} 0 & x \lt 0 \text{ or } y \lt 0 \\ x \cdot y & 0 \leq x, y \leq 1 \\ x & 0 \leq x \leq 1, y \gt 1 \\ y & 0 \leq y \leq 1, x \gt 1 \\ 1 & x \gt 1 \text{ and } y \gt 1 \end{cases}
$$
<!-- 수식 안나옴-->




















### References

$\tag*{}\label{n} \text{[n] }$
