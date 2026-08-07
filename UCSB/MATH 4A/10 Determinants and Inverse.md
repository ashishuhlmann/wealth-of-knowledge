## Determinant

The **determinant** is the amount that space (any area, volume, higher dimensional volume...) is scaled by during a linear transformation.
- If the determinant is zero, the space was squished into a lower dimension.
- If the determinant is negative, the space was somehow relfected over itself.
### In One Dimension
$$
\text{det}
\begin{bmatrix}
a_{11}
\end{bmatrix}
=a_{11}
$$
## Laplace Expansion

The $(i,j)$th **cofactor** of a matrix $A$ is
$$
C_{ij}=(-1)^{i+j}\text{det}A_{ij}
$$
where $A_{ij}$ is the matrix obtained by removing the $i$th row and $j$th column from $A$.
- *Note: Remember one-based indexing.*

**Theorem**: For any $n\times n$ matrix $A$, you can preform Laplace expansion along *any* row $i$ and *any* column $j$, giving the same determinant.
- If any row or column in $A$ is zero, then $\text{det}A=0$ since you can do Laplace expansion along that zero row, making every term zero.
### In Two Dimensions

Laplace Expansion along the first row
$$
\begin{align}
\text{det}
\begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22} \\
\end{bmatrix}
&=
a_{11}\text{det}[a_{22}]-a_{12}\text{det}[a_{21}] \\
&=
a_{11}a_{22}-a_{12}a_{21}
\end{align}
$$
### In Three Dimensions

Laplace Expansion along the first row
$$
\begin{align}
\text{det}
\begin{bmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
\end{bmatrix}
&=
a_{11}\text{det}
\begin{bmatrix}
a_{22} & a_{23} \\
a_{32} & a_{33} \\
\end{bmatrix}
-a_{12}\text{det}
\begin{bmatrix}
a_{21} & a_{23} \\
a_{31} & a_{33} \\
\end{bmatrix}
+a_{13}\text{det}
\begin{bmatrix}
a_{21} & a_{22} \\
a_{31} & a_{32} \\
\end{bmatrix} \\
&=
a_{11}(a_{22}\text{det}[a_{33}]-a_{23}\text{det}[a_{32}])
-a_{12}(a_{21}\text{det}[a_{33}]-a_{23}\text{det}[a_{31}])
+a_{13}(a_{22}\text{det}[a_{31}]-a_{21}\text{det}[a_{32}])
\end{align}
$$
### Tricks

A square matrix is **upper triangular** if all entries below the diagonal are zero. Similarly, a square matrix is **lower triangular** if all entries above the diagonal are zero. (The diagonal can be non-zero.)
### Example
$$
\begin{bmatrix}
1 & 4 & 5 \\
0 & 2 & 0 \\
0 & 0 & 3 \\
\end{bmatrix}
$$
$$
\begin{bmatrix}
1 & 0 & 0 \\
4 & 2 & 0 \\
5 & 0 & 3 \\
\end{bmatrix}
$$
**Theorem**: If $A$ is upper triangular or lower triangular, then $\text{det}A$ is the product of diagonal entries.
## Properties of Determinants

1. If any two rows of a matrix are swapped, the determinant of the resulting matrix has the negative of the determinant of the original matrix.
2. The determinant of a matrix obtained from elementary row opperations has the same determinant as the original (other than row swaps, which will negate the determinant).
3. The determinant of a matrix $A$ with one row multiplied by a scalar $k$ is $k\text{det}A$.
4. $\text{det}A=\text{det}A^{T}$
5. $\text{det}(A^{-1})=(\text{det}A)^{-1}$
6. $\text{det}(AB)=\text{det}(A)\text{det}(B)$
7. $\text{det}(A+B)\neq\text{det}A+\text{det}B$

That means that the determinant of any matrix is the product of some non-zero factors times the determinant of the RREF of that matrix. 
The determinant of the RREF is one or zero, because either it will be the identity matrix, or a matrix with zero rows. 

**Theorem**: If a square matrix $A$ has two equal rows or columns, then $\text{det}A=0$. This is also true if two rows or columns are scalar multiples of each other.
## Transpose

If $A$ is an $m\times n$ matrix, its **transpose** $A^{T}$ is an $n\times m$ matrix whose rows are the columns of $A$ and columns are the rows of $A$.
### Properties of Tranposes

- $(A^{T})^{T}=A$
- $(A+B)^{T}=A^{T}+B^{T}$
- $(rA)^{T}=rA^{T}$
- $(AB)^{T}=B^{T}A^{T}$
## Inverse

Let $A$ be a $n\times n$ matrix  (it must be square). $A$ is said to be **invertable** iff there exists another $n\times n$ matrix $B$ such that $AB=BA=I_{n}$.

**Theorem**: Algorithm for Inverting
To solve for an inverse, we must solve for $B$ in $AB=I_{n}$. Matrix multiplication is simply repeated matrix-vector multiplication. Therefore, row reduce the following augmented matrix into RREF.
$$
\left[
  \begin{matrix}
	A
  \end{matrix}
  \left|
    \,
    \begin{matrix}
	I_{n}
    \end{matrix}
  \right.
\right]
$$
- If $\text{RREF}([A|I_{n}])=[I_{n}|B]$, then $A^{-1}=B$.
- If $\text{RREF}([A|I_{n}])\neq[I_{n}|B]$, then $A$ is not invertable.

A matrix is invertable iff it it's corresponding linear transformation is bijective.

**Theorem**: Let $A$ be a $2\times2$ matrix. The $A$ is invertable iff $\text{det}(A)\neq0$
- $A$ is said to be **non-singular**.

An **invertable linear transformation** $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{n}$
- there exists a linear transformation $S:\mathbb{R}^{n}\rightarrow\mathbb{R}^{n}$ such that $S(T(\vec{x}))=\vec{x}\forall\vec{x}\in\mathbb{R}^{n}$ and $T(S(\vec{x}))=\vec{x}\forall\vec{x}\in\mathbb{R}^{n}$
- Then, $S=T^{-1}$
### Properties of Inverses

- If $A$ is invertable, than $A^{-1}$ is also invertable.
- If $A$ and $B$ are invertable matricies of the same size, then $(AB)^{-1}=B^{-1}A^{-1}$

**Orthogonal** matricies have equal tranpose and inverses.

Let $A$ be an $n\times n$ matrix. The **adjoint or adjugate** of $A$ is the transpose of the **cofactor matrix** of $A$.
$$
\text{adj}A=
\begin{bmatrix}
c_{11} & c_{12} & ... & c_{1n} \\
c_{21} & c_{22} & ... & c_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
c_{n1} & c_{n2} & ... & c_{nn} \\
\end{bmatrix}^{T}
$$
$$
c_{ij}=(-1)^{i+j}\text{det}A_{ij}
$$
$$
A^{-1}=\frac{1}{\text{det}A}\text{adj}A
$$
## Symmetry

A matrix $A$ is called **symmetric** when $A=A^{T}$

A matrix $A$ is called **skew-symmetric** if $A=-A^{T}$
