# Series Solutions around a Regular Singular Point
>[!example] Defintion: Regular Singular Point
>The point $x=x_0$ is called a **regular singular point** of the differential equation$$y''+P(x)y'+Q(x)y=0$$if and only if the following two conditions are satisfied:
>1. $x_0$ is a [[Series Solutions around an Ordinary Point#^3dcc3a|singular point]] of the equation
>2. Both of the functions$$p(x)=(x-x_0)P(x)\quad\text{and}\quad q(x)=(x-x_0)^2Q(x)$$are analytic at $x=x_0$
>
>A singular point that does not satisfy the second requirement is called an **irregular singular point**.
>Example: The standard differential equation for with a regular singular point at $x=0$$$x^2y''+xp(x)y'+q(x)y=0$$
>- The simplest equation of this form is$$x^2y''+p_0xy'+q_0y=0$$where $p_0$ and $q_0$ are constants, which is called the **Cauchy-Euler Equation**

^8ff73a

>[!defintion] Theorem using Frobenius Series
>First, let us define the Frobenius series as$$y(x)=x^{r}\sum\limits_{n=0}^{\infty}a_{n}x^{n}$$where $r$ is a root of the **indicial equation** $r(r-1)+p_0r+q_0=0$
>
>**Theorem:**
>Consider the differential equation $$x^{2}y''+xp(x)y'+q(x)y=0,\quad x>0$$where $p$ and $q$ are analytic at $x=0$. Suppose that$$p(x)=\sum\limits_{n=0}^{\infty}p_{n}x^{n},\quad\space q(x)=\sum\limits_{n=0}^{\infty}q_{n}x^{n},$$for $|x|<R$. Let $r_1$ and $r_2$ denote the roots of the indicial equation$$r(r-1)+p_0r+q_0=0$$and assume $r_{1}\ge r_{2}$ if these roots are real. Then the differential equation has a solution of the form$$y_1(x)=x^{r_1}\sum\limits_{n=0}^{\infty}a_{n}x^{n},\quad a_{0}\neq0$$Further, provided $r_1$ and $r_2$ are distinct, and do not differ by an integer, then there is a second solution, of the form$$y_1(x)=x^{r_2}\sum\limits_{n=0}^{\infty}b_{n}x^{n},\quad b_{0}\neq0$$

^6c0c37
