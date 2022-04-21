# The Doppler Effect
If a light source moves relative to an observer, the frequency observed may be different than the frequency emitted

<u>**Explanation**</u>
- We will be using similar variables to the [[Lorentz Transformations#^4d085e|lorentz transformations]] page
- An Observer stands at the origin, in frame $S$
- A light source, at rest in frame $S'$, moves relative to frame $S$
	- It moves away from the observer
	- It moves exactly enough distance so that it propogates one wave at position 1 and the next wave at position 2
- It emits a frequency of $f_{source}$
- Let us call the time between the prodcution each wave front $\Delta t_p$
- Since the source gets farther away beetween each wave front, the time of arrival at the observer, $\Delta t_a$, will be greater than $\Delta t_p$$$\Delta t_a=\Delta t_{p}+\frac{v}{c}\Delta t_pcos(\theta)=\Delta t_p\left(1+\frac{v}{c}cos(\theta)\right)$$
- The period observed by the viewer at the origin of $S$ will be $\Delta t_a$
- However, the source period is not $\Delta t_p$ due to special relativity
	- Due to [[Consequences of SR#^9271df|time dilation]], the period of the source will be longer
	- This gives $\Delta t_p=\gamma_vT_{source}$$$\Delta t_{a}=\gamma_vT_{source}\left(1+\frac{v}{c}cos(\theta)\right)=T_{source}\frac{1+\frac{v}{c}cos(\theta)}{\sqrt{1-\frac{v^2}{c^2}}}$$
- We can invert this equation to get the frequency

>[!info] Frequency of a moving source
>The frequency as viewed by an observer $f_{obs}$ is given as a function of the source frequency $f_{source}\space$ as the source moves away at an angle $\theta$:$$f_{obs}=f_{source}\frac{\sqrt{1-\frac{v^2}{c^2}}}{1+\frac{v}{c}cos(\theta)}$$
>If the source moves directly away ($\theta=0$):$$f_{obs}=f_{source}\left(\frac{1-\frac{v}{c}}{1+\frac{v}{c}}\right)^\frac{1}{2}$$

- Notice how the observed frequency is smaller than the source frequency, meaning the wavelength must increase to conserve wave speed
- This is called a **redshift** since it shifts the color to a longer wavelength and closer to the red end of the spectrum
	- A clue the universe is expanding is shown in the redshift from distant stars
- When the source moves toward the observer (with an angle $\theta$ of $0$), one just replaces the sign of $v$ in the above equations