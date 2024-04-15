> Recall: Lie derivative $L_{x}T^{a\ldots}_{b\ldots}$ is a tensor
>
> Recall: Covariant derivative $\nabla_{c} T^{a\ldots}_{b\ldots}$ is defined by  using a affine connection $\Gamma^{a}_{bc}$
>
> e.g. $\nabla_{c}X^{a} = \partial_{c}X^{a} + \Gamma^{a}_{bc} X^{b}$ is a $(1,1)$-tensor, the price we need to pay is that $\Gamma^{a}_{bc}$ is NOT a tensor.
> $$
> \nabla_{c} T = \lim_{\delta x_c \to 0} \frac{T(x')-T(x)}{\delta x_{c}}
> $$

Also, if we define
$$
T^{a}_{bc} = \Gamma^{a}_{bc} - \Gamma^{a}_{cb}
$$
is a *torsion tensor* which is a $(1,2)$-type tensor.

> If $\Gamma^{a}_{bc} = \Gamma^{a}_{cb}$, the the connection is *torsion free*.

### $\odot$ Affine Geodesics

> A curve induced by connection

$\nabla_{c} T^{a\ldots}_{b\ldots}$ covariant derivative along $\delta x_{c}$. Let $X^{a}$ be a tangent vector od $x^{a}(u)$, that is 
$$
X^{a} = \frac{dx^{a}}{du}
$$
<u>Fig</u>

then $X^{c}\nabla_{c} T^{a\ldots}_{b\ldots}$ is the covariant dericative along the curve, denoted by
$$
\frac{DT^{a\ldots}_{b\ldots}}{Du}
$$

> Rmk:
>
> $X^{a}$ is a $(1,0)$-type tensor, $\nabla_{c}T^{a\ldots}_{b\ldots}$ is a $(p,q+1)$-type tensor, $X^{c}\nabla_{c}T^{a\ldots}_{b\ldots}$ is a $(p,q)$-type tensor

> **Parallel transported tensor field** 
>
> <u>Fig</u>
>
> i.e.
> $$
> \frac{DT^{a\ldots}_{b\ldots}}{Du} = 0
> $$

#### Affien geodesic 

If a cure $x^{c}(u)$ is constructed such that the tangent vector $X^{a}$ at $x'$ is just the parallel transported vector from $x$. The curve is called *affine geodesic*.
$$
X^{c}\nabla_{c}X^{a} = \frac{DX^{a}}{Du} = 0
$$
<u>Fig</u>
$$
X^{c}\left(\partial_{c}X^{a} + \Gamma^{a}_{bc} X^{b}\right) = 0
$$
then 
$$
\frac{dx^{c}}{du}\frac{\partial X^{a}}{\partial x^{c}} + \frac{dx^{c}}{du}\Gamma^{a}_{bc} \frac{dx^b}{du} = 0
$$
Plugin $X^{a} = dx^{a}/du^2$, we have
$$
\frac{d^2x^a}{du^2} + \Gamma^{a}_{bc}\frac{dx^b}{du}\frac{dx^{c}}{du} = 0.
$$

> Rmk:
>
> - Given a $\Gamma^{a}_{bc}$, then $x^{a}(u)$ is determined.
> - After reparametrized $u\to \alpha u + \beta$, the geodesic still the same.
> - In equation $\displaystyle \frac{d^2x^a}{du^2} + \Gamma^{a}_{bc}\frac{dx^b}{du}\frac{dx^{c}}{du} = 0$,only the symmetric part $\Gamma^{a}_{bc}$ involved



## Riemann tensor

In Euclilean space, the derevative
$$
\partial_{a}\partial_{c}T = \partial_{c}\partial_{a}T
$$
 is commutative. However, in non-Euclilean space, is that
$$
\nabla_{a}\nabla_{c} T \stackrel{?}{=} \nabla_{c}\nabla_{a} T.
$$
In general, $\nabla_{a}\nabla_{c} T \neq \nabla_{c}\nabla_{a} T$, which is non-commutative. 

#### Second derivative

Consider
$$
\begin{cases}
\nabla_{d}X^{a} = \partial_{d}X^{a} + \Gamma^{a}_{bd}X^{b}\\
\nabla_{c}Y^{a}_{d} = \partial_{c}Y^{a}_{d} + \Gamma^{a}_{bc}Y^{b}_{d} - \Gamma^{b}_{dc}Y^{a}_{b}
\end{cases}
$$
we can calculate the second derivative
$$
\begin{aligned}
\nabla_{c}\nabla_{d} X^{a}
&= \nabla_{c} \left(\partial_{d}X^{a} + \Gamma^{a}_{bd}X^{b}\right)\\
&= \partial_{c}\left(\partial_{d}X^{a} + \Gamma^{a}_{bd}X^{b}\right)
	+ \Gamma^{a}_{bc}\left(\partial_{d}X^{b} + \Gamma^{b}_{ed}X^{e}\right) - \Gamma^{b}_{dc} \left(\nabla_{b}X^{a}\right)\\
&= \partial_{c}\partial_{d}X^{a} + \partial_{c}\left(\Gamma^{a}_{bd}X^{b}\right)
	+ \Gamma^{a}_{bc}\partial_{d}X^{b} + \Gamma^{a}_{bc}\Gamma^{b}_{ed}X^{e} - \Gamma^{b}_{dc} \left(\nabla_{b}X^{a}\right)\\
&= \partial_{c}\partial_{d}X^{a} 
+ X^{b}\partial_{c}\Gamma^{a}_{bd} + \Gamma^{a}_{bd}\partial_{c}X^{b}
	+ \Gamma^{a}_{bc}\partial_{d}X^{b} + \Gamma^{a}_{bc}\Gamma^{b}_{ed}X^{e} - \Gamma^{b}_{dc} \left(\nabla_{b}X^{a}\right)\\
\end{aligned}
$$

the the defference between second derivative, we have
$$
\begin{aligned}
\nabla_{c}\nabla_{d} X^{a} - \nabla_{d}\nabla_{c} X^{a} 
&= \left(\partial_{c}\partial_{d}X^{a} 
	+ X^{b}\partial_{c}\Gamma^{a}_{bd} + \Gamma^{a}_{bd}\partial_{c}X^{b}
	+ \Gamma^{a}_{bc}\partial_{d}X^{b} 
	+ \Gamma^{a}_{bc}\Gamma^{b}_{ed}X^{e} 
		- \Gamma^{b}_{dc} \nabla_{b} X^{a}\right)\\
	&\quad - \left(\partial_{d}\partial_{c}X^{a} 
	+ X^{b}\partial_{d}\Gamma^{a}_{bc} + \Gamma^{a}_{bc}\partial_{d}X^{b}
	+ \Gamma^{a}_{bd}\partial_{c}X^{b} 
	+ \Gamma^{a}_{bd}\Gamma^{b}_{ec}X^{e} 
		- \Gamma^{b}_{cd} \nabla_{b} X^{a}\right)\\
&= \left(\partial_{c}\partial_{d}-\partial_{d}\partial_{c}\right)X^{a} 
	+ X^{b}\left(\partial_{c}\Gamma^{a}_{bd}-\partial_{d}\Gamma^{a}_{bc}\right)\\
	&\quad+ \left(\Gamma^{a}_{bd}\partial_{c}X^{b} - \Gamma^{a}_{bc}\partial_{d}X^{b}\right)
	+\left(\Gamma^{a}_{bc}\partial_{d}X^{b} - \Gamma^{a}_{bd}\partial_{c}X^{b}\right)\\
	&\quad +\left(\Gamma^{a}_{bc}\Gamma^{b}_{ed}- \Gamma^{a}_{bd}\Gamma^{b}_{ec}\right)X^{e}
	- \left(\Gamma^{b}_{dc} - \Gamma^{b}_{cd}\right)\nabla_{b}X^{a}\\
&= \left(\partial_{c}\partial_{d}-\partial_{d}\partial_{c}\right)X^{a} 
	+ X^{b}\left(\partial_{c}\Gamma^{a}_{bd}-\partial_{d}\Gamma^{a}_{bc}\right)\\
	&\quad +\left(\Gamma^{a}_{bc}\Gamma^{b}_{ed}- \Gamma^{a}_{bd}\Gamma^{b}_{ec}\right)X^{e}
	- \left(\Gamma^{b}_{dc} - \Gamma^{b}_{cd}\right)\nabla_{b}X^{a}
\end{aligned}
$$
If $\Gamma^{a}_{bc}$ is torsion free $\Gamma^{a}_{bc} = \Gamma^{a}_{cb}$, the between second derivative is given by
$$
\begin{aligned}
\nabla_{c}\nabla_{d} X^{a} - \nabla_{d}\nabla_{c} X^{a}
&= \left(\partial_{c}\partial_{d}-\partial_{d}\partial_{c}\right)X^{a} 
	+ X^{b}\left(\partial_{c}\Gamma^{a}_{bd}-\partial_{d}\Gamma^{a}_{bc}\right)\\
	&\quad +\left(\Gamma^{a}_{bc}\Gamma^{b}_{ed}- \Gamma^{a}_{bd}\Gamma^{b}_{ec}\right)X^{e}
	- \left(\Gamma^{b}_{dc} - \Gamma^{b}_{cd}\right)\nabla_{b}X^{a}\\
&= \left(\partial_{c}\partial_{d}-\partial_{d}\partial_{c}\right)X^{a} 
	+ \left(\partial_{c}\Gamma^{a}_{bd}-\partial_{d}\Gamma^{a}_{bc}\right)X^{b}
	+\left(\Gamma^{a}_{bc}\Gamma^{b}_{ed}- \Gamma^{a}_{bd}\Gamma^{b}_{ec}\right)X^{e}
	- 0
\end{aligned}
$$
so that
$$
\begin{aligned}
\left(\nabla_{c}\nabla_{d} - \nabla_{d}\nabla_{c}\right)X^{a} 
&=\left(\partial_{c}\partial_{d}-\partial_{d}\partial_{c}\right)X^{a} 
	+ \left(\partial_{c}\Gamma^{a}_{bd}-\partial_{d}\Gamma^{a}_{bc}\right)X^{b}
	+\left(\Gamma^{a}_{bc}\Gamma^{b}_{ed}- \Gamma^{a}_{bd}\Gamma^{b}_{ec}\right)X^{e}\\
&=\left(\partial_{c}\partial_{d}-\partial_{d}\partial_{c}\right)X^{a} 
	+ \left(\partial_{c}\Gamma^{a}_{bd}-\partial_{d}\Gamma^{a}_{bc}\right)X^{b}
	+\left(\Gamma^{a}_{ec}\Gamma^{e}_{bd}- \Gamma^{a}_{ed}\Gamma^{e}_{bc}\right)X^{b}\\
&=\left(\partial_{c}\partial_{d}-\partial_{d}\partial_{c}\right)X^{a} 
	+ \left(\partial_{c}\Gamma^{a}_{bd}-\partial_{d}\Gamma^{a}_{bc} + \Gamma^{a}_{ec}\Gamma^{e}_{bd}- \Gamma^{a}_{ed}\Gamma^{e}_{bc}\right)X^{b}
\end{aligned}
$$
If we write
$$
\left(\nabla_{c}\nabla_{d} - \nabla_{d}\nabla_{c}\right)X^{a}  = \left(\partial_{c}\partial_{d} - \partial_{d}\partial_{c}\right)X^{a} + R^{a}_{bcd} X^{b},
$$
where we define the *Reimann tensor* is given by
$$
R^{a}_{bcd} = \partial_{c}\Gamma^{a}_{bd}-\partial_{d}\Gamma^{a}_{bc} + \Gamma^{a}_{ec}\Gamma^{e}_{bd}- \Gamma^{a}_{ed}\Gamma^{e}_{bc}.
$$

