# Fourier Series
>[!Example] Definition: The Fourier Series
>By definition, a **Fourier Series** is an infinite series of the form:$$f(x)=\frac{a_0}{2}+\sum\limits_{n=1}^{\infty}\bigg\{a_n\cos\Big(\frac{n\pi x}{L}\Big)+b_n\sin\Big(\frac{n\pi x}{L}\Big)\bigg\}$$
>Where $L$ is some positive number.
>Note that all of the terms are periodic on a period of $2L$, or $$f(x+2L)=f(x)$$

^0cc02e

>[!example] Definition: Piecewise Smooth
>A function $f(x)$ is said to be **piecewise smooth** if it can be broken up into subintervals, where $f(x)$ and $f'(x)$ are [[Laplace Transforms#^10c23f|piecewise continuous]] on each subinterval.

^24448d

>[!list] The Orthogonality Integrals
>$$\begin{align*}
&\int_{-L}^{L}\cos\Big(\frac{n\pi x}{L}\Big)\cos\Big(\frac{m\pi x}{L}\Big)dx&=
\begin{cases}
 0 & ,m\neq n\\
 L & ,m=n
\end{cases}\\\\
&\int_{-L}^{L}\sin\Big(\frac{n\pi x}{L}\Big)\sin\Big(\frac{m\pi x}{L}\Big)dx&=
\begin{cases}
 0 & ,m\neq n\\
 L & ,m=n
\end{cases}\\\\
&\int_{-L}^{L}\sin\Big(\frac{n\pi x}{L}\Big)\cos\Big(\frac{m\pi x}{L}\Big)dx&=0,\space\text{all }\space m,n
\end{align*}$$

^1c412e

>[!example] Deriving the Fourier Coefficients
>Let $m$ denote some fixed positive integer. We then multiply both sides of the fourier series equation by $\cos\Big(\frac{m\pi x}{L}\Big)$, and then integrate from $-L$ to $L$.
>$$\begin{align*}
\int_{-L}^{L}f(x)\cos\Big(\frac{m\pi x}{L}\Big)dx&=\frac{a_0}{2}\int_{-L}^{L}\cos\Big(\frac{m\pi x}{L}\Big)dx\space+\\&\sum\limits_{n=1}^{\infty}\bigg\{a_n\int_{-L}^{L}\cos\Big(\frac{n\pi x}{L}\Big)\cos\Big(\frac{m\pi x}{L}\Big)+b_n\int_{-L}^{L}\sin\Big(\frac{n\pi x}{L}\Big)\cos\Big(\frac{m\pi x}{L}\Big)\bigg\}
\end{align*}$$
>Notice that the right side can be broken up into three sections. The first one is always equal to $0$, the second one is equal to $0$ when $m\neq n$, and the third is always equal to $0$ regardless of $m$ or $n$. This is shown in the orthogonality integrals above.
>Therefore, the equation can be simplified to$$\int_{-L}^{L}f(x)\cos\Big(\frac{m\pi x}{L}\Big)dx=a_m\int_{-L}^{L}\cos^2\Big(\frac{m\pi x}{L}\Big)dx$$
>Using the actual value of the orthogonality integral with cosines (since $m=n$), we get$$a_m=\frac{1}{L}\int_{-L}^{L}f(x)\cos\Big(\frac{m\pi x}{L}\Big)dx\space,\space\space m>0$$
>The formula for $b_n$ will the same with cosine replaced with sine.

^5882b3


>[!list] Convergent Fourier Series Theorem
>The function $f(x)$ will have a convergent Fourier series, with coefficients $a_n$ and $b_n$ given by:$$a_n=\frac{1}{L}\int_{-L}^{L}f(x)\cos\Big(\frac{n\pi x}{L}\Big)dx\space,\space\space n\ge0$$
>and$$b_n=\frac{1}{L}\int_{-L}^{L}f(x)\sin\Big(\frac{n\pi x}{L}\Big)dx\space,\space\space n>0$$
>provided $f(x)$ is periodic with period $2L$, and both $f(x)$ and $f'(x)$ are at least [[Laplace Transforms#^10c23f|piecewise continuous]] on $-L<x<L$

^965f8d
