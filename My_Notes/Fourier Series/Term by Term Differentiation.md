Interestingly, not all infinite series can be differentiated term by term, that is, it is not always true that
$$\frac{d}{dx}\sum\limits_{n=1}^{\infty}c_{n}u_{n}=\sum\limits_{n=1}^{\infty}c_{n}\frac{du_n}{dx}$$

>[!example] Differentiation Theorem
>A [[Intro To the Fourier Series#^0cc02e|fourier series]] that is continuous can be differentiated term by term if $f'(x)$ is [[Intro To the Fourier Series#^24448d|piecewise smooth]]
>s
>If $f(x)$ is [[Intro To the Fourier Series#^24448d|piecewise smooth]], then the [[Intro To the Fourier Series#^0cc02e|fourier series]] of a continuous function $f(x)$ can be differentiated term by term if $f(-L)=f(L)$

### Method of Eigenvalue Expansion
How do we put these theorems into practice? Consider the [[The Heat Equation#^f7f168|heat equation]] with zero boundary conditions at $x=0$ and $x=L$. 

In this example, the eigenfunctions are $\sin{n\pi x/L}$, suggesting the Fourier sine series:
$$u(x,t)=\sum\limits_{n=1}^{\infty}B_{n}(t)\sin{\frac{n\pi x}{L}}$$

The [[The Heat Equation#^84b5c4|initial condition]] $u(x,0)=f(x)$ is satisfied if
$$f(x)=\sum\limits_{n=1}^{\infty}B_{n}(0)\sin{\frac{n\pi x}{L}}$$

We determine an initial condition $B_n$ by using the [[Intro To the Fourier Series#^1c412e|orthogonality relations]] and get
$$B_{n}(0)=\frac{2}{L}\int_{0}^{L}f(x)\sin{\frac{n\pi x}{L}}dx$$

Then we plug the series into the heat equation, first justifying the term by term differentiation in order to get the partial derivatives.
$$\sum\limits_{n=1}^{\infty}B'_{n}(t)\sin{\frac{n\pi x}{L}}=-k\sum\limits_{n=1}^{\infty}\Big(\frac{n\pi}{L}\Big)^{2}B_{n}(t)\sin{\frac{n\pi x}{L}}$$

We can see that in order for the series to satisfy the heat equation, the coefficient equation must satisfy this ODE:
$$B'_{n}(t)=-k\Big(\frac{n\pi}{L}\Big)^{2}B_{n}(t)$$

This is an easily solvable first order linear ODE, meaning the solution is given by
$$B_n(t)=B_n(0)e^{-(n\pi/L)^{2}kt}$$
Where $B_n(0)$ is given by the above equation.

### Term by Term integration
>[!example] Term by Term Integration
>A [[Intro To the Fourier Series#^0cc02e|fourier series]] of a [[Intro To the Fourier Series#^24448d|piecewise smooth]] $f(x)$ can always be integrated term by term, and the result is a convergent infinite series that always converges to the integral of $f(x)$ for $-L\le x\le L$
>
>This new series may not be a fourier series, but it is continuous