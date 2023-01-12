# Odd and Even Functions with Fourier Series

>[!example] Even and Odd Functions
>A function $f(x)$ is **even** if $f(x)=f(-x)$ for all $x$
>A function $f(x)$ is **odd** if $f(x)=-f(-x)$ for all $x$
>Even and Odd designation is a representation of symmetry
>
>**Properties**
>- The product of two even functions is even
>
>- The product of two odd functions is even
>- The product of an odd function and an even function is odd
>- The derivative of an even function is odd
>- The derivative of an odd function is even
>- If $g(x)$ is even, then$$\int_{-L}^{L}g(x)dx=2\int_{0}^{L}g(x)dx$$
>- If $g(x)$ is odd, then $$\int_{-L}^{L}g(x)dx=0$$

We can then apply this protocol to [[Intro To the Fourier Series#^0cc02e|the Fourier Series]]. Suppose $f(x)$ is an even function. Then$$f(x)\cos\left(\frac{n\pi x}{L}\right)\space\space\text{is even, and}$$$$f(x)\sin\left(\frac{n\pi x}{L}\right)\space\space\text{is odd}$$By the integral properties above, we can simplify the [[Intro To the Fourier Series#^965f8d|coefficients]]. In this case, we can say$$a_n=\frac{2}{L}\int_{0}^{L}f(x)\cos\left(\frac{n\pi x}{L}\right)dx$$and$$b_n=0$$Therefore, for an even $f(x)$,$$f(x)=\frac{a_0}{2}+\sum\limits_{n=1}^{\infty}a_n\cos\left(\frac{n\pi x}{L}\right)$$Similarly, we can apply this to an odd $f(x)$, arriving at$$f(x)=\sum\limits_{n=1}^{\infty}b_n\sin\left(\frac{n\pi x}{L}\right)$$Where$$b_n=\frac{2}{L}\int_{0}^{L}f(x)\sin\left(\frac{n\pi x}{L}\right)dx$$ ^153b55