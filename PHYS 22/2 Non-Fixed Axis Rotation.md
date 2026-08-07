## 1/22/26

Using an insitintaneous angular velocity $\vec{\omega}$, the velocity about the center of mass is
$$
\vec{v_{i}}=\vec{\omega}\times\vec{r_{i}}
$$
So the angular momentum about the center of mass is
$$
\vec{L_{c}}=\sum_{i}\vec{r_{i}}\times m_{i}(\vec{\omega}\times \vec{r_{i}})
$$
1. 
$$
\vec{\omega}\times\vec{r}=(z\omega_{y}-y\omega_{z})\hat{\bf{x}}-(x\omega_{z}-z\omega_{x})\hat{\bf{y}}+(y\omega_{x}-x\omega_{y})\hat{\bf{z}}
$$
2. 
$$
\begin{align}
\vec{r}\times(\vec{\omega}\times\vec{r})=\phantom{--------} \\
\biggr(\sum_{i}(y_{i}^{2}+z_{i}^{2})\omega_{x}-\sum_{i}x_{i}y_{i}\omega_{y}-\sum_{i}x_{i}z_{i}\omega_{z}\biggr)\hat{\bf{x}} \\
-\biggr(\sum_{i}x_{i}y_{i}\omega_{x}-\sum_{i}(x_{i}^{2}+z_{i}^{2})\omega_{y}+\sum_{i}y_{i}z_{i}\omega_{z}\biggr)\hat{\bf{y}}\\
-\biggr(\sum_{i}z_{i}x_{i}\omega_{x}+\sum_{i}z_{i}y_{i}\omega_{y}-\sum_{i}(x_{i}^{2}+y_{i}^{2})\omega_{z}\biggr)\hat{\bf{z}}\\
\end{align}
$$
## Inertia Tensor
$$
\vec{L}=
\begin{bmatrix}
I_{xx} & I_{xy} & I_{xz} \\
I_{yx} & I_{yy} & I_{yz} \\
I_{zx} & I_{zy} & I_{zz} \\
\end{bmatrix}
\vec{\omega}
$$
**moments of inertia** - a fixed axis moment of inertia
$$
\begin{align}
I_{xx}&=\sum_{M}(y_{j}^{2}+z_{j}^{2})m_{j}\rightarrow\int_{M}(y^{2}+z^{2})dm \\
I_{yy}&=\sum_{M}(x_{j}^{2}+z_{j}^{2})m_{j}\rightarrow\int_{M}(x^{2}+z^{2})dm \\
I_{zz}&=\sum_{M}(x_{j}^{2}+y_{j}^{2})m_{j}\rightarrow\int_{M}(x^{2}+y^{2})dm
\end{align}
$$
**products of inertia** - symmetrical terms
$$
\begin{align}
I_{xy}=I_{yx}&=-\sum_{M}x_{j}y_{j}m_{j}\rightarrow-\int_{M}xydm \\
I_{yz}=I_{zy}&=-\sum_{M}y_{j}z_{j}m_{j}\rightarrow-\int_{M}yzdm \\
I_{xz}=I_{zx}&=-\sum_{M}x_{j}z_{j}m_{j}\rightarrow-\int_{M}xzdm \\
\end{align}
$$
## [[3 Central Force Motion]]