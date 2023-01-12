### Null Space and Injectivity

>[!example] Definition: Null Space
>For $T\in\mathcal{L}(V,W)$, the *null space* of $T$, denoted $\text{null }T$, is the [[Subsets and Power Sets#^610582|subset]] of $V$ consisting of those vectors which $T$ maps to zero.
>$$\text{null }T=\{v\in V:Tv=0\}$$

^1553fb

>[!example] Theorem: Null Space is a Subspace
>If $T\in\mathcal{L}(V,W)$, then [[Null Spaces and Ranges#^1553fb|null]] $T$ is a [[Subspaces#^66ed31|subspace]] of $V$

>[!example] Definition: Injective
>A function $T:V\rightarrow W$ is called **injective** if $Tu=Tv$ implies $u=v$

^897d70

>[!example] Theorem: Injectivity and Null Space
>Let $T\in\mathcal{L}(U,V)$. Then $T$ is [[Null Spaces and Ranges#^897d70|injective]] if and only if [[Null Spaces and Ranges#^1553fb|null]] $T=\{0\}$

^d29891

>[!example] Theorem: Injectivity and Dimension
>Suppose $V$ and $W$ are [[Span and Linear Independence#^158509|finite dimensional]] [[Definition of Vector Space#^2686ea|vector spaces]] such that $\text{dim }V >\text{dim }W$. Then no [[Linear Maps#^844f9b|linear map]] from $V$ to $W$ is [[Null Spaces and Ranges#^897d70|injective]]

### Ranges and Surjectivity

>[!example] Definition: Range
>For $T$ a function from $V$ to $W$, the **range** of $T$ is the [[Subsets and Power Sets#^610582|subset]] of $W$ consisting of those vectors that are of the form $Tv$ for some $v\in V$.
>$$\text{range }T=\{Tv:v\in V\}$$

^d42c21

>[!example] Theorem: Range is a Subspace
>If $T\in\mathcal{L}(V,W)$, then [[Null Spaces and Ranges#^d42c21|range]] $T$ is a [[Subspaces#^66ed31|subspace]] of $W$

>[!example] Definition: Surjectivity
>A funciton $T$ from $V$ to $W$ is called **surjective** if [[Null Spaces and Ranges#^d42c21|range]] $T$ is $W$.

^b23aca

>[!example] Theorem: Surjectivity and Dimension
>Suppose $V$ and $W$ are [[Span and Linear Independence#^158509|finite dimensional]] [[Definition of Vector Space#^2686ea|vector spaces]] such that $\text{dim }V <\text{dim }W$. Then no [[Linear Maps#^844f9b|linear map]] from $V$ to $W$ is [[Null Spaces and Ranges#^b23aca|surjective]]