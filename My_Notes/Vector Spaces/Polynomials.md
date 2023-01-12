## Uniqueness of Coefficients
>[!example] Theorem: Zero Function
>Suppose $a_0,\dots,a_m\in\mathbb{F}$ are coefficients to a [[Span and Linear Independence#^8dcd73|polynomial]]. If
>$$a_0+a_1z+\cdots+a_mz^m=0$$
>for every $z\in\mathbb{F}$, then $a_0=\cdots=a_m=0$

^8a6e74

## Division Algorithm
>[!example] Definition: Division Algorithm
>Suppose that $p,s\in\mathcal{P}(\mathbb{F})$, with $s\neq0$. Then there exist uniqe polynomials $q,r\in\mathcal{P}(\mathbb{F})$ such that
>$$p=sq+r$$
>and $\text{deg }r<\text{deg }s$

## Zeros of Polynomials
>[!example] Definition: Zero of a Polynomial
>A number $\lambda\in\mathbb{F}$ is called *zero* of a [[Span and Linear Independence#^8dcd73|polynomial]] $p\in\mathcal{P}(\mathbb{F})$ if
>$$p(\lambda)=0$$

^a95526

>[!example] Definition: Factor
>A [[Span and Linear Independence#^8dcd73|polynomial]] $s\in\mathcal{P}(\mathbb{F})$ is called *factor* of $p\in\mathcal{P}(\mathbb{F})$ if there exists a polynomial $q\in\mathcal{P}(\mathbb{F})$ such that $p=sq$

>[!example] Theorem: Corresponding Zero
>Suppose $p\in\mathcal{P}(\mathbb{F})$ and $\lambda\in\mathbb{F}$. Then $p(\lambda)=0$ if and only if there is a polynomial $q\in\mathcal{P}(\mathbb{F})$ such that
>$$p(z)=(z-\lambda)q(z)$$
>for every $z\in\mathbb{F}$

>[!example] Theorem: Number of Zeroes
>Suppose $p\in\mathcal{P}(\mathbb{F})$ is a [[Span and Linear Independence#^8dcd73|polynomial]] with degree $m\ge0$. Then $p$ has at most $m$ [[Polynomials#^a95526|zeroes]] in $\mathbb{F}$

## Factorization of Polynomials over $\mathbb{C}$
>[!example] The Fundamental Theorem of Algebra
>Every nonconstant [[Span and Linear Independence#^8dcd73|polynomial]] with complex coefficients has a zero.

>[!example] Factorization of a polynomials
>If $p\in\mathcal{P}(\mathbb{F})$ is a nonconstant [[Span and Linear Independence#^8dcd73|polynomial]], then $p$ has a unique factorization in the form 
>$$c(z-\lambda_1)\cdots(z-\lambda_m)$$
>Where $c,\lambda_1,\dots,\lambda_m\in\mathbb{C}$

>[!example] Theorem: Zeroes of Real Polynomials
>Suppose $p\in\mathcal{P}(\mathbb{C})$ is a [[Span and Linear Independence#^8dcd73|polynomial]] with real coefficients. If $\lambda\in\mathbb{C}$ is a [[Polynomials#^a95526|zero]] of $p$, then so is $\bar{\lambda}$

>[!example] Theorem: Quadratic Factorization
>Suppose $b,c\in\mathbb{R}$. Then there is a polynomial factorization of the form
>$$x^2+bx+c=(x-\lambda_1)(x-\lambda_2)$$
>with $\lambda_1,\lambda_2\in\mathbb{R}$ if and only if $b^2\ge4c$