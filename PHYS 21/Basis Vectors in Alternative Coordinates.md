
In cartesian coordinates, the position vector is defined as a certain distance along each axis in a column vector.
- We can also use *fixed* unit vectors $\boldsymbol{î}$ and $\boldsymbol{ĵ}$, and $\boldsymbol{\hat{k}}$ (in 3-D) to express these distances as well.
- Since this basis does not change in time, the position, velocity, acceleration, or any other quantity can simply be expressed in terms of these unit vectors.

The positions, velocities, and accelerations of objects should be invariant over whichever coordinate system we are using.
## Polar Basis 

![[polar.excalidraw]]
### Definiton

The **polar basis** is simply a 2-D coordinate system that rotates freely about a fixed point with respect to any fixed coordinate system.

In the polar basis, the position vector is defined as a certain distance away from the pole, or the radial distance, and a certain distance away from that point perpendicular to the first distance, or the tangential distance.
- We use *dynamic* unit vectors $\hat{\textbf{r}}$ and $\boldsymbol{\hat{\theta}}$ to express these distances, meaning they *change in time*. Specifically, they rotate freely together. Like cartesian basis vectors, they are always perpendicular to one another.
### Basis Vectors

0. Definition
$$
\begin{align}
\hat{\textbf{r}}&=\cos{(\theta)}\hat{\textbf{x}}+\sin{(\theta)}\hat{\textbf{y}} \\
\boldsymbol{\hat{\theta}}&=-\sin{(\theta)}\hat{\textbf{x}}+\cos{(\theta)}\hat{\textbf{y}} \\
\end{align}
$$
$$
\begin{align}
\hat{\textbf{x}}&=\cos{(\theta)}\hat{\textbf{r}}-\sin{(\theta)}\boldsymbol{\hat{\theta}} \\
\hat{\textbf{y}}&=\sin{(\theta)}\hat{\textbf{r}}+\cos{(\theta)}\boldsymbol{\hat{\theta}} \\
\end{align}
$$
0. First Time Derivative
$$
\begin{align}
\frac{d\hat{\textbf{r}}}{dt}=\dot{\theta}\boldsymbol{\hat{\theta}} \\
\frac{d\boldsymbol{\hat{\theta}}}{dt}=-\dot{\theta}\hat{\textbf{r}} \\
\end{align}
$$
1. Second Time Derivative
$$
\begin{align}
\frac{d^{2}\hat{\textbf{r}}}{dt^{2}}=-\dot{\theta}^{2}\hat{\textbf{r}}+\ddot{\theta}\boldsymbol{\hat{\theta}} \\
\frac{d^{2}\boldsymbol{\hat{\theta}}}{dt^{2}}=-\ddot{\theta}\hat{\textbf{r}}-\dot{\theta}^{2}\boldsymbol{\hat{\theta}} \\
\end{align}
$$
### Rotation Matrix Representation
$$
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\theta}}
\end{bmatrix}
=
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \\
-\sin{\theta} & \cos{\theta} \\
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\end{bmatrix}
$$
- *Note: This is an inverse rotation matrix because this is a passive rotation. If I rotate my frame of reference one way, it looks like all the vectors rotate the other way.*

skew-symmetric matricies
$$
\frac{d}{dt}
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\theta}}
\end{bmatrix}
=
\begin{bmatrix}
0 & \dot{\theta} \\
-\dot{\theta} & 0 \\
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \\
-\sin{\theta} & \cos{\theta} \\
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\end{bmatrix}
$$
$$
\frac{d^{2}}{dt^{2}}
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\theta}}
\end{bmatrix}
=
\begin{bmatrix}
-\dot{\theta}^{2} & \ddot{\theta} \\
-\ddot{\theta} & -\dot{\theta}^{2} \\
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \\
-\sin{\theta} & \cos{\theta} \\
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\end{bmatrix}
$$
### Gradient
$$
\nabla=\frac{d}{dx}\hat{\textbf{x}}+\frac{d}{dy}\hat{\textbf{y}}
$$
$$
\nabla=\frac{d\hat{\textbf{x}}dy+d\hat{\textbf{y}}dx}{dxdy}
$$
$$
\nabla=\frac{d\hat{\textbf{x}}dy+d\hat{\textbf{y}}dx}{rdrd\theta}
$$
$$
\nabla=\frac{d}{dx}(\cos{(\theta)}\hat{\textbf{r}}-\sin{(\theta)}\boldsymbol{\hat{\theta}})+\frac{d}{dy}(\sin{(\theta)}\hat{\textbf{r}}+\cos{(\theta)}\boldsymbol{\hat{\theta}})
$$
$$
\nabla=\frac{d}{dx}\cos{(\theta)}\hat{\textbf{r}}-\frac{d}{dx}\sin{(\theta)}\boldsymbol{\hat{\theta}}+\frac{d}{dy}\sin{(\theta)}\hat{\textbf{r}}+\frac{d}{dy}\cos{(\theta)}\boldsymbol{\hat{\theta}}
$$$$
\frac{d}{dr}\hat{\textbf{r}}+\frac{1}{r}\frac{d}{d\theta}\hat{\boldsymbol{\theta}}
$$
### Polar Kinematics

