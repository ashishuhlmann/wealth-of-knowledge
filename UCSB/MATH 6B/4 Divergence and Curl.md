## 4/13/26

The **divergence** of a vectorfield describes how much it acts like a source or sink.
$$
\nabla\cdot\textbf{F}
$$
- positive for source-like places
- negative for sink-like places
- An **incompressable** vectorfield has zero divergence.

The **curl** of a vectorfield describes how much it circulates.
$$
\nabla\times\textbf{F}
$$
- This is another vector field.
- An **irrotational** vectorfield has zero curl.
- Curl is only defined in $\mathbb{R}^{3}$ and $\mathbb{R}^{7}$.
### Properties

1. $\nabla\cdot\textbf{E}_{1}+\textbf{E}_{2})=\nabla\cdot\textbf{E}_{1}+\nabla\cdot\textbf{E}_{2}$
2. $\nabla\cdot c\textbf{E}=c\nabla\cdot\textbf{E}$
3. $\nabla\cdot(\varphi\textbf{E})=\varphi\nabla\cdot\textbf{E}+\textbf{E}\cdot\nabla\varphi$
4. $\nabla\cdot\nabla$ is the **Laplacian**.
5. $\nabla\times\textbf{E}_{1}+\textbf{E}_{2})=\nabla\times\textbf{E}_{1}+\nabla\times\textbf{E}_{2}$
6. $\nabla\times c\textbf{E}=c\nabla\times\textbf{E}$
7. $\nabla\times(\varphi\textbf{E})=\varphi\nabla\times\textbf{E}+\textbf{E}\times\nabla\varphi$
8. $\nabla\cdot(\nabla\times\textbf{E})=0$
9. $\nabla\times(\nabla\times\textbf{E})=\nabla(\nabla\cdot\textbf{E})-(\nabla\cdot\nabla)\textbf{E}$

**Theorem**: Green (2-D case of Stoke's theorem)

In the 2-D case, we can take the cross product analogy for curl:
$$
\begin{vmatrix}
\frac{\partial}{\partial x} & F_{x}\\
\frac{\partial}{\partial y} & F_{y}\\
\end{vmatrix}
$$
to get
$$
\oint_{\textbf{c}}\textbf{F}\cdot d\textbf{s}=\int\int_{A}(\frac{\partial F_{y}}{\partial x}-\frac{\partial F_{x}}{\partial y})dA
$$
- To compute the area inside a curve, choose a $P$ and $Q$ such that the right expression of the derivatives is equal to one.
### Example

To verify Green's Theorem for the expression
$$
\int_{\textbf{c}}(2x^{3}-y^{3})dx+(x^{2}+y^{3})dy
$$
where
$$
\textbf{c}(t)=
\begin{bmatrix}
\cos(t) \\
\sin(t) \\
\end{bmatrix}
$$
on $0\leq t\leq2\pi$.

First, we will verify the left hand side. Let us substitute
$$
\begin{bmatrix}
dx \\
dy \\
\end{bmatrix}
=
\textbf{c}'(t)dt=
\begin{bmatrix}
-\sin{(t)} \\
\cos{(t)} \\
\end{bmatrix}
dt
$$
$$
\int_{0}^{2\pi}(2\cos^{3}{(t)}-\sin^{3}{(t)})(-\sin{(t)})+(\cos^{2}{(t)}+\sin^{3}{(t)})(\cos{t})dt
$$
to get $\frac{3\pi}{2}$. Next, we will verify the right hand side.
$$
\int_{A}\frac{\partial}{\partial x}(x^{2}+y^{3})-\frac{\partial}{\partial x}(2x^{3}+y^{3})dA=\int_{A}(2x+3y^{2})dA
$$
Let us use the polar jacobian $|DT_{x}^{\theta}|=rdrd\theta$.
$$
\int_{0}^{2\pi}\int_{0}^{1}(2\cos{(\theta)+3\sin^{2}{(\theta)}})rdrd\theta=\frac{3\pi}{2}
$$
The theorem is verified.
## Midterm Recap

- gradient vector field
- flow line 
- 1st and 2nd type of path integration
- fundamental theorem
- judgement of gradient (4 equivalent statements)
- Green's theorem
## [[5 Surface Integrals]]