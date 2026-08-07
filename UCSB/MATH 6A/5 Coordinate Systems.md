## 1/26/26
## Polar Coordinates
$$
\begin{align}
x=r\cos{\theta} \\
y=r\sin{\theta} \\
\end{align}
$$
$$
\begin{align}
r=\sqrt{x^{2}+y^{2}} \\
\theta=\tan^{-1}{(\frac{y}{x})} \\
\end{align}
$$
### Vector Representation
$$
\boldsymbol{T}_{\theta}^{x}(
\begin{bmatrix}
r \\
\theta \\
\end{bmatrix})
=
\begin{bmatrix}
r\cos{\theta} \\
r\sin{\theta} \\
\end{bmatrix}
$$
The Jacobian matrix of this function is
$$
D\boldsymbol{T}_{\theta}^{x}=
\begin{bmatrix}
\cos{\theta} & -r\sin{\theta} \\
\sin{\theta} & r\cos{\theta} \\
\end{bmatrix}
=
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} \\
\sin{\theta} & \cos{\theta} \\
\end{bmatrix}
\begin{bmatrix}
1 & 0 \\
0 & r \\
\end{bmatrix}
$$
- It is a rotation about the origin and a stretch along the $y$-axis

So that means determinant of the Jacobian is
$$
|D\boldsymbol{T}_{\theta}^{x}|=r
$$
Therefore, the polar differential area is
$$
dxdydz=rdrd\theta
$$
### Area of a Circle
$$
\int_{0}^{R}\int_{0}^{2\pi}rdrd\theta =\pi R^{2}
$$
## Cylindrical Coordinates
$$
\begin{align}
x=r\cos{\theta} \\
y=r\sin{\theta} \\
z=z \\
\end{align}
$$
$$
\begin{align}
r=\sqrt{x^{2}+y^{2}} \\
\theta=\tan^{-1}{(\frac{y}{x})} \\
z=z
\end{align}
$$
### Vector Representation
$$
\boldsymbol{C}_{\theta}^{x}(
\begin{bmatrix}
r \\
\theta \\
z \\
\end{bmatrix})
=
\begin{bmatrix}
r\cos{\theta} \\
r\sin{\theta} \\
z \\
\end{bmatrix}
$$
The Jacobian matrix of this function is
$$
D\boldsymbol{C}_{\theta}^{x}=
\begin{bmatrix}
\cos{\theta} & -r\sin{\theta} & 0 \\
\sin{\theta} & r\cos{\theta} & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
=
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} & 0 \\
\sin{\theta} & \cos{\theta} & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 0 \\
0 & r & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$
- It is a rotation about the $z$-axis and a stretch along the $y$-axis

So that means determinant of the Jacobian is
$$
|D\boldsymbol{T}_{\theta}^{x}|=r
$$
Therefore, the cylindrical differential volume is
$$
dxdydz=rdrd\theta dz
$$
### Volume of a Cylinder
$$
\int_{0}^{R}\int_{0}^{2\pi}\int_{0}^{h}rdrd\theta dz=\pi R^{2}h
$$
## Spherical Coordinates
*Math Convention*
$$
\begin{align}
x=\rho\cos{\theta}\sin{\phi} \\
y=\rho\sin{\theta}\sin{\phi} \\
z=\rho\cos{\phi} \\
\end{align}
$$
$$
\begin{align}
\rho=\sqrt{x^{2}+y^{2}+z^{2}} \\
\theta=\tan^{-1}{(\frac{y}{x})} \\
\phi=\tan^{-1}{(\frac{z}{\sqrt{x^{2}+y^{2}}})}
\end{align}
$$
### Vector Representation
$$
\boldsymbol{S}_{\theta}^{x}(
\begin{bmatrix}
\rho \\
\theta \\
\phi \\
\end{bmatrix}
)=
\begin{bmatrix}
\rho\cos{\theta}\sin{\phi} \\
\rho\sin{\theta}\sin{\phi} \\
\rho\cos{\phi} \\
\end{bmatrix}
$$
The Jacobian matrix of this function is
$$
\begin{align}
D\boldsymbol{S}_{\theta}^{x}=
\begin{bmatrix}
\cos{\theta}\sin{\phi} & -\rho\sin{\theta}\sin{\phi} & \rho\cos{\theta}\cos{\phi} \\
\sin{\theta}\sin{\phi} & \rho\cos{\theta}\sin{\phi} & \rho\sin{\theta}\cos{\phi} \\
\cos{\phi} & 0 & -\rho\sin{\phi} \\
\end{bmatrix}
\\ =
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} & 0 \\
\sin{\theta} & \cos{\theta} & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
\begin{bmatrix}
\cos{\phi} & 0 & \sin{\phi} \\
0 & 1 & 0 \\
-\sin{\phi} & 0 & \cos{\phi} \\
\end{bmatrix}
\begin{bmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0 \\
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 0 \\
0 & \rho\sin{\phi} & 0 \\
0 & 0 & \rho \\
\end{bmatrix}
\end{align}
$$
- It is a rotation about the $z$-axis, a reverse rotation about the $y$-axis, a reflection about the plane $z=x$, and a stretch along both the $y$ and $z$ axes.

So that means that the determinant of the Jacobian is
$$
|D\boldsymbol{T}_{\theta}^{x}|=-\rho^{2}\sin{\phi}
$$
Therefore, the spherical differential volume is
$$
dxdydz=-\rho^{2}\sin{(\phi)}d\rho d\theta d\phi
$$
### Volume of a Sphere
$$
\int_{0}^{\pi}\int_{0}^{2\pi}\int_{0}^{R}-\rho^{2}\sin{(\phi)}d\rho d\theta d\phi=\frac{-4}{3}\pi R^{3}
$$
- *Note: We only need to integrate half a circle in $\phi$, and then go all the way around in* $\theta$.
## Hyperbolic Coordinates
$$
\begin{align}
x=r\cosh{\gamma} \\
y=r\sinh{\gamma} \\
\end{align}
$$
$$
\begin{align}
r=\sqrt{x^{2}-y^{2}} \\
\gamma=\tanh^{-1}{(\frac{y}{x})} \\
\end{align}
$$
### Vector Representation
$$
\boldsymbol{T}_{\gamma}^{x}(
\begin{bmatrix}
r \\
\gamma \\
\end{bmatrix})
=
\begin{bmatrix}
r\cosh{\gamma} \\
r\sinh{\gamma} \\
\end{bmatrix}
$$
The Jacobian matrix of this function is
$$
D\boldsymbol{T}_{\theta}^{x}=
\begin{bmatrix}
\cosh{\gamma} & r\sinh{\gamma} \\
\sinh{\gamma} & r\cosh{\gamma} \\
\end{bmatrix}
=
\begin{bmatrix}
\cosh{\gamma} & \sinh{\gamma} \\
\sinh{\gamma} & \cosh{\gamma} \\
\end{bmatrix}
\begin{bmatrix}
1 & 0 \\
0 & r \\
\end{bmatrix}
$$
- It is a hyperbolic rotation about the origin and a stretch along the $y$-axis

So that means determinant of the Jacobian is
$$
|D\boldsymbol{T}_{\theta}^{x}|=r
$$
Therefore, the hyperbolic differential area is
$$
dxdydz=rdrd\gamma
$$
## [[Basis Vectors in Alternative Coordinates]]