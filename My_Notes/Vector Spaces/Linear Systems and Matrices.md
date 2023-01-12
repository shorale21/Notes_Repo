### Linear Systems

>[!example] Definition: Linear System
>A linear system is given by 
>$$\begin{align*}
\sum\limits_{k=1}^{n}A_{1,k}x_{k}&=B_{1}\\
\vdots&\\
\sum\limits_{k=1}^{n}A_{m,k}x_{k}&=B_{m}
\end{align*}$$
>Where each $A$ and $B$ are constants.

^24ebc5


>[!example] Definition: Homogenous Linear System
>A [[Linear Systems and Matrices#^24ebc5|linear system]] is called **homogenous** if all the $B$ constants are equal to zero.

^913d30

>[!example] Theorem: Sols of Homogenous Linear System
>A [[Linear Systems and Matrices#^913d30|homogenous]] linear system with more variables than equations ($m<k$) has nonzero solutions

>[!example] Theorem: Sols of Inhomogenous Linear System
>An [[Linear Systems and Matrices#^913d30|inhomogenous]] linear system with more variables than equations ($m<k$) has no nonzero solutions for some choice of the constants $A$ and $B$

### Matrices

>[!example] Definition: Matrix
>Let $m,n$ denote positive integers. An $m$ by $n$ matrix $\textbf{A}$ is a rectangular array of elements of $\mathbb{F}$ with $m$ rows and $n$ columns.
>$$\textbf{A}=\begin{bmatrix}
>A_{1,1} & \cdots & A_{m,1}\\
>\vdots & & \vdots\\
>A_{1,n} & \cdots & A_{m,n}
>\end{bmatrix}$$
>Notation $\textbf{A}_{i,k}$ represents the element in the $i$th row and $k$th column of $\textbf{A}$

^8bad47

>[!example] Definition: Matrix of a Linear Map
>Suppose $T$ is a [[Linear Maps#^844f9b|linear map]] ($T\in\mathcal{L}(V,W)$), and $v_1,\dots,v_n$ forms a [[Bases and Dimension#^d92bcc|basis]] of $V$, and $w_1,\dots,w_m$ forms a basis for $W$. The **matrix of $T$** is the $m$ by $n$ [[Linear Systems and Matrices#^8bad47|matrix]] $\mathcal{M}(T)$ whose entries $A_{j,k}$ are defined as
>$$Tv_{k}=A_{1,k}w_{1}+\cdots+A_{m,k}w_{m}$$

>[!example] Matrix Addition
>The sum of two [[Linear Systems and Matrices#^8bad47|matrices]] $\textbf{A}+\textbf{B}=\textbf{C}$ is defined to be the sum of each element:
>$$\textbf{C}_{j,k}=\textbf{A}_{j,k}+\textbf{B}_{j,k}$$

^2c0d58

>[!example] Definition: Scalar Multiplication of Matrices
>Suppose $\lambda\in\mathbb{F}$ and $\textbf{A}$ is a [[Linear Systems and Matrices#^8bad47|matrix]]. The scalar muliplication of these two is defined to be
>$$(\lambda\textbf{A})_{j,k}=\lambda A_{j,k}$$

^f863e7

>[!example] Theorem: Sum and Scalar Multiplication of Linear Maps
>Suppose $S,T\in\mathcal{L}(V,W)$. Then $\mathcal{M}(S+T)=\mathcal{M}(S)+\mathcal{M}(T)$
>And $(\lambda\mathcal{M})(S)=\lambda\mathcal{M}(S)$

>[!example] Definition: Vector Space of Matrices
>Let $\mathbb{F}^{m,n}$ be the [[Sets#^cfbc64|set]] of all $m$ by $n$ matrices with entries in $\mathbb{F}$. With [[Linear Systems and Matrices#^2c0d58|addition]] and [[Linear Systems and Matrices#^f863e7|scalar multiplication]] defined, this is a [[Definition of Vector Space#^2686ea|vector space]] with [[Bases and Dimension#^e06091|dimension]] $m\cdot n$

>[!example] Definition: Matrix Multiplication
>Let $\textbf{A}$ be an $m$ by $n$ and $\textbf{C}$ be an $n$ by $p$.
>The product of these two [[Linear Systems and Matrices#^8bad47|matrices]] is defined to be
>$$(\textbf{A}\textbf{C})_{j,k}=\sum\limits_{r=1}^{n}A_{j,r}C_{r,k}$$
