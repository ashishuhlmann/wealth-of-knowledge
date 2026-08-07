## 11/4/25
## Addition and Scalar Multiplication

Let $A$ and $B$ both be $m\times n$ matricies with real entries.
- $A+B$ is an $m\times n$ matrix whos entries are the sums of the corresponding entries in $A$ and $B$.

$$
\begin{bmatrix}
	a_{11} & a_{12} & ... & a_{1n}  \\
    a_{21} & a_{22} & ... & a_{2n}  \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{m1} & a_{m2} & ... & a_{mn}  \\
\end{bmatrix}
+
\begin{bmatrix}
	b_{11} & b_{12} & ... & b_{1n}  \\
    b_{21} & b_{22} & ... & b_{2n}  \\
    \vdots & \vdots & \ddots & \vdots \\
    b_{m1} & b_{m2} & ... & b_{mn}  \\
\end{bmatrix}
=
\begin{bmatrix}
	a_{11}+b_{11} & a_{12}+b_{12} & ... & a_{1n}+b_{1n}  \\
    a_{21}+b_{21} & a_{22}+b_{22} & ... & a_{2n}+b_{2n}  \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{m1}+b_{m1} & a_{m2}+b_{m2} & ... & a_{mn}+b_{mn}  \\
\end{bmatrix}
$$

Let $c$ be a scalar and $A$ be an $m\times n$ matrix with real entries.
- $cA$ is an $m\times n$ matrix whose entries are the entries of $A$ multiplied by $c$.
$$
c
\begin{bmatrix}
	a_{11} & a_{12} & ... & a_{1n}  \\
    a_{21} & a_{22} & ... & a_{2n}  \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{m1} & a_{m2} & ... & a_{mn}  \\
\end{bmatrix}
=
\begin{bmatrix}
	ca_{11} & ca_{12} & ... & ca_{1n}  \\
    ca_{21} & ca_{22} & ... & ca_{2n}  \\
    \vdots & \vdots & \ddots & \vdots \\
    ca_{m1} & ca_{m2} & ... & ca_{mn}  \\
\end{bmatrix}
$$
## Properties of Matrix Algebra

Let $A, B, C$ be matricies of the same size and let $r, s$ be scalars.

- $A+B=B+A$
- $(A+B)+C=A+(B+C)$
- $r(A+B)=rA+rB$
- $(r+s)A=rA+sA$
- $r(sA)=(rs)A$
- $A+\boldsymbol{0_{n}}=A$
## Matrix Multiplication

If $A$ is an $m\times n$ matrix, then multiplication by $A$ defines a linear transformation $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$ where $A$ is the standard matrix.

If $A$ is and $m\times n$ matrix, and $B$ is an $n\times p$ matrix, (where the number of columns of $A$ is the same as the number of rows in $B$), then the matrix product $AB$ is the standard matrix of the composition of transformations $T_{A}\circ T_{B}:\mathbb{R}^{p}\rightarrow\mathbb{R}^{m}$.
$$
 \vec{x}\rightarrow B\vec{x}\rightarrow A(B\vec{x})=AB\vec{x}=T_{A}(T_{B}(\vec{x}))
$$ 
Using the standard basis,
$$AB=
\begin{bmatrix}
T_{A}\circ T_{B}(\vec{e_{1}}) & T_{A}\circ T_{B}(\vec{e_{2}}) & ... & T_{A}\circ T_{B}(\vec{e_{p}}) \\
\end{bmatrix}
$$
### Method: Column Scaling
$$
B=
\begin{bmatrix}
\vec{v_{1}} & \vec{v_{2}} & ... & \vec{v_{p}}
\end{bmatrix}
$$
$$
AB=
\begin{bmatrix}
A\vec{v_{1}} & A\vec{v_{2}} & ... & A\vec{v_{p}}
\end{bmatrix}
$$
- Matrix multiplication is simply *repeated matrix-vector multiplication*, where the vectors are the columns of $B$.
### Method: Dot Product
$$
A=
\begin{bmatrix}
\vec{u_{1}} \\
\vec{u_{2}} \\
\vdots \\
\vec{u_{m}}
\end{bmatrix}
$$
$$
B=
\begin{bmatrix}
\vec{v_{1}} & \vec{v_{2}} & ... & \vec{v_{p}} \\
\end{bmatrix}
$$

$$
AB=
\begin{bmatrix}
\vec{u_{1}}\cdot\vec{v_{1}} & \vec{u_{1}}\cdot\vec{v_{2}} & ... & \vec{u_{1}}\cdot\vec{v_{p}} \\
\vec{u_{2}}\cdot\vec{v_{1}} & \vec{u_{2}}\cdot\vec{v_{2}} & ... & \vec{u_{2}}\cdot\vec{v_{p}} \\
\vdots & \vdots & \ddots & \vdots \\
\vec{u_{m}}\cdot\vec{v_{1}} & \vec{u_{m}}\cdot\vec{v_{2}} & ... & \vec{u_{m}}\cdot\vec{v_{p}} \\
\end{bmatrix}
$$
### Properties of Matrix Multiplication

Let $A,B,C$ be matricies of the appropriate sizes such that the following operations are defined:

- $A(BC)=(AB)C$
- $A(B+C)=AB+AC$
- $(B+C)A=BA+CA$
- $r(AB)=r(A)B=A(rB)$ for any scalar $r$
- $IA=A$
### Non-properties of Matrix Multiplication

- $AB\neq BA$
- If $AB=\boldsymbol{0}$, then it *does not* imply that $A=\boldsymbol{0}$ or $B=\boldsymbol{0}$  
- If $AB=AC$, that does not impy that $B=C$
- If $BA=CA$, that does not imply $B=C$
## [[10 Determinants and Inverse]]