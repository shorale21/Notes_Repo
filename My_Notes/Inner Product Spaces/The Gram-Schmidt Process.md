# The Gram-Schmidt Process
>[!definition] Lemma: Orthogonality formula
>Let $\{\textbf{v}_1,\textbf{v}_2,\dots,\textbf{v}_n\}$ be an [[Orthogonal Sets of Vectors#^5d518e|orthogonal set]] of vectors in an [[Inner Product Space#^531b63|inner product space]] $V$. If $\textbf{x}\in V$, then the vector$$\textbf{x}-\textbf{P}(\textbf{x},\textbf{v}_1)-\textbf{P}(\textbf{x},\textbf{v}_2)-\cdots-\textbf{P}(\textbf{x},\textbf{v}_n)$$is orthogonal to $v_i$ for each $i$

>[!example] The Gram-Schmidt Process
>Let $\{\textbf{x}_1,\textbf{x}_2,\dots,\textbf{x}_m\}$ be a basis for the [[Inner Product Space#^531b63|inner product space]] $V$. Then an orthogonal basis for $V$ is given by $\{\textbf{v}_1,\textbf{v}_2,\dots,\textbf{v}_m\}$ where
>$$\begin{align*}
\textbf{v}_1&=\textbf{x}_1\\
\textbf{v}_2&=\textbf{x}_2-\frac{\langle\textbf{x}_2,\textbf{v}_1\rangle}{||\textbf{v}_1||^2}\textbf{v}_1\\
\textbf{v}_3&=\textbf{x}_3-\frac{\langle\textbf{x}_3,\textbf{v}_1\rangle}{||\textbf{v}_1||^2}-\frac{\langle\textbf{x}_3,\textbf{v}_2\rangle}{||\textbf{v}_2||^2}\textbf{v}_2\\
\vdots\\
\textbf{v}_i&=\\
\vdots\\
\textbf{v}_m&=
\end{align*}$$