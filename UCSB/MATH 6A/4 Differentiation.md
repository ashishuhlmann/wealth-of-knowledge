## 1/23/26

- All regular derivatives apply. Use the gradient or Jacobian matrix as necessary to take a derivative.
- Dot and cross products work like the regular product rule.
## Linearization
### Real Valued Functions
$$
L(\vec{x})=f(\vec{a})+\nabla f|_{\vec{x}=\vec{a}}\cdot(\vec{x}-\vec{a})
$$
### Vector Valued Functions
$$
\vec{L}(\vec{x})=\vec{F}(\vec{a})+D\vec{F}|_{\vec{x}=\vec{a}}(\vec{x}-\vec{a})
$$

## Parabolic Approximation

### Real Valued Functions
$$
L(\vec{x})=f(\vec{a})+\nabla f|_{\vec{x}=\vec{a}}\cdot(\vec{x}-\vec{a})+(\nabla f|_{\vec{x}=\vec{a}}\cdot(\vec{x}-\vec{a}))^{2}
$$

$$
\begin{align}
f(x,y)+f_{x}(a,b)(x-a)+f_{y}(a,b)(y-b)+ \\
\frac{1}{2}f_{xx}(a,b)(x-a)^{2}+\frac{1}{2}f_{yy}(a,b)(y-b)^{2}+f_{xy}(a,b)(x-a)(y-b)
\end{align}
$$

### Vector Valued Functions
$$
\vec{L}(\vec{x})=\vec{F}(\vec{a})+D\vec{F}|_{\vec{x}=\vec{a}}(\vec{x}-\vec{a})
$$

## Taylor Series

