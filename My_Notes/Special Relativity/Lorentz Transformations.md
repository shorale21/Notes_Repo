# The Lorentz Transformations

^4d085e

<u>**Variables**</u> ^c960c4
- Let there be two reference frames, $S$ and $S'$
- $S'$ moves at a velocity $v$ in the postitive-$x$ direction relative to $S$
- $S$ moves at a velocity $v$ in the negative-$x$ direction relative to $S'$
- The symbol $u$ will denote the velocity of an object moving relative to one of the frames
- Quantities such as velocity, position, and time will be denoted as $u$, $x$, and $t$ in $S$ and $u'$, $x'$ and $t'$ in $S'$
- The instant at which the origins pass (the frames are the same) is denoted as $t=0$

>[!example] Definition: The Gamma Factor
>Let $\gamma_v$ denote the gamma factor.$$\gamma_v=\frac{1}{\sqrt{1-\frac{v^2}{c^2}}}\ge1$$
>Notice that $\gamma_v=1$ when $v=0$ and has $v$ approaches the speed of light $\gamma_v$ approaches infinity

^eeedf7

>[!example] The Lorentz Transformation Equations
>For $S$ to $S'$: $$x'=\gamma_v(x-vt)\quad\quad\quad t'=\gamma_v\left(-\frac{v}{c^2}x+t\right)$$
>For $S'$ to $S$: $$x=\gamma_v(x'+vt')\quad\quad\quad t=\gamma_v\left(\frac{v}{c^2}x'+t'\right)$$
>Note that for speeds $v\ll c$, $\gamma_v\approx1$, so special relativity laws can essentially be ignored

>[!info]- Derivation of the Lorentz Transform
>- Consider a free object (net force is zero). This object moves at constant velocity in all [[Intro to Special Relativity#^054abc|inertial frames]]
>- Therefore in both frames:$$x=ut\space\text{and}\space x'=u't'$$
>- We seek a function to essentially transform an $x$ and $t$ in $S$ to an $x'$ and $t'$ in $S'$
>	- It turns out that this is a **linear transformation**
>$$x'=Ax+Bt\quad\quad\quad t' = Cx+Dt$$
>- We now consider three special cases of motion:
>	- Case 1: Object fixed at the origin of frame $S'$
>		- In frame $S$, this would move with a speed $v$ in the positive-$x$ direction
>		- We then have $x' = 0$ and $x=vt$
>		- We then obtain $$B=-Av$$
>	- Case 2: Object fixed at the origin of frame $S$
>		- In frame $S'$ this woulfd move with a speed $v$ in the negative-$x$ direction
>		- We then have $x'=-vt'$ and $x=0$
>		- We then obtain $$D=-\frac{B}{v}\quad\text{or}\quad D=A$$
>	- Case 3: The object is a beam of light
>		- The speed will be $c$ in each frame
>		- This means $x'=ct'$ and $x=ct$
>		- We then obtain $$C=-\frac{v}{c^2}A$$
>	- Substituting all of these back into the original equations, we get$$x'=A(x-vt)\quad\quad\text{and}\quad\quad t'=A\left(-\frac{v}{c^2}x+t\right)$$
>	- Now we need to find $A$
>	- The first step is to solve the equations for $x$ and $t$ $$x=\frac{1}{A\left(1-\frac{v^2}{c^{2}}\right)}(x'+vt')\quad\quad\quad t=\frac{1}{A\left(1-\frac{v^2}{c^{2}}\right)}\left(\frac{v^2}{c^2}x'+t'\right)$$
>	- Since the only difference between the frames is $v$, the previous sets of equations must be identical except for the sign of $v$
>	- This gives $$\frac{1}{A\left(1-\frac{v^{2}}{c^{2}}\right)}=A\space\implies\space A=\frac{1}{\sqrt{1-\frac{v^2}{c^2}}}$$
>	- We call this value the **gamma factor** denoted by $\gamma_v$