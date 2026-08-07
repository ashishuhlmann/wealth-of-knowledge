## 3/4/26

The general form of a system of linear first order ODE's with constant coefficients is
$$
\left\{ \begin{aligned} 
	\frac{dx_{1}}{dt}&=c_{1}x_{1}+c_{2}x_{2}+...+c_{n}x_{n}+c_{n+1} \\
	\frac{dx_{2}}{dt}&=c_{1}x_{1}+c_{2}x_{2}+...+c_{n}x_{n}+c_{n+1} \\
	&\vdots \\
	\frac{dx_{n}}{dt}&=c_{1}x_{1}+c_{2}x_{2}+...+c_{n}x_{n}+c_{n+1} \\
\end{aligned} \right.
$$
The general form of a system of linear first order ODE's is
$$
\left\{ \begin{aligned} 
	\frac{dx_{1}}{dt}&=p_{11}(t)x_{1}+p_{12}(t)x_{2}+...+p_{1n}(t)x_{n}+g_{1}(t) \\
	\frac{dx_{2}}{dt}&=p_{21}(t)x_{1}+p_{22}(t)x_{2}+...+p_{2n}(t)x_{n}+g_{2}(t) \\
	&\vdots \\
	\frac{dx_{n}}{dt}&=p_{n1}(t)x_{1}+p_{n2}(t)x_{2}+...+p_{nn}(t)x_{n}+g_{n}(t) \\
\end{aligned} \right.
$$
This can be written as the vector equation
$$
\textbf{x}'(t)=\hat{A}(t)\textbf{x}(t)+\textbf{b}(t)
$$
### Reduction of Order

Higher order differential equations can be written as systems of first order differential equations. Given a high order equation,
$$
y^{n}=F(t,y,y',...,y'^{..n-1..'})
$$
we can just define
$$
\begin{align}
x_{1}&=y \\
x_{2}&=y' \\
\vdots \\
x_{n}&=y^{n-1} \\
\end{align}
$$
Now we create the system of first order equations and solve it.
$$
\left\{ \begin{aligned} 
	\frac{dx_{1}}{dt}&=x_{2} \\
	\frac{dx_{2}}{dt}&=x_{3} \\
	\vdots \\
	\frac{dx_{n}}{dt}&=F(t,y,y',...,y'^{..n-1..'}) \\
\end{aligned} \right.
$$
### Example
$$
x'''+2\cos{(t)}x''-2t^3x'=-3\cos{(t)}
$$
$$
\frac{d}{dx}
\begin{bmatrix}
x \\
v \\
a \\
\end{bmatrix}
=
\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
0 & 2t^{3} & -2\cos{(t)} \\
\end{bmatrix}
\begin{bmatrix}
x \\
v \\
a \\
\end{bmatrix}
+\begin{bmatrix}
0 \\
0 \\
-3\cos{(t)} \\
\end{bmatrix}
$$
**Theorem**: Existence and Uniqueness

Let $\hat{A}(t)$ be an $n\times n$ matrix-valued function and $\textbf{b}(t)$ be an $n\times1$ vector-valued function. If $\hat{A}$ and $\hat{b}$ are both continuous on an open interval $I$ for every $t_{0}\in I$ and $x_{0}\in \mathbb{R}^{n}$, there is a unique vector-valued solution such that $\textbf{x}(t_{0})=\textbf{x}_{0}$.
$$
\textbf{x}'(t)=\hat{A}(t)\textbf{x}(t)+\textbf{b}(t)
$$
where $\hat{A}(t)$ is a matrix-valued function (in complex numbers).
## Matrix-Valued Functions
$$
\begin{bmatrix}
p_{11}(t) & p_{12}(t) & ... & p_{1n}(t) \\
p_{21}(t) & p_{22}(t) & ... & p_{2n}(t) \\
\vdots & \vdots & \ddots & \vdots \\
p_{n1}(t) & p_{n2}(t) & ... & p_{nn}(t) \\
\end{bmatrix}
$$
- Limits, derivatives, and continuity all exist iff they exist for all of the individual elements.
- Integrals and derivatives are applied to every element individually.

For two matrix-valued functions, the product rule follows the *specific order*
$$
(\hat{A}(t)\hat{B}(t))'=\hat{A}'(t)\hat{B}(t)+\hat{A}(t)\hat{B}'(t)
$$
## Solution Spaces

Let $\hat{A}(t)$ be an $n\times n$ matrix-valued function and $\textbf{b}(t)$ be an $n\times1$ vector-valued function.
$$
\textbf{x}'(t)=\hat{A}(t)\textbf{x}(t)+\textbf{b}(t)
$$
- All solutions are the sum of the homogenous part $\textbf{x}_{c}(t)$ and the particular part $\textbf{x}_{p}(t)$.
- All $\textbf{x}_{c}(t)$ form an $n$-dimensional function space.
### Homogeneous Constant Case
$$
\textbf{x}'(t)=\hat{A}\textbf{x}(t)
$$
If $\hat{A}$ is diagonal, we are solving a simple system of equations. If we diaganolize $\hat{A}$, we will get $\hat{A}$ between two identity matricies.
$$
\textbf{x}'(t)=\hat{Q}\hat{D}{Q}^{-1}\textbf{x}(t)
$$
- Let $\textbf{y}(t)=\hat{Q}^{-1}\textbf{x}(t)$. Then, $\textbf{y}'(t)=\hat{Q}^{-1}\textbf{x}'(t)$.
$$
\textbf{y}=
\begin{bmatrix}
e^{\lambda_{1}t} & 0 & ... & 0 \\
0 & e^{\lambda_{2}t} & ... & 0\\
\vdots & \vdots & \ddots & \vdots\\
0 & 0 & ... &e^{\lambda_{n}t} \\
\end{bmatrix}
\begin{bmatrix}
c_{1} \\
c_{2} \\
\vdots \\
c_{n} \\
\end{bmatrix}
=
\begin{bmatrix}
c_{1}e^{\lambda_{1}t} \\
c_{2}e^{\lambda_{2}t} \\
\vdots \\
c_{n}e^{\lambda_{n}t} \\
\end{bmatrix}
$$
- We only need to find $\hat{Q}$ and $\hat{D}$ to find all the solutions for $\textbf{x}$.

If $\hat{A}$ is atleast diagnolizable, then the solutions can be written in eigenvector form
$$
\textbf{x}=c_{1}\textbf{q}_{1}e^{\lambda_{1}t}+c_{2}\textbf{q}_{2}e^{\lambda_{2}t}+...+c_{n}\textbf{q}_{n}e^{\lambda_{n}t}
$$
If the eigenvectors $\textbf{z}$ have complex conjugate eigenvalues $\lambda=\alpha\pm\boldsymbol{i}\beta$. Then,
$$
\textbf{x}=c_{1}\textbf{z}e^{\alpha t}(\cos{(\beta t)+\boldsymbol{i}\sin{(\beta t)}})+c_{2}\textbf{z}^{*}e^{\alpha t}(\cos{(\beta t)-\boldsymbol{i}\sin{(\beta t)}})+...
$$
Using real vectors for a basis, we can define $\textbf{z}=\textbf{a}+\boldsymbol{i}\textbf{b}$ and multiply out
$$
\textbf{x}=c_{1}e^{\alpha t}(\cos{(\beta t)}\textbf{a}-\sin{(\beta t)}\textbf{b})+c_{2}e^{\alpha t}(\sin{(\beta t)}\textbf{a}+\cos{(\beta t)}\textbf{b})
$$
If $\hat{A}$ is not diagnolizable, and there is some repeated eigenvalue $\lambda$, then the solutions take the form
$$
\textbf{x}=c_{1}\textbf{q}_{1}e^{\lambda t}+c_{2}(\textbf{q}_{2}+t\textbf{q}_{1})e^{\lambda t}+...
$$
where $\textbf{q}_{2}$ is a vector that satisfies the equation $(\hat{A}-\lambda\hat{I})\textbf{q}_{2}=\textbf{q}_{1}$
### Example Problem
$\text{Solve the IVP.}$
$$
\textbf{x}'=
\begin{bmatrix}
1 & 1 \\
4 & -2 \\
\end{bmatrix}
\textbf{x}
$$
$$
\textbf{x}(0)=
\begin{bmatrix}
7 \\
2 \\
\end{bmatrix}
$$
1. 
$$
\begin{vmatrix}
1-\lambda & 1 \\
4 & -2-\lambda \\
\end{vmatrix}
=\lambda^{2}+\lambda-6=(\lambda+3)(\lambda-2)=0
$$
2. 
$$
\lambda=-3
$$
$$
\begin{bmatrix}
4 & 1 \\
4 & 1 \\
\end{bmatrix}
\textbf{q}_{1}=\textbf{0}
$$
$$
\left[
  \begin{matrix}
	1 & \frac{1}{4} \\
	0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		0 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
$$
\textbf{q}_{1}=c_{1}
\begin{bmatrix}
-\frac{1}{4} \\
1 \\
\end{bmatrix}
$$
$$
\lambda=2
$$
$$
\begin{bmatrix}
-1 & 1 \\
4 & -4 \\
\end{bmatrix}
\textbf{q}_{1}=\textbf{0}
$$
$$
\left[
  \begin{matrix}
	1 & -1 \\
	0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		0 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
$$
\textbf{q}_{2}=c_{2}
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
$$
$$
\textbf{x}(t)=c_{1}
\begin{bmatrix}
-\frac{1}{4} \\
1 \\
\end{bmatrix}
e^{-3t}+c_{2}
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
e^{2t}
$$
$$
\textbf{x}(0)=c_{1}
\begin{bmatrix}
-\frac{1}{4} \\
1 \\
\end{bmatrix}
+c_{2}
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
=
\begin{bmatrix}
7 \\
2 \\
\end{bmatrix}
$$
$$
\left[
  \begin{matrix}
	1 & 0 \\
	0 & 1 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		-4 \\
		6 \\
    \end{matrix}
  \right.
\right]
$$
$$
\textbf{x}(t)=-4
\begin{bmatrix}
-\frac{1}{4} \\
1 \\
\end{bmatrix}
e^{-3t}+6
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
e^{2t}
$$
### Example Problem
$\text{If }\textbf{x}'(t)=\hat{A}\textbf{x}(t)\text{ has a basis of solutions}$
$$
\textbf{x}_{1}(t)=
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
e^{-t},\phantom{-}
\textbf{x}_{2}(t)=
\begin{bmatrix}
1 \\
2 \\
\end{bmatrix}
e^{2t}
$$
$\text{find }\hat{A}.$
1. 
$$
D=
\begin{bmatrix}
-1 & 0 \\
0 & 2 \\
\end{bmatrix}
$$
$$
Q=
\begin{bmatrix}
1 & 1 \\
1 & 2 \\
\end{bmatrix}
$$
2. 
$$
Q^{-1}=
\begin{bmatrix}
2 & -1 \\
-1 & 1 \\
\end{bmatrix}
$$
3. 
$$
A=QDQ^{-1}=
\begin{bmatrix}
-4 & 3 \\
-6 & 5 \\
\end{bmatrix}
$$
### Example Problem
$\text{Solve the IVP.}$
$$
\textbf{x}'=
\begin{bmatrix}
-1 & -2 \\
2 & -1 \\
\end{bmatrix}
\textbf{x}
$$
$$
\textbf{x}(0)=
\begin{bmatrix}
1 \\
0 \\
\end{bmatrix}
$$
$$
\lambda^{2}+2\lambda+5=0
$$
$$
\lambda=-1\pm2\boldsymbol{i}
$$
2 - i
$$
\left[
  \begin{matrix}
	-2\boldsymbol{i} & -1 \\
	 1 & -2\boldsymbol{i} \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		0 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
$$
\textbf{x}=e^{-t}()
$$
### Example Problem
$\text{Solve the system of equations.}$
$$
\textbf{x}'=
\begin{bmatrix}
4 & -1 \\
1 & 2 \\
\end{bmatrix}
\textbf{x}
$$
1. 
$$
\begin{vmatrix}
4-\lambda & -1 \\
1 & 2-\lambda \\
\end{vmatrix}
=(\lambda-3)^{2}=0
$$
2. 
$$
\lambda=3
$$
$$
\begin{bmatrix}
1 & -1 \\
1 & -1 \\
\end{bmatrix}
\textbf{q}_{1}=\textbf{0}
$$
$$
\left[
  \begin{matrix}
	1 & -1 \\
	0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		0 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
$$
\textbf{q}_{1}=c_{1}
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
$$
3. 
$$(\hat{A}-\lambda\hat{I})\textbf{q}_{2}=\textbf{q}_{1}$$
$$
\left[
  \begin{matrix}
	1 & -1 \\
	0 & 0 \\
  \end{matrix}
  \left|
    \,
    \begin{matrix}
		1 \\
		0 \\
    \end{matrix}
  \right.
\right]
$$
$$
\textbf{q}_{2}=s
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
+
\begin{bmatrix}
1 \\
0 \\
\end{bmatrix}
$$
$$\text{Let }s=0\text{ knowing that we must make }\textbf{q}_{2}\neq\textbf{0}.$$
4. 
$$
\textbf{x}=c_{1}
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}e^{3t}+c_{2}(
\begin{bmatrix}
1 \\
0 \\
\end{bmatrix}
+t
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix})e^{3 t}
$$
## [[18 The Phase Plane]]