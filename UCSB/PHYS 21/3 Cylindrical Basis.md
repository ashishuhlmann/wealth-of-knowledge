## ??/??/26
## Definition

The **cylindrical basis** is identical to the polar basis with a fixed vector perpendicular to both $\hat{\textbf{r}}$ and $\hat{\boldsymbol{\theta}}$. 

0. Definition
$$
\begin{align}
\hat{\textbf{r}}&=\cos{(\theta)}\hat{\textbf{x}}+\sin{(\theta)}\hat{\textbf{y}} \\
\hat{\boldsymbol{\theta}}&=-\sin{(\theta)}\hat{\textbf{x}}+\cos{(\theta)}\hat{\textbf{y}} \\
\hat{\textbf{z}}&=\hat{\textbf{z}} \\
\end{align}
$$
1. First Time Derivative
$$
\begin{align}
\frac{d\hat{\textbf{r}}}{dt}&=\dot{\theta}\boldsymbol{\hat{\theta}} \\
\frac{d\boldsymbol{\hat{\theta}}}{dt}&=-\dot{\theta}\hat{\textbf{r}} \\
\frac{d\hat{\textbf{z}}}{dt}&=\vec{0} \\
\end{align}
$$
2. Second Time Derivative
$$
\begin{align}
\frac{d^{2}\hat{\textbf{r}}}{dt^{2}}&=-\dot{\theta}^{2}\hat{\textbf{r}}+\ddot{\theta}\boldsymbol{\hat{\theta}} \\
\frac{d^{2}\boldsymbol{\hat{\theta}}}{dt^{2}}&=-\ddot{\theta}\hat{\textbf{r}}-\dot{\theta}^{2}\boldsymbol{\hat{\theta}} \\
\frac{d^{2}\hat{\textbf{z}}}{dt^{2}}&=\vec{0} \\
\end{align}
$$
### Rotation Matrix Representation
$$
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\theta}} \\
\hat{\textbf{z}}
\end{bmatrix}
=
\begin{bmatrix}
\cos{\theta} & \sin{\theta} & 0 \\
-\sin{\theta} & \cos{\theta} & 0 \\
0 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\hat{\textbf{z}} \\
\end{bmatrix}
$$
$$
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\hat{\textbf{z}} \\
\end{bmatrix}
=
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} & 0 \\
\sin{\theta} & \cos{\theta} & 0 \\
0 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\theta}} \\
\hat{\textbf{z}}
\end{bmatrix}
$$
- *Note: This is an inverse rotation matrix because this is a passive rotation. If I rotate my frame of reference one way, it looks like all the vectors rotate the other way.*
$$
\frac{d}{dt}
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\theta}} \\
\hat{\textbf{z}} \\
\end{bmatrix}
=
\begin{bmatrix}
0 & \dot{\theta} & 0 \\
-\dot{\theta} & 0 & 0 \\
0 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} & 0 \\
-\sin{\theta} & \cos{\theta} & 0 \\
0 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\hat{\textbf{z}} \\
\end{bmatrix}
$$
$$
\frac{d^{2}}{dt^{2}}
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\theta}} \\
\hat{\textbf{z}} \\
\end{bmatrix}
=
\begin{bmatrix}
-\dot{\theta}^{2} & \ddot{\theta} & 0 \\
-\ddot{\theta} & -\dot{\theta}^{2} & 0 \\
0 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} & 0 \\
-\sin{\theta} & \cos{\theta} & 0 \\
0 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\hat{\textbf{z}} \\
\end{bmatrix}
$$
## Gradient

$$
\frac{d}{dx}\hat{\textbf{x}}+\frac{d}{dy}\hat{\textbf{y}}+\frac{d}{dx}\hat{\textbf{z}}=\frac{d}{dr}\hat{\textbf{r}}+\frac{1}{r}\frac{d}{d\theta}\hat{\boldsymbol{\theta}}+\frac{d}{dx}\hat{\textbf{z}}
$$
## Cylindrical Kinematics

