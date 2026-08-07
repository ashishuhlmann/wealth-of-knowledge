## 2/4/26

Consider the second order linear homogenous equation on the interval $I\subset\mathbb{R}$.
$$
y''+p(t)y'+q(t)y=0
$$
**Theorem:** existence and uniqueness for second order
Suppose $p(t)$ and $q(t)$ are both continuous on an open inteval $I\subset\mathbb{R}$. Then for every $t_{0}\in I$ and constants $a$, $b$, the IVP 
$$
y''+p(t)y'+q(t)y=0
$$
with $y(t_{0})=a$ and $y'(t_{0})=b$ has a unique solution on $I$.
- All solutions are parametrized by $a$ and $b$, meaning all solutions are linear combinations of two linearly independent functions.
- The solution space of $y$ and $y'$ is isomorphic to $\mathbb{R}^{2}$.
- If the two solutions $y_{1}$ and $y_{2}$ are linearly independent, all solutions are a linear combination of the two functions.
- The Wrońskian is either *identically zero or never zero* on $I$, so it is sufficient to check at any one point.
## Abel's Formula

For the following differential equation, the Wrońskian of the two solutions $y_{1}$ and $y_{2}$ is either *identically zero or never zero*.
$$
y''+p(t)y'+q(t)y=0
$$
We can calculate that
$$
\frac{dW[y_{1},y_{2}]}{dt}=
\begin{vmatrix}
y_{1}' & y_{2}' \\
y_{1}' & y_{2}' \\
\end{vmatrix}
+
\begin{vmatrix}
y_{1} & y_{2} \\
y_{1}'' & y_{2}'' \\
\end{vmatrix}
=-p(t)W[y_{1},y_{2}]
$$
This shows that the Wrońskian is the solution to the linear first order homogenous equation
$$
u'+p(t)u=0
$$
That means that
$$
W[y_{1},y_{2}]=Ce^{-\int p(t)dt}
$$
This equation is either *identically zero or never zero*.
### Example Problem
$\text{Solve}$
$$
y''-6y'+5y=0
$$
$\text{where}$
$$
\begin{align}
y(0)=2 \\
y'(0)=-1
\end{align}
$$
$$
\lambda^{2}-6\lambda+5=0
$$
$$
\begin{align}
\lambda=5 \\
\lambda=1 \\
\end{align}
$$
$$
\begin{align}
2=c_{2} +c_{2} \\
-1=5c_{1}+c_{2}\\
\end{align}
$$
$$
\begin{bmatrix}
1 & 1 \\
5 & 1 \\
\end{bmatrix}
\begin{bmatrix}
c_{1} \\
c_{2} \\
\end{bmatrix}
=
\begin{bmatrix}
2\\
-1 \\
\end{bmatrix}
$$
$$
\begin{bmatrix}
c_{1} \\
c_{2} \\
\end{bmatrix}
=
\begin{bmatrix}
\frac{1}{-4} & \frac{5}{4} \\
\frac{1}{4} & \frac{1}{-4} \\
\end{bmatrix}
\begin{bmatrix}
2\\
-1 \\
\end{bmatrix}
$$
## [[11 Reduction of Order]]
