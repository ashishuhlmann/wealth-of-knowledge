## 2/12/26

## Variation of Parameters

Suppose that the end of the spring is moving from a driving force and has a position of
$$
s(t)=s_{0}\cos{(\omega_{f}t)}
$$
That means that the total spring force on the mass is
$$
F_{s}=-k(x-s_{0}\cos{(\omega_{f} t))}
$$
The equation of motion is therefore
$$
m\ddot{x}+kx+b\dot{x}=\frac{f_{0}}{m}\cos{(\omega_{f}t)}
$$
Using the solutions to the homogeneous equation and [[14 Non-Homogeneous Equations]], we get that
$$
x(t)=\frac{f_{0}}{m(\lambda_{2}-\lambda_{1})}\biggr(\int-\cos(\omega_{f}t)e^{-\lambda_{1}t}dte^{\lambda_{1}t}+\int\cos(\omega_{f}t)e^{-\lambda_{2}t}dte^{\lambda_{2}t}\biggr)  \\
$$
Integrating gives
$$
x(t)=\frac{f_{0}}{m(\lambda_{2}-\lambda_{1})}\biggr(\frac{\lambda_{1}\cos{(\omega_{f} t)-\omega_{f}\sin{(\omega_{f} t)}}}{\omega_{f}^{2}+\lambda_{1}^{2}}
+\frac{\omega_{f}\sin{(\omega_{f} t)-\lambda_{2}\cos{(\omega_{f} t)}}}{\omega_{f}^{2}+\lambda_{2}^{2}}\biggr)+c_{1}e^{\lambda_{1}t}+c_{2}e^{\lambda_{2}t}
$$
But the initial condition terms together create a term that is simply the solution to the homogeneous equation. For early times, we can add on those solutions depending on whether it is underdamped, critically damped, or over damped. For very large times, the system approaches **steady state**, and we can approximate it very well by dropping off the intial condition term, as it approach zero exponentially.
$$
x(t\gg0)=\frac{f_{0}}{m(\lambda_{2}-\lambda_{1})}\biggr(\frac{\lambda_{1}\cos{(\omega_{f} t)-\omega_{f}\sin{(\omega_{f} t)}}}{\omega_{f}^{2}+\lambda_{1}^{2}}
+\frac{\omega_{f}\sin{(\omega_{f} t)-\lambda_{2}\cos{(\omega_{f} t)}}}{\omega_{f}^{2}+\lambda_{2}^{2}}\biggr)
$$
## Transient State

The **transient** state is the time in which the oscillator is still greatly impacted by initial conditions. The energy decays at this time
$$
E(t)\approx E_{0}e^{-\gamma t}
$$
## Steady State

The **steady state** is the behavior of the system after a long time has passed.

Substituting for the roots of the characteristic polynomial for $\lambda$, we get
$$
x(t)=f_{0}\frac{(k-m\omega_{f}^{2})\cos{(\omega_{f}t)}+b\omega_{f}\sin{(\omega_{f}t)}}{(k-m\omega_{f}^{2})^{2}+(b\omega_{f})^{2}}
$$
Now, substitute the parts of the root 
$$
\begin{align}
\gamma&=\frac{b}{m} \\
\omega^{2}&=\gamma^{2}+\omega_{0}^{2} \\
\omega_{0}^{2}&=\frac{k}{m}\\
\end{align}
$$
we get that
$$
x(t)=\frac{f_{0}}{m}\cdot\frac{(\omega_{0}^{2}-\omega_{f}^{2})\cos{(\omega_{f}t)}+\gamma\omega_{f}\sin{(\omega_{f}t)}}{(\omega_{0}^{2}-\omega_{f}^{2})^{2}+(\gamma\omega_{f})^{2}}
$$
Using a linear combination of sine and cosine, we can also write
$$
x(t)=\frac{f_{0}}{m}\cdot\frac{1}{\sqrt{(\omega^{2}-\omega_{f}^{2})^{2}+(\gamma\omega_{f})^{2}}}\cos{(\omega_{f}t+\phi)}
$$
### Near Resonant Frequency

When the driving force is near the resonant frequency, we can make the approximation that $\omega_{f}^{2}-\omega_{0}^{2}\approx2\omega_{0}(\omega_{0}-\omega_{f})$ and simplify our steady state equations to
$$
x(t)\approx\frac{f_{0}}{2m\omega_{0}}\cdot\frac{1}{\sqrt{(\omega_{0}-\omega_{f})^{2}+(\frac{\gamma}{2})^{2}}}\cos{(\omega_{f}t+\phi)}
$$
The energy of the system is then
$$
E\approx\frac{1}{2}k(\frac{f_{0}}{2m\omega_{0}})^{2}\cdot\frac{1}{(\omega_{0}-\omega_{f})^{2}+(\frac{\gamma}{2})^{2}}
$$
The stored energy in the system during steady state is
$$
E(\omega_{f})\approx\frac{1}{8}\frac{f_{0}^{2}}{m}\cdot\frac{1}{(\omega_{f}-\omega_{0})^{2}+(\frac{\gamma}{2})^{2}}=\pi E_{0}Q^{2}L(\omega_{f})
$$
But this is simply the product of three easy terms
$$
\begin{align}
E_{0}&=\frac{1}{2}\frac{f_{0}^{2}}{m\omega_{0}^{2}}=\frac{1}{2}\frac{f_{0}^{2}}{k} \\
Q^{2}&=\biggr(\frac{\omega_{0}}{\gamma}\biggr)^{2} \\
\pi L(\omega_{f})&=\frac{(\frac{\gamma}{2})^{2}}{(\omega_{f}-x_{0})^{2}+(\frac{\gamma}{2})^{2}} \\
\end{align}
$$
where $E_{0}$ is twice the kinetic energy of a free mass $m$ driven by the driving force $f_{0}\cos{(\omega_{f}t)}$, $Q$ is the quality factor, and $L(\omega_{f})$ is the **lineshape function** or **Lorentzian function**.

At resonance, $L(\omega_{f})=1$, the curve decreases to half of its peak value at $\omega_{f}-\omega_{0}=\pm\frac{\gamma}{2}$, which is the **full width at half maxmimum (FWHM)**.

The maximum stored energy is
$$
E_{max}=Q^{2}E_{0}
$$

$$
V=\frac{f_{0}^{2}\omega_{f}^{2}}{2\pi m^{2}}L(\omega^{2})\sin^{2}(\omega_{f}t+\phi)
$$
## [[15 Linear Algebra]]