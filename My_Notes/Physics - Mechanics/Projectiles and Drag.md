# Projectile Motion and Drag Forces
Constants: $g=9.8\space m/s^2$, $\beta=1.6\times10^{-4}\space N\cdot s/m^{2}$,$\gamma=0.25\space N\cdot s^{2}/m^{4}$
$$\DeclareMathOperator{\arctanh}{arctanh}$$ 
## Kinematics
Basic Projectile Motion (no air resistance) includes two properties:
- Constant horizontal velocity $v_x$
- Linear vertical velocity $v_y$
Essentially, the only acceleration is towards the surface of the earth

Start with Newton's 2nd Law: $\vec{F}=m\vec{a}$, where $\vec{a}$ is the acceleration vector.
We know that the only force is gravity, equal to $-mg$, so we can find the acceleration:$$\vec{a}=-g\hat{y}$$

Next, we set up the differential equations for $x$ and $y$ directions:
$$\ddot{x}=0$$$$\ddot{y}=-g$$

These are simple to solve, just by using integration, and this will give us velocity equations:
$$\int{\ddot{x}dt}=\int{0dt}\quad\longrightarrow\quad\dot{x}=C_1$$
$$\int{\ddot{y}dt}=\int{-gdt}\quad\longrightarrow\quad\dot{y}=-gt+C_2$$

And then again, giving position equations:
$$\int{\dot{x}dt}=\int{C_1dt}\quad\longrightarrow\quad x=C_1t+C_3$$
$$\int{\dot{y}dt}=\int{(-gt+C_2)dt}\quad\longrightarrow\quad y=-\frac{g}{2}t^2+C_2t+C_4$$

All of the constants, $C_1,C_2,C_3,C_4$ correspond to initial conditions.
$$C_1=v_{0x}$$
$$C_2=v_{0y}$$
$$C_3=x_0$$
$$C_4=y_0$$

And these give us the final kinematic equations:
>[!example] The General Kinematic Equations for Projectile Motion
>$$x(t)=v_{0x}t+x_0$$
>$$y(t)=-\frac{g}{2}t^2+v_{0y}t+y_0$$

## Air Resistance
Air resistance is a type of **drag force**, a force related to the **velocity** of the object. Here we will be assuming all of the velocity related forces point opposite to the velocity. In reality there exists other forces such as **lift** which points sideways usually.
$$\vec{F}_{drag}=-f(v)\hat{\textbf{v}}$$

The function that describes this, $f(v)$, varies in a very complicated way, but for speeds small compared to the speed of sound, it can be approximated by the following:
$$f(v)=bv+cv^2=f_{lin}+f_{quad}$$The combination of linear an quadratic drag forces.

The physical origins of these are the facts that 
1. the medium exterts a viscous drag in one direction, giving a linear force
2. the projectile has to accelerate the mass of air in front of it, relating to the cross sectional area

This gives us relations (for a spherical particle) such as$$b=\beta D\quad\text{and}\quad c=\gamma D^2$$where $D$ is the diameter of the sphere and $\beta,\gamma$ depend on the medium
1. Some objects we can neglect the quadratic drag since the linear drag is dominant, like small drops in the air, or larger objects in a very viscous medium
2. For most projectiles, the dominant drag force is quadratic, with the linear term neglected. This includes golf balls, cannonballs, and humans
>[!example] Definition: The Reynolds Number
>The dimensionless quantity $R=DvQ/\eta$ is called the Reynolds number
>$D$ has to do with the shape of the object
>$v$ is the velocity
>$Q$ is the density of the medium
>$\eta$ is the viscosity of the medium

When the Reynolds number is large, quadratic drag is dominant

### Linear Air Resistance

Let us begin by working with **linear** air resistance.

We can set up the Newton's Second Law equation$$m\ddot{\textbf{r}}=-mg-bv$$
$$m\dot{\textbf{v}}=-mg-bv$$
This separates into components very easily:$$m\dot{v}_x=-bv_x$$$$m\dot{v}_y=-mg-bv_y$$

