>[!example] Definition: Diagonal Matrix
>A Diagonal matrix is a square [[Linear Systems and Matrices#^8bad47|matrix]] that is $0$ everywhere except along the [[Eigenvectors And Upper Triangular Matrices#^ac90f9|diagonal]]

>[!example] Definition: Eigenspace
>Suppose $T\in\mathcal{L}(V)$ and $\lambda\in\mathbb{F}$. The *eigenspace* of $T$ corresponding to $\lambda$ is defined as
>$$E(\lambda,T)=\text{null}(T-\lambda I)$$
>It is the set of all eigenvectors of $T$ corresponding to $\lambda$ (including the zero vector)

>[!example] Theorem: Sum of Eigenspaces
>Suppose $V$ is [[Span and Linear Independence#^158509|finite dimensional]] and $T\in\mathcal{L}(V)$. Suppose $\lambda_1,\dots,\lambda_m$ are distinct eigenvalues of $T$. Then,
>$$E(\lambda_1,T)+\cdots+E(\lambda_m,T)$$
>is a [[Subspaces#^fe9044|direct sum]]. Furthermore,
>$$\text{dim }E(\lambda_1,T)+\cdots+\text{dim }E(\lambda_m,T)\le\text{dim }V$$

>[!example] Definition: Diagonalizable
>An [[Invertibility and Isomorphic Vector Spaces#^05873f|operator]] is called *diagonalizable* if the operator has a diagonal matrix with respect to some basis of $V$

>[!example] Theorem: Conditions of Diagonalizability
>Suppose $V$ is [[Span and Linear Independence#^158509|finite dimensional]] and $T\in\mathcal{L}(V)$. Let $\lambda_1,\dots,\lambda_m$ denote the distinct eigenvalues of $T$. Then the following statements are equivalent:
>1. $T$ is diagonalizable
>2. $V$ has a basis consisting of eigenvectors of $T$
>3. there exist 1-dimensional subspaces $U_1,\dots,U_n$ of $V$, each invariant under $T$, such that$$V=U_1\oplus\cdots\oplus U_n$$
>4. $V=E(\lambda_1,T)\oplus\cdots\oplus E(\lambda_m,T)$
>5. $\text{dim }V=\text{dim }E(\lambda_1,T)+\cdots+\text{dim }E(\lambda_m,T)$

>[!example] Eigenvalues imply Diagonalizability
>If $T\in\mathcal{L}(V)$ has $\text{dim }V$ distinct eigenvalues, the $T$ is diagonalizable.