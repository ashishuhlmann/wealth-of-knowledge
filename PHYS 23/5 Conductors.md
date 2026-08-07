## 5/4/26

Charges can move freely through conductors, meaning that
1. The electric field inside a conductor is zero.
2. The electric field inside an empty cavity of a conductor is zero.
3. The electric flux is constant at all positions on the surface of a conductor.
4. The surface charge density on a conductor is constant.
- Charges must rearrange themselves until this relation is fulfilled.
5. The electric field is normal to the surface of a conductor with magnitude $\sigma/\epsilon_{0}$
6. The voltage is the same everywhere across a conductor.
- This means that the surface of a conductor is a level set of the electric field.

The total charge on a conductor is therefore
$$
Q=\epsilon_{0}\int_{S}\textbf{E}\cdot d\textbf{A}
$$
Outside a conductor, we know that $\nabla^{2}V$=0. To find $V$ everywhere, we need to find a $V$ that satisfies this equation and some given boundary conditions.

Everywhere outside a conductor, the there is no charge density, so the voltage satisfies Laplace's partial differential equation and meet some specific boundary conditions (eg. The voltage of the conductor is known, so its boundary is all the same voltage). 
$$
\nabla^{2}V=\frac{\partial^{2}V}{\partial x^{2}}+\frac{\partial^{2}V}{\partial y^{2}}+\frac{\partial^{2}V}{\partial z^{2}}=0
$$
**Theorem**: existence and uniqueness

Assuming that there is a solution $V(x,y,z)$ for a given set of conductors with potentials $V_{i}$ , this solution must be unique.
- There is only one unique solution $V(x,y,z)$ that will satisfy Laplace's equations and the boundary conditions.

## Capacitance

**capacitance** - ratio of the amount of charge on a conductor to its voltage
- property of a conductor based on geometry
- For two conductors of charges $\pm Q$, the capacitance is the ratio of that charge $Q$ to the voltage difference between the conductors.

### Energy Stored in a Capacitor
$$
E=\frac{1}{2}CV^{2}
$$
## [[6 Electric Current]]