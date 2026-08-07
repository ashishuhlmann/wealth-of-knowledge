## 3/12/26
## The Fundamental Matrix
$$
\textbf{x}'(t)=\hat{A}(t)\textbf{x}(t)
$$
Arranging the basis of solutions gives the **fundamental matrix**.
$$
\hat{\Psi}=\begin{bmatrix}
\textbf{x}_{1} & \textbf{x}_{2} & ... \textbf{x}_{n} \\
\end{bmatrix}
$$
- The determinant is non-zero.
- All solutions have the form $\textbf{x}=\hat{\Psi}\textbf{c}$.
## Abel's Formula
$$
W'(t)=\text{trace}(\hat{A})W(t)
$$
- If $\hat{A}$ is continuous on some open interval $I$, the Wronskian is either identically zero or never zero.
## Variation of Parameters

Consider the differential equation on an open interval $I$.
$$
\textbf{x}'(t)=\hat{A}(t)\textbf{x}(t)+\textbf{b}(t)
$$
Let $\hat{\Psi}(t)$ be the fundamental matrix of the homogeneous part $\textbf{x}_{c}'(t)=\hat{A}(t)\textbf{x}_{c}(t)$. The general solution is then $\textbf{x}(t)=\hat{\Psi}(t)\textbf{u}(t)$ where
$$
\textbf{u}(t)=\int(\hat{\Psi}(t))^{-1}\textbf{b}(t)dt
$$
### Example Problem
$\text{Solve the differential equation.}$
$$
\textbf{x}'=
\begin{bmatrix}
3 & 1 \\
1 & 3 \\
\end{bmatrix}
\textbf{x}+
\begin{bmatrix}
e^{2t} \\
e^{2t} \\
\end{bmatrix}
$$
1. 
$$
\begin{vmatrix}
3-\lambda & 1 \\
1 & 3-\lambda \\
\end{vmatrix}
=(\lambda-4)(\lambda-2)=0
$$
2. 
$$\lambda=4$$
$$
\begin{bmatrix}
-1 & 1 \\
1 & -1 \\
\end{bmatrix}
\textbf{q}_{1}=\textbf{0}
$$
$$
\left[
  \begin{matrix}
	-1 & 1 \\
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
\textbf{q}_{1}=s
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
$$
$$
\textbf{x}_{1}=
\begin{bmatrix}
1 \\
1 \\
\end{bmatrix}
e^{4t}
$$
3. 
$$\lambda=2$$
$$
\begin{bmatrix}
1 & 1 \\
1 & 1 \\
\end{bmatrix}
\textbf{q}_{1}=\textbf{0}
$$
$$
\left[
  \begin{matrix}
	1 & 1 \\
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
\textbf{q}_{2}=s
\begin{bmatrix}
-1 \\
1 \\
\end{bmatrix}
$$
$$
\textbf{x}_{2}=
\begin{bmatrix}
-1 \\
1 \\
\end{bmatrix}
e^{2t}
$$
4. 
$$
\hat{\Psi}=
\begin{bmatrix}
e^{4t} & -e^{2t} \\
e^{4t} & e^{2t} \\
\end{bmatrix}
$$
$$
\hat{\Psi}^{-1}=
\frac{1}{2}
\begin{bmatrix}
e^{-4t} & e^{-4t} \\
-e^{-2t} & e^{-2t} \\
\end{bmatrix}
$$
5. 
$$
\textbf{u}(t)=\frac{1}{2}\int
\begin{bmatrix}
e^{-4t} & e^{-4t} \\
-e^{-2t} & e^{-2t} \\
\end{bmatrix}
\begin{bmatrix}
e^{2t} \\
e^{2t} \\
\end{bmatrix}
dt=
\int
\begin{bmatrix}
e^{-2t} \\
0 \\
\end{bmatrix}
dt
=\frac{1}{-2}
\begin{bmatrix}
e^{-2t} \\
0 \\
\end{bmatrix}
+\textbf{c}
$$
6. 
$$
\begin{align}
\textbf{x}(t)&=
\begin{bmatrix}
e^{4t} & -e^{2t} \\
e^{4t} & e^{2t} \\
\end{bmatrix}
\biggr(\frac{1}{-2}
\begin{bmatrix}
e^{-2t} \\
0 \\
\end{bmatrix}
+\textbf{c}
\biggr) \\
&=
\frac{1}{-2}
\begin{bmatrix}
e^{2t} \\
e^{2t} \\
\end{bmatrix}
+
\begin{bmatrix}
e^{4t}-e^{2t} \\
e^{4t}+e^{2t} \\
\end{bmatrix}
\textbf{c}
\end{align}
$$
## Integrating Factor

For a constant matrix equation
$$
\textbf{x}'(t)+\hat{A}\textbf{x}(t)=\textbf{b}(t)
$$
The solution is the **matrix exponential**
$$
\textbf{x}(t)=\exp{(-\hat{A} t)}\int\exp{(\hat{A} t)}\textbf{b}(t)dt
$$
### Taking the Exponential

If $\hat{M}$ is a diagonal matrix,
$$
\exp{(\hat{M}t)}=
\begin{bmatrix}
e^{\lambda_{1}t} & 0 & ... & 0 \\
0 & e^{\lambda_{2}t} & ... & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & ... & e^{\lambda_{n}t} \\
\end{bmatrix}
$$
If $\hat{M}$ is a diaganolizable matrix,
$$
\exp{(\hat{M}t)}=Q\exp{(\hat{D}t)}Q^{-1}
$$
If $\hat{M}$ is a two by two non-diagnolizable matrix,
$$
\exp{(\hat{M}t)}=e^{\lambda t}
\begin{bmatrix}
1 & t \\
0 & 1 \\
\end{bmatrix}
$$