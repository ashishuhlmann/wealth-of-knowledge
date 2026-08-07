## 3/3/26
## Ideal Gases

An **ideal gas** has the following properties:
- made of particles that obey $\textbf{F}=m\textbf{a}$
- large number of particles
- forces between particles can be ignored (density is low)
- completely elastic collisions

The pressure on the walls of a container of an ideal gas is
$$
p=\frac{\rho}{3}\langle v^{2}\rangle
$$
- $\rho$ is the density.
- $\langle v^{2}\rangle$ is the average square of the speed of particles.

The **ideal gas law** is
$$
pV=Nk_{B}T=nRT
$$
- $N$ is the number of particles.
- $k_{B}\approx1.3806\cdot10^{-23}\frac{\text{J}}{\text{K}}$ is the Boltzmann constant.
- $n=\frac{N}{N_{a}}$ is the number of moles of particles.
- $R=N_{a}k_{B}=8.314\frac{\text{J}}{\text{K}\cdot\text{mol}}$ is the Boltzmann constant times one mole.
- $N_{a}\approx6.022\cdot10^{23}$ is Avogrado's constant.

The mass of any molecule is the sum of the masses of the atoms in **atomic mass units**. The **molar mass** of any molecule is that same number.
$$
1\text{amu}=\frac{1\text{g}}{\text{mol}}
$$
$$
1\text{mol}\approx6.022\cdot10^{23}
$$
**mean free path** - how far a particle goes on average before coliding
$$
\lambda=\frac{kT}{\sqrt{2}\pi d^{2}p}\approx\frac{kT}{\pi d^{2}p}
$$
- $T$ is temperature
- $d$ is the diameter of the particle
- $p$ is the pressure.
- If assuming that all other particles are stationary in the derivation, it simplifies to the expression without $\sqrt{2}$.
- If $\frac{\lambda}{d}$ is pretty large, the gas is ideal.

## Speed Distribution

**Maxwell-Boltzmann distribution** - probability distribution function of speeds for an ideal gas
$$
P(v)=4\pi \biggr(\frac{m}{2\pi k_{B}T}\biggr)^{\frac{3}{2}}v^{2}\exp{\biggr(\frac{-mv^{2}}{2k_{B}T}\biggr)}
$$
- $m$ is the mass of a molecule.
- $T$ is the temperature.

Recall that integrating across every speed gives
$$
\int_{0}^{\infty} P(v)dv=100\%
$$
The expected speed for any given particle is
$$
\langle v\rangle=\int_{0}^{\infty}vP(v)dv=\sqrt{\frac{8k_{B}T}{\pi m}}=\sqrt{\frac{8RT}{\pi M}}
$$
- $v$ is some particular speed
- $P(v)dv$ is the elemental probablity of that speed ocurring
- $m$
- $M$ is the molar mass of the molecules
- $m$ is the mass of a molecule.

The mean square of the speed is
$$
\langle v^{2}\rangle=\int_{0}^{\infty}v^{2}P(v)dv=\frac{3k_{B}T}{m}=\frac{3RT}{M}
$$
$$
\frac{k_{B}T}{m}=\frac{RT}{M}=\frac{p}{\rho}
$$
- $v^{2}$ is some particular square speed
- $P(v)dv$ is the elemental probablity of that speed ocurring
- $m$ is the mass.
- $M$ is the molar mass.

The **root mean squares (RMS)** speed is $\sqrt{\langle v^{2}\rangle}$.

The **mode** or **most probable speed** is the speed at which $P(v)$ is maximized.
$$
v=\sqrt{\frac{2k_{B}T}{m}}=\sqrt{\frac{2RT}{M}}
$$
## Energy Distribution

Consider monatomic gases that only have translational kinetic energy (as opposed to rotation).

**Maxwell-Boltzmann distribution** - probability distribution function of energies for an ideal gas
$$
P(E)=\frac{2}{\sqrt{\pi}}\cdot\frac{1}{(k_{B}T)^{\frac{3}{2}}}\sqrt{E}\exp{(\frac{-E}{k_{B}T})}
$$
- $\exp{(\frac{-E}{k_{B}T})}$ is the **Boltzmann factor**, or a rough estimate of the relative probability for a particle to have energy $E$ in a given system at temperature $T$.

The average translational kinetic energy per molecule is
$$
\langle K\rangle=\frac{3}{2}k_{B}T
$$
**degrees of freedom** - degrees in which particles can have kinetic energy
- There are three degrees of freedom for translational kinetic energy in 3-D space
## Non-Ideal Gases
### Virial Expansion
$$
pV=nRT\biggr(1+B_{1}(\frac{n}{V})+B_{2}(\frac{n}{V})^{2}+...\biggr)
$$
- $B_{i}$ are the **virial coefficients**, or functions of temperature.
- Virial coefficients are experimentally calculated.

Rotation does not change the temperature of a gas.
### van der Walls Equation
$$
(p+a\frac{n^{2}}{V^{2}})(V-bn)=nRT
$$
- $a$ and $b$ are the coefficients determined by experiment.

The volume correction is
$$
b=\frac{1}{2}N_{a}(\frac{4}{3}\pi d^{3})
$$
- $d$ is the diameter of the molecule
## [[9 Thermodynamics]]