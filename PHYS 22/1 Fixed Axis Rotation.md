## 1/8/26

## Definitions

There is no well defined concept of an angular position vector $\vec{\theta}$. This is because rotations are not commutative like position vectors.
- We can still define an angular velocity vector that is the time derivative of angular position because as we take the limit to really small changes, the changes become commutatitive.
- In other words, *infinitesimal rotations* commute.

**psuedo vector** - quantity that transforms like a vector under rotation and translation (continuous rigid transformations), but flips direction under reflection, (a *discontinuous* rigid transformation)
## Describing Rotation

To begin, we will pick an *arbitrary* inertial coordinate system with position vector $\vec{R}$ and measure the physical quantities associated with some particle moving in space. 

**angular velocity** - psuedovector of magnitude equal to the **angular frequency** of rotation and direction perpendicular to the **instantaneous plane of rotation** ($\text{Hz}$)
$$
\vec{v}=\vec{\omega}\times\vec{R}
$$
**angular momentum** - psuedovector ($\text{Js}$)
$$
\vec{L}=\vec{R}\times\vec{p}
$$
**torque** - psuedovector ($\text{J}$)
$$
\vec{\tau}=\vec{R}\times\vec{F}
$$
- torque is the change in angular momentum over time
$$
\begin{align}
\frac{d\vec{L}}{dt}&=\frac{d\vec{R}}{dt}\vec{p}+\vec{R}\frac{d\vec{p}}{dt} \\
&=\vec{v}\times(m\vec{v})+\vec{R}\times{\vec{F}} \\
&=\vec{0}+\vec{\tau} \\
&=\vec{\tau}
\end{align}
$$
The **moment of inertia** or **second mass moment** is the measure of resistance to angular acceleration. For any point mass, the moment of inertia is
$$
I=MR^{2}
$$
Angular momentum can be rewritten as
$$
\vec{L}=I\vec{\omega}
$$
Torque can be rewritten as
$$
\vec{\tau}=I\alpha
$$
**Theorem:** parallel axis
$$
I'=I+ML^{2}
$$
When changing coordinate systems through translation, these quanities will change.
- The descriptions of motion are still valid from any coordinate system.

| Changes Under Translation  | Invariant Under Translation         |
| -------------------------- | ----------------------------------- |
| angular momentum $\vec{L}$ | angular velocity $\vec{\omega}$     |
| torque $\vec{\tau}$        | angular acceleration $\vec{\alpha}$ |
| moment of inertia $I$      |                                     |

## Rotational Kinetic Energy

$$
\begin{align}
T&=\sum_{i}\frac{1}{2}m_{i}v_{i}^{2} \\
&=\sum_{i}\frac{1}{2}m_{i}\omega_{i}^{2}r_{i}^{2} \\
&=\frac{1}{2}I\omega^2 \\
\end{align}
$$
## Rigid Bodies

**rigid body** - a dimensional object that does not deform

Extended objects or large collections of masses can be described a group of many tiny point masses.
$$
I=\sum_{i}m_{i}r_{i}^{2}\rightarrow\int_{M}r^{2}dm
$$
$$
\vec{L}=\sum_{i}\vec{r_{i}}\times\vec{p_{i}}\rightarrow\int_{M}\vec{r}\times \vec{v}dm
$$
- The total angular momentum on a system with no net torque is conserved.
$$
\vec{\tau}=\sum_{i}\vec{r_{i}}\times\vec{f_{i}}\rightarrow\int_{\vec{F}}\vec{r}\times d\vec{f}
$$
Extended objects tend to rotate about their **center of mass**.
$$
\vec{R_{c}}=\frac{\sum_{i}m_{i}\vec{r_i}}{\sum_{i}m_i}\rightarrow\frac{\int_{M}\vec{r}dm}{\int_{M}dm}
$$
### Point Masses and the Dirac Delta Function

A point mass $M$ can be in reverse be described as an extended object with an infinite spike of mass density
$$
\rho(\vec{x})=M\delta(\|\vec{x}-\vec{R}\|)
$$
## Translation and Rotation

**Theorem:** Chasles' Theorem
- It is always possible to represent an arbitrary displacement of a rigid body by a translation of its center of mass plus an **instintaneous rotation** around its center of mass.

The angular momentum of a rigid body is the sum of angular momentum due to rotation about the center of mass and the angular momentum due to motion of the mass with respect to an inertial coordinate system. With fixed-axis rotation about the $z$-axis the total angular momentum will only point in the $z$-direction.
$$
L_{z}=\sum_{i}\vec{r_{i}}\times m_{i}\vec{v_{i}}+(\vec{R_{c}}\times M\vec{v})_{z}
$$
- **spin term** - the total angular momentum in a coordinate system moving with the center of mass $\vec{r_{i}}\times m\vec{v_{i}}$
- the position $\vec{r_{i}}$ and velocity $\vec{v_{i}}$ are measured from the center of mass
- **orbital term** - the angular momentum about an inertial coordinate system $(\vec{R_{c}}\times M\vec{V})_{z}$

From differentiated the angular momentum with respect to time, we obtain that the torque is
$$
\tau_{z}=\sum_{i}\vec{r_{i}}\times m_{i}\vec{a_{i}}
$$
- Notice how this only has a spin term. The torque around the center of mass doesn't depend on the center of mass motion.
## [[2 Non-Fixed Axis Rotation]]