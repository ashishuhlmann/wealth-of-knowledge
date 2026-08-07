## 10/14/25

A linear system is **homogeneous** if its augment matrix is of the form
$$
\left[
  \begin{matrix}
	A
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		\vec{0}
    \end{matrix}
  \right.
\right]
$$
- $A\vec{x}=\vec{0}$
- a homogeneous linear system always has a **trivial solution** $\vec{x}=\vec{0}$
- if there is another solution $\vec{x}\neq\vec{0}$ , then it is said to be a **nontrivial solution**

**Theorem**: A homogenous linear system can only have
1. exactly one solution, being the **trivial solution**
2. infinitely many solutions with free variables
### Example Problem

$\text{Determine whether the following homogeneous linear system has nontrivial solutions:}$
$$
\begin{align}
x_{1}+3x_{2}-5x_{3}=0 \\
x_1+4x_{2}-8x_{3}=0 \\
-3x_{1}-7x_{2}+9x_{3}=0 \\
\end{align}
$$
1. 
$$\text{The associated augmented matrix is:}$$
$$
\left[
  \begin{matrix}
    1 & 3 & -5 \\
    1 & 4 & -8 \\
    -3 & -7 & 9 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      0 \\
      0 \\
    \end{matrix}
  \right.
\right]
$$
2. 
$$R_{2}-R_1$$
$$R_{3}+3R_1$$
$$
\left[
  \begin{matrix}
    1 & 3 & -5 \\
    0 & 1 & -3 \\
    0 & 2 & -6 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      0 \\
      0 \\
    \end{matrix}
  \right.
\right]
$$
3. 
$$R_{3}-2R_{2} $$
$$R_{1}-3R_{2}$$
$$
\left[
  \begin{matrix}
    1 & 0 & 4 \\
    0 & 1 & -3 \\
    0 & 0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      0 \\
      0 \\
    \end{matrix}
  \right.
\right]
$$
4. 
$$
\begin{align}
x_{1}+4x_{3}=0 \\
x_{2}-3x_{3}=0 \\
\end{align}
$$
$$ \text{Let }s=x_{3}$$
$$
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
\end{bmatrix}
=
\begin{bmatrix}
-4s \\
3s \\
s \\
\end{bmatrix}
$$
- The **parametric vector form of the solution** is
$$
\begin{bmatrix}
x_{1} \\
x_{2} \\
y_{2} \\
\end{bmatrix}
=
s
\begin{bmatrix}
-4 \\
3 \\
1 \\
\end{bmatrix}
\phantom{-} s\in\mathbb{R}
$$
$$\text{The nontrivial solutions to the homogeneous system belong to the set:}$$
$$
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
\end{bmatrix}
\in\text{span}\{
\begin{bmatrix}
-4 \\
3 \\
1 \\
\end{bmatrix}
\}$$
### Example Problem

