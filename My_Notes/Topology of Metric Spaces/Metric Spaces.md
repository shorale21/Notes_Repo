# Metric Spaces
>[!example] A Metric
>A **metric** for a [[Sets#^cfbc64|set]] $X$ is a function $d$ from $X\times X$ to the non-negative real numbers, $\mathbb{R}_{\ge0}$.$$d:X\times X\rightarrow\mathbb{R}_{\ge0}$$
>Such that for all $x,y,x\in X$,
>$$\begin{align*}
&d(x,y)=d(y,x)\\\\
&d(x,z)\le d(x,y)+d(y,z)\\\\
&d(x,x)=0\\\\
&\text{If }d(x,y)=0,\text{ then }x=y
\end{align*}$$
>The inequality in the second condition is known as the **triangle inequality** since if $X$ represents all points in the plane, and $d$ is the concept of distance between said points, then the second condition says that every side length in a triangle must be less than or equal to the sum of the other two sides (barring of course the situation in which all three points are collinear)
>A function $d$ which satisfies only the first three conditions is called **pseudo-metric**.

^ae1289

>[!example] Metric Spaces
>A **Metric Space** is a pair $(X,d)$ where $X$ is a [[Sets#^c7baeb|set]] and $d$ is a metric on $X$.
>The notation is similar for a **Pseudo-Metric Space** 
>We call $d(x,y)$ the **distance** between $x$ and $y$ with $d$ being understood

^b21030


>[!definition] Balls in a Metric Space
>Let $(X,d(x,y))$ be a [[Metric Spaces#^b21030|Metric Space]]. 
>If $r$ is a positive number and $x\in X$, then the (open) **ball of radius $r$** about $x$ is defined to be the set of points with a distance less than $r$ from $x$ Symbolically,$$B_{r}(x):=\{y|d(x,y)<r\}$$
>If $r$ and $s$ are positive real numbers and if $x$ and $z$ are points of a pseudo-metric space $X$, then it is possible that $B_{t}(x)\cap B_{s}(z)=\emptyset$. This is definitely true if $d(x,z)>r+s$. Otherwise, suppose the interesection is not empty, and that $$w=B_{t}(x)\cap B_{s}(z)$$.
>If $y\in X$ is such that $d(y,w)<\text{min}[r-d(x,w),s-d(z,w)]$, then the triangle inequality implies that $y\in B_{r}(x)\cap B_{s}(z)$, or if we set $t=\text{min}[r-d(x,w),s-d(z,w)]$, then$$B_{t}(w)\subset B_{r}(x)\cap B_{s}(z)$$
>In essentials, if we call a set on $X$ **open**, it is either empty, or the union of open balls. This gives two properties:
>1. The intersection of any finite number of open sets is open
>2. The union of any number of open sets is open

>[!example] Maps in Metric Spaces
>A map $f:X\rightarrow Y$ from one metric space to another is called **continuous** if the inverse image under $f$ of any open set in $Y$ is an open set in $X$.