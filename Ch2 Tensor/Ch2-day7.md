> Note:
>
> If it is not torsion-free
> $$
> \left(\nabla_{c}\nabla_{d} - \nabla_{d}\nabla_{c}\right)X^{a} 
> =  R^{a}_{bcd} X^{b} \left(\partial_{c}\partial_{d} 
> + \left(\Gamma^{b}_{cd}-\Gamma^{b}_{dc}\right)\nabla_{b} X^{a}
> - \partial_{d}\partial_{c}\right)X^{a} ,
> $$

### Geodesic coordiante

Locally, we may choose $\{x^{a}\}$ s.t. $\Gamma^{a}_{bc} \stackrel{*}{=} 0$ , $[x^{a}]_{p} \stackrel{*}{=} 0$

Suppose, 
$$
x^{a} \mapsto x'^{a} + \frac{1}{2}Q^{a}_{bc} x^{b} x^{c},
$$
where we require $Q^{a}_{bc} = Q^{a}_{bc}$ (constant), then we calculte
$$
\frac{\partial x'^{a}}{\partial x^{d}}\Bigg|_{p} = \delta^{a}_{d} \Bigg|_{p} + Q^{a}_{bc} x^{b}\Bigg|_{p} = \delta^{a}_{d}
$$
then
$$
\frac{\partial^2 x'^{a}}{\partial x^{d}\partial x^{c}}\Bigg|_{p} = Q^{a}_{cd}
$$

> **Recall:**
> $$
> \begin{aligned}
> \Gamma'^{a}_{bc} 
> &= \left(\frac{\partial x'^{a}}{\partial x^{d}}
> 	\frac{\partial x^{f}}{\partial x'^{c}}
> 	\frac{\partial x^{e}}{\partial x'^{b}}\right)\Bigg|_{p}
> 	\Gamma^{d}_{ef}\Bigg|_{p} 
> 	- \frac{\partial^2 x'^{a}}{\partial x^{d}\partial x^{c}}
> 	\frac{\partial x^{d}}{\partial x'^{c}}
> 	\frac{\partial x^{e}}{\partial x'^{b}}\Bigg|_{p}\\
> &= \delta^{a}_{b} \, \delta^{f}_{c} \, \delta^{e}_{b} \,\Gamma^{d}_{ef}\Bigg|_{p} 
> 	- Q^{a}_{ed}\delta^{d}_{c}\delta^{e}_{b}\\
> &= \Gamma^{a}_{bc}\Bigg|_{p} - Q^{a}_{bc}
> \end{aligned}
> $$

So, if we choose 
$$
Q^{a}_{bc} = \Gamma^{a}_{bc}\Bigg|_{p}
$$
then 
$$
\Gamma'^{a}_{bc} \stackrel{*}{=} 0
$$
This "trick" for computation set $\Gamma^{a}_{bc}\Bigg|_{p} = 0$. After computation, restore $\Gamma$ by $\partial_{a}\to \nabla_{a}$.

> **Rmk:**
>
> In general, it is impossible to find a coordinate transforamtion, s.t. $\Gamma^{a}_{bc} = 0$ globally. If it does, then the manifold is affine flat manifold.

## Affine flatness

### $\odot$ Integrable connetion

#### **Definition**:

If a parallel transport of a vector from $P$ to $Q$ is *independent* pf path then the connection is *integrable*.

#### Lemma 1.

The connection is *integrable* or *torsion free*t $\Longleftrightarrow$  $R^{a}_{bcd} = 0$.

##### proof $\Rightarrow$ (necessary)

If $\Gamma^{a}_{bc}$ is integrable $\Rightarrow$ $\displaystyle \frac{dc^{c}}{du} \nabla_{c} X^{a} = 0$ is path integrable $\Rightarrow$ Since, $\displaystyle \frac{dc^{c}}{du}$ is arbitrary. $\nabla_cX^{a}=0$ , that is 
$$
\nabla_{c} X^{a} = \partial_{c} X^{a} + \Gamma^{a}_{bc} X^{b} = 0
$$
which is 1st order P.D.E. the existence of solution: $\partial_{d}\partial_{c}X^{a} = \partial_{c}\partial_{d}X^{a}$, 
$$
\begin{aligned}
\nabla_{c}\nabla_{d} X^{a} - \nabla_{d}\nabla_{c} X^{a}
&= R^{a}_{bcd} X^{b} + \left(\Gamma^{e}_{cd} - \Gamma^{e}_{dc}\right)\nabla_{e}X^{a} + \left(\partial_{d}\partial_{c}X^{a} - \partial_{c}\partial_{d}\right)X^{a}\\
&= R^{a}_{bcd} X^{b} = 0
\end{aligned}
$$
Since $X^{b}$ is arbitrary, $R^{a}_{bcd} = 0$.

##### proof $\Leftarrow$ (sufficient)

Consider an infinitesmal loop:

<u>FIg</u>

compute parallel transport along two paths.

1. For the path $C_1$:

    - $x^{a}\to x^{a} + \delta x^{a}$
        $$
        \begin{aligned}
        X^{a}(x+\delta x) 
        &= X^{a}(x) + \bar{\delta} X^{a}(x)\\
        &= X^{a}(x) - \Gamma^{a}_{bc} X^{b}\delta x^{c}
        \end{aligned}
        $$

    - $x^{a}+\delta x^{a}\to (x^{a} + \delta x^{a}) + dx^{a}$
        $$
        \begin{aligned}
        X^{a}(x+\delta x+dx) 
        &= X^{a}(x+\delta x) + \bar{\delta} X^{a}(x+\delta x)\\
        &= \left(X^{a}(x) - \Gamma^{a}_{bc} X^{b}\delta x^{c}\right) 
        	- \left(\Gamma^{a}_{bc}+\partial_{d}\Gamma^{a}_{bc}\delta x^{d}\right)
        	\left(x^{b} - \Gamma^{b}_{ef}X^{e}\delta x^{f}\right) dx^{c}
        \end{aligned}
        $$
        

2. For the path $C_2$:
    $$
    \begin{aligned}
    X^{a}(x+dx+\delta x)
    &= X^{a} - \Gamma^{a}_{bc} X^{b} dx^{c} - \Gamma^{a}_{bc} x^{b}\delta x^{c}\\
    &= 
    \end{aligned}
    $$
    

Last we have the difference 
$$
\begin{aligned}
\Delta X &= X^{a}_{C_1}(x+\delta x+dx) - X^{a}_{C_2}(x+\delta x+dx)\\
&= \left(\partial \Gamma^{a}_{bd} - \partial\right) X^{b}\delta x^{d}\delta x^{c}\\
&= R^{a}_{cbd}
\end{aligned}
$$

#### Lemma 2

A manifold $M$ is affine flat ($\Gamma^{a}_{bc}=0$ globally) $\Longleftrightarrow$ The connection symmetric and integrable.

##### proof $\Rightarrow$ (necessary)

If $M$ is affoine flat, then $\Gamma^{a}_{bc}=0$ everywhere, then parallel transport is path independent, trivially.

##### proof $\Leftarrow$ (sufficient)

If $\Gamma^{a}_{bc}$ is integrable, around $P$ choose L.T. vector  $\{X^{a}_{1},\ldots,X^{a}_{n}\}$, where $\operatorname{dim} M = n$. Now, using $\Gamma^{a}_{bc}$ to parallel transport $\{X^{a}_{i}\}$ everywhere. 

Hence, for any $x\in M$, $\{X^{a}_{i}(x)\}$ is L.T., then $\abs{X^{a}_{i}}\neq 0$ (by L.T.), so $\exists !$ inverse $X^{i}_{b}$ s.t. 
$$
X^{a}_{i}X^{i}_{a} = \delta^{a}_{b}.
$$
Since
$$
0 = \nabla_{b} X^{a}_{i} = \partial_{b} X^{a}_{i} + \Gamma^{a}_{cb} X^{c}_{i}
\quad\Rightarrow\quad
\Gamma^{a}_{cb} = - X^{i}_{c} \partial X^{a}_{i}.
$$
Thus 
$$
o = \Gamma^{a}_{bc} - \Gamma^{a}_{cb} = X^{i}_{c}\partial_{b} X^{a}_{i} - X^{i}_{b} \partial_{c}X^{a}_{i} = \left(X^{i}_{c}\partial_{b} - X^{i}_{b} \partial_{c}\right)X^{a}_{i}
$$
Because, $(X^{a}_{i})$ is non-degenerate $\Rightarrow$ $\partial_c X^{i}_{b} = \partial_{b} X^{i}_{c}$, then $\forall x\in M, \exists$ functions $f^{i}(x)$ s.t. $X^{i}_{b} = \partial_{b} f^{i}$
