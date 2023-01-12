# Convergence Properties of Fourier Series
Recall our definition of a [[Intro To the Fourier Series#^0cc02e|Fourier series]] for a periodic function $f(x)$, and the [[Intro To the Fourier Series#^965f8d|convergence theorem]] for such functions.

In our analysis we consider the error of the fourier series, as given in the [[Error Bounds#^f8ec4b|general error equation]]$$E_N(x)=f(x)-S_N(x)=\sum\limits_{n=N+1}^{\infty}\left\{a_n\cos\left(\frac{n\pi x}{L}\right)+b_n\sin\left(\frac{n\pi x}{L}\right)\right\}$$Notice that the Fourier series will converge pointwise to $f(x)$ if and only if$$\lim_{N\rightarrow\infty}[E_N(x)]=0\quad\text{at all values of }x$$We can represent this by saying that it will converge uniformly if and only if$$|E_N(x)|\le\epsilon_N\quad\text{and}\quad\lim_{N\rightarrow\infty}[\epsilon_N]=0$$Interestingly enough, both functions inside the fourier series are trigonometric functions, meaning they are less than or equal to one for all $x$. Therefore we can create the inequality$$|E_N(x)|\le\sum\limits_{n=N+1}^{\infty}\{|a_n|+|b_n|\}$$

>[!example] Theorem: Convergence of Fourier Series
>The [[Intro To the Fourier Series#^0cc02e|Fourier series]] for $f(x)$ converges uniformly, and therefore $f(x)$ is continuous if$$\sum\limits_{n=1}^{\infty}\{|a_n|+|b_n|\}\quad\text{converges.}$$
>The Fourier series for $f(x)$ converges in the mean-square sense if$$\sum\limits_{n=1}^{\infty}\{a^2_n+b^2_n\}\quad\text{converges}$$
>Here is a list of convergence types from most stringent to least stringent:$$\textit{Uniform Convergence}\implies\textit{Pointwise Convergence}\implies\textit{Mean-Square Convergence}$$
>Notice the more stringent convergence types imply the less stringent ones
>- If a Fourier series converges uniformly, then it converges to a continuous function
>- If a Fourier series converges, but not uniformly, it will converge to a discontinuous function
>- A series that converges in mean-square does not need to converge to $f(x)$, but only some "close" function