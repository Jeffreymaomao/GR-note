# Tensors

>  Tensors is *generalization of vector*.

- What;s tensors
- Tensors Algebra
- Tensor differentiation
- Tensor integration

## Introduction

- **Newtonian mechanics** $\Rightarrow$ ODE
- **Quantum physics** $\Rightarrow$ Linear Algebra
- **Relativity** $\Rightarrow$ Tensor Calculus

### Vector

> Ex.
>
> <u>Ch2 - Fig2</u>
>
> $\vec{A}$ is a vector
> $$
> \vec{A} = A_1\hat{e}_1 + A_2 \hat{e}_2 = A'_1\hat{e}'_1 + A'_2 \hat{e}'_2
> $$
> and
> $$
> \begin{pmatrix}
> A'_1\\A'_2
> \end{pmatrix}
> =
> R(\theta)
> \begin{pmatrix}
> A_1\\A_2
> \end{pmatrix}
> $$

> **Definition**
>
> A vector $\vec{A}$ is an object that tranforms as the same as $\vec{r}$​ under axis rotation.

In matrix notation:
$$
A_i' = \sum_{j=1}^{n}R_{ij}(\theta) A_j,\quad \text{in $\mathbb{R}^n$}
$$
We denote as 
$$
A'_i = R_{ij}A_j,
$$
also called Einstein's convention (*Summing over repested indeces.*)

### Tensor

**Definition**

A rank-2 tensor $A_{ij}$ is an object such that each index transforms like a vector.

i.e.
$$
A'_{ij} = R_{ik}R_{g\ell}A_{k\ell}
$$

In general, a rank-$n$ tensor $A_{i_1,\ldots,i_n}$ transformation as 
$$
A'_{i_1,\ldots,i_n} = R_{i_1,j_1}R_{i_2,j_2}\cdots R_{i_n,j_n}\cdot A_{j_1,\ldots,j_n}
$$

> Rmk:
>
> - In $\mathbb{R}^{n}$, $\{\hat{e}_1,\hat{e}_2,\ldots,\hat{e}_n\}$ are constant basis.
>
> - In polar coordinate system, basis are not constant
>
>     <u>Ch1 - Fig 2 polar</u>

## Manifold and coordinate

> Manifold (mfld) 流形 

What is the dimension of a manifold $M$ ?

<u>Fig3 - A manifold locally likes R^n</u>

**Definition**

An $n$-dimension manifold $M$ is something which locally look like $\mathbb{R}^n$.
$$
\begin{aligned}
x^{i} : 
&U \to \mathbb{R}^n\\
&p \mapsto  x(p)
\end{aligned}
$$

> Ex.
>
> $M = S^2$ (Two sphere)
>
> <u>Fig4 - sphere</u>

> Rmk.
>
> If $(x^{1},x^{2},\ldots,x^{n})$ be a set of $n$ coordinates , which is non-degenerate if
> $$
> p \longleftrightarrow (x^{1},x^{2},\ldots,x^{n})
> $$
> is 1-1 or *one-to-one mapping*.
>
> e.g.
>
> <u>Fig4 - degenerate sphere</u>

In overlapping region

<u>Fig5 - overlapping</u>

> Ex. **stereo graphic projection**
>
> spherical coordinate $\theta,\varphi$, notice that it is singular at $\theta = 0$ (north pole) and $\theta = \pi$ (south pole).
> $$
> x^2+y^2+z^2=1
> $$
> <u>Fig6 - projection</u>
>
> - $U_N$:
>     $$
>     \begin{aligned}
>     &(x,y,z-1) = \lambda (X,Y,-1)\\
>     &\Rightarrow \frac{x}{X} = \frac{y}{Y} = \frac{z-1}{-1} = \lambda\\
>     &\Rightarrow \begin{cases}
>     \displaystyle X= \frac{x}{\lambda} = \frac{x}{1-z}\\
>     \displaystyle Y= \frac{y}{\lambda} = \frac{y}{1-z}
>     \end{cases}
>     \end{aligned}
>     $$
>
> - $U_S$:
>     $$
>     \begin{aligned}
>     &(x,y,z-1) = \lambda (X,Y,+1)\\
>     &\Rightarrow \frac{x}{X} = \frac{y}{Y} = \frac{z+1}{+1} = \lambda\\
>     &\Rightarrow \begin{cases}
>     \displaystyle X= \frac{x}{\lambda} = \frac{x}{1+z}\\
>     \displaystyle Y= \frac{y}{\lambda} = \frac{y}{1+z}
>     \end{cases}
>     \end{aligned}
>     $$
>
> Then, the manifold $M = U_{N}\cup U_{S}$, where $U_{N}\cap U_{S}=\phi$. And we called
>
> -  Two subset $U_N$ and $U_S$ to be a *patch* of covering (覆蓋).
> - The set $\{U_N,U_S\}$ is the Altas.
>
> 
>
> **Claim**
>
> For a point
> $$
> p\in U_{N}\cap U_S
> $$
> we have
> $$
> \begin{cases}
> \displaystyle X' = \frac{X}{X^2+Y^2}\\
> \displaystyle Y' = \frac{Y}{X^2+Y^2}
> \end{cases}
> $$
> coordinate transformation between 2 system.

#### Tensors on $M$

The tensors on $M$ are geometric quantities that obey coordinate transformation in overlapping region.

#### Curve on $M$

<u>Fig7 - curves on M</u>

In general, an $m$-dimension object in $M$ can be parametrized by
$$
x^{a} = x^{a}\left(u^1,u^2,\ldots,u^m\right), \quad a = 1,2,\ldots,n
$$

>  In particular, if $m=n-1$​, i.e.
>  $$
>  x^{a} = x^{a} \left(u^1,u^2,\ldots,u^{n-1}\right), \quad a = 1,2,\ldots,n
>  $$
>  is a *hypersurface*. We also using a function $f(x^{1},x^{2},\ldots,x^{n})=0$.
