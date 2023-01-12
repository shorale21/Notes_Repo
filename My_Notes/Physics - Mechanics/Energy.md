There are many different types of energy.

## Kinetic Energy
Kinetic energy is the energy of motion. It is defined to be related to the velocity of the object, and is a type of mechanical energy.

>[!example] Definition: Kinetic Energy
>**Kinetic Energy** is the energy of a moving object. For an object with a velocity $v$ and a mass $m$, it is defined to be $$T=\frac{1}{2}mv^2$$

^1c7dc1

Let us look at the change in kinetic energy. Suppose we have a particle moving along a path while under the influence of a force. Taking the time derivative $dt$ of the kinetic energy gives:
$$\frac{dT}{dt}=\frac{d}{dt}\frac{1}{2}m(\textbf{v}\cdot\textbf{v})=\frac{1}{2}m(\dot{\textbf{v}}\cdot\textbf{v}+\textbf{v}\cdot\dot{\textbf{v}})=m\dot{\textbf{v}}\cdot\textbf{v}$$
[[Newtonian Dynamics#^c616f8|Newton's Second Law]] states that $\textbf{F}=m\textbf{a}=m\dot{\textbf{v}}$. Thus the equation becomes:
$$\frac{dT}{dt}=\textbf{F}\cdot\textbf{v}$$
Multiplying both sides by $dt$ gives$$dT=\textbf{F}\cdot d\textbf{r}$$
We define this to be the work, introducing the next theorem.
>[!example] Work-Kinetic Energy Theorem
>The change in kinetic energy is equal to the work done on the object.
>$$\Delta T=T_{2}-T_{1}=\int_{1}^{2}\textbf{F}\cdot d\textbf{r}=\int_{1}^{2}\sum\limits_{i}\textbf{F}_i\cdot d\textbf{r}=W(1\rightarrow2)$$

^947638

## Potential Energy

Forces with a corresponding potential energy are called **conservative forces**. 

The first condition for a force $\textbf{F}$ to be conservative is that $\textbf{F}$ depends only on the particle's postion $\textbf{r}$. For example the gravitation force:
$$\textbf{F}=-\frac{GmM}{r^2}\hat{\textbf{r}}$$

>[!example] Definition: Conservative Forces
>A force $\textbf{F}$ acting on a particle is **conservative** if and only if it satisfies these two conditions:
>1. $\textbf{F}$ depends only on the particle's postion $\textbf{r}$
>2. For any two points 1 and 2, the work $W(1\rightarrow2)$ done by $\textbf{F}$ is the same for all paths between 1 and 2
>If all of the forces on an object are conservative, we can define a quantity called the **potential energy**, a function of only the position, with the property that the total mechanical energy
>$$E=KE+PE=T+U(r)$$is constant, or *conserved*.

^8b8deb

>[!example] Definition: Potential Energy
>The potential energy $U(\textbf{r})$ corresponding to a [[Energy#^8b8deb|conservative force]] $\textbf{F}$. By selecting a reference point $\textbf{r}_0$ where $U(\textbf{r})=0$, we can define the potential energy in terms of the [[Energy#^947638|work]] done:
>$$U(\textbf{r})=-W(\textbf{r}_0\rightarrow\textbf{r})=-\int_{\textbf{r}_0}^{\textbf{r}}\textbf{F}(\textbf{r}')\cdot d\textbf{r}'$$

^4f5cbe

Notice that if the force is not conservative, $U(r)$ is not unique since the work done is not unique.

This also allows us define work in terms of the potential energy:
$$W(\textbf{r}_1\rightarrow\textbf{r}_2)=-\Delta U$$

This leads to a conservation of energy theorem.

>[!example] Principle of Conservation of Energy for One Particle
>If all of the $n$ forces $\textbf{F}_i$ acting on a particle are [[Energy#^8b8deb|conservative]], each with its corresponding [[Energy#^4f5cbe|potential energy]] $U_{i}(\textbf{r})$, the total mechanical energy defined as $$E=T+\sum\limits_{j=1}^{n}U_{j}(\textbf{r})$$ is constant in time.

^3aeaa2

Let us consider a particle acted on by a conservative force $\textbf{F}(\textbf{r})$ with corresponding potential energy $U(\textbf{r})$.
The work done by $\textbf{F}(\textbf{r})$ in a small displacement from $r$ to $r+dr$, is
$$W(r\rightarrow r+dr)=\textbf{F}(\textbf{r})\cdot d{\textbf{r}}=F_xdx+F_ydy+F_zdz$$
for any small displacement $d\textbf{r}$.

In addition, the work is the change in potential energy, so
$$W(\textbf{r}\rightarrow\textbf{r}+d\textbf{r})=-dU=-[U(\textbf{r}+d\textbf{r})-U(\textbf{r})]=-\bigg[\frac{\partial U}{\partial x}dx+\frac{\partial U}{\partial y}dy+\frac{\partial U}{\partial z}dz\bigg]$$

By combining these equations, we get three expressions:
$$F_x=-\frac{\partial U}{\partial x}\quad\quad F_y=-\frac{\partial U}{\partial y}\quad\quad F_z=-\frac{\partial U}{\partial z}$$

This allows us to get an expression for force in terms of the potential energy.

>[!example] Definition of Force in terms of Potential Energy
>A [[Energy#^8b8deb|conservative]] force with [[Energy#^4f5cbe|potential energy]] $U(r)$ can be expressed as:
>$$\textbf{F}=-\nabla U$$

## Curl

How do we test whether a force is [[Energy#^8b8deb|conservative]]? We cannot test every possible path to determine whether the work is the same.

>[!example] Curl and Work
>A Force $\textbf{F}$ is [[Energy#^8b8deb|conservative]], or more specifically it fulfills the second property if the curl is zero.
>$$\nabla\times\textbf{F}=0$$ 

## Time Dependent Potential Energy

Sometimes there is a force that satisfies the property that $\nabla\times\textbf{F}=0$, but since the force is time dependent it does not satisfy the first condition of conservative forces. We can still define a potential energy $U(\textbf{r},t)$ with the property that $\textbf{F}=-\nabla U$, but the mechanical energy is no longer conserved.

## Energy for Linear One-Dimensional Systems 

A one-dimensional system is a system that can be expressed with only one parameter. 
Anything constrained to move in a straight line, anything contrained to a curved track, and anything that can only move in two dimensions, backwards and forwards. 

The work done is then a one dimensional integral:
$$W(x_1\rightarrow x_2)=\int_{x_1}^{x_2}F_x(x)dx$$

If $F_x$ only depends on $x$, this guarantees the second property of conservatism since the system can only have one path.

Potential energy graphs are extremely simple, and give us an excellent visualization of a system.

>[!example] Unstable Equilibrium
>If the Potential Energy of an equilibrium state has the property that $d^2U/dx^2<0$, a small nudge away from equilibrium leads to a force **away** from equilibrium, so the object will always leave equilibrium. 
>
>This is unstable equilibrium, a place where the potential energy is at a local maximum, like the top of a hill

>[!example] Stable Equilibrium
>If the Potential Energy of an equilibrium state has the property that $d^2U/dx^2>0$, a small nudge away from equilibrium creates a force **towards** the equilibrium point, so the object will tend to return
>
>This is stable, a place where the potential energy is at a local minimum, like the bottom of a valley.

^6562c3

Let's derive a solution to the motion in a one-dimensional conservative system.

We can then use the [[Energy#^3aeaa2|conservation of energy]] property to set up an equation:
$$T=\frac{1}{2}m\dot{x}^2=E-U(x)$$
Thus we can create a differential equation:
$$\dot{x}(x)=\pm\sqrt{\frac{2}{m}}\sqrt{E-U(x)}$$
This has uncertainty since energy does not have direction and thus cannot determine the direction of the velocity.
$$t_f-t_i=\int_{x_i}^{x_f}\frac{dx}{\dot{x}}$$
If we assume $t_i=0$, then we can get an equation for $t$:
$$t=\sqrt{\frac{m}{2}}\int_{x_0}^{x}\frac{dx'}{\sqrt{E-U(x')}}$$
Solving this equation by integrating the known function of $U(x)$ will give a solution to the system.

## Curvilinear One-Dimensional Systems

Other systems can be said to one-dimensional, for example a roller coaster on a curved track.
This position of the cart can be specified by $s$, the distance along the track.
$$T=\frac{1}{2}m\dot{s}^2$$

As the object follows the path, the normal force (often called the force of constrant) forces it to follow the path.
However, the normal force does no work since it is always perpendicular. 
Thus $F_{tang}=m\ddot{s}$
If all the forces that have a tangential component are conservative, we can define a [[Energy#^4f5cbe|potential energy]] such that the total energy is
$$E=T+U(s)$$and is conserved.

## Central Forces

>[!example] Definition: Central Force
>A force that is everywhere directed toward or away from a fixed "center"
>If the center is the origin, this force looks like
>$$\textbf{F}(\textbf{r})=f(\textbf{r})\hat{\textbf{r}}$$
>A Central force that is [[Energy#^8b8deb|conservative]] is also spherically symmetric

^b84951

## Elastic Collisions

>[!example] Definition: Elastic Collision
>A collision between two particles that interact via a [[Energy#^8b8deb|conservative]] force tht goes to zero as their separation increases. 
>
>This means the potential energy approaches a constant, which provided the reference frame, could be considered zero.
>
>Kinetic Energy is conserved in an elastic collision.

## Multiparticle Systems

In a multiparticle system where $\textbf{F}^{ext}_{\alpha}$ is conservative, we can introduce the potential energy as $$\textbf{F}^{\text{ext}}_{\alpha}=-\nabla_{\alpha}U^{\text{ext}}_{\alpha}(\textbf{r}_{\alpha})$$
If we define
$$U=U^{\text{int}}+U^{\text{ext}}=\sum\limits_{i<j}^{N}U_{ij}+\sum\limits_{i=1}^{N}U^{\text{ext}}_{i}$$
Then in general, the net force on the particle $\alpha$ is given by
$$-\nabla_{\alpha}U$$
Also, energy is constant if there are no external forces.