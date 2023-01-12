>[!example] Definition: Inner Product
>An *inner product* on $V$ is a function that takes each ordered pair $(u,v)$ of elements of $V$ and maps to a number in $\mathbb{F}$. It is denoted by $\langle u,b\rangle$, and satisfies the following properties:
>1. **Positivity**
>	1. $\langle v,v \rangle\ge0$ for all $v\in V$
>2. **definiteness**
>	1. $\langle v,v\rangle=0$ if and only if $v=0$
>3. **additivity in first slot**
>	1. $\langle u+v,w\rangle=\langle u,w\rangle+\langle v,w\rangle$
>4. **Homogeneity in first slot**
>	1. $\langle\lambda u,v\rangle=\lambda\langle u,v\rangle$
>	2. $\langle u,\lambda v\rangle=\overline{\lambda}\langle u,v\rangle$
>5. **conjugate symmetry**
>	1. $\langle u,v\rangle=\overline{\langle v,u\rangle}$ 

>[!example] Definition: Inner Product Space
>For an alternate definition, see here: [[Inner Product Space#^531b63|inner product space]]
>An inner product space is a [[Definition of Vector Space#^2686ea|vector space]] $V$ along with an inner product on $V$.

>[!example] Definition: Norm
>For $v\in V$, the *norm* of $v$, denoted $||v||$, is defined by
>$$||v||=\sqrt{\langle v,v\rangle}$$
>It fulfills some basic properties:
>1. $||v||=0$ if and only if $v=0$
>2. $||\lambda v||=|\lambda|\space||v||$

>[!example] Theorem: The zero vector and orthogonality
>1. $0$ is [[Orthogonal Sets of Vectors#^e50394|orthogonal]] to every vector in $V$
>2. $0$ is the only vector in $V$ that is orthogonal to itself.

>[!example] Theorem: Parallelogram Equality
>Suppose $u,v\in V$. Then
>$$||u+v||^2+||u-v||^2=2(||u||^2+||v||^2)$$

>[!example] Theorem: Norm of Orthonormal linear combination
>If $e_1,\dots,e_m$ is an [[Orthogonal Sets of Vectors#^5b5063|orthonormal]] list of vectors in $V$, then
>$$||a_1e_1+\cdots+a_me_m||^2=|a_1|^2+\cdots+|a_m|^2$$

>[!example] Theorem: Orthonormal Linear Independence
>Every single [[Orthogonal Sets of Vectors#^5b5063|orthonormal]] list of vectors is [[Span and Linear Independence#^31a3aa|linearly independent]]