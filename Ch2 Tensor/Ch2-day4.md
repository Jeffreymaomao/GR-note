Why $\displaystyle X = X^{a}\frac{\partial}{\partial x^{a}}$? For example a transformation between two 2-D system:



<u>FIg</u>


$$
\vec{r} = \sum x_{i}\hat{e}_i = \sum x'_i \hat{e}'_i
$$
Since $x'_i = \vec{r}\cdot \hat{e}'_{i}$, so that 
$$
\begin{aligned}
x'_1 
&= \vec{r}\cdot \hat{e}'_{1} \\
&= \vec{r}\cdot \left(\cos\theta\,\hat{e}_1+\sin\theta\,\hat{e}_1\right) \\
&= \cos\theta\,x_1+\sin\theta\,x_2\\[2ex]
x'_2
&= \vec{r}\cdot \hat{e}'_{2} \\
&= \vec{r}\cdot \left(-\sin\theta\,\hat{e}_1+\cos\theta\,\hat{e}_1\right) \\
&= -\sin\theta\,x_1+\cos\theta\,x_2\\
\end{aligned}
$$
That is 
$$
\begin{pmatrix}
x'_1\\x'_2
\end{pmatrix}
=
\begin{pmatrix}
\cos\theta&\sin\theta\\
-\sin\theta&\cos\theta
\end{pmatrix}
\begin{pmatrix}
x_1\\x_2
\end{pmatrix}
\quad\text{or}\quad
\begin{pmatrix}
x_1\\x_2
\end{pmatrix}
=
\begin{pmatrix}
\cos\theta&-\sin\theta\\
\sin\theta&\cos\theta
\end{pmatrix}
\begin{pmatrix}
x'_1\\x'_2
\end{pmatrix}
$$
Last, we have
$$
\begin{aligned}
\frac{\partial}{\partial x'_1} 
&= \left(\frac{\partial x_1}{\partial x'_1}\right)\frac{\partial}{\partial x_1}
	+\left(\frac{\partial x_2}{\partial x'_1}\right)\frac{\partial}{\partial x_2}\\
&= \cos\theta\frac{\partial}{\partial x_1} + \sin\theta\frac{\partial}{\partial x_2}\\[2ex]
\frac{\partial}{\partial x'_2} 
&= \left(\frac{\partial x_1}{\partial x'_2}\right)\frac{\partial}{\partial x_1}
	+\left(\frac{\partial x_2}{\partial x'_2}\right)\frac{\partial}{\partial x_2}\\
&= -\sin\theta\frac{\partial}{\partial x_1} + \cos\theta\frac{\partial}{\partial x_2}
\end{aligned}
$$
**Example**: Tangent vector field on a curve $\mathcal{C}$:

<u>Fig</u>

(e.g. a curve in $\mathbb{R}^2$: $x^{1}=\cos u$, $x^{2}=\sin u$). We know that
$$
X = X^{a}\frac{\partial}{\partial x^{a}}
$$
then how to describe $X^{a}$ depend on curve $\mathcal{C}$ (relation with $\partial/\partial u$)?

Consider a function on $\mathcal{C}$: $f(x^{a}(u))$, rate of change of $f$ is
$$
\frac{df}{du} = \frac{\partial}{\partial x^{a}}\left(\frac{\partial x^{a}}{\partial u}\right).
$$
That is the derevative
$$
\frac{d}{du} =\left(\frac{\partial x^{a}}{\partial u}\right)\frac{\partial}{\partial x^{a}} = X^{a}\frac{\partial}{\partial x^{a}}
$$

#### Two vector field

For a vector field $X\displaystyle  = X^{a}\frac{\partial}{\partial x^{a}}$

<u>FIg</u>

where $\displaystyle X\bigg|_{p} = X^{a}(p)\frac{\partial}{\partial x^{a}}\bigg|_p$. Then consider a new vector field $\displaystyle Y = Y^{a}\frac{\partial}{\partial x^{a}}$

**Claim**: (How to generate a vector field by this two vector fields)

1. $X+Y=Z$  is a vector field: $\displaystyle X+Y=\left(X^{a}+Y^{a}\right)\frac{\partial}{\partial x^{a}}$

2. Lie bracket $[X,Y] = Z$ is a vector field, where 
    $$
    Z^{a} = X^{b}\frac{\partial Y^{a}}{\partial x^{b}} - Y^{b}\frac{\partial X^{a}}{\partial x^{b}},
    $$
    then we can check $\displaystyle X'^{a} = \frac{\partial x'^{a}}{\partial x^{b}}Z^{b}$ holds.

> Also, the Lie bracket $[X,Y]$ satisfies
>
> 1. $[X,Y] = -[Y,X]$ (skew-symmetric)
> 2. $[XY,Z] = X[Y,Z] + [X,Z]Y$ (Leibnitz rule)
> 3. $[X,[Y,Z]] + [Y,[Z,X]]+[X,[X,Y]] = 0$



## Tensor Calculus

How to define a partial derivative of a tensor field? Recall the definition of derivative in calculus:

> **Definition:** 
> $$
> \frac{df}{dx} = \lim_{\epsilon\to0}\frac{f(x+\epsilon) - f(x)}{\epsilon}
> $$

The question is: Is the subtraction meaniful? In $\mathbb{R}^{2}$, $x+\epsilon$ and $x$ are using the same coordinate. However, the coordinate in manifold using the different coordinate system.

<u>Fig</u>

In other words,

> **Problem 1**
>
> $f_{p}$ and $f_{a}$ refer to different coordinate system.

and 

> **Problem 2**
>
> If $\partial_b X^{a}$ is a $(1,1)$-type tensor, 
> $$
> \partial'_{b} X'^{a} = \left(\frac{\partial x'^{a}}{\partial x^{c}}\right)\left(\frac{\partial x^{d}}{\partial x'^{b}}\right) \partial_{d}X^{c}
> $$
> must be the $(1,1)$-type tensor as well.

Consider ordinary derivative
$$
\begin{aligned}
\partial'_{c} X'^{a}
&= \partial'_{c}\left(\frac{\partial x'^{a}}{\partial x^{b}}X^{b}\right)\\
&= \frac{\partial x'^{a}}{\partial x^{b}}\left(\partial'_{c}X^{b}\right)
	+ \left(\partial'_{c}\frac{\partial x'^{a}}{\partial x^{b}}\right)X^{b}\\
&= \frac{\partial x'^{a}}{\partial x^{b}}\frac{\partial x^{d}}{\partial x'^{c}}\left(\partial_{d}X^{b}\right)
	+ \left(\frac{\partial^2 x'^{a}}{\partial x'^{c}x^{b}}\right)X^{b}\\
&= \underbrace{\frac{\partial x'^{a}}{\partial x^{b}}\frac{\partial x^{d}}{\partial x'^{c}}\left(\partial_{d}X^{b}\right)}_{\text{This is what we want.}}
	+ \underbrace{\left(\frac{\partial^2 x'^{a}}{\partial x'^{c}x^{b}}\right)X^{b}}_{\text{This is what we unwant term.}}\\
\end{aligned}
$$
There are two approachs 

1. Lie derivative
2. introducting a *connetion* to defone derivative.

### $\odot$ Lie derivative

- integral curve

    <u>FIg family of curve</u>

Consider a differentiation of a tensor $T^{a}$ along the curve $x^{a}(u)$.

> **key point**: move/drag $T^{a}\bigg|_{p}$ to point $Q$.

Lie first define express the $T'^{a}$ by
$$
T^{a}\to T'^{a}(x') = \left(\frac{\partial x'^{a}}{\partial x^{b}}\right) T^{b}
$$
Notice $x'^{a}\simeq x^{a} + \delta u X^{a}$, then $\displaystyle \frac{\partial x'^{a}}{\partial x^{b}} = \delta^{a}_{b} + \delta u \partial_{b} x^{a}$, so that

Lie define the dragged of $T^{a}(x)$​ by
$$
\begin{aligned}
T^{a}\to T'^{a}(x') &= \left(\frac{\partial x'^{a}}{\partial x^{b}}\right) T^{b}\\
&= \left(\delta^{a}_{b} + \delta u \partial_b X^{a}\right)T^{b}(x)\\
&= T^{a}(x) + \delta u \partial_b X^{a}T^{b}(x),
\end{aligned}
$$
and the *Lie derivative* is
$$
\begin{aligned}
L_{x} T^{a} 
&= \lim_{\delta u \to 0} \frac{T^{a}(x') - T'^{a}(x')}{\delta u},\text{point at $Q-$dragged point}\\
&= \lim_{\delta u \to 0} \frac{T^{a}(x+\delta X^{a}) - \left(T^{a}(x)+\delta u \partial_{b}X^{a}\right) T^{b}(x)}{\delta u}\\
&= \lim_{\delta u\to 0} \frac{\left(T^{a}(x) + \delta u \partial_{b}T^{a}X^{b}\right) - \left(T^{a}(x)+\delta u \partial_{b} X^{a} T^{b}\right)}{\delta u}\\
&= X^{b}\partial_{b}T^{a} - \partial_{b}X^{a}T^{b}
\end{aligned}
$$
Check $L_{x} T^{a} = x^{b}\partial_{b}T^{a} - \partial_{b}X^{a}T^{b}$ is a $(1,0)$-type tensor. 

> **Example**:
> $$
> L_{x}T^{ab} = X^{c}\partial_{c} T^{ab} - \partial_{c} X^{a}T^{cb} - \partial_{c}X^{b}T^{ac}
> $$
> Try $L_{x}T^{abc}$ and $L_{x}X_{a}$

> **Example** (scalar)
> $$
> \lim_{\delta u \to 0} \frac{\phi(x'^{a}) - \phi^{\rm dragged}(x'^{a})}{\delta u} = \lim_{\delta u \to 0} \frac{\phi(x^{a}+\delta u X^{a}) - \phi(x^{a})}{\delta u} = X^{a}\partial_{a}\phi
> $$
