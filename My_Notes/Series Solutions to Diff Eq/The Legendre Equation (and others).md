# The Legendre Equation
Several differential equations arise in applied mathematics that require series to evaluate.
>[!example] Special Differential Equations
>**The Legendre Equation**$$(1-x^2)y''-2xy'+\alpha(\alpha+1)y=0$$
>**The Hermite Equation**$$y''-2xy+2\alpha y=0$$
>**The Chebysev Equation**$$(1-x^2)y''-xy'+\alpha^2y=0$$
>- $\alpha$ is an arbitrary constant


One case of particular importance is the legendre equation of the form$$(1-x^2)y''-2xy'+N(N+1)y=0$$
Where $N$ is a non-negative [[Sets#^d3aac2|integer]]. In this case, the [[Series Solutions around an Ordinary Point#^f5cc1e|recurrence relation]] is$$a_{n+2}=\frac{n(n+1)-N(N+1)}{(n+1)(n+2)}a_n\text{,}\quad n=0,1,2,\dots$$
This implies that $a_{N+2}=a_{N+4}=\cdots=0$
Therefore, the solution must be a polynomial of degree $N$

>[!example] Definition: The Legendre Equation
>Let $N$ be a nonnegative integer. The **Legendre polynomial of degree $N$**, denoted by $P_N(x)$, is defined to be the polynomial solution to$$(1-x^2)y''-2xy'+N(N+1)y=0$$
>Which has been normalized so that $P_N(1)=1$

>[!important]- Solving the Legendre Polynomial
>Take the differential equation $$(1-x^2)y''-2xy'+\alpha(\alpha+1)y=0$$
>Divide both sides by $(1-x^2)$ to isolate the second derivative$$y''-\frac{2x}{1-x^2}y'+\frac{\alpha(\alpha+1)}{1-x^2}y=0$$
>- Notice the radius of covergence is $1$
>
>Now substitute $y(x)=\sum\limits_{n=0}^{\infty}a_nx^n$ into the original equation$$\sum\limits_{n=2}^{\infty}n(n-1)a_nx^{n-2}-\sum\limits_{n=2}^{\infty}n(n-1)a_nx^n-2\sum\limits_{n=1}^{\infty}na_nx^n+\sum\limits_{n=0}^{\infty}\alpha(\alpha+1)a_nx^n=0$$
>Redefining their summations gives:$$\sum\limits_{n=0}^{\infty}\left[(n+2)(n+1)a_{n+2}-n(n-1)a_n-2na_n+\alpha(\alpha+1)a_n\right]x^n=0$$
>Thus, we obtain the [[Series Solutions around an Ordinary Point#^f5cc1e|recurrence relation]] of:$$a_{n+2}=\frac{n(n+1)-\alpha(\alpha+1)}{(n+1)(n+2)}a_n$$
>Which can be rewritten as:$$a_{n+2}=-\frac{(\alpha-n)(\alpha+n+1)}{(n+1)(n+2)}a_n$$
>**Even Values of $n$:**
>$$\begin{align*}
n=0&\implies a_2=-\frac{\alpha(\alpha+1)}{2}a_0\\
n=2&\implies a_4=-\frac{(\alpha-2)(\alpha+3)}{3\cdot4}a_2=\frac{(\alpha-2)\alpha(\alpha+1)(\alpha+3)}{4!}a_0\\
n=4&\implies a_6=-\frac{(\alpha-4)(\alpha+5)}{5\cdot6}a_4=-\frac{(\alpha-4)(\alpha-2)\alpha(\alpha+1)(\alpha+3)(\alpha+5)}{6!}a_0
\end{align*}$$
>In general, for $k=1,2,3\dots$, we have$$a_{2k}=(-1)^{k}\frac{(\alpha-2k+2)(\alpha-2k+4)\cdots(\alpha-2)\alpha(\alpha+1)\cdots(\alpha+2k-1)}{(2k)!}a_0$$
>**Odd Values of $n$:**
>$$\begin{align*}
n=1&\implies a_3=-\frac{(\alpha-1)(\alpha+2)}{2\cdot3}a_1\\
n=3&\implies a_5=-\frac{(\alpha-3)(\alpha+4)}{4\cdot5}a_3=\frac{(\alpha-3)(\alpha-1)(\alpha+2)(\alpha+4)}{5!}a_1\\
n=5&\implies a_7=-\frac{(\alpha-5)(\alpha+6)}{6\cdot7}a_5=-\frac{(\alpha-5)(\alpha-3)(\alpha-1)(\alpha+2)(\alpha+4)(\alpha+6)}{7!}a_1
\end{align*}$$
>In general, for $k=1,2,3\dots$, we have$$a_{2k}=(-1)^{k}\frac{(\alpha-2k+1)\cdots(\alpha-3)(\alpha-1)(\alpha+2)(\alpha+4)\cdots(\alpha+2k)}{(2k+1)!}a_1$$
>Consequently, for $a_0\neq0$ and $a_1\neq0$, we have two linearly independent solutions:
>$$\begin{align*}
y_{1}(x)&=a_0\left[1-\frac{\alpha(\alpha+1)}{2}x^{2}+\frac{(\alpha-2)\alpha(\alpha+1)(\alpha+3)}{4!}x^{4}-\frac{(\alpha-4)(\alpha-2)\alpha(\alpha+1)(\alpha+3)(\alpha+5)}{6!}x^{6}+\cdots\right]\\\\
y_2(x)&=a_1\left[x-\frac{(\alpha-1)(\alpha+2)}{2\cdot3}\right]
\end{align*}$$

>[!example] Legendre Polynomial Derivation
>We want to find $P_N(x)$ for different values of $N$
>**Rodrigues' Formula:**$$P_N(x)=\frac{1}{2^{N}N!}\frac{d^N}{dx^N}(x^2-1)^N\quad N=0,1,2\dots$$
>**Recurrence Relation:**$$P_{N+1}(x)=\frac{(2N+1)xP_{N}(x)-NP_{N-1}(x)}{N+1}\quad N=1,2,3\dots$$
>$$\quad$$
>$$\begin{array}{l l} 
 \hline
 N &&& \textbf{Legendre Polynomial of Degree}\space N \\
 \hline
 0 &&& P_0(x)=1 \\ 
 1 &&& P_1(x)=x  \\
 2 &&& P_2(x)=\frac{1}{2}(3x^2-1) \\
 3 &&& P_3(x)=\frac{1}{2}x(5x^2-3)  \\
 4 &&& P_4(x)=\frac{1}{8}(35x^4-30x^2+3) \\  
 \hline
\end{array}$$

>[!example] Orthogonality of the Legendre Polynomial
>We defined an [[Inner Product Space#^329856|inner product on the vector space]] $C^0[a,b]$ by$$\langle f,g\rangle=\int_{a}^{b}f(x)g(x)dx$$ for all $f$ and $g$ in $C^0[a,b]$.
>**Orthogonality Theorem:**
>The set of Legendre Polynomials $\{P_0,P_1,P_2,\dots\}$ is an [[Orthogonal Sets of Vectors#^5d518e|orthogonal set]] of functions on the interval $[-1,1]$. That is,$$\int_{-1}^{1}P_{M}(x)P_{N}(x)dx=0\quad\text{whenever }M\neq N$$
>>[!info]- Proof of the Orthogonality Theorem
>>Using the product rule for differentiation, we can see Legendre's Equation$$(1-x^{2})y''-2xy'+\alpha(\alpha+1)y=0$$can be written as $$[(1-x^2)y']'+\alpha(\alpha+1)y=0$$
>>The Legendre Polynomials $P_N$ and $P_M$ must satisfy$$[(1-x^2)P_N'(x)]'+N(N+1)P_N(x)=0$$$$[(1-x^2)P_M'(x)]'+M(M+1)P_M(x)=0$$
>>Now, we multiply the first equation by $P_M$ and the second equation by $P_N$ and subtract:$$\left[(1-x^2)P_N'(x)\right]'P_{M}-\left[(1-x^2)P_M'(x)\right]'P_{N}+\left[N(N+1)-M(M+1)\right]P_NP_M=0$$
>>Which can be written as$$\Big\{\big[(1-x^2)P'_NP_M\big]'-(1-x^2)P'_NP'_M\Big\}-\Big\{\big[(1-x^2)P'_MP_N\big]'-(1-x^2)P'_NP'_M\Big\}+\Big[N(N+1)-M(M+1)\Big]P_MP_N=0$$
>>This can be further rewritten as$$\Big[(1-x^2)(P'_NP_M-P'_MP_N)\Big]'-\Big[N(N+1)-M(M+1)\Big]P_MP_N=0$$
>>When we integrate both sides:$$\Big[(1-x^2)(P'_NP_M-P'_MP_N)\Big]_{-1}^{1}-\Big[N(N+1)-M(M+1)\Big]\int_{-1}^{1}P_{N}(x)P_{M}(x)dx=0$$
>>The first term on the left vanishes at $x=\pm 1$, and the coefficient to the integral can be factored:$$(N-M)(N+M+1)\int_{-1}^{1}P_{N}(x)P_{M}(x)dx=0$$
>>And so, if $N\neq M$, then the coefficient will not be $0$, so the integral must be $0$, and therefore$$\int_{-1}^{1}P_{M}(x)P_{N}(x)dx=0\quad\text{whenever }N\neq M$$


>[!example] Coefficient Theorem
>Let $f$ and $f'$ be continuous on the interval $(-1,1)$. Then, for $-1<x<1$,$$f(x)=a_0P_0(x)+a_1P_1(x)+\cdots=\sum\limits_{n=0}^{\infty}a_nP_n(x)$$where$$a_n=\frac{2n+1}{2}\int_{-1}^{1}f(x)P_n(x)dx$$