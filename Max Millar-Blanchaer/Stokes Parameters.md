The force on a charged particle $q_{2}$ due to another charged particle $q_{2}$ accelerating is
$$
\textbf{F}=\frac{-q_{1}q_{2}}{4\pi\epsilon_{0}c^{2}}\frac{1}{r}(t-\frac{r}{c})(\textbf{a}-\frac{\textbf{a}\cdot\textbf{r}}{\textbf{r}\cdot\textbf{r}}\textbf{r})
$$
- $\textbf{a}$ is the acceleartion of $q_{1}$.
- $t$ is the time since $q_{1}$ began accelerating.
- $r$ is ths distance between the charges.

A large group of charges all under simple harmonic motion will essentially produce pure sine wave oscillations of the electric field if they are sufficiently far away.

**linear polarization** - electric field oscillates along a line

**circular polarization** - electric field rotates along a circle
- **RH** - vector moves counter clockwise (looking at source)
- **LH** - vector moves clockwise (looking at source)
- the sum of right and left circular polarizations is linearly polarized light

**elliptical polarization** - electric field rotates along an ellipse
## Stokes Vector

A beam of elliptically polarized light can be characterized by four numbers.
$$
\textbf{S}=
\begin{bmatrix}
I \\
Q \\
U \\
V \\
\end{bmatrix}
\rightarrow
\begin{bmatrix}
1 \\
Q \\
U \\
V \\
\end{bmatrix}
$$
- $I$ is the total flux density of the light.
- Typically, we normalize everything by total intensity.
![[Elliptical Polarization]]
Suppose we had a beam of parallel monochromatic light and a linearly polarizing filter. It has a total flux intensity $F$. We orient the filter and four angles, 0°, 45°, 90°, and 135°, and measure the respective flux densities $F_{0}$, $F_{45}$, $F_{90}$, and $F_{135}$. 

The normalized $Q$ parameter is given by
$$
Q=\frac{F_{0}-F_{90}}{F}
$$
The normalized $U$ parameter is given by
$$
U=\frac{F_{45}-F_{135}}{F}
$$
The eccentricity of the polarization can be recovered by
$$
e_{c}^{2}=\frac{2\sqrt{Q^{2}+U^{2}}}{1+\sqrt{Q^{2}+U^{2}}}
$$
with the angle of the ellipse with respect to our polarizing filter as
$$
\tan{(2\theta)}=\frac{U}{Q}
$$
- It is much more practical to know the quadrant as well, so we will use
`theta = arctan2(U,Q)/2`

Next, we will place a filter that only passes through circularly polarized light (ex. linear polarizer and a quarter wave plate), and measure the flux intensity $F_{C}$.
$$
V=\frac{2F_{C}}{F}-1
$$
- The sign indicates the clockwise circular polarization.

The **degree of polarization**, assuming normalized terms can be written as
$$
p=\sqrt{Q^{2}+U^{2}+V^{2}}=\sqrt{V^{2}+\frac{e_{c}^{2}}{(2-e_{c}^{2})}}
$$
- $p=1$ for completely polarized light.
- $p<1$ for partially polarized light.

This suggests polarization state can be described as a vector in a $QUV$-space contained in what's called a **Poincaré sphere**.
![[Poincare Sphere]]
![[Stokes]]