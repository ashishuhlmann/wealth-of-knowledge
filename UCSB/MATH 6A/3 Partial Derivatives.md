## 1/21/26
## Derivative in Real-Valued Functions

Let $f:U\subseteq\mathbb{R}\rightarrow\mathbb{R}$ be a real-valued function defined on an open set $U\subseteq\mathbb{R}$. The derivative of $f$ with respect to $x$ is a real-valued function variables defined
$$
\frac{df}{dx}=\lim_{h\rightarrow0}\frac{f(x+h)-f(x)}{h}
$$
Similarly, the derivative $f'(a)$ evaluated at a point $x=a$ is
$$
\frac{df}{dx}\biggr\lvert_{x=a} =\lim_{x\rightarrow a}\frac{f(x)-f(a)}{x-a}
$$

Let $f:U\subseteq\mathbb{R}^{m}\rightarrow\mathbb{R}$ be a real-valued function of $m$ variables $x_{1},x_{2},...x_{m}$ defined on an open set $U\subseteq\mathbb{R}^{m}$. The **partial derivative** of $f$ with respect to $x_{i}$ is a real-valued function of $m$ variables defined by
$$
\frac{\partial f}{\partial x_{i}}=\lim_{h\rightarrow 0}\frac{f(x_{1},...x_{i}+h,...x_{m})-f(f(x_{1},...x_{i},...x_{m})}{h}
$$
- treat any other variables as constants when differentiating
### Example

$$
\begin{align}
\frac{\partial}{\partial x}\frac{\sin{(xy^{2})}}{x^2+1}&=\frac{y^{2}\cos(xy^{2})(x^{2}+1)-2x\sin(xy^{2})}{(x^{2}+1)^2} \\

\frac{\partial}{\partial y}\frac{\sin{(xy^{2})}}{x^2+1}&=\frac{2xy\cos(xy^{2})}{x^{2}+1} \\
\end{align}
$$
## Gradient

Let $f:U\subseteq\mathbb{R}^{n}\rightarrow\mathbb{R}$ be a real valued function.
$$
\nabla_nF=
\begin{bmatrix}
\frac{\partial F}{\partial x_{1}} \\
\frac{\partial F}{\partial x_{2}} \\
\vdots \\
\frac{\partial F}{\partial x_{n}} \\
\end{bmatrix}
$$
### Example

Force Potential
$$
\vec{F}=-\nabla U
$$
Electric Field Potential
$$
\vec{E}=-\nabla V
$$
Magnetic Potential
$$
\vec{B}=\nabla\times\vec{A}
$$
## Jacobian Matrix

Let $\vec{F}:U\subseteq\mathbb{R}^{m}\rightarrow\mathbb{R}^{n}$ be a vector valued function.
- Remember, this is just a collection of $n$ real-valued functions of $m$ variables.

The **Jacobian matrix** of a vector-valued function is the matrix of all its first-order partial derivatives.
$$
D\vec{F}(\vec{x})=
\begin{bmatrix}
\frac{\partial F_{1}}{\partial x_{1}} & \frac{\partial F_{1}}{\partial x_{2}} & ... & \frac{\partial F_{1}}{\partial x_{m}} \\
\frac{\partial F_{2}}{\partial x_{1}} & \frac{\partial F_{2}}{\partial x_{2}} & ... & \frac{\partial F_{2}}{\partial x_{m}} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial F_{n}}{\partial x_{1}} & \frac{\partial F_{n}}{\partial x_{2}} & ... & \frac{\partial F_{n}}{\partial x_{m}} \\
\end{bmatrix}
$$
This can also be written as
$$
D\vec{F}(\vec{x})=
\begin{bmatrix}
\frac{\partial\vec{F}}{\partial x_{1}},\frac{\partial\vec{F}}{\partial x_{2}},...\frac{\partial\vec{F}}{\partial x_{m}}
\end{bmatrix}
$$
## Derivative Tensor

The **Kronecker tensor product** is a generalization of the **outer product** defined as
$$
\textbf{u}\otimes\textbf{v}=\textbf{u}\textbf{v}^{T_{n}}
$$
where $T_{n}$ is the transpose into one higher than the rank of $\textbf{u}$ and $\textbf{v}$.

