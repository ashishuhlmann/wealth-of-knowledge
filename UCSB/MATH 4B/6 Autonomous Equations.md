## 1/21/26

Differential equations where the derivative is a function of itself are called **autonomous**.
$$
y'=f(y)
$$
- If $y(t)$ is a solution, then $y(t+c$) is also a solution.

A value with $f(y_{0})=0$ is called an **equilibrium**.
- $y=y_{0}$ is a solution, but may not be the only solution at that point.
- If $f'(y)$ is continuous, the EUT applies and $y=y_{0}$ is the only solution to the IVP.
- If $y$ is between two equilibria, then the limits to infinity of $y(t)$ both exist.
- If $y$ has one equilibrium, atleast one of the limit to infinity exists.

If $f(y)>0$ for $a<y<b$: A solution y(t) with initial condition in this interval is strictly increasing.
If $f(y)<0$ for $a<y<b$: A solution y(t) with initial condition in this interval is strictly decreasing.

If $c$ is the largest equilibrium and a solution passes through $(t_{0}, y_{0})$ with $y_{0}\in(c,\infty)$.
- For $f(y)>0$ and $y>c$, a solution $y(t)$ is stricltly increasing with a limit to negative infinity equalling $c$.
If $d$ is the smallest equilibrium and a solution passes through $(t_{0}, y_{0})$ with $y_{0}\in(-\infty, d)$.
- For $f(y)<0$ and $y<d$, a solution $y(t)$ is stricltly decreasing with a limit to positive infinity equalling $c$.
## Stability

Let $a$ be an equilibrium. Consider $f(y)$ when $y$ is close to $a$.
- If $f(y)>0$ for $y>a$, and $f(y)<0$ for $y<a$, $y$ goes away from $a$ as $t$ goes to infinity. The equilibrium is **unstable**.
- If $f(y)<0$ for $y>a$ and $f(y)>0$ for $y<a$, $y$ goes toward $a$ as $t$ goes to infinity. This equilibirum is **asymoptotically stable**.
- If $f(y)>0$ or $f(y)<0$ for all $y\neq a$ near $a$, the equilibrium is **semistable**. This usually happens in polinomials with double roots.
## [[8 Linear Constants]]