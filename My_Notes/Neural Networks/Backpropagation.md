How do we train the neural network to make it produce desired results?

The first thing we need to do is to define a "cost" function of the entire network.
>[!example] Definition: Neural Network Cost Function
>Let the last layer of [[Structure of Neural Networks#^45e85c|neurons]] have activation values denoted $a_0,\dots,a_n$, and let the desired output for this test case be denoted $d_0,\dots,d_n$.
>The the cost function $C$ is defined as
>$$\sum\limits_{j=0}^{n}(a_j-d_j)^2$$
>The sum of the squares of the differences.

The cost function is essentially function of all the weights and biases, outputting a scalar representing how poorly the network performed.

## Gradient Descent Method
The gradient descent method is a numerical way to minimize an $n$ dimensional function.
It is analagous to "walking down a hill" in $n$-dimensional space.

Let $f(x_1,\dots,x_n)$ be a function of $n$ variables.
We compute the [[Vector Fields#^062dc4|gradient]] of the function. This is the direction of steepest ascent. The negative gradient gives the direction of steepest descent. 

We then step in this direction in order to "go downhill".
If we do this as many times as possible, recomputing the gradient every step, we get incredibly close to the minimum of the cost function.

## Backpropagation
This is the way neural networks learn.

Consider an extremely simple network, one where each layer has only one [[Structure of Neural Networks#^45e85c|neuron]].
Let's focus on the final two layers.

The last neuron's activation is $a^{(L)}$.
The desired output is $y$.
The second to last neuron's activation is $a^{(L-1)}$.

We can set up an equation then, where 
$$a^{(L)}=\sigma(w^{(L)}a^{(L-1)}+b^{(L)})$$
and we can represent the cost function:
$$C_{0}=(a^{(L)}-y)^2$$
Let's call the weighted sum
$$z^{(L)}=w^{(L)}a^{(L-1)}+b^{(L)}$$
for ease.

All of these are just numbers. We want  to calculate $\partial C_{0} /\partial w^{(L)}$. The chain rule can tell us that:
$$\frac{\partial C_0}{\partial w^{(L)}}=\frac{\partial z^{(L)}}{\partial w^{(L)}}\frac{\partial a^{(L)}}{\partial z^{(L)}}\frac{\partial C_{0}}{\partial a^{(L)}}$$
Now we compute the relevant derivatives:
$$\frac{\partial C_0}{\partial a^{(L)}}=2(a^{(L)}-y)$$
$$\frac{\partial a^{(L)}}{\partial z^{(L)}}=\sigma'(z^{(L)})$$
$$\frac{\partial z^{(L)}}{\partial w^{(L)}}=a^{(L-1)}$$
This gives the gradient for a single training example. We average it out for all training examples.
$$\frac{\partial C}{\partial w^{(L)}}=\frac{1}{n}\sum\limits_{k=0}^{n-1}\frac{\partial C_k}{\partial w^{(L)}}$$
We also take this gradient with respect to the biases, deriving $z$ with respect to $b$ instead of $w$. We then iterate backwards doing the same thing for all the previous layers.
How does this work?
The first iteration determines a set of "desired values" for the previous layer. Using these values, you can determine how to change the layer before that, and so on.

>[!example] Detailed Outline of the Backpropogation Method
>Suppose we have a neural network with $l$ layers including the input and output layers.
>Let the $i^{\text{th}}$ layer have $n_{i}$ neurons.
>Let the activation values of the $i^{\text{th}}$ layer be a vector $\vec{a}^{(i)}$
>Let the bias values of the $i^{\text{th}}$ layer be a vector $\vec{b}^{(i)}$
>Let the weight matrix of the $i^{\text{th}}$ layer be the $n_i$ by $n_{i-1}$ matrix $\textbf{W}^{(i)}$
>$$\textbf{W}^{(i)}=\begin{bmatrix}
>w_{0,0}^{(i)} & \cdots & w_{0,n_{i-1}}^{(i)}\\
>\vdots & & \vdots\\
>w_{n_{i},0}^{(i)} & \cdots & w_{n_{i},n_{i-1}}^{(i)} 
>\end{bmatrix}$$
>Therefore $\vec{a}^{(i)}=\textbf{W}^{(i)}\vec{a}^{(i-1)}+\vec{b}^{(i)}$
>
>Let's examine the last layer. 
>Suppose we have the desired output of the $j^{th}$ test case denoted to be $\vec{y}^{(j)}$. Note that $\vec{y}^{(j)}$ has $n_{l}$ elements
>Then the cost function for the single test case is
>$$C_{j}=\sum\limits_{k=0}^{n_{l}}(\vec{a}_{k}^{(l)}-\vec{y}_{k}^{(j)})^{2}$$
>Of course the total cost would be averaged over all the test cases.
>Our goal is to calculate the gradient of this cost function.
>In other words, we need to find:
>$$\nabla C_{j}=\bigg\langle\frac{\partial C_{j}}{\vec{a}_{0}^{(l)}},\dots,\frac{\partial C_{j}}{\vec{a}_{n_{l}}^{(l)}}\bigg\rangle$$and then average it over all test cases. 