## 10/2/25
## Pivot Positions

**pivot position** - location in a matrix that corresponds to a leading one in a RREF of that matrix
**pivot column** - column of that matrix that contains a pivot position
### Example

$$
\begin{bmatrix}
\bf{1} & 4 & 5  \\
-1 & -2 & -1 \\
-2 & -3 & 0 \\
\end{bmatrix}
$$
- $(1,1)$ is the pivot position and column $1$ is the pivot column
$$
\begin{align}
R_{2}+R_{1}  \\
R_{3}+2R_{1} \\
\end{align}
$$
$$
\begin{bmatrix}
1 & 4 & 5  \\
0 & \bf{2} & 4 \\
0 & 5 & 10 \\
\end{bmatrix}
$$
- $(2,2)$ is the new pivot position and column $2$ is the new pivot column
## REFF Forms
1. it has a unique solution
	 - iff there are no free variables
	 - iff all variables are **basic variables** (leading variables)
2. it has infinitely many solutions
	 - iff there are free variables
	 - iff not all variables are leading variables
3. it is inconsistent
	 - iff it contains a zero row with a non-zero constant

*Note: if and only if (iff) signifies reciprocal conditions (if A then B AND if B then A)*

If all variables are leading variables, then the system is consistent.
### Example

$$
\left[
  \begin{matrix}
    1 & 1 & -2  \\
    0 & -4 & 2  \\
    0 & 0 & 6 \\
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
- if there are any free variables, the system has infinitely many solutions
### Example

$$
\left[
  \begin{matrix}
    1 & 1 & -2  \\
    0 & -4 & 2  \\
    0 & 0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      -3  \\
      7  \\
      0  \\
    \end{matrix}
  \right.
\right]
$$
## Exam Steps

1. the **associated augmented matrix** is:
2. this system is **inconsistent** and has **no solution**
3. the augmented matrix is in **RREF**: ... the solution is:
## [[4 Vector Equations]]