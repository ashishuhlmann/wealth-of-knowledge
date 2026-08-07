## 5/20/26

**Mechanical waves** need a medium and originate through an original displacement.
- The medium itself does not propegate. The final displacement of any one particle is zero.
- **transverse waves** - medium displacement direction is perpendicular to the propegation direction
- **longitudinal wave** - medium displacement direction is parallel to the propegation direction

For a waveform of shape $f(x)$ traveling at a **phase velocity** $v$, the whole medium can be described by
$$
y(x,t)=f(x')=f(x-vt)
$$
- **harmonic wave** - wave in which $f$ is sinusoidal
## Transverse Harmonic Waves

A transverse harmonic wave is is characterized by
$$
y(x,t)=y_{max}\sin{(\frac{2\pi}{\lambda}(x-vt))}=y_{m}\sin{(kx-\omega t)}
$$
- $\lambda$ is the **wavelength**.
- $v$ is the phase velocity.
- $k$ is the **angular wave number**.
- $\omega$ is the angular frequency.

Such a wave has both *temporal* and *spacial* characteristics, beginning with its period $T$ and wavelength $\lambda$. These are characteristic lengths of the wave in time and space, respectively.

We invert these measures into characteristic frequencies of the wave, where $\nu=\frac{1}{T}$. (A frequency analogue for the wavelength, $\frac{1}{\lambda}$, is not really needed for anything.) Next, we convert the amount of wave *cycles* per unit of time and space into the amount of *radians* per unit of time and space, where $2\pi$ radians make one complete wave cycle.
$$
\omega=\frac{2\pi}{T}\phantom{--}k=\frac{2\pi}{\lambda}
$$
$$
v=\lambda f=\frac{\omega}{k}
$$
$$
\lambda=vT
$$
$$
\nu=\frac{\omega}{2\pi}=\frac{v}{\lambda}
$$
The transverse velocity of an individual particle in the medium is obsviously
$$
\frac{\partial y}{\partial t}=-y_{m}\omega\cos{(kx-\omega t)}
$$
Then, the transverse acceleration is
$$
\frac{\partial^{2} y}{\partial t^{2}}=-y_{m}\omega^{2}\sin{(kx-\omega t)}
$$so $y$ satisfies the partial differential equation
$$
\frac{\partial^{2} y}{\partial t^{2}}=-\omega^{2}y
$$
## Phase

- $\phi = kx-\omega t$ is called the **phase**.

## Strings

The speed of a wave on a string of linear mass density $\mu$ under tention $F$ is
$$
v=\sqrt{\frac{F}{\mu}}
$$
## Wave Equation

The general equation of a wave is
$$
\frac{\partial^{2} U}{\partial^{2} t}=v^{2}\nabla^{2}U
$$
- Since the equation is linear, the sum of any two solutions is also a solution.
## Energy

The rate at which energy is transmitted by a mechanical wave is
$$
\frac{dE}{dt}=\mu\omega^{2}y_{m}^{2}v\cos^{2}{(kx-\omega t)}
$$

$$
\bar{P}=\frac{1}{P}\int_{0}^{T}\frac{dE}{dt}dt
$$
The average power over many wave cycles is
$$
\frac{1}{2}\mu\omega^{2}y_{m}^{2}v
$$
Addition
$$
y_{m}\sin{(kx-\omega t-\varphi)}
$$
$$
2y_{m}\cos{(\frac{1}{2}\Delta\varphi)}\sin{(kx-\omega t-\frac{1}{2}(\varphi_{1}+\varphi_{2}))}
$$Standing wave
$$
y_{m}\sin{(kx\pm\omega t)}
$$
$$
2y_{m}\sin{(kx)}\cos({\omega t})
$$
Sound waves
pressure, density, velocity are in phase
displacement is out of phase

speed of sound
$$
v=\sqrt{\frac{B}{\rho_{0}}}
$$
[[6 Fluid Basics]] - bulk modulus

observer moves
$$
f'=f(1\pm\frac{v_{O}}{v})
$$
+motion towards source
-motion away from source

source moves
$$
f'=f\frac{v}{v\pm v_{s}}
$$
-motion towards observer
+motion away from observer

both move: observer hears a frequency:
$$
f'=f\frac{v\pm v_{O}}{v\pm v_{S}}
$$
top: + bottom: - they move towards each other
top: - bottom: + they move away from each other

Formula sheet
$$
\frac{1}{1\pm\epsilon}\approx1\mp\epsilon
$$
$$
(1+\epsilon)^{\alpha}\approx1+\alpha\epsilon
$$
polar gradient
$$
\frac{\partial f}{\partial r}\hat{\textbf{r}}+\frac{1}{r}\frac{\partial f}{\partial\theta}\hat{\boldsymbol{\theta}}
$$
