The Calculus of Variations involves finding the minimum or maximum of a quantity, usually expressable as an integral.

## Functionals
>[!example] Definition: Functional
>A **Functional** $\mathcal{F}$ is a function that maps a function to a scalar, as opposed to an ordinary function mapping a scalar to a scalar.
>$$\mathcal{F}:f\rightarrow\mathbb{R}$$
>A functional takes a function and maps it to one and only one scalar. It *only* changes depending on the input function, not the scalar input to said function

^2a28a5

Functionals are a tricky subject, since functions of functions are usually still scalar. For example, parametric equations where $y$ is a function of $t$ and $x$ is a function of $t$, then $y(x)$ can still be a function of $t$, but both input and output are scalar.

For a functional, the scalar is fixed and the function is varied, for example, take $\mathcal{F}(x(t))=x^{2}(t=t_0)$. Notice that the $t$ is fixed, and so the functional only changes depending on the function itself. Each function is mapped to one and only one scalar in this sense.
>[!example] Definition: Integral Functional
>The most common and most important [[Introduction to Variational Calculus#^2a28a5|functional]] is the integral functional given as:
>$$\mathcal{F}(x(t))=\int_{t_1}^{t_2}f(x,\dot{x},t)dt$$

^b078e9