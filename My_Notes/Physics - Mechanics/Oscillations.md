## Hooke's Law

>[!example] Definition: Hooke's Law
>The force exterted by a spring (restricted to the x-axis) has the form 
>$$F_{x}(x)=-kx$$
>Where $x$ is the displacement of the spring from equilibrium, and $k$ is a positive number called the force constant. This force is an example of a restoring force.
>From this, we get the [[Energy#^4f5cbe|potential energy]] of the object-spring system:
>$$U(x)=\frac{1}{2}kx^2$$

^ba95a0

>[!example] Definition: Restoring Force
>A Restoring Force is a force that drives an object back into a stable equilibrium.
>In other words, it is a force that goes opposite the direction of motion when motion is away from a stable equilibrium.

^b1ad56

Here is a proof that for sufficiently small displacements, hooke's law is valid for an arbitrary one dimensional system.
Consider a [[Energy#^8b8deb|conservative]] one dimensional system that has a [[Energy#^6562c3|stable equilibrium]] position at $x=0$.
The potential energy is given by $U(x)$. We can expand this into a taylor series around the equilibrium point, giving us
$$U(x)=U(0)+U'(0)x+\frac{1}{2}U''(0)x^2+\cdots$$
If $x$ remains small, the first three terms should be good enough. 
1. The first term is a constant, which may be subtracted since that is physically the same as changing reference frame inertially, so we can say $U(0)=0$. 
2. Since $x=0$ is an equilibrium point, $U'(0)=0$, and thus we are just left with the third term.

If we set $k$ to $U''(0)$, we are left with$$U(x)=\frac{1}{2}kx^2$$

## Simple Harmonic Motion

We now examine [[Newtonian Dynamics#^c616f8|Newton's Second Law]] for a particle of mass $m$ displaced from the equilibrium position.

We introduce the constant $\omega=\sqrt{k/m}$ such that the equation becomes:
$$\ddot{x}=-\frac{k}{m}x=-\omega^2x$$

The constant $\omega$ is the angular frequency.

The general solution to this equation can be given in the form of [[Complex Exponentials#^8e81f7|complex exponentials]]:
$$x(t)=C_1e^{i\omega t}+C_2e^{-i\omega t}$$
In other terms, this means
$$x(t)=B_{1}\cos{(\omega t)}+B_2\sin{(\omega t)}$$
The above equation is the definition of simple harmonic motion.
>[!example] Definition: Simple Harmonic Motion
>Simple Harmonic Motion is oscillatory motion governed by [[Oscillations#^ba95a0|Hooke's Law]] and represented by the equation
>$$B_1\cos{(\omega t)}+B_2\sin{(\omega t)}$$
>where $\omega=\sqrt{\frac{k}{m}}$ is the angular frequency of the motion.

^5ef503

Notice that this function repeats itself after time $\tau$ for which $\omega\tau=2\pi$. Thus the period is
$$\tau=2\pi\sqrt{\frac{m}{k}}$$

Let's define a new constant $A=\sqrt{B_1^2+B_2^2}$. Let's define $\delta$ as the lower angle of the right triangle where the hypotnuse is $A$. Thus
$$x(t)=A\bigg[\frac{B_1}{A}\cos{(\omega t)}+\frac{B_2}{A}\sin{(\omega t)}\bigg]=A[\cos{\delta}\cos{(\omega t)}+\sin{\delta}\sin{(\omega t)}]=A\cos{(\omega t-\delta)}$$

This allows us to determine the oscillation amplitude as $A$. The above equation is the **phase-shifted cosine solution**.

## Two-Dimensional Oscillators

>[!example] Definition: Isotropic Harmonic Oscillator
>In this case, the [[Oscillations#^b1ad56|restoring force]] is propertional to the displacement from equilibrium, with the same constant in all directions. The force is then
>$$\textbf{F}=-k\textbf{r}$$
>This force is a [[Energy#^b84951|central force]].

The isotropic harmonic oscillator is described by two independent equations:
$$\ddot{x}=-\omega^2x$$$$\ddot{y}=-\omega^2y$$
These resolve into oscillatory equations:
$$x(t)=A_x\cos{(\omega t)}$$$$y(t)=A_{y}\cos{(\omega t-\delta)}$$
Where $\delta=\delta_y-\delta_x$ the relative phase of the oscillations

>[!example] Definition: Anisotropic Oscillation
>The components of the [[Oscillations#^b1ad56|restoring force]] are proportional to the components of displacement, but the constants are different for each component. In math:
>$$\textbf{F}=\langle -k_xx,-k_yy,-k_zz\rangle$$

In anisotropic oscillation, the solution is again a trignometric function. Now however, we define the angular frequency to be different for each component:
$$\omega_i=\sqrt{\frac{k_i}{m}}$$
Thus the solution looks like
$$x(t)=A_x\cos{(\omega_x t)}$$$$y(t)=A_{y}\cos{(\omega_y t-\delta)}$$
This brings some interesting results. The ratio $\omega_y/\omega_x$ gives insight into the motion. If the ratio is [[Sets#^d3aac2|rational]], then the motion is periodic.
If the ration is irrational, the motion is aperiodic, and never repeats itself. This kind of oscillatory motion is called **quasiperiodic**, since the motion of the individual components is periodic, but the entire motion is not.

## Damped Oscillations
Consider an object in one dimension that is subject to a [[Oscillations#^ba95a0|hooke's law]] force and a linear resistive force.
This gives us a differential equation:
$$m\ddot{x}+b\dot{x}+kx=0$$
Defining constants $b/m=2\beta$ and $\sqrt{k/m}=\omega_0$, this can be rewritten as
$$\ddot{x}+2\beta\dot{x}+\omega_0^2x=0$$
Both $\beta$ and $\omega_0$ have units of inverse time, or frequency.
The solution to this differential equation is then
$$x(t)=e^{-\beta t}\bigg(C_1e^{\sqrt{\beta^2-\omega_0^2}}+C_2e^{-\sqrt{\beta^2-\omega_0^2}}\bigg)$$
Now we check the various ranges of the damping constant $\beta$.
#### Undamped Oscillation
If the constant $\beta$ is zero, then the solution reduces to 
$$x(t)=C_1e^{i\omega_0t}+C_2e^{-i\omega_0t}$$
Which is the equation for [[Oscillations#^5ef503|Simple Harmonic Motion]].

#### Weak Damping
Suppse the damping constant $\beta$ is small. Specifically, $\beta<\omega_0$. In this case, the square root in the exponents is imaginary, and we can write:
$$\sqrt{\beta^2-\omega_0^2}=i\sqrt{\omega_0^2-\beta^2}$$
Let's set
$$\omega_1=\sqrt{\omega_0^2-\beta^2}$$
The solution is then 
$$x(t)=e^{-\beta t}\Big(C_1e^{i\omega_{1}t}+C_2e^{-i\omega_{1}t}\Big)$$
Qualitatively, this is the product between an infinitely undamped oscillator, and a decaying exponential. Thus the graph of this motion will appear as an oscillator in which the amplitude is exponentially decreasing.

#### Strong Damping
Suppose that $\beta>\omega_0$. In this case the square root is real, and this the solution is
$$x(t)=C_1e^{-\Big(\beta-\sqrt{\beta^2-\omega_0^2}\Big)}+C_2e^{-\Big(\beta+\sqrt{\beta^2-\omega_0^2}\Big)}$$
Both coefficients to $t$ will always be negative, so this function simply decays after the initial swing.
A graph with an initial kick would rise above the equilibrium to a maximum and then exponentially decay back to zero as time goes to infinity.

#### Critical Damping
This is when $\beta=\omega_0$. The two separate solutions are actually the same in this one, since
$$\sqrt{\beta^2-\omega_0^2}=0$$
therefore
$$x(t)=e^{-\beta t}$$
then we can define another linearly independent solution to be 
$$x(t)=te^{-\beta t}$$
Thus the general solution is
$$x(t)=C_1e^{-\beta t}+C_2te^{-\beta t}$$
Both of these functions decay at the same rate when $t$ is arbitarily large, so the decay parameter is $\beta$
####
Thus we can define:
>[!example] Types of Damping in Oscillatory Motion
>$$\begin{array}{ c c c }
>\text{damping} & \beta & \text{decay parameter}\\
>\hline
>\text{none} & \beta=0 & 0\\
>\text{under} & \beta<\omega_{0} & \beta\\
>\text{critical} & \beta=\omega_{0} & \beta\\
>\text{over} & \beta>\omega_{0} & \beta-\sqrt{\beta^2-\omega_0^2}
>\end{array}$$

## Driven Damped Oscillations

Any natural oscillator will come to rest due to the inevitable damping forces that drain energy.
If one wants the oscillation to continue, there must be an external "driving" force to maintain them.

This gives a a nonhomogenous differential equation:
$$m\ddot{x}+b\dot{x}+kx=F(t)$$
We again replace the constants to give us:
$$\ddot{x}+2\beta\dot{x}+\omega_0^2x=f(t)$$
Let us assume the driving force is oscillatory and sinusoidal, given by:
$$f(t)=f_0\cos{(\omega t)}$$
>[!defintion]- Solving this equation
>We have the equation
>$$\ddot{x}+2\beta\dot{x}+\omega_0^2x=f_0\cos{(\omega t)}$$
>We solve this by finding a particular solution, $x_p$ and also a homogenous solution $x_c$.
>First, let's define a complex function
>$$z(t)=x(t)+iy(t)$$
>where $y(t)$ satisfies the differential equation.
>Thus
>$$\ddot{z}+2\beta\dot{z}+\omega_0^2z=f_0e^{i\omega t}$$
>Now we need to find a solution for $z(t)$ and simply take the real part.
>We use the method of undetermined coefficients, and set $z(t)=Ce^{i\omega t}$.
>Substituting this gives us:
>$$(-w^2+2i\beta\omega+\omega_0^2)Ce^{i\omega t}=f_0e^{i\omega t}$$
>Then our guess is only a solution if
>$$C=\frac{f_0}{\omega_0^2-\omega^2+2i\beta\omega}$$
>Suppose $C=Ae^{-i\delta}$
>We then multiply by the complement such that
>$$A^2=CC^*=\frac{f_0^2}{(\omega_0^2-w^2)^2+4\beta^2\omega^2}$$
>Next, we find $\delta$:
>$$f_0e^{i\delta}=A(\omega_0^2-w^2+2i\beta\omega)$$
>$$\delta=\arctan{\bigg(\frac{2\beta\omega}{\omega_0^2-\omega^2}\bigg)}$$
>Thus we have $$z(t)=Ae^{i(\omega t-\delta)}$$
>By [[Complex Exponentials#^8e81f7|Euler's Formula]] the real part of this exponential is
>$$x(t)=A\cos{(\omega t-\delta)}$$
>This is the particular solution. It is easy to solve the homogenous solution, as it is of the form
>$$x_c=C_1e^{r_1t}+C_2e^{r_2t}$$

>[!example] Definition: transients
>Functions that become irrelevant as time passes. In the driven oscillator equation, the homogenous solution,
>$$x_c=C_1e^{r_1t}+C_2e^{r_2t}$$
>is a sum of transiets, since the long term solution is dominated by the cosine term.

Due to all of this, we can rewrite the final equation (for a linear damped driven oscillator) as
$$x(t)=A\cos{(\omega t-\delta)}+A_{tr}e^{-\beta t}\cos{(\omega_1-\delta_{tr})}$$

## Resonance

Let's take a look at the amplitude constant for the linear driven oscillator:
$$A^2=\frac{f_0^2}{(\omega_0^2-w^2)^2+4\beta^2\omega^2}$$
One thing to notice is that $A\propto f_0$. In addition, when $\omega_0=\omega$, or when the driving frequency is equal to the oscillation frequency, the entire first term of the denominator is canceled out.

>[!example] Definition: Resonance
>The phenomenon in which there is a dramatically greater response of an oscillator when driven at the right frequency. 
>
>Normally this frequency is the same as the natural frequency

>[!example] Definition: Quality Factor of Resonance
>For resonance, we can define a **quality factor** $Q$ where
>$$Q=\omega_0/2\beta$$the ratio between the height of the resonance peak and the width of the peak.

The phase difference $\delta$ by which the oscillator's motion lags behind the driving force is given by
$$\delta=\arctan{\bigg(\frac{2\beta\omega}{\omega_0^2-\omega^2}\bigg)}$$
When $\omega$ is very small compared to $\omega_0$, the oscillations are almost always in perfect step with the driving force. At resonance, the inside of the inverse tangent is infinite, and thus $\delta=\pi/2$ and the oscillations are $90\degree$ behind the driving force.

## Fourier Series Solutions

Let us return to the equation of motion:
$$\ddot{x}+2\beta\dot{x}+\omega_0^2x=f$$
By the theory of [[Intro To the Fourier Series#^0cc02e|fourier series]], the driving force can be written as
$$f(t)=\sum\limits_{n=0}^{\infty}f_n\cos{(n\omega t)}$$
And thus 
$$x_n(t)=A_n\cos{(n\omega t-\delta_n)}$$