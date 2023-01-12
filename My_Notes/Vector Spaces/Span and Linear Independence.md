# Span and Linear Independence


## Span
>[!example] Definition: Linear Combination
>A linear combination of a list $v_1,\dots,v_m$ of vectors in $V$ is a vector of the form
>$$a_1v_1+\cdots+a_mv_m$$
>Where $a_1,\dots,a_m\in\mathbb{F}$

^08e478

>[!example] Definition: Span
>The [[Sets#^cfbc64|set]] of all [[Span and Linear Independence#^08e478|linear combinations]] of a list of vectors in $V$ is called the **span** of those vectors.
>$$\text{span}(v_1,\dots,v_m)=\{a_1v_1+\cdots+a_mv_m:a_1,\dots,a_m\in\mathbb{F}\}$$
>The Span of the empty list $()$ is defined to be $\{0\}$

^f876bf

>[!example] Theorem: Span is the smallest containing subspace
>The [[Span and Linear Independence#^f876bf|span]] of a list of vectors in $V$ is the smallest [[Subspaces#^66ed31|subspace]] of $V$ containing all the vectors in that list.

>[!example] Definition: Finite-Dimensional
>A [[Definition of Vector Space#^2686ea|vector space]] is called *finite dimensional* if some list of vectors inside of it [[Span and Linear Independence#^f876bf|spans]] the whole space
>
>Every [[Subspaces#^66ed31|subspace]] of a finite dimensional vector space is finite dimensional

^158509


>[!example] Definition: Polynomial
>A function $p:\mathbb{F}\rightarrow\mathbb{F}$ is called a polynomial with coefficients in $\mathbb{F}$ if there exist $a_0,\dots,a_m\in\mathbb{F}$ such that $$p(z)=a_0+a_1z+a_2z^2+\cdots+a_mz^m$$for all $z\in\mathbb{F}$.
>$\mathcal{P}(\mathbb{F})$ is the [[Sets#^cfbc64|set]] of all polynomials with coefficients in $\mathbb{F}$
>
>A polynomial is said to have degree $m$ if $a_m\neq0$ in the above scenario.
>- The polynomial that is identically 0 has the degree $-\infty$
>
>For $m$ as a nonnegative integer, $\mathcal{P}(\mathbb{F})$ denotes the set of all polynomials with degree at most $m$

^8dcd73

>[!example] Definition: Infinite Dimensional
>A [[Definition of Vector Space#^2686ea|vector space]] is said to be *infinite dimensional* if it is not [[Span and Linear Independence#^158509|finite dimensional]]

## Linear Independence

>[!example] Definition: Linearly independent
>A list of vectors in $V$ is called linearly independent if the only choice of scalars in $\mathbb{F}$ that makes the [[Span and Linear Independence#^08e478|linear combination]] of those vectors and scalars equal to zero is that they are all zero
>
>The empty list is linearly independent
>
>Another way to state this is that each vector in the [[Span and Linear Independence#^f876bf|span]] of a list only appears once

^31a3aa

>[!example] Definition: Linearly Dependent
>A list of vectors is called linearly dependent if they are not [[Span and Linear Independence#^31a3aa|linearly independent]]

^746172

>[!example] Lemma: Linear Dependence
>Suppose $v_1,\dots,v_m$ is a [[Span and Linear Independence#^746172|linearly dependent]] list in $V$. Then there exists $j\in\{1,2,\dots,m\}$ such that the following hold:
>1. $v_j\in\text{span}(v_1,\dots,v_{j-1})$
>
>2. If the $j^{\text{th}}$ term is removed from $v_1,\dots,v_m$, the span of the remaining list equals $\text{span}(v_1,\dots,v_m)$

>[!example] Theorem: Length of Linearly independet list
>In a [[Span and Linear Independence#^158509|finitie dimensional]] [[Definition of Vector Space#^2686ea|vector space]], the length of every single [[Span and Linear Independence#^31a3aa|linearly independent]] list of vectors is less than or equal to the length of every [[Span and Linear Independence#^f876bf|spanning]] list of vectors.