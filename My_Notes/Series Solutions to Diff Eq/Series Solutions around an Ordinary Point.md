# Series Solutions around an Ordinary Point
Consider the second-order linear homogenous differential equation:$$y''+p(x)y'+q(x)y=0$$

>[!example] Definition: Ordinary Point
>The point $x=x_0$ is called an **ordinary point** of the differential equation $$y''+p(x)y'+q(x)y=0$$
>if $p$ and $q$ are *both* analytic at $x=x_0$. Any point that is not an ordinary point is called a **singular point** of the differential equation


>[!info] Power series Theorem
>Let $p$ and $q$ be analytic at $x=x_0$, and suppose that their power series expansions are valid for $|x-x_0|<R$. The the general solution to the differential equation$$y''+p(x)y'+q(x)y=0$$
>can be represented as a power series centered at $x_0$ with a radius of converges of at least $R$. The coefficients of the series solution can be determined in terms of $a_0$ and $a_1$ by directly substituting $$y(x)=\sum_{n=0}^{\infty} a_n(x-x_0)^n$$ into the differential equation.
>The resulting solution is of the form:$$y(x)=a_0y_1(x)+a_1y_2(x)$$ Where $y_1$ and $y_2$ are linearly independent solutions on the interval of existence.