## 10/??/26
![[polar.excalidraw]]
## Definiton

The **polar basis** is a 2-D coordinate system that rotates freely about a fixed point with respect to a fixed coordinate system.

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
1. First Time Derivative
$$
\begin{align}
\frac{d\hat{\textbf{r}}}{dt}=\dot{\theta}\boldsymbol{\hat{\theta}} \\
\frac{d\boldsymbol{\hat{\theta}}}{dt}=-\dot{\theta}\hat{\textbf{r}} \\
\end{align}
$$
2. Second Time Derivative
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
$$
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\
\end{bmatrix}
=
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} \\
\sin{\theta} & \cos{\theta} \\
\end{bmatrix}
\begin{bmatrix}
\hat{\textbf{r}} \\
\boldsymbol{\hat{\theta}}
\end{bmatrix}
$$
- *Note: This is an inverse rotation matrix because this is a passive rotation. If I rotate my frame of reference one way, it looks like all the vectors rotate the other way.*
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
## Gradient
$$
\frac{d}{dx}\hat{\textbf{x}}+\frac{d}{dy}\hat{\textbf{y}}=\frac{d}{dr}\hat{\textbf{r}}+\frac{1}{r}\frac{d}{d\theta}\hat{\boldsymbol{\theta}}
$$
## Polar Kinematics

Using this system, we can now define the position of an object.
$$
\vec{r}=r\hat{\textbf{r}}\in\mathbb{R}^{2}
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
- The radial component is made up of any physical radial acceleration along with **psuedo force** centripedal acceleration formula $r\dot{\theta}^{2}$. It is negative since it points inwards, while the radial unit vector $\hat{\textbf{r}}$ points outwards.
- The tangential component is made up of the tangential acceleration $r\ddot{\theta}$ and the psuedo force **Coriolis acceleration** $2\dot{r}\dot{\theta}$.

**psuedo force** - apparent force that seems to act on an object when observed from a non-inertial frame of reference
- Any dynamic basis can be a non-inertial frame of reference.
### Example - Simple Pendulum

1. The only forces that act on the bob are gravity $-mg\hat{\textbf{y}}$, and tension with unknown magnitude $-F_{T}\hat{\textbf{r}}$. Tension already points along one of the polar basis vectors. The gravitational force acts in another direction.
$$
-mg\hat{\textbf{y}}=-mg\sin{(\theta)}\hat{\textbf{r}}-mg\cos{(\theta)}\boldsymbol{\hat{\theta}}
$$
- The radial and tangential forces on the bob can be written as
$$
\begin{align}
\vec{F_{r}}=(-mg\sin{\theta}-F_{T})\hat{\textbf{r}} \\
\vec{F_{\theta}}=-mg\cos{(\theta)}\boldsymbol{\hat{\theta}}
\end{align}
$$
2. With the radial and tangential forces, we can write the acceleration in polar basis.
$$
\frac{d^{2}\vec{r}}{dt^{2}}=(-g\sin{\theta}-\frac{F_{T}}{m})\hat{\textbf{r}}-g\cos{(\theta)}\boldsymbol{\hat{\theta}}
$$
3. Using the polar basis acceleration formula, we can create the following equivalencies.
$$
\begin{align}
g\sin{\theta}+\frac{F_{T}}{m}=r\dot{\theta}^{2}-\ddot{r} \\
-g\cos{(\theta)}=r\ddot{\theta}+2\dot{r}\dot{\theta} \\
\end{align}
$$
4. Now, we will consider the constraint of the simple pendulum: $r$ is a fixed length. That means $\dot{r}=\ddot{r}=0$.
$$
\begin{align}
g\sin{\theta}+\frac{F_{T}}{m}=r\dot{\theta}^{2} \\
-g\cos{(\theta)}=r\ddot{\theta} \\
\end{align}
$$
5. The equation of motion, is therefore
$$
r\ddot{\theta}+g\cos{(\theta)}=0 \\
$$
6. We can also solve for the magnitude of the tension force $F_{T}$.
$$
F_{T}=m(r\dot{\theta}^{2}-g\sin{\theta}) \\
$$
## [[3 Cylindrical Basis]]
