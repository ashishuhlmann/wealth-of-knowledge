## 2/6/26

**Euler equations** are a family of differential equations whose solutions are linear combinations of two functions of $t$. They have the form
$$
t^{2}y''+\alpha ty'+\beta y=0\phantom{-}t>0
$$
One change of variable to consider is
$$
\begin{align}
x=\ln{(t)} \\
\frac{dx}{dt}=\frac{1}{t} \\
\frac{d^{2}x}{dt^{2}}=\frac{-1}{t^{2}} \\
\end{align}
$$
We know that
$$
\begin{align}
\frac{\frac{dy}{dt}}{\frac{dx}{dt}}=\frac{dy}{dx} \\
\end{align}
$$
So
$$
\frac{d^{2}y}{dx^{2}}+(\alpha-1)\frac{dy}{dx}+\beta y=0
$$
Now, we can solve it using polynomial and exponential functions, and substituting back the original variable.
### Example
$$
t^{2}y''+5ty'+3y=0\phantom{-}t>0
$$
Let $x=\ln{(t)}$.
$$
\frac{d^{2}y}{dx^{2}}+4\frac{dy}{dx}+3y=0
$$
$$
(\lambda+1)(\lambda+3)=0
$$
We can use a solution $y_{1}=e^{-x}$, so $y=ue^{-x}$. We use the formula
$$
y_{1}u''+(2y_{1}'+py_{1})u'=0
$$
to get
$$
\begin{align}
e^{-x}u''+(-2e^{-x}+4e^{-x})u'=0 \\
e^{-x}u''+2e^{-x}u'=0 \\
u''+2u'=0 \\
\end{align}
$$
We can solve that $u=c_{1}e^{-2x}+c_{2}$.
$$
y=c_{1}e^{-3x}+c_{2}e^{-x}
$$
Substituting $x=\ln{(t)}$ back gives
$$
y=c_{1}t^{-3}+c_{2}t^{-1}
$$
## [[13 Undetermibned Coefficients]]
