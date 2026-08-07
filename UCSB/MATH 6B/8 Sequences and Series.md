## 5/11/26

**sequence** - order of numbers $a_{1},a_{2},...a_{n}$

**series** - summation of a sequence $S_{n}=a_{1}+a_{2}+...+a_{n}$

**function series** - series that uses functions $f_{1}(x)+f_{2}(x)+...+f_{n}(x)$

The natural question is whether a series converges or diverges.
$$
S_{\infty}=\sum_{n=1}^{\infty}a_{n}
$$
1. $\textbf{p}$**-series test**
$$
\sum_{n=1}^{\infty}\frac{1}{n^{p}}
$$
- If $p>1$, the sum converges.
2. **ratio test** - Assume $L$ exists.
$$
L=\lim_{n\rightarrow\infty}\biggr|\frac{a_{n+1}}{a_{n}}\biggr|
$$
- If $L<1$, $S_{\infty}$ converges.
- If $L>1$, $S_{\infty}$ diverges.
- If $L=1$, $S_{\infty}$, the test is inconclusive.
3. **root test** - Assume $C$ exists.
$$
C=\lim_{n\rightarrow\infty}|a_{n}|^{\frac{1}{n}}
$$
- If $C<1$, $S_{\infty}$ converges.
- If $C>1$, $S_{\infty}$ diverges.
- If $C=1$, the test is inconclusive.
4. **comparison test**
$$
S_{b}=\sum_{n=1}^{\infty}b_{n}
$$
- If $S_{b}$ converges and $0\leq a_{n}\leq b_{n}\forall n$, then $S_{a}$ converges.
- If $S_{b}$ diverges and $0\leq b_{n}\leq a_{n}\forall n$, then $S_{a}$ diverges.
5. **geometric series**
$$
a_{n}=ar^{n},\phantom{-}a\neq0,\phantom{-}r\in\mathbb{R}
$$
- If $|r|<1$, $S_{\infty}$ converges.
6. **alternating series test**
$$
\sum_{n=1}^{\infty}(-1)^{n}a_{n}
$$
The sum converges iff
- $a_{n}$ are all positive or all negative.
- $|a_{n}|$ strictly decreases.
- $\displaystyle\lim_{n\rightarrow\infty}a_{n}=0$.
7. **integral test**
$$
\int_{0}^{\infty}a(x)dx
$$
- If the integral diverges, $S_{\infty}$ diverges.
## [[9 Fourier Series]]
