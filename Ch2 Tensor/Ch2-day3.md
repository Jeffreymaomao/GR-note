> For rank-$n$, $n\geq 3$, e.x 
> $$
> X^{a_1,a_2,\ldots,a_n},\quad a_1,a_2,\ldots,a_n = 1,2,\ldots,n
> $$
> we have $n^3$ elements. We define
> $$
> \begin{aligned}
> X_{(a_1,a_2,\ldots,a_N)} &= \frac{1}{n!}\sum \text{all permutations}\\
> X_{[a_1,a_2,\ldots,a_N]} &= \frac{1}{n!}\sum \text{alternating permutations}
> \end{aligned}
> $$
> 
>
> Ex: $n=3$, for anti-symmetric tensor
> $$
> \begin{aligned}
> X_{[a,b,c]} = \frac{1}{6} \left(
>  X_{abc}+X_{bca}+X_{cab}
> -X_{bac}-X_{cba}-X_{acb}\right)
> \end{aligned}
> $$
> For aymmetric tensor
> $$
> X_{(a,b,c)} = \frac{1}{6}\left(++++++\right)
> $$
> **Check**: Also, the symmetrized tensor still remain the properties of original tensor, e.x.
> $$
> X'_{(a,b)} = \frac{\partial x^{c}}{\partial x'^{a}}\frac{\partial x^d}{\partial x'^{b}}X_{(c,d)}
> $$

##### 4. tensor product

Ex: For $(1,1)$-type tensor $Y^{a}_{b}$ and $(0,2)$-type tensor $Z_{cd}$, we want to construct a $(1,3)$-type tensor. 

> **Define**
> $$
> X^{a}_{bcd} = Y^{a}_{b} Z_{cd}
> $$
> Check:
>
> 1. $\displaystyle Y'^{a}_{b} = \frac{\partial x'^{a}}{\partial x^{e}}\frac{\partial x'^{f}}{\partial x^{b}}Y^{e}_{f}$
> 2. $\displaystyle Z'_{cd} = \frac{\partial x^{g}}{\partial x'^{c}}\frac{\partial x^{h}}{\partial x'^{d}}Z^{gh}$
>
> then 
> $$
> \begin{aligned}
> X'^{a}_{bcd} &= Y'^{a}_{b} Z'_{cd}\\
> &= \frac{\partial x'^{a}}{\partial x^{e}}\frac{\partial x'^{f}}{\partial x^{b}}\frac{\partial x^{g}}{\partial x'^{c}}\frac{\partial x^{h}}{\partial x'^{d}}Y^{e}_{f}Z^{gh}
> \end{aligned}
> $$

##### 5. tensor contraction

> *contraction* means summing over some indices

$$
X^{a}_{bcd} \quad\longrightarrow\quad X^{c}_{bcd}
$$

that is $(1,3)$-type to $(0,2)$-type. That is 
$$
X^{c}_{acd} = X^{1}_{a1d} + X^{2}_{a2d} + \cdots + X^{n}_{and}
$$

> Notice that repeated need to be sum, so it is not a $(1,3)$-type anymore.

> Check:
> $$
> \begin{aligned}
> X'^{c}_{bcd} 
> &= \frac{\partial x'^{c}}{\partial x^{e}}
> 	\frac{\partial x^{f}}{\partial x'^{b}}
> 	\frac{\partial x^{g}}{\partial x'^{c}}
> 	\frac{\partial x^{h}}{\partial x'^{d}} X^{e}_{fgh}\\
> &= \left(\frac{\partial x'^{c}}{\partial x^{e}}
> 	\frac{\partial x^{g}}{\partial x'^{c}}\right)
> 	\frac{\partial x^{f}}{\partial x'^{b}}
> 	\frac{\partial x^{h}}{\partial x'^{d}} X^{e}_{fgh}\\
> &= \delta^{g}_{e}
> 	\frac{\partial x^{f}}{\partial x'^{b}}
> 	\frac{\partial x^{h}}{\partial x'^{d}} X^{e}_{fgh}\\
> &= \frac{\partial x^{f}}{\partial x'^{b}}
> 	\frac{\partial x^{h}}{\partial x'^{d}} X^{g}_{fgh}\\
> \end{aligned}
> $$

### Vector fields

<u>Fig vector filed</u>

> **Define**
>
> A vector filed on $M$ is an assignment (smoothly) of tangent at each point of $M$.

Recall:

<u>Fig cirlce</u>

In patch $\{x^{a}\}$, the tangent vector in this patch is expressed as 
$$
X = X^{a}\frac{\partial}{\partial x^{a}}
= \underbrace{X^{a}}_{\rm component} \underbrace{\frac{\partial}{\partial x^{a}}}_{\rm basis}
= X'^{b}\frac{\partial}{\partial x'^{b}}
$$

> Similar to $\displaystyle \vec{A} = \sum_{i=1}^{3}a_{i}\hat{e}_i = \sum_{j=1}^{3}a'_{j}\hat{e}'_j$

> we then check 
> $$
> \frac{\partial}{\partial x^{a}} = \frac{\partial x'^{b}}{\partial x^{a}} \frac{\partial }{\partial x'^{b}} 
> $$
> so 
> $$
> X 
> = X^{a}\frac{\partial}{\partial x^{a}} 
> = X^{a}\frac{\partial x'^{b}}{\partial x^{a}} \frac{\partial }{\partial x'^{b}}
> = X'^{b} \frac{\partial }{\partial x'^{b}}
> $$
> so the component is a controvariant.



We need to clearify the notation. $T_{p}(M)$ is the tangent space at $p$, then 
$$
T(M)=\bigcup_{p} T_{p}(M)
$$
is a vector field, where $X\in T(M)$ and $X\bigg|_{p} = T_{p}(M)$

> **Lie bracket**  
>
> Suppose $X$ and $Y$ are two vector field, i.e. locally 
> $$
> X=X^{a}\frac{\partial}{\partial x^{a}}
> \quad\text{and}\quad 
> Y=Y^{b}\frac{\partial}{\partial x^{b}}.
> $$
> Then the *Lie bracket* is still a vector field. 
>
> **Check**: For a function $f$
> $$
> \begin{aligned}
> \,[X,Y] f 
> &= \left(XY-YX\right)f\\
> &= \left(XY^{b}\frac{\partial}{\partial x^{b}}-YX^{a}\frac{\partial}{\partial x^{a}}\right)f\\
> &= \left(
> 	X^{a} \frac{\partial}{\partial x^{a}}
> 	\left(Y^{b}\frac{\partial f}{\partial x^{b}}\right)
> 	-
> 	Y^{b}\frac{\partial}{\partial x^{b}}
> 	\left(X^{a}\frac{\partial f}{\partial x^{a}}\right)\right)\\
> &= X^{a}\left(\frac{\partial Y^{b} }{\partial x^{a}}\frac{\partial f}{\partial x^{b}} + Y^{b}\frac{\partial^2 f}{\partial x^{a}x^{b}}\right)
> 	-
> 	Y^{b}\left(\frac{\partial X^{a}}{\partial x^{b}}\frac{\partial f}{\partial x^{a}}+X^{a}\frac{\partial^2 f}{\partial x^{b}x^{a}}\right)\\
> &= X^{a}\frac{\partial Y^{b} }{\partial x^{a}}\frac{\partial f}{\partial x^{b}} 
> 	+ X^{a}Y^{b}\frac{\partial^2 f}{\partial x^{a}x^{b}}
> 	- Y^{b}\frac{\partial X^{a}}{\partial x^{b}}\frac{\partial f}{\partial x^{a}}
> 	+Y^{b}X^{a}\frac{\partial^2 f}{\partial x^{b}x^{a}}\\
> &= X^{a}\frac{\partial Y^{b} }{\partial x^{a}}\frac{\partial f}{\partial x^{b}} 
> 	- Y^{b}\frac{\partial X^{a}}{\partial x^{b}}\frac{\partial f}{\partial x^{a}}\\
> &= \left(X^{a}\frac{\partial Y^{b} }{\partial x^{a}}\frac{\partial}{\partial x^{b}} - Y^{b}\frac{\partial X^{a}}{\partial x^{b}}\frac{\partial}{\partial x^{a}}\right)f
> \end{aligned}
> $$
> Now we define the Lie bracket to be $\displaystyle Z = [X,Y] = Z^{a}\frac{\partial}{\partial x^{a}}$, since 
> $$
> Z=[X,Y] = X^{b}\frac{\partial Y^{a} }{\partial x^{b}}\frac{\partial}{\partial x^{a}} - Y^{b}\frac{\partial X^{a}}{\partial x^{b}}\frac{\partial}{\partial x^{a}} 
> = \left(X^{b}\frac{\partial Y^{a} }{\partial x^{b}} - Y^{b}\frac{\partial X^{a}}{\partial x^{b}}\right)\frac{\partial}{\partial x^{a}} 
> = Z^{a}\frac{\partial}{\partial x^{a}}
> $$
> Let 
> $$
> Z^{a} =X^{b}\frac{\partial Y^{a} }{\partial x^{b}} - Y^{b}\frac{\partial X^{a}}{\partial x^{b}}
> $$
> **Check**: $Z^{a}$ is a contravariant vector.
>
> 
