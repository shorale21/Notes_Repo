# Newtonian Dynamics


#### Newton's First and Second Laws
>[!example] Newton's First Law
>**<p style="text-align:center;">In the absence of forces, a particle moves with constant velocity.</p>**
>
>This is often called the law of inertia, showing that massful bodies resist changes in states of motion

>[!example] Newton's Second Law
>**<p style="text-align:center;">Force equals mass time acceleration</p>**
>
>This of course leads to the classic equation $$\textbf{F}=m\textbf{a}=m\ddot{\textbf{r}}$$

^c616f8

Note that momentum, $\textbf{p}$, is $m\textbf{v}$, and therefore$$\dot{\textbf{p}}=m\dot{\textbf{v}}=m\textbf{a}$$

The second law can then be restated as$$\textbf{F}=\dot{\textbf{p}}$$

Due to more modern discoveries, especially in general and [[Intro to Special Relativity|special]] relativity, it has been revealed that Newton's Second Law only holds true in what are known as [[Intro to Special Relativity#^054abc|inertial reference frames]], frames moving at constant velocity.

Let's explore an example:

Say there is a skateboard on a bus.
Imagine the reference frame being the bus. When the bus accelerates to the right, the skateboard appears to accelerate to the left from the current reference frame.

However, there is no net force on the skateboard. This means the bus is a **non-inertial** frame, since the net force is zero and the acceleration is not, thus breaking the second law.

#### Newton's Third Law
An interesting thing to note in physics is that forces always invole two objects. If there is a force on an object, there must also be another object to *extert* that force, and objects must also extert a force on another object.

>[!example] Newton's Third Law
>If object 1 exterts a force $\textbf{F}_{21}$ on object 2, the object 2 always exterts a reaction force $\textbf{F}_{12}$ on object 1 given by$$\textbf{F}_{12}=-\textbf{F}_{21}$$

Let's discuss how this relates to the conservation of momentum.

Consider two objects, where object 1 exterts force $\textbf{F}_{21}$ on object 2.

The net force on object 1 is given by $\textbf{F}_{1}=\textbf{F}_{1}^{\text{ext}}+\textbf{F}_{12}$

And the net force on object 2 is given by $\textbf{F}_2=\textbf{F}^{\text{ext}}_{2}+\textbf{F}_{21}$

Using the second law, we can compute the time derivatives of the momenta:
$$\dot{\textbf{p}}_1=\textbf{F}_{12}+\textbf{F}_{1}^{\text{ext}}$$
$$\dot{\textbf{p}}_2=\textbf{F}_{21}+\textbf{F}_{2}^{\text{ext}}$$
The total momentum of the two objects is given by
$$\textbf{P}=\textbf{p}_{1}+\textbf{p}_{2}$$and
$$\dot{\textbf{P}}=\dot{\textbf{p}}_{1}+\dot{\textbf{p}}_{2}$$
In this equation the forces exterted on each particle by the other cancel out, giving:
$$\dot{\textbf{P}}=\textbf{F}_{1}^{\text{ext}}+\textbf{F}_{2}^{\text{ext}}=\textbf{F}^{\text{ext}}$$
So, when the external force is zero, the momentum does not change, or in other words, it is conserved.

>[!example] Law of Conservation of Momentum
>If the net external force on an $N$-particle system is zero, the systen's total momentum is constant.
>In mathematics:
>If$$\textbf{F}^{\text{ext}}=0$$Then$$\textbf{P}=C$$
>Where $C$ is a constant

^5b1640

#### Newton's Second Law in Polar Coordinates
Let's derive Newton's Second Law in [[Mathematical Formalisations#^ae1334|Polar Coordinates]].
First we start with the basic law:$$\vec{\textbf{F}}=m\vec{\textbf{a}}$$

In Polar Coordinates, $\vec{\textbf{a}}=\ddot{\vec{\textbf{r}}}$, and $\vec{\textbf{r}}=r\hat{\textbf{r}}$
So,
$$\dot{\vec{\textbf{r}}}=\frac{d}{dt}(r\hat{\textbf{r}})=\dot{r}\hat{\textbf{r}}+r\frac{d\hat{\textbf{r}}}{dt}$$
Now we search for the time derivative of $\hat{\textbf{r}}$, since in polar coordinates $\hat{\textbf{r}}$ changes with $\phi$, In fact since $\hat{\textbf{r}}_1$ and $\hat{\textbf{r}}_2$ would be sufficiently parallel for a sufficiently small $\Delta t$, the change in $\hat{\textbf{r}}$ is in the direction of $\hat{\phi}$ with a magnitude of $\Delta \phi$. In other words, the infinitesimally small (the derivative) change in $\hat{\textbf{r}}$ is given by:
$$\frac{d\hat{\textbf{r}}}{dt}=\dot{\phi}\hat{\phi}$$
This gives us our velocity vector in polar coordinates,$$\vec{\textbf{v}}=\dot{r}\hat{\textbf{r}}+r\dot{\phi}\hat{\phi}$$
Now we need to differentiate a second time, to get the acceleration:
$$\vec{\textbf{a}}=\ddot{r}\hat{\textbf{r}}+\frac{d\hat{\textbf{r}}}{dt}\dot{r}+\dot{r}\dot{\phi}\hat{\phi}+r\ddot{\phi}\hat{\phi}+\frac{d\hat{\phi}}{dt}r\dot{\phi}$$
Next we need to determine the time derivative of $\hat{\phi}$. $\hat{\phi}$ Notice how $\hat{\phi}$ gets flatter as $\phi$ increases, meaning they are inversely related. In addition, $\hat{\phi}$ changes in the direction of $\hat{\textbf{r}}$. This gives us
$$\frac{d\hat{\phi}}{dt}=-\dot{\phi}\hat{\textbf{r}}$$
This gives us the final result for the acceleration:
$$\vec{\textbf{a}}=(\ddot{r}-r\dot{\phi}^2)\hat{\textbf{r}}+(r\ddot{\phi}+2\dot{r}\dot{\phi})\hat{\phi}$$
Multiply this result by $m$ and we get the net force, thus giving us Newton's Second Law

#### Center of Mass

^71cc46

Consider of group of $N$ particles. The center of mass of the system is defined to be 
$$\textbf{R}=\frac{1}{M}\sum\limits_{\alpha=1}^{N}m_{\alpha}\textbf{r}_{\alpha}$$

A non point object can be considered a continuous set of particles, and therefore this sum becomes an integral:
$$\textbf{R}=\frac{1}{M}\int\limits_{Z}\textbf{r}dm$$

#### Moment of Inertia
>[!example] Moment of Inertia
>Defined to be an object or system's resistance to rotation, the moment of inertia is given by
>$$I=\sum m_{\alpha}r^{2}_{\alpha}$$
>Where $r_\alpha$ is the distance to the axis of rotation
>
>When  system is continuous, not discrete, this sum becomes an integral.

^7d2a62
