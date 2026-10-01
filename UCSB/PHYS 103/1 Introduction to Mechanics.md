## 9/28/26
## Three Dimensionless Constants

1. Speed
$$
\frac{v}{c}
$$
- $c$ is the speed of light.
- When $\frac{v}{c}\ll1$, **Newtonian mechanics** is sufficient. If $\frac{v}{c}\sim O(1)$, **special relativity** is needed.
2. Action
$$
\frac{\hbar}{s}
$$
- $s$ is the classical **action**.
- $\hbar$ is the smallest unit of action.
- When $\frac{\hbar}{s}\ll1$, classical mechanics is sufficient. If $\frac{\hbar}{s}\sim O(1)$, **quantum mechanics** is needed.
3. Gravity
$$
\frac{GM}{\pi c^{2}}
$$
- $G$ is the gravitational constant.
- When $\frac{GM}{\pi c^{2}}\ll1$, classical mechanics is sufficient. If $\frac{GM}{\pi c^{2}}\sim O(1)$, **general relativity** is needed.

|           | **slow**          | **fast**             |
| --------- | ----------------- | -------------------- |
| **small** | quantum mechanics | quantum field theory |
| **big**   | classical physics | special relativity   |
## Reference Frames

**reference frame** - set of coordinates to describe space
- **rest frame** - chosen **non-inertial** or non-accelerating frame

**Galilean transformation** - classical interpretation of inertial frames

If a frame $S'$ with coordinates $(\textbf{x}',t')$ is moving at a constant velocity $\textbf{v}$ with respect to a rest frame $S$ with coordinates $(\textbf{x},t)$, then the transformations from one frame to another are
$$
\begin{align}
\textbf{x}'&=\textbf{x}-\textbf{v}t \\
t'&=t
\end{align}
$$
with transformation matrix
$$
T_{x}^{x'}=
\begin{bmatrix}
1 & -\textbf{v} \\
0 & 1 \\
\end{bmatrix}
$$
and
$$
\begin{align}
\textbf{x}&=\textbf{x}'+\textbf{v}t \\
t&=t'
\end{align}
$$
with transformation matrix
$$
T_{x'}^{x}=
\begin{bmatrix}
1 & \textbf{v} \\
0 & 1 \\
\end{bmatrix}
$$