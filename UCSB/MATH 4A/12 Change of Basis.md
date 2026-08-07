## 12/2/25

Let
$$
\vec{u_{1}}=
\begin{bmatrix}
1 \\
-1 \\
0 \\
\end{bmatrix}
,\vec{u_{2}}=
\begin{bmatrix}
1 \\
0 \\
-1 \\
\end{bmatrix}
$$
$\vec{v_{1}}$ and $\vec{v_{2}}$ are linearly independent since they are not scalar multiples of each other.
$$
\begin{align}
V=\text{span}\{\vec{u_{1}},\vec{u_{2}}\} \\
\beta=\{\vec{u_{1}},\vec{u_{2}}\} \\
\end{align}
$$
Now consider
$$
\vec{v_{1}}=
\begin{bmatrix}
2 \\
-1 \\
-1 \\
\end{bmatrix}
,\vec{v_{2}}=
\begin{bmatrix}
0 \\
-1 \\
1 \\
\end{bmatrix}
$$
$$
\begin{align}
\vec{v_{1}}=\vec{u_{1}}+\vec{u_{2}} \\
\vec{v_{2}}=\vec{u_{1}}-\vec{u_{2}} \\
\end{align}
$$
$$
\begin{align}
\vec{v_{1}},\vec{v_{2}}\in V \\
\gamma=\{\vec{v_{1}},\vec{v_{2}}\} \\
\end{align}
$$
Now let $\vec{x}\in V$ such that 
$$
[\vec{x}]_{\beta}=
\begin{bmatrix}
5 \\
3 \\
\end{bmatrix}
=5\vec{u_{1}}+3\vec{u_{2}}
$$
What is $[\vec{x}]_{\gamma}$?

Multiply $[\vec{x}]_{\beta}$ by the **change of basis matrix**.

1. Write $\vec{u_{1}}$ and $\vec{u_{2}}$ in terms of $\vec{v_{1}}$ and $\vec{v_{2}}$.
$$
\begin{align}
\vec{u_{1}}=\frac{1}{2}\vec{v_{1}}+\frac{1}{2}\vec{v_{2}} \\
\vec{u_{2}}=\frac{1}{2}\vec{v_{1}}+\frac{1}{2}\vec{v_{2}} \\
\end{align}
$$
$$
\begin{align}
[\vec{u_{1}}]_{\gamma}= 
\begin{bmatrix}
\frac{1}{2} \\
-\frac{1}{2} \\
\end{bmatrix} \\
[\vec{u_{2}}]_{\gamma}= 
\begin{bmatrix}
\frac{1}{2} \\
\frac{1}{2} \\
\end{bmatrix} \\
\end{align}
$$
The change of basis matrix is
$$
P_{\beta}^{\gamma}=
\begin{bmatrix}
[\vec{u_{1}}]_{\gamma} & [\vec{u_{2}}]_{\gamma} \\
\end{bmatrix}
=
\begin{bmatrix}
\frac{1}{2} & \frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} \\
\end{bmatrix}
$$
$$
[\vec{x}]_{\gamma}=
\begin{bmatrix}
\frac{1}{2} & \frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} \\
\end{bmatrix}
\begin{bmatrix}
5 \\
3 \\
\end{bmatrix}
=
\begin{bmatrix}
4 \\
-1 \\
\end{bmatrix}
$$
## [[13 Eigenvectors and Eigenvalues]]