## 1/12/26

A differential equation of first order has the form
$$
\frac{dy}{dx}=f(x,y)
$$
A **seperable differential equation** has the form
$$
M(x)+N(y)\frac{dy}{dx}=0
$$
Using differentials, we can multiply everything by $dx$.
$$
M(x)dx+N(y)dy=0
$$
Integrating both sides gives an *implicit* formula relating $x$ and $y$.
$$
\int M(x)dx+\int N(y)dy=0
$$
For an initial value problem, substituting the intial $x_{0}$ and $y_0$ values will give the specific relation that satisfies the intial conditions.
$$
\int_{y_{0}}^{y_{f}} N(y)dy=-\int_{x_{0}}^{x_{f}} M(x)dx
$$

Let $\mu(y)$ be *an* antiderivative of $N(y)$, and let $\nu(x)$ be an antiderivative of $M(x)$.
$$
M(x)+N(y)\frac{dy}{dx}=M(x)+\frac{d\mu}{dx}
$$
### Example

$\text{Solve }$
$$
\frac{dy}{dx}=ky
$$
1. 
$$
\int\frac{dy}{y}=\int kdx
$$
- *Note: This division assumes that* $y\neq0$ *. We will have to check this at the end.*
1. 
$$
\ln{|y|}=kx+\text{const}
$$
2. 
$$
y=e^{kx+\text{const}}=e^{\text{const}}e^{kx}=ce^{kx}
$$
- But we did not obtain the solution $y=0$ ! This is because we divided by $y$, and skipped this solution.
### Example

$\text{Solve }$
$$
\frac{dy}{dx}=1+y^{2}
$$
1. 
$$
\int\frac{dy}{1+y^{2}}=\int dx
$$
2. 
$$
\tan^{-1}{y}=x+c
$$
3. 
$$
y=\tan{(x+c)}
$$
- All solutions were found in this example.
## [[5 Change of Variable]]