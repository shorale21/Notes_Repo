>[!example] Definition: Neuron
>A container for a value, often fitted to the sigmoid to be between 0 and 1.
>
>These make up each layer of the network.
>The final layer will be a layer of neurons that represent your possible outputs.

^45e85c

The "brightest" neuron of the output layer is the reached output.

>[!example] Defintion: Connection
>The connection between two neurons in the network.
>Each connection has a weight associated with it

Suppose your first layer has neurons with values $a_1,\dots,a_n$, and your second layer has $m$ neurons.
The way to calculate the $j^{th}$ neuron is to compute the weighted sum using the connections. Each of the $m$ neurons has $n$ connections with the first layer, corresponding to $n$ weights. Thus there are $m\cdot n$ weights in total for the second layer.
For the $j^{th}$ neuron in the second layer, the activation, $a_j^{(1)}$, will be the sum
$$a_j^{(1)}=w_{j,1}a^{(0)}_1+\cdots+w_{j,n}a^{(0)}_n+b_j$$
Where $w_{j,k}$ corresonds to the weight associated with the connection between the $k^{th}$ neuron in the first layer and the $j^{th}$ neuron in the second layer, and $b_j$ is called the bias, a chosen value to limit the active state of neurons.
We might then apply the sigmoid to limit the value.
>[!example] The Sigmoid Function
>This function maps any real number to a number between zero and one.
>Very negative numbers are mapped close to zero and very positive numbers are mapped close to one.
>$$\sigma:\mathbb{R}\rightarrow\mathbb{R}(0,1) = \frac{1}{1+e^{-x}}$$

It is useful to package the weights in a matrix, and multiply it by the vector of activation values, then adding the bias vector (of course then using the sigmoid).
$$\textbf{W}=\begin{bmatrix}
w_{0,0} & \cdots & w_{0,n}\\
\vdots & & \vdots\\
w_{m,0} & \cdots & w_{m,n}
\end{bmatrix}$$
$$\vec{a}^{(0)}=\begin{bmatrix}
a^{(0)}_0\\
\vdots\\
a^{(0)}_n
\end{bmatrix}$$
$$\vec{b}=\begin{bmatrix}
b_0\\
\vdots\\
b_n
\end{bmatrix}$$
This gives an equation:
$$\vec{a}^{(1)}=\sigma(\textbf{W}\space\vec{a}^{(0)}+\vec{b})$$
This is the equation to calculate the next layer of activations.