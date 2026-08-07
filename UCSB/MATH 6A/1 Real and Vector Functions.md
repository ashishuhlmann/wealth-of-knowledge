## 1/12/26
## Open Sets

An **open ball** $B(\vec{a},r)\subseteq\mathbb{R}^n$ with center $\vec{a}$ and radius $r>0$ is the set of all points $\vec{x}\in\mathbb{R}^n$ whose distance from the fixed point $\vec{a}$ is exclusively smaller than $r$.
$$
B(\vec{a},r)=\{\vec{x}\in\mathbb{R}^{n}|\|\vec{x}-\vec{a}\|<r\}
$$
An **open set** is a subset $U\subseteq\mathbb{R}^{n}$ if for every point $\vec{a}\in U$  
there exists a real number $\epsilon>0$ such that the open ball $B(\vec{a},\epsilon)$ is contained in $U$.

For the following definitions, we will asume $U$ is an open set.

**real valued function** - a function of $m$ variables whose domain is a subset $U\subseteq\mathbb{R}^{m}$ such that $m\geq 1$ and whose range is contained in $\mathbb{R}^{n}$ if $n=1$.

**vector valued functions** - a function of $m$ variables if $n>1$
### Examples

Distance  $f:\mathbb{R}^{3}\rightarrow\mathbb{R}^{1}$
$$
f(
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix})=\
\sqrt{x^{2}+y^{2}+z^{2}}
$$

Projection $\vec{F}:\mathbb{R}^{3}\rightarrow\mathbb{R}^{2}$
$$
\vec{F}(
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
)=
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
$$
**vector field** - a vector-valued function $\vec{F}:U\subseteq\mathbb{R}^{m}\rightarrow\mathbb{R}^{m}$ defined on a subset $U\subseteq\mathbb{R}^{m}$
## Multivariable Functions

A **real valued function of** $n$ **variables** $f:U\subseteq\mathbb{R}^{n}\rightarrow\mathbb{R}^{1}$ is the set
$$
\{(x_{1},x_{2},...x_{n},y)|y=f(x_{1},x_{2},...x_{n})\text{ for some }(x_{1},x_{2},...x_{n})\in U\}\in\mathbb{R}^{n+1}
$$
where $U\subseteq \mathbb{R}^{n}$.
- a **level set** is the set of all points in the domain $U$ on which $f$ has a constant value.
$$
\{(x_{1},x_{2},...x_{n})\in U|f(x_{1},x_{2},...x_{n})=c\}
$$
## [[2 Limits and Continuity]]