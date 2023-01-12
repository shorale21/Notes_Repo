# Proving Non-Conditional Statements
Recall the [[Logical Operators#^c54ef0|conditional statement]] of the form "If $P$, then $Q$"

The first form of nonconditional proof is the **biconditional statement**.
>[!example] Proving a biconditional statement
>Recall the [[Logical Operators#^c54ef0|biconditional statement]] of the form $P\Leftrightarrow Q$.
>Here is an outline of the Proof:
>$$\begin{align*}
&\textbf{Proposition: }\text{If }P\text{ then }Q\text{.}\\\\
&\textit{Proof.}\\
&[\text{Prove }P\implies Q]\\
&[\text{Prove }Q\implies P]
\end{align*}$$
>The proofs of the conditional statements can use any of the previous methods

>[!list] Definition: Equivalent Statements
>If a [[Direct Proof#^ba2a06|theorem]] provides a list of statements, stating that they are **equivalent**, for example$$\begin{align*}
&\textbf{Theorem }X:\text{ the following statements are equivalent.}\\
&\quad a)\space P\\
&\quad b)\space Q\\
&\quad c)\space R\\
&\quad d)\space S
\end{align*}$$Then if any of the statements are true, all of them are true. If any of the statements are false, all of them are false.
Or, in mathematical terms, $P\Leftrightarrow Q\Leftrightarrow R\Leftrightarrow S$
>How do we prove this?
>We make it simpler by using the logically equivalent statement:$$P\implies Q\implies R\implies S\implies P$$
>The cyclic nature of this allows for the proof. We then use any of the previous methods to prove this series of conditional statements.


>[!example] Existence and Uniqueness Proofs
>We want to prove a statement of the form: $\exists x, P(x)$
>These statements are called **Existence Statements**
>We can usually prove this with an example, although a single example does not prove a conditional statement. (if $P(x)$ is a conditional statement)
>Statements of the form "there exists a *unique* $x$ such that $P(x)$" are called **Uniqueness Statements**
>To prove these, you must prove that $x=d$ is an fulfills $P(x)$ and that it is the only example that does so
>- A **Constructive** existence proof finds an example that proves the theorem
>- A **Non-Constructive** existence proof proves there must exist an example, without finding a specific one
>
>>[!important]- Example of a Non-Constructive Proof
>>$$\begin{align*}
&\textbf{Proposition: }\text{There exist irrational numbers }x,y\text{ such that }x^y\text{ is rational }\\\\
&\textit{Proof.}\text{ Let }x=\sqrt{2}^{\sqrt{2}}\text{ and }y=\sqrt{2}.\text{ We know that }y\text{ is irrational, but we are not sure about }x.\\
&\underline{\text{Case 1:}}\text{ Suppose }x\text{ is irrational}\\
&\text{Then we have }x^{y}=\left(\sqrt{2}^{\sqrt{2}}\right)^{\sqrt{2}}=\sqrt{2}^{\sqrt{2}\sqrt{2}}=\sqrt{2}^{2}=2\text{  , which is rational}\\
&\underline{\text{Case 2:}}\text{ Suppose }x\text{ is rational }\\
&\text{Well then we have our example, since }x=\sqrt{2}^{\sqrt{2}}\text{, which is now rational}\\\\
&\textbf{Either way, an example of the proposition must exist, proving the statement}
\end{align*}$$
>
>>[!important]- Example of a Constructive Proof
>>$$\begin{align*}
&\textbf{Proposition: }\text{There exist irrational numbers }x,y\text{ such that }x^y\text{ is rational }\\\\
&\textit{Proof.}\text{ Let }x=\sqrt{2}\text{ and }y=\text{log}_{2}9\text{, and suppose we have proven that log}_{9}\text{ is irrational.}\\
&\text{Then we have }x^{y}=\sqrt{2}^{\text{log}_{2}9}=\sqrt{2}^{\text{log}_{2}3^{2}}=\sqrt{2}^{2\text{log}_{2}3}=2^{\text{log}_{2}3}=3\\
&\text{Since }3\text{ is rational, the statement is proven.}
\end{align*}$$