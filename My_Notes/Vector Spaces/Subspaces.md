# Subspaces
>[!example] Definition: Subspace
>A subset $U$ of $V$ is called a **subspace** of $V$ if $U$ is also a [[Definition of Vector Space#^2686ea|vector space]]
>
>This means $U$ must satisfy the following properties:
>- $U$ contains an additive identity
>- closd under addition
>- closd under scalar multiplication

^66ed31

>[!example] Theorem: Sum of Subspaces
>Suppose $U_1,\dots,U_m$ are subspaces of $V$. Then $U_1+\cdots+U_m$ is the smallest subspace of $V$ containing $U_1,\dots,U_m$

>[!example] Definition: Direct Sum
>Suppose $U_1,\dots,U_m$ are subspaces of $V$
>- The sum $U_1+\cdots+U_m$ is called a **direct sum** if each element of $U_1+\cdots+U_m$ can be written in only one way as a sum $u_1+\cdots+u_m$ where each $u_j$ is in $U_j$
>
>- If $U_1+\cdots+U_m$ is a direct sum, then $U_1\oplus\cdots\oplus U_m$ denotes $U_1+\cdots+U_m$, with the $\oplus$ notation indicating that it is a direct sum.
>
>- Another condition is that the only way to write $0$ as a sum $u_1+\cdots+u_m$ where each $u_j$ is in $U_j$ is to take each $u_j$ equal to $0$

^fe9044

>[!example] Theorem: Direct Sum of Two Subspaces
>Suppose $U$ and $W$ are subspaces of $V$. Then $U+W$ is a [[Subspaces#^fe9044|direct sum]] if and only if $U\space\cap\space W=\{0\}$ 

>[!example] Theorem: Every subspace is part of a direct sum
>Suppose $V$ is [[Span and Linear Independence#^158509|finite dimensional]] and $U$ is a [[Subspaces#^66ed31|subspace]] of $V$. Then there exists a subspace $W$ of $V$ such that $V=U\oplus W$
