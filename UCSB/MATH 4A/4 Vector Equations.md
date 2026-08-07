## 10/7/25
## Vectors

Denote the $n$-dimensional **real Euclidean space** with $\mathbb{R}^{n}$
- an $n\times1$ matrix is a **column vector** of size $n$
- $\mathbb{R}^{n}$ is the set of all vectors of size $n$ with real entries
- **parallelogram law of vector addition**
- the **zero vector** $\vec{0}$ in $\mathbb{R}^{n}$ is
$$
\begin{bmatrix}
0 \\
0 \\
\vdots \\
0 \\
\end{bmatrix}
$$
## Properties of Euclidean Space $\mathbb{R}^n$ 
1. Commutativity
	$\vec{u}+\vec{v}=\vec{v}+\vec{u}$
2. Associativity
	$(\vec{u}+\vec{v})+\vec{w}=\vec{v}+(\vec{u}+\vec{w})$
3. Zero
	$\vec{u}+\vec{0}=\vec{u}$
4. Inverse
	$\vec{u}+-\vec{u}=\vec{0}$
5. Distributivity of Constants
	$c(\vec{u}+\vec{v})=c\vec{u}+c\vec{v}$
6. Distributivity of Vectors
	$(c+d)\vec{u}=c\vec{u}+d\vec{u}$
7. Scalar Multiplication
	$c(d\vec{u})=(cd)\vec{u}$
8. Multaplicative Identity
	$1\vec{v}=\vec{v}$

A **linear combination of vectors** $\vec{v_{1}},\vec{v_{2}},...\vec{v_{n}}\in\mathbb{R}^{n}$ is another vector of the form
$$
c_{1}\vec{v_{1}}+c_{2}\vec{v_{2}}+...+c_{n}\vec{v_{n}}\phantom{-}c_{i}\in\mathbb{R}\forall i
$$
### Example

$$
\begin{align}
\text{Let }\vec{v_{1}}\text{ and }\vec{v_{2}}\in\mathbb{R}^{n}\text{.}
\end{align}
$$
- $2\vec{v_{1}}+\vec{v_{2}}$ is a linear combination of $\vec{v_{1}}\text{ and }\vec{v_{2}}$.
- $\vec{0}$ is also a linear combination of $\vec{v_{1}}\text{ and }\vec{v_{2}}$

A **vector equation** is an equation of the form $$c_{1}\vec{v_{1}}+c_{2}\vec{v_{2}}+...+c_{n}\vec{v_{n}}=\vec{u}$$
has a solution iff the following augmented matrix is consistent.
$$
\left[
  \begin{matrix}
    \vec{v_{1}} & \vec{v_{2}} & ... & \vec{v_{n}} \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      \vec{u} \\
    \end{matrix}
  \right.
\right]
$$
## Spans and Spanning Sets

Let $\vec{v_{1}},\vec{v_{2}},...\vec{v_{m}}\in\mathbb{R}^{n}$. The **span** of $\vec{v_{1}},\vec{v_{2}},...\vec{v_{m}}$ is a **subset** of $\mathbb{R}^{n}$ consisting of all the vectors that are linear combinations of $\vec{v_{1}},\vec{v_{2}},...\vec{v_{m}}$.
$$
\text{span}\{\vec{v_{1}},\vec{v_{2}},...\vec{v_{n}}\}
=
\{c_{1}\vec{v_{1}}+c_{2}\vec{v_{2}}+...+c_{n}\vec{v_{n}}\phantom{-}\forall c_{i}\in\mathbb{R}\}
$$
### Example Problem

$\text{Find the equation of the plane spanned by the vectors}$
$$
\begin{bmatrix}
1 \\
1 \\
1 \\
\end{bmatrix}
\text{, and }
\begin{bmatrix}
2 \\
1 \\
0 \\
\end{bmatrix}
$$
1. 
$$\text{Let }x,y,z\in\mathbb{R}$$
$$
c_{1}
\begin{bmatrix}
1 \\
1 \\
1 \\
\end{bmatrix}
+ c_{2}
\begin{bmatrix}
2 \\
1 \\
0 \\
\end{bmatrix}
=
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
$$
2. 
$$\text{The associated augmented matrix is:}$$
$$
\left[
  \begin{matrix}
    1 & 2 \\
    1 & 1 \\
    1 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      x \\
      y \\
      z \\
    \end{matrix}
  \right.
\right]
$$
3. 
$$
R_{2}-R_{3}
$$

$$
\left[
  \begin{matrix}
    1 & 2 \\
    0 & 1 \\
    1 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      x \\
      y-z \\
      z \\
    \end{matrix}
  \right.
\right]
$$
4. 
$$
R_{1}-2R_{2}
$$
$$
\left[
  \begin{matrix}
    1 & 0 \\
    0 & 1 \\
    1 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      x-2y+2z \\
      y-z \\
      z \\
    \end{matrix}
  \right.
\right]
$$
5. 
$$
R_{3}-R_{1}
$$
$$
\left[
  \begin{matrix}
    1 & 0 \\
    0 & 1 \\
    0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      x-2y+2z \\
      y-z \\
      -x+2y-z \\
    \end{matrix}
  \right.
\right]
$$
6. 
$$\text{In order for the system to be consistent,}$$
$$
x-2y+z=0
$$

$$∴\text{In order for the vector }
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
\in\text{span}
\{
\begin{bmatrix}
1 \\
1 \\
1 \\
\end{bmatrix}
,
\begin{bmatrix}
2 \\
1 \\
0 \\
\end{bmatrix}
\},
\phantom{-}
x-2y+z=0$$
### Example Problem

$\text{Find the equation for the space spanned by the vectors}$
$$
\begin{bmatrix}
1 \\
3 \\
0 \\
2 \\
\end{bmatrix}
\text{, and }
\begin{bmatrix}
0 \\
1 \\
1 \\
1 \\
\end{bmatrix}
$$
1. 
$$\text{Let }x,y,z\in\mathbb{R}$$
$$
c_{1}
\begin{bmatrix}
1 \\
3 \\
0 \\
2 \\
\end{bmatrix}
+ c_{2}
\begin{bmatrix}
0 \\
1 \\
1 \\
1 \\
\end{bmatrix}
=
\begin{bmatrix}
x \\
y \\
z \\
w \\
\end{bmatrix}
$$
2. 
$$\text{The associated augmented matrix is:}$$
$$
\left[
  \begin{matrix}
    1 & 0 \\
    3 & 1 \\
    0 & 1 \\
    2 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      x \\
      y \\
      z \\
      w \\
    \end{matrix}
  \right.
\right]
$$
3. 
$$
R_{2}-3R_{1}
$$
$$
\left[
  \begin{matrix}
    1 & 0 \\
    0 & 1 \\
    0 & 1 \\
    2 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      x \\
      y-3x \\
      z \\
      w \\
    \end{matrix}
  \right.
\right]
$$
4. 
$$
R_{4}-2R_{1}
$$
$$
\left[
  \begin{matrix}
    1 & 0 \\
    0 & 1 \\
    0 & 1 \\
    0 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      x \\
      y-3x \\
      z \\
      w-2x \\
    \end{matrix}
  \right.
\right]
$$
5. 
$$
R_{3}-R_{2}
$$
$$
\left[
  \begin{matrix}
    1 & 0 \\
    0 & 1 \\
    0 & 0 \\
    0 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      x \\
      y-3x \\
      3x-y+z\\
      w-2x \\
    \end{matrix}
  \right.
\right]
$$
6. 
$$
R_{4}-R_{2}
$$
$$
\left[
  \begin{matrix}
    1 & 0 \\
    0 & 1 \\
    0 & 0 \\
    0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      x \\
      y-3x \\
      3x-y+z\\
      x-y+w \\
    \end{matrix}
  \right.
\right]
$$
7. 
$$\text{In order for the system to be consistent,}$$
$$
\begin{align}
3x-y+z=0 \\
x-y+w=0 \\
\end{align}
$$
$$
∴\text{In order for the vector }
\begin{bmatrix}
x \\
y \\
z \\
w \\
\end{bmatrix}
\in\text{span}\{
\begin{bmatrix}
1 \\
3 \\
0 \\
2 \\
\end{bmatrix}
,
\begin{bmatrix}
0 \\
1 \\
1 \\
1 \\
\end{bmatrix}
\},\phantom{-}
4x-2y+z+w=0
$$
## [[5 Matrix Equations]]