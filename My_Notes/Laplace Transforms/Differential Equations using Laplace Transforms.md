# Solving Differential Equations with Laplace Transforms
[[Laplace Transforms#^374085|Laplace Transforms]] are mainly used to solve differential equations, and provide a quick and easy way to reduce differentials

<u>**Theorem 10.4.1**</u>
Suppose $f$ is of [[Inverse Laplace Transforms#^565e2b|exponential order]] and that $f'$ exists and is [[Laplace Transforms#^10c23f|piecewise continuous]]. Then $\mathcal{L}[f']$ exists and is given by: $$\mathcal{L}[f']=s\mathcal{L}[f]-f(0)$$
>[!abstract]- Proof of Theorem 10.4.1
>$$\mathcal{L}[f']=\int_{0}^{\infty}e^{-st}f'(t)dt=\left[e^{-st}f(t)\right]_0^\infty+\int_{0}^{\infty}e^{-st}f(t)dt$$
>Notice that the rightmost term is simply the [[Laplace Transforms#^374085|Laplace Transform]] of $f$ and $e^{-st}$ goes to $0$ as $t$ goes to infinity. Therefore we can write this as $$\mathcal{L}[f']=s\mathcal{L}[f]-f(0)$$


<u>**Method to solve initial value problems**</u>
1. Take the [[Laplace Transforms#^374085|laplace transform]] of the equation, substituting for the derivative and initial values as needed
2. Solve the resulting equation algebraically for $Y(s)$
3. Take the [[Inverse Laplace Transforms#^3f32a7|inverse laplace transform]] of $Y(s)$ to determine the solution

>[!important]+ General Laplace Transform of Derivatives
>$$\mathcal{L}[f^{(n)}]=s^n\mathcal{L}[f]-s^{n-1}f(0)-s^{n-2}f'(0)-\cdots-sf^{(n-2)}(0)-f^{(n-1)}(0)$$