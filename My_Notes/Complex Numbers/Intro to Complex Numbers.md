# Intro to Complex Numbers
In this note we will explore the basics of the scalars contained in the [[Sets#^cfbc64|set]] $\mathbb{C}$, the set of complex numbers.

>[!example] Definition: Complex Numbers
>A **Complex Number** is an ordered pair $(a,b)$ where $(a,b)\in\mathbb{R}$ but we will write this as $a+bi$, remembering that $i=\sqrt{-1}$
>
>The [[Sets#^cfbc64|set]] of all complex numbers is denoted by $\mathbb{C}$:$$\mathbb{C}=\{a+bi:a,b\in\mathbb{R}\}$$
>
>Addition an multiplication are defined on $\mathbb{C}$ by
>$$(a+bi)+(c+di)=(a+c)+(b+d)i$$
>$$(a+bi)(c+di)=(ac-bd)+(ad+bc)i$$
>Where $a,b,c,d\in\mathbb{R}$

^580f4e


##### Properties of Complex Arithmatic
Let $\alpha,\beta,\lambda$ be in $\mathbb{C}$

**Commutativity:**$$\alpha+\beta=\beta+\alpha\quad\text{and}\quad\alpha\beta=\beta\alpha$$
**Associativity:**$$(\alpha+\beta)+\lambda=\alpha+(\beta+\lambda)\quad\text{and}\quad(\alpha\beta)\lambda=\alpha(\beta\lambda)$$
**Identities:**$$\lambda+0=\lambda\quad\text{and}\quad\lambda1=\lambda$$
**Additive Inverse:**$$\text{For every }\alpha,\text{ there exists a unique }\beta\text{ such that }\alpha+\beta=0$$
**Multiplicative Inverse:**$$\text{For every }\alpha,\text{ with }\alpha\neq0,\text{ there exists a unique }\beta\text{ such that }\alpha\beta=1$$
**Distributive Property:**$$\lambda(\alpha+\beta)=\lambda\alpha+\lambda\beta$$

#### Properties of Conjugates and Absolute values
>[!example] Definition: Real and Complex Parts
>Suppose we have a complex number $z=a+bi$.
>- The real part of $z$, denoted $\text{Re }z$, is $a$
>- The imaginary part of $z$, denoted, $\text{Im }b$
>Then $z=\text{Re }z+(\text{Im }z)i$

>[!example] Definition: Complex Conjugate
>Suppose $z\in\mathbb{C}$
>The *complex conjugate* of $z\in\mathbb{C}$, denoted $\bar{z}$ is defined by
>$$\bar{z}=(\text{Re }z)-(\text{Im }z)i$$

>[!example] Definition: Absolute value on $\mathbb{C}$
>The *absolute value* of a complex number $z$, denoted $|z|$, is defined by
>$$|z|=\sqrt{(\text{Re }z)^2+(\text{Im }z)^2}$$

**Properties**
Suppose $w,z\in\mathbb{C}$
1. $z+\bar{z}=2(\text{Re }z)$
2. $z-\bar{z}=2(\text{Im }z)i$
3. $z\bar{z}=|z|^2$
4. $\overline{w+z}=\bar{w}+\bar{z}$
5. $\overline{wz}=\bar{w}\bar{z}$
6. $\bar{\bar{z}}=z$
7. $|\text{Re }z|\le|z|$
8. $|\text{Im }z|\le|z|$
9. $|\bar{z}|=|z|$
10. $|wz|=|w||z|$
11. $|w+z|\le|w|+|z|$ better known as the [[Metric Spaces#^ae1289|triangle inequality]]