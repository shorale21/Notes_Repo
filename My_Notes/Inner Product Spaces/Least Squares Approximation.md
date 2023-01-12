# Least Squares Approximation
We will focus on inconsistent systems of linear equations

>[!example] Least Squares Approximation
>The line or equation that best fits a certain system or set of data.
>**Problem of Least Squares**
>- Let $A$ be an $m\times n$ matrix, and let $\textbf{b}$ be a fixed vector in $\mathbb{R}^m$. If $A\textbf{x}=\textbf{b}$ is a linear system of $m$ equations and $n$ unknowns, seek to minimize the quantity $\epsilon(\textbf{x})=||A\textbf{x}-\textbf{b}||$ by an appropriate choice of $\textbf{x}$, say $\textbf{x}_0$. The vector $\textbf{x}_0$ is called a **least squared solution** to the system $A\textbf{x}=\textbf{b}$.
>
>>[!list]+ Derivation of the Least Squared Solution
>>Let $A$ be an $m\times n$ matrix, $\textbf{x}$ a vector of unknowns in $\mathbb{R}^n$ and $\textbf{b}$ a vector given in $\mathbb{R}^m$.
>>Observe that a vector $\textbf{x}_0$ in $\mathbb{R}^n$ will be a least squares solution if and only if $\textbf{b}-A\textbf{x}_0$ is orthogonal to every vector in the subspace$$\text{colspace}(A)=\{A\textbf{x}:\textbf{x}\in\mathbb{R}^n\}$$of $\mathbb{R}^m$.
>>That is, for every $\textbf{x}\in\mathbb{R}^n$, we must have$$\langle A\textbf{x},\textbf{b}-A\textbf{x}_0\rangle=0$$
>>Since the inner product of two vectors can be written as matrix multiplication, then the above formula becomes$$(A\textbf{x})^{T}(\textbf{b}-A\textbf{x}_0)=0$$$$\textbf{x}^{T}A^{T}(\textbf{b}-A\textbf{x}_0)=0$$
>>Since this must work for all $\textbf{x}$ in $\mathbb{R}^n$, the $\textbf{x}$ is trivial and therefore can be eliminated.$$A^{T}(\textbf{b}-A\textbf{x}_0)=0$$
>>So then it works out that$$A^TA\textbf{x}_0=A^T\textbf{b}$$
>>Provided that $A$ has linearly independent columns, the matrix $A^TA$ is invertible and thus$$\textbf{x}_0=(A^TA)^{-1}A^T\textbf{b}$$
>
>The **Projection Matrix** of an invertible matrix $A$ is given by $P=A(A^TA)^{-1}A^T$
>To find the least squares solution we simply need to solve the system of equations given by$$A\textbf{x}_0=P\textbf{b}$$