## Shortest Path between Two Points
Given two points in a plane, what is the shortest path between them? 

Consider two points, $(x_1,y_1)$ and $(x_2,y_2)$, and a path $y=y(x)$ joining them. Our task is to minimize $y(x)$.
The length of a short segment of the path is $ds=\sqrt{dx^2+dy^2}$ which is $$ds=\sqrt{1+y'(x)^2}$$Therefore, the total length of the path between $1$ and $2$ is$$L=\int_{1}^{2}ds=\int_{x_1}^{x_2}\sqrt{1+y'(x)^2}dx$$Our job is to minimize this quantity, by variating the unknown $y(x)$. We can do this by solving the [[Euler-Lagrange Equations#^ce4f09|Euler-Lagrange Equation]], with our $f(y,y',x)=(1+y'^2)^{1/2}$
The first partial derivative:
$$\frac{\partial f}{\partial y}=0$$
The second partial derivative:
$$\frac{\partial f}{\partial y'}=\frac{y'}{(1+y'^2)^{1/2}}$$
Since $\partial f/\partial y$ is zero, in order to satisfy the euler-lagrange equation the second term must also be zero. Thus
$$\frac{d}{dx}\bigg(\frac{\partial f}{\partial y'}\bigg)=0$$
Therefore $\partial f /\partial y'$ is a constant.
$$y'^2=C^2(1+y'^2)$$
Rearranging this gives that $y'$ is constant, thus we have the equation for a straight line. This is consistent with the observation that a straight line is the shortest path between two points in a plane.

## The Brachistochrone
Given two points 1 and 2, with 1 higher above the ground than 2, in what shape should we build a frictionless roller coaster track so that a cart released from point 1 will reach point 2 in the shortest possible time?
The time to travel from one to two is 
$$\text{time}(1\rightarrow2)=\int_{1}^{2}\frac{ds}{v}$$
The speed at any height $y$ is determined by conservation of energy to be $v=\sqrt{2gy}$. We conveniently choose $y$ as out independent variable. Our unknown path is $x=x(y)$
Thus our $ds$ is given as 
$$ds=\sqrt{x'(y)^2+1}\space dy$$
Then our [[Introduction to Variational Calculus#^2a28a5|functional]] becomes 
$$\text{time}(1\rightarrow2)=\frac{1}{\sqrt{2g}}\int_{0}^{y_2}\frac{\sqrt{x'(y)^2+1}}{\sqrt{y}}dy$$
We then define the [[Euler-Lagrange Equations#^ce4f09|eulere-lagrange equation]]:
$$\frac{\partial f}{\partial x}=\frac{d}{dy}\frac{\partial f}{\partial x'}$$
Then
$$0=\frac{d}{dy}\bigg(\frac{x'^2}{y(1+x'^2)}\bigg)$$
Thus the term on the right is a constant, which we will define to be $1/2a$ for convenience. Therefore we have$$x'=\sqrt{\frac{y}{2a-y}}$$
This is a solvable equation by integration:
$$x=\int\sqrt{\frac{y}{2a-y}}$$
>[!defintion] Solving this integral
>We make a substitution $y=a(1-\cos{\theta})$, making the integral
>$$x=a\int(1-\cos{\theta})d\theta$$
>$$\space\space=a(\theta-\sin{\theta})+C$$
>This gives us parametric equations in terms of $\theta$,
>$$x=a(\theta-\sin{\theta})\quad\text{and}\quad y=a(1-\cos{\theta})$$
>The constant $a$ can be chosen to fit the conditions of the first (or second) point.

The solution is a pair of parametric equations that describes a cycloid.