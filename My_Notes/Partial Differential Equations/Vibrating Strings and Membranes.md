## Derivation of a Vibrating String
Consider a horizontally stretched spring in its equilibrium configuration (meaning it won't just start vibrating)
We track the motion of each particle, by letting $\alpha$ be the x-coordinate of a particle when the string is in equilibrium. 
We assume the motion is entirely vertical and not horizontal. Giving us an equation:
$$y=u(x,t)$$
Consider an infinitesimally thin segment of the string contained between $x$ and $x+\Delta x$. The mass density $\rho_0(x)$ is known.
The total mass of this segment is then $\rho_0(x)\Delta x$. We also assume this string has no resistance to bending. The tension in the string is denoted $T(x,t)$.
The tension force pulls at both ends of the small segment, tangential to the string.
The slope of said segment is $dy/dx$, which is equal to the tangent of the angle the string is at:
$$\frac{dy}{dx}=\tan{\theta(x,t)}=\frac{\partial u}{\partial x}$$
Using [[Newtonian Dynamics#^c616f8|Newton's Second Law]] we can remember that the forces can be described by the acceleration:
$$\rho_0(x)\Delta x\frac{\partial^{2u}}{\partial t^{2}}=T(x+\Delta x,t)\sin{\theta}(x+\Delta x,t)-T(x,t)\sin{\theta}(x,t)+\rho_0(x)\Delta xQ(x,t)$$
Where $Q$ is the vertical component of the tensile force.
We divide by $\Delta x$ and take the limit as it goes to zero:
$$\rho_{0}(x)\frac{\partial^2{u}}{\partial{x}^2}=\frac{\partial}{\partial{x}}[T(x,t)\sin{\theta(x,t)}]+\rho_{0}(x)Q(x,t)$$
For small angles $\theta$, 
$$\frac{\partial{u}}{\partial{x}}=\tan{\theta}\approx\sin{\theta}$$
And thus
$$\rho_{0}(x)\frac{\partial^2{u}}{\partial{x}^2}=\frac{\partial}{\partial{x}}\bigg(T\frac{\partial{u}}{\partial{x}}\bigg)+\rho_{0}(x)Q(x,t)$$
>[!example] Perfectly Elastic Strings
>A perfectly elastic string is a string where the tension force $T(x,t)$ depends only on the local stretching of the string. In this, the tensile force can be approximated by a constant $T_0$

>[!example] One-Dimensional Wave Equation
>The differential equation of motion describing a one dimensional wave is:
>$$\frac{\partial^{2}u}{\partial t^{2}}=c^{2}\frac{\partial^{2}u}{\partial x^2}$$
>$c$ is the velocity

^8e1319

## Boundary Conditions
Since the wave equation has a second order spatial derivative, we need a boundary condition at each end. 
>[!example] Definition: Variable Support Boundary Condition
>This is a special type of [[The Heat Equation#^acae29|boundary condition]] where one end is attached to a dynamical system.
>For example, a spring-mass system.

Let's work an example. Suppose the right side of a string is attached to the ground:
$$u(L,t)=0$$
Then suppose the left end is attached to mass connected to a spring. Then
$$u(0,t)=y(t)$$
The function $y$ obeys [[Oscillations#^ba95a0|Hooke's Law]] and its own differential equation:
$$m\frac{d^{2}y}{dt^{2}}=-k(y(t)-y_s(t)-l)+\text{other forces}$$
Other forces on the mass are the tensile force from the string $T(0,t)\sin{\theta(0,t)}$ and a force $g(t)$ representing any other forces.
$$T(0,t)\approx T_{0}\frac{\partial u}{\partial x}(0,t)$$
The final differential equation describing the boundary condition is
$$m\frac{d^2}{dt^2}u(0,t)=-k(u(0,t)-y_s(t)-l)+T_0\frac{\partial{u}}{\partial{x}}(0,t)+g(t)$$

## Vibrating String with Fixed Ends
Imagine if the boundary conditions were both zero.
We also need two initial conditions:
$$u(x,0)=f(x)\quad\text{and}\quad\frac{\partial u}{\partial t}(x,0)=g(x)$$
We can then use [[Separation of Variables#^3661da|separation of variables]] to try and solve this equation.
We suppose $u(x,t)=\phi(x)h(t)$ This results in
$$h(t)=c_1\cos{c\sqrt{\lambda}t}+c_2\cos{c\sqrt{\lambda}t}$$
Then $$\lambda=\bigg(\frac{n\pi}{L}\bigg)^2$$
Our corresponding eigenfunctions are $\sin{n\pi x/L}$ for the spatial derivative and $\sin{n\pi ct/L}$ or $\cos{n\pi ct/L}$ for the time derivative. For the superposition principle, we can define a general solution as
$$u(x,t)=\sum\limits_{n=1}^{\infty}\bigg(A_{n}\sin{\frac{n\pi x}{L}}\cos{\frac{n\pi ct}{L}}+B_{n}\sin{\frac{n\pi x}{L}}\sin{\frac{n\pi ct}{L}}\bigg)$$

## Vibrating Membrane
The multi-dimensional wave equation is as such
$$u_{tt}=c^{2}\nabla^{2}u$$
We won't solve this yet.