## 2/9/26

A second order linear non-homogenous equation with constant coefficients has the form
$$
y''+ay'+by=r(t)
$$
- The general solution to this equation is the sum of the **complementary solution** $y_{c}$ and the **particular solution** $y_{p}$.
- The complementary solution is simply the solution to the homogeneous system.
### Guessing the Particular Solution

If $r(t)=P(t)e^{\alpha t}$ where $P(t)$ is a polynomial, then $y_{p}(t)$ should be $Q(t)e^{\alpha t}$ where $Q(t)$ is a polynomial of degree $Q$.
$$
Q(t)=a_{Q}t^{Q}+a_{Q-1}t^{Q-1}+...+a_{1}t+a_{0}
$$
- Plugging it back into the differential equation gives a system of linear equations to solve.

If $r(t)=P_{1}(t)e^{\alpha t}\cos{(\beta t)}+P_{2}(t)e^{\alpha t}\sin{(\beta t)}$ where $P_{1}(t)$ and $P_{2}(t)$ are polynomials, then $y_{p}(t)$ should be $Q_{1}(t)e^{\alpha t}\cos{(\beta t)}+Q_{2}(t)e^{\alpha t}\sin{(\beta t)}$ where $Q_{1}$ and $Q_{2}$ are polynomials.
- This is because of the complex exponential
$$
e^{(\alpha+\boldsymbol{i}\beta)}=e^{\alpha t}\cos{(\beta t)}+\boldsymbol{i}e^{\alpha t}\sin{(\beta t)}
$$
If $a$, $b$, $\alpha$, and $\beta$ are real and $\beta\neq0$, the degree of $Q_{1}$ and $Q_{2}$ are no more than $A+B$, where $A$ is the maximum of the degree of $P_{1}$ and $P_{2}$ and $B$ is the multiplicity of $\alpha+\boldsymbol{i}\beta$ in the roots of the characteristic polynomial $\lambda^{2}+a\lambda+b$.

If $r(t)=P(t)$ where $P(t)$ is a polynomial and $b\neq0$, then there is a solution $y_{p}(t)=Q(t)$ where $Q(t)$ is a polynomial of the same degree.
- If $a\neq0$ and $b=0$, the degree of $Q$ will be one more than the degree of $P$.
- If $a=0$ and $b=0$, the degree of $Q$ will be two more than the degree of $P$.
## [[14 Non-Homogeneous Equations]]