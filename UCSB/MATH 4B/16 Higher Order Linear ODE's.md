## 2/25/26
$$
y^{(n)}+a_{1}(t)y^{(n-1)}+...+a_{n}y=0
$$
High order linear differential equations still follow the EUT if
- The coefficient of the highest derivative is one.
- All the coefficients are continuous.

Abel's formula still works from [[10 Application of the Wronskian]].
- The Wronskian is either *identically zero* or *never zero*.
### General Characteristic Roots

If a particular root is repeated $n$ times, the homogenous solutions will take the form
$$
\begin{align}
y_{1}&=e^{\lambda t} \\
y_{2}&=te^{\lambda t} \\
&\vdots \\
y_{n}&=t^{n-1}e^{\lambda t} \\
\end{align}
$$
If there is a pair of complex conjugate roots $\alpha\pm\beta\boldsymbol{i}$, the homogenous solutions will take the form
$$
\begin{align}
y_{1}&=e^{\alpha t}\cos{(\beta t)} \\
y_{2}&=e^{\alpha t}\sin{(\beta t)} \\
\end{align}
$$
If there are complex conjugate roots $\alpha\pm\beta\boldsymbol{i}$ repeated $n$ times,
$$
\begin{align}
y_{1a}&=e^{\alpha t}\cos{(\beta t)} \\
y_{1b}&=e^{\alpha t}\sin{(\beta t)} \\
y_{2a}&=te^{\alpha t}\cos{(\beta t)} \\
y_{2b}&=te^{\alpha t}\sin{(\beta t)} \\
&\vdots \\
y_{na}&=t^{n-1}e^{\alpha t}\cos{(\beta t)} \\
y_{nb}&=t^{n-1}e^{\alpha t}\sin{(\beta t)} \\
\end{align}
$$
### Example
$$
y''''+2y''+y=0
$$
$$
\begin{align}
\lambda^{4}+2\lambda^{2}+1=0 \\
(\lambda^{2}+1)^{2}=0 \\
\end{align}
$$The root is $0\pm\boldsymbol{i}$ with multiplicity two.
$$
\begin{align}
y_{1a}&=\cos{(\beta t)} \\
y_{1b}&=\sin{(\beta t)} \\
y_{2a}&=t\cos{(\beta t)} \\
y_{2b}&=t\sin{(\beta t)} \\
\end{align}
$$
### Wronskian 

The **Vandermonde matrix** is the Wronskian matrix of these homogeneous solutions evaluated at $t=0$.
$$
W(0)=
\begin{bmatrix}
1 & 1 & ... & 1 \\
\lambda_{1} & \lambda_{2} & ... & \lambda_{n} \\
\vdots & \vdots & \ddots & \vdots \\
\lambda_{1}^{n-1} & \lambda_{2}^{n-1} & ... & \lambda_{n}^{n-1} \\
\end{bmatrix}
$$
The **Vandermonde determinant** is equal to $\Pi(\lambda_{i}-\lambda_{j})$ where $1\leq i<j\leq n$. These are all the upper triangular indicies.
### Example Problem

$$
y''''-y'''-y''+y'=0
$$
$$
\begin{align}
y(0)&=0 \\
y'(0)&=0 \\
y''(0)&=1 \\
y'''(0)&=0 \\
\end{align}
$$
$$
\begin{align}
\lambda^{4}-\lambda^{3}-\lambda^{2}+\lambda=0 \\
\lambda(\lambda^{3}-\lambda^{2}-\lambda+1) \\
\lambda(\lambda-1)^{2}(\lambda+1) \\
\end{align}
$$
$$
\begin{align}
y_{1}&=1 \\
y_{2}&=e^{-t} \\
y_{3}&=e^{t} \\
y_{4}&=te^{t} \\
\end{align}
$$
$$
\begin{align}
y(0)&=c_{1}+c_{2}+c_{3} \\
y'(0)&=-c_{2}+c_{3}+c_{4} \\
y''(0)&=c_{2}+c_{3}+2c_{4} \\
y'''(0)&=-c_{2}+c_{3}+3c_{4} \\
\end{align}
$$
## Non-Homogeneous Cases

All solutions are still sums of the homogeneous solution and the particular solution.
### Variation of Parameters

