## 2/18/26

**critical point** - if all of the partial derivatives are zero or at least one is undefined

A function has a local minimum or maximum if
$$
\nabla f=\textbf{0}
$$

Suppose the second partial derivatives of $f:\mathbb{R}^{n}\rightarrow\mathbb{R}$ are continuous on an open ball with center $(a, b)$. and suppose that $\nabla f (a, b) = \vec{0}$. Recall that

$$
D=
\begin{vmatrix}
f_{xx} & f_{xy} \\
f_{yx} & f_{yy} \\
\end{vmatrix}
f_{xx}(a,b)f_{yy}(a,b)-f_{xy}^{2}(a,b)
$$
is called the Hessian of $f$ or $\nabla^{T}\nabla f$

- If $D>0$, and $f_{xx}>0$, then it is a local minimum
- If $D>0$, and $f_{xx}<0$, then it is a local maximum
- If $D<0$, it is nont a local maxmium or minimum

**closed set** - set containing *all* boundary points

**bounded set** - a set that is contained within a ball
## [[9 Contrained Optimization]]
