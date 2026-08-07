## 2/9/26

Non-homogenous second order linear ODE's have the form
$$
y''+p(t)y'+q(t)y=r(t)
$$
The existence and uniqueness theorem still applies with the original conditions as well as the condition that $r(t)$ is continuous on the interval.
## Variation of Parameters
$$
y''+p(t)y'+q(t)y=r(t)
$$
Recall that if $p$, $q$, and $r$ are continuous, the full solution is simply the sum of the complementary solution and a particular solution to satisfy $r(t)$. There is a formula to get a particular solution when we know the solutions of the homegenous part.
$$
y_{c}''+p(t)y_{c}'+q(t)y_{c}=0
$$
Here, $y_{c}=c_{1}y_{1}+c_{2}y_{2}$ for constants $c_{1}$ and $c_{2}$, and $y_{1}$ and $y_{2}$ are solutions to the homogenous part. Assume that solutions to the non-homogeneous equation are of the form $u_{1}y_{1}+u_{2}y_{2}$ where $u_{1}$ and $u_{2}$ are functions of $t$.
$$
\begin{align}
y'&=u_{1}'y_{1}+u_{1}y_{1}'+u_{2}'y_{2}+u_{2}y_{2}' \\
y''&=u_{1}''y_{1}+u_{1}'y_{1}'+...
\end{align}
$$
Assume the constraint that
$$
u_{1}'y_{1}+u_{2}'y_{2}=0
$$
That makes
$$
\begin{align}
y'&=u_{1}y_{1}'+u_{2}y_{2}' \\
y''&=u_{1}y_{1}''+u_{2}y_{1}''+u_{1}'y_{1}'+u_{2}'y_{2}'
\end{align}
$$
Using the original differential equations gives $u_{1}'y_{1}'+u_{2}'y_{2}'=r(t)$ along with our constraint.
$$
\begin{bmatrix}
y_{1} & y_{2} \\
y_{1}' & y_{2}' \\
\end{bmatrix}
\begin{bmatrix}
u_{1} \\
u_{2}' \\
\end{bmatrix}
=
\begin{bmatrix}
0 \\
r(t) \\
\end{bmatrix}
$$
$$
\begin{align}
u_{1}'=\frac{-y_{2}r(t)}{W[y_{1},y_{2}]} \\
u_{2}'=\frac{y_{1}r(t)}{W[y_{1},y_{2}]} \\
\end{align}
$$
$$
y=\biggr(\int\frac{-y_{2}r(t)}{W[y_{1},y_{2}]}dt\biggr)y_{1}+\biggr(\int\frac{y_{1}r(t)}{W[y_{1},y_{2}]}dt\biggr)y_{2} \\
$$
### Example
$\text{Solve}$
$$
y''+4y=\tan(t)
$$
1. 
$$\text{The homogenous equation has two solutions making the general solution}$$
$$
y_{c}=c_{1}\cos{(2t)}+c_{2}\sin{(2t)}
$$
2. 
$$\text{The Wronskian is}$$
$$
W[y_{1},y_{2}]=
\begin{vmatrix}
\cos{(2t)} & \sin{(2t)} \\
-2\sin{(2t)} & 2\cos(2t) \\
\end{vmatrix}
=2
$$
3. 
$$\text{So we form}$$
$$
\begin{align}
u_{1}'=\frac{-\sin{(2t)}\tan{(t)}}{2} \\
u_{1}'=\frac{\cos{(2t)}\tan{(t)}}{2} \\
\end{align}
$$
4.
$$
y=\int\frac{-\sin{(2t)}\tan{(t)}}{2}dt\cos{(2t)}+\int\frac{\cos{(2t)}\tan{(t)}}{2}dt\sin{(2t)}
$$
$$
y=\int-\sin^{2}{(t)}dt\cos{(2t)}+\int\frac{\cos{(t)}\sin{(t)}-\sin^{2}{t}\tan{(t)}}{2}dt\sin{(2t)}
$$
$$
y=\frac{1}{2}(t-\sin{(t)}\cos{(t)}+c_{1})\cos{(2t)}+\frac{1}{2}(\ln{(\cos{(t)}-\cos^{2}{(t)})}+c_{2})\sin{(2t)}
$$
$$
y''+4y=\cos{(2t)}
y''+y=\sec{(t)}
$$
## [[4 Damped and Driven Oscillators]]