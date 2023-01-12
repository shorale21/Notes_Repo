# The Uncertainty Principle

The values of momentum and velocity must be uncertain, as the [[Double Slit Experiment#^1ac403|double slit experiment]] shows that a particle will go through either of the slits, or both.

If the experiment is repeated identically, the momentum will have a range of values.

For this, we require some statistical mechanics.

>[!example] Statistics of the uncertainty principle
>The **Standard Deviation** is a measure of how far values deviate from the average (mean)
>Suppose a repeated experiment is performed to determine the value of a quantity $Q$
>- The Value $Q_1$ is found $n_1$ times, and $Q_2$ is found $n_2$ times
>
>The mean average will be given by$$\overline{Q}=\frac{\sum_{i}Q_{i}n_{i}}{\sum_{i}n_i}$$
>The standard deviation is often called the root-mean-squared deviation, and the formula shows why:$$\Delta Q=\sqrt{\frac{\sum_{i}(Q_{i}-\overline{Q})^{2}n_{i}}{\sum_{i}n_{i}}}$$

^a97947

>[!example] Example: Single Slit Interference
>Suppose we set up an experiment where a beam of particles is sent through a single, narrow slit, creating a diffraction pattern on a screen
>- The momentum of these particles, $p_x$, can be determined easier the wider/larger the diffraction pattern
>- However, the thinner the diffraction pattern, the easier it is the predict the position of the particles, $x$
>
>This leads us to a relation:$$\Delta p_{x}\propto\frac{1}{\Delta x}$$or, the uncertainties are *inverseley proportional*
>
>We can see this by looking at the wave mechanics
>- Remember that momentum is [[Properties of Matter Waves#^72f630|related]] to wavelength
>- So, if we know $\lambda$, we can find $p$
>- Say we are looking at a wave, and we want to select a random particle of the wave and check its values for momentum and position
>- If the wave stretched infinitely long, we would be completely certain of wavelength
>	- This means we have 100% certainty of the momentum
>	- However, it is 100% impossible to predict where a particle taken at random will exist on the infinite x-axis
>- If the wave was very small, say we could only see a part of one cycle, it would be difficult to know the wavelength
>	- Therefore, we would be uncertain on the momentum
>	- We would also be uncertain on the position of a particle, but there are a much smaller range of values it could be at, and therefore less uncertainty than before
>- If there was only an infinitesimally small slice of the wave,
>	- The wavelength would be completely unknown, with no way of approximating or guessing it, in other words, 100% uncertainty
>	- However, there would only be 1 value of x where a particle could be found, so we have 100% certainty on the position

>[!definition] Heisenberg Uncertainty Principle
>It is theoretically impossible to know both the position and momentum of a particle with 100% certainty, or $\Delta p_x$ and $\Delta x$ cannot be zero simultaneously
>There is a theoretical lower limit:$$\Delta p_{x}\Delta x\ge\frac{\hbar}{2} $$
>This can be extended to 3 dimensions:$$\Delta p_{x}\Delta x\ge\frac{\hbar}{2}\quad\quad\Delta p_{y}\Delta y\ge\frac{\hbar}{2}\quad\quad\Delta p_{z}\Delta z\ge\frac{\hbar}{2}$$
>Another consequence is:$$\Delta E\Delta t\ge\frac{\hbar}{2}$$