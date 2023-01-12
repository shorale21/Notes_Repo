# Momentum
Before diving into this subject is it worthy to recall the [[Newtonian Dynamics#^5b1640|Law of Conservation of Momentum]]

This is also extended to systems of particles with no external forces.
We can also write the total momentum of any $N$-particle system as
$$M\dot{\textbf{R}}$$
Where $\textbf{R}$ is the position of the [[Newtonian Dynamics#^71cc46|center of mass]]

## Rocket Analysis
Let's begin with a thought experiment. 
Suppose an astronaut holding a wrench is drifting away from their spacecraft. How do they get back?

One simple way is to throw the wrench as hard as they can in the opposite direction. With no external forces in space, momentum must be constant, and therefore to resolve this, the astronaut will accelerate towars the spacecraft.

This is the basic principle of rockets, although in the case of propulsion systems, it is a continuous expulsion of gas towards the earth that thrusts the rocket upwards.

Let's examine a rocket already in space.
Note that the rocket's mass is steadily decreasing.
At time $t$, the momentum is $P(t)=mv$
At time $t+dt$, the mass is $m+dm$ and the momentum is $(m+dm)(v+dv)$
The fuel that has been ejected has a mass of $-dm$ and a speed of $v-v_{ex}$

Then, the momentum of the system looks like this:
$$P(t+dt)=(m+dm)(v+dv)-dm(v-v_{ex})=mv+mdv+dmv_{ex}$$
Then, since $dP=P(t+dt)-P(t)$, 
$$dP=mdv+dmv_{ex}$$

In space, there are no external forces, so the momentum is constant, that is, $dP=0$ at all times.
Therefore
$$m\space dv=-dm\space v_{ex}$$
We can divide both sides by $dt$, giving 
$$m\dot{v}=-\dot{m}v_{ex}$$

The product $-\dot{m}v_{ex}$ is called the **thrust**. The differential equation can be solved using separation of variables, giving
$$v-v_{0}=v_{ex}\ln(m_{0}/m)$$

## Angular Momentum
#### Single Particle
>[!example] Definition of Angular Momentum for a Single Particle
>The angular momentum of a single particle is defined to be
>$$\ell=\textbf{r}\times\textbf{p}$$
>Where $\textbf{r}$ is the position relative to a chosen origin, and $\textbf{p}$ is the linear momentum of the particle
>This vector has the relation:
>$$\dot{\ell}=\Gamma$$

Let's that the time derivative:
$$\dot{\ell}=\frac{d}{dt}(\textbf{r}\times\textbf{p})=(\dot{\textbf{r}}\times\textbf{p})+(\textbf{r}\times\dot{\textbf{p}})=\textbf{r}\times\textbf{F}=\Gamma$$
this is possible because $\textbf{p}=m\dot{\textbf{r}}$, and finally, $\Gamma$ represents the net torque around the origin.

>[!example] Kepler's Second Law
>As each planet moves around the sun, a line drawn from the planet to the sun sweeps out equal areas in equal times.
>If we choose two points on a planet's orbit, separated by $dt$, and draw lines from each point to the sun, it creates a sector of the ellipse. 
>The law says that any other sector created by a pair of points separated by the same $dt$ (with lines drawn to the sun), will have the exact same area 

#### Several Particles
>[!example] Angular Momentum of Several Particles
>A system of $N$ particles has an angular momentum about an origin, $\textbf{L}$ given by
>$$\textbf{L}=\sum\limits_{\alpha=1}^{N}\ell_{\alpha}=\sum\limits_{\alpha=1}^{N}\textbf{r}_\alpha\times\textbf{p}_\alpha$$
>$\textbf{r}_\alpha$ is the position of each particle (with respect to the origin), and $\textbf{p}_\alpha$ is the linear momentum of each particle.
>
>Conservation Law:
>$$\dot{\textbf{L}}=\Gamma^{\text{ext}}$$

We can define the angular momentum using the [[Newtonian Dynamics#^7d2a62|moment of inertia]] of the system, as
$$\textbf{L}=I\omega$$
Where $\omega$ is the angular velocity