# Complex Exponentials

>[!example] Euler's Formula and Relations
>$$e^{ix}=\cos(x)+i\sin(x)$$
>$$\cos(x)=\frac{e^{ix}+e^{-ix}}{2}$$
>$$\sin(x)=\frac{e^{ix}-e^{-ix}}{2i}$$
>>[!definition]- Proof
>>We know the taylor series for $e^x$ is given by
>>$$e^x=1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\cdots=\sum\limits_{n=0}^{\infty}\frac{x^n}{n!}$$
>>We now attempt to evaluate $e^{iz}$ where $i=\sqrt{-1}$ and $z$ is a constant.
>>$$e^{iz}=1+iz+\frac{(iz)^2}{2!}+\frac{(iz)^3}{3!}+\cdots$$
>>Since $i^2=-1$, we can evaluate some of these expressions
>>$$e^{iz}=1+iz-\frac{(z)^2}{2!}-\frac{(iz)^3}{3!}+\cdots$$
>>Now we can divide this into two parts, an imaginary and real part
>>$$e^{iz}=\bigg[1-\frac{z^2}{2!}+\frac{z^4}{4!}+\cdots\bigg]+i\bigg[z-\frac{z^3}{3!}+\frac{z^5}{5!}+\cdots\bigg]$$
>>We can find the series represented by this, and they become recongnizable
>>$$e^{iz}=\sum\limits_{n=0}^{\infty}\frac{z^{2n}(-1)^n}{(2n)!}+i\sum\limits_{n=0}^{\infty}\frac{z^{2n+1}(-1)^n}{(2n+1)!}$$
>>These taylor series are of course commonly known as trigonometric and so we can replace them:
>>$$e^{iz}=\cos{(z)}+i\sin{(z)}$$
^8e81f7

Based on Euler's Formula, raising $e$ to the power of a complex number geometrically indicates a rotation around the origin. 
