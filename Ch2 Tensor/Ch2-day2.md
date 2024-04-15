#### Tangent space

For a mani fold $M$

<u>Fig - tangent space</u>



> If $M$ is locally the same as $\mathbb{R}^n$, introducting coordinate patchs
> $$
> \{U_1,U_2,\ldots\} = \text{atlas.}
> $$
> In the overlapping $U_\alpha \cap U_\beta \neq \phi$ , $\alpha\neq\beta$
>
> <u>Fig - overlapping region</u>
>
> we have $x^{a} = x^{a}(y^1,y^2,\ldots,y^n)$, $a=1,2,\ldots,n$.

### $\odot$ Tensor transformations of coordinates

Consider a change of coordinates
$$
x^{a}\mapsto x'^{a} = f^{a} (x^1,x^2,\ldots,x^n)\equiv x'^{a}(x)
$$
which means $x'$ is a function of $x$. We define

> **Definition**
>
> A matrix
> $$
> {J'^{a}}_{b} \equiv \frac{\partial x'^{a}}{\partial x^{b}}
> $$
> called *Jocobian matrix*, and 
> $$
> J'\equiv \abs{J'^{a}_{b}} = \det(J^{a}_{b}).
> $$
> Also, by implicit function theorem $x^{a} = x'^{a}(x')$, we have
> $$
> J^{a}_{b} = \frac{\partial x'^{a}}{\partial x^{b}}.
> $$
> In fact $J'^{a}_{b}J^{b}_{c} = \delta^{a}_{c}$, then $J' = \det(J^{a}_{b}) = 1/J$. (Notice $\delta^{a}_{b}$ is the Kronecker delta function.)

> Rmk:
> $$
> J'^{a}_{b} = \frac{\partial x'^{a}}{\partial x^{b}} 
> = \begin{pmatrix}
> \frac{\partial x'^{1}}{\partial x^{1}} & \frac{\partial x'^{1}}{\partial x^{2}} & \cdots & \frac{\partial x'^{1}}{\partial x^{n}}\\
> \frac{\partial x'^{2}}{\partial x'^{1}} & \frac{\partial x^{2}}{\partial x^{2}} & \cdots & \frac{\partial x'^{2}}{\partial x^{n}}\\
> \vdots & \vdots & \ddots & \vdots \\
> \frac{\partial x'^{n}}{\partial x^{1}} & \frac{\partial x'^{n}}{\partial x^{2}} & \cdots & \frac{\partial x'^{n}}{\partial x^{n}}\\
> \end{pmatrix}
> $$

> Rmk:
>
> $\frac{\partial x^{a}}{\partial x'^{b}}$ can be viewd as coefficients of infinitesmall defferentials, then
> $$
> \begin{aligned}
> dx'^{a} &= 
> 	\frac{\partial x'^{a}}{\partial x^{1}}dx^{1} 
> 	+ \frac{\partial x'^{a}}{\partial x^{2}}dx^{2}  
> 	+ \cdots 
> 	+ \frac{\partial x'^{a}}{\partial x^{n}}dx^{n} \\
> &= \sum_{b=1}^{n} \frac{\partial x^{a}}{\partial x'^{b}} dx^{b}\\
> &= \frac{\partial x^{a}}{\partial x'^{b}} dx^{b},\quad \text{Einstein convension}
> \end{aligned}
> $$

We shall classify geometric tensors quantities by transformation properties.

> **Definition**
>
> A *contravariant* vector (rank-1) is a set of quantities $X^{a}$ defined on $p\in M$, such that under coordinate transformation:
> $$
> x^{a}\mapsto x'^{a}(x),
> $$
> we have
> $$
> X'^{a} = \frac{\partial x'^{a}}{\partial x^{b}} X^{b}
> $$
> <u>Fig - point p in overlapping patch</u>

> e.g. tangent vector at $p$ in $M$.
>
> <u>Fig - tangent vector at p on M</u>
>
> For $f$ is a function defined on the curve $\gamma$, where 
> $$
> f = f(x^{a}(u)),
> $$
> and
> $$
> \frac{df}{du} = \frac{\partial f}{\partial x^{a}} \frac{dx^a}{du}
> $$
> holds for any $f$. Therefore
> $$
> \frac{d}{du} = \left(\frac{dx^{a}}{du}\right)\frac{\partial}{\partial x^{a}},
> $$
> and here where $\partial / \partial x^{a}$​ is like a basis.
>
> Notice that, for $X'^{a} = dx^a/du$
> $$
> X'^{a} = \frac{dx'^a}{du} = \frac{dx'^{a}}{dx^{b}}\frac{dx^{b}}{du} = \frac{dx'^{a}}{dx^{b}}X^{a},
> $$
>  therefore, $dx^a/du$ is a contravariant vector.

How about higher rank tensors? e.g. rank-2
$$
X'^{ab} = \frac{\partial x^{a}}{\partial x^{c}}\frac{\partial x^{b}}{\partial x^{d}}X^{cd}.
$$
In general, for rank-$n$ tensor
$$
X'^{i_1,\ldots,i_n} = 
	\frac{\partial x^{i_1}}{\partial x^{j_1}}
	\frac{\partial x^{i_2}}{\partial x^{j_2}}
	\cdots
	\frac{\partial x^{i_3}}{\partial x^{j_3}}
	X'^{j_1,\ldots,j_n}
$$

> Rmk:
>
> For a scalar $\phi$ (without indices or rank-0), we have
> $$
> \phi'(x') = \phi(x)
> $$
> Here, notice $\phi'$ is not the differentiation of function $\phi$.

> **Definition**
>
> A covarariant vector (rank-1) is a set of quantities $X_a$ defined at $p\in M$, such that under coordinate transformation, we have
> $$
> X'_{a} = \frac{\partial x^b}{\partial x'^a} X_b.
> $$
> e.g. a gradient of $\phi$ 
> $$
> \frac{\partial \phi}{\partial x'^{a}} = \frac{\partial \phi}{\partial x^{b}} \frac{\partial x^{b}}{\partial x'^{a}},
> $$

Also, for rank-2 covariant vector 
$$
X'_{ab} = \frac{\partial x^{c}}{\partial x^{a}} \frac{\partial x^{d}}{\partial x^{b}} X_{cd}
$$
If a tensor has a form:
$$
X^{a_1,\ldots,a_{p}}_{b_1,\ldots,b_q},
$$
we called a *mixed-type* tensor denoted by $(p,q)$ type (up,down).

In summary:

|  tensor  |  Type   |
| :------: | :-----: |
|  $\phi$  | $(0,0)$ |
| $X^{a}$  | $(1,0)$ |
| $X_{a}$  | $(0,1)$ |
| $X^{ab}$ | $(2,0)$ |
| $X_{ab}$ | $(0,2)$ |

#### Coordinate-independent 

Physical laws are described by tensor equatios which are coordinates-independent, e.g. Suppose a law is written in the form
$$
X_{ab} = Y_{ab}
$$
in $x$-system, $X$ and $Y$must the same type, since the physical laws must valid in any system. We rewrite the equation to $X_{ab} - Y_{ab} = 0$, and this equation must holds for $X'_{cd} - Y'_{cd} = 0$, and since the transformation is 
$$
\begin{aligned}
X'_{cd} = \frac{\partial x^{a}}{\partial x'^{c}} \frac{\partial x^{d}}{\partial x'^{b}} X_{cd}\\
Y'_{cd} = \frac{\partial x^{a}}{\partial x'^{c}} \frac{\partial x^{d}}{\partial x'^{b}} Y_{cd}
\end{aligned}
$$
so that
$$
\left(X'_{ab} - Y'_{ab}\right) = \frac{\partial x^{a}}{\partial x'^{c}} \frac{\partial x^{d}}{\partial x'^{b}}  \left(X_{ab} - Y_{ab}\right) = 0
$$

##### example

Maxwell's equations for $\vec{E} = (E_1,E_2,E_3)$ and $\vec{B} = (B_1,B_2,B_3)$ is given by
$$
F_{\mu\nu} = - F_{\mu\nu},
$$
where the tensor is
$$
F_{\mu\nu}=
\begin{pmatrix}
0			&E_{1}/c	&E_{2}/c	&E_{3}/c\\
-E_{1}/c	&0			&-B_{3}		&B_{2}\\
-E_{2}/c	&B_{3}		&0			&-B_{1}\\
-E_{3}/c	&-B_{2}		&B_{1}		&0
\end{pmatrix}
$$
and for $j^{\mu} = \left(\rho c,\vec{J}\right)$, we have
$$
\partial_{\mu}F^{\mu\nu} = j^{nu},
$$
rand-1 controvariant equation under Lorentz transformation $x'^{\mu} = x^{\mu}(x)$​ .

### $\odot$ Tensor fiels

> **Definition**
>
> Over $M$, we asign smoothly every point a tensor, which forms a tensor field.

e.g. a vector field

<u>Fig - vector field</u>

Now, we denote as 
$$
X^{ab}(x),\quad x\in M.
$$

### $\odot$ Elementary operation of tensors

##### 1. Addition

For three $(1,2)$-type tensors $X^{a}_{bc}$, $Y^{a}_{bc}$ and $X^{a}_{bc}$, we have
$$
X^{a}_{bc} = Y^{a}_{bc} + Z^{a}_{bc}
$$

##### 2. scalar multiplication 

For $k\in\mathbb{R}$, we have $kX^{a}_{bc}$

##### 3. symmetrization

$$
\begin{aligned}
X_{ab} &= \frac{1}{2}\left(X^{ab} + X^{ba}\right) + \frac{1}{2}\left(X^{ab} - X^{ba}\right)\\
&= X_{(a,b)} + X_{[a,b]}
\end{aligned}
$$

then 
$$
\begin{aligned}
X_{(a,b)} &= + X_{(b,a)}\\
X_{[a,b]} &= - X_{[b,a]}
\end{aligned}
$$

and $X_{(a,b)}$ called symmetric tensor, $X_{[a,b]}$ called anti-symmetric tensor.