##### Horizontal Linear Drag
In this situation, $v_y$ is zero, so we only have one differential equation:
$$\dot{v}_x=-\frac{b}{m}v_x$$
This is an easy enough equation to solve, since it is first order linear:
$$v_x(t)=Ae^{-\frac{b}{m}t}$$
We denote a time parameter $\tau=\frac{m}{b}$ (for linear drag)
$$v_{0x}e^{-\frac{t}{\tau}}$$
Now we find the equation for position, using simple integration.
$$\int_{0}^{t}v_x(t')dt'=x(t)-x(0)$$
$$x(t)=x(0)+\Big[-v_{0x}\tau e^{-\frac{t'}{\tau}}\Big]^{t}_{0}$$
$$x(t)=v_{0x}\tau\big(1-e^{-t/\tau}\big)$$

Notice that as $t$ goes to infinity, $x$ approaches $v_{0x}\tau$, which we can refer to as a **terminal velocity**

##### Vertical Linear Drag
In this case the $v_x$ is always zero, so we only have $v_y$, given by$$m\dot{\vec{v}}_y=-mg-b\vec{v}_y$$
If $v_y$ is small then the object will accelerate downwards until the drag force balances out the gravitational force and we reach a terminal velocity
This value is easy to find by setting $\dot{\vec{v}}_y$ to zero:
$$\vec{v}_{y}=-\frac{mg}{b}=\vec{v}_{\text{ter}}$$

We can rewrite the [[Newtonian Dynamics#^c616f8|2nd Law]] equation to be
$$m\dot{v}_y=-b(v_y-v_{\text{ter}})$$
Solving the differential equation yields:
$$v_y-v_{\text{ter}}=Ae^{-t/\tau}$$
By noting that when $t=0$, $v_y=v_{yo}$, we find our final solution
$$v_{y}(t)=v_{\text{ter}}+(v_{yo}-v_{\text{ter}})e^{-t/\tau}=v_{yo}e^{-t/\tau}+v_{\text{ter}}(1-e^{-t/\tau})$$
Finally, to find $y(t)$ we integrate this function over time.
$$\int_{0}^{t}v_{y}(t')dt'=v_{\text{ter}}t+(v_{yo}-v_{\text{ter}})\tau(1-e^{-t/\tau})$$


##### Range in a Linear Medium

By putting the two above equations together, and eliminating $t$, we get an equation for $y(x)$:
$$y=\frac{v_{yo}+v_{\text{ter}}}{v_{xo}}x+v_{\text{ter}}\tau\ln\bigg(1-\frac{x}{v_{xo}\tau}\bigg)$$

Recall the horizontal range equation without air resistance:
$$R_{\text{vac}}=\frac{2v_{xo}v_{yo}}{g}$$

Solving the $y(x)$ equation when $y=0$ gives us 
$$\frac{v_{yo}+v_{\text{ter}}}{v_{xo}}R+v_{\text{ter}}\tau\ln\bigg(1-\frac{R}{v_{xo}\tau}\bigg)$$
This is a transcendental equation and cannot be solved analytically. Since we usually view air resistance as having a small effect, which suggests that $\tau$ is large and therefore the second term in the logarithm is small.
Thus we can utilize a well known taylor series:
$$\ln(1-\epsilon)=-\bigg(\epsilon+\frac{1}{2}\epsilon^2+\frac{1}{3}\epsilon^3+\cdots\bigg)$$
Given that $\tau$ is sufficiently large we can neglect terms after $\epsilon^3$.
$$\bigg[\frac{v_{yo}+v_{\text{ter}}}{v_{xo}}\bigg]R-v_{\text{ter}}\tau\bigg[\frac{R}{v_{xo}\tau}+\frac{1}{2}\bigg(\frac{R}{v_{xo}\tau}\bigg)^{2}+\frac{1}{3}\bigg(\frac{R}{v_{xo}\tau}\bigg)^{3}\bigg]=0$$
Notice that one obvious solution is $R=0$, since of course its one of the solutions for $y=0$
In addition, we get the less trivial solution of
$$R=\frac{2v_{xo}v_{yo}}{g}-\frac{2}{3v_{xo}\tau}R^2$$
which is easily solved since it is a quadratic.

### Quadratic Air Resistance
Unfortunately, linear air resistance only becomed prevalent in specific cases, the more general case involving quadratic air resistance. Remember, this has to do with accelerating the area in from of the object.

This is when $f_{\text{drag}}=-cv^2\hat{\textbf{v}}$

This poses a problem with a nonlinear differential equation, however since it is first order and separable, it can be solved.

##### Horizontal Quadratic Drag
With no vertical motion, we can set up the differential equation
$$m\frac{dv}{dt}=-cv^2$$
This is of course separable, and so we rewrite like the following:
$$m\int_{v_0}^{v}\frac{dv'}{v'^2}=-c\int_{0}^{t}dt'$$
>[!definition]- Solving the Equation
>We have $$m\int_{v_0}^{v}\frac{dv'}{v'^2}=-c\int_{0}^{t}dt'$$
>The right integral is easy enough, it is just $t'$ evaluated at the ends, but the left integral is a bit trickier:
>$$\int_{v_0}^{v}\frac{dv'}{v'^2}=\bigg[-\frac{1}{v'}\bigg]_{v_0}^{v}=\bigg(\frac{1}{v_{0}}-\frac{1}{v}\bigg)$$
>Thus we have:
>$$m\bigg(\frac{1}{v_{0}}-\frac{1}{v}\bigg)=-ct$$
>$$\frac{1}{v}=\frac{ct}{m}+\frac{1}{v_0}$$
>$$\frac{1}{v}=\frac{ctv_{0}+m}{v_0m}=\frac{ctv_{0}/m+1}{v_0}$$
>$$v=\frac{v_0}{1+cv_0t/m}$$
>Replacing $cv_0/m$ by $1/\tau$ gives the final form:
>$$v=\frac{v_0}{1+t/\tau}$$


The solution is then given by
$$v(t)=\frac{v_0}{1+t/\tau}$$
For quadratic drag, we define $\tau$ to be $\frac{m}{cv_o}$
To find the position, all we do is integrate the velocity, to get:
$$x(t)=v_0\tau\ln(1+t/\tau)$$
With linear drag, the velocity approached a finite limit, whereas with quadratic drag it does not. There is no $v_{ter}$ for horizontal quadratic drag (with no other forces).

##### Vertical Quadratic Drag

As before, we set up the differential equation:
$$m\dot{v}=mg-cv^2$$

In this case, the object has a terminal speed, which happens when the drag force is equal and opposite to gravity.
$$cv^{2}=mg\quad\rightarrow\quad v_{\text{ter}}=\sqrt{\frac{mg}{c}}$$

This second law can be rearranged to $$\dot{v}=g\bigg(1-\frac{v^2}{v_{\text{ter}}^2}\bigg)$$
>[!definition]- Solving the equation
>We have $$\dot{v}=g\bigg(1-\frac{v^2}{v_{\text{ter}}^2}\bigg)$$
>We can separate the variables to get
>$$\frac{dv}{1-v^{2}/v^{2}_{\text{ter}}}=g\space dt$$
>Then
>$$\int_{v_0}^{v}\frac{dv'}{1-v'^{2}/v^{2}_{\text{ter}}}=\int_{0}^{t}g\space dt$$
>This is in fact an inverse hyperbolic tangent integral, and so we integrate
>$$\frac{v_{\text{ter}}}{g}\arctanh{\frac{v}{v_{\text{ter}}}}=t$$
>Solving for $v$ gives us
>$$v=v_{\text{ter}}\tanh{\frac{gt}{v_{\text{ter}}}}$$

To find the position we of course integrate and find the equation
$$y=\frac{v^2_{\text{ter}}}{g}\ln{\bigg(\cosh{\frac{gt}{v_{\text{ter}}}}\bigg)}$$

##### Both Horizontal and Vertical Quadratic Drag

This is where we encounter some problems. We end up with this set of equations:
$$\begin{align*}
m\dot{v}_{x}&=-c\sqrt{v^{2}_{x}+v_{y}^{2}}\space v_x\\
m\dot{v}_{y}&=-mg-c\sqrt{v^2_x+v_y^2}\space v_y
\end{align*}$$
Which are nonlinear, and non separable, meaning not analytically solvable.

## Uniform Magnetic Field Motion
In a magnetic field, force is related to velocity by this relation:
$$\textbf{F}=q\textbf{v}\times\textbf{B}$$
Of course, we can then set up the differential equation:
$$m\dot{\textbf{v}}=q\textbf{v}\times\textbf{B}$$
Suppose $\textbf{v}=(v_x,v_y,v_z)$ and $\textbf{B}=(B_x,B_y,B_z)$
Then
$$q\textbf{v}\times\textbf{B}=(v_yB_z-v_zB_y,\space v_xB_z-v_zB_x,\space v_xB_y-v_yB_x)$$
We can set up the system:
$$\begin{align*}
&m\dot{v}_x=q(v_yB_z-v_zB_y)\\
&m\dot{v}_y=q(v_xB_z-v_zB_x)\\
&m\dot{v}_z=q(v_xB_y-v_yB_x)
\end{align*}$$

This is a system of differential equations, and a linear one (provided the magnetic field is not dependent on the velocity or position)

For simplicity's sake we will assume $B_x$ and $B_y$ are zero, that is that the magnetic field only points in  the z-direction.

This gives us that $\dot{v}_z=0$ meaning the $z$ velocity is constant.
With this we can derive the z position using integration, giving us:
$$z(t)=z_0+v_{z0}t$$

The $x$ and $y$ velocities are more complicated, however. We have
$$\begin{align*}
&\dot{v}_{x}=\omega v_y\\
&\dot{v}_{y}=-\omega v_x
\end{align*}$$
Where $\omega=qB_z/m$
We choose a [[Intro to Complex Numbers#^580f4e|complex number]] such that $\eta=v_x+iv_y$
$$\dot{\eta}=\omega v_{y}-i\omega v_{x}=-i\omega\eta$$
This is a simple ODE to solve, giving us:
$$\eta=Ae^{-i\omega t}$$
Notice that due to [[Complex Exponentials#^8e81f7|Euler's Formula]], this indicates rotation.
Choose another complex number such that $\zeta=x+iy$
Then $$\zeta=\int\eta dt=\frac{iA}{\omega}e^{-i\omega t}+C$$
So,$$x+iy=C_{1}e^{-i\omega t}+C_2+iC_3$$
We then reframe our origin so that the z axis goes through the point $(C_2,C_3)$
$$x+iy=C_{1}e^{-i\omega t}$$
Then, setting $t=0$, we can find $C_1$
$$C_{1}=x_0+iy_0$$
Using this, we get the positions:
$$\begin{align*}
x(t)&=x_{0}e^{-i\omega t}\\
y(t)&=y_{0}e^{-i\omega t}
\end{align*}$$
Let's discuss this geometrically. We already know that the complex exponential indicates sinusoidal motion, so what does it mean for both the x and y coordinates to vary this way?

Usually it indicates circular motion, but remember that z is also changing linearly with time, and therefore the full motion of the particle is around the z-axis as the center of rotation moves along it. 

This is called **helical motion**