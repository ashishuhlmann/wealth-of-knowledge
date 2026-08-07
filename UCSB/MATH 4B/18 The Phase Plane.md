## 3/9/26

Consider a system of two differential equations of $x_{1}$ and $x_{2}$: $\textbf{x}'(t)=\hat{A}\textbf{x}(t)$. The $x_{1}x_{2}$-plane is called the **phase plane**.
- Solutions all have distinct trajectories in the phase plane.
- The direction field at $\textbf{x}$ is $\hat{A}\textbf{x}$.
- The critical points are $\hat{A}\textbf{x}=\textbf{0}$.
## Critical Point Stability
### Real Eigenvalues

Let $\lambda_{1}$ and $\lambda_{2}$ be the eigenvalues of $\hat{A}$.
- If $\lambda_{1}>\lambda_{2}>0$, the point is a **nodal source**. It is unstable.
- If $\lambda_{1}<\lambda_{2}<0$, the point is a **nodal sink**. It is asymptotically stable.
- If $\lambda_{1}<0<\lambda_{2}$, the point is a **saddle point**. It is unstable. 
- If $\lambda_{1}=\lambda_{2}\neq0$ and $\hat{A}=\lambda\hat{I}$, it is a **proper node**. If $\hat{A}\neq\lambda\hat{I}$, it is an **improper node**. If $\lambda>0$ it is unstable, and if $\lambda<0$ it is asymptoptically stable.
### Complex Eigenvalues

Let $\lambda=\alpha\pm\boldsymbol{i}\beta$ be complex conjugate eigenvalues of $\hat{A}$.
- If $\alpha>0$, the point is a **spiral source**. It is unstable.
- If $\alpha<0$, the point is a **spiral sink**. It is asymptotically stable.
- If $\alpha=0$, the point is stable and solutions are periodic, circling around.
## [[19 Non-Homogeneous Systems]]