Using this system, we can now define the position of an object.
$$
\vec{r}=r\hat{\textbf{r}}
$$
1. Velocity
$$
\frac{d\vec{r}}{dt}=\dot{r}\hat{\textbf{r}}+r\dot{\theta}\boldsymbol{\hat{\theta}}
$$
- This is a combination of the radial velocity $v_{r}=\dot{r}$ and the tangential velocity $v_{t}=r\dot{\theta}$.
2. Acceleration
$$
\frac{d^{2}\vec{r}}{dt^{2}}=(\ddot{r}-r\dot{\theta}^2)\hat{\textbf{r}}+(r\ddot{\theta}+2\dot{r}\dot{\theta})\boldsymbol{\hat{\theta}}
$$
- The radial component is made up of any physical radial acceleration along with circular motion centripedal acceleration formula $r\dot{\theta}^{2}$. It is negative since it points inwards, while the radial unit vector $\hat{\textbf{r}}$ points outwards.
- The tangential component is made up of the tangential acceleration $r\ddot{\theta}$ and the **Coriolis acceleration** $2\dot{r}\dot{\theta}$.
### Problem Solving

1. Identify all the forces acting on the given objects
2. Compute the values of radial and tangential forces, substituting for any unknowns if applicable.
3. Apply any constraints of the system to the polar basis acceleration formula and equate the radial and tangential components with the radial and tangential forces over the mass.
4. Simplify and arrive at the equations of motion.
### Example - Simple Pendulum

1. The only forces that act on the bob are gravity with magnitude $mg$, and tension with unknown magnitude $F_{T}$. (Let $g$ be the magnitude of gravitational acceleration.)
- The radial and tangential forces on the bob can be written as
$$
\begin{align}
\vec{F_{r}}=m(g\cos{\theta}-F_{T})\hat{\textbf{r}} \\
\vec{F_{t}}=-mg\sin{(\theta)}\boldsymbol{\hat{\theta}}
\end{align}
$$
2. With the radial and tangential forces, we can write the acceleration in polar basis.
$$
\frac{d^{2}\vec{r}}{dt^{2}}=(g\cos{\theta}-\frac{F_{T}}{m})\hat{\textbf{r}}-g\sin{(\theta)}\boldsymbol{\hat{\theta}}
$$
3. Using the polar basis acceleration formula, we can create the following equivalencies.
$$
\begin{align}
g\cos{\theta}-\frac{F_{T}}{m}=\ddot{r}-r\dot{\theta}^{2} \\
-g\sin{(\theta)}=r\ddot{\theta}+2\dot{r}\dot{\theta} \\
\end{align}
$$
4. Now, we will consider the main constraint of the simple pendulum: $r$ is a fixed length. That means $\dot{r}=\ddot{r}=0$.
$$
\begin{align}
\frac{F_{T}}{m}-g\cos{\theta}=r\dot{\theta}^{2} \\
-g\sin{(\theta)}=r\ddot{\theta} \\
\end{align}
$$
5. The equation of motion, is therefore
$$
r\ddot{\theta}+g\sin{(\theta)}=0 \\
$$
6. We can also solve for the magnitude of the tension force $F_{T}$.
$$
F_{T}=m(r\dot{\theta}^{2}+g\cos{\theta}) \\
$$
## Cylindrical Basis

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
### Cylindrical Kinematics

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
- The verical component is simply the linear vertical acceleration.

### Example - Whirling Block

1. Determine the forces acting on each block.

block A
- gravity: $-mg\hat{\textbf{z}}$
- normal: $mg\hat{\textbf{z}}$
- tension: $-F_{T}\hat{\textbf{r}}$

block B
- gravity: $-Mg\hat{\textbf{z}}$
- tension: $F_{T}\hat{\textbf{z}}$

