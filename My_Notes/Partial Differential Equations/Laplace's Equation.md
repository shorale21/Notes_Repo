>[!example] Definition: Laplace's Equation
>Laplace's Equation is the [[Intro to PDE#^9a515d|Partial Differential Equation]] shown as follows:
>$$\nabla^{2}u=0$$
>It is homogenous and linear


## Inside a Rectangle
Laplace's equation can describe steady state heat conduction (using conservation of thermal energy) in a two dimensional region. The equation is given as
$$\nabla^{2}u=\frac{\partial^{2}u}{dx^{2}}+\frac{\partial^{2}u}{\partial y^2}=0$$
Boundary conditions for a rectangle are given like:
$$u(0,y)=g_1(y)$$
$$u(L,y)=g_2(y)$$
$$u(x,0)=f_1(y)$$
$$u(x,H)=f_2(y)$$
We cannot apply the [[Separation of Variables#^3661da|method of separation of variables]] since the boundary conditions are nonhomogeneous.
However, the principle of superposition can be applied in this situation. Let's assume
$$u(x,y)=u_{1}(x,y)+u_{2}(x,y)+u_{3}(x,y)+u_{4}(x,y)$$
where each function corresponds to one of the boundary conditions. So,
$$u_1(0,y)=g_1(y)$$
$$u_2(0,y)=0$$
$$u_3(0,y)=0$$
$$u_4(0,y)=0$$
and so on with all the other functions. Let's take a look at $u_1$ and solve it.
$$u_1(x,y)=h(x)\phi(x)$$
$$\phi(y)\frac{d^{2}h}{dx^{2}}+h(x)\frac{d^{2}\phi}{dy^{2}}=0$$
We can then separate the variables.
$$\frac{1}{h}\frac{d^{2}h}{dx^{2}}=-\frac{1}{\phi}\frac{d^{2}\phi}{dy^{2}}=\lambda$$
The $\phi$ function will help us determine the eigenvalues since it has homogenous boundary conditions.

$$\frac{d^{2}\phi}{dy^{2}}=-\phi\lambda$$
And so by the separation [[Separation of Variables#^2d21c9|method]] we can determine the eigenvalues to be
$$\lambda=\Big(\frac{n\pi}{H}\Big)^2$$
$$\phi(y)=\sin{\frac{n\pi y}{H}}$$
Next, we look at the $h$ function of $x$. 
$$h(x)=a_{1}\cosh{\frac{n\pi}{H}(x-L)}+a_{2}\sinh{\frac{n\pi}{H}(x-L)}$$
Applying the boundary condition shows that the $\cosh$ term is zeroed out and thus we find the full equation:
$$u_{4}(x,t)=A\sin{\frac{n\pi y}{H}}\sinh{\frac{n\pi}{H}(x-L)}$$
Similar processes can be done with the other $u$ functions, which can then be added together to get the final equation.

## Inside a Circle
The lengthy proof of this is similar to the [[Separation of Variables#^3661da|separation of variables]] method above, and it results in the final series
$$u(r,\theta)=\sum\limits_{n=0}^{\infty}A_nr^n\cos{n\theta}+\sum\limits_{n=1}^{\infty}B_nr^n\sin{n\theta}$$

## Fluid Flow outside a Cylinder

Conservation of mass and momentum can be used to derive laplace's equation in fluid dynamics.

It is shown that conservation of mass for a fluid along with constant mass density yields
$$\nabla\cdot\textbf{u}=0$$Where $\textbf{u}$ is the velocity vector field, $\textbf{u}=(u,v)$. A **stream** function $\psi$ is often introduced that automatically satisfies 
$$u=\frac{\partial\psi}{\partial y}\quad\text{and}\quad v=-\frac{\partial\psi}{\partial x}$$
When $\psi$ is constant it can be shown in some cases that the fluid is irrotational ($\nabla\times u=0$) so that the stream function satisfies laplace's equation

## Qualitative Properties

#### Mean Value Theorem

If we evaulate the temperature at the center of the circle using Laplace's equation, we find it is
$$u(0,\theta)=a_0=\frac{1}{2\pi}\int_{-\pi}^{\pi}f(\theta)d\theta$$
this is the mean value property. 
>[!example] Mean Value Property of Laplace's Equation
>the temperature at any point in $R$ is the average of the temperature along any circle of radius $r_0$ lying in $R$ centered at that point

#### Maximum Principles

>[!example] Maximmum Principles of Laplace's Equation
>In Steady State the maximum and minimum temperatures occur on the boundary.
>For a region $R$, with heat given by laplace's homogenous equation, the extrema of the temperature lie on the boundary of $R$