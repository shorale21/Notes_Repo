# Basic Logical Operators
We use logical operators to symbolically notate [[Statements#^1794d4|statements]]

A **Truth Table** is a table describing all possible outcomes of a logical operator

>[!example]+ And, Or, and Not
>- The **And** operator connects two statements that must both be true. 
>- We use the $\land$ operator to denote "And"
>- [[Truth_Table_Storage#^4192cd|Truth Table for And]]
>$\space$
>- The **Or** operator connects two statements where one of them must be true
>- We use the $\lor$ operator to denote "Or"
>- [[Truth_Table_Storage#^5df80f|Truth Table for Or]]
>$\space$
>- The **Not** operator simply reverses a statement
>- We use the $\sim$ operator to denote "not"
>- [[Truth_Table_Storage#^4c16ea|Truth Table for Not]]

>[!example]+ The Conditional Operator
>- For statements of the form "If $P$, then $Q$"
>	- Also if something is "necessary" **or** "sufficient"
>- We use the notation $P\implies Q$ to denote the above statement
>- [[Truth_Table_Storage#^cd45c2|Truth Table for the conditional operator]]
>- There is also a **biconditional operator**
>- Used for statements of the form "$P$ if and only if $Q$"
>	- Also if something is "necessary" **and** "sufficient"
>- We use the symbol $\Leftrightarrow$ to denote the above statement
>- [[Truth_Table_Storage#^a61472|Truth table for the biconditional operator]]
>	- This operator is essentiall equivalent to $(P\implies Q)\land (Q\implies P)$

>[!example]+ Quantifiers
>"$\forall$" stands for "for all" or "for every"
>- Called the **Universal Quantifier**
>
>"$\exists$" stands for "there exists" or "there is" 
>- Called the **Existential Quantifier**
>>[!info]- Examples
>>"For every integer $n$" becomes $\forall n\in\mathbb{Z}$
>>"There exists a natural number $n$" becomes "$\exists n\in\mathbb{N}$"

>[!example]+ Special Laws for Logical Operators
>**Contrapositive Law**
>$$P \implies Q \space=\space (\sim Q)\implies(\sim P)$$
>**Commutative Laws**
>$$P\land Q \space = \space Q\land P$$
>$$P\lor Q \space = \space Q\lor P$$
>**Distributive Laws**
>$$P\land(Q\lor R) = (P\land Q)\lor(P\land R)$$
>$$P\lor(Q\land R) = (P\lor Q)\land(P\lor R)$$
>**Associative Laws**
>$$P\land (Q\land R)=(P\land Q)\land R$$
>$$P\lor (Q\lor R)=(P\lor Q)\lor R$$
>**Conditional and Quantifier Rules**
>$$\forall x\in X, Q(x)\quad=\quad(x\in X)\implies Q(x)$$

^b00fb9

