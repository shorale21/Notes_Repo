# Proof by Contradiction
Consider the [[Truth_Table_Storage#^cd32e4|truth table]] for $(\sim P)\implies(C\land\sim C)$

Notice that the result is the same as the values for $P$ itself.

This means that $P$ and $(\sim P)\implies(C\land\sim C)$ are logically equivalent, and therefore proving $(\sim P)\implies(C\land\sim C)$ will also prove $P$.

This is **Proof by contradiction**. Essentially, you must prove that the [[Negating Statements#^a7e8e6|negation]] of $P$ implies a contradiction.

>[!example] Proof by Contradiction
>Consider the proposition: $P$
>To prove it, do the following:
>$$\begin{align*}
&\textbf{Proposition}: P\\
&Proof. \text{ suppose } \sim P.\\
&\quad\text{.}\\
&\quad\text{.}\\
&\quad\text{.}\\
&\text{Therefore } C\land\sim C.
\end{align*}$$

^4ed34d

>[!Definition] Definition: Rational
>A real number $x$ is [[Sets#^d3aac2|rational]] if $x=\frac{a}{b}$ for some $a,b\in\mathbb{Z}$
>- $\exists\space a,b\in\mathbb{Z}:x=\frac{a}{b}\implies x\in\mathbb{Q}$
>
>A real number $x$ is irrational if $x\neq\frac{a}{b}$ for every $a,b\in\mathbb{Z}$
>- $\forall\space a,b\in\mathbb{Z}:x\neq\frac{a}{b}\implies x\notin\mathbb{Q}$

>[!important]- Example Proof: Infinite Primes
>**Proposition:** There are infinitely many [[Direct Proof#^9dcb62|prime numbers]].
>*Proof.* For the sake of contradiction, assume there are finitely many prime numbers. Then we can list all of the prime numbers as $p_1,p_2,p_3,\dots,p_n$. Thus $p_n$ is the $n$th and largest prime number. 
>Consider the number $a$, such that $a=(p_1p_2p_3\cdots p_n)+1$. That is, $a$ is the product of all the prime numbers plus 1.
>$a$, like any [[Sets#^d3aac2|natural number]], has at least one prime divisor. That is, there exists a prime number, $p_k$, such that $p_k|a$ and $a=cp_k$$$(p_1p_2p_3\cdots p_{k-1}p_kp_{k+1}\cdots p_n)+1=cp_k$$
>Divide both sides by $p_k$:$$(p_1p_2p_3\cdots p_{k-1}p_{k+1}\cdots p_n)+\frac{1}{p_k}=c$$
>So, we have$$c-(p_1p_2p_3\cdots p_{k-1}p_{k+1}\cdots p_n)=\frac{1}{p_k}$$
>Notice that the left side is an integer (since it is the product and difference of multiple natural numbers), and the right side is not an integer
>This is a contradiction, and therefore we have proven the proposition.


>[!example] Proof of Contradiction for a conditional
>Recall the [[Negating Statements#^a7e8e6|negation of a conditional statement]].
>Therefore, we can define an outline of the proof.
>$$\begin{align*}
&\textbf{Proposition}: P\implies Q\\
&Proof. \text{ suppose } P\space\text{and}\space\sim Q\\
&\quad\text{.}\\
&\quad\text{.}\\
&\quad\text{.}\\
&\text{Therefore } C\land\sim C.
\end{align*}$$