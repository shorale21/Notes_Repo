## Lagrange's Equations for Unconstrained Motion
Consider a particle moving unconstrained in three dimensions subject to a [[Energy#^8b8deb|conservative]] net force $\textbf{F}(\textbf{r})$. The [[Energy#^1c7dc1|kinetic energy]] of the particle is of course
$$\frac{1}{2}m\dot{\textbf{r}}^2=\frac{1}{2}m(\dot{x}^2+\dot{y}^2+\dot{z}^2)$$
And the [[Energy#^4f5cbe|potential energy]] is
$$U=U(\textbf{r})=U(x,y,z)$$
>[!example] Definition: The Lagrangian
>The Lagrangian Function, or just the Lagrangian is defined as
>$$\mathcal{L}=T-U$$
>The difference beween [[Energy#^1c7dc1|kinetic]] and [[Energy#^4f5cbe|potential]] energy.
>Notice that this depends on the derivatives and the positions:
>$$\mathcal{L}=\mathcal{L}(x,y,z,\dot{x},\dot{y},\dot{z})$$

^9ad443

Let us consider the two derivatives from the [[Euler-Lagrange Equations#^ce4f09|Euler-Lagrange]] equation 
$$\frac{\partial\mathcal{L}}{\partial x}=-\frac{\partial U}{\partial x}=F_x$$
$$\frac{\partial\mathcal{L}}{\partial\dot{x}}=\frac{\partial T}{\partial\dot{x}}=m\dot{x}=p_x$$
Differentiating the second one with respect to time givs $\dot{p_x}$. Remember from [[Newtonian Dynamics#^c616f8|Newton' Second Law]] that $F_x=\dot{p}_x$, so when these equations fulfill the lagrange equations, Newtonian Mechanics emerges.
>[!example] Definition: Action
>The action is a mathematical quantity defined in terms of the [[Lagrangian Mechanics#^9ad443|lagrangian]] of the system:
>$$S=\int_{t_1}^{t_2}\mathcal{L}\space dt$$

^75f2a1

>[!example] Hamilton's Principle
>The actual path which a particle follows between points 1 and 2 in a give time interval $t_1$ to $t_2$ is such that the [[Lagrangian Mechanics#^75f2a1|action integral]] is stationary when taken along the actual path. 
>
>In other words, the action integral is a [[Introduction to Variational Calculus#^2a28a5|functional]] that must be minimized using the calculus of variations.

The beauty of this method is that it works for any generalized coordinate system.
The steps are 
1. Identify Generalized coordinates
2. Put the lagrangian in those generalized coordinates
3. Solve Lagrange's Equations

For several unconstrained particles, the lagragian is defined exactly as before, in terms of the potential and kinetic energy, but those energies are now dependent on multiple positions.

Each position then corresponds to three lagrange equations as before.

## Constrained Systems
The lagrangian is especially useful when the system is constrained, or has less degrees of freedom than dimensions.

For example, consider a pendulum in the $xy$ plane with a string length of $l$. The system is constrained by the fact that $\sqrt{x^2+y^2}=l$ meaning either $x$ or $y$ can be considered dependent so the system has one degree of freedom. 
>[!example]- Example: Plane Pendulum
>We can choose a generalized coordinate as the angle between the string and the vertical, $\phi$.
>
>The kinetic energy is $T=\frac{1}{2}ml^2\dot{\phi}^2$, and the potential energy is $U=mgh=mgl(1-\cos{\phi})$
>Using this we can set up our lagrangian:
>$$\mathcal{L}=T-U=\frac{1}{2}ml^2\dot{\phi}^2-mgl(1-\cos{\phi})$$
>Now we can solve the euler lagrange equations for the motion:
>$$\frac{\partial\mathcal{L}}{\partial\phi}=-mgl\sin{\phi}=\frac{d}{dt}\frac{\partial\mathcal{L}}{\partial\dot{\phi}}=\frac{d}{dt}(ml^2\dot{\phi})=ml^2\ddot{\phi}$$
>Thus, since $ml^2$ is the moment of inertia $I$, this equation is actually the result
>$$\Gamma=I\alpha$$

>[!example] Definition: Generalized Coordinates
>For an arbitrary system of $N$ particles $\alpha=1,\dots,N$ with positions $\textbf{r}_{\alpha}$.
>We call the parameters $q_1,\dots,q_n$ **generalized coordinates** if each position can be expressed as a function of the parameters and possibly the time $t$.
>$$\textbf{r}_{\alpha}=\textbf{r}_{\alpha}(q_1,\dots,q_n,t)$$
>
>We also require that the number of parameters $n$ is the smallest possible for the system.
>
>This set of parameters is called *natural* if the relation between the cartesian and generalized coordinates does not depend on the time 

^865c15

A system with the property that the amount of generalized coordinates is equal to the degrees of freedom is called **holonomic**

## Proof of Lagrange's Equations with Constraints
Let's prove Lagrange's equations for any holonomic system, for just one particle for now.

Suppose the particle is constrained to move on a surface. This means it has two degrees of freedom and can be described by two generalized coordinates $q_1$ and $q_2$.

The nonconstraint forces are 
$$\textbf{F}=-\nabla U(\textbf{r},t)$$
The total forces are $\textbf{F}_{tot}=\textbf{F}_{cstr}+\textbf{F}$

Consider any points $\textbf{r}_1$ and $\textbf{r}_2$ through which the particle passes at times $t_1$ and $t_2$. Suppose $\textbf{r}(t)$ is the correct path, and $\textbf{R}(t)$ is the actual path, given by
$$\textbf{R}(t)=\textbf{r}(t)+\epsilon(t)$$
Let us denote the action integral as 
$$S=\int_{t_1}^{t_2}\mathcal{L}(\textbf{R},\dot{\textbf{R}},t)dt$$
And $S_0$ the same integral except along the correct path.
Another way to say this is that:
$$\delta S=S-S_0$$
As well as this:
$$\delta\mathcal{L}=\frac{1}{2}m\Big[(\dot{\textbf{r}}+\dot{\epsilon})^2-\dot{\textbf{r}}^2\Big]-\big[U(\textbf{r}-\epsilon,t)-U(\textbf{r},t)\big]$$
So,
$$\delta S=\int_{t_1}^{t_{2}}\delta\mathcal{L}\space dt$$
Thus,
$$\delta S=-\int_{t_{1}}^{t_{2}}\epsilon\cdot\textbf{F}_{\text{cstr}}\space dt$$
But the constraint force is normal to our surface while $\epsilon$ is on the surface, so the dot product is zero and therefore $\delta S=0$, meaning the action integral must be stationary.

## Generalized Momenta and Forces
>[!example] Definition: Generalized Forces
>For a system of with $n$ [[Lagrangian Mechanics#^865c15|generalized coordinates]] $q_i$ the quantities 
>$$\frac{\partial\mathcal{L}}{\partial{q_i}}=F_i$$are called *generalized forces*
>
>$\mathcal{L}$ is the [[Lagrangian Mechanics#^9ad443|lagrangian]] of course

>[!example] Definition: Generalized Momenta
>For a system of with $n$ [[Lagrangian Mechanics#^865c15|generalized coordinates]] $q_i$ the quantities 
>$$\frac{\partial\mathcal{L}}{\partial{\dot{q}_i}}=p_i$$are called *generalized momenta*
>
>$\mathcal{L}$ is the [[Lagrangian Mechanics#^9ad443|lagrangian]] of course
>
>this is also called the canonical momentum or the momentum conjugate to $q_i$

With these definitions, the Lagrange equations can be written as
$$F_i=\frac{d}{dt}p_i$$
Which of course is the analogy to [[Newtonian Dynamics#^c616f8|Newton's Second Law]].

Note that generalized momenta and forces are not the same as regular forces, they are pseudo-forces that act on the generalized coordinates.

When the lagrangian is independent of a coordinate $q_i$ that coordinate is called **ignorable** or **cyclic**. This means their corresponding momenta are constant and therefore conserved.

## Conservation Laws
If a lagrangian function is *translationally invariant*, meaning the lagrangian is unchanged when the entire system is moved in a direction, then total momentum is conserved. 
>[!defintion]- Proof
>Consider an $N$ body system of particles, each at positions $\textbf{r}_\alpha$ where $\alpha=1,\dots,N$.
>
>To translate the system, we move every particle though a fixed displacement $\epsilon$ such that all the new positions are $\textbf{r}_\alpha+\epsilon$.
>
>The potential energy will be unaffected by the displacement, since the point of zero potential energy is arbitrary, meaning $\delta U=0$.
>
>Clearly, the velocities are also unchanged by the motion, since adding a constant $\epsilon$ does not effect the derivatives
>
>Therefore $\delta T=0$ and thus $\delta\mathcal{L}=0$.
>
>Let us choose $\epsilon$ to be a infinitesimal displacement in the $x$ direction, so that the change in $\mathcal{L}$ is 
>$$\delta\mathcal{L}=\epsilon\frac{\partial\mathcal{L}}{\partial{x_{1}}}+\cdots+\epsilon\frac{\partial\mathcal{L}}{\partial{x_{N}}}=0$$
>This (since $\epsilon$ is not zero) implies that
>$$\sum\limits_{\alpha=1}^{N}\frac{\partial\mathcal{L}}{\partial{x_{\alpha}}}=0$$
>Using Lagrange's Equations we can rewrite each derivative like
>$$\frac{\partial\mathcal{L}}{\partial{x_{\alpha}}}=\frac{d}{dt}\frac{\partial\mathcal{L}}{\partial{\dot{x}_{\alpha}}}=\frac{d}{dt}p_{\alpha x}$$
>Thus,
>$$\sum\limits_{\alpha=1}^{N}\frac{d}{dt}p_{\alpha x}=\frac{d}{dt}P_{x}=0$$
>Meaning the total momentum of the system is constant, and therefore conserved.

>[!example] Theorem: Conservation of the Hamiltonian
>If the [[Lagrangian Mechanics#^9ad443|lagrangian]] does not depend explicitly on time, that is $\partial{\mathcal{L}}/\partial{t}=0$, then the Hamiltonian $\mathcal{H}$ is conserved.

## Lagrange Multipliers
Consider a system with coordinates $x$ and $y$, restricted by a constraint given by
$$f(x,y)=\text{const}$$
We define the action as
$$S=\int_{t_1}^{t_2}\mathcal{L}(x,\dot{x},y,\dot{y})dt$$
We want this to be stationary so we imagine a small displacement to the equations:
$$x(t)\rightarrow x(t)+\delta x(t)\quad\text{ and }\quad y(t)\rightarrow y(t)+\delta y(t)$$
We can write $\delta S$ in terms of the displacements then:
$$\delta S=\int\Bigg(\frac{\partial\mathcal{L}}{\partial{x}}\delta{x}+\frac{\partial\mathcal{L}}{\partial{\dot{x}}}\delta{\dot{x}}+\frac{\partial\mathcal{L}}{\partial{y}}\delta{y}+\frac{\partial\mathcal{L}}{\partial{\dot{y}}}\delta{\dot{y}}\Bigg)dt$$
We can split and integrate by parts to obtain two lagrange equations. First however, we apply a similar premise to the constraint equation
$$\delta f=\frac{\partial f}{\partial{x}}\delta{x}+\frac{\partial f}{\partial{y}}\delta{y}=0$$
We can multiply this, since it is zero, by an arbitrary function $\lambda(t)$ called a **lagrange multiplier**. And we can add it to the integrand without changing the value.
$$\delta S=\int\bigg(\frac{\partial\mathcal{L}}{\partial{x}}+\lambda(t)\frac{\partial f}{\partial{x}}-\frac{d}{dt}\frac{\partial\mathcal{L}}{\partial{\dot{x}}}\bigg)\delta{x}dt+\int\bigg(\frac{\partial\mathcal{L}}{\partial{y}}+\lambda(t)\frac{\partial f}{\partial{y}}-\frac{d}{dt}\frac{\partial\mathcal{L}}{\partial{\dot{y}}}\bigg)\delta{y}dt=0$$
We then get two modified lagrange equations of the form:
$$\frac{\partial\mathcal{L}}{\partial{x}}+\lambda\frac{\partial f}{\partial{x}}=\frac{d}{dt}\frac{\partial\mathcal{L}}{\partial{\dot{x}}}$$
In order to solve for the three functions $x,y,\lambda$, we need three equations. We use the two modified lagrange equations and the one constraint equation.
We also have this relation:
$$\lambda\frac{\partial{f}}{\partial{x}}=F^{\text{cstr}}_{x}$$