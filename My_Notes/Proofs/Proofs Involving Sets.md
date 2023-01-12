# Proofs Involving Sets
Recall the [[Union, Intersection, Difference, Complement#^ca7d90|definitions]] involving [[Sets#^cfbc64|sets]].

>[!important] How to prove $a\in A$
>Generally, the set $A$ will be in the form $\{x:P(x)\}$.
>There's two important cases to cover.
>1. How to prove $a\in\{x:P(x)\}$
>	- Show that $P(a)$ is true
>2. How to prove $a\in\{x\in S:P(x)\}$
>	- Show that $a\in S$
>	- Show that $P(a)$ is true

>[!tip] How to prove $A\subseteq B$
>If we have two sets $A$ and $B$, and we want to prove $A\subseteq B$, then all we need to do is prove the [[Logical Operators#^c54ef0|conditional statement]] $a\in A\implies a\in B$
>We can do this with either [[Direct Proof#^d81cb3|direct]] or [[Contrapositive Proof#^733994|contrapositive]] proof
>Most proofs start with either "Suppose $a\in A$" or "Suppose $a\notin B$" and then continue from there

>[!important] How to prove $A=B$
>We sometimes want to prove two sets are the same
>We do this by first proving $A\subseteq B$, and then proving $B\subseteq A$
>If these are both true, then $A=B$

>[!example] Defintion: Perfect Numbers
>A number $p\in\mathbb{N}$ is called **perfect** if it equals the sum of its positive divisors other than itself
>- For example, $6$ is a perfect number since $6=3+2+1$