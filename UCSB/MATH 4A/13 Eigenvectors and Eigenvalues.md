## 12/2/25
## Definition

Let $A$ be an $n\times n$ matrix. A non-zero vector $\vec{x}\in\mathbb{R}^{n}$ is called an **eigenvector** of $A$ if $A\vec{x}=\lambda\vec{x}$ for some scalar $\lambda$ called the **eigenvalue**.
- In this case, $\lambda$ is the eigenvalue of $A$ corresponding to the eigenvector $\vec{x}$.
### Example

Let
$$
A=
\begin{bmatrix}
1 & 1 \\
1 & 1 \\
\end{bmatrix}
,\vec{u}=
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
$$
$$
A\vec{u}=
\begin{bmatrix}
1 & 1 \\
1 & 1 \\
\end{bmatrix}
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
=
\begin{bmatrix}
2 \\
2 \\
\end{bmatrix}
=2\vec{u}
$$
- $\vec{u}$ is an eigenvector of $A$ and $\lambda=2$ is the corresponding eigenvalue.
## Computation
$$
\begin{align}
A\vec{x}&=\lambda\vec{x} \\
A\vec{x}-\lambda\vec{x}&=\vec{0} \\
(A-\lambda I_n)\vec{x}&=\vec{0} \\
\end{align}
$$
- This homogeneous system has non-trivial solutions.
- $(A-\lambda I_n)$ must be non-invertible, which means the determinant is zero.
$$
\text{det}(A-\lambda I_n)=0
$$
- With this characteristic polynomial, solve for $\lambda$.

In general, the characteristic polynomial for any two by two matrix can be written as
$$
\lambda^{2}-\text{trace}(A)\lambda+\text{det}(A)
$$
Eigenvectors of $A$ are in the nullspace of $A-\lambda I_{n}$. The nullspace of $A-\lambda I_{n}$ is called the **eigenspace** of $A$ corresponding to $\lambda$. It is a subspace of $\mathbb{R}^{n}$.

A matrix is invertible iff zero is not an eigenvalue.
### Example Problem
$$
A=
\begin{bmatrix}
1 & 2 \\
4 & 3 \\
\end{bmatrix}
$$
$\text{Find all the eigenvalues of }A.$
1. 
$$
A-\lambda I_{2}=
\begin{bmatrix}
1 & 2 \\
4 & 3 \\
\end{bmatrix}
-
\begin{bmatrix}
\lambda & 0 \\
0 & \lambda \\
\end{bmatrix}
=
\begin{bmatrix}
1-\lambda & 2 \\
4 & 3-\lambda \\
\end{bmatrix}
$$
2. 
$$\text{By invertible matrix theorem,}$$
$$
\begin{vmatrix}
1-\lambda & 2 \\
4 & 3-\lambda \\
\end{vmatrix}
=0
$$
$$
\begin{align}
(1-\lambda)(3-\lambda)-2\cdot4=0 \\
(\lambda-5)(\lambda+1)=0 \\
\end{align}
$$
3. 
$$
∴\lambda=5,\lambda=-1
$$
$\text{Find the corresponding eigenvectors}$
4. 
$$\lambda=5$$
$$
\begin{align}
A\vec{x}=5\vec{x} \\
A\vec{x}-5\vec{x}=\vec{0} \\
(A-5 I_2)\vec{x}=\vec{0} \\
\end{align}
$$
5. 
$$
A-5I_{2}=
\begin{bmatrix}
-4 & 2 \\
4 & -2 \\
\end{bmatrix}
$$
$$\text{The associated augmented matrix is:}$$
$$
\left[
  \begin{matrix}
	-4 & 2 \\
	4 & -2 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		0 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
$$\text{The RREF is:}$$
$$
\left[
  \begin{matrix}
	1 & \frac{-1}{2} \\
	0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		0 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
$$
x_{1}-\frac{1}{2}x_{2}=0
$$
1. 
$$\text{Let }x_{2}=s\text{, so }x_{1}=\frac{s}{2}.$$
$$
\vec{x}=
s
\begin{bmatrix}
\frac{1}{2} \\
1 \\
\end{bmatrix}
|s\in\mathbb{R}
$$
2. 
$$∴\text{Any vector that is a scalar multiple of }
\begin{bmatrix}
\frac{1}{2} \\
1
\end{bmatrix}
\text{ is an eigenvector of }A\text{ with corresponding eigenvalue }\lambda=5.
$$
- The eigenspace of $A$ for $\lambda=5$ is
$$E_{5}=\text{span}\{
\begin{bmatrix}
\frac{1}{2} \\
1 \\
\end{bmatrix}
\}
$$

For triangular matricies, the eigenvalues are the entries along the diagonal. The determinant is also then the product of the eigenvalues.

The **trace** of an $n\times n$ matrix is the sum of its diagonal entries.

$$
A=
\begin{bmatrix}
a & b \\
c & d \\
\end{bmatrix}
$$
$$
\begin{align}
\text{det}(A-\lambda I_{2})=
\begin{vmatrix}
a-\lambda & b \\
c & d-\lambda \\
\end{vmatrix} \\
=(a-\lambda)(b-\lambda)-bc \\
=\lambda^{2}-(a+d)\lambda+ad-bc \\
=\lambda^{2}-\text{trace}(A)\lambda+\text{det}A
\end{align}
$$
For a general $n\times n$ matrix,
$$
\text{det}(A-\lambda I_{2})=(-\lambda)^{n}+\text{trace}(A)(-\lambda)^{n-1}+...+\text{det}(A)
$$
By the fundamental theorem of algebra, this matrix will have at most $n$ real eigenvalues.

The transpose of $A$ has the same eigenvalues as $A$.


