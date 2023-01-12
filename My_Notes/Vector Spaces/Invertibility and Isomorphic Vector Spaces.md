
## Invertiblity
>[!example] Definition: Invertible Linear Map
>A [[Linear Maps#^844f9b|linear map]] $T\in\mathcal{L}(V,W)$ is called *invertible* if there exists a linear map $S\in\mathcal{L}(W,V)$ on $V$  and $TS$ equals the identity map on $W$
>
>If $v$ is in $V$, and $Tv=w$ in $W$, then $Sw=v$.
>
>The linear map $S$ satisfying $ST=I$ (on $V$) and $TS=I$ (on $W$) is called an *inverse* of $T$
>
>such an $S$ would be denoted as $T^{-1}$

^4130b0

>[!example] Theorem: Uniqueness
>An [[Invertibility and Isomorphic Vector Spaces#^4130b0|invertible]] linear map has a unique inverse.

>[!example] Theorem: Equivalence
>A [[Linear Maps#^844f9b|linear map]] is [[Invertibility and Isomorphic Vector Spaces#^4130b0|invertible]] if and only if it is [[Null Spaces and Ranges#^897d70|injective]] and [[Null Spaces and Ranges#^b23aca|surjective]]

## Isomorphism
>[!example] Definition: Isomorphism
>An *isomorphism* is an [[Invertibility and Isomorphic Vector Spaces#^4130b0|invertible]] [[Linear Maps#^844f9b|linear map]]
>
>Two [[Definition of Vector Space#^2686ea|vector spaces]] are called *isomorphic* if there is an *isomorphism* from one vector space onto the other one

^989fe0

>[!example] Theorem: Isomorphism and Dimension
>Two [[Span and Linear Independence#^158509|finite dimensional]] [[Definition of Vector Space#^2686ea|vector spaces]] over $\mathbb{F}$ are [[Invertibility and Isomorphic Vector Spaces#^989fe0|isomorphic]] if and only if they have the same [[Bases and Dimension#^e06091|dimension]] 

>[!example] Theorem: Specific Isomorphisms
>Suppose $v_1,\dots,v_n$ is a basis of $V$ and $w_1,\dots,w_m$ is a basis of $W$. Then $\mathcal{M}$ is an [[Invertibility and Isomorphic Vector Spaces#^989fe0|isomorphism]] between $\mathcal{L}(V,W)$ and $\mathbb{F}^{m,n}$

>[!example] Theorem: Dimension of Linear Maps
>Suppose $V$ and $W$ are [[Span and Linear Independence#^158509|finite dimensional]]. Then $\mathcal{L}(V,W)$ is finite dimensional and 
>$$\text{dim }\mathcal{L}(V,W)=(\text{dim }V)(\text{dim }W)$$

## Linear Maps as Matrices
>[!example] Definition: Matrix of a Vector
>Suppose $v\in V$ and $v_1,\dots,v_n$ is a [[Bases and Dimension#^d92bcc|basis]] of $V$. The [[Linear Systems and Matrices#^8bad47|matrix]] of $v$ with respect to this basis is the $n$ by $1$ matrix
>$$\mathcal{M}(v)=\begin{pmatrix}
>c_{1}\\
>\vdots\\
>c_n
>\end{pmatrix}$$
>where $c_1,\dots,c_n$ are the scalars where
>$$v=c_1v_1+\cdots+c_nv_n$$

>[!example] Theorem: Matrices of linear maps
>Suppose $T\in\mathcal{L}(V,W)$ and $v_1,\dots,v_n$ is a basis of $V$ and $w_1,\dots,w_m$ is a basis of $W$. Let $1\le k\le n$. Then the $k^\text{th}$ column of $\mathcal{M}(T)$, which is denoted by $\mathcal{M}(T)_{.,k}$, equals $\mathcal{M}(v_k)$

>[!example] Theorem: Linear Maps and Multiplications
>Suppose $T\in\mathcal{L}(V,W)$ and $v\in V$. Suppose $v_1,\dots,v_n$ is a basis of $V$ and $w_1,\dots,w_m$ is a basis of $W$. Then$$\mathcal{M}(Tv)=\mathcal{M}(T)\mathcal{M}(v)$$

## Operators
>[!example] Definition: Operator
>An *operator* is a [[Linear Maps#^844f9b|linear map]] from a [[Definition of Vector Space#^2686ea|vector space]] to itself
>
>The notation $\mathcal{L}(V)$ denotes the [[Sets#^cfbc64|set]] of all operators on $V$.
>This means $\mathcal{L}(V)=\mathcal{L}(V,V)$

^05873f

>[!example] Theorem: Equivalency of functions
>Suppose $V$ is [[Span and Linear Independence#^158509|finite dimensional]] and $T\in\mathcal{L}(V)$. Then the following are equivalent:
>1. $T$ is [[Invertibility and Isomorphic Vector Spaces#^4130b0|invertible]]
>2. $T$ is [[Null Spaces and Ranges#^d29891|injective]]
>3. $T$ is [[Null Spaces and Ranges#^b23aca|surjective]]