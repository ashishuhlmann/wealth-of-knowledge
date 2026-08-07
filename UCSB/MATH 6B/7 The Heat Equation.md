## 5/11/26

Consider a homogeneous solid material in $\mathbb{R}^{3}$.
- Let $U(x,y,z,t)$ be the temperature at time $t$.
- Let $\textbf{q}(x,y,z,t)$ be the heat current density. $\textbf{q}\cdot\hat{\textbf{n}}$ is the heat flux in the direction of a unit vector $\hat{\textbf{n}}$.

Let $W$ be a solid region within the material with surface $S$. The total heat flowing out of $W$ at time $t$ is
$$
\int\int_{S}\textbf{q}\cdot d\textbf{A}=\int\int\int_{W}\nabla\cdot\textbf{q}DV
$$
And we use **Fourier's law of conduction**
$$
\textbf{q}=-k\nabla U
$$
The total amount of energy inside $W$ at time $t$ is
$$
E=\int\int\int_{W}\sigma\rho UdV
$$
- $\sigma$ is the **heat capacity**.
- $\rho$ is the density.

Assume no external sources of heat. The rate at which heat flows from the outside space into the region $W$ is
$$
\frac{\partial E}{\partial t}=-\int\int_{S}\textbf{q}\cdot d\textbf{A}
$$
where we substitute
$$
\frac{\partial}{\partial t}\int\int\int_{W}\sigma\rho U dV=-\int\int_{S}\textbf{q}\cdot d\textbf{A}
$$
Use the divergence theorem
$$
\int\int\int_{W}\sigma\rho \frac{\partial U}{\partial t} dV=-\int\int\int_{W}\nabla\cdot\textbf{q}dV
$$
and substitute
$$
\int\int\int_{W}\sigma\rho \frac{\partial U}{\partial t} dV=k\int\int\int_{W}\nabla^{2}UdV
$$
and finally get
$$
\frac{\partial U}{\partial t}=\frac{k}{\sigma\rho}\nabla^{2}U
$$
$U(x,y,z,t)$ satisfies the **patrial differential equation**
$$
\frac{\partial U}{\partial t}=\alpha^{2}\nabla^{2}U
$$
- $\alpha$ is the **diffusivity** of the material.
### Example
$$
\begin{cases}
&\frac{\partial U}{\partial t}=\alpha^{2}\frac{\partial^{2}U}{\partial x^2} \\
&U(x,0)=f(x) \\
&U(0,t)=U(2\pi,t)=0
\end{cases}
$$
The solution is
$$
\sum_{k=1}^{\infty}c_{k}e^{-\alpha^{2} t}\sin(k\sqrt{\alpha}x)
$$
$$
c_{k}=\frac{1}{\pi}\int_{0}^{2\pi}f(x)\sin{(nx)}dx
$$
## [[8 Sequences and Series]]