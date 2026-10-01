## 9/30/26

The charge density due to a point charge in space is
$$
\rho(\textbf{r})=q\delta(\textbf{r}-\textbf{r}_{0})
$$
The current density due to a moving point charge in space is
$$
\textbf{j}(\textbf{r})=q\textbf{v}(\textbf{r})\delta(\textbf{r}-\textbf{r}_{0})
$$
## Biot-Savart Law

The magnetic field from a moving charge $q$ at a distance $\textbf{r}$ is
$$
\textbf{B}=\frac{\mu_{0}}{4\pi}\frac{q\textbf{v}\times\textbf{r}}{r^{2}}
$$
- $\mu_{0}=4\pi\cdot10^{-7}$ is the magnetic constant.
$$
\oint_{\delta A}\textbf{B}\cdot d\textbf{s}=\mu_{0}\int_{A}\textbf{j}\cdot dA
$$

The magnetic field around a current carrying wire is
$$
\textbf{B}(\textbf{r})=\frac{\mu_{0}I}{2\pi r}\hat{\boldsymbol{\theta}}
$$

Generalizing to current density gives
$$
\textbf{B}(\textbf{r})=\frac{\mu_{0}}{4\pi}\int(\textbf{j}(\textbf{r})\times\frac{\textbf{r}-\textbf{r}'}{|\textbf{r}-\textbf{r}'|^{3}})d^{3}\textbf{r}'
$$
paralleling the electric field
$$
\textbf{E}(\textbf{r})=\frac{1}{4\pi\epsilon_{0}}\int\rho(\textbf{r})(\frac{\textbf{r}-\textbf{r}'}{|\textbf{r}-\textbf{r}'|^{3}})d^{3}\textbf{r}
$$
The force between two loops of wire on each other is
$$
\frac{\mu_{0}I_{1}I_{2}}{4\pi}\oint_{c_{1}}\oint_{c_{2}}d\textbf{r}_{1}\cdot d\textbf{r}_{2}\frac{\textbf{r}_{12}}{r_{12}^{3}}
$$
The force between two parallel current carrying wires on eachother is
$$
d\textbf{F}_{12}=\frac{\mu_{0}I_{1}I_{2}}{2\pi d}dz_{1}\hat{\textbf{x}}
$$