For higher order non-homogeneous linear differential equations, variation of parameters extends to
$$
\begin{bmatrix}
y_{1} & y_{2} & ... & y_{n} \\
y_{1}' & y_{2}' & ... & y_{n}' \\
\vdots & \vdots & \ddots &\vdots \\
y_{1}^{(n-1)} & y_{2}^{(n-1)} & ... & y_{n}^{(n-1)} \\
\end{bmatrix}
\begin{bmatrix}
u_{1}' \\
u_{2}' \\
\vdots \\
u_{n}' \\
\end{bmatrix}
=
\begin{bmatrix}
0 \\
0 \\
\vdots \\
r(t) \\
\end{bmatrix}
$$
- Solve for $u_{i}'$ and integrate. The final form will again be
$$
y=y_{1}u_{1}+y_{2}u_{2}+...+y_{n}u_{n}
$$
### Example Problem

$\text{Solve all the solutions of the differential equation.}$
$$
y'''-2y''+y'=t
$$
1. $$\text{The characteristic polynomial is}$$
$$
\lambda(\lambda-1)^{2}=0
$$
$$\text{and gives complementary solutions}$$
$$
\begin{align}
y_{1}&=1 \\
y_{2}&=e^{t} \\
y_{3}&=te^{t} \\
\end{align}
$$
2. 
$$
\begin{bmatrix}
1 & e^{t} & te^{t} \\
0 & e^{t} & (t+1)e^{t} \\
0 & e^{t} & (t+2)e^{t} \\
\end{bmatrix}
\begin{bmatrix}
u_{1}' \\
u_{2}' \\
u_{3}' \\
\end{bmatrix}
=
\begin{bmatrix}
0 \\
0 \\
t \\
\end{bmatrix}
$$
3. $$\text{Calculate the last row of the inverse Wronskian.}$$
$$
\left[
  \begin{matrix}
	1 & e^{t} & te^{t} \\
	0 & e^{t} & (t+1)e^{t} \\
	0 & e^{t} & (t+2)e^{t} \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0  \\
      0  \\
      1  \\
    \end{matrix}
  \right.
\right]
$$
$$R_{3}-R_{2}$$
$$
\left[
  \begin{matrix}
	1 & e^{t} & te^{t} \\
	0 & e^{t} & (t+1)e^{t} \\
	0 & 0 & e^{t} \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      0  \\
      0  \\
      1  \\
    \end{matrix}
  \right.
\right]
$$
$$R_{1}-R_{2}+R_{3}$$
$$
\left[
  \begin{matrix}
	1 & 0 & 0 \\
	0 & e^{t} & (t+1)e^{t} \\
	0 & 0 & e^{t} \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      1  \\
      0  \\
      1  \\
    \end{matrix}
  \right.
\right]
$$
$$R_{2}-(t+1)R_{3}$$
$$
\left[
  \begin{matrix}
	1 & 0 & 0 \\
	0 & e^{t} & 0 \\
	0 & 0 & e^{t} \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      1  \\
      -(t+1)  \\
      1  \\
    \end{matrix}
  \right.
\right]
$$
$$\div$$
$$
\left[
  \begin{matrix}
	1 & 0 & 0 \\
	0 & 1 & 0 \\
	0 & 0 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
      1  \\
      -(t+1)e^{-t}  \\
      e^{-t}  \\
    \end{matrix}
  \right.
\right]
$$
4. 
$$
\begin{bmatrix}
u_{1}' \\
u_{2}' \\
u_{3}' \\
\end{bmatrix}
=
\begin{bmatrix}
... & ... & 1 \\
... & ... & -(t+1)e^{-t} \\
... & ... & e^{-t} \\
\end{bmatrix}
\begin{bmatrix}
0 \\
0 \\
t \\
\end{bmatrix}
=
\begin{bmatrix}
t \\
-t(t+1)e^{-t} \\
te^{-t} \\
\end{bmatrix}
$$
$$
y=\int tdt+\int-t(t+1)e^{-t}dt(e^{t})+\int te^{-t}dt(te^{t})
$$
$$
y=\frac{t^{2}}{2}+(t^{2}+3t+3)-t(t+1)+c_{1}+c_{2}e^{t}+c_{3}te^{t}
$$
$$
y=\frac{t^{2}}{2}+2t+c_{1}+c_{2}e^{t}+c_{3}te^{t}
$$
## [[17 Systems of First Order Linear ODE's]]