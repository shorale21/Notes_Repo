# Orthogonal Sets of Vectors

>[!example] Definition: Orthogonal Vectors
>Two vectors $\textbf{u}$ and $\textbf{v}$ in an [[Inner Product Space#^531b63|inner product space]] $V$ are said to be **orthogonal** if $\langle\textbf{u},\textbf{v}\rangle=0$

^e50394

>[!example] Definition: Orthogonal Set
>A [[Sets#^cfbc64|set]] of nonzero vectors $\{\textbf{v}_1,\textbf{v}_2,\dots,\textbf{v}_k\}$ in an [[Inner Product Space#^531b63|inner product space]] $V$ is called an **orthogonal set** of vectors if$$\langle\textbf{v}_i,\textbf{v}_j\rangle=0\quad\quad\text{whenever }i\neq j$$

^5d518e

>[!example] Defintion: Unit Vector
>A vector $\textbf{v}$ is called a unit vector if $$||v||=1$$

>[!example] Definition: Orthonormal Set
>An orthogonal [[Sets#^cfbc64|set]] of unit vectors is called an **orthonormal set** of vectors
>1. $\langle\textbf{v}_i,\textbf{v}_j\rangle=0\quad\text{whenever }i\neq j$
>2. $\langle\textbf{v}_i,\textbf{v}_i\rangle=1\quad\text{for all }i=1,2,\dots,k$

^5b5063

>[!example] Definition: Orthogonal and Orthonormal Bases
>A basis $\{\textbf{v}_1,\textbf{v}_2,\dots,\textbf{v}_k\}$ for a finite dimensional inner product space is called an **orthogonal basis** if $$\langle\textbf{v}_i,\textbf{v}_j\rangle=0\quad\text{whenever }i\neq j$$
>and it is called an **orthonormal basis** if$$\langle\textbf{v}_i,\textbf{v}_j\rangle=\delta_{ij},\quad i,j=1,2,\dots,k$$
>**Independence Theorem**:
>If $\{\textbf{v}_1,\textbf{v}_2,\dots,\textbf{v}_k\}$ is an orthogonal set of nonzero vectors in an [[Inner Product Space#^531b63|inner product space]] $V$, then $\{\textbf{v}_1,\textbf{v}_2,\dots,\textbf{v}_k\}$ is linearly independent
>
>**Linear Combination Theorem:**
>Let $V$ be a finite dimensional inner product space with orthogonal basis $\{\textbf{v}_1,\textbf{v}_2,\dots,\textbf{v}_n\}$. Then any vector $\textbf{v}$ in $V$ may be expressed in terms of the basis as$$\textbf{v}=\left(\frac{\langle\textbf{v},\textbf{v}_{1}\rangle}{||\textbf{v}_{1}||^{2}}\right)\textbf{v}_{1}+\left(\frac{\langle\textbf{v},\textbf{v}_{2}\rangle}{||\textbf{v}_{2}||^{2}}\right)\textbf{v}_{2}+\cdots+\left(\frac{\langle\textbf{v},\textbf{v}_{n}\rangle}{||\textbf{v}_{n}||^{2}}\right)\textbf{v}_{n}$$If the basis is orthonormal, then this is simpler:$$\textbf{v}=\langle\textbf{v},\textbf{v}_{1}\rangle\textbf{v}_1+\langle\textbf{v},\textbf{v}_{2}\rangle\textbf{v}_2+\cdots+\langle\textbf{v},\textbf{v}_{n}\rangle\textbf{v}_n$$

^800dc8
