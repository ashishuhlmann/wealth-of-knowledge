## ??/??/??
## Subsets

A **subset** $W$ of $\mathbb{R}^{n}$ is a subspace of it if
1. $\vec{0}_{W}\in W$
2. $\vec{w_{1}}+\vec{w_{2}}\in W$ for any $\vec{w_{1}},\vec{w_{2}}\in W$
3. If $\vec{w}\in W$, then $c\vec{w}\in W$  for any scalar $c$
### Example

The $x$-axis is a subspace of $\mathbb{R}^{2}$. In  general, any line through the origin is a subspace of $\mathbb{R}^{2}$ In $\mathbb{R}^{3}$, any line or plane through the origin is a subspace.
- $\mathbb{R}^{n}$ is a subspace of itself.
## Nullspace

Let $A$ be an $m\times n$ matrix. The **nullspace** of $A$ is the solution set to the homogenous system
$$
\text{null}A=\{\vec{x}\in\mathbb{R}^{n}|A\vec{x}=\vec{0}\}
$$
Let $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$ be a linear transformation. The **nullspace** of $T$, also called the **kernel** of $T$ is
$$
\text{ker}T=\text{null}T=\{\vec{x}\in\mathbb{R}^{n}|T(\vec{x})=\vec{0}\}
$$

The nullspace of an $n\times n$ invertible matrix is $\vec{0}_{n}$.
### Example Problem

$$
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
\rightarrow
\begin{bmatrix}
x+y+z   \\
x+2y+3z \\
\end{bmatrix}
$$
1. 
$$\text{The standard matrix }A\text{ of }T\text{ is:}$$
$$
A=
\begin{bmatrix}
1 & 1 & 1 \\
1 & 2 & 3 \\
\end{bmatrix}
$$
$$
A\vec{x}=\vec{0}
$$
2. 
$$\text{The associated agumented matrix in RREF is:}$$
$$
\left[
  \begin{matrix}
	1 & 0 & -1 \\
	0 & 1 & 2  \\
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
3. 
$$
∴\text{null}T=\{t
\begin{bmatrix}
1 \\
-2 \\
1 \\
\end{bmatrix}
|t\in\mathbb{R}
\}
$$
## Column Space

The **column space** of an $m\times n$ matrix $A$, noted as $\text{col}A$, is defined as the span of its columns.

Let $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$ be a linear transformation given by $T(\vec{x})=A\vec{x}$. Then the image of $T$
$$
\text{im}T=\{T(\vec{x})|\vec{x}\in\mathbb{R}^{n}\}
=
\{A\vec{x}|\vec{x}\in\mathbb{R}^{n}\}
$$

$\text{im}T$ is a subspace of $\mathbb{R}^{m}$.
- $T$ is onto iff $\text{im}T=\mathbb{R}^{m}$
### Example Problem

$\text{Find the column space of the following matrix:}$
$$
A=
\begin{bmatrix}
1 & 3 & 3 & 2 & -9 \\
-2 & -2 & 2 & -8 & 2 \\
2 & 3 & 0 & 7 & 1 \\
3 & 4 & -1 & 11 & -8 \\
\end{bmatrix}
$$
1. 
$$
\begin{align}
\text{RREF}A=
\begin{bmatrix}
1 & 0 & -3 & 5 & 0 \\
0 & 1 & 2 & -1 & 0 \\
0 & 0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 & 0 \\
\end{bmatrix} \\
\vec{v_{1}}\phantom{-.}\vec{v_{2}}\phantom{-.}\vec{v_{3}}\phantom{-.}\vec{v_{4}}\phantom{-.}\vec{v_{5}}\phantom{.}
\end{align}
$$
2. 
$$
\begin{align}
\text{Notice that} \\
\vec{v_{3}}&=-3\vec{v_{1}}+2\vec{v_{2}} \\
\vec{v_{4}}&=5\vec{v_{1}}-2\vec{v_{2}}
\end{align}
$$
$$
\vec{v_{1}},\vec{v_{2}}\text{, and }\vec{v_{5}}\text{ are linearly independent and }\vec{v_{3}},\vec{v_{4}}\text{ are linear combinations of }\vec{v_{1}},\vec{v_{2}}\text{, and }\vec{v_{5}}
$$
3. 
$$
∴\vec{v_{1}},\vec{v_{2}}\text{, and }\vec{v_{5}}\text{ form a basis of col}A\text{ and the dimensions of col}A\text{ is }3.
$$
**Theorem**: The pivot columns of $A$ form a basis of the column space of $A$.
*When in doubt, RREF it.* 

Let $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$ be a linear transformation with standard matrix $A$. Then the **rank** $\text{rank}T=\text{rank}A$ is the dimension of the column space of $A$. It is the number of leading variables in the RREF of $A$.

The **nulity** $\text{nulity}T=\text{nulity}A$ is the dimension of the nullspace of $A$. It is the number of free variables in the RREF of $A$.

**Theorem**: Rank-Nulity
Let $A$ be an $m\times n$ matrix. Then the rank of $A$ plus the nulity of $A$ is $n$. Similarly if $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$ is a linear transformation, then the rank of $T$ plus the nulity of $T$ is $n$.
## Basis

Let $W$ be a subspace of $\mathbb{R}^{n}$. We say that the set $\{\vec{v_{1}},\vec{v_{2}},...\vec{v_{r}}\}$ is a basis of $W$ if
1. $\text{span}\{\vec{v_{1}},\vec{v_{2}},...\vec{v_{r}}\}=W$
2. $\{\vec{v_{1}},\vec{v_{2}},...\vec{v_{r}}\}$ is linearly independent.

**Theorem**: If $W$ is a subspace of $\mathbb{R}^{n}$, then $W$ has a basis. 
- Any two bases of $W$ have the same number of vectors which is the dimension of $W$.
ndent set o
**Theorem**: Basis
Let $W$ be a $p$-dimensional subspace of $\mathbb{R}^{n}$.
- Any linearly independent set of exactly $p$ vectors in $W$ is a basis of $W$.
- Any set of $p$ vectors in $W$ that spans $W$ is also a basis of $W$. 

**Theorem**: Invertible Matrix
Let $A$ be an $n\times n$ matrix. Then $A$ is invertible iff
- $\text{null}A=\{\vec{0_{n}}\}$
- $\text{nulity}A=0$
- $\text{rank}A=n$
- $\text{col}A=\mathbb{R}^{n}$
- columns of $A$ form a basis of $\mathbb{R}^{n}$
- $A\vec{x}=\vec{b}$ has a solution for every $\vec{b}\in\mathbb{R}^{n}$
- $\text{im}T=\mathbb{R}^{n}$
- $T$ is bijective
## Row Space

The **row space** $\text{row}A$ is the span of the rows of $A$.

If $A$ is an $m\times n$ matrix, and it is the standard matrix of $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$, then $\text{null}A$ is actually a subspace of $\mathbb{R}^{n}$.
- The column space $\text{col}A$ is a subspace of $\mathbb{R}^{m}$.
- The row space $\text{row}A$ is subspace of $\mathbb{R}^{n}$.

## [[11 Vector Spaces]]