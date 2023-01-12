## Polynomials Applied to Matrices
>[!example] Definition: Power of a Linear Operator
>Suppose $T\in\mathcal{L}(V)$ and $m\in\mathbb{Z}^{+}$
>- $T^m$ is defined to be $T^m=T\cdots T$
>- $T^0$ is deined to be the identity operator on $V$
>- If $T$ is [[Invertibility and Isomorphic Vector Spaces#^4130b0|invertible]] with inverse $T^{-1}$, then $T^{-m}=(T^{-1})^{m}$

>[!example] Definition: Operator Polynomials
>Suppose $T\in\mathcal{L}(V)$ and $p\in\mathcal{P}(\mathbb{F})$
>Then $p(T)$ is the operator defined by
>$$p(T)=a_{0}I+a_{1}T+a_{2}T^{2}+\cdots+a_{m}T^{m}$$

>[!example] Product of Polynomials
>If $p,q\in\mathcal{P}(\mathbb{F})$, the $pq\in\mathcal{P}(\mathbb{F})$ is the [[Span and Linear Independence#^8dcd73|polynomial]] defined by
>$$(pq)(z)=p(z)q(z)$$
>for $z\in\mathbb{F}$

>[!example] Suppose $p,q\in\mathcal{P}(\mathbb{F})$ and $T\in\mathcal{L}(V)$
>Then
>1. $(pq)(T)=p(T)q(T)$
>2. $p(T)q(T)=q(T)p(T)$

## Existence of Eigenvalues
>[!example] Theorem: Operators
>Every [[Invertibility and Isomorphic Vector Spaces#^05873f|operator]] on a finite dimensional, nonzero, complex vector space has an [[Invariant Subspaces#^e3b82a|eigenvalue]]

## Upper Triangular Matrices
>[!example] Matrix of an Operator
>Suppose $T\in\mathcal{L}(V)$ and $v_1,\dots,v_n$ is a basis of $V$. The [[Linear Systems and Matrices#^8bad47|matrix]] of $T$ with respect to this basis is the $n$ by $n$ matrix
>$$\mathcal{M}(T)=\begin{bmatrix} A_{1,1} & \cdots & A_{1,n} \\ \vdots & & \vdots\\ A_{n,1} & \cdots & A_{n,n}\end{bmatrix}$$
>Whose enttries $A_{j,k}$ are defined as
>$$Tv_{k}=A_{1,k}v_{1}+\cdots+A_{n,k}v_{n}$$

>[!example] Definition: Diagonal of a Matrix
>The diagonal of a square matrix are all the entries $A_{n,n}$ (along the diagonal)

^ac90f9

>[!example] Definition: Upper-Triangular Matrix
>A matrix is called *upper-triangular* if all the entries below the diagonal equal 0

>[!example] Theorem: Upper Triangular Matrix Conditions
>Suppose $T\in\mathcal{L}(V)$ and $v_1,\dots,v_n$ is a [[Bases and Dimension#^d92bcc|basis]] of $V$. Then the following are equivalent:
>1. The matrix of $T$ with respect to $v_1,\dots,v_n$ is upper triangular
>2. $Tv_j\in\text{span}(v_1,\dots,v_j)$ for each $j$
>3. $\text{span}(v_1,\dots,v_j)$ is invariant under $T$ for each $j$

>[!example] Theorem: Operators and Matrices
>Suppose $V$ is a [[Span and Linear Independence#^158509|finite-dimensional]] complex vector space and $T\int\mathcal{L}(V)$. Then $T$ has an upper-triangular matrix with respect to some basis of $V$

>[!example] Invertibility from upper-triangular matrices
>Suppose $T\in\mathcal{L}(V)$ has an upper-triangular matrix with respect to some basis of $V$. Then $T$ is [[Invertibility and Isomorphic Vector Spaces#^4130b0|invertible]] if and only if all the entries on the diagonal are nonzero.

>[!example] Eigenvalues of Triangular Matrices
>Suppose $T\in\mathcal{L}(V)$ has an upper-triangular matrix with respect to the some basis of $V$. Then the [[Invariant Subspaces#^e3b82a|eigenvalues]] of $T$ are precisely the entries on the diagonal of that matrix.

