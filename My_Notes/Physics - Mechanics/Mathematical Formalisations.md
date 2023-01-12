## Coordinate Transforms and Basic Structures
>[!example] Concept of a Scalar
>A **Scalar** is a quantity that is invariant under coordinate transformations
>For an example, imagine a particle in the $x, y$ coordinate axes, so that we can express the particle as the ordered pair $(x,y)$
>Say that this particle has a mass $M$ that can then be expressed as $M(x,y)$, denoting the mass of the particular particle
>If the coordinate system transforms, the mass will of course remain the same and therefore is *invariant*
>
>Consider a coordinate transform such as $x'_i=\sum\limits_{j}\lambda_{ij}x_{j}$
>If, under such a transformation, a quantity $\phi$ is unaffected, then $\phi$ is called a **Scalar**

^6a1758


>[!example] Coordinate Transformations
>Take a vector in a simple coordinate system, $X=(x_1,x_2,...,x_n)$
>Now say we define a new coordinate system in which $X=(x'_1,x'_2,...,x'_n)$
>
>Let us also notate the angle between two axes as $(x_i,x_j)$
>Now, we define the **Directional Cosines** of each pair of axes to be $\lambda_{ij}=\cos(x'_i,x_j)$
>
>Now we can define a foraward transform and an inverse transform like so:
>$$x'_i=\sum\limits_{j=1}^{n}\lambda_{ij}x_{j}$$
>$$x_{i}=\sum\limits_{j=1}^{n}\lambda_{ji}x'_{j}$$
>It's also convenient to arrange the directional cosines into a matrix:
>$$\lambda=\begin{pmatrix}
\lambda_{11} & \lambda_{12} & \cdots & \lambda_{1n}\\
\lambda_{21} & \lambda_{22} & \cdots & \lambda_{2n}\\
\vdots & & & \vdots\\
\lambda_{n1} & \lambda_{n2} & \cdots & \lambda{nn} 
\end{pmatrix} $$
>This is calld the **Transformation Matrix**
>>[!definition]- Example of a Coordinate Transformation
>>Consider a point $P$ with coordinates $(x_1,x_2,x_3)$ with respect to a certain coordinate system
>>
>>Now consider a new coordinate system, created by rotating the original system
>>Let $P$ in the new coordinate system be at $(x'_1,x'_2,x'_3)$.
>>
>>The new coordinate $x'_1$ is the sum of the projection of $x_1$ onto the $x'_1$-axis plus the projection of $x_2$ onto the $x'_1$-axis
>>
>>![[Thornton_1.2.png|350]]
>>
>>That is,
>>$$\begin{align*}
x'_{1}&=x_{1}\cos(\theta)+x_{2}\sin(\theta)\\\\
&=x_{1}\cos(\theta)+x_{2}\cos\bigg(\frac{\pi}{2}-\theta\bigg)
\end{align*}$$
>>The coordinate $x'_2$ is a sum of similar projections.
>>
>>We write the angle between the $x'_1$-axis and the $x_1$-axis as $(x'_1,x_1)$
>>
>>Let us also define the set of numbers $\lambda_{ij}=\cos(x'_i,x_j)$
>>d
>>Now we can define our transformations in terms of this new value.
>>$$\begin{cases}
x'_{1}=\lambda_{11}x_{1}+\lambda_{12}x_{2}+\lambda_{13}x_{3} \\\\
x'_{2}=\lambda_{21}x_{1}+\lambda_{22}x_{2}+\lambda_{23}x_{3} \\\\
x'_{3}=\lambda_{31}x_{1}+\lambda_{32}x_{2}+\lambda_{33}x_{3}
\end{cases}$$
>>Or, in better notation:$$x_{i}=\sum\limits_{j=1}^{3}\lambda_{ji}x'_{j}$$
>
>**Properties of Direction Cosines** (let the angles between axes and a line on the origin be $\alpha,\beta,\gamma$)
>- $\cos^{2}(\alpha)+\cos^{2}(\beta)+\cos^{2}(\gamma)=1$
>- If there are two lines, with angles $\alpha,\beta,\gamma,\alpha',\beta',\gamma'$, then the angle between them, $\theta$, is given by $\cos(\theta)=\cos(\alpha)\cos(\alpha')+\cos(\beta)\cos(\beta')+\cos(\gamma')\cos(\gamma')$
>- $\sum\limits_{j}\lambda_{ij}\lambda_{kj}=0,\quad i\neq k$
>- $\sum\limits_{j}\lambda_{ij}\lambda_{kj}=1,\quad i=k$
>- These can be combined into the **kronecker delta**: $\sum\limits_{j}\lambda_{ij}\lambda_{kj}=\delta_{ik}$
>- $\sum\limits_{i}\lambda_{ij}\lambda_{ik}=\delta_{jk}$

>[!example] Definition: Permutation Symbol
>The symbol $\epsilon_{ijk}$ is called the **permutation symbol** and has the following properties:
>$$$$

^de9a0c

## Matrix Operations
**Matrix Multiplication**
The multiplication of matrx $\textbf{A}$ and a matrix $\textbf{B}$ is defined only if the number of *columns* of $\textbf{A}$ is equal to the number of *rows* $\textbf{B}$

The product $\textbf{A}\textbf{B}$ is given by:$$\textbf{C}=\textbf{A}\textbf{B}$$$$C_{ij}=[\textbf{A}\textbf{B}]_{ij}=\sum\limits_{k}A_{ik}B_{kj}$$

Matrix Multiplication is not commutative, meaning in general, $\textbf{A}\textbf{B}\neq\textbf{B}\textbf{A}$

Matrix Multiplication is associative, $[\textbf{A}\textbf{B}]\textbf{C}=\textbf{A}[\textbf{B}\textbf{C}]$

**Transposition**
A **transposed** matrix is derived by interchanging rows and columns, denoted by $\textbf{A}^{t}$

$$\lambda_{ij}^{t}=\lambda_{ji}$$
Evidently, $$(\lambda^t)^t=\lambda$$

>[!example] Definition: Vector
>A vector is abstractly defined as a linear combination of basis vectors, ie. a list of numbers contained in a space.
>Mathematically, if we have basis vectors $\hat{e}_i$, then a vector $V$ would be defined as$$V=\sum\limits_{i}V_i\hat{e}_i$$
>In cartiesian coordinates, we use the basis vectors $\hat{x},\hat{y},\hat{z}$, so a vector in this space would be $$V=X\hat{x}+Y\hat{y}+Z\hat{z}$$where $X,Y,Z$ are [[Mathematical Formalisations#^6a1758|Scalars]]
>If we have a coordinate transform of the type $x'_{i}=\sum\limits_{j}\lambda_{ij}x_j$, and a set of quantities $V_i$ is transformed using the matrix $\lambda$, resulting in these quantities being transformed, then the quantity $\textbf{V}=V_i$ is termed a **Vector**

^8a0889

^95af69
>[!example] Definition: Directional Cosines
>A **Directional Cosine** is defined as the cosine of the angle between two lines, usually one of them being an axis of the current coordinate system
>
>For an example with vectors $\textbf{A}$ and $\textbf{B}$, $A_1/A$ is the cosine of the angle $\alpha$ between $\textbf{A}$ and the $x_1$-axis
>This means it is the **Directional Cosine** $\Lambda^{A}_{1}$
>
>In general, $A_i/A$ and $B_i/B$ are the direction cosines $\Lambda_{i}^{A}$ and $\Lambda_{i}^{B}$

^4076d2

## Vector and Scalar Operations
In the following, $\textbf{A}$ and $\textbf{B}$ are [[Mathematical Formalisations#^8a0889|vectors]] and $\phi$, $\psi$, and $\xi$ are [[Mathematical Formalisations#^6a1758|scalars]]

**Addition**
$$\begin{align*}
A_i+B_i&=B_i+A_{i} & \quad\quad\text{Commutative Law}\\\\
A_i+(B_i+C_i)&=(A_i+B_i)+C_{i} & \quad\quad\text{Associative Law}\\\\
\phi+\psi &=\psi+\phi & \text{Commutative Law}\\\\
\phi+(\psi+\xi)&=(\phi+\psi)+\xi & \text{Associative Law} 
\end{align*}$$

**Scalar Multiplication**
$$\begin{align*}
\xi\textbf{A}&=\textbf{B}\quad\text{is a vector}\\
\xi\phi&=\psi\quad\text{is a scalar}
\end{align*}$$

**Scalar Product**
The scalar product between two vectors is defined to be$$\textbf{A}\cdot\textbf{B}=\sum\limits_{i}A_iB_i$$sometimes called the dot product

In addition,$$\textbf{A}\cdot\textbf{B}=AB\cos(\textbf{A},\textbf{B})$$ where $A$ and $B$ are the respective magnitudes of the vectors

The Scalar Product can be used to find the magnitude of the vector as$$|\textbf{A}|=\sqrt{\textbf{A}\cdot\textbf{A}}$$

The Scalar Product obeys the commutative and distributive laws:
$$\begin{align*}
\textbf{A}\cdot\textbf{B}&=\textbf{B}\cdot\textbf{A}\\\\
\textbf{A}\cdot(\textbf{B}+\textbf{C})&=(\textbf{A}\cdot\textbf{B})+(\textbf{A}\cdot\textbf{C})
\end{align*}$$

**Direction Cosines**
Using [[Mathematical Formalisations#^4076d2|direction cosines]],
$$\frac{\textbf{A}\cdot\textbf{B}}{AB}=\sum\limits_{i}\Lambda_{i}^{A}\Lambda_{i}^{B}$$
The sum $\sum\limits_{i}\Lambda_{i}^{A}\Lambda_{i}^{B}$ is the cosine of the angle between $\textbf{A}$ and $\textbf{B}$

**Vector Product**
(sometimes called the *cross product*)

The vector product of two vectors acts like a vector, although we can easily calculate the scalar magnitude of it

The vector product is notated $\textbf{A}\times\textbf{B}=\textbf{C}$, and it is given by
$$\textbf{C}_i=\sum\limits_{jk}\epsilon_{ijk}A_{j}B_{k}$$
where $\epsilon_{ijk}$ is the [[Mathematical Formalisations#^de9a0c|permutation symbol]].
As well as this, there is an identity similar to the [[Mathematical Formalisations#^8a0889|scalar product]]:
$$C=AB\sin{\theta}$$

**Differentiation of Vectors**

The derivative of a vector *is* a vector. Each component is differentiated like the following:
$$\frac{d}{dt}\textbf{A}(t)=\sum\limits_{i}\frac{d}{dt}(A_{i})\hat{e}_i$$

Here are some rules for differentiation of vectors:
$$\frac{d}{ds}(\textbf{A}\cdot\textbf{B})=\textbf{A}\cdot\frac{d\textbf{B}}{ds}+\frac{d\textbf{A}}{ds}\cdot\textbf{B}$$
$$\frac{d}{ds}(\textbf{A}\times\textbf{B})=\textbf{A}\times\frac{d\textbf{B}}{ds}+\frac{d\textbf{A}}{ds}\times\textbf{B}$$

>[!example] Definition: Scalar Product of Vectors
>The scalar product between two [[Mathematical Formalisations#^8a0889|vectors]] is defined to be$$\textbf{A}\cdot\textbf{B}=\sum\limits_{i}A_iB_i$$sometimes called the dot product
>
>In addition,$$\textbf{A}\cdot\textbf{B}=AB\cos(\textbf{A},\textbf{B})$$ where $A$ and $B$ are the respective magnitudes of the vectors

^6abdd3

>[!example] Definition: Vector Product of two Vectors
>
>The vector product (sometimes called the *cross product*) of two vectors acts like a vector, although we can easily calculate the scalar magnitude of it
>
>The vector product is notated $\textbf{A}\times\textbf{B}=\textbf{C}$, and it is given by
$$\textbf{C}_i=\sum\limits_{jk}\epsilon_{ijk}A_{j}B_{k}$$
where $\epsilon_{ijk}$ is the [[Mathematical Formalisations#^de9a0c|permutation symbol]].
As well as this, there is an identity similar to the [[Mathematical Formalisations#^6abdd3|scalar product]]:
$$C=AB\sin{\theta}$$

## Two Dimensional Polar Coordinates
The normal $x$ and $y$ coordinates are known as **Rectangular Coordinates**
Given these values, we can calculate a new, rotation based system called **Polar Coordinates**
>[!example] Definition: Polar Coordinates
>Polar Coordinates are a curvilinear system of coordinates based on rotation. In two dimensions, polar coordinates are based on a radius and an angle. 
>Coordinates in this system are given by $(\phi,r)$
>Given cartesian coordinates, we can transform to polar coordinates with the following rules:
>$$\begin{matrix*}
x=r\cos{\phi} & & r=\sqrt{x^{2}+y^{2}}\\
y=r\sin{\phi} & & \phi=\arctan(y/x)
\end{matrix*}$$
>
>Polar Coordinates have two unit vectors: $\hat{\textbf{r}}$ and $\hat{\phi}$

^ae1334

