## 2/23/26

**opporator** - takes in a function and outputs another function
- analagous to transformations on vectors or vector-valued functions
- **linearity** - satisfies $\boldsymbol{H}(af+bg)=a\boldsymbol{H}f+b\boldsymbol{H}g$  where $f$ and $g$ are functions and $a$ and $b$ are any constants
- if two opporators are linear, their composition is also linear

**differential opporator** $\boldsymbol{\partial}$ - oppporator that outputs the derivatives of a function
- $\boldsymbol{\partial}^{n}$ is taking a derivative $n$ times, or the $n$-th derivative
- linear and has standard $\infty\times\infty$ matrix
$$
\begin{bmatrix}
0 & 1 & 0 & 0 & ... \\
0 & 0 & 2 & 0 & ... \\
0 & 0 & 0 & 3 & ... \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
\end{bmatrix}
$$
- this matrix has eigenvectors $e^{rt}$ with corresponding eigenvalue $r$.

Any linear ODE can be written in opporator form
$$
\boldsymbol{L}=p_{0}(t)\boldsymbol{\partial}^{n}+p_{1}(t)\boldsymbol{\partial}^{n-1}+...+p_{n-1}(t)\boldsymbol{\partial}+p_{n}(t)
$$
so we are solving $\boldsymbol{L}y=g(t)$.
- The solutions $\boldsymbol{L}y_{c}=\boldsymbol{0}$ form a linear subspace of complex solutions.
- Use the Wronskian to test that the solutions are all linearly independent.
- The general solution $y$ is therefore the sum of the homogeneous solution of $\boldsymbol{L}y=0$ and the particular solution from [[6 Homogeneous Linear Systems]].
## [[16 Higher Order Linear ODE's]]