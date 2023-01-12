# Definition of Vector Space
>[!example] Definition: Vector Space
>A **Vector Space** is a set $V$ along with an addition on $V$ and a scalar multiplication on $V$ such that the following properties hold:
>
>**Commutativity:**$$u+v=v\space\text{  for all  }\space u,v\in V$$
>**Associativity:**$$(u+v)+w=u+(v+w)\quad\text{and}\quad(ab)v=a(bv)\space\text{ for all }u,v,w\in V\space\text{ and all }a,b\in\mathbb{F}$$
>**Additive Identity:**$$\text{there exists an element }0\in V\text{ such that }v+0=v\space\text{ for all }v\in V$$
>**Additive Inverse:**$$\text{for every }v\in V,\text{ there exists }w\in V\text{ such that }v+w=0$$
>**Multiplicative Identity:**$$1v=v\space\text{ for all }v\in V$$
>**Distributive Properties:**$$a(u+v)=au+av\quad\text{and}\quad(a+b)v=av+bv\space\text{ for all }a,b\in\mathbb{F}\text{ and all }u,v\in V$$
>
>Elements of a vector space are called *vectors* or *points*

^2686ea


>[!example] Definition: $\mathbb{F}^S$
>If $S$ is a [[Sets#^cfbc64|set]], then $\mathbb{F}^S$ denotes the set of functions from $S$ to $\mathbb{F}$
>
>For $f,g\in\mathbb{F}^S$, the sum $f+g\in\mathbb{F}^S$ is the function defined by$$(f+g)(x)=f(x)+g(x)$$for all $x\in S$
>
>For $\lambda\in\mathbb{F}$ and $f\in\mathbb{F}^S$, the product $\lambda f\in\mathbb{F}^S$ is the function defined by$$(\lambda f)(x)=\lambda f(x)$$for all $x\in S$

##### Vector Space Information
- A Vector Space has a *unique* additive identity
- Every element in a vector space has a *unique* additive inverse