For real-valued functions $f:U\subseteq\mathbb{R}^{n}\rightarrow\mathbb{R}$, the derivative tensors are:
1. first derivative:
$$
\nabla=
\begin{bmatrix}
\frac{\partial}{\partial x_{1}} \\
\frac{\partial}{\partial x_{2}} \\
\vdots \\
\frac{\partial}{\partial x_{n}} \\
\end{bmatrix}
$$
2. second derivative:
- The **hessian matrix** is the Jacobian of the gradient. It is also the gradient outer gradient.
$$
\nabla\otimes\nabla=
\begin{bmatrix}
\frac{\partial^{2}}{\partial x_{1}^{2}} & \frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{1}} & ... & \frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{1}} \\
\frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{2}} & \frac{\partial^{2}}{\partial x_{2}^{2}} & ... & \frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{2}} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{n}} & \frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{n}} & ... & \frac{\partial}{\partial x_{n}^{2}} \\
\end{bmatrix}
$$
3. third derivative:
- This is a three-dimensional block of elements. Going from one slice to another inward, it is
$$
\nabla\otimes\nabla\otimes\nabla=
\begin{bmatrix}
\frac{\partial^{3}}{\partial x_{1}^{3}} & \frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{1}} & ... & \frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{1}} \\
\frac{\partial^{2}}{\partial x_{1}^{2}}\frac{\partial}{\partial x_{2}} & \frac{\partial}{\partial x_{1}}\frac{\partial^{2}}{\partial x_{2}^{2}} & ... & \frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{2}} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial^{2}}{\partial x_{1}^{2}}\frac{\partial}{\partial x_{n}} & \frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{n}} & ... & \frac{\partial}{\partial x_{1}}\frac{\partial^{2}}{\partial x_{n}^{2}} \\
\end{bmatrix}
..
\begin{bmatrix}
\frac{\partial}{\partial x_{2}}\frac{\partial^{2}}{\partial x_{1}^{2}} & \frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{1}} & ... & \frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{1}} \\
\frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{2}} & \frac{\partial^{3}}{\partial x_{2}^{3}} & ... & \frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{2}} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{n}} & \frac{\partial^{2}}{\partial x_{2}^{2}}\frac{\partial}{\partial x_{n}} & ... & \frac{\partial}{\partial x_{2}}\frac{\partial^{2}}{\partial x_{n}^{2}} \\
\end{bmatrix}
...
\begin{bmatrix}
\frac{\partial}{\partial x_{n}}\frac{\partial^{2}}{\partial x_{1}^{2}} & \frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{1}} & ... & \frac{\partial^{2}}{\partial x_{n}^{2}}\frac{\partial}{\partial x_{1}} \\
\frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{2}} & \frac{\partial}{\partial x_{n}}\frac{\partial^{2}}{\partial x_{2}^{2}} & ... & \frac{\partial^{2}}{\partial x_{n}^{2}}\frac{\partial}{\partial x_{2}} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{1}}\frac{\partial}{\partial x_{n}} & \frac{\partial}{\partial x_{n}}\frac{\partial}{\partial x_{2}}\frac{\partial}{\partial x_{n}} & ... & \frac{\partial^{3}}{\partial x_{n}^{3}} \\
\end{bmatrix}
$$
4. $n$-th derivative
- This is a rank $n$ tensor.
$$
\nabla^{n}
$$
### In Two Variables
$$
\nabla\otimes\nabla=
\begin{bmatrix}
\frac{\partial^{2}}{\partial x^{2}} & \frac{\partial}{\partial y}\frac{\partial}{\partial x}\\
\frac{\partial}{\partial x}\frac{\partial}{\partial y} & \frac{\partial^{2}}{\partial y^{2}} \\
\end{bmatrix}
$$
### Third Derivative Tensor
$$
\nabla\otimes\nabla\otimes\nabla=
\begin{bmatrix}
\frac{\partial^{3}}{\partial x^{3}} & \frac{\partial}{\partial x}\frac{\partial}{\partial y}\frac{\partial}{\partial x} \\
\frac{\partial^{2}}{\partial x^{2}}\frac{\partial}{\partial y} & \frac{\partial}{\partial x}\frac{\partial^{2}}{\partial y^{2}}
\end{bmatrix}
..
\begin{bmatrix}
\frac{\partial}{\partial y}\frac{\partial^{2}}{\partial x^{2}} & \frac{\partial^{2}}{\partial y^{2}}\frac{\partial}{\partial x} \\
\frac{\partial}{\partial y}\frac{\partial}{\partial x}\frac{\partial}{\partial y} & \frac{\partial^{3}}{\partial y^{3}} \\
\end{bmatrix}
$$
## [[4 Differentiation]]