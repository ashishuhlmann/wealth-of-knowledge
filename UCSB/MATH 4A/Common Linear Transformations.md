## The $n\times n$ Identity Matrix

$$
I_{n}=
\begin{bmatrix}
1 & 0 & ... & 0 \\
0 & 1 & ... & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & ... & 1
\end{bmatrix}
$$
- the do nothing matrix
## Rotation Matrix
$$
R:\mathbb{R}^{2}\rightarrow\mathbb{R}^{2}
$$
$$
R=
\begin{bmatrix}
\cos(\theta) & -\sin(\theta) \\
\sin(\theta) & \cos(\theta) \\
\end{bmatrix}
$$
- *Note: All circles centered on the origin remain unchanged under this transformation.*
$$
R_{x},R_{y},R_{z}:\mathbb{R}^{3}\rightarrow\mathbb{R}^{3}
$$
$$
R_{x}=
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos(\alpha) & -\sin(\alpha) \\
0 & \sin(\alpha) & \cos(\alpha) \\
\end{bmatrix}
,\phantom{-}
R_{y}=
\begin{bmatrix}
\cos(\beta) & 0 & -\sin(\beta) \\
0 & 1 & 0 \\
\sin(\beta) & 0 & \cos(\beta)
\end{bmatrix}
,\phantom{-}
R_{z}=
\begin{bmatrix}
\cos(\alpha) & -\sin(\alpha) & 0 \\
\sin(\alpha) & \cos(\alpha) & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
- *Note: All spheres centered on the origin remain unchanged under this transformation.*
## Hyperbolic Rotation Matrix

$$
R:\mathbb{R}^{2}\rightarrow\mathbb{R}^{2}
$$
$$
R=
\begin{bmatrix}
\cosh(\varphi) & \sinh(\varphi) \\
\sinh(\varphi) & \cosh(\varphi) \\
\end{bmatrix}
$$