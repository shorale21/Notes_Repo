# The Infinite Well
This is the situation in which $U(x)$ gives the simplest solution to the [[Bound States - The Shrodinger Equation#^f83325| time-independent Shrodinger equation]]

We have a particle confined between insurmountable, infinitely rigid walls. Classically, it would bounce back and forth, but the quantum solution is actually standing waves.

In this situation, we imagine an infinitely high $U(x)$ outside the walls. Then the wavefunction must be $0$ outside the walls.


>[!example] Deriving the Infinite Well Function
>we choose the potential energy to be $0$ between the walls
>So, the time independent schrodinger equation becomes$$-\frac{\hbar}{2m}\frac{d^2\psi(x)}{dx^2}=E\psi(x)$$
>So, assigning $k=\sqrt{\frac{2mE}{\hbar^2}}$,$$\frac{d^2\psi(x)}{dx^2}=-k^2\psi(x)$$
>One satisfactory result is this:$$\psi(x)=A\sin(kx)$$
>Now we impose the boundary condition that the wavefunction must be zero outside the walls.
>We first demand that $\psi(x)=0$ when $x=L$, the "right" wall$$A\sin(kL)=0$$
>Notice that $A$ cannot be zero, since that eliminates the particle entirely. The only way the wavefunction can be continuous yet nonzero is if $$kL=n\pi$$where $n$ is an integer.
>Now we can write $$E=\frac{n^2\pi^2\hbar^2}{2mL^2}$$
>So then we get$$\psi_n(x)=A\sin\left(\frac{n\pi x}{L}\right)$$
>Which is the standing wave form.

>[!example] The continuous wave function for a particle in an infinite well
>$$\psi_n(x)=\begin{cases}
 \sqrt{\frac{2}{L}}\sin(\frac{n\pi x}{L}) & 0 < x < L\\
 0 & x<0,\space x>L
\end{cases}\quad\quad E_n=\frac{n^2\pi^2\hbar^2}{2mL^2}$$