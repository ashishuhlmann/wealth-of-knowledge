## 1/5/26

An **ordinary differential equation (ODE)** is an equation involving an independent variable $t$ and a dependent variable $y$ in the form
$$
F(t,y,y',y'',...y^{(n)})=0
$$
where $n\geq 1$ and $F$ is a multivariable function.

A **parital differential equation (PDE)** is an equation involving partial derivatives of a multivariable function $y$ with multiple independent variables.
### Examples

- exponential population growth
$$
\frac{dP}{dt}=kP
$$
- logistic population growth
$$
\frac{dP}{dt}=kP(1-\frac{P}{L})
$$
- damped harmic oscillator
$$
m\frac{d^{2}x}{dt^{2}}+c\frac{dx}{dt}+kx=0
$$
A **system of differential equations** is when there are two or more functions on the same indepedent variables
### Examples

$$
\begin{equation}
\left\{ \begin{aligned} 
  x'&=ax+by \\
  y'&=cx+dy \\
\end{aligned} \right.
\end{equation}
$$
$$
\frac{d^{2}\vec{r}}{dt^{2}}=-\frac{GM}{|\vec{r}|^{3}}\vec{r}
$$
- a vector differential equation involves multiple components and can be split up into a system of differential equations

**order** - the highest derivative present in a differential equation
## Linear Differential Equations

**linear differential equation** - a differential equation in a linear form with derivatives of $y$ were the coefficients are any functions of $t$.
$$
a_{0}(t)y^{(n)}+a_{1}(t)y^{(n-1)}+...+a_n(t)y=g(t)
$$
- If $g(t)=0$, the equation is **homogenous**.
- Nonlinear differential equations contain terms of more complicated expressions like squares, trigonometry, or exponents.
### Examples

$$y'=\frac{-t+\sqrt{t^{2}-16y}}{2}$$
- nonlinear
$$my''=mg-k(y')^{2}$$
- nonlinear
$$t^{2}y''+ty'+2y=e^{t}$$
- linear, not homogenous
## Existence and Uniqueness

For first order differential equations, there is no algorithm to give explicit solutions.
$$
y'=f(t,y)
$$
**direction field** - vector field with directions pointing with the slope
- given an initial value problem $y'=f(t,y)$ and $y(t_{0})=y_{0}$, the directionfield provide a flow where an object in the field has to go along with the assigned direction
- the intial condition gives a starting place for the solution

**Theorem:** existence and uniqueness
- Suppose $f$ and $\frac{\partial f}{\partial y}$ are both continuous in a rectangular region $a<t_{0}<b$, $c<y_{o}<d$ on the $ty$ plane. Then for every point $(t_{0},y_{0})$ in that region, there is a *local* interval $(t_{0}-h,t_{0}+h)$ in which the solution to the IVP exists uniquely.
- If $f$ and $\frac{\partial f}{\partial y}$ are continuous for all $y$, a *global* solution to the IVP exists uniquely.
### Example
$$
y'+ty=\sin{t}
$$
$$
y'=f(t,y)=\sin{t}-ty
$$
- $f(t,y)$ is continuous on the whole $ty$ plane. Therefore, the existence and uniqueness theorem ensures a unique local solution for every intial condition $(t_{0},y_{0})$.
## Example

$$
y'=\frac{t+y}{t-y}
$$
- Here, $f(t,y)$ is continuous except for the line $y=t$. Therefore the existence and uniqueness theorem ensures a unique local solution for every $(t_{0},y_{0})$ such that $y\neq t$.
## [[2 Solving Differential Equation]]