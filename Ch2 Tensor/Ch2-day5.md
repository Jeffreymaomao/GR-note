> **Review**: Lie dedrivative
> $$
> \lim_{\delta u \to 0} \frac{T(Q)-T(P)}{\delta u}
> $$
> <u>Fig</u>
>
> Drag $T(P)\to T'(Q)$ then define $\displaystyle L_X T = \lim_{\delta u\to 0} \frac{T(Q)-T'(Q)}{\delta u}$, where the drag
> $$
> T'^{a}(x+\delta u\, X) = \left(\frac{\partial x'^{a}}{\partial x^{b}}\right) T^{b}(x)
> $$
> So that the Lie dedrivative  $L_X = X^{b}\partial_{b}T^{a} - T^{b}\partial_b X^{a}$, which is a contravariant vector.
>
> In general, for $T^{a_1,a_2,\cdots,a_n}$, the Lie dedrivative is defined to be
> $$
> L_X T^{a_1,a_2,\ldots,a_n} = X^{b}\partial_b T^{a_1,a_2,\ldots,a_n} - \left(\right)
> $$

> Rmk:
> $$
> \begin{aligned}
> L_X Y^{a} &= X^{b}\partial_b Y^{a} - Y^{b}\partial_b X^{a}\\
> &= [X,Y]^{a}
> \end{aligned}
> $$

> Rmk:
>
> For scalar $\phi$, its drag is $\phi'(x') = \phi(x)$, so 
> $$
> L_{X} \phi = \lim_{\delta u\to 0}\frac{\phi(X+\delta u) - \phi(X)}{\delta u} = X^{c}\partial_c \phi
> $$

How about covariant vector $L_XY_a$? We write
$$
L_XY_a = \lim_{\delta u\to0}\frac{Y_{a}(X+\delta u X) - Y'_{a}(X')}{\delta u}
$$
Its drag:









#### Summary

| Contravariant                                               | Covariant                                                   |
| ----------------------------------------------------------- | ----------------------------------------------------------- |
| $L_X Y^{a} = X^{b}\partial_b Y^{a} - Y^{b}\partial_b X^{a}$ | $L_X Y_{a} = X^{b}\partial_b Y_{a} + Y_{b}\partial_a X^{b}$ |

> Ex: $(1,1)$-type 
> $$
> L_{X}T^{a}_{b} = X^{c}\partial_c T^{a}_{b} - T^{c}_{b}\partial_{c}X^{a} + T^{a}_{c}\partial_{b}X^{c}
> $$

> Check for $(2,1)$-type

$$
L_X(Y^{a}Y_{a})=
$$

### $\odot$ Covariant differentiation

> 協變微分（引入了connection）

If we replace the dragged vector by a "*parallel vector*".
$$
X^{a}_{\parallel}(x+\delta x) = X^{a}(x) - \delta \bar{X}^{a}
$$
Notice $\delta \bar{X}^{a}$ very small, so it is propotion to (linear to) $X^{a}$ and $\delta x$, i.e.
$$
\delta \bar{X}^{a} = -\Gamma^{a}_{bc} X^{b}\delta x^{c},
$$
where $\Gamma^{a}_{bc}$ is a 3 indices object connect the ... and ... called "*connection coefficient*".

> Notice the repeating indices
> $$
> \delta \bar{X}^{a} = -\sum_{b,c=1}^{n}\Gamma^{a}_{bc} X^{b}\delta x^{c},
> $$

<u>Fig</u>

Then we have
$$
\begin{aligned}
\nabla_{c}X^{a} &\equiv \lim_{\delta x^{a}\to 0} \frac{X^{a}(x+\delta x^{a}) - X^{a}_{\parallel}}{\delta x^{a}}\\
&= \lim_{\delta x^{c}\to 0} \frac{\left(X^{a}(x)+\delta x^{c}\partial_c X^{a}\right)-\left(X^{a}(x)-\Gamma^{a}_{bc}X^{v}\delta x^{c}\right)}{\delta x^{c}}
\end{aligned}
$$
So we define the covariant derivative 
$$
\nabla_{c} X^{a} = \partial_{c}X^{a} + \Gamma^{a}_{bc} X^{b}
$$
We hope $\nabla_c X^{a}$ is a $(1,1)$-type tensor, so we will obtain the transformation rule for connection foefficients $\Gamma^{a}_{bc}$

