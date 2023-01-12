# Frobenius Theory
We have seen how [[Series Sols. Around a Regular Singular Point#^6c0c37|Frobenius Series]] can be used to solve differential equations of the form$$x^{2}y''+xp(x)y'+q(x)y=0$$
We want to extend this theorem to when the roots differ by an integer.

>[!example] Establishing one Frobenius Solution
>We assume that $x=0$ is a [[Series Sols. Around a Regular Singular Point#^8ff73a|regular singular point]], and so it follows that $p$ and $q$ are analytic at $x=0$. We can then write:$$p(x)=\sum\limits_{n=0}^{\infty}p_{n}x^{n},\quad q(x)=\sum\limits_{n=0}^{\infty}q_{n}x^{n}$$for $|x|<R$. Consequently, the differential equation can then be written as$$x^{2}y''+x\sum\limits_{n=0}^{\infty}p_{n}x^{n}y'+\sum\limits_{n=0}^{\infty}q_{n}x^{n}y=0$$
>We try for a Frobenius solution, and therefore let$$y(x)=x^{r}\sum\limits_{n=0}^{\infty}a_{n}x^{n},\quad a_{0}\neq0$$
>where $r$ and $a_n$ are constants to be determined. Differentiating $y$ twice yields$$y'=\sum\limits_{n=0}^{\infty}(r+n)a_{n}x^{r+n-1},\quad y''=\sum\limits_{n=0}^{\infty}(r+n)(r+n-1)a_nx^{r+n-2}$$
>We can now substitute back into the differential equation:$$\sum\limits_{n=0}^{\infty}(r+n)(r+n-1)a_nx^{n}+\Bigg[\sum\limits_{n=0}^{\infty}p_{n}x^{n}\Bigg]\Bigg[\sum\limits_{n=0}^{\infty}(r+n)a_{n}x^{n}\Bigg]+\Bigg[\sum\limits_{n=0}^{\infty}q_{n}x^{n}\Bigg]\Bigg[\sum\limits_{n=0}^{\infty}a_{n}x^{n}\Bigg]=0$$ 
>$$\sum\limits_{n=0}^{\infty}(r+n)(r+n-1)a_nx^{n}+\sum\limits_{n=0}^{\infty}\Bigg[\sum\limits_{k=0}^{n}p_{n-k}x^{n-k}(k+r)a_{k}x^{k}\Bigg]+\sum\limits_{n=0}^{\infty}\Bigg[\sum\limits_{k=0}^{n}q_{n-k}x^{n-k}a_{k}x^{k}\Bigg]=0$$
>Which can be written as$$\sum\limits_{n=0}^{\infty}\bigg\{(r+n)(r+n-1)a_{n}+\sum\limits_{k=0}^{n}\Big[p_{n-k}(k+r)+q_{n-k}\Big]a_{k}\bigg\}x^{n}=0$$