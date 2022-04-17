# The Convolution Integral
Very often when we are doing [[Laplace Transforms#^374085|Laplace Transforms]], we come across a problem where we must take the [[Inverse Laplace Transforms#^3f32a7|Inverse Laplace Transform]] of a function of the form $$H(s)=F(s)G(s)$$
It is important to note that $\mathcal{L}^{-1}[H(s)]\neq\mathcal{L}^{-1}[F(s)]\mathcal{L}^{-1}[G(s)]$
>[!example] Definition: The Convolution Product
>Suppose $f$ and $g$ are continuous on the interval $[0, b]$. Then for $t$ in $(0,b]$ the **convolution product**, $f\ast g$, of $f$ and $g$ is defined by $$(f\ast g)(t) = \int_{0}^{t}f(t-\tau)g(\tau)d\tau$$
>The Integral above is called the **Convolution Integral**

>[!definition] Theorem: The Convolution Theorem
>If $f$ and $g$ are in [[Inverse Laplace Transforms#^9bead4|E(0, ∞)]], then $$\mathcal{L}[f\ast g]=\mathcal{L}[f]\mathcal{L}[g]$$
>Conversely,$$\mathcal{L}^{-1}[F(s)G(s)]=(f\ast g)(t)$$
>>[!info]- Proof of the Convolution Theorem
>>We must use the definiton of the convolution product to show that$$\mathcal{L}[(f\ast g)(t)]=\int_{0}^{\infty}\int_{0}^{t}e^{-st}f(t-\tau)g(\tau)d\tau dt$$
>>We can rewrite the iterated double integral and modify the order to obtain$$\mathcal{L}[(f\ast g)(t)]=\int_{0}^{\infty}\int_{\tau}^{\infty}e^{-st}f(t-\tau)g(\tau)dtd\tau$$
>>We now make a $u$-substitution, using $u=t-\tau$, so that $du=dt$$$\mathcal{L}[(f\ast g)(t)]=\int_{0}^{\infty}\int_{0}^{\infty}e^{-s(u+\tau)}g(\tau)f(u)dud\tau = \int_{0}^{\infty}e^{-s\tau}g(\tau)\left[\int_{0}^{\infty}e^{-su}f(u)du\right]d\tau=\left[\int_{0}^{\infty}e^{-su}f(u)du\right]\left[\int_{0}^{\infty}e^{-s\tau}g(\tau)d\tau\right]$$$$=\mathcal{L}[f]\mathcal{L}[g]$$

One application of the convolution integral is the **Volterra Integral**. 
>[!example] Definition: The Volterra Integral
>An equation of the form:$$x(t)=f(t)+\int_{0}^{t}k(t-\tau)x(\tau)d\tau$$
>where $f$ and $k$ are given

- the function $k$ is called the **kernel** of the function
- Our goal is, when given $k$ and $f$, to find $x(t)$
- We do this using laplace transforms

>[!example] Finding the Volterra Equation
>Take the Laplace Transform of both sides:$$X(s)=F(s)+\mathcal{L}[k(t)\ast x(t)]=F(s)+K(s)X(s)$$
>This can easily be simplified to  $$X(s) = \frac{F(s)}{1-K(s)}$$
>Then we simply take the inverse laplace transform to find what we are looking for:$$x(t)=\mathcal{L}^{-1}\left[\frac{F(s)}{1-K(s)}\right]$$