## 2/6/26

Consider a general second order linear differential equation with non-constant coefficients
$$
y''+p(t)y'+q(t)y=0
$$
If $y_{1}$ is a non-zero solution, let
$$
u=\frac{y}{y_{1}}\Leftrightarrow y=y_{1}u
$$
The derivatives are
$$
y'=y_{1}u'+y_{1}'u
$$
and
$$
y''=y_{1}u''+2y_{1}'u'+y_{1}''u
$$
Equating this to the orginal differential equation, we can get that
$$
y_{1}u''+(2y_{1}'+py_{1})u'+(y_{1}''+py_{1}'+qy_{1})=0
$$
The last coefficient is zero by our assumption of $y_{1}$ being a solution.
$$
y_{1}u''+(2y_{1}'+py_{1})u'=0
$$This is a first order differential equation of $u'$. We can then solve it for $u$, and multiply by $y_{1}$ to get the final solution. 
- We can choose any starter solution $y_{n}$ to get the same answer.
### Example
$$
y''+3y'+2y=0
$$
The characteristic polynomial is
$$
\lambda^2+3\lambda+2=0
$$
where the roots are
$$
\begin{align}
\lambda=-1 \\
\lambda=-2 \\
\end{align}
$$
1. Using the first root, $y_{1}=e^{-t}$ is a solution, so we use $y=ue^{-t}$. Remember that $y_{1}\neq0$.
$$
y_{1}u''+(2y_{1}'+py_{1})u'=0
$$
Substituting gives
$$
\begin{align}
e^{-t}u''+(-2e^{-t}+3e^{-t})u'=0 \\
e^{-t}u''+e^{-t}u'=0 \\
u''+u'=0 \\
\end{align}
$$
That means that $u'=c_{1}e^{-t}$ and $u=-c_{1}e^{-t}+c_{2}$. So we get the general solution
$$
y=c_{1}e^{-2t}+c_{2}e^{-t}
$$
- Absorb the sign into $c_{1}$.
2. Using the second root, $y_{1}=e^{-2t}$ is a solution, so we use $y=ue^{-2t}$. Remember that $y_{1}\neq0$.
$$
y_{1}u''+(2y_{1}'+py_{1})u'=0
$$
$$
\begin{align}
e^{-2t}u''+(-4e^{-2t}+3e^{-2t})u'=0 \\
e^{-2t}u''-e^{-2t}u'=0 \\
u''-u'=0 \\
\end{align}
$$
That means that $u'=c_{1}e^{t}$ and $u=c_{1}e^{t}+c_{2}$. We get the same general solution
$$
y=c_{1}e^{-t}+c_{2}e^{-2t}
$$
### Example
$$
4y''+20y'+25y=0
$$
$$
\begin{align}
y(0)=1 \\
y'(0)=0 \\
\end{align}
$$
Dividing by $4$ gives
$$
y''+5y'+\frac{25}{4}y=0
$$
This is of the repeated root form $y''-2cy'+c^{2}y=0$ where $c=\frac{-5}{2}$.

So $y_{1}=(at+b)e^{(-\frac{5}{2}t)}$ is a solution. Let $y=u(at+b)e^{(-\frac{5}{2}t)}$. We use the formula
$$
y_{1}u''+(2y_{1}'+py_{1})u'=0
$$
to get
$$
\begin{align}
(at+b)e^{-(\frac{5}{2}t)}u''+(2(ae^{(-\frac{5}{2}t)}-\frac{5a}{2}te^{(-\frac{5}{2}t)}-\frac{5b}{2}e^{(-\frac{5}{2}t)})+5(at+b)e^{(-\frac{5}{2}t)})u'=0 \\
(at+b)e^{-(\frac{5}{2}t)}u''+(2ae^{(-\frac{5}{2}t)}-5ate^{(-\frac{5}{2}t)}-5be^{(-\frac{5}{2}t)}+5(at+b)e^{(-\frac{5}{2}t)})u'=0 \\
(at+b)u''+(2a-5at-5b+5(at+b))u'=0 \\
(at+b)u''+2au'=0 \\
u''+\frac{2a}{at+b}u'=0 \\
\end{align}
$$
With seperation of variables, we can get $u=\frac{c_{1}}{a(at+b)}+c_{2}$
$$
y=(\frac{c_{1}}{a(at+b)}+c_{2})(at+b)e^{(-\frac{5}{2}t)}
$$
By multiplying by $y_{1}$ and absorbing the constants, we get
$$
y=(c_{1}t+c_{2})e^{(-\frac{5}{2}t)}
$$
Then, we can use the intial conditions in a matrix to solve that
$$
\begin{align}
c_{1}&=\frac{5}{2} \\
c_{2}&=1 \\
\end{align}
$$
## [[12 Euler Equation]]
