# Laplace Transforms
Used for linear, constant coefficient, ordinary differential equations of the form:
$$ay''+by'+cy=F$$
These transforms are especially useful for periodic functions and piecewise functions.

>[!example] Definition: Laplace Transforms
>Let $f$ be a function defined on $[0, \infty)$. The Laplace Transform of $f$ is the function $F(s)$ defined as: $$F(s)=\int_{0}^{\infty}e^{-st}f(t)dt$$
>Provided that the improper integral converges. We denote the Laplace Transform of $f$ as $\mathcal{L}[f]$

^374085

We have determined the following Laplace Transforms: 
$$\displaylines{\mathcal{L}[t^n]=\frac{n!}{s^{n+1}},\:\:\:s>0 \\\mathcal{L}[e^{\alpha t}]=\frac{1}{s-\alpha},\:\:\:s>\alpha \\\mathcal{L}[cos(bt)]=\frac{s}{s^2 + b^2},\:\:\:s>0
\\\mathcal{L}[sin(bt)]=\frac{b}{s^2 + b^2},\:\:\:s>0}$$
Note that the Laplace Transform is a linear operator, meaning it follows this simple rule:$$\mathcal{L}[\alpha f(t)\:+\:\beta g(t)]=\alpha \mathcal{L}[f(t)]\:+\:\beta \mathcal{L}[g(t)]$$

>[!example] Definition: Piecewise Continuous
>A function $f$ is piecewise continuous on the interval $[a,b]$ if we can divide $[a,b]$ into a finite number of subintervals such that:
>1. $f$ is continuous on each subinterval
>2. $f$ approaches a finite limit as the endpoints of each subinterval are approached from within ^10c23f


General Table of Laplace Transforms:

| Function $f(t)$                                                            | Laplace Transform $F(s)$                                  |
| -------------------------------------------------------------------------- | --------------------------------------------------------- |
| $f(t)=t^n$, $n\:\ge\:0$                                                    | $F(s)=\frac{n!}{s^{n+1}},\:s\:>\:0$                       |     
| $f(t)=e^{at}$,  $a$ is constant                                            | $F(s)=\frac{1}{s-a},\:s\:>\:a$                            |     
| $f(t)=sin(bt)$,  $b$ is constant                                           | $F(s)=\frac{b}{s^{2}+ b^2},\:s\:>\:0$                     |     
| $f(t)=cos(bt)$,  $b$ is constant                                          | $F(s)=\frac{s}{s^{2}+ b^2},\:s\:>\:0$                     |     
| $f(t)=t^(-\frac{1}{2})$                                                    | $F(s)=\left(\frac{\pi}{s}\right)^{\frac{1}{2}},\:s\:>\:0$ |     
| $f(t)=u_a(t)\quad$([[Special Laplace Part 2#^08bff2\|unit step function]]) | $F(s)=\frac{1}{s}e^{-as}$                                 |     
| $f(t)=\delta(t-a)\quad$([[Special Laplace Part 2#^dc18ec\|dirac delta]])   | $F(s)=e^{-as}$                                            |    
| $f'(t)$                                                                    | $\mathcal{L}[f']=s\mathcal{L}[f]-f(0)$                    |     
| $f''(t)$                                                                   | $\mathcal{L}[f'']=s^2\mathcal{L}[f]-sf(0)-f'(0)$          |     
| $e^{at}f(t)$                                                               | $F(s-a)$                                                  |    
| $u_a(t)f(t-a)$                                                             | $e^{-as}F(s)$                                             |   
