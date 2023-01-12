# Disproof

In this section, I want to focus on disproving statements that are false.

>[!example] Definition: Conjecture
>A **Conjecture** is a [[Statements#^1794d4|statement]] that is suspected to be true, but has not yet been proven to be true.

The best way to disprove $P$ is to prove $\sim P$. This will be fairly simple for certain examples.

>[!tip] Disproving Universal or Conditional Statements
>Say we have a conjecture of the form $P:\space\forall x\in S,\space Q(x)$
>Remember that the [[Negating Statements#^a7e8e6|negation]] of this is$$\sim(\forall x\in S,\space Q(x))\space\space=\space\space\exists\space x\in S,\space\sim Q(x)$$
>This makes things considerably easier, because now all we have to do is find a **counterexample**
>All you need to do is find an example of $x\in S$ where $Q(x)$ is false.
>The process of finding a counterexample works for $P(x)\implies Q(x)$
>- All we have to do for the [[Logical Operators#^c54ef0|conditional]] statement is to find an example of an $x$ for which $P(x)$ is true and $Q(x)$ is false

Another general way of disproof is through [[Proof By Contradiction#^4ed34d|proof by contradiction]]. Except in this case, one would assuve $P$ is true, and then reach a contradiction, in order to prove $P$ is false.