In this note, $u$ will always denote the **dependent variable**

### Linearity
We introduce the **Heat Operator** which is given by
$$L(u)=\frac{\partial u}{\partial t}-k\frac{\partial^{2}u}{\partial x^2}$$
This is a **linear** operator

### The Heat Equation
In this section the example of the [[The Heat Equation#^f7f168|the heat equation]] is used to demonstrate the technique of separation of variables.

Say we have a rod where the temperatures are zero at each end. This gives us our [[The Heat Equation#^acae29|boundary]] and [[The Heat Equation#^84b5c4|initial]] conditions:
$$u(0,t)=0$$ $$u(L,t)=0$$ $$u(x,0)=f(x)$$

Now, we assume solutions of a **separate** form:
$$u(x,t)=\phi(x)G(t)$$
Evaluating the derivatives then gives:
$$\frac{\partial u}{\partial t}=\phi(x)\frac{dG}{dt}$$
$$\frac{\partial^{2}u}{\partial x^2}=G(t)\frac{d^2\phi}{dx^2}$$
Plugging this into the heat equation gives us 
$$\phi(x)\frac{dG}{dt}-kG(t)\frac{d^2\phi}{dx^2}=0$$
And thus we can separate the variables, I'll denote derivatives with subscripts from now on for ease. 
$$\frac{G_t}{G}=k\frac{\phi_{xx}}{\phi}$$
When a relation of this occurs, a special property is introduced. Since each side of the equation depends on the different variable, their relation must be constant. When one variable is changed, the other must as well in order to preserve the equality relationship described above. This allows us to add one thing to the equation:
$$\frac{G_t}{kG}=\frac{\phi_{xx}}{\phi}=-\lambda$$
And finally, we have separated this equation into two ODEs that are easily solvable. 
$$G_{t}=-\lambda kG\quad\text{ and }\quad\phi_{xx}=-\lambda\phi$$
These general solution of the first is of the form:
$$G(t)=ce^{-\lambda kt}$$
The second one requires a bit more action and knowledge of eigenvalues and eigenfunctions. The special values of $\lambda$ where there are nontrivial solutions for $\phi$ are called eigenvalues. The solutions are then eigenfunctions. ^3661da

Let's take a look at the second order ODE. We have a linear, constant coefficient, homogeneous differential equation. The solutions of which are in the form
$$\phi=e^{rx}$$
This now depends on the value of $\lambda$. The key to proving whether values of $\lambda$ are eigenvalues is based on the [[The Heat Equation#^acae29|boundary conditions]]:
$$u(0,t)=0$$ $$u(L,t)=0$$
Which for this equation, in order to have a nontrivial $u$, correspond to$$\phi(0)=0$$$$\phi(L)=0$$
$r$ in the above general solution corresponds to the solutions to the characteristic polynomial, which is
$$r^2=-\lambda$$
There are four cases for what $\lambda$ could be, which will help us find the eigenvalues. ^2d21c9
1. $\lambda>0$ in which $r=\pm i\sqrt{\lambda}$
2. $\lambda=0$ in which $r=0$
3. $\lambda<0$ in which $r=\pm\sqrt{-\lambda}$
4. $\lambda$ is complex (which we won't consider as of now)

First, let us consider case 1, in which $\lambda>0$.
Then our solutions to the characteristic polynomial are given as $r=\pm i\sqrt{\lambda}$, meaning our general solution to the differential equation is then$$\phi=ce^{\pm i\sqrt{\lambda}x}$$
Remembering [[Complex Exponentials#^8e81f7|euler's formula]], this can be expanded to sines and cosines,
$$\phi=c_1\cos{\sqrt{\lambda}x}+c_2\sin{\sqrt{\lambda}x}$$
We then apply the boundary condition that $\phi(0)=0$, giving us
$$c_1=0\quad\quad\text{meaning}\quad\quad\phi=c_2\sin{\sqrt{\lambda}x}$$
Then the second boundary condition is applied, giving
$$c_2\sin{\sqrt{\lambda}L}=0$$
We solve for lambda in order to have a nontrivial solution (trivial would be if we set $c_2$ to zero):
$$\sqrt{\lambda}L=n\pi\quad\quad n=0,1,2,\dots$$
$$\lambda=\Big(\frac{n\pi}{L}\Big)^2$$
Then the eigenfunctions corresponding to these eigenvalues are then
$$\phi=c_2\sin{\frac{n\pi x}{L}}$$where $c_2$ is an arbitrary constant. The constant will not matter in the general solution since it will be multiplied by the general solution to $G$, which already contains a constant.

Next we consider the case where $\lambda=0$, where $r=0$. Then
$$\phi=c_1+c_2x$$
Applying the boundary conditions forces us to set $c_1$ and $c_2$ to zero, meaning no $\lambda$ will give a nontrivial solution.

Finally we consider the case where $\lambda<0$ where $r=\pm\sqrt{-\lambda}$, the general solution is given by
$$\phi=c_1e^{\sqrt{-\lambda}x}+c_2e^{\sqrt{-\lambda}x}=c_3\cosh{\sqrt{-\lambda}x}+c_4\sinh{\sqrt{-\lambda}x}$$
The boundary conditions go as follows:
When $\phi(0)=0$,
$$c_1\cosh{\sqrt{-\lambda}}=0$$
Which means $c_1$ must be zero since hyperbolic cosine is never zero.
Then when $\phi(L)=0$
$$c_2\sinh{\sqrt{-\lambda}}=0$$
Since the square root in the sine is the one that is positive, $c_2$ must be zero since hyperbolic sine is never zero after $x$ is greater than zero.
Since both the constants are zero, the solution is trivial and thus there are no eigenvalues less than zero.

Thus all the eigenvalues are greater than zero, and 
$$\phi(x)=\sin{\frac{n\pi x}{L}}\quad\quad n=1,2,3,\dots$$

We can now substitute our $\lambda$ int the solution for $G$ and multiply.
$$u(x,t)=B\sin{\frac{n\pi x}{L}}e^{k(n\pi/L)^2t}$$Where $n$ can be any [[Sets#^d3aac2|natural number]]

By the principle of superposition, we can add up all the solution for each $n$, so the true general solution becomes an infinite sum (or series).
$$u(x,t)=\sum\limits_{n=1}^{\infty}B_{n}\sin{\frac{n\pi x}{L}}e^{-k(n\pi/L)^2t}$$