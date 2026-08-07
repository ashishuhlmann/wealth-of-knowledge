## 1/29/26

Consider two gravitationally interacting bodies at positions $\textbf{r}_{1}$ and $\textbf{r}_{2}$ with masses $m_{1}$ and $m_{2}$, respectively. Define the new vector
$$
\textbf{r}=\textbf{r}_{1}-\textbf{r}_{2}
$$
giving the system of two differential equations
$$
\left\{ \begin{aligned} 
	m_{1}\ddot{\textbf{r}}_{1}=f(r)\hat{\textbf{r}} \\
	m_{2}\ddot{\textbf{r}}_{2}=-f(r)\hat{\textbf{r}} \\
\end{aligned} \right.
$$
The center of mass of the system is
$$
\textbf{R}_{cm}=\frac{m_{1}\textbf{r}_{1}+m_{2}\textbf{r}_{2}}{m_{1}+m_{2}}
$$
and stays fixed assuming the initial momentum is zero.
$$
\ddot{\textbf{R}}_{cm}=\textbf{0}
$$
We can write that
$$
\ddot{\textbf{r}}=\ddot{\textbf{r}}_{1}-\ddot{\textbf{r}}_{2}=(\frac{1}{m_{1}}+\frac{1}{m_{2}})f(r)\hat{\textbf{r}}
$$
Let the **reduced mass** be
$$
\mu=\frac{1}{\frac{1}{m_{1}}+\frac{1}{m_{2}}}=\frac{m_{1}m_{2}}{m_{1}+m_{2}}
$$
and substitute
$$
\mu\ddot{\textbf{r}}=f(\|\bf{r}\|)\hat{\textbf{r}}
$$
The angular momentum can be written as
$$
\textbf{L}=\textbf{r}\times\mu\dot{\textbf{r}}
=\mu r^{2}\dot{\theta}\hat{\textbf{z}}
$$
and only points perpendicular to the plane of motion. The bodies never leave this plane. The elemental area traced out by one body measured from the other is
$$
dA=\frac{r^{2}}{2}d\theta
$$
meaning that
$$
\frac{dA}{dt}=\frac{r^{2}}{2}\dot{\theta}=\frac{L}{2\mu}=\text{Const.}
$$
proving **Kepler's second law**. Subsituting in polar coordainates gives the system of two differential equations
$$
\left\{ \begin{aligned} 
	\mu(\ddot{r}-r\dot{\theta}^{2})=f(r) \\
	\mu(r\ddot{\theta}+2\dot{r}\dot{\theta})=0 \\
\end{aligned} \right.
$$
From this, we can write that the kinetic energy is
$$
K=\frac{1}{2}\mu v^{2}=\frac{1}{2}\mu(\dot{r}^{2}+r^{2}\dot{\theta}^{2})
$$
and the potential energy is
$$
U(r_{f})-U(r_{0})=-\int_{r_{0}}^{r_{f}}f(r)dr
$$
The constant $U(r_{0})$ doesn't really have any significance. We can then write the work-kinetic-energy theorem
$$
E=\frac{1}{2}\mu\dot{r}^{2}+\frac{1}{2}r^{2}\dot{\theta}^{2}+U(r)=\frac{1}{2}\mu\dot{r}^{2}+\frac{1}{2}\frac{L^{2}}{\mu r^{2}}+U(r)
$$
Now, we will simply define the **effective potential energy as**
$$
U_e(r)=\frac{1}{2}\frac{L^{2}}{\mu r^{2}}+U(r)
$$
and write our total energy as
$$
E=\frac{1}{2}\mu\dot{r}^{2}+U_{e}(r)
$$This holds for any kind of central force motion.
## Orbits

The eccentricity of an eliptical orbit is given from the formula
$$
\epsilon=\sqrt{1-\frac{b^{2}}{a^{2}}}=\sqrt{1-\frac{EL^{2}}{\mu(Gm_{1}m_{2})^{2}}}
$$
For a hyperbolic orbit, we can use the formula
$$
\epsilon=\sqrt{1+\frac{b^{2}}{a^{2}}}=\sqrt{1+\frac{EL^{2}}{\mu(Gm_{1}m_{2})^{2}}}
$$
