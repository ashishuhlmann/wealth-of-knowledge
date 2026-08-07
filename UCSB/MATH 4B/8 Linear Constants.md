## 1/28/26
$$
ay''+by'+cy=d
$$
- If $y_{s}$ is a solution, then $y$ is also a solution iff $y_{h}=y-y_{s}$ is a solution to the *homogeneous equation* $ay''+by'+cy=0$.
- If $y_{1}$ and $y_{2}$ are both solutions, then any linear combination of the two is also a solution.
- Furthermore, all solutions are exactly the linear combinations of two *linearly independent* functions.
### Homogenous Constant Equations
$$
ay''+by'+cy=0
$$
Let $y_{c}=e^{\lambda t}$ for some constant $\lambda$.
$$
a\lambda^{2}y+b\lambda y + cy=0
$$
We can factor and divide out by $y$ knowing it is never zero.
$$
(a\lambda^{2}+b\lambda  + c)y=0
$$
The **characteristic polynomial** is 
$$
a\lambda^{2}+b\lambda  + c=0
$$
All solutions can be formed by the following basis
$$
\begin{align}
y_{1}=e^{\lambda_{1} t} \\
y_{2}=e^{\lambda_{2} t} \\
\end{align}
$$
and are written as
$$
y=c_{1}e^{\lambda_{1}t}+c_{2}e^{\lambda_{2}t}
$$
### Repeated Roots

If the characteristic polynomial of a second order ODE has a repeated root, then it has the form
$$
y''-2\lambda y'+\lambda^{2}y=0
$$
If $\lambda=0$, then $y''=0$, or $y=at+b$. If $\lambda\neq0$, then $y=e^{\lambda t}$ is a solution. 

Let $u=ye^{-\lambda t}$, or $y=ue^{\lambda t}$. That means that
$$
y'=e^{\lambda t}u'+\lambda e^{\lambda t}u
$$
and
$$
y''=e^{\lambda t}u''+2\lambda e^{\lambda t}u'+\lambda^{2}e^{\lambda t}u
$$
Then,
$$
y''-2\lambda y'+\lambda^{2}y=e^{\lambda t}u''
$$
Using the original differential equation, we can see that  $u''=0$ since
$e^{\lambda t}\neq0$.
$$
u=at+b
$$
So
$$
y=(at+b)e^{\lambda t}
$$
All solution can be formed by the following basis 
$$
\begin{align}
y_{1}=e^{\lambda t} \\
y_{2}=te^{\lambda t} \\
\end{align}
$$
and are written as
$$
y=c_{1}e^{\lambda t}+c_{2}te^{\lambda t} \\
$$
### Complex Roots

If $\lambda=\alpha+\boldsymbol{i}\beta$, where $\beta\neq0$, then then all solutions can be formed by the following basis through
$$
\begin{align}
y_{1}=e^{\alpha t}\cos{(\beta t)} \\
y_{2}=e^{\alpha t}\sin{(\beta t)} \\
\end{align}
$$
and are written as
$$
y=e^{\alpha t}(c_{1}\cos{(\beta{t})}+c_{2}\sin{(\beta{t})})
$$
### Example
$$
y''+y=0
$$
$$
\lambda^{2}+1=0
$$
$$
\lambda=\pm \boldsymbol{i}
$$
$$
\begin{align}
y_{1}(t)=\cos{t} \\
y_{2}(t)=\sin{t} \\
\end{align}
$$
## Initial Value Problems
$$
y=c_{1}e^{\lambda_{1} t}+c_{1}e^{\lambda_{2} t}
$$
$$
\begin{align}
y(0)=c_{2} +c_{2} \\
y'(0)=\lambda_{1}c_{1}+\lambda_{2}c_{2}\\
\end{align}
$$
$$
\begin{bmatrix}
1 & 1 \\
\lambda_{1} & \lambda_{1} \\
\end{bmatrix}
\begin{bmatrix}
c_{1} \\
c_{2} \\
\end{bmatrix}
=
\begin{bmatrix}
y(0) \\
y'(0) \\
\end{bmatrix}
$$
- If this matrix is non-singular, then the IVP has a unique solution.
### Example
$$
y''-5y'+3y=0
$$
$$
\begin{align}
y(0)=0 \\
y'(0)=1 \\
\end{align}
$$
$$
\lambda^{2}-5\lambda+3=0
$$
$$
\begin{bmatrix}
1 & 1 \\
\frac{5+\sqrt{13}}{2} & \frac{5-\sqrt{13}}{2} \\
\end{bmatrix}
\begin{bmatrix}
c_{1} \\
c_{2} \\
\end{bmatrix}
=
\begin{bmatrix}
0 \\
1 \\
\end{bmatrix}
$$
$$
\begin{bmatrix}
\frac{5-\sqrt{13}}{-2\sqrt{13}} & \frac{1}{\sqrt{13}} \\
\frac{5+\sqrt{13}}{2\sqrt{13}} & \frac{1}{-\sqrt{13}} \\
\end{bmatrix}
\begin{bmatrix}
0 \\
1 \\
\end{bmatrix}
=
\begin{bmatrix}
c_{1} \\
c_{2} \\
\end{bmatrix}
$$
$$
y=\frac{1}{\sqrt{13}}e^{\frac{5+\sqrt{13}}{2}t}-\frac{1}{\sqrt{13}}e^{\frac{5-\sqrt{13}}{2}t}
$$
## [[9 Wronskian Matrix]]






