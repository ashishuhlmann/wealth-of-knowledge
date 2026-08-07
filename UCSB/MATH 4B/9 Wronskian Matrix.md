## 2/2/26

The **Wronskian Matrix** is a matrix formed by placing $n$ functions and their subsequent derivatives into a square matrix.
$$
\begin{bmatrix}
f_{1}(t) & f_{2}(t) & ... & f_{n}(t) \\
\frac{df_{1}(t)}{dt} & \frac{df_{2}(t)}{dt} & ... & \frac{df_{n}(t)}{dt} \\
\frac{d^{2}f_{1}(t)}{dt^{2}} & \frac{d^{2}f_{2}(t)}{dt^{2}} & ... & \frac{d^{2}f_{n}(t)}{dt^{2}} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{d^{n-1}f_{1}(t)}{dt^{n-1}} & \frac{d^{n-1}f_{2}(t)}{dt^{n-1}} & ... & \frac{d^{n-1}f_{n}(t)}{dt^{n-1}} \\
\end{bmatrix}
$$If the Wrońskian is **indentically zero**, the functions are linearly dependent. If the Wrońskian is non-zero at any point in an interval, the functions are linearly independent.
$$
W(f_{1},f_{2},...f_{n})=
\begin{vmatrix}
f_{1}(t) & f_{2}(t) & ... & f_{n}(t) \\
\frac{df_{1}(t)}{dt} & \frac{df_{2}(t)}{dt} & ... & \frac{df_{n}(t)}{dt} \\
\frac{d^{2}f_{1}(t)}{dt^{2}} & \frac{d^{2}f_{2}(t)}{dt^{2}} & ... & \frac{d^{2}f_{n}(t)}{dt^{2}} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{d^{n-1}f_{1}(t)}{dt^{n-1}} & \frac{d^{n-1}f_{2}(t)}{dt^{n-1}} & ... & \frac{d^{n-1}f_{n}(t)}{dt^{n-1}} \\
\end{vmatrix}
$$
In two functions, the Wrońskian is
$$
W[y_{1},y_{2}]=
\begin{vmatrix}
y_{1}(0) & y_{2}(0) \\
y_{1}'(0) & y_{2}'(0) \\
\end{vmatrix}
=y_{1}(0)y_{2}'(0)-y_{2}(0)y_{1}'(0)
$$
### Example

Let $\alpha$ and $\beta$ be constants such that $\beta\neq0$.
$$
\begin{align}
f_{1}(t)=e^{\alpha t}\cos{(\beta t)} \\
f_{2}(t)=e^{\alpha t}\sin{(\beta t)} \\
\end{align}
$$
$$
\begin{align}
f_{1}'(t)=e^{\alpha t}(\alpha\cos{(\beta t)}-\beta\sin{(\beta t)}) \\
f_{2}'(t)=e^{\alpha t}(\alpha\sin{(\beta t)}+\beta\cos{(\beta t)}) \\
\end{align}
$$
$$
\begin{bmatrix}
y_{1}(0) & y_{2}(0) \\
y_{1}'(0) & y_{2}'(0) \\
\end{bmatrix}
=
\begin{bmatrix}
1 & 0 \\
\alpha & \beta \\
\end{bmatrix}
$$
- This matrix is of full rank, so the functions are linearly independent.
## [[10 Application of the Wronskian]]