> Check: Is it a $(1,1)$-type tensor?
> $$
> \nabla'_{c}X^{a} = \left(\frac{\partial x'^{a}}{\partial x^{d}}\right)\left(\frac{\partial x^{b}}{\partial x^{c}}\right)\nabla_{b}X^{d}
> $$
> Then the left hand side is 
> $$
> \begin{aligned}
> \mathrm{LHS} 
> &= \partial'_{c} X'^{a} + \Gamma'^{a}_{bc}X'^{b}\\
> &= \partial'_{c}\left(\frac{\partial x'^{a}}{\partial x^{b}}X^{b}\right) 
> 	+ \Gamma'^{a}_{bc} \left(\frac{\partial x'^{b}}{\partial x^{d}}X^{d}\right)\\
> &= \partial'_{c}\left(\frac{\partial x'^{a}}{\partial x^{b}}\right) X^{b}
> 	+  \frac{\partial x'^{a}}{\partial x^{b}}\partial'_{c}X^{b}
> 	+ \Gamma'^{a}_{bc} \left(\frac{\partial x'^{b}}{\partial x^{d}}X^{d}\right)\\
> \end{aligned}
> $$
> and the right hand side
> $$
> \begin{aligned}
> \mathrm{RHS} 
> &=\left(\frac{\partial x'^{a}}{\partial x^{d}}\right) \left(\frac{\partial x^{b}}{\partial x'^{c}}\right) \left(\partial_{b}X^{d} + \Gamma^{d}_{eb}X^{e}\right)\\
> &=\left(\frac{\partial x'^{a}}{\partial x^{d}}\right) \frac{\partial x^{b}}{\partial x'^{c}} \frac{\partial}{\partial x^{b}}X^{d} 
> 	+ \left(\frac{\partial x'^{a}}{\partial x^{d}}\right) \left(\frac{\partial x^{b}}{\partial x'^{c}}\right)\Gamma^{d}_{eb}X^{e}\\
> &=\left(\frac{\partial x'^{a}}{\partial x^{d}}\right)\frac{\partial}{\partial x'^{c}}X^{d} 
> 	+ \left(\frac{\partial x'^{a}}{\partial x^{d}}\right) \left(\frac{\partial x^{b}}{\partial x'^{c}}\right)\Gamma^{d}_{eb}X^{e}\\
> &=\left(\frac{\partial x'^{a}}{\partial x^{d}}\right)\partial'_{c}X^{d} 
> 	+ \left(\frac{\partial x'^{a}}{\partial x^{d}}\right) \left(\frac{\partial x^{b}}{\partial x'^{c}}\right)\Gamma^{d}_{eb}X^{e}
> \end{aligned}
> $$
> Then solving that
> $$
> \begin{aligned}
> \mathrm{LHS} 
> &= \partial'_{c}\left(\frac{\partial x'^{a}}{\partial x^{b}}\right) X^{b}
> 	+  \frac{\partial x'^{a}}{\partial x^{b}}\partial'_{c}X^{b}
> 	+ \Gamma'^{a}_{bc} \frac{\partial x'^{b}}{\partial x^{d}}X^{d}\\
> \mathrm{RHS} 
> &= \frac{\partial x'^{a}}{\partial x^{d}}\partial'_{c}X^{d} 
> 	+ \left(\frac{\partial x'^{a}}{\partial x^{d}}\right) \frac{\partial x^{b}}{\partial x'^{c}}\Gamma^{d}_{eb}X^{e}\\
> &\Rightarrow 
> \partial'_{c}\left(\frac{\partial x'^{a}}{\partial x^{b}}\right) X^{b} 
> + 
> \Gamma'^{a}_{bc} \frac{\partial x'^{b}}{\partial x^{d}}X^{d}
> = 
> \left(\frac{\partial x'^{a}}{\partial x^{d}}\right) \left(\frac{\partial x^{b}}{\partial x'^{c}}\right)\Gamma^{d}_{eb}X^{e} \\
> &\Rightarrow 
> \left[
> \partial'_{c}\left(\frac{\partial x'^{a}}{\partial x^{e}}\right) 
> + 
> \Gamma'^{a}_{bc} \frac{\partial x'^{b}}{\partial x^{e}}
> \right]X^{e}
> = 
> \left(\frac{\partial x'^{a}}{\partial x^{d}}\right) \left(\frac{\partial x^{b}}{\partial x'^{c}}\right)\Gamma^{d}_{eb}X^{e} 
> \end{aligned}
> $$
> Deriving that
> $$
> \partial'_{c}\left(\frac{\partial x'^{a}}{\partial x^{e}}\right) 
> + 
> \Gamma'^{a}_{bc} \frac{\partial x'^{b}}{\partial x^{e}}
> = 
> \frac{\partial x'^{a}}{\partial x^{d}} \frac{\partial x^{b}}{\partial x'^{c}}\Gamma^{d}_{eb}
> $$

> Rmk:
>
> A manifold $M$ with prescribed connection on it is called an "*Affined manifold*" denoted as $(M,\Gamma)$.

> Ex: For the covariant tensor $\nabla_{c} X_{a}$.
>
> Since $\nabla_{c}(X_{a}X^{a}) = \partial_{c}(X_{a}X^{a})$, we can expand
> $$
> \nabla_{c}\left(X_{a}X^{a}\right) = \left(\nabla_{c}X_{a}\right)X^{a} + X_{a}\nabla_{c}X^{a} = \partial_{c}(X_{a}X^{a})
> $$
> so that 
> $$
> \nabla_{c}X_{a} = \partial_{c} X_{a} - \Gamma^{a}_{bc} X_{b}
> $$

In general, for the tensor $\nabla_{c}T^{a}_{bc}$

