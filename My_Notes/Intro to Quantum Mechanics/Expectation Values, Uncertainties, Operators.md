# Expectation Values, Uncertainties, and Operators
>[!example] Expectation Values
>The probability per unit length is $|\psi(x)|^2$, so we could write that the probability of being found in the interval $dx$ around $x$ is $$P(dx)=|\psi(x)|^2dx$$
>The **Expectation Value** is found by multiplying the probability of a certain $x$ by $x$ and then integrating, or$$\overline{x}\equiv\int\limits_{\text{all space}}x|\psi(x)|^2dx$$
>Note that the expectation value is slightly different than saying "average position", because it does not imply the particle has a position
>By the same logic, the expectation value of the square of the position is$$\overline{x^2}\equiv\int\limits_{\text{all space}}x^2|\psi(x)|^2dx$$
>The General Form of calculating an observable $Q$ is$$\overline{Q}=\int\limits_{\text{all space}}\Psi^{*}(x,t)\hat{Q}\Psi(x,t)dx$$
>The location of $\hat{Q}$ is important, since it denotes the **operator** associated with $Q$

>[!example] Uncertainty
>In quantum mechanics, we define uncertainty as the standard deviation of the observable we wish to measure. In the case of position $x$,$$\Delta x=\sqrt{\int\limits_{\text{all space}}(x-\overline{x})^2|\psi(x)|^2dx}$$
>Where $\overline{x}$ is the expectation value.
>One may remember this as the [[The Uncertainty Principle#^a97947|root-mean-squared deviation]].
>We can rewrite the above deviation as$$\Delta x=\sqrt{\int\limits_{\text{all space}}(x^2-2x\overline{x}+\overline{x}^2)|\psi(x)|^{2dx}}=\sqrt{\int x^2|\psi(x)|^2dx-2\overline{x}\int x|\psi(x)|^2dx+\overline{x^2}\int|\psi(x)|^2dx}$$
>Notice that the first integral is the expectation value of $x^2$, and the second is the expectation value of $x$, and the third is simply the normalization and therefore $1$.
>Thus,$$\Delta x=\sqrt{\overline{x^2}-\overline{x}^2}$$
>Generalized uncertainty:$$\Delta Q=\sqrt{\overline{Q^2}-\overline{Q}^2}$$

>[!list] Basic Operators
>**Momentum**$$\hat{p}=-i\hbar\frac{\partial}{\partial x}$$
>**Position**$$\hat{x}=x$$
>**Energy**$$\hat{E}=i\hbar\frac{\partial}{\partial t}$$