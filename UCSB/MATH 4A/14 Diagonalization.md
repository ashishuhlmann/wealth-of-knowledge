If a $n\times n$ matrix has $n$ linearly independent eigenvectors, it is **diagnolizable**.
$$
A=Q^{-1}DQ
$$
- $D$ is the matrix of eigenvalues going down the diagonal.
- $Q$ is the matrix of column eigenvectors.
## The Jordan Block

Some matricies are not diagnolizable. In the two by two case, we have one eigenvalue and define the **Jordan block**
$$
J=
\begin{bmatrix}
\lambda & 1 \\
0 & \lambda
\end{bmatrix}
$$
such that $A=P^{-1}JP$. The first column of $\textbf{p}_{1}$ is the eigenvector. The second column satisfies the equation
$$
(\hat{A}-\lambda\hat{I})\textbf{p}_{2}=\textbf{p}_{1}
$$

This is all usefull because 
$$
A^{k}=QD^{k}Q^{-1}
$$
or
$$
A^{k}=PJ^{k}P^{-1}
$$
and especially useful because
$$
\exp(A)=Q\exp(D)Q^{-1}
$$
where the exponential of a diagonal matrix is
$$
\exp{(
\begin{bmatrix}
\lambda_{1} & 0 & ... & 0 \\
0 & \lambda_{2} & ... & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & ... & \lambda_{n} \\
\end{bmatrix}
t)}=
\begin{bmatrix}
e^{\lambda_{1}t} & 0 & ... & 0 \\
0 & e^{\lambda_{2}t} & ... & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & ... & e^{\lambda_{n}t} \\
\end{bmatrix}
$$
or 
$$
\exp(A)=P\exp(J)P^{-1}
$$
where the exponential of a two by two **Jordan block** is
$$
\exp{(
\begin{bmatrix}
\lambda & 1 \\
0 & \lambda \\
\end{bmatrix}
t)}=
\begin{bmatrix}
e^{\lambda t} & te^{\lambda t} \\
0 & e^{\lambda t} \\
\end{bmatrix}
$$
## [[1 Differential Equations]]