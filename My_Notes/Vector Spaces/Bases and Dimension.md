# Bases and Dimension

## Bases
>[!example] Definition: Basis
>A *basis* of $V$ is a list of vectors in $V$ that is [[Span and Linear Independence#^31a3aa|linearly independent]] and [[Span and Linear Independence#^f876bf|spans]] $V$

^d92bcc

>[!example] Theorem: Spanning List Contains Basis
>Every [[Span and Linear Independence#^f876bf|spanning]] list in a vector space can be reduced to a [[Bases and Dimension#^d92bcc|basis]] of that vector space

>[!example] Theorem: Finite Dimensional Basis
>Every [[Span and Linear Independence#^158509|finite dimensional]] vector space has a basis.

>[!example] Theorem: Linearly independent extends to basis
>Every [[Span and Linear Independence#^31a3aa|linearly independent]] list of vectors in a finite dimensional vector space can be extended to a [[Bases and Dimension#^d92bcc|basis]] of the vector space

>[!example] Theorem: Direct Sum
>Suppose $V$ is [[Span and Linear Independence#^158509|finite dimensional]] and $U$ is a [[Subspaces#^66ed31|subspace]] of $V$. Theen there is a subspace $W$ of $V$ such that $V=U\oplus W$

## Dimension

>[!example] Theorem: Basis Length
>Any two [[Bases and Dimension#^d92bcc|bases]] of a [[Span and Linear Independence#^158509|finite dimensional]] [[Definition of Vector Space#^2686ea|vector space]] have the same length

^b9cd13

>[!example] Definition: Dimension
>- The *dimension* of a [[Span and Linear Independence#^158509|finite dimensional]] [[Definition of Vector Space#^2686ea|vector space]] is the length of any [[Bases and Dimension#^d92bcc|basis]] of the vector space
>- The dimension of $V$ is denoted $\text{dim}\space V$

^e06091

>[!example] Theorem: Dimension of a subspace
>If $V$ is [[Span and Linear Independence#^158509|finite dimensional]] and $U$ is a [[Subspaces#^66ed31|subspace]] of $V$, then $\text{dim}\space U\le\text{dim}\space V$

>[!example] Theorem: Linear independent Basis
>Suppose $V$ is [[Span and Linear Independence#^158509|finite dimensional]]. Then every [[Span and Linear Independence#^31a3aa|linearly independent]] list of vectors in $V$ with length $\text{dim}\space V$ is a [[Bases and Dimension#^d92bcc|basis]] of $V$

>[!example] Theorem: Spanning Basis
>Suppose $V$ is [[Span and Linear Independence#^158509|finite dimensional]]. Then every [[Span and Linear Independence#^f876bf|spanning]] list of vectors in $V$ with length $\text{dim}\space V$ is a [[Bases and Dimension#^d92bcc|basis]] of $V$

>[!example] Theorem: Dimension of a Sum
>If $U_1$ and $U_2$ are [[Subspaces#^66ed31|subspaces]] of a [[Span and Linear Independence#^158509|finite dimensional]] [[Definition of Vector Space#^2686ea|vector space]] then $$\text{dim}(U_1+U_2)=\text{dim}(U_2)-\text{dim}(U_1\cap U_2)$$