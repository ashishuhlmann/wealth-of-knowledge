## 4/8/26

Let $\textbf{F}=\nabla f$ be a gradient vector field on $U\subseteq\mathbb{R}^{n}$. Let $\textbf{c}:[a,b]\rightarrow U$ be a piecewise path. Then
$$
\int_{\textbf{c}}\textbf{F}\cdot d\textbf{s}=f(\textbf{c}(b))-f(\textbf{c}(a))
$$
this can be written as
$$
\int_{\textbf{c}}\nabla f\cdot d\textbf{s}=f(\textbf{c}(b))-f(\textbf{c}(a))
$$
- $f$ is called a **potential function**.
## Conservative Forces

A force $\textbf{F}(\textbf{x})$ is a **conservative** force iff it can be written as the negative of a gradient vectorfield of some potential function $U(\textbf{x})$.
- The change in energy of some path only depends on the endpoints.
### Four Equivalent Statments

**Theorem**: conservative and liberal forces

For a conservative vectorfield $\textbf{F}$ on $U\subseteq\mathbb{R}^{n}(n=2,3)$, the following conditions are equivalent:
1. For any piecewise simple closed curve
$$
\oint_{\textbf{c}}\textbf{F}\cdot d\textbf{s}=0
$$
2. For any two piecewise oriented simple curves $\textbf{c}_{1}$ and $\textbf{c}_{2}$ with the same intial and final point,
$$
\oint_{\textbf{c}_{1}}\textbf{F}\cdot d\textbf{s}=\oint_{\textbf{c}_{2}}\textbf{F}\cdot d\textbf{s}
$$
3. $\textbf{F}$ is a gradient vectorfield with a defined potential function. In physics, the potential energy is the negative of the potential function.
4. The **curl** (or curl analogies) of $\textbf{F}$ is zero.
$$
\nabla\times\textbf{F}=\nabla\times(\nabla f)=0
$$
In general, when dealing with $\mathbb{R}^{2}$, we can just augment the space with an extra zero component to take cross products.
## [[4 Divergence and Curl]]