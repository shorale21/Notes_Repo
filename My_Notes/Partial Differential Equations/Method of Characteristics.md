## Introduction
Remember the [[Vibrating Strings and Membranes#^8e1319|one-dimensional wave equation]].
This can be factored to be
$$\bigg(\frac{\partial}{\partial{t}}+c\frac{\partial}{\partial{x}}\bigg)\bigg(\frac{\partial{u}}{\partial{t}}-c\frac{\partial{u}}{\partial{x}}\bigg)=0$$Or
$$\bigg(\frac{\partial}{\partial{t}}-c\frac{\partial}{\partial{x}}\bigg)\bigg(\frac{\partial{u}}{\partial{t}}+c\frac{\partial{u}}{\partial{x}}\bigg)=0$$
Let us define the functions 
$$w=\frac{\partial{u}}{\partial{t}}-c\frac{\partial{u}}{\partial{x}}\quad\text{and}\quad v=\frac{\partial{u}}{\partial{t}}+c\frac{\partial{u}}{\partial{x}}$$
This yields two first order equations:
$$\frac{\partial{w}}{\partial{t}}+c\frac{\partial{w}}{\partial{x}}=0\quad\text{and}\quad\frac{\partial{v}}{\partial{t}}-c\frac{\partial{v}}{\partial{x}}=0$$
Let's take a look at the first equation involving $w$. Consider $w(x(t),t)$, and the chain rule implies that
$$\frac{d}{dt}w(x(t),t)=\frac{\partial{w}}{\partial{t}}+\frac{\partial{x}}{\partial{t}}\frac{\partial{w}}{\partial{x}}$$
This is sort of looking at the rate of change as measured by a moving observer, $x=x(t)$. If the observer move with a speed $c$, then 
$$\frac{dw}{dt}=0$$
Thus $w$ is constant, an observer with speed $c$ would measure no changes in $w$.
In this way, the partial differential equation has been replaced with two ODEs:
$$\frac{dx}{dt}=c\quad\text{and}\quad\frac{dw}{dt}=0$$
Integrating the first one yields:
$$x=ct+x_0$$
This is a family of parallel **characteristics** of the differential equation. $w(x,t)$ is constant along these lines. $w$ propogates as a wave with wave speed $c$. The function $w(x(t),t)$ is constant because to an observer moving at speed $c$, $w$ does not change.
Suppose then we are given $w(x,0)=P(x)$. We can then determine $w$ at the point $(x,t)$.
Since $w$ is constant along the characteristic, 
$$w(x,t)=w(x_0,0)=P(x_0)$$
Then the parameter is known from the characteristic determined previously, so $x_0=x-ct$
$$w(x,t)=P(x-ct)$$

## Applications to the One-Dimensional Wave Equation
Recall the [[Vibrating Strings and Membranes#^8e1319|one-dimensional wave equation]]. In the introductory section, we derived two first order partial differential equations from this equation.
We show that $w=P(x-ct)$ where $w(x,0)=P(x)$
Identically, $v$ can be shown to be $v=Q(x+ct)$
Thus, based on our definitions of $w$ and $v$,
$$2\frac{\partial u}{\partial t}=P(x-ct)+Q(x+ct)\quad\text{and}\quad 2c\frac{\partial u}{\partial x}=Q(x+ct)-P(x-ct)$$
Let us make the change of variables:
$$r=x+ct\quad\text{and}\quad s=x-ct$$
Then
$$\frac{\partial}{\partial r}=\frac{\partial}{\partial x}\frac{\partial x}{\partial r}+\frac{\partial}{\partial t}\frac{\partial t}{\partial r}=\frac{1}{2c}\bigg(\frac{\partial}{\partial t}+c\frac{\partial}{\partial x}\bigg)$$
$$\frac{\partial}{\partial s}=\frac{\partial}{\partial x}\frac{\partial x}{\partial s}+\frac{\partial}{\partial t}\frac{\partial t}{\partial s}=-\frac{1}{2c}\bigg(\frac{\partial}{\partial t}-c\frac{\partial}{\partial x}\bigg)$$
Then multiplying these like so:
$$-4c^{2}\frac{\partial^{2}u}{\partial r\partial s}$$
yields the one dimensional wave equation, which of course equals zero.
Thus$$-4c^{2}\frac{\partial^{2}u}{\partial r\partial s}=0$$
We integrate with respect to $r$, yielding a function of $s$ on the other side (since integrating a zero by one variable gives a function of all other variables as a "constant")
$$\frac{\partial{u}}{\partial{s}}=S(s)$$
Now suppose we have a function $F(s)$ such that $S=F'$
Then integrating both sides of the equation gives:
$$u(r,s)=\int F'(s)ds=F(s)+G(r)$$
Then substituting back into the equation yields the general solution:
$$u(x,t)=F(x-ct)+G(x+ct)$$
Now suppose we have [[The Heat Equation#^84b5c4|initial conditions]] such as
$$u(x,0)=f(x)\quad\text{and}\quad\frac{\partial u}{\partial t}(x,0)=g(x)$$
These conditions imply
$$f(x)=F(x)+G(x)$$
$$\frac{g(x)}{c}=-\frac{dF}{dx}+\frac{dG}{dx}$$
We can then eliminate $F(x)$ by adding the derivative of the $f(x)$ equation to the second equation, and integrating, yielding
$$G(x)=\frac{1}{2}f(x)+\frac{1}{2c}\int_{0}^{x}g(\bar{x})d\bar{x}$$
$$F(x)=\frac{1}{2}f(x)-\frac{1}{2c}\int_{0}^{x}g(\bar{x})d\bar{x}$$
>[!example] d'Alembert's Solution to the One Dimensional Wave Equation
>Suppose a variable $u$ obeys the [[Vibrating Strings and Membranes#^8e1319|one-d wave equation]] and has initial conditions $u(x,0)=f(x)$ and $\frac{\partial u}{\partial t}(x,0)=g(x)$.
>Then the general solution (not taking into account the boundary conditions) is given as
>$$u(x,t)=\frac{f(x-ct)+f(x+ct)}{2}+\frac{1}{2c}\int_{x-ct}^{x+ct}g(\overline{x})d\overline{x}$$

## Semi-Infinite Strings and Reflections
We define our boundary conditions to be fixed at one end, allowing the string to continue to infinity as $x>0$.
Thus $u(0,t)=0$ is our one boundary condition.

Remember, we have our general solution: $u(x,t)=F(x-ct)+G(x+ct)$
The initial conditions are only valid for $x>0$, so $G$ requires only positive arguments, since $x+ct$ is positive if $x>0$ and $t>0$, and $F$ requires positive arguments if $x>ct$ but negative arguments if $x<ct$.
We then use d'Alembert's solution. Since $x+ct>0$,
$$G(x+ct)=\frac{1}{2}f(x+ct)+\frac{1}{2c}\int_{0}^{x+ct}g(\overline{x})d\overline{x}$$
To obtain $F$ for negative arguments the boundary condition is used, implying that
$$0=F(-ct)+G(ct)$$ for $t>0$.
Then $F(z)=-G(-z)$ for $z<0$.
Then the solution for $x-ct<0$ is 
$$u(x,t)=F(x-ct)+G(x-ct)=\frac{1}{2}[f(x+ct)-f(ct-x)]+\frac{1}{2c}\int_{ct-x}^{x+ct}g(\overline{x})d\overline{x}$$
This right moving wave $-G(ct-x)$ is called the reflected wave. For $x<ct$ the total solution is the reflected wave plus the unreflected left moving wave.

## Vibrating String of Fixed Length
Imagine we have a finite string, with boundary conditions given by
$$u(0,t)=u(L,t)=0$$
We get an analytic solution on an infinite domain by extending the initial condtions as odd periodic functions with period $2L$.

## Quasilinear Partial Differential Equations
The method of characteristics can be applied to equations of the form:
$$\frac{\partial\rho}{\partial t}+c\frac{\partial\rho}{\partial x}=Q$$
Where $Q$ and $c$ can be functions of $\rho, x,t$.
If we again consider the observer moving in some way $x(t)$, we get
$$\frac{d\rho}{dt}=Q(\rho,x,t)$$
$$\frac{dx}{dt}=c(\rho,x,t)$$
This trajectory is called a characteristic curve, where the function is constant. Of course, we can easily solve first order nonlinear differential equations if they are separable.
>[!example]- Application: Traffic Flow
>The traffic density $\rho(x,t)$ is the number of cars per mile at time $t$ located at position $x$. The traffic flow $q(x,t)$ is the number of cars per hour passing a fixed place $x$ at time $t$.
>If there are neither entraces or exits on a certain segment of road, for $a$ to $b$, we get
>$$\frac{d}{dt}\int_{a}^{b}\rho(x,t)dx=q(a,t)-q(b,t)$$
>Note that the right side itself can be expressed as an integral with respect to $x$ of the derivative of $q$, and thus we get
>$$\frac{\partial \rho}{\partial t}+\frac{\partial{q}}{\partial{x}}=0$$
>Suppose we introduce $u(x,t)$ as the car velocity, which is $q=\rho u$. Thus
>$$\frac{\partial\rho}{\partial{t}}+c(\rho)\frac{\partial\rho}{\partial{x}}=0$$
>this is then a quasilinear differential equation, solvable by characteristics.
>Our characteristics are given as
>$$\frac{d\rho}{dt}=0$$
>$$\frac{dx}{dt}=c(\rho)$$
>Along one characteristic corresponding to an initial condition,
>$$\rho(x,t)=\rho(x_0,0)=f(x_0)$$
>Then
>$$x=c(f(x_0))t+x_0$$