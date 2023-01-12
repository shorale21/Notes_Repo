# The complex form of the Fourier Series


Using [[Complex Exponentials#^8e81f7|Euler's formula]], we can reduce the [[Intro To the Fourier Series#^0cc02e|Fourier Series]] to a single term:$$f(x)=\sum\limits_{n=-\infty}^{\infty}c_{n}e^{in\pi x/L}$$We can then derive the coefficients in the a similar way to [[Intro To the Fourier Series#^5882b3|deriving the trigonometric coefficients]].$$\int_{-L}^{L}f(x)e^{ik\pi x/L}dx=\sum\limits_{n=-\infty}^{\infty}c_{n}\int_{-L}^{L}e^{i(k+n)\pi x/L}dx$$It can be shown that complex exponentials obey an orthogonality relation as shown below:$$\int_{-L}^{L}e^{i(k+n)\pi x/L}dx=\begin{cases}
 0 & ,n\neq -k\\
 2L & ,n=-k
\end{cases}$$Thus the above expression simplifies to$$\int_{-L}^{L}f(x)e^{ik\pi x/L}dx=2Lc_{-k}$$Since $n=-k$, then we can get$$c_n=\frac{1}{2L}\int_{-L}^{L}f(x)e^{-in\pi x/L}dx$$

>[!example] The Complex form of the Fourier Series
>The [[Intro To the Fourier Series#^0cc02e|Fourier Series]] can be represented with a complex exponential:
>$$f(x)\sim\sum\limits_{n=-\infty}^{\infty}c_{n}e^{-in\pi x/L}$$
>
>With the complex coefficients given by
>$$c_{n}=\frac{1}{2L}\int_{-L}^{L}f(x)e^{-in\pi x/L}$$