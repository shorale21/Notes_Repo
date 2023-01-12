>[!example] Definition: Boundary Value Problem
>A boundary value problem consists of a linear homogenous differential equation, with corresponding linear homogenous boundary conditions. A general form for common ones is here:
>$$\frac{d}{dx}\bigg(p\frac{d\phi}{dx}\bigg)+q\phi+\lambda\sigma\phi=0$$
>Where $\lambda$ is the eigenvalue.
>This is known as the **Sturm-Liouville Differential Equation**

## The Sturm-Liouville Problem
The regular sturm-liouville problem consists of the above equation and the boundary conditions:
$$\beta_1\phi(a)+\beta_2\frac{d\phi}{dx}(a)=0$$
$$\beta_1\phi(b)+\beta_2\frac{d\phi}{dx}(b)=0$$
Where $\beta_i$ are real. $p,q,$ and $\sigma$ must be real and continuous everywhere, and $p>0$ and $\sigma>0$ everywhere.

We now turn to the Sturm-Liouville Theorems. For any regular sturm-liouville problem, the following theorems are valid:
1. All the eigenvalues $\lambda$ are real
2. There exist an infinite number of eigenvalues
	1. There is a smallest eigenvalue, but there is no largest eigenvalue
3. There is an eigenfunction, denoted $\phi_{n}(x)$ corresponding to each eigenvalue $\lambda_n$. $\phi_{n}(x)$ has exacty $n-1$ zeros for $a<x<b$.
4. The eigenfunctions form a complete set, meaning any [[Intro To the Fourier Series#^24448d|piecewise smooth]] function $f(x)$ can be represented can be represented by a generalized fourier series of the eigenfunctions
5. Eigenfunctions belonging to different eigenvalues are orthogonal relative to the weight function $\sigma(x)$.
6. Any eigenvalue can be related to its eigenfunction by the Rayleigh quotient: $$\lambda=\frac{-p\phi d\phi/dx|^{b}_{a}+\int_{a}^{b}[p(d\phi/dx)^{2}-q\phi^{2}]dx}{\int_{a}^{b}\phi^{2}\sigma dx}$$