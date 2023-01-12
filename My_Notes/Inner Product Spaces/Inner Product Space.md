# The Inner Product Space
We want to extend the idea of a dot product for geometric vectors to a general vector space $V$.

>[!example] Defintion: Standard Inner Product
>Let $x=(x_1,x_2,\dots,x_n)$ and $y=(y_1,y_2,\dots,y_n)$ be vectors in $\mathbb{R}^n$. We define the **Standard Inner Product** in $\mathbb{R}^n$, denoted $\langle x,y\rangle$, by$$\langle x,y\rangle=x_1y_1+x_2y_2+\cdots+x_ny_n.$$The **norm** of $x$ is$$||x||=\sqrt{\langle x,x\rangle}=\sqrt{x_1^2+x_2^2+\cdots+x_n^2}$$
>Properties of the Inner Product:
>- We consider $\langle x,y \rangle$ to be a mapping $\mathbb{R}^n\rightarrow\mathbb{R}$ of two vectors
>- So, for all $x$,$y$, and $z$ in $\mathbb{R}^n$, and all real numbers $k$,
>	1. $\langle x,x\rangle\ge0$ and $\langle x,x\rangle=0$ only if $x=0$
>	2. $\langle x,y\rangle=\langle y,x\rangle$
>	3. $\langle kx,y\rangle=k\langle x,y\rangle$
>	4. $\langle x+y,z\rangle=\langle x,z\rangle+\langle y,z\rangle$

^c02554


>[!example] Definition: Inner product space
>Let $V$ be a (real or complex) vector space. A mapping that associates any pair of vectors $u$ and $v$ in $V$ with a real number is called te **inner product in $V$** provided it satisfies the following properties for any $\textbf{u}$,$\textbf{v}$, and $\textbf{w}$ in $V$, and all scalars $k$
>1. $\langle\textbf{v},\textbf{v}\rangle\ge0$. Furthermore, $\langle\textbf{v},\textbf{v}\rangle=0$ if and only if $\textbf{v}=0$
>2. $\langle\textbf{v},\textbf{u}\rangle=\overline{\langle\textbf{u},\textbf{v}\rangle}$
>3. $\langle k\textbf{u},\textbf{v}\rangle=k\langle\textbf{v},\textbf{v}\rangle$
>4. $\langle\textbf{u}+\textbf{v},\textbf{w}\rangle=\langle\textbf{u},\textbf{w}\rangle+\langle\textbf{v},\textbf{w}\rangle$
>
>The **norm** of $\textbf{v}$ in $V$ is defined as $$||\textbf{v}||=\sqrt{\langle\textbf{v},\textbf{v}\rangle}$$

^531b63


One of the fundamental inner products arises in the vector space $C^0[a,b]$ of all
real-valued functions that are continuous on the interval $[a,b]$. In this vector space, we
define the mapping $\langle f,g\rangle$ by$$\langle f,g\rangle=\int_{a}^{b}f(x)g(x)dx,$$for all $f$ and $g$ in $C^0[a,b]$. ^329856

>[!tip] Theorem: The Cauchy-Schwartz Inequality
>Let $\textbf{u}$ and $\textbf{v}$ be arbitrary vectors in the vector space $V$. Then$$|\langle\textbf{u},\textbf{v}\rangle|\le||\textbf{u}||\space||\textbf{v}||.$$
>**Proof:**
>Let $k$ be an arbitrary real number. For the vector $\textbf{u}+k\textbf{v}$, we have$$0\le||\textbf{u}+k\textbf{v}||^{2}=\langle\textbf{u}+k\textbf{v},\textbf{u}+k\textbf{v}\rangle$$But, using properties of the inner product,
>$$\begin{align*}
\langle\textbf{u}+k\textbf{v},\textbf{u}+k\textbf{v}\rangle &=\langle\textbf{u},\textbf{u}+k\textbf{v}\rangle+\langle k\textbf{v},\textbf{u}+k\textbf{v}\rangle\\
&=\langle\textbf{u}+k\textbf{v},\textbf{u}\rangle+\langle \textbf{u}+k\textbf{v},k\textbf{v}\rangle\\
&=\langle\textbf{u},\textbf{u}\rangle+\langle k\textbf{v},\textbf{u}\rangle+\langle\textbf{u},k\textbf{v}\rangle+\langle k\textbf{v},k\textbf{v}\rangle\\
&=\langle\textbf{u},\textbf{u}\rangle+2k\langle\textbf{v},\textbf{u}\rangle+k^{2}\langle\textbf{v},\textbf{v}\rangle\\
&=||\textbf{u}||^{2}+2k\langle\textbf{v},\textbf{u}\rangle+k^{2}||\textbf{v}||^2
\end{align*}$$
Consequently,$$||\textbf{v}||^{2}k^{2}+2\langle\textbf{u},\textbf{v}\rangle k+||\textbf{u}||^{2}\ge0$$
The Left hand side is a quadratic, which we will call $P(k)$, with a discriminant given by$$\Delta=4(\langle\textbf{u},\textbf{v}\rangle)^{2}-4||\textbf{u}||^{2}||\textbf{v}||^{2}$$If $\Delta>0$, then $P(k)$ would have two real roots and therefore have negative values, which would contradict the first statement. So we know that $\Delta\le0$ and$$4(\langle\textbf{u},\textbf{v}\rangle)^{2}-4||\textbf{u}||^{2}||\textbf{v}||^{2}\le0$$or equivalently,$$(\langle\textbf{u},\textbf{v}\rangle)^{2}\le||\textbf{u}||^{2}||\textbf{v}||^{2}$$
Hence,$$\langle\textbf{u},\textbf{v}\rangle\le||\textbf{u}||\space||\textbf{v}||$$