2. 
The radial, tangential, and vertical forces on block A can be written as
$$
\begin{align}
\vec{F_{r}}=-F_{T}\hat{\textbf{r}} \\
\vec{F_{\theta}}=\vec{0} \\
\vec{F_{z}}=\vec{0} \\
\end{align}
$$

The radial, tangential, and vertical forces on block B can be written as
$$
\begin{align}
\vec{F_{r}}=\vec{0} \\
\vec{F_{\theta}}=\vec{0} \\
\vec{F_{z}}=(F_{T}-Mg)\hat{\textbf{z}} \\
\end{align}
$$
3. acceleration
block A
$$
\frac{d^{2}\vec{r_{A}}}{dt^{2}}=\frac{-F_{T}}{m}\hat{\textbf{r}}
$$
block B
$$
\frac{d^{2}\vec{r_{B}}}{dt^{2}}=(\frac{F_{T}}{M}-g)\hat{\textbf{z}}
$$
4. Create the equivalencies using cylindrical acceleration 
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
## Spherical Basis

0. For the spherical basis, we will use the physics convention of spherical coordinates.efinition

$$
\begin{align}
\boldsymbol{\hat{\rho}}&=
\cos{(\theta)}\cos{(\phi)}\hat{\textbf{x}}
+\sin{(\theta)}\cos{(\phi)}\hat{\textbf{y}}
+\sin{(\phi)}\hat{\textbf{z}} \\

\boldsymbol{\hat{\theta}}&=
-\sin{(\theta)}\hat{\textbf{x}}
+\cos{(\theta)}\hat{\textbf{y}} \\

\boldsymbol{\hat{\phi}}&=
-\cos{(\theta)}\sin{(\phi)}\hat{\textbf{x}}
-\sin{(\theta)}\sin{(\phi)}\hat{\textbf{y}}
+\cos{(\phi)}\hat{\textbf{z}} \\
\end{align}
$$
1. First Time Derivative
$$
\begin{align}
\frac{d\boldsymbol{\hat{\rho}}}{dt}&=\dot{\theta}\cos{(\phi)}\boldsymbol{\hat{\theta}}+\dot{\phi}\boldsymbol{\hat{\phi}} \\

\frac{d\boldsymbol{\hat{\theta}}}{dt}&=
-\dot{\theta}\cos{(\theta)}\hat{\textbf{x}}
-\dot{\theta}\sin{(\theta)}\hat{\textbf{y}}=-\dot{\theta}\hat{\textbf{r}} \\

\frac{d\boldsymbol{\hat{\phi}}}{dt}&=
-\dot{\phi}\boldsymbol{\hat{\rho}}-\dot{\theta}\sin{(\phi)}\boldsymbol{\hat{\theta}} \\
\end{align}
$$
2. Second Time Derivative
$$
\begin{align}
\frac{d^{2}\boldsymbol{\hat{\rho}}}{dt^{2}}&=-\dot{\phi}^{2}\boldsymbol{\hat{\rho}}-\dot{\theta}^{2}\cos{(\phi)}\hat{\textbf{r}}+(\ddot{\theta}\cos{(\phi)}-2\dot{\theta}\dot{\phi}\sin{(\phi)})\boldsymbol{\hat{\theta}}+\ddot{\phi}\boldsymbol{\hat{\phi}} \\

\frac{d^{2}\boldsymbol{\hat{\theta}}}{dt^{2}}&=-\ddot{\theta}\hat{\textbf{r}}-\dot{\theta}^{2}\boldsymbol{\hat{\theta}} \\

\frac{d\boldsymbol{\hat{\phi}}}{dt}&=-\ddot{\phi}\boldsymbol{\hat{\rho}}+\dot{\theta}^{2}\sin{(\phi)}\hat{\textbf{r}}-(2\dot{\theta}\dot{\phi}\cos{(\phi)}+\ddot{\theta}\sin{(\phi)})\boldsymbol{\hat{\theta}}-\dot{\phi}^{2}\boldsymbol{\hat{\phi}} \\
\end{align}
$$
### Rotation Matrix Representation
$$
\begin{bmatrix}
\boldsymbol{\hat{\rho}} \\
\boldsymbol{\hat{\theta}} \\ 
\boldsymbol{\hat{\phi}} \\
\end{bmatrix}
=
\begin{bmatrix}
\cos{\theta}\cos{\phi} & \sin{\theta}\cos{\phi} & \sin{\phi} \\
-\sin{\theta} & \cos{\theta} & 0 \\
-\cos{\theta}\sin{\phi} & -\sin{\theta}\sin{\phi} & \cos{\phi} \\
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\ 
\hat{\textbf{z}} \\
\end{bmatrix}
$$
This is simply an inverse rotation matrix about the $z$-axis followed by an inverse rotation matrix about the $y$-axis.
$$
\begin{bmatrix}
\boldsymbol{\hat{\rho}} \\
\boldsymbol{\hat{\theta}} \\ 
\boldsymbol{\hat{\phi}} \\
\end{bmatrix}
=
\begin{bmatrix}
\cos{\phi} & 0 & \sin{\phi} \\
0 & 1 & 0 \\
-\sin{\phi} & 0 & \cos{\phi} \\
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} & 0 \\
-\sin{\theta} & \cos{\theta} & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\ 
\hat{\textbf{z}} \\
\end{bmatrix}
$$
### Spherical Kinematics

