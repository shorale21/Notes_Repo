# Inverse Laplace Transforms
>[!example] Defintion: Exponential Order
>A function $f$ is said to be of exponential order if there exist constants $M$ and $\alpha$ such that$$|f(t)|\le Me^{\alpha t},$$
>for all $t\:>\:0$

^565e2b

For future purposes, let $E(0,\infty)$ denote the set of functions that are both [[Laplace Transforms#^10c23f|piecewise continuous]] on $[0,\infty)$ and of [[Inverse Laplace Transforms#^565e2b|exponential order]].  ^9bead4

>[!example] Theorem 10.2.4
>If $f$ is in $E(0,\infty)$ there exists a number $\alpha$ such that: $$\mathcal{L}[f]=\int_{0}^{\infty}e^{-st}f(t)dt$$
>exists for all $s\:>\:\alpha$
>>[!summary]- Proof of Theorem 10.2.4
>>We know that $f$ must be integrable over $[0,\infty]$ Let:$$F(t)=|e^{-st}f(t)|$$
>>Then, $$F(t)=|e^{-st}f(t)|\le Me^{(\alpha - s)t}$$
>>But, for $s\:>\:\alpha$,$$\int_{0}^{\infty}Me^{(\alpha - s)t}dt=\lim_{N\to\infty}\int_{0}^{N}Me^{(\alpha - s)t}dt=\frac{M}{s-\alpha}$$
>>Applying the comparison test for improper integrals with $F(t)$ as defined previously and $G(t)=Me^{(\alpha -s)t}$, it is shown that: $$\int_{0}^{\infty}|e^{-st}f(t)|dt$$
>>converges for $s\:>\:\alpha$ and so does $$\int_{0}^{\infty}e^{-st}f(t)dt$$
>>Therefore, $\mathcal{L}[f]$ exists for $s\:>\:\alpha$

We can say that $\mathcal{L}$ defines of linear transformation of $V$ onto $Rng(\mathcal{L})$. $\mathcal{L}$ is also one-to-one which means $\mathcal{L}^{-1}$ exists.
>[!example] Definition: Inverse Laplace Transform
>The Linear Transformation $\mathcal{L}^{-1}:Rng(\mathcal{L})\rightarrow V$ defined by $$\mathcal{L}^{-1}[F](t)=f(t)\:\:\text{if and only if}\:\:\mathcal{L}[f](s)=F(s)$$
>is called the Inverse Laplace Transform
>>[!INFO]- Important Note
>>The Inverse Laplace Transform is a linear transformation, meaning $$\mathcal{L}^{-1}[\alpha F\:+\:\beta G]=\alpha \mathcal{L}^{-1}[F] + \beta \mathcal{L}^{-1}[G]$$

^3f32a7

>[!example] Known Inverse Laplace Transforms
>$$\mathcal{L}^{-1}\left[\frac{1}{s^{n+1}}\right]=\frac{1}{n!}t^n\quad\quad\quad\quad \mathcal{L}^{-1}\left[\frac{1}{s-a}\right]=e^{at}$$
>$$\quad\quad\mathcal{L}^{-1}\left[\frac{s}{s^2 + b^2}\right]=cos(bt)\quad\quad\quad\quad\mathcal{L}^{-1}\left[\frac{b}{s^2 + b^2}\right]=sin(bt)$$