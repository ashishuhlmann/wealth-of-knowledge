## 1/16/26
## Epsilon Delta Defintion

A function $f:U\subseteq\mathbb{R}\rightarrow\mathbb{R}$ has a limit $L$ as $x$ approaches $a$
$$
\lim_{x\rightarrow a}=L
$$ iff for any given number $\epsilon>0$ there is a number $\delta>0$ such that
$$
0<|x-a|<\delta\Rightarrow 0<|f(x)-L|<\epsilon
$$

The **limit of a multivariable function** $f:U\subseteq\mathbb{R}^{m}\rightarrow\mathbb{R}$ has a limit $L$ as $\vec{x}$ approaches $\vec{a}$
$$
\lim_{x\rightarrow a}f(\vec{x})=L
$$
iff for given number $\epsilon>0$ there is a number $\delta>0$ such that $\vec{x}\in U$ and
$$
0< ||\vec{x}-\vec{a}||<\delta\Rightarrow|f(\vec{x})-L|<\epsilon
$$There are infintely many ways to approach $\vec{a}$.
- For the limit to exist, you must prove that *every* direction has the same limit
- To show the limit does not exist, you only need to show two directions that don't have the same limit.
### Example

$$
\lim_{(x,y)\rightarrow(0,0)}\frac{2xy}{2x^{2}+y^{2}}
$$
### Example

$$
\lim_{(x,y)\rightarrow(0,0)}\frac{x^{2}y}{x^{2}-y^{2}}
$$


The **limit of a vector-valued function**
$$
\vec{F}(\vec{x})=
\begin{bmatrix}
F_{1}(\vec{x}) \\
F_{2}(\vec{x}) \\
\vdots \\
F_{n}(\vec{\vec{x}}) \\
\end{bmatrix}
$$has a limit $\vec{L}$ as $\vec{x}$ approaches $\vec{a}$ 
$$
\lim_{\vec{x}\rightarrow\vec{a}}\vec{F}(x)=\vec{L}
$$ iff
$$
\begin{align}
\lim_{\vec{x}\rightarrow\vec{a}}\vec{F_{1}}(\vec{x})=L_{1} \\
\lim_{\vec{x}\rightarrow\vec{a}}\vec{F_{2}}(\vec{x})=L_{2} \\
\vdots\phantom{--} \\
\lim_{\vec{x}\rightarrow\vec{a}}\vec{F_{n}}(\vec{x})=L_{n} \\
\end{align}
$$
### Example

$$
\vec{F}(\vec{x})=
\begin{bmatrix}
\frac{e^{2t}-1}{t} \\
\frac{t^{3}}{t^{4}-t^{3}} \\
\frac{\sin{3t}}{t} \\
\end{bmatrix}
$$
## [[3 Partial Derivatives]]