## 10/23/25
## The Standard Basis
$$
\text{span}\{
\begin{bmatrix}
1 \\
0 \\
0 \\
\end{bmatrix}
,
\begin{bmatrix}
0 \\
1 \\
0 \\
\end{bmatrix}
,
\begin{bmatrix}
0 \\
0 \\
1 \\
\end{bmatrix} \}
=\mathbb{R}^{3}
$$
$$
\text{span}\{
\begin{bmatrix}
1 \\
0 \\
\end{bmatrix}
,
\begin{bmatrix}
0 \\
1 \\
\end{bmatrix}
 \}
=\mathbb{R}^{2}
$$

Let 
$$
\vec{e_{1}}=
\begin{bmatrix}
1 \\
0 \\
\vdots \\
0 \\
\end{bmatrix}
,
\vec{e_{2}}=
\begin{bmatrix}
0 \\
1 \\
\vdots \\
0 \\
\end{bmatrix}
,...
\vec{e_{n}}=
\begin{bmatrix}
0 \\
0 \\
\vdots \\
1 \\
\end{bmatrix}
$$
$$
\text{span}\{\vec{e_{1}}, \vec{e_{2}},...\vec{e_{n}}\}=\mathbb{R}^{n}
$$
$\vec{e_{1}}, \vec{e_{2}},...\vec{e_{n}}$ are linearly independent and are the standard basis of $\mathbb{R}^{n}$.

Let $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$ be a linear transformation.
1. We say that $T$ is onto or subject if for all $\vec{b}\in\mathbb{R}^{m}$ there exists *at least* one vector $\vec{x}\in\mathbb{R}^{n}$ such that $T(\vec{x})=\vec{b}$.
2. We say that $T$ is one to one or injective if for all $\vec{b}\in\mathbb{R}^{m}$ there exists *at most* one vector in $\mathbb{R}^{n}$ such that $T(\vec{x})=\vec{b}$
3. We say that $T$ is bijective if $T$ is both onto and one to one.
### Example

Consider the projection transformation $T:\mathbb{R}^{2}\rightarrow\mathbb{R}^{2}$:
$$T(
\begin{bmatrix}
x_{1} \\
x_{2} \\
\end{bmatrix})=
\begin{bmatrix}
x_{1} \\
0 \\
\end{bmatrix}
$$
- $T$ is not onto because there is no vector such that
$$T(
\begin{bmatrix}
x_{1} \\
x_{2} \\
\end{bmatrix})=
\begin{bmatrix}
0 \\
1 \\
\end{bmatrix}
$$
- $T$ is not one to one because there exists two vectors in the domain that get mapped to the same vector in the codomain
$$T(
\begin{bmatrix}
1 \\
2 \\
\end{bmatrix})=
T(
\begin{bmatrix}
1 \\
3 \\
\end{bmatrix})=
\begin{bmatrix}
1 \\
0 \\
\end{bmatrix}
$$
### Question

Let T Rn to Rm be a linear transformation such that only the zero vector in Rn gets mappe dto the zero vector in Rm. Is T one to one?
### Example Problem
$$
A=
\begin{bmatrix}
1 & 3 & 5 & 7 \\
3 & 5 & 7 & 9 \\
5 & 7 & 9 & 3 \\
\end{bmatrix}
$$
Is T one to one?
Is T onto?

**Theorem** Let $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$ be a linear transformation with standard matrix $A$.
1. $T$ is one to one iff $A\vec{x}=\vec{0}$ has a unique solution.
	- The columns of $A$ are linearly independent.
	- The RREF of $A$ has a pivot position in every column (meaning it has no free variables).
2. $T$ is onto iff the RREF of $A$ has a leading one in every row
	- The columns of $A$ span $\mathbb{R}^{m}$.
	- Every vector b Rm is a linear combination of the columns

**Remark**: T Rn to Rm be a linear transformation with standard matrix A mxn.
1. If n>m, T cannot be one to one
2. If n<m, T cannot be onto.
3. If n=m, check for one to one. T is either bijective or nothing. Both or nothing
## Linearity

