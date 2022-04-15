# Special Laplace Transforms Part 1
>[!example] Definition: Periodic Functions
>A function $f$ defined on the interval $[0,\infty)$ is said to be **periodic with period** $T$ if $T$ is the smallest real number satisfying the equation$$f(t+T)=f(t)$$
>for all $t\:>\:0$

The Laplace transform of a periodic function $f(t)$ with period $T$ is given to be:$$\mathcal{L}[f]=\frac{1}{1-e^{-sT}}\int_{0}^{T}e^{-st}f(t)dt$$

>[!abstract]- Derivation of $\mathcal{L}\:$ for a Periodic Function
>By definition of the [[Laplace Transforms#^374085|Laplace Transform]] we have: $$\mathcal{L}[f]=\int_{0}^{T}e^{-st}f(t)dt\:+\:\int_{T}^{2T}e^{-st}f(t)dt\:+\cdots+\:\int_{nT}^{(n+1)T}e^{-st}f(t)dt\:+\cdots$$
>We can now consider the general integral$$I=\int_{nT}^{(n+1)T}e^{-st}f(t)dt$$
>Let $x=t-nT$, giving us $dx=dt$. Notice that $t=nT$ corresponds to $x=0$ and $t=(n+1)T$ corresponds to $x=T$. We can rewrite $I$ as $$\int_{0}^{T}e^{-s(x+nT)}f(x+nT)dx=e^{-snT}\int_{0}^{T}e^{-sx}f(x)dx$$
>Where we can use the fact that $f$ is periodic to state that $f(x+nT)=f(x)$. Therefore, adding up all the $I$ intervals, we can write the [[Laplace Transforms#^374085|Laplace Transform]] as $$\mathcal{L}[f]\:=\:(1+e^{-sT}+e^{-2sT}+\cdots+e^{-nsT}+\cdots)\int_{0}^{T}e^{-sx}f(x)dx$$
>Notice how the integral is multiplied by a geometric series with a common ratio $e^{-sT}$. This means the coefficient in question sums to $\frac{1}{1-e^{-sT}}$ so that $$\mathcal{L}[f]=\frac{1}{1-e^{-sT}}\int_{0}^{T}e^{-st}f(t)dt$$



<u>**First Shifting Theorem**</u>
If $\mathcal{L}[f]=F(s)$, then$$\mathcal{L}[e^{at}f(t)]=F(s-a)$$
Conversely, if $\mathcal{L}^{-1}[F(s)]=f(t)$, then$$\mathcal{L}^{-1}[F(s-a)]=e^{-st}f(t)$$
>[!abstract]- Proof of the First Shifting Theorem
>From the definition of the [[Laplace Transforms#^374085|laplace transform]] we have, $$\mathcal{L}[e^{-st}f(t)]=\int_{0}^{\infty}e^{-st}e^{at}f(t)dt=\int_{0}^{\infty}e^{-(s-a)t}f(t)dt$$
>Based on the definition of $F(s)$, $F(s-a)$ can be defined as$$F(s-a)=\int_{0}^{\infty}e^{-(s-a)t}f(t)dt$$
>Which is clearly equal to the previous one, therefore proving the first shifting theorem. 



<u>**Second Shifting Theorem**</u>
Let $\mathcal{L}[f(t)]=F(s)$. Then$$\mathcal{L}[u_a(t)f(t-a)]=e^{-as}F(s)$$
where $u_a(t)$ is the [[Special Laplace Part 2#^08bff2|unit step function]]. Conversely, $$\mathcal{L}^{-1}[e^{-as}F(s)]=u_a(t)f(t-a)$$
>[!abstract]- Proof of the Second Shifting Theorem
>Use the definition of the [[Laplace Transforms#^374085|laplace transform]], We get $$\mathcal{L}[u_a(t)f(t-a)]=\int_{0}^{\infty}e^{-st}u_a(t)f(t-a)dt=\int_{a}^{\infty}e^{-st}f(t-a)dt$$
>Let $x=t-a$. Then $dx=dt$ and $t=a$ corresponds to $x=a$. Therefore, $$\mathcal{L}[u_a(t)f(t-a)]=\int_{0}^{\infty}e^{-s(x+a)}f(x)dx=e^{-as}\int_{0}^{\infty}e^{-sx}f(x)dx=e^{-as}\mathcal{L}[f]$$
>This is the same as $e^{-as}F(s)$

Another variation is stated as follows:$$\mathcal{L}[u_a(t)f(t)]=e^{-as}\mathcal{L}[f(t+a)]$$