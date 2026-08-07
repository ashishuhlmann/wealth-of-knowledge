## 4/29/26

**Stoke's theorem** is a generalization of Green's theorem.

**Theorem**: Stoke's

Let $A$ be a closed and bounded region in $\mathbb{R}^{n}$ whose boundary $\textbf{c}$ is a piecewise smooth simple closed curve. Let $\textbf{F}$ be a vectorfield on $A$. Then, with *any* surface $A$ inside that boundary,
$$
\oint_{\textbf{c}}\textbf{F}\cdot d\textbf{s}=\int\int_{A}(\nabla\times\textbf{F})\cdot d\textbf{A}
$$
- looking from the tip of the normal vectors to the surface, the boundary should be oriented counterclockwise
- An **orientation** of a surface $S\in\mathbb{R}^{3}$ is a continuous choice of unit normal vector as $p$ varies over $S$.
- If the surface is closed, there is no boundary curve and the integral is zero.
### Example

Let
$$
\textbf{F}(
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
)=
\begin{bmatrix}
z^{3} \\
x^{3}-y^{3} \\
y^{3} \\
\end{bmatrix}
$$
and surface $\textbf{S}$ be given by $x^{2}+y^{2}+z^{2}=1$ on $z\geq0$ with outward normal. We will verify Stoke's theorem. The first part is given by
$$
\textbf{c}(t)=
\begin{bmatrix}
\cos{(t)} \\
\sin{(t)} \\
0 \\
\end{bmatrix}
$$
$$
\oint_{\textbf{c}}\textbf{F}\cdot d\textbf{s}=
\int_{0}^{2\pi}
\begin{bmatrix}
0 \\
\cos^{3}{(t)}-\sin^{3}{(t)} \\
\sin^{3}{(t)} \\
\end{bmatrix}
\cdot
\begin{bmatrix}
\sin{(t)} \\
-\cos{(t)} \\
0
\end{bmatrix}
dt
$$
which results in
$$
\int_{0}^{2\pi}-\cos^{4}{(t)}+\cos{(t)}\sin^{3}{(t)} dt=\frac{-3\pi}{4}
$$
The second part is given by
$$
\Omega(
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
$$
\int\int_{A}(\nabla\times\textbf{F})\cdot d\textbf{A}=\int_{0}^{2\pi}\int_{0}^{\frac{\pi}{2}}(\nabla\times\textbf{F}(\Omega))\cdot(\frac{\partial\Omega}{\partial u}\times\frac{\partial\Omega}{\partial v})dvdu
$$
$$
\nabla\times\textbf{F}=
\begin{bmatrix}
3y^{2} \\
3z^{2} \\
3x^{2} \\
\end{bmatrix}
=
\begin{bmatrix}
3\sin^{2}{(u)}\sin^{2}{(v)} \\
3\cos^{2}{(v)} \\
3\cos^{2}{(u)}\sin^{2}{(v)} \\
\end{bmatrix}
$$
$$
(\frac{\partial\Omega}{\partial u}\times\frac{\partial\Omega}{\partial v})dvdu=
\begin{bmatrix}
-\cos{(u)}\sin^{2}{(v)} \\
-\cos{(v)}\sin{(u)}\sin{(v)} \\
-\cos^{2}{(v)}\sin^{2}{(u)} - \cos^{2}{(u)}\cos{(v)}\sin{(v)} \\
\end{bmatrix}
dvdu
$$
$$
\int_{0}^{2\pi}\int_{0}^{\frac{\pi}{2}}
-3\cos{(u)}\sin^{2}{(u)}\sin^{4}{(v)}
-3\cos^{3}{(v)}\sin{(u)}\sin{(v)}
-3\sin^{2}{(u)}\cos^{2}{(u)}\cos^{2}{(v)}\sin^{2}{(v)} -3\cos^{4}{(u)}\cos{(v)}\sin^{3}{(v)}
dvdu
$$
## [[2 Gauss' Law]]