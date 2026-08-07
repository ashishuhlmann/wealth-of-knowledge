## 2/10/26
## Mass on a Spring

The differential equation for a mass on a spring is
$$
m\ddot{x}+kx=0
$$
where $m,k>0$ are the positive mass and spring constant, respectively. It has a characteristic polynomial
$$
m\lambda^{2}+k=0
$$
The polynomial has solutions where we can define the **angular frequency** $\omega_{0}$.
$$
\lambda=\pm\boldsymbol{i}\sqrt{\frac{k}{m}}=\pm\boldsymbol{i}\omega_{0}
$$
where
$$
\omega_{0}=\sqrt{\frac{k}{m}}
$$
From [[8 Linear Constants]], we can characterize all the solutions by two linearly independent functions with the following intial conditions.
$$
x(t)=x_{0}\cos{(\omega_{0}t)}+\frac{v_{0}}{\omega_{0}}\sin{(\omega_{0}t)} \\
$$
We can also make the linear combination
$$
x(t)=x_{0}\cos(\omega_{0}t+\phi) \\
$$
## Linear Air Drag

Let a resitive force on the block be defined by
$$
\textbf{F}_{d}=-b\textbf{v}
$$
where $b>0$ is a positive resistive constant. In one dimension, the force is
$$
F=-kx-b\dot{x}
$$
yielding the linear second order homogenous differential equation.
$$
m\ddot{x}+b\dot{x}+kx=0
$$
It has a characteristic polynomial
$$
m\lambda^{2}+b\lambda+k=0
$$
with two roots. We can also define new terms $\gamma$ and $\omega$.
$$
\begin{align}
\lambda_{1}=\frac{-b+\sqrt{b^{2}-4mk}}{2m}=-\gamma+\sqrt{\gamma^{2}-\omega_{0}^{2}}=-\gamma+\omega\\
\lambda_{2}=\frac{-b-\sqrt{b^{2}-4mk}}{2m}=-\gamma-\sqrt{\gamma^{2}-\omega_{0}^{2}}=-\gamma-\omega\\
\end{align}
$$
where
$$
\begin{align}
\gamma&=\frac{b}{2m} \\
\omega^{2}&=\gamma^{2}+\omega_{0}^{2} \\
\omega_{0}^{2}&=\frac{k}{m}\\
\end{align}
$$
This differential equation can have three different forms:
1. **underdamped**: $b^{2}-4mk<0$
2. **critically damped**: $b^{2}-4mk=0$
- creates a repeated root
1. **overdamped**: $b^{2}-4mk>0$
### Underdamped Case

![[underdamped.png]]

In this case, we get two complex roots of the characteristic polynomial
$$
\begin{align}
\lambda_{1}=-\gamma+\boldsymbol{i}\omega \\
\lambda_{2}=-\gamma-\boldsymbol{i}\omega \\
\end{align}
$$
We can characterize all the solutions by two linearly independent functions with the following intial conditions.
$$
x(t)=x_{0}\cos{(\omega t)}e^{-\gamma t}+(\frac{\gamma x_{0}+v_{0}}{\omega})\sin{(\omega t)}e^{-\gamma t} \\
$$
We can also make the linear combination
$$
x(t)=x_{0}\cos{(\omega t+\phi)}e^{\gamma t} \\
$$
### Critical Damping Case

![[critical_damp.png]]

In this case, $\lambda=\frac{-b}{2m}$ is a repeated root. We can characterize all the solutions by two linearly independent functions with the following intial conditions.
$$
x(t)=(x_{0}\gamma+v_{0})te^{-\gamma t}+x_{0}e^{-\gamma t} \\
$$
When $v_{0}=0$, we get
$$
\begin{align}
x(t)=x_{0}(1-\gamma t)e^{\gamma t} \\
v(t)=-x_{0}\gamma^{2}te^{\gamma t}
\end{align}
$$
where
$$
\begin{align}
\gamma&=\frac{-b}{2m} \\
\end{align}
$$
### Overdamped Case

![[overdamped.png]]

In this case, we get two real roots of the characteristic polynomial
$$
\begin{align}
\lambda_{1}=-\gamma+\omega \\
\lambda_{2}=-\gamma-\omega \\
\end{align}
$$
We can characterize all the solutions by two linearly independent functions with the following intial conditions.
$$
x(t)=\biggr(\frac{(\omega+\gamma)x_{0}+v_{0}}{2\omega}\biggr)e^{(-\gamma+\omega)t}+\biggr(\frac{(\omega-\gamma)x_{0}+v_{0}}{2\omega}\biggr)e^{(-\gamma-\omega)t} \\
$$
## Driving Force

A driving force moves the other end of the spring giving the non-homogeneous differential equation
$$
m\ddot{x}+b\dot{x}+kx=f(t)
$$
From [[14 Non-Homogeneous Equations]], we know that the solution of this equation will be the sum of the complementary solution and a particular solution. First, we can solve homogeneous system using the methods above and determine the complementary functions.
$$
\begin{align}
x_{1}(t)=e^{\lambda_{1}t} \\
x_{2}(t)=e^{\lambda_{2}t} \\
\end{align}
$$
The Wronskian is
$$
\begin{vmatrix}
e^{\lambda_{1}t} & e^{\lambda_{2}t} \\
\lambda_{1}e^{\lambda_{1}t} & \lambda_{2}e^{\lambda_{2}t} \\
\end{vmatrix}
=
(\lambda_{2}-\lambda_{1})e^{(\lambda_{1}+\lambda_{2})t}
$$
Assume that solutions are of the form $u_{1}x_{1}+u_{2}x_{2}$ where $u_{1}$ and $u_{2}$ are functions of $t$.
$$
\begin{align}
\dot{u}_{1}=\frac{-e^{\lambda_{2}t}f(t)}{W[y_{1},y_{2}]}=\frac{-f(t)}{(\lambda_{2}-\lambda_{1})e^{\lambda_{1}t}} \\
\dot{u}_{2}=\frac{e^{\lambda_{1}t}f(t)}{W[y_{1},y_{2}]}=\frac{f(t)}{(\lambda_{2}-\lambda_{1})e^{\lambda_{2}t}} \\
\end{align}
$$
Using variation of parameters, we get
$$
x(t)=\frac{1}{\lambda_{1}-\lambda_{2}}\biggr(\int-f(t)e^{-\lambda_{1}t}dte^{\lambda_{1}t}+\int f(t)e^{-\lambda_{2}t}dte^{\lambda_{2}t} \biggr) \\
$$
## [[5 Resonance]]