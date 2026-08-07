## 2/9/26

**curve** - a function $\vec{c}:[a,b]\rightarrow\mathbb{R}^{n}$ whose domain is a subset $[a,b]\subseteq\mathbb{R}$.
- Any small portion of a curve looks like $\mathbb{R}$.
- also known as a **parametrization** or **parametric representation**

**closed curve** - curve that begins and ends at the same point

**simple closed curve** - closed curve that does not intersect itself

A curve $\textbf{c}(t)$ is said to be **smooth** iff
- The derivative of its functions are all continuous and not simultaneously zero
- The curve does not cross over with itself.
### Example

Line
$$
\vec{r}(t)=\vec{a}+t\vec{v}
$$
### Example Parametrization
$$
\begin{align}
x^{2}(t)+y^{2}(t)=1 \\
x(t)+z(t)=1 \\
\end{align}
$$
$$
\begin{align}
x(t)=\cos(t) \\
y(t)=\sin(t) \\
z(t)=1-\cos(t) \\
\end{align}
$$
$$
\begin{align}
x^{2}+y^{2}+z^{2}=4 \\
x^{2}+z^{2}=1 \\
\end{align}
$$
$$
\begin{align}
x^{2}(t)+y^{2}(t)+z^{2}(t)=4 \\
x^{2}(t)+z^{2}(t)=1 \\
\end{align}
$$
$$
\begin{align}
x(t)=\cos(t) \\
y(t)=\pm\sqrt{3} \\
z(t)=\sin(t) \\
\end{align}
$$
$$
\begin{align}
\textbf{c}_{1}(t)=
\begin{bmatrix}
\cos(t) \\
\sqrt{3} \\
\sin(t)
\end{bmatrix}
\textbf{c}_{2}(t)=
\begin{bmatrix}
\cos(t) \\
-\sqrt{3} \\
\sin(t)
\end{bmatrix}
\end{align}
$$
$$
\begin{align}
x+y-z=2 \\
2x-5y+z=3 \\
\end{align}
$$
Choose a free variable $x(t)=t$
$$
\begin{align}
y-z=2-t \\
z-5y=3-2t \\
\end{align}
$$
$$
4y=3t-5
$$
$$
y(t)=\frac{3}{4}t-\frac{5}{4}
$$
$$
z(t)=\frac{7}{4}t-\frac{13}{4}
$$
$$
\begin{align}
\textbf{c}(t)=
t
\begin{bmatrix}
1 \\
\frac{3}{4} \\
\frac{7}{4} \\
\end{bmatrix}
+
\begin{bmatrix}
0 \\
-\frac{5}{4}  \\
-\frac{13}{4} \\
\end{bmatrix}
\end{align}
$$The **velocity** is the derivative of the curve
## [[8 Critical Points]]