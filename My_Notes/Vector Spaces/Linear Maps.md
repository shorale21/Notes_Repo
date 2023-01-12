>[!example] Definition: Linear Map
>A *linear map* from $V$ tp $W$ is a function $T:V\rightarrow W$ with the following properties:
>- $T(u+v)=T(u)+T(v)$ for all $u,v\in V$
>
>- $T(\lambda v)=\lambda T(v)$ for all $\lambda\in\mathbb{F}$ and all $v\in V$
>
>The set of all linear maps from $V$ to $W$ is denoted $\mathcal{L}(V,W)$
>
>$\mathcal{L}(V,W)$ is a [[Definition of Vector Space#^2686ea|vector space]]

^844f9b

**Examples of Linear Maps**
The identity map, denoted $I$, is the function that takes each element to itself, specifically:
$$I(v)=v$$

The differential map, defined as $D\in\mathcal{L}(\mathcal{P}(\mathbb{R}),\mathcal{P}(\mathbb{R}))$, is such that
$$D(p)=p'$$

The integral map, defined as $T\in\mathcal{L}(\mathcal{P}(\mathbb{R}),\mathbb{R})$, is such that $$T(p)=\int_{0}^{1}p(x)dx$$



>[!example] Theorem: Basis of Domain for Linear Maps
>Suppose $v_1,\dots,v_m$ is a [[Bases and Dimension#^d92bcc|basis]] of $V$ and $w_1,\dots,w_m\in W$. Then there exists a unique [[Linear Maps#^844f9b|linear map]] $T:V\rightarrow W$ such that$$T(v_j)=w_j$$For each $j$

>[!example] Definition: Algebra on $\mathcal{L}(V,W)$
>Suppose $S,T\in\mathcal{L}(V,W)$ and $\lambda\in\mathbb{F}$. The sum $S+T$ and the product $\lambda T$ are the [[Linear Maps#^844f9b|linear maps]] from $V$ to $W$ defined by 
>$$(S+T)(v)=S(v)+T(v)\quad\text{and}\quad(\lambda T)(v)=\lambda T(v)$$

>[!example] Definition: Product of Linear Maps
>If $T\in\mathcal{L}(U,V)$ and $S\in\mathcal{L}(V,W)$, then the product $ST\in\mathcal{L}(U,W)$ is defined by$$(ST)(u)=S(T(u))$$For all $u\in U$
>[[Linear Maps#^844f9b|Linear maps]] will adhere to associativity, identiy, and distributive properties

### Fundamental Theorems of Linear Maps
>[!example] The Fundamental Theorem of Linear Maps
>Suppose $V$ is [[Span and Linear Independence#^158509|finite dimensional]] and $T\in\mathcal{L}(V,W)$. Then [[Null Spaces and Ranges#^d42c21|range]] $T$ is finite dimensional and 
>$$\text{dim }V=\text{dim } \text{null }T+\text{dim }\text{range }T$$