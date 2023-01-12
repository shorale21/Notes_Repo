# Sets

^c7baeb

>[!info] Definition of Sets
>- A set is any collection of items
>- These items are called **elements**
>- Sets are often denoted with curly braces, such as $\{1,2,3\}$

^cfbc64

- Sets can have infinite or finite elements, ex: $\{\dots,1,2,3,\dots\}$
- Two sets are considered **equal** if they have exactly the same elements
		- ex: $\{1,2,3\}=\{1,2,3\}$
- To express an element inside a set, we use "$\in$"
		- ex: $2\in\{1,2,3\}$
- Fundamental sets:
		- Natural numbers, $\mathbb{N}=\{1,2,3,\dots\}$
		- Integer numbers, $\mathbb{Z}=\{\dots,-2,-1,0,1,2,\dots\}$
		- Rational numbers, $\mathbb{Q}=\{\frac{a}{b}|a\in\mathbb{Z},b\in\mathbb{Z}\}$
		- Real numbers, $\mathbb{R}$ ^d3aac2
- The **Cardinality** of a set describes the size, and is the number of elements. Denoted by $|A|$
		- ex: If $A=\{1,2,3\}$ then $|A|=3$ ^f7ff23
- The **empty set** is the set $\{\}$ and is usually denoted by $\varnothing$ or $\emptyset$ ^a39cdf
- **Set builder notation** consists of $X=\{expression:rule\}$ with $:$ or $|$ meaning "such that"
- **Interval Notation** is used to describe an interval of values, describing an infinite set. 
		- Closed Interval: $[n_1, n_2]$
		- Half Open Interval: $[n_1,n_2)$ or $(n_1,n_2]$
		- Open Interval: $(n_1,n_2)$
		- Infinite Interval: $[n_1,\infty)$ or $(-\infty,n_2]$ or $(-\infty,\infty)$

>[!example] DeMorgan's Laws for sets
>These are version of [[Negating Statements#^ee17f3|DeMorgan's Laws]] for sets.
>$$\begin{align*}
\overline{A\cap B}&=\overline{A}\cup\overline{B}\\
\overline{A\cup B}&=\overline{A}\cap\overline{B}
\end{align*}$$

>[!example] Other laws for sets
>First is a version of the [[Logical Operators#^b00fb9|Distributive Laws]] for sets.
>$$\begin{align*}
A\cap(B\cup C)&=(A\cap B)\cup(A\cap C)\\
A\cup(B\cap C)&=(A\cup B)\cap(A\cup C)\\
A\times(B\cup C)&=(A\times B)\cup(A\times C)\\
A\times(B\cap C)&=(A\times B)\cap(A\times C)
\end{align*}$$