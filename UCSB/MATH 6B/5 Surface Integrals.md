## 4/20/26

**surface** - a function $\boldsymbol{\phi}:[a,b]\times[c,d]\rightarrow\mathbb{R}^{n}$ whose domain is a subset $[a,b]\times[c,d]\subseteq\mathbb{R}^{2}$.
- Any small portion of a surface looks like $\mathbb{R}^{2}$.
- Curves are parametrizations with one dummy variable. Surfaces are parametrizations with two dummy variables. 

In order to integrate a scalar or vector field across a surface, we need to parametrize the surface. A **parametrized surface** in $\mathbb{R}^{3}$ is a continuous mapping.
$$
\begin{align}
\boldsymbol{\phi}:D\subseteq\mathbb{R}^{2}\rightarrow\mathbb{R}^{3} \\
\boldsymbol{\phi}(
\begin{bmatrix}
u \\
v \\
\end{bmatrix}
)=
\begin{bmatrix}
\phi_{x}(\begin{bmatrix}u \\ v \\ \end{bmatrix}) \\
\phi_{y}(\begin{bmatrix}u \\ v \\ \end{bmatrix}) \\
\phi_{z}(\begin{bmatrix}u \\ v \\ \end{bmatrix}) \\
\end{bmatrix}
\end{align}
$$
### Example

The surface of the sphere is the set of all points $S$ where
$$
S=\{(x,y,z)\in\mathbb{R}^{3}|x^{2}+y^{2}+z^{2}=1\}
$$
To parametrize this surface, we can plug in spherical coordinates.
$$
\boldsymbol{\phi}(
\begin{bmatrix}
u \\
v \\
\end{bmatrix}
)=
\begin{bmatrix}
\cos{u}\sin{v} \\
\sin{u}\sin{v} \\
\cos{v} \\
\end{bmatrix}
$$
For the domain $[0,2\pi]\times[0,\pi]$, we will recover the whole sphere.

The normal vector to a surface can be computed by its two partial derivatives.
$$
\textbf{N}(
\begin{bmatrix}
u \\
v \\
\end{bmatrix}
)=
\frac{\partial\boldsymbol{\phi}}{\partial u}\times\frac{\partial\boldsymbol{\phi}}{\partial v}
$$
### Example

In order to find the tangent plane of
$$
\boldsymbol{\phi}(
\begin{bmatrix}
u \\
v \\
\end{bmatrix}
)=
\begin{bmatrix}
-4u \\
-2u^{2}+4v \\
-5v^{2}
\end{bmatrix}
$$
at $u=2$ and $v=1$, we will use the normal vector. The normal vector is orthogonal to the difference of any vector in the plane and the touching point.
$$
\biggr(
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
-
\boldsymbol{\phi}(
\begin{bmatrix}
u_{0} \\
v_{0} \\
\end{bmatrix}
)\biggr)\cdot
\textbf{N}(
\begin{bmatrix}
u_{0} \\
v_{0} \\
\end{bmatrix}
)=0
$$
$$
\textbf{N}(
\begin{bmatrix}
u \\
v \\
\end{bmatrix}
)=
\begin{bmatrix}
-4 \\
-4u \\
0 \\
\end{bmatrix}
\times
\begin{bmatrix}
0 \\
4 \\
-10v \\
\end{bmatrix}
=
\begin{bmatrix}
40uv \\
-40v \\
-16 \\
\end{bmatrix}
$$
$$
\boldsymbol{\phi}(
\begin{bmatrix}
2 \\
1 \\
\end{bmatrix}
)=
\begin{bmatrix}
-8 \\
-4 \\
-5
\end{bmatrix}
$$
$$
\biggr(
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
-
\boldsymbol{\phi}(
\begin{bmatrix}
2 \\
1 \\
\end{bmatrix}
)\biggr)\cdot
\textbf{N}(
\begin{bmatrix}
2 \\
1 \\
\end{bmatrix}
)=0
$$

We say that $\boldsymbol{\phi}$ is **smooth** iff
$$
\textbf{N}\neq\textbf{0}
$$
- $\boldsymbol{\phi}$ is **regular** if it is smooth at all points on its domain.

The elemental surface area of a surface is
$$
dA=\|\textbf{N}\|dudv
$$
and the elemental vectorized surface area is
$$
d\textbf{A}=\textbf{N}dudv
$$
## Scalar Fields (1st Type)

Let $\Omega:[a,b]\times[c,d]\rightarrow U\subseteq\mathbb{R}^{n}$ be a smooth surface in $U$, parametrized by $u$ and $v$, and let $f:U\subseteq\mathbb{R}^{n}\rightarrow\mathbb{R}$ be a real-valued function. The **surface integral** along $\Omega$ of $f$ is given by
$$
\int_{\Omega}fdA=\int_{c}^{d}\int_{a}^{b} f(\boldsymbol{\phi}(u,v))\|\frac{\partial\boldsymbol{\phi}}{\partial u}\times\frac{\partial\boldsymbol{\phi}}{\partial v}\|dudv
$$
## Vector Fields (2nd Type)

Now, let $\textbf{F}:U\subseteq\mathbb{R}^{n}\rightarrow\mathbb{R}^{n}$ be a vectorfield. The **flux** along $\Omega$ of $\textbf{F}$ is given by
$$
\int_{\Omega}\textbf{F}\cdot d\textbf{A}=\int_{c}^{d}\int_{a}^{b} \textbf{F}(\boldsymbol{\phi}(u,v))\cdot(\frac{\partial\boldsymbol{\phi}}{\partial u}\times\frac{\partial\boldsymbol{\phi}}{\partial v})dudv
$$
### Example

To find the surface area of a helicoid
$$
\boldsymbol{\phi}(
\begin{bmatrix}
u \\
v \\
\end{bmatrix}
)=
\begin{bmatrix}
u\cos{v} \\
u\sin{v} \\
v
\end{bmatrix}
$$
on the domain
$$
[0,1]\times[0,4\pi]
$$
we will integrate
$$
\int_{0}^{1}\int_{0}^{4\pi}\|\frac{\partial\boldsymbol{\phi}}{\partial u}\times\frac{\partial\boldsymbol{\phi}}{\partial v}\|dvdu=\int_{0}^{1}\int_{0}^{4\pi}\sqrt{1+u^{2}}dvdu
$$
We then substitute $u=\sinh{(\varphi)}$ and $du=\cosh{(\varphi)}d\varphi$ to get
$$
4\pi\int_{0}^{\sinh^{-1}{(1)}}\cosh^{2}{(\varphi)}d\varphi
$$
and finally
$$
\frac{\pi}{2}(e^{2\sinh^{-1}{(1)}}-e^{-2\sinh^{-1}{(1)}}+4\sinh^{-1}{(1)})
$$
## [[6 Stoke's Theorem]]