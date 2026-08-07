## 1/14/26
## Change of Variable

Some differential equations are of the form
$$
\frac{dy}{dx}=f(\frac{y}{x})
$$
Let $z=y/x$, meaing $y=zx$.
$$
\frac{dy}{dx}=\frac{d}{dx}xz=z+x\frac{dz}{dx}
$$
Then, the equation becomes
$$
x\frac{dz}{dx}=f(z)-z
$$
which is seperable
$$
\frac{dz}{f(z)-z}=\frac{dx}{x}
$$
### Example

$\text{Solve}$
$$
\frac{dy}{dx}=\frac{-4x+y}{x-y}
$$
1. 
$$
\frac{dy}{dx}=\frac{-4+\frac{y}{x}}{1-\frac{y}{x}}
$$
2. 
$$\text{Let }z=\frac{y}{x}$$
$$
\frac{dy}{dx}=\frac{-4+z}{1-z}
$$
3. 
$$
x\frac{dz}{dx}=\frac{-4+z}{1-z}-z=\frac{z^{2}-4}{1-z}
$$
4. 
$$
\frac{1-z}{z^{2}-4}dz=\frac{dx}{x}
$$
5. 
$$
\int\frac{-3}{4(z+2)}-\frac{1}{z-2}dz=\int\frac{dx}{x}
$$
6. 
$$
\frac{-3}{4}\ln{|z+2|}-\ln{|z-2|}=\ln{|x|}+c
$$
7. 
$$
\frac{-3}{4}\ln{|\frac{y}{x}+2|}-\ln{|\frac{y}{x}-2|}=\ln{|x|}+c
$$
### Example Problem

$\text{Solve}$
$$
\frac{dy}{dx}=\frac{y}{x}+e^{\frac{y}{x}}
$$
1. 
$$\text{Let }z=\frac{y}{x}$$
2. 
$$
x\frac{dz}{dx}=z+e^{z}-z=e^{z}
$$
3. 
$$
\int e^{-z}dz=\int\frac{dx}{x}
$$
4. 
$$
-e^{-z}=\ln{|x|}+C
$$
5. 
$$
-e^{-\frac{y}{x}}=\ln{|x|}+C
$$
## [[6 Autonomous Equations]]