$$
\frac{1}{0!}f(\textbf{a})+\frac{1}{1!}(\textbf{x}-\textbf{a})_{i}\nabla f(\textbf{a})_{i}+(\textbf{x}-\textbf{a})_{i}(\nabla\otimes\nabla f(\textbf{a}))_{ij}(\textbf{x}-\textbf{a})_{j}+(\nabla\otimes\nabla\otimes\nabla f(\textbf{a}))_{ijk}(\textbf{x}-\textbf{a})_{i}(\textbf{x}-\textbf{a})_{j}(\textbf{x}-\textbf{a})_{k}+...
$$
$$
\frac{1}{0!}\vec{F}(\vec{a})+\frac{1}{1!}D\vec{F}|_{\vec{x}=\vec{a}}(\vec{x}-\vec{a})+\frac{1}{2!}(\vec{x}-\vec{a})^{T}D^{2}\vec{F}|_{\vec{x}=\vec{a}}(\vec{x}-\vec{a})
$$
### Example
$$
f(x,y)=e^{xy}
$$
$$
\nabla f=
\begin{bmatrix}
ye^{xy} \\
xe^{xy} \\
\end{bmatrix}
$$
$$
\nabla\otimes\nabla f=
\begin{bmatrix}
y^{2}e^{xy} & (xy+1)e^{xy} \\
(xy+1)e^{xy} & x^{2}e^{xy} \\
\end{bmatrix}
$$
$$
\nabla\otimes\nabla\otimes\nabla f=
\begin{bmatrix}
y^{3}e^{xy} & y(xy+2)e^{xy} \\
y(xy+2)e^{xy} & x(xy+2)e^{xy} \\
\end{bmatrix}
..
\begin{bmatrix}
y(xy+2)e^{xy} & x(xy+2)e^{xy} \\
x(xy+2)e^{xy} & x^{3}e^{xy} \\
\end{bmatrix}
$$
$$
T_{3}(x,y)=
\frac{1}{0!}f(0,0)
+
\frac{1}{1!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\nabla f(0,0)
+
\frac{1}{2!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\biggr(\nabla\otimes\nabla f(0,0)\biggr)
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
+
\frac{1}{3!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\biggr(\nabla\otimes\nabla\otimes\nabla f(0,0)\biggr)
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
\otimes
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
$$
$$
=\frac{1}{0!}e^{0\cdot0}
+
\frac{1}{1!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\begin{bmatrix}
0e^{0\cdot0} \\
0e^{0\cdot0} \\
\end{bmatrix}
+
\frac{1}{2!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\begin{bmatrix}
0^{2}e^{0\cdot0} & (0\cdot0+1)e^{0\cdot0} \\
(0\cdot0+1)e^{0\cdot0} & 0^{2}e^{0\cdot0} \\
\end{bmatrix}
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
+
\frac{1}{3!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\biggr(
\begin{bmatrix}
y^{3}e^{xy} & y(xy+2)e^{xy} \\
y(xy+2)e^{xy} & x(xy+2)e^{xy} \\
\end{bmatrix}
..
\begin{bmatrix}
y(xy+2)e^{xy} & x(xy+2)e^{xy} \\
x(xy+2)e^{xy} & x^{3}e^{xy} \\
\end{bmatrix}
\biggr)
\begin{bmatrix}
x^{2} & xy \\
yx & y^{2} \\
\end{bmatrix}
$$
$$
=1+0+
\frac{1}{2!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\begin{bmatrix}
0 & 1 \\
1 & 0 \\
\end{bmatrix}
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
+
\frac{1}{3!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\biggr(
\begin{bmatrix}
x^{2} & yx \\
\end{bmatrix}
\begin{bmatrix}
y^{3}e^{xy} & y(xy+2)e^{xy} \\
y(xy+2)e^{xy} & x(xy+2)e^{xy} \\
\end{bmatrix}
+
\begin{bmatrix}
xy & y^{2} \\
\end{bmatrix}
\begin{bmatrix}
y(xy+2)e^{xy} & x(xy+2)e^{xy} \\
x(xy+2)e^{xy} & x^{3}e^{xy} \\
\end{bmatrix}
\biggr)
$$
$$
=1+
\frac{1}{2!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\begin{bmatrix}
y \\
x \\
\end{bmatrix}
+
\frac{1}{3!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\biggr(
\begin{bmatrix}
x^{2}y^{3}e^{xy} + xy^{2}(xy+2)e^{xy} \\
x^{2}y(xy+2)e^{xy} + x^{2}y(xy+2)e^{xy} \\
\end{bmatrix}
+
\begin{bmatrix}
y(xy+2)e^{xy} & x(xy+2)e^{xy} \\
x(xy+2)e^{xy} & x^{3}e^{xy} \\
\end{bmatrix}
\begin{bmatrix}
xy \\
y^{2} \\
\end{bmatrix}
\biggr)
$$
$$

$$
### Example
$$
f(x,y)=e^{xy}
$$
$$
\nabla f=
\begin{bmatrix}
ye^{xy} \\
xe^{xy} \\
\end{bmatrix}
$$
$$
\nabla\otimes\nabla f=
\begin{bmatrix}
y^{2}e^{xy} & (xy+1)e^{xy} \\
(xy+1)e^{xy} & x^{2}e^{xy} \\
\end{bmatrix}
$$
$$
\nabla\otimes\nabla\otimes\nabla f=
\begin{bmatrix}
y^{3}e^{xy} & y(xy+2)e^{xy} \\
y(xy+2)e^{xy} & x(xy+2)e^{xy} \\
\end{bmatrix}
..
\begin{bmatrix}
y(xy+2)e^{xy} & x(xy+2)e^{xy} \\
x(xy+2)e^{xy} & x^{3}e^{xy} \\
\end{bmatrix}
$$
$$
T_{3}(x,y)=
\frac{1}{0!}f(0,0)
+
\frac{1}{1!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\nabla f(0,0)
+
\frac{1}{2!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\biggr(\nabla\otimes\nabla f(0,0)\biggr)
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
+
\frac{1}{3!}
\begin{bmatrix}
x & y \\
\end{bmatrix}
\biggr(\nabla\otimes\nabla\otimes\nabla f(0,0)\biggr)
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
\otimes
\begin{bmatrix}
x \\
y \\
\end{bmatrix}
$$
## [[5 Coordinate Systems]]

