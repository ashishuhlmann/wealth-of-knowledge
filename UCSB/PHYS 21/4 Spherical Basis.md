## ??/??/26
## Definition

0. For the spherical basis, we will use the **physics convention** of spherical coordinates.
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
$$
\begin{bmatrix}
\hat{\textbf{x}} \\
\hat{\textbf{y}} \\ 
\hat{\textbf{z}} \\
\end{bmatrix}
=
\begin{bmatrix}
\cos{\theta}\cos{\phi} & -\sin{\theta}\cos{\phi} & -\sin{\phi} \\
\sin{\theta} & \cos{\theta} & 0 \\
\cos{\theta}\sin{\phi} & \sin{\theta}\sin{\phi} & \cos{\phi} \\
\end{bmatrix}
\begin{bmatrix}
\boldsymbol{\hat{\rho}} \\
\boldsymbol{\hat{\theta}} \\ 
\boldsymbol{\hat{\phi}} \\
\end{bmatrix}
$$
This is an inverse rotation matrix about the $z$-axis followed by an inverse rotation matrix about the $y$-axis (passive rotations).
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
## Gradient
$$
\frac{d}{dx}\hat{\textbf{x}}+\frac{d}{dy}\hat{\textbf{y}}+\frac{d}{dx}\hat{\textbf{z}}=
$$
## Spherical Kinematics

0. The position is defined similarly to polar coordinates.
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