Using this system, we can now define the position of an object.
$$
\vec{r}=r\hat{\textbf{r}}+z\hat{\textbf{z}}\in\mathbb{R}^{3}
$$
1. Velocity
$$
\frac{d\vec{r}}{dt}=\dot{r}\hat{\textbf{r}}+r\dot{\theta}\boldsymbol{\hat{\theta}}+\dot{z}\hat{\textbf{z}}
$$
- This is a combination of the radial velocity $v_{r}=\dot{r}$ and the tangential velocity $v_{t}=r\dot{\theta}$.
2. Acceleration
$$
\frac{d^{2}\vec{r}}{dt^{2}}=(\ddot{r}-r\dot{\theta}^2)\hat{\textbf{r}}+(r\ddot{\theta}+2\dot{r}\dot{\theta})\boldsymbol{\hat{\theta}}+\ddot{z}\hat{\textbf{z}}
$$
- The radial component is made up of any physical radial acceleration along with circular motion centripedal acceleration formula $r\dot{\theta}^{2}$. It is negative since it points inwards, while the radial unit vector $\hat{\textbf{r}}$ points outwards.
- The tangential component is made up of the tangential acceleration $r\ddot{\theta}$ and the **Coriolis acceleration** $2\dot{r}\dot{\theta}$.
- The verical component is the linear vertical acceleration.
### Example - Whirling Block

1. Determine the forces acting on each block.

block A
- gravity: $-mg\hat{\textbf{z}}$
- normal: $mg\hat{\textbf{z}}$
- tension: $-F_{T}\hat{\textbf{r}}$

block B
- gravity: $-Mg\hat{\textbf{z}}$
- tension: $F_{T}\hat{\textbf{z}}$

2. Write the radial, tangential, and vertical force components.

block A
$$
\begin{align}
\vec{F_{r}}=-F_{T}\hat{\textbf{r}} \\
\vec{F_{\theta}}=\vec{0} \\
\vec{F_{z}}=\vec{0} \\
\end{align}
$$

block B
$$
\begin{align}
\vec{F_{r}}=\vec{0} \\
\vec{F_{\theta}}=\vec{0} \\
\vec{F_{z}}=(F_{T}-Mg)\hat{\textbf{z}} \\
\end{align}
$$
3. Get the acceleration.

block A
$$
\frac{d^{2}\vec{r_{A}}}{dt^{2}}=\frac{-F_{T}}{m}\hat{\textbf{r}}
$$
block B
$$
\frac{d^{2}\vec{r_{B}}}{dt^{2}}=(\frac{F_{T}}{M}-g)\hat{\textbf{z}}
$$
4. Create the equivalencies using cylindrical acceleration.

block A
$$
\begin{align}
r\dot{\theta}^{2}-\ddot{r}=\frac{F_{T}}{m} \\
r\ddot{\theta}+2\dot{r}\dot{\theta}=0 \\
\end{align}
$$
block B
$$
\ddot{z}=\frac{F_{T}}{M}-g
$$
5. Consider the constraint that the string is at a fixed length, meaning $r+z=l$. Differentiating twice gives $\ddot{r}=-\ddot{z}$.
$$
\begin{align}
Mg-F_{T}=-M\ddot{r} \\
F_{T}=M(\ddot{r}+g)
\end{align}
$$
6. By substituting $F_{T}$, we get our two coupled equations of motion.
$$
\begin{equation}
\left\{ \begin{aligned} 
	\ddot{r}(\frac{M}{m}+1)-r\dot{\theta}^{2}+\frac{M}{m}g&=0 \\
	r\ddot{\theta}+2\dot{r}\dot{\theta}&=0 \\
\end{aligned} \right.
\end{equation}
$$
7. Now, we must integrate the solution on a computer. Let $v=\dot{r}$ and $\omega=\dot{\theta}$. Also, let $\gamma=\frac{M}{m}$.
$$
\vec{S}=
\begin{bmatrix}
r \\
v \\
\theta \\
\omega \\
\end{bmatrix}
$$
$$
\frac{d\vec{S}}{dt}=
\begin{bmatrix}
v \\
\frac{2v\omega+r\omega^{2}-2v\omega-\gamma g}{\gamma+1} \\
\omega \\
\frac{-2v\omega}{r} \\
\end{bmatrix}
$$
```Python
import numpy scipy

t = numpy.linspace(0,10,1000)
y = 1
g = 10
S0 = [1, 0, 0, np.sqrt(10)]

def dSdt(S, t):
	r, v, o, w = S
	return [
		v,
		(2*v*w + r*w**2 - 2*v*w - y*g) / (y + 1),
		w,
		(-2*v*w) / r
	]

r_vals, v_vals, o_vals, w_vals = scipy.integrate.odeint(dSdt, S0, t).T
```
## [[4 Spherical Basis]]