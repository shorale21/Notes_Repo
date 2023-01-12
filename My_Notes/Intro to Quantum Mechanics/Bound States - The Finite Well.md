# Bound States - The Finite Well
This is a more realistic potential energy function than the [[Bound States - The Infinite Well|infinite well]].

$$U(x)=\begin{cases}
 0 & 0 < x < L\\
 U_0 & x<0,\space x>L
\end{cases}$$

This still jumps at the walls, but to a finite value rather than infinity. We can now write the [[Bound States - The Shrodinger Equation#^f83325|time independent schrodinger equation]] as$$\frac{d^2\psi(x)}{dx^2}=\frac{2m(U(x)-E)}{\hbar^2}\psi(x)$$
Again, this hints at a proportionality constant between $\psi$ and its second derivative. In between the walls, where $U(x)=0$, this constant is negative, implying a wavelike function. When we are outside the walls, when $U_0>E$, the sign of the constant is positive, implying an exponential function.
For this, we would have to assume $e^{\alpha x}$ to the left of the wall and $e^{-\alpha x}$ on the right side so no part of the function diverges.

>[!example] Definition: Quantum Penetration Depth
>Notice that there is a probability of finding the particle outside the walls, in the finite well. 
>We can say that the exponentially decaying wavefunction has the form$$\psi(x)\propto e^{-\alpha|x|}$$
>The exponential decays by a fraction $1/e$ at the point where $\alpha|x|=1$, corresponding to a distance from the wall of $|x|=1/\alpha$. This distance is called the **penetration depth** and is given by the symbol $\delta$$$\delta=\frac{1}{\alpha}=\frac{\hbar}{\sqrt{2m(U_0-E)}}$$