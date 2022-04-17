# Special Laplace Transforms Part 2
<u>**The Unit Step Function**</u>
When examining equations of the form $y''+by'+cy=F(t)$, it often arises that the forcing function $F(t)$ is either [[Laplace Transforms#^10c23f|piecewise continuous]] or discontinuous.

The **Unit Step Function** $u_a(t)$ is defined by $$u_a(t)=\begin{cases}0,\quad 0\le t<a\\1,\quad t \ge a \\ \end{cases}$$
where $a$ is any positive number ^08bff2

<u>**The Dirac Delta Function**<u/>
- We must consider the differential equation $ay''+by+c=f(t)$ where $f(t)$ is an impulse force rather than a continuous or periodic force
- Suppose a force acts on an object over the time interval $[t_1,t_2]$.
	- The Impulse of this force is described by: $I=\int_{t_1}^{t_2}f(t)dt$
	- Since $f(t)=0$ for any $t$ outside the interval described, we can say $I=\int_{-\infty}^{\infty}f(t)dt$
	- Define the function $d_{\epsilon}(t-a)=\frac{u_a(t)-u_{a+\epsilon}(t)}{\epsilon}$ where $u_a(t)$ is the [[Special Laplace Part 2#^08bff2|unit step function]]
		- Notice $I=\int_{-\infty}^{\infty}d_{\epsilon}(t-a)dt = 1$
	- We then take the limit as $\epsilon$ approaches $0$ in order to get an instantaneous force
- We then define the **dirac delta function** (or **unit impulse function**) as the generalized function that satisfies: ^dc18ec
	1. $\delta (t-a) = 0, \quad t \neq a$
	2. $\int_{-\infty}^{\infty}\delta (t-a)dt = 1$ 
- It can be shown that if $g$ is a continuous function on $(-\infty,\infty)$, then $$\int_{-\infty}^{\infty}g(t)\delta (t-a)dt = g(t)$$