0. The position is defined similarly to polar:
$$
\vec{\rho}=\rho\boldsymbol{\hat{\rho}}
$$
1. Velocity
$$
\frac{d\vec{\rho}}{dt}=\dot{\rho}\boldsymbol{\hat{\rho}}+\rho\dot{\theta}\cos{(\phi)}\boldsymbol{\hat{\theta}}+\rho\dot{\phi}\boldsymbol{\hat{\phi}}
$$
- This is a combination of radial velocity, as well as both tangential velocities.
2. Acceleration
$$
\frac{d^{2}\vec{\rho}}{dt^{2}}=(\ddot{\rho}-\rho\dot{\phi}^{2})\boldsymbol{\hat{\rho}}-\rho\dot{\theta}^{2}\cos{(\phi)}\hat{\textbf{r}}+(-2\rho\dot{\phi}\dot{\theta}\sin{(\phi)}+(2\dot{\rho}\dot{\theta}+\rho\ddot{\theta})\cos{(\phi)})\boldsymbol{\hat{\theta}}+(2\dot{\rho}\dot{\phi}+\rho\ddot{\phi})\boldsymbol{\hat{\phi}}
$$
## Hyperbolic Basis

0. 
$$
\begin{align}
\hat{\textbf{r}}&=\frac{1}{\sqrt{\cosh2\gamma}}(\cosh{(\gamma)}\hat{\textbf{x}}+\sinh{(\gamma)}\hat{\textbf{y}}) \\
\hat{\boldsymbol{\gamma}}&=\frac{1}{\sqrt{\cosh2\gamma}}(-\sinh{(\gamma)}\hat{\textbf{x}}+\cosh{(\gamma)}\hat{\textbf{y}}) \\
\end{align}
$$
1. first time derivative
$$
\begin{align}
\frac{d\hat{\textbf{r}}}{dt}&=\dot{\gamma}\hat{\boldsymbol{\gamma}} \\
\frac{d\hat{\boldsymbol{\gamma}}}{dt}&=\dot{\gamma}\hat{\textbf{r}} \\
\end{align}
$$
2. second time derivative
$$
\begin{align}
\hat{\textbf{r}}&=\dot{\gamma}^{2}\hat{\textbf{r}}+\ddot{\gamma}\hat{\boldsymbol{\gamma}} \\
\hat{\boldsymbol{\gamma}}&=\ddot{\gamma}\hat{\textbf{r}}+\dot{\gamma}^{2}\hat{\boldsymbol{\gamma}} \\
\end{align}
$$
### Rotation Matrix Representation
$$
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\gamma}}
\end{bmatrix}
=
\begin{bmatrix}
\cosh{\gamma} & \sinh{\gamma} \\
-\sinh{\gamma} & \cosh{\gamma} \\
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\end{bmatrix}
$$
- *Note: This is an inverse rotation matrix because this is a passive rotation. If I rotate my frame of reference one way, it looks like all the vectors rotate the other way.*

skew-symmetric matricies
$$
\frac{d}{dt}
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\varphi}}
\end{bmatrix}
=
\begin{bmatrix}
\dot{\gamma} & 0 \\
0 & \dot{\gamma} \\
\end{bmatrix}
\begin{bmatrix}
\cosh{\varphi} & \sinh{\varphi} \\
\sinh{\varphi} & \cosh{\varphi} \\
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\end{bmatrix}
$$
$$
\frac{d^{2}}{dt^{2}}
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\theta}}
\end{bmatrix}
=
\begin{bmatrix}
-\dot{\theta}^{2} & \ddot{\theta} \\
-\ddot{\theta} & -\dot{\theta}^{2} \\
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \\
-\sin{\theta} & \cos{\theta} \\
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\end{bmatrix}
$$
