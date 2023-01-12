# Direct Proofs
We often like to use elements of [[Sets#^cfbc64|set theory]] and [[Logical Operators#^8c3800|mathematical logic]] to prove [[Statements#^1794d4|statements]].
>[!example] Definition: Theorems and others
>A **Theorem** is a statement that is true and that has been proved to be true
>
>A **Proposition** is a statement that is true but not as significant
>
>A **Lemma** is a theorem whose main purpose is to prove another theorem
>
>A **Corollary** is a result or immediate consequnce of a theorem

^ba2a06

>[!important]- Helpful Definitions
>- An integer $n$ is **even** if $n=2a$ for some integer $a\in\mathbb{Z}$
>
>- An integer $n$ is **odd** if $n=2a+1$ for some integer $a\in\mathbb{Z}$
>
>- Two integers have the same **parity** if they are both odd or both even
>
>- Suppose $a$ and $b$ are integers. We say that $a$ **divides** $b$, written $a|b$ if $b=ac$ for some integer $c\in\mathbb{Z}$. In this case we also say that $a$ is a **divisor** of $b$, and that $b$ is a **multiple** of $a$
>- A number $n\in\mathbb{N}$ is **prime** if it is exactly two positive divisors, $1$ and $n$. If $n$ has more than two positive divisors it is called **composite**.
>- The **greatest common divisor** of integers $a$ and $b$, denoted gcd$(a,b)$ is the largest integer that divides both $a$ and $b$
>- The **least common multiple** of non-zero integers $a$ and $b$, denoted lcm($a$,$b$), is the smallest integer in $\mathbb{N}$ that is a multiple of both $a$ and $b$
>- If $a$ and $b$ are integers, then so are their sum, product and differences
>- Given integers $a$ and $b$ with $b>0$, there exist unique integers $q$ and $r$ for which $a=qb+r$ and $0\le r<b$
>- Given integers $a$ and $b$, we say that $a$ and $b$ are **congruent modulo n** if $n|(a-b)$. We express this as $a\equiv b\space\text{(mod n)}$

^9dcb62

>[!example] Direct Proof of a Proposition
>Consider the proposition: If $P$, then $Q$
>To prove it, do the following:
>$$\begin{align*}
&\textbf{Proposition}\text{: If }P\text{ then }Q\\
&Proof. \text{ suppose } P.\\
&\quad\text{.}\\
&\quad\text{.}\\
&\quad\text{.}\\
&\text{Therefore } Q.
\end{align*}$$
>Often times, it is useful to consider cases in order to prove things
>If there are very similar cases, sometimes it is appropriate to use "without loss of generality" or "WLOG"

^d81cb3
