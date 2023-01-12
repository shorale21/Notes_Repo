# Bessel's Equations of an order p

>[!definition] Definition: Bessel's Equation of order $p$
>Bessel's equation, of an order $p$, is the differential equation$$x^2y''+xy'+(x^2-p^2)y=0$$
>Note that $x=0$ is a [[Series Sols. Around a Regular Singular Point#^8ff73a|regular singular point]]

Due to this singular point, we can then apply Frobenius Technique in and assume $x>0$. We get an indicial equation of$$r(r-1)+r-p^2=0$$which will have roots of $r=\pm p$. Consequently, if $2p$ is not an integer, then the Frobenius solution has two linearly independent solutions.

>[!example] Bessel Functions of a First Kind
>A corrseponding frobenius solution to the Bessel equation is$$y_{1}(x)=a_{0}x^{p}\Bigg[1+\sum\limits_{k=1}^{\infty}\frac{(-1)^{k}}{2^{2k}k!(p+1)(p+2)\cdots(p+k)}x^{2k}\Bigg]$$
>**Case 1:** $p$ is $N$, a nonnegative integer
>$$y_{1}(x)=a_{0}x^{N}\Bigg[1+\sum\limits_{k=1}^{\infty}\frac{(-1)^{k}}{2^{2k}k!(N+1)(N+2)\cdots(N+k)}x^{2k}\Bigg]$$
>We can conveniently let $$a_{0}=\frac{1}{N!2^{N}}$$
>Substituting it in, we get the **Bessel function of the first kind of integer order $N$**, denoted as $J_N(x)$$$J_{N}(x)=\sum\limits_{k=0}^{\infty}\frac{(-1)^{k}}{k!(N+k)!}\left(\frac{x}{2}\right)^{2k+N}$$
>
>**Case 2:** $p$ is not an integer
>In order to generalize this, we must introduce another function, the [[Bessel's Equations#^412fa0|gamma function]]. We then choose $a_0$ as follows:$$a_0=\frac{1}{2^p\Gamma(p+1)}$$
>This leads to the Bessel equation of the the first kind:$$J_{p}(x)=\sum\limits_{k=0}^{\infty}\frac{(-1)^{k}}{\Gamma(k+1)\Gamma(p+k+1)}\left(\frac{x}{2}\right)^{2k+p}$$

From this, we can say that the general solution to Bessel's equation can be given by$$y(x)=c_1J_1(p)+c2J_{-p}(x)$$
More generally, we can often find a particular solution of the form:$$Y_p(x)=\frac{J_{p}\cos(p\pi)-J_{-p}}{\sin(p\pi)}$$so $$y(x)=c_1J_{p}(x)+c_2Y_p(x)$$
>[!info] The Gamma Function
>Not to be confused with the [[Lorentz Transformations#^eeedf7|Lorentz gamma factor]] from special relativity, the gamma function is a mathematical function given by:$$\Gamma(p)=\int_{0}^{\infty}t^{p-1}e^{-t}dt,\quad p>0$$
>One special property of this function is the following:$$\Gamma(p+1)=p\Gamma(p)$$

^412fa0

^22ae58
>[!example] Properties of the Bessel function of the first kind
>**Property 1:**$$\frac{d}{dx}[x^{p}J_p(x)]=x^{p}J_{p-1}(x)$$
>**Property 2:**$$\frac{d}{dx}[x^{-p}J_p(x)]=-x^{-p}J_{p+1}(x)$$
>**Property 3:**$$J_{p+1}(x)=2x^{-1}pJ_{p}(x)-J_{p-1}(x)$$
>**Property 4:**$$J'_p(x)=\frac{1}{2}\big[J_{p-1}(x)-J_{p+1}(x)\big]$$