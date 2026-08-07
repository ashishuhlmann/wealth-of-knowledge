## 3/30/26

**vector field** - special vector-valued function on $\mathbb{R}^{n}$ or a subset $U\subseteq\mathbb{R}^{n}$
- a vector field maps $\mathbb{R}^{n}$ to $\mathbb{R}^{n}$
- a vector field on $U$ is maps $U$ to $\mathbb{R}^{n}$

**flow line** - a differentiable curve $\textbf{c}(t)$ in a vector field $\textbf{F}$ such that $\textbf{F}(\textbf{c}(t))=\textbf{c}'(t)$ 
### Example

To find the flow lines for
$$
\textbf{F}(
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
)=
\begin{bmatrix}
-y \\
x \\
\end{bmatrix}
$$
- This happens to be a linear transformation.
We need to solve the system of differential equations
$$
\begin{bmatrix}
x'(t) \\
y'(t) \\
\end{bmatrix}
=
\begin{bmatrix}
0 & -1 \\
1 & 0 \\
\end{bmatrix}
\begin{bmatrix}
x(t) \\
y(t) \\
\end{bmatrix}
$$
to get
$$
\textbf{c}(t)=
\begin{bmatrix}
c_{1}\cos{(t)}+c_{2}\sin{(t)} \\
c_{1}\sin{(t)}-c_{2}\cos{(t)} \\
\end{bmatrix}
$$
**gradient vector field** - vector field given by the gradient of a function
- points in the direction of steepest increase
- normal to any level set
## [[2 Path Integrals]]