## 4/1/26

## Scalar Field (1st Type)

Recall [[7 Curves and Parametrization]].

Let $\textbf{c}:[a,b]\rightarrow U\subseteq\mathbb{R}^{n}$ be a smooth curve in $U$, and let $f:U\subseteq\mathbb{R}^{n}\rightarrow\mathbb{R}$ be a real-valued function. The **path integral** along $\textbf{c}$ of $f$ is given by
$$
\int_{c}fds=\int_{a}^{b}f(\textbf{c}(t))\|\textbf{c}'(t)\|dt
$$
- $ds=\|\textbf{c}'(t)\|dt$ is the infinitesimal arclength of the curve.
### Example

Let $\textbf{c}:[0,2\pi]\rightarrow\mathbb{R}^{3}$ be given by
$$
\textbf{c}(t)=
\begin{bmatrix}
\cos{(t)} \\
\sin{(t)} \\
t \\
\end{bmatrix}
$$
Let $f:\mathbb{R}^{3}\rightarrow\mathbb{R}$ be a real-valued function 
$$
f(
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
)=x+y+z
$$
The path integral of $f$ along $\textbf{c}$ is
$$
\int_{c} fds=\int_{0}^{2\pi}(\cos{(t)}+\sin{(t)}+t)\sqrt{1+t^{2}}dt
$$
We can cross out the $\sin{(t)}$ and $\cos{(t)}$ terms because the bounds go through one whole period, so the integral is zero.
$$
\int_{c} fds=\int_{0}^{2\pi}t\sqrt{1+t^{2}}dt
$$
and we get the final answer
$$
\frac{1}{3}((1+4\pi^{2})^{\frac{3}{2}}-1)
$$
## Vector Field (2nd Type)

### Dot Product

Let $\textbf{c}:[a,b]\rightarrow U\subseteq\mathbb{R}^{n}$ be a smooth curve in $U$, and let $\textbf{F}:U\subseteq\mathbb{R}^{n}\rightarrow\mathbb{R}^{n}$ be a vector-valued function. The **line integral** along $\textbf{c}$ of $\textbf{F}$ is given by
$$
\int_{c}\textbf{F}\cdot d\textbf{s}=\int_{a}^{b}\textbf{F}(\textbf{c}(t))\cdot\textbf{c}'(t)dt
$$
- $d\textbf{s}=\textbf{c}'(t)dt$ is the infinitesimal arclength vector of the curve.
### Cross Product

Let $\textbf{c}:[a,b]\rightarrow U\subseteq\mathbb{R}^{3}$ be a smooth curve in $U$, and let $\textbf{F}:U\subseteq\mathbb{R}^{3}\rightarrow\mathbb{R}^{3}$ be a vector-valued function. The orthogonal integral along $\textbf{c}$ of $\textbf{F}$ is given by
$$
\int_{c}\textbf{F}\times d\textbf{s}=\int_{a}^{b}\textbf{F}(\textbf{c}(t))\times\textbf{c}'(t)dt
$$
- $ds=\textbf{c}'(t)dt$ is the infinitesimal arclength vector of the curve.
### Example

Let $\textbf{c}:[a,b]\rightarrow\mathbb{R}^{3}$ be given by
$$
\textbf{c}(t)=
\begin{bmatrix}
t \\
t \\
0 \\
\end{bmatrix}
$$
Let $f:\mathbb{R}^{3}\rightarrow\mathbb{R}^{3}$ be a vector-valued function 
$$
\textbf{F}(
\begin{bmatrix}
x \\
y \\
z \\
\end{bmatrix}
)=
\begin{bmatrix}
y \\
4y^{3}-2x \\
z \\
\end{bmatrix}
$$
The work done on the object by a force $\textbf{F}$ along $\textbf{c}$ is
$$
\int_{c}\textbf{F}\cdot d\textbf{s}=\int_{a}^{b}
\begin{bmatrix}
5 \\
4t^{3}-2t \\
0 \\
\end{bmatrix}
\cdot
\begin{bmatrix}
1 \\
1 \\
0 \\
\end{bmatrix}
dt
=\int_{a}^{b}4t^{3}-2t+5dt
$$
This becomes
$$
b^{4}-b^{2}+5b-a^{4}+a^{2}+5a
$$
## Circulation

Let $\textbf{F}$ be a vector field on $\mathbb{R}^{n}$ and let $\textbf{c}$ be an oriented closed curve in $\mathbb{R}^{n}$. The **circulation** of $\textbf{F}$ is
$$
\oint_{\textbf{c}}\textbf{F}\cdot d\textbf{s}
$$
### Example

The enclosed current $I_{enc}$ inside a closed curve (**Amperian loop**) $\textbf{c}$ is given by the circulation of the magnetic field $\textbf{B}$ along that loop
$$
\oint_{\textbf{c}}\textbf{B}\cdot d\textbf{s}=\mu_{0}I_{enc} 
$$
- The **winding number** is the number of turns a closed curved does.
- The integral is denoted with a circle to indicate closure.

## [[3 Fundamental Theorem of Line Integrals]]