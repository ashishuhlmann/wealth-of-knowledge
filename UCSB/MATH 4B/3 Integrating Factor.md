## 1/9/25

A linear first order differential equation has the form
$$
y'+a(t)y=b(t)
$$
1. Find *an* antiderivative $A(t)$ of $a(t)$. All choices will lead to valid solutions.

2. Let $\mu(t)=e^{A(t)}$

$$
\mu'=ae^{A}=a\mu
$$
3. Notice that
$$
(\mu y)'=\mu(y'+ay)=\mu b
$$
4. Integrate both sides
$$
\mu y=\int\mu bdt
$$
$$
y=\frac{\int\mu bdt}{\mu}
$$
If there is a coefficient infront of the $y'$ term, simply divide both sides of the equation by that term.
### Example

$\text{Solve}$
$$
y'+2y=e^{4t}
$$
1. 
$$
\text{Let }\mu=e^{2t}
$$
2. 
$$
\int \mu b dt=\int2te^{4t}dt
$$
3. 
$$
u=2t, du=2dt, v=\frac{1}{4}e^{4t}, dv=e^{4t}dt
$$
$$
\int udv=uv-\int vdu=\frac{1}{2}e^{4t}(t-\frac{1}{4})
$$
$$
∴y=\frac{\int\mu bdt}{\mu}=\frac{e^{2t}(4t-1)}{16t}
$$
## [[4 Seperable Differential Equations]]