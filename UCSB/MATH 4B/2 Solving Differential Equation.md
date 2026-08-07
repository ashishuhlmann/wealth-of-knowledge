## 1/7/26

Goal: find all functions $y$ (on a given domain) such that the equation is verified
- usually, we consider the domain in $\mathbb{R}$ in intervals or unions of intervals
- even if the equation is defined on the whole interval, the solution may not extend on the entire interval

**initial value problem** - differential equation with an initial condition
- solutions to such a problem are expected to be defined on an interval containing the point and must pass through the point
## Constant Function

The only solution to $y'=0$ is a constant function by the fundamental theorem of calculus part I.
## Exponential Function

We know that $y'-y=0$ has solutions of the form $y_{t}(t)=ce^{t}$ for all constants $c$.

$\text{Prove that this form is the only solution.}$

1. 
$$\text{Let}$$
$$
u(t)=\frac{y(t)}{y_{1}(t)}=\frac{y(t)}{e^{t}}
$$
$$
y(t)=e^{t}u(t)
$$

$$\text{Plug in }y(t)\text{ back into the differential equation.}$$
$$
(e^{t}u(t))'-e^{t}u(t)=0
$$
$$
e^{t}u(t)+e^{t}u'(t)-e^{t}u(t)=0
$$
$$e^{t}\text{ is never zero, so we can divide.}$$
$$
u(t)+u'(t)-u(t)=0
$$
$$
u'(t)=0
$$
$$∴\text{u is a constant function, so the form }ce^{t}\text{ is the only solution.}$$
## [[3 Integrating Factor]]
