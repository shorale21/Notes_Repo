$x$ and $y$ are boolean variables.
Here are the axioms of boolean algebra:
1. $0\cdot0=0$
2. $1\cdot1=1$
3. $0\cdot1=1\cdot0=0$
4. $\overline{0}=1$
5. $1+1=1$
6. $0+0=0$
7. $1+0=0+1=1$
8. $\overline{1}=0$

Multiple Variable Theorems:
1. $x$ and $y$ are commutative
2. $x$ and $y$ are associative
3. The distributive property is obeyed
4. Absorption: $x\cdot(x+y)=x$
5. [[Negating Statements#^ee17f3|DeMorgan's Laws]]

>[!example] Operators in Boolean Algebra
>We define operators in boolean logic.
>The "$\cdot$" operator is called the AND operator and is the logical multiplication operation
>
>The "$+$" operator is called the OR operator and is logical addition
>
>The "$\overline{ }$" overbar operator is called the NOT operator and it defines an inversion or complementation
>
>[[Truth_Table_Storage#^4192cd|AND truth table]]
>[[Truth_Table_Storage#^5df80f|OR truth table]]

^daf0c1
## Boolean Functions and DeMorgan's Theorem
>[!example] Definition: SOP form
>SOP (sum of products) form is a formalism for boolean functions, where the algebra of the function is represented as a sum of products as so:
>$$F=(A\cdot B\cdot C)+(\overline{A}\cdot B\cdot C)+(\overline{A}\cdot B\cdot\overline{C})$$

>[!example] Definition: POS form
>POS (product of sums) form is a formalism for boolean functions, where the algebra of the function is represented as a product of multiple sums as so:
>$$F=(A+B+C)\cdot(\overline{A}+B+C)\cdot(\overline{A}+B+\overline{C})$$

Also important to design forms is [[Negating Statements#^ee17f3|DeMorgan's Law]]

## Minterms and Maxterms
There are two standard ways we can use a truth table to produce a boolean function.

The first way is to find the combinations of variables that make ones. Let's look at an example:

|  A  |  B  |  C  |  F  |
|:---:|:---:|:---:|:---:|
|  0  |  0  |  0  |  0  |
|  0  |  0  |  1  |  0  |
|  0  |  1  |  0  |  0  |
|  0  |  1  |  1  |  0  |
|  1  |  0  |  0  |  0  |
|  1  |  0  |  1  |  1  |
|  1  |  1  |  0  |  1  |
|  1  |  1  |  1  |  1  |

Where F is the output. Notice that the combination A=1, B=0, and C=1 produces a 1 for F. Thus we can define a product saying that F=1 if A$\cdot\overline{\text{B}}\cdot$C is 1. 

This product is known as a **minterm**. There are two other combinations that produce 1. These three minterms can be OR'ed together to define F in totality. Thus the minterm approach is the standard SOP approach as well.

The flipside is the **maxterm**. The **maxterm** is the OR statement that produces one of the zeroes in the truth table. The first row shows that if A=1, B=1, and C=1, then F=0. Thus we can define our maxterm as A+B+C. Note that this is the negation of the product (ABC). Each term in the truth table is associated with a maxterm or a minterm this way. 

The function F can be represented as a product of all the maxterms (POS form) or a sum of all the minterms (SOP form).  
