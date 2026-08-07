## 9/30/25
## Matrix

An $m\times n$ **matrix** is a rectangular array with $m$ rows and $n$ columns.
- $m\times n$ is called the **size** of the matrix
- $a_{ij}$ is the $(i,j)\text{th}$ entry of the matrix (the entry in the $i\text{th}$ row and $j\text{th}$ column using **one-based indexing**)
### Example
$$
\begin{bmatrix}
1 & 2 & 3 \\
-4 & 5 & 7 \\
\end{bmatrix}
$$
- $2\times 3$ matrix
- the $(2,1)\text{th}$ entry is $-4$
### Example
$$
\begin{bmatrix}
1 \\
\end{bmatrix}
$$
- $1\times 1$ matrix
## Solving Linear Systems

Consider a system of $m$ linear equations in $n$ variables $x_1, x_2,...x_n$.
$$
\begin{align}
a_{11}x_{1}+a_{12}x_2+...+a_{1n}x_{n}=b_{1} \\
a_{21}x_{1}+a_{22}x_2+...+a_{2n}x_{n}=b_{2} \\
\vdots\phantom{---}\vdots\phantom{---}\vdots\phantom{--=}\vdots\phantom{---}\vdots \\
a_{m1}x_{1}+a_{m2}x_2+...a_{mn}x_{n}=b_{m} \\
\end{align}
$$
Encode the information of this linear system in its associated **augmented matrix**.
$$
\left[
  \begin{matrix}
    a_{11} & a_{12} & ... & a_{1n}  \\
    a_{21} & a_{22} & ... & a_{2n}  \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{m1} & a_{m2} & ... & a_{mn}  \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      b_{1}  \\
      b_{2}  \\
      \vdots  \\
      b_{m}  \\
    \end{matrix}
  \right.
\right]
$$
## Elementary Row Operations

1. row replacement
2. row interchange
3. row scaling

**Row Echelon Form (REF)**
1. all zero rows are at the bottom of the matrix
2. the first non-zero entry of each row is to the right of the first non-zero entry of the row above it
3. all entries in a column below a leading entry are zero
### Example
$$
\begin{bmatrix}
4 & -1 & 3 & 2  \\
0 & -1 & -3 & 1 \\
0 & 0 & 0 & -5  \\
\end{bmatrix}
$$
- [x] no zero rows
- [x] all the first non-zero entries of each row are to the right of the first non-zero entry of the row above
- [x] all entries blow a leading entry are zero

**Reduced Row Echelon Form (RREF)**
	1. a special case of REF
	2. the leading entry of each non-zero row is one (leading one)
	3. if a column contains a leading one, then all other entries of that column are zero
### Example

$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$
- REF and RREF
$$
\begin{bmatrix}
1 & -1 & 0 & 2 \\
0 & 0 & 1 & -1 \\
0 & 0 & 0 & 0  \\
\end{bmatrix}
$$
- REF and RREF
$$
\begin{bmatrix}
1 & 0 & 0 & 29 \\
0 & 1 & 0 & 16 \\
0 & 0 & 1 & 3  \\
\end{bmatrix}
$$
- REF and RREF
## Gauss-Jordan Elimination

- linear system -> associated augmented matrix -> RREF -> immediate solution
- Transforming a matrix into just REF is called **Gaussian Elimination**.
## RREF Solution

- Each row corresponds to a final equation that can be read off from left to right.
- **leading variables** - variables corresponding to the first entries of RREF (by convention)
- **free variables** - variables corresponding to non leading entries of RREF (by convention)
- Use dummy variables for free variables and functions of those dummy variables for leading variables in the solution to a linear system.

**Theorem**: RREF's are *unique.* Each matrix is row equivalent to exactly one matrix in RREF
- two matrices are **row equivalent** if there is a finite amount of row operations between them
### Example Problem

$\text{Solve the following linear system:}$
$$
\begin{align}
x_{3}-2x_{4}&=-3 \\
-x_{1}+7x_{2}-4x_{3}+2x_{4}&=7 \\
x_{1}-7x_{2}\phantom{---}+6x_{4}&=5 \\
\end{align}

$$

1. 
$$\text{The associated augmented matrix is:}$$
$$
\left[
  \begin{matrix}
    0 & 0 & 1 & -2  \\
    -1 & 7 & -4 & 2  \\
    1 & -7 & 0 & 6 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      -3  \\
      7  \\
      5  \\
    \end{matrix}
  \right.
\right]
$$
2. 
$$
R_{1} \xleftrightarrow{} R_{3}
$$

$$
\left[
  \begin{matrix}
	1 & -7 & 0 & 6  \\
    -1 & 7 & -4 & 2 \\
    0 & 0 & 1 & -2  \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      5  \\
      7  \\
      -3  \\
    \end{matrix}
  \right.
\right]
$$
3. 
$$
R_{2}+R_{1}
$$
$$
\left[
  \begin{matrix}
	1 & -7 & 0 & 6 \\
    0 & 0 & -4 & 8 \\
    0 & 0 & 1 & -2 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      5  \\
      12  \\
      -3  \\
    \end{matrix}
  \right.
\right]
$$
4. 
$$
R_{2} \xleftrightarrow{} R_{3}
$$
$$
\left[
  \begin{matrix}
	1 & -7 & 0 & 6 \\
    0 & 0 & 1 & -2 \\
    0 & 0 & -4 & 8 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      5  \\
      -3  \\
      12  \\
    \end{matrix}
  \right.
\right]
$$
5. 
$$
R_{3}+4R_{2}
$$
$$
\left[
  \begin{matrix}
	1 & -7 & 0 & 6 \\
    0 & 0 & 1 & -2 \\
    0 & 0 & 0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      5  \\
      -3  \\
      0  \\
    \end{matrix}
  \right.
\right]
$$
6. 
$$\text{The system is now in RREF.}$$
$$
\begin{align}
x_{1}-7x_{2}\phantom{---}+6x_{4}&=5 \\
x_{3}-2x_{4}&=-3 \\
0&=0 \\
\end{align}
$$
$$
\begin{align}
\text{leading variables: } x_{1},x_{3} \\
\text{free variables: }x_{2},x_{4}
\end{align}
$$
7. 
$$
\text{Let }x_{2}=s\text{ and }x_{4}=t
$$
$$
\begin{align}
x_{1}-7s\phantom{--}+6t&=5 \\
x_{3}-2t&=-3 \\
\end{align}
$$
$$
\begin{align}
x_{1}&=5-6t+7s \\
x_{3}&=2t-3 \\
\end{align}
$$
$$
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
x_{4} \\
\end{bmatrix}
=
\begin{bmatrix}
5-6t+7s \\
s \\
2t-3 \\
t \\
\end{bmatrix}
$$
$$
∴\text{This system has }infinitely\text{ many solutions.}
$$
## Example

A contradiction is formed when a zero row has a non-zero constant.
$$
\left[
  \begin{matrix}
	1 & -7 & 0 & 6 \\
    0 & 0 & 1 & -2 \\
    0 & 0 & 0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      5  \\
      -3  \\
      1  \\
    \end{matrix}
  \right.
\right]
$$$$
\begin{align}
x_{1}-7x_{2}\phantom{---}+6x_{4}&=5 \\
x_{3}-2x_{4}&=-3 \\
0&=1\phantom{-}\# \\
\end{align}
$$
$$
∴\text{This system has no solution.}
$$

## Information

- Elementary row operations don't change the system or solution at all.
- Elementary row operations do not delete information
- Multiplying a row by zero *is not an elementary row operation*
## [[3 Notes on Systems]]