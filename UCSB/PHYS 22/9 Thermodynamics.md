
**temperature** - property of a system of particles in equilibrium related to the kinetic energy
- solid: masses on springs


**equilibrium**
- local section of the system is identical to any other part
- the average of all the motion is stationary

**linear expansion**
$$
\Delta L=\alpha L\Delta T
$$
where $\alpha$ is the coefficient of linear expansion
- For a 2-D surface, it will be $2\alpha$. For a 3-D object, it will be $3\alpha$. 
## Heat

Heat is a transfer of energy
- **Conduction**
- **Convection**
- **Radiation**

Suppose a slab of homogeneous material has two sides at different constant temperatures. The rate at which heat is transfered through the slab in watts is
$$
H=k\frac{A\Delta T}{x}=\frac{A\Delta T}{R}
$$
- $x$ is the thickness.
- $\Delta T$ is the temperature difference.
- $k$ is the thermal conductivity, and $R=\frac{x}{k}$ is the thermal resistivity.

**specific heat** - amount of energy needed to heat a substance by a certain temperature
$$
C=\frac{Q}{m\Delta T}
$$

$$
Q=m\int_{T_{0}}^{T_{F}}C(T)dT
$$
**latent heat** - heat transfer required for a phase change
$$
Q=Lm
$$
## Laws of Thermodynamics

0. If systems $A$ and $B$ are in equilibrium and systems $B$ and $C$ are in equilibrium, then $A$ and $C$ are in equilibrium.
1. The change in internal energy of a system is the sum of the change in heat and the work done on the system.
$$
\Delta E_{int}=Q+W
$$
- $Q$ is the heat transfered in or out of the system.
- $W$ is the work done on the system.

## Transition Processes For Ideal Gasses

In any thermodynamic process between equilibrium states $i$ and $f$, the quantity $Q+W$ has the same value for any path between $i$ and $f$. This quantity is equal to the change in value of a **state function** called the **internal energy** .

The internal energy of a gas from average translational kinetic energy in [[8 Gases]] is
$$
E_{int}=\frac{3}{2}nRT
$$
and
$$
\Delta E_{int}=\frac{3}{2}nR\Delta T
$$
The internal energy of an ideal gas depends only on its temperature.

**Theorem**: equipartion of energy

When the number of molecules is large, the average energy per molecule is $\nu=+\frac{1}{2}kT$ for each independent **degree of freedom**.
- monotomic gas: $E_{int}=\frac{3}{2}nRT$
- diatomic gas: $E_{int}=\frac{5}{2}nRT$
- polyatomic gas or solid: $E_{int}=3nRT$

Consider an ideal gas inside a cylinder with a moveable piston on top and a thermal bath that can transfer heat. The work done on the gas is
$$
W=-\int_{V_{0}}^{V_{f}} pdV
$$
- If the volume compresses, there is positive work done on the gas.
- If the volume increases, there is negative work done on the gas.

A **pressure-volume (pV) diagram** shows the path of a process with pressure on the vertical axis and volume on the horizontal axis. The magnitude of work done on the gas is the area under the curve. 
- For a closed loop, it is the area inside the loop.
### Isothermal Proccess

An **isothermal proccess** is one where the temperature remains constant.
- **isotherm** - corresponding hyperbolic curve of the path on the pV-diagram
$$
W=-\int_{V_{0}}^{V_{f}}\frac{nRT}{V}dV=-nRT\ln(\frac{V_{f}}{V_{0}})
$$
### Adiabatic Proccess

An **adiabatic proccess** is one where there is no heat transfer in or out of the system.
- It follows a parabola-like curve on the pV-diagram.
$$
W=-\int_{V_{0}}^{V_{f}}\frac{p_{0}V_{0}^{\gamma}}{V^{\gamma}}dV=\frac{1}{\gamma-1}(p_{f}V_{f}-p_{0}V_{0})
$$
$$
pV^{\gamma}=\text{Const.}
$$
$$
T_{0}V_{0}^{\gamma-1}=T_{f}V_{f}^{\gamma-1}
$$
$$
\gamma=\frac{C_{p}}{C_{V}}
$$
### Molar Heat Capacity at Constant Volume
$$
C_{V}=\frac{Q}{n\Delta T}=\frac{\Delta E_{int}}{n\Delta T}=\frac{\nu}{2}R
$$
- $\nu$ is the degrees of freedom
### Molar Heat Capacity at Constant Pressure
$$
C_{p}=C_{V}+R=\frac{\nu}{2}(R+1)
$$