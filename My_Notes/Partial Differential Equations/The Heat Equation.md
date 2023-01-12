>[!example]- Derivation of Heat in a One-Dimensional Rod
>Consider of rod of constant cross-sectional area $A$
>- Oriented in the $x$-direction
>- From $x=0$ to $x=L$
>
>We introduce the amount of thermal energy per unit volume as the **Thermal Energy Density**
>$$\textbf{Thermal Energy Density}=e(x,t)$$
>We insulate perfectly the lateral surface of the rod so that no thermal energy can escape that way
>The **heat energy** of the rod between $x$ and $x+\Delta x$ is given by$$\textbf{Heat Energy}=e(x,t)A\Delta x$$
>- Note that as $\Delta x$ becomes smaller, $e(x,t)$ becomes a better approximation of the heat density in the slice
>
>The **rate of change** of heat energy is given by$$\frac{\partial}{\partial t}[e(x,t)A\Delta x]$$
>We will also denote the heat flux as $\phi(x,t)$ and the heat source/generation as $Q(x,t)$
>Let us now derive a conservation of heat equation
>$$\text{Consider any finite segment, from }x=a\text{ to }x=b\text{of the one-dimensional rod,}$$
>$$\text{The total heat energy is }\int_{a}^{b}[e(x,t)A]dx,$$
>$$\frac{d}{dt}\int_{a}^{b}edx=\phi(a,t)-\phi(b,t)+\int_{a}^{b}Qdx,$$
>$$\text{by fundamental theories, }\phi(a,t)-\phi(b,t)=-\int_{a}^{b}\frac{\partial\phi}{\partial x}dx,$$
>$$\int_{a}^{b}\bigg(\frac{\partial e}{\partial t}+\frac{\partial\phi}{\partial x}-Q\bigg)dx=0,$$
>$$\frac{\partial e}{\partial t}=-\frac{\partial\phi}{\partial x}+Q$$
>Let $u(x,t)$ denote the temperature, and let us introduce the heat capacity, or specific heat $c(x)$, of the rod
>As well as this, let $\rho(x)$ be the mass density of the rod, meaning
>$$e(x,t)A\Delta x=c(x)u(x,t)\rho(x)A\Delta x$$
>$$e(x,t)=c(x)\rho(x)u(x,t)$$
>Placing this in the above result gives us$$c(x)\rho(x)\frac{\partial u}{\partial t}=-\frac{\partial\phi}{\partial x}+Q$$
>Now, using [[The Heat Equation#^a4e867|Fourier's Law]], we can consolidate this further into the general heat equation:$$c(x)\rho(x)\frac{\partial u}{\partial t}=\frac{\partial}{\partial x}\bigg(K_{0}\frac{\partial u}{\partial x}\bigg)+Q(x,t)$$
>In the case of a constant rod and constant sources:$$c\rho\frac{\partial u}{\partial t}=K_{0}\frac{\partial^2 u}{\partial x^2}+Q$$
>And finally, in the case of no sources, and dividing by the constant $c\rho$,$$\frac{\partial u}{\partial t}=k\frac{\partial^2 u}{\partial x^2}$$
>Where $k$ is called the **thermal diffusivity**


>[!List] Fourier's Law
>Let heat flux be $\phi(x,t)$ and let temperature be $u(x,t)$
>1. If the temperature is constant in a region, no heat energy flows
>2. If there are temperature differences, the heat energy flows from the hotter region to the colder one
>3. The greater the temperature differences, the greater is the flow of energy
>4. The flow of heat energy will vary for different materials
>Let's summarize these in terms of our equations:
>1. If $u(x_0,t_0)=C$, $\phi(x_0,t_0)=0$
>2. If $u(x_0,t_0)$ is hotter that the surroundings, then $\phi(x_0,t_0)<0$
>All of these conform into **Fourier's Law:**$$\phi=-K_{0}\frac{\partial u}{\partial x}$$
>Note that $K_0$ is the thermal conductivity of the material

^a4e867

^a52976
>[!example] The Heat Equation (or the diffusion equation)
>The Heat equation for a uniform rod with no external sources is as follows:
>$$u_{t}=ku_{xx}$$
>Where $k$ is the thermal diffusivity

^f7f168

>[!example] Definition: Initial Conditions
>An **Initial Condition** for a [[Intro to PDE#^9a515d|partial differential equation]] is a given condition of the problem showing the state at a initial **time**
>For example:$$u(x,t_0)=f(x)$$
>Note that one initial condition is required per time differential order

^84b5c4

>[!example] Definition: Boundary Conditions
>A **Boundary Condition** is a given condition of the problem showing the state at a certain **position**, or boundary
>For example: $$u(x_0,t)=f(t)$$
>This is called **prescribed value**
>In addition, we can use differentials to describe rate of change at boundaries:
>$$\frac{\partial u}{\partial x}(0,t)=f(t)$$
>This is called **prescribed flux**
>Boundary conditions are called **Steady** if they do not depend on $t$

^acae29

>[!example] Definition: Newton's Law of Cooling
>Newton's law of cooling is a specific boundary condition:
>$$-K_{0}(0)\frac{\partial u}{\partial x}(0,t)=-H\big[u(0,t)-u_B(t)\big]$$

>[!example] Definition: Steady-State Solution
>A **Steady State** or **Equilibrium** solution is one that does not depend on time. 
>For example, in the heat equation:
>$$u(x,t)=u(x)$$

#### Derivation of the Heat Equation in Higher Dimensions

Let's start by looking at **Heat Energy**, which in three dimensions looks like:$$\iiint\limits_{R}c\rho u\space dV$$

Heat flux, which is the the flow of heat energy is therefore a [[Mathematical Formalisations#^35a3f1|vector]], denoted by $\phi$
For a solid body, the flux is related to the outward unit normal vector $\hat{n}$

Now we use the conservation of heat energy to derive an equation. At each point on the surface the amount of heat flowing out is the normal component of the heat flux vector, which is given by$$\phi\cdot\hat{n}$$

To find the total heat flow outwards, we use the differential $dS$ and add up all the normal vectors across the surface. This gives the total heat flow outwards as:
$$\oint \phi\cdot\hat{n}\space dS$$

Using $Q$ is the amount of heat generated per unit colume, this gives a heat conservation equation:
$$\frac{d}{dt}\iiint\limits_{R}c\rho u\space dV=-\oint\phi\cdot\hat{n}\space dS\space +\iiint\limits_{R}Q\space dV$$
Which is essentially "Heat Energy = Heat Generated - Heat Flux Out"

Using Gauss's Divergence Theorem, the equation resolves to:
$$\frac{d}{dt}\iiint\limits_{R}c\rho u\space dV=-\iiint\limits_{R}\nabla\cdot\phi\space dS\space +\iiint\limits_{R}Q\space dV$$

Combining the integrals and reducing produces the following equation:
$$c\rho\frac{\partial u}{\partial t}-\nabla\cdot\phi+Q$$
Expanding [[The Heat Equation#^a4e867|Fourier's Law]] in three dimensions, $\phi=-K_0\nabla u$
Thus the above equation reduces to the final heat equation
>[!example] Definition: The Multi Dimensional Heat Equation
>The Heat Equation in three dimensions (or more) is given by
>$$c\rho\frac{\partial u}{\partial t}=k\nabla^2u$$
>
>In Polar Coordinates, the equation looks like this:
>$$\frac{c\rho}{k}\frac{\partial u}{\partial t}=\frac{1}{r^{2}}\frac{\partial}{\partial r}\bigg(r^{2}\frac{\partial u}{\partial r}\bigg)+\frac{1}{r^{2}\sin\phi}\frac{\partial}{\partial\phi}\bigg(\sin\phi\frac{\partial u}{\partial\phi}\bigg)+\frac{1}{r^{2}\sin^{2}\phi}\frac{\partial^{2}u}{\partial\theta^2}$$