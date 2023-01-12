# The Shrodinger Equation with bound states

Recall the [[The Free Particle Schroedinger Equation#^913c87|free particle shroedinger equation]].

Notice that this equation essentially represents the energy in the wave as shown here:$$\frac{p^{2}}{2m}\Psi(x,t)=\textbf{E}\Psi(x,t)\rightarrow\textbf{KE}\Psi(x,t)=\textbf{E}\Psi(x,t)$$However, this equation only accounts for a free particle, where all of the total energy is kinetic energy. In real life, particles have potential energy from electromagnetism and gravity.$$\big(\text{KE}+U(x)\big)\Psi(x,t)=\text{E}\Psi(x,t)$$

>[!example] Time-Dependent General Shrodinger Equation in 1 dimension
>The General Shrodinger Equation in one dimension is as follows:$$-\frac{\hbar^{2}}{2m}\frac{\partial^{2}\Psi(x,t)}{\partial x^{2}}+U(x)\Psi(x,t)=i\hbar\frac{\partial\Psi(x,t)}{\partial t}$$In this way, we can find a potential energy function for a particle, and then successfully solve the specific shrodinger equation
>>[!tip]+ Solving the temporal part of the schroedinger equation
>>The key here is to use separation of variables. 
>>Let$$\Psi(x,t)=\psi(x)\phi(t)$$
>>Then when we substitute this into the schrodinger equation, we get$$-\frac{\hbar^{2}}{2m}\phi(t)\frac{\partial^{2}\psi(x)}{\partial x^{2}}+U(x)\psi(x)\phi(t)=i\hbar\psi(x)\frac{\partial\phi(t)}{\partial t}$$
>>If we divide both sides by $\psi(x)\phi(t)$, then we get$$-\frac{\hbar^{2}}{2m}\frac{1}{\psi(t)}\frac{\partial^{2}\psi(x)}{\partial x^{2}}+U(x)=i\hbar\frac{1}{\phi(t)}\frac{\partial\phi(t)}{\partial t}$$
>>So, the left side depends soley of position while the right side depends only on time. Notice that since $x$ and $t$ are independently values, the relationship between them must hold constant. So, $$-\frac{\hbar^{2}}{2m}\frac{1}{\psi(t)}\frac{\partial^{2}\psi(x)}{\partial x^{2}}+U(x)=i\hbar\frac{1}{\phi(t)}\frac{\partial\phi(t)}{\partial t}=C$$Note that this only works when the potential energy function is time-independent.
>>So now we can set up the first order differential equation:$$i\hbar\frac{1}{\phi(t)}\frac{\partial\phi(t)}{\partial t}=C\quad\quad\text{or}\quad\quad\frac{d\phi(t)}{dt}=\frac{iC}{\hbar}\phi(t)$$
>>As one can tell, this is a simple first order differential equation to solve. The answer is simply$$\phi(t)=e^{-i(C/\hbar)t}$$
>>We can prove that $C=\hbar\omega=E$, so the full schrodinger equation comes to be:$$\Psi(x,t)=\psi(x)e^{-i(E/\hbar)t}$$

>[!example] Definition: Stationary States
>Let's calculate the probability density of the temportal function derived above.$$\Psi^{*}(x,t)\Psi(x,t)=\big[\psi^{*}(x)e^{i(E/\hbar)t}\big]\big[\psi(x)e^{-i(E/\hbar)t}\big]=\psi^{*}(x)\psi(x)$$
>As can be seen, the time dependency vanishes. So we can see that the wherabouts of the particle do not change in any *observable* way. This is called a **stationary state**. 
>
>For example, consider the atom. [[The Standard Model#^80ae64|Electrons]] orbiting the nucleus should constantly lose energy due to electromagnetic radiation, meaning the atom should be unstable. However, if the electron were simply a stationary cloud, the probability density would be constant and therefore the energy would remain constant.

>[!example] The Spatial Wave Function
>Also known as the time independent shrodinger equation:$$-\frac{\hbar}{2m}\frac{d^{2}\psi(x)}{dx^{2}}+U(x)\psi(x)=E\psi(x)$$
>This is as far as we can go without the potential energy function being defined.
>Notice that the imaginary number $i$ has been removed from the equation as well.

^f83325

>[!tip] Physical Conditions of the wave function
>**Normalization**
>- The total probability of finding the particle must be 1, or$$\int\limits_{\text{all space}}|\Psi(x,t)|^{2}dx=1$$
>- This means the wavefunction cannot diverge
>- The probability integral must converge
>	- This means the function must fall to 0 faster than $|x|^{-1/2}$ as $x\rightarrow\pm\infty$
>
>**Smoothness**
>- The wavefunction and its derivative must be continuous
>	- A discontinuous wavefunction describes a particle with infinite kinetic energy
>	- It also implies infinite momentum due to an arbitrarily small wavelength at the point of discontinuity
>	- If the derivitive is continuous, the second derivative, the kinetic energy, is finite