$\text{Determine whether the following homogeneous linear system has nontrivial solutions:}$
$$
\begin{align}
x_{1}+3x_{2}-x_{3}+x_{4}=0 \\
x_2+x_{3}=0 \\
\end{align}
$$
1. 
$$\text{The associated augmented matrix is:}$$
$$
\left[
  \begin{matrix}
    1 & 3 & -1 & 1 \\
    0 & 1 & 1 & 0  \\
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
2. 
$$R_{1}-3R_{2}$$
$$
\left[
  \begin{matrix}
    1 & 0 & -4 & 1 \\
    0 & 1 & 1 & 0  \\
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
$$\text{Let }x_{3}=r\text{, and }x_{4}=s$$
$$
\begin{align}
x_{1}-4r+s=0 \\
x_2+r=0 \\
\end{align}
$$

- **parametric vector form of the solution**
$$
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
x_{4} \\
\end{bmatrix}
=
r
\begin{bmatrix}
4  \\
-1 \\
1  \\
0  \\
\end{bmatrix}
+s
\begin{bmatrix}
-1 \\
0 \\
0  \\
1  \\
\end{bmatrix}
\phantom{-} s\in\mathbb{R}
$$
$$\text{The nontrivial solutions to the homogeneous system belong to the set:}$$
$$
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
x_{4}
\end{bmatrix}
\in
\text{span}\{
\begin{bmatrix}
4 \\
-1 \\
1 \\
0 \\
\end{bmatrix},

\begin{bmatrix}
-1 \\
0 \\
0 \\
1 \\
\end{bmatrix}
\}
$$
## The Homogeneous Component

Consider the equation $A\vec{x}=\vec{b}$.
- Let $\vec{x_{h}}$ be a solution of $A\vec{x}=\vec{0}$.
- Let $\vec{x_{p}}$ be a parametric solution of $A\vec{x}=\vec{b}$. 
- Then the vector $\vec{x_{p}}+\vec{x_{h}}$ is also a solution of the equation $A\vec{x}=\vec{b}$.

If $\vec{x_{p}}$ is a solution of $A\vec{x}=\vec{b}$ then $A\vec{x_{p}}=\vec{b}$
If $\vec{x_{h}}$ is a solution of $A\vec{x}=\vec{0}$ then $A\vec{x_{h}}=\vec{0}$
- Add both equations up and get $A\vec{x_{p}}+A\vec{x_{h}}=\vec{b}+\vec{0}$
### Example

Consider the non-homogeneous system:
$$
\begin{align}
x_{1}+3x_{2}-x_{3}+x_{4}=5 \\
x_2+x_{3}=2 \\
\end{align}
$$
$$
\left[
  \begin{matrix}
    1 & 3 & -1 & 1 \\
    0 & 1 & 1 & 0  \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      5 \\
      2 \\
    \end{matrix}
  \right.
\right]
$$
$$R_{1}-3R_{2}$$
$$
\left[
  \begin{matrix}
    1 & 0 & -4 & 1 \\
    0 & 1 & 1 & 0  \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      -1 \\
      2 \\
    \end{matrix}
  \right.
\right]
$$
The solution of a non-homogeneous system is the *sum of the particular solution and the general homogenous solution*.
$$
\begin{align}
x_{1}-4r+s=-1 \\
x_2+r=2 \\
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
4r-1-s  \\
2-r \\
r  \\
s  \\
\end{bmatrix}
=
\begin{bmatrix}
-1  \\
2 \\
0  \\
0  \\
\end{bmatrix}
+
r
\begin{bmatrix}
4  \\
-1 \\
1  \\
0  \\
\end{bmatrix}
+s
\begin{bmatrix}
-1 \\
0 \\
0  \\
1  \\
\end{bmatrix}
\phantom{-} s\in\mathbb{R}
$$
- *Note: The solution set in this case is not the span of the three vectors above.*
## Linear Dependence and Independence

The vectors $\vec{v_{1}}, \vec{v_{2}},...\vec{v_{n}}$ are **linearly dependent** if there exists constants $c_{1},c_{2},...c_{n}$ not all zero such that $c_{1}\vec{v_{1}}+c_{2}\vec{v_{2}}+...+c_{n}\vec{v_{n}}=\vec{0}$.
## Example

Consider the following vectors:
$$
\begin{bmatrix}
1 \\
2 \\
\end{bmatrix}
,
\begin{bmatrix}
-3 \\
-6 \\
\end{bmatrix}
$$

- These vectors are linearly dependent because

$$
3
\begin{bmatrix}
1 \\
2 \\
\end{bmatrix}
+1
\begin{bmatrix}
-3 \\
-6 \\
\end{bmatrix}
=\vec{0}
$$

**Theorem**: To determine whether $\vec{v_{1}}, \vec{v_{2}},... \vec{v_{n}}\in\mathbb{R}^{m}$ are linearly indpendented or linearly dependent, solve the homogenous linear system $A\vec{x}=\vec{0}$ where $A=[\vec{v_{1}}, \vec{v_{2}},... \vec{v_{n}}]$
1. $\vec{v_{1}}, \vec{v_{2}},... \vec{v_{n}}$ are linearly independent iff $A\vec{x}=\vec{0}$ only has the trivial solution
2. $\vec{v_{1}}, \vec{v_{2}},... \vec{v_{n}}$ are linearly dependent iff $A\vec{x}=\vec{0}$ has nontrivial solutions
### Question

Let $\vec{v_{1}}, \vec{v_{2}},... \vec{v_{n}}\in\mathbb{R}^{m}$ where $n>m$. Can this set of vectors be linearly independent?
- If $A=[\vec{v_{1}}, \vec{v_{2}},... \vec{v_{n}}]$, then in it's RREF there will be free variables.
- If $m<n$, no conclusion can be made.
### Question

Let $\vec{v_{1}}, \vec{v_{2}}, \vec{v_{3}}\in\mathbb{R}^{m}$ be linearly independent. Let $\vec{w_{1}}=\vec{v_{1}}, \vec{w_{2}}=\vec{v_{1}}+\vec{v_{2}}, \vec{w_{3}}=\vec{v_{1}}+\vec{v_{2}}+\vec{v_{3}}$ . Are $w_{1}, w_{2}$, and $w_{3}$ linearly independent?

A collection of vectors including the zero vector will always be linearly dependent.

Two vectors are linearly dependent iff they are scalar multiples of eachother
### Example Problem

$\text{Are the following vectors}$
$$
\begin{bmatrix}
1 \\
2 \\
3 \\
\end{bmatrix}
,
\begin{bmatrix}
-1 \\
2  \\
3  \\
\end{bmatrix}
,
\begin{bmatrix}
4 \\
5 \\
6 \\
\end{bmatrix}
$$
$\text{linearly dependent or not?}$
1. 
$$
c_{1}
\begin{bmatrix}
1 \\
2 \\
3 \\
\end{bmatrix}
+c_{2}
\begin{bmatrix}
-1 \\
2  \\
3  \\
\end{bmatrix}
+c_{3}
\begin{bmatrix}
4 \\
5 \\
6 \\
\end{bmatrix}
=\vec{0}
$$
$$\text{The associated augmented matrix is:}$$
$$
\left[
  \begin{matrix}
    1 & -1 & 4 \\
    2 & 2 & 5 \\
    3 & 3 & 6 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      0 \\
      0 \\
    \end{matrix}
  \right.
\right]
$$
2. 
$$
\begin{align}
R_{2}-2R_{1} \\
(R_{3}-3R_{1})/6 \\
\end{align}
$$
$$
\left[
  \begin{matrix}
    1 & -1 & 4 \\
    0 & 4 & -3 \\
    0 & 1 & -1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      0 \\
      0 \\
    \end{matrix}
  \right.
\right]
$$
3. 
$$
\begin{align}
4R_{3}-R_{2} \\
4R_{1}+R_{2} \\
\end{align}
$$
$$
\left[
  \begin{matrix}
    1 & 0 & 13 \\
    0 & 4 & -3 \\
    0 & 0 & -1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      0 \\
      0 \\
    \end{matrix}
  \right.
\right]
$$
4. 
$$
\begin{align}
R_{1}+13R_{3} \\
R_{2}-3R_{3} \\
\end{align}
$$
$$
\left[
  \begin{matrix}
    1 & 0 & 0 \\
    0 & 4 & 0 \\
    0 & 0 & -1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      0 \\
      0 \\
    \end{matrix}
  \right.
\right]
$$
5. 
$$\div$$
$$
\left[
  \begin{matrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      0 \\
      0 \\
    \end{matrix}
  \right.
\right]
$$
$$\text{RREF}$$
$$
\begin{align}
c_{1}=0 \\
c_{2}=0 \\
c_{3}=0 \\
\end{align}
$$
$$
∴\text{The vectors }
\begin{bmatrix}
1 \\
2 \\
3 \\
\end{bmatrix}
,
\begin{bmatrix}
-1 \\
2  \\
3  \\
\end{bmatrix}
,
\begin{bmatrix}
4 \\
5 \\
6 \\
\end{bmatrix}
\text{are linearly independent.}
$$
## [[8 Linear Transformations]]