A transformation $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$ is **linear** iff:
1. $T(\vec{u}+\vec{v})=T(\vec{u})+T(\vec{v})\forall\vec{u},\vec{v}\in\mathbb{R}^{n}$
2. $T(c\vec{u}=cT(\vec{u})\forall\vec{u}\in\mathbb{R}^{n},c$

In general, $T$ preserves *all* linear combinations of any vectors.
### Example
$$
T:\mathbb{R}^{2}\rightarrow\mathbb{R}^{2}
$$
$$
\begin{bmatrix}
x_{1} \\
x_{2} \\
\end{bmatrix}
\rightarrow
\begin{bmatrix}
x_{1}+2x_{2} \\
x_{2}
\end{bmatrix}
$$
1. Linear
### Example
$$
T:\mathbb{R}^{3}\rightarrow\mathbb{R}^{2}
$$
$$
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
\end{bmatrix}
\rightarrow
\begin{bmatrix}
x_{1}^{2} \\
0 \\
\end{bmatrix}
$$
1. Not a linear transformation
### Example

Let $A$ be an $m\times n$ matrix. Then the function $T:\mathbb{R}^{n}\rightarrow\mathbb{R}^{m}$ defined by $T(\vec{x})=A\vec{x}$ is a linear transformation.
1. Linear

The zero vector in any linear transformation gets mapped to the zero vector.
$$
T:\mathbb{R}^{m}\rightarrow\mathbb{R}^{n}
$$

$$
T(\vec{0})=\vec{0}
$$
*Note: The zero vectors above do not have the same dimension.*
## Types of Linear Transformations

$$T(\vec{x})=r\vec{x}$$
1. Dilation: $1<r$
2. Contraction: $0<r<1$

## [[Common Linear Transformations]]
### Example Problem

$\text{Let }T:\mathbb{R}^{2}\rightarrow\mathbb{R}^{2}\text{ be a linear transformation.}$ 
$$
T(
\begin{bmatrix}
1 \\
0 \\
\end{bmatrix}
)=
\begin{bmatrix}
4 \\
0 \\
\end{bmatrix}
,
T(
\begin{bmatrix}
0 \\
1 \\
\end{bmatrix}
)=
\begin{bmatrix}
3 \\
1 \\
\end{bmatrix}
$$
$\text{What is}$
$$
T(
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
) ?
$$
1. 
$$
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
=x
\begin{bmatrix}
1 \\
0 \\
\end{bmatrix}
+y
\begin{bmatrix}
0 \\
1 \\
\end{bmatrix}
$$
2. 
$$
T(
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
)=x
\begin{bmatrix}
4 \\
0 \\
\end{bmatrix}
+y
\begin{bmatrix}
3 \\
1 \\
\end{bmatrix}
$$
$$
\text{by definition of linear transformations.}
$$
$$
∴T(
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
)=
\begin{bmatrix}
4 & 3 \\
0 & 1 \\
\end{bmatrix}
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
$$

**Theorem**: Let $T:\mathbb{R}^{m}\rightarrow\mathbb{R}^{n}$ be a linear transformation.
- For any vector $\vec{x}\in\mathbb{R}^{m}$, $T(\vec{x})=A\vec{x}$ when $A=[T(\vec{e_{1}}), T(\vec{e_{2}}),...T(\vec{e_{m}})]$.
- *Every* linear transformation has a standard matrix.
- The **standard matrix** of $T$ is the matrix representation of a linear transformation.
### Example Problem

$\text{Let } T:\mathbb{R}^{3}\rightarrow\mathbb{R}^{2} \text{ be a linear transformation given by:}$
$$
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
\rightarrow
\begin{bmatrix}
x-y+2z \\
4y+3z \\
\end{bmatrix}
$$
$\text{i. Show that } T \text{ is linear.}$
$\text{ii. Find its standard matrix.}$
1. 
$$
\text{Let }\vec{u},\vec{v}\in\mathbb{R}^{3}\text{ and } c\in\mathbb{R}
$$
$$
T(
\begin{bmatrix}
u_{x} \\
u_{y} \\
u_{z} \\
\end{bmatrix}
+
\begin{bmatrix}
v_{x} \\
v_{y} \\
v_{z} \\
\end{bmatrix}
)=T(
\begin{bmatrix}
u_{x}+v_{x} \\
u_{y}+v_{y} \\
u_{z}+v_{z} \\
\end{bmatrix}
)=
\begin{bmatrix}
(u_{x}+v_{x})-(u_{y}+v_{y})+2(u_{z}+v_{z}) \\
4(u_{y}+v_{y})+3(u_{z}+v_{z}) \\
\end{bmatrix}
$$
$$
=
\begin{bmatrix}
u_{x}+v_{x}-u_{y}-v_{y}+2u_{z}+2v_{z} \\
4u_{y}+4v_{y}+3u_{z}+3v_{z} \\
\end{bmatrix}
=
\begin{bmatrix}
u_{x}-u_{y}+2u_{z} \\
4u_{y}+3u_{z} \\
\end{bmatrix}
+
\begin{bmatrix}
v_{x}-v_{y}+2v_{z} \\
4v_{y}+3v_{z} \\
\end{bmatrix}
$$
$$
=
T(
\begin{bmatrix}
u_{x} \\
u_{y} \\
u_{z} \\
\end{bmatrix}
)+T(
\begin{bmatrix}
v_{x} \\
v_{y} \\
v_{z} \\
\end{bmatrix}
)
$$
2. 
$$
T(c
\begin{bmatrix}
u_{x} \\
u_{y} \\
u_{z} \\
\end{bmatrix}
)=
\begin{bmatrix}
cu_{x}-c_u{y}+2cu_{z} \\
4cu_{y}+3cu_{z} \\
\end{bmatrix}
=c
\begin{bmatrix}
u_{x}-_u{y}+2u_{z} \\
4u_{y}+3u_{z} \\
\end{bmatrix}
=cT(
\begin{bmatrix}
u_{x} \\
u_{y} \\
u_{z} \\
\end{bmatrix}
)
$$
3. 
$$
\begin{bmatrix}
x-y+2z \\
4y+3z \\
\end{bmatrix}
=x
\begin{bmatrix}
1 \\
0 \\
\end{bmatrix}
+y
\begin{bmatrix}
-1 \\
4 \\
\end{bmatrix}
+z
\begin{bmatrix}
2 \\
3 \\
\end{bmatrix}
$$
$$
∴T=
\begin{bmatrix}
1 & -1 & 2 \\
0 & 4 & 3  \\
\end{bmatrix}
$$
### Example Problem

$\text{Let } T:\mathbb{R}^{3}\rightarrow\mathbb{R}^{3} \text{ be a linear transformation given by:}$
$$
T(
\begin{bmatrix}
1 \\
1 \\
0 \\
\end{bmatrix}
)=
\begin{bmatrix}
2 \\
0 \\
-1 \\
\end{bmatrix}
,\phantom{-}
T(
\begin{bmatrix}
0 \\
1 \\
1 \\
\end{bmatrix}
)=
\begin{bmatrix}
0 \\
1 \\
0 \\
\end{bmatrix}
,\phantom{-}
T(
\begin{bmatrix}
1 \\
0 \\
1 \\
\end{bmatrix}
)=
\begin{bmatrix}
1 \\
-3 \\
2 \\
\end{bmatrix}
$$
$\text{Find its standard matrix.}$
1. 
$$
\text{Let }\vec{v_{1}}=
\begin{bmatrix}
1 \\
1 \\
0 \\
\end{bmatrix}
,\vec{v_{2}}=
\begin{bmatrix}
0 \\
1 \\
1 \\
\end{bmatrix}
,\vec{v_{3}}=
\begin{bmatrix}
1 \\
0 \\
1 \\
\end{bmatrix}
$$
2. 
$$
\left[
  \begin{matrix}
    1 & 0 & 1 \\
    1 & 1 & 0 \\
    0 & 1 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      1 \\
      0 \\
      0 \\
    \end{matrix}
  \right.
\right]
\xrightarrow{\text{RREF}}
\left[
  \begin{matrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      1/2 \\
      -1/2 \\
      1/2 \\
    \end{matrix}
  \right.
\right]
$$
$$
\left[
  \begin{matrix}
    1 & 0 & 1 \\
    1 & 1 & 0 \\
    0 & 1 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      1 \\
      0 \\
    \end{matrix}
  \right.
\right]
\xrightarrow{\text{RREF}}
\left[
  \begin{matrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      1/2 \\
      1/2 \\
      -1/2 \\
    \end{matrix}
  \right.
\right]
$$
$$
\left[
  \begin{matrix}
    1 & 0 & 1 \\
    1 & 1 & 0 \\
    0 & 1 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0 \\
      0 \\
      1 \\
    \end{matrix}
  \right.
\right]
\xrightarrow{\text{RREF}}
\left[
  \begin{matrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      -1/2 \\
      1/2 \\
      1/2 \\
    \end{matrix}
  \right.
\right]
$$
$$
\text{The standard basis vectors can be written as:}
$$
$$
\begin{align}
\boldsymbol{\hat{x}}=1/2\vec{v_{1}}-1/2\vec{v_{2}}+1/2\vec{v_{3}} \\
\boldsymbol{\hat{y}}=1/2\vec{v_{1}}+1/2\vec{v_{2}}-1/2\vec{v_{3}} \\
\boldsymbol{\hat{z}}=-1/2\vec{v_{1}}+1/2\vec{v_{2}}+1/2\vec{v_{3}}
\end{align}
$$
3. 
$$
\text{Since } T \text{ is linear,}
$$
$$
\begin{align}
T(\boldsymbol{\hat{x}})=1/2
\begin{bmatrix}
2 \\
0 \\
-1 \\
\end{bmatrix}
-1/2
\begin{bmatrix}
0 \\
1 \\
0 \\
\end{bmatrix}
+1/2
\begin{bmatrix}
1 \\
-3 \\
2 \\
\end{bmatrix}
=
\begin{bmatrix}
3/2 \\
-2 \\
1/2 \\
\end{bmatrix} \\
T(\boldsymbol{\hat{y}})=1/2
\begin{bmatrix}
2 \\
0 \\
-1 \\
\end{bmatrix}
+1/2
\begin{bmatrix}
0 \\
1 \\
0 \\
\end{bmatrix}
-1/2
\begin{bmatrix}
1 \\
-3 \\
2 \\
\end{bmatrix}
=
\begin{bmatrix}
1/2 \\
-1 \\
-3/2 \\
\end{bmatrix} \\
T(\boldsymbol{\hat{z}})=-1/2
\begin{bmatrix}
2 \\
0 \\
-1 \\
\end{bmatrix}
+1/2
\begin{bmatrix}
0 \\
1 \\
0 \\
\end{bmatrix}
+1/2
\begin{bmatrix}
1 \\
-3 \\
2 \\
\end{bmatrix}
=
\begin{bmatrix}
-1/2 \\
-1 \\
3/2 \\
\end{bmatrix} \\
\end{align}
$$
$$
∴T=
\begin{bmatrix}
3/2 & 1/2 & -1/2 \\
0 & 4 & 3  \\
\end{bmatrix}
$$
## [[9 Matrix Algebra]]