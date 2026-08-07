## 11/26/25

A **vector space** $V$ is a set of vectors equipped with addition and scalar mulitplication such that:
1. If $\vec{u},\vec{v}\in V$, then $\vec{u}+\vec{v}\in V$.
2. If $\vec{u},\vec{v}\in V$, then $\vec{u}+\vec{v}=\vec{v}+\vec{u}$.
3. If $\vec{u},\vec{v},\vec{w}\in V$, then $(\vec{u}+\vec{v})+\vec{w}=\vec{u}+(\vec{v}+\vec{w})$.
4. $\vec{0}\in V$ such that $\vec{u}+\vec{0}=\vec{0}+\vec{u}=\vec{u}\phantom{-}\forall \vec{u} \in V$.
5. For each $\vec{u}\in V$, $-\vec{u}\in V$ such that $\vec{u}+(-\vec{u})=\vec{0}$.
6. If $\vec{u}\in V$, then $c\vec{u}\in V$ for any scalar $c$.
7. If $\vec{u}\in V$, and $c,d$ are any scalars, $(c+d)\vec{u}=c\vec{u}+d\vec{u}$.
8. If $\vec{u}\in V$ and $c,d$ are any scalars, $c(d\vec{u})=(cd)\vec{u}$.
9. $1\vec{u}=\vec{u}\phantom{-}\forall \vec{u}\in V$

These are the properties of real Euclidean space $\mathbb{R}^{n}$.
## Coordinate Systems

Let $W\subset\mathbb{R}^{n}$ be a subspace of $\mathbb{R}^{n}$ and let $\beta=\{\vec{v_{1}},\vec{v_{2}},...,\vec{v_{p}}\}$ be a basis of $W$.
- Any vector in $W$ is a \mathbb{R}^{n}linear combination of the $\vec{v_{i}}$'s.
$$
\vec{x}=c_{1}\vec{v_{1}}+c_{2}\vec{v_{2}}+...+c_{p}\vec{v_{p}}
$$
- These scalars are called are *unique*.
### Proof

1. Let us say, that if there could be another linear combination for $\vec{x}$, then
$$
\begin{align}
\vec{x}&=c_{1}\vec{v_{1}}+c_{2}\vec{v_{2}}+...+c_{p}\vec{v_{p}} \\
\vec{x}&=d_{1}\vec{v_{1}}+d_{2}\vec{v_{2}}+...+d_{p}\vec{v_{p}} \\
\end{align}
$$
2. Subtract the equations.
$$
\vec{0} = (c_{1}-d_{1})\vec{v_{1}}+(c_{2}-d_{2})\vec{v_{2}}+...+(c_{p}-d_{p})\vec{v_{p}}
$$
3. We know all the $\vec{v_{i}}'$s are linearly independent because they form a basis of $W$. All the scalar subtractions must be zero, meaning 
$$
\begin{align}
c_{i}-d_{i}&=0\phantom{-}\forall i \\
c_{i}&=d_{i}\phantom{-}\forall i \\
\end{align}$$
4. Therefore, all linear combinations for a given vector in $\vec{x}\in W$ are unique.

Let $W$ be asubspace of $\mathbb{R}^{n}$ and let $\beta=\{\vec{v_{1}},\vec{v_{2}},...,\vec{v_{p}}\}$ be a basis of $W$.
- The unique scalars $c_{1},c_{2},...c_{p}$ such that $\vec{x}\in W$ is $\vec{x}=c_{1}\vec{v_{1}}+c_{2}\vec{v_{2}}+...+c_{p}\vec{v_{p}}$ are the **coordinates** of $\vec{x}$ in the basis $\beta$ or are **relative** to the basis $\beta$.
$$
[\vec{x}]_{\beta}=
\begin{bmatrix}
c_{1} \\
c_{2} \\
\vdots \\
c_{p} \\
\end{bmatrix}
$$
### Example Problem

$\text{Let }$
$$
\vec{v_{1}}=
\begin{bmatrix}
1 \\
1 \\
1 \\
\end{bmatrix}
\text{ and }\vec{v_{2}}=
\begin{bmatrix}
1 \\
2 \\
3 \\
\end{bmatrix}
$$$\text{Let }V=\text{span}\{\vec{v_{1}},\vec{v_{2}}\}$.
$\text{Is the vector}$
$$
\vec{x}=
\begin{bmatrix}
5 \\
7 \\
9 \\
\end{bmatrix}
\in V\text{ ? If so, find }[\vec{x}]_{V}.
$$
1. 
$$\text{The associated agumented matrix is:}$$
$$
\left[
  \begin{matrix}
	1 & 1 \\
	1 & 2 \\
	1 & 3 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		5 \\
		7 \\
		9 \\
    \end{matrix}
  \right.
\right]
$$
2. 
$$\text{The RREF is:}$$
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
		3 \\
		2 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
3. 
$$
\begin{align}
c_{1}=3 \\
c_{2}=2 \\
\end{align}
$$
$$
∴[\vec{x}]_{V}=
\begin{bmatrix}
3 \\
2 \\
\end{bmatrix}
$$
### Example Problem
$$
\vec{v_{1}}=
\begin{bmatrix}
1 \\
1 \\
3 \\
-1 \\
\end{bmatrix}
,\vec{v_{2}}=
\begin{bmatrix}
0 \\
-1 \\
2 \\
2 \\
\end{bmatrix}
,\vec{v_{3}}=
\begin{bmatrix}
4 \\
0 \\
1 \\
1 \\
\end{bmatrix}
$$
$\text{i. Show that }\beta=\{\vec{v_{1}},\vec{v_{2}},\vec{v_{3}}\}\text{ is a basis of }V=\text{span}\{\vec{v_{1}},\vec{v_{2}},\vec{v_{3}}\}.$
$\text{ii. Find a vector } \vec{x}\in V\text{ such that}$
$$
[\vec{x}]_{B}=
\begin{bmatrix}
2 \\
1 \\
-1 \\
\end{bmatrix}
$$
1. 
$$\text{Are }\vec{v_{1}},\vec{v_{2}}\text{, and }\vec{v_{3}}\text{ linearly independent? The associated augmented matrix is:}$$
$$
\left[
  \begin{matrix}
	1 & 0 & 4 \\
	1 & -1 & 0 \\
	3 & 2 & 1 \\
	-1 & 2 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		0 \\
		0 \\
		0 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
2. 
$$\text{The RREF is:}$$
$$
\left[
  \begin{matrix}
	1 & 0 & 0 \\
	0 & 1 & 0 \\
	0 & 0 & 1 \\
	0 & 0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		0 \\
		0 \\
		0 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
$$\text{The only solution is the trivial solution so }\vec{v_{1}},\vec{v_{2}}\text{, and }\vec{v_{3}}\text{ must be linearly independent.}$$
3. 
$$
∴\vec{v_{1}},\vec{v_{2}}\text{, and }\vec{v_{3}}\text{ form a basis for }V.
$$
$$
\vec{x}=2\vec{v_{1}}+1\vec{v_{2}}-1\vec{v_{3}}=
\begin{bmatrix}
-2 \\
1 \\
7 \\
-1 \\
\end{bmatrix}
$$
## [[12 Change of Basis]]