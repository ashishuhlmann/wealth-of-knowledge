## 10/9/25
## Matrix Vector Multiplication
### Method: Column Scaling

Let $A$ be an $m\times n$ matrix with *columns* $\vec{a_{1}}, \vec{a_{2}},...\vec{a_{n}}\in\mathbb{R}^{m}$ and $\vec{x}\in\mathbb{R}^{n}$
$$
A\vec{x}=x_{1}\vec{a_{1}}+x_{2}\vec{a_{2}}+...+x_{n}\vec{a_{n}}
$$
- *Note: The number of columns in* $A$ *must be equal to the number of entries in* $\vec{x}$
### Example

$$
A=
\begin{bmatrix}
1 & 2 \\
3 & 4 \\
5 & 6 \\
\end{bmatrix}
$$
$$
\vec{x}=
\begin{bmatrix}
7 \\
8 \\
\end{bmatrix}
$$
$$
A\vec{x}=
7
\begin{bmatrix}
1 \\
3 \\
5 \\
\end{bmatrix}
+8
\begin{bmatrix}
2 \\
4 \\
6 \\
\end{bmatrix}
=
\begin{bmatrix}
23 \\
53 \\
73 \\
\end{bmatrix}
$$
### Method: Dot Product

Let  be an  matrix with *rows* $\vec{a_{1}}, \vec{a_{2}},...\vec{a_{n}}\in\mathbb{R}^{n}$ and $\vec{x}\in\mathbb{R}^{n}$
$$
A\vec{x}=
\begin{bmatrix}
\vec{x}\cdot\vec{a_{1}} \\
\vec{x}\cdot\vec{a_{2}} \\
\vdots \\
\vec{x}\cdot\vec{a_{m}} \\
\end{bmatrix}
$$

An $m\times n$ matrix multiplied by an $n\times k$ matrix results in a $m\times k$ matrix.
## Connection to Linear Systems

We can think of a linear system in the variables $x_{1},x_{2},...x_{n}$ with the associated augmented matrix in two ways.

$$
\left[
  \begin{matrix}
    A \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      \vec{b} \\
    \end{matrix}
  \right.
\right]
$$
1. 
$$
x_{1}\vec{a_{1}}+x_{2}\vec{a_{2}}+...+x_{n}\vec{a_{n}}=\vec{b}
$$
2. 
$$
A\vec{x}=\vec{b}
$$
$$
\vec{x}=
\begin{bmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{n}
\end{bmatrix}
$$
## Solvability

Consider an $m\times n$ matrix matrix.

$$
\left[
  \begin{matrix}
    \vec{a_{1}} & \vec{a_{2}} & ... & \vec{a_{n}} \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      \vec{b} \\
    \end{matrix}
  \right.
\right]
,\phantom{-}\vec{b}\in\mathbb{R}^{m}
$$
- The associated augment matrix is:
$$
\left[
  \begin{matrix}
    A \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      \vec{b} \\
    \end{matrix}
  \right.
\right]
$$
- Use row reduction to arrive at:
$$
\left[
  \begin{matrix}
    A' \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      \vec{d} \\
    \end{matrix}
  \right.
\right]
$$
- If $A'$ has a zero row with a non-zero constant, the system would be inconsistent and $A\vec{x}=\vec{b}$ would not be solvable.
- We need every row in $A'$ to have a leading one or pivot position.

**Theorem**: Let $A$ be an $m\times n$ matrix.
1. For every $\vec{b}\in\mathbb{R}^{m}$, the matrix equation $A\vec{x}=\vec{b}$ has a solution.
2. For every $\vec{b}\in\mathbb{R}^{m}$, $\vec{b}$ is a linear combination of the columns of $A$.
3. $\text{span}\{\vec{a_{1}}, \vec{a_{2}},...\vec{a_{n}}\}=\mathbb{R}^{m}$ where $\vec{a_{i}}$ are the columns of $A$.
4. $A'$ has a leading one in every row.
## Question

Let $A$ be an $m\times n$ matrix where $m>n$. Is $A\vec{x}=\vec{b}$ solvable *for all* vectors $\vec{b}$ in $\mathbb{R}^{m}$?
$$
\left[
  \begin{matrix}
    \bf{a} & b & c \\
    d & \bf{e} & f \\
    g & h & \bf{i} \\
    j & k & l \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      b_{1} \\
      b_{2} \\
      b_{3} \\
      b_{4} \\
    \end{matrix}
  \right.
\right]
$$
- Since the last row could be zero with a non-zero constant, not for every $\vec{b}$ will have a solution.
## Question

Let $A$ be an $m\times n$ matrix with $m< n$ and let $\vec{b}$ in $\mathbb{R}^m$. Is $A\vec{x}=\vec{b}$ solvable *for all* vectors $\vec{b}$ in $\mathbb{R}^{m}$?
$$
\left[
  \begin{matrix}
    \bf{a} & b & c & d \\
    e & \bf{f} & g & h \\
    i & j & \bf{k} & l \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      b_{1} \\
      b_{2} \\
      b_{3} \\
    \end{matrix}
  \right.
\right]
$$
- There is a free variable, meaning infinitely many solutions.
## [[6 Homogeneous Linear Systems]]
