#### Recall

- $(M,\Gamma)$​ affine manifold

- $\Gamma^{a}_{bc}$ affine connection

- e.g. for a $(1,1)$-type tensor): $\nabla_{c}X^{a} = \partial_{c}X^{a} + \Gamma^{a}_{bc}X^{b}$

- trosion free: $\Gamma^{a}_{bc} = \Gamma^{a}_{cb}$

- Integrable: parrellel transport is path independent

- affine geodesic $x^{a}(u)$
    $$
    \frac{d^2x^{a}}{du^2} + \Gamma^{a}_{bc}\frac{dx^{b}}{du}\frac{dx^{b}}{du} = 0
    $$

- Riemannian tensor ($(1,3)$-type tensor)
    $$
    R^{a}_{bcd} = 
    	\partial_{c}\Gamma^{a}_{bd} 
    	- \partial_{d}\Gamma^{a}_{bc}
        + \Gamma^{e}_{bd}\Gamma^{a}_{ec}
        - \Gamma^{e}_{bc}\Gamma^{a}_{ed}
       
    $$

- How flat?

    - $M$ is affine flat $\Leftrightarrow$ $\Gamma^{a}_{bc}$​ is tegrable symmetry
    - $\Gamma^{a}_{bcd} = 0$ $\Leftrightarrow$ $\Gamma^{a}_{bc}$ is tegrable symmetry
    - $M$ is affine flat $\Leftrightarrow$$\Gamma^{a}_{bcd} = 0$ 

- geodesic coordinate $\{x^{a}\}$: $\Gamma^{a}_{dc} = 0$

## Metric

> 度規：$(M,g_{\mu\nu})$

If we add an additional structure called mretric $g_{ab}(x)$, a $(0,2)$-type symmetric tensor.

#### Def: (Riemannian manifold)

A Riemannian manifold $(M,g)$ where $g_{ab}$ is the metric defoned by
$$
(ds)^{2} = g_{ab}dx^{a}dx^{b}
$$
also called *1st fundamental form*.

<u>Fig</u>

> e.g. in $\mathbb{R}^{3}$
> $$
> (ds)^2 = (dx)^2 + (dy)^2 + (dz)^2 
> $$
> where
> $$
> g_{ab}=\begin{pmatrix}
> 1 & 0 & 0\\
> 0 & 1 & 0\\
> 0 & 0 & 1\\
> \end{pmatrix}.
> $$

> e.g. in $\mathbb{R}^{2}$
> $$
> (ds)^2 = (dr)^2 + r^2(d\theta)^2 = (dx)^2 + (dy)^2
> $$
> where
> $$
> g_{ab}\bigg|_{\rm polar} = \begin{pmatrix}1 & 0\\ 0 & r^2\end{pmatrix}
> ,\quad
> g_{ab}\bigg|_{\rm Cartisian} = \begin{pmatrix}1 & 0\\ 0 & r^2\end{pmatrix}
> $$

For $x^{a} \in T_{p}(M)$, we define
$$
\cos(X,Y) = \frac{g_{ab}X^{a}Y^{b}}{\sqrt{|X|^2|Y|^2}} 
$$
where $|X|^2 = g_{ab}X^{a}X^{b}$. Notice that
$$
\begin{cases}
|X|^2 > 0 & \text{positive}\\
|X|^2 < 0 & \text{negative}
\end{cases}
$$

> **Rmk:**
>
> 1. $X^{a}\perp Y^{b}$, if $g_{ab}X^{a}Y^b = 0$
>
> 2. $g_{ab}$ is non-singular, if $\det(g_{ab}) \neq 0$
>
> 3. $(g_{ab})^{-1}=g^{ab}$, that is $g_{ab}g^{ab} = \delta^{a}_{b}$
>
> 4. $g_{ab}$ and $g^{ab}$ can be used to lowering and rasing tensorial indices. e.g.
>     $$
>     \begin{aligned}
>     X^{a} = g^{ab}X_{b}\\
>     X_{a} = g_{ab}X^{b}\\
>     \end{aligned}
>     $$
>     Notice that 
>     $$
>     g_{ab}T^{bc} = {T_{a}}^{c}
>     $$
>     In general, 
>     $$
>     {X_{b}}^{a} = g^{ac}X_{bc}
>     \quad\neq\quad
>     {X^{a}}_{b} = g^{ac}X_{cb}
>     $$

#### Geodesic equation

For the Riemannian manifold $(M,g)$,
$$
(ds)^2 = g_{ab} dx^a dx^b
$$
Then the path $x^{a}(u)$  from $u=P$ to $u=Q$, can be interpreted as
$$
S 
= \int_{P}^{Q} ds 
= \int_{P}^{Q} \sqrt{g_{ab}dx^a dx^b} 
= \int_{P}^{Q} \sqrt{g_{ab}\frac{dx^a}{du}\frac{dx^b}{du}} du
$$
then if we want to minimize the path to find the shortest path from $P$ to $Q$ , we can define the Lagrangian to be
$$
L(x^{a}, x^{b}, u) = \sqrt{g_{ab}\frac{dx^a}{du}\frac{dx^b}{du}} = \sqrt{g_{ab}\dot{x}^{a}\dot{x}^b}
$$
the the path reduced to 
$$
S = \int_{P}^{Q}L(x^{a}, x^{b}, u)du
$$
Using the *Least Action Principle* the shortest path $x^{a}$ corresponding to the solution for the *Euler-Lagrangian equation*
$$
\frac{d}{du}\left(\frac{\partial L}{\partial \dot{x}^{a}}\right) = \frac{\partial L}{\partial x^{a}}
$$
the EL equation becomes
$$
g^{ab}\ddot{x}^{b} + \left(\partial_{c}g_{ab} -\frac{1}{2}\partial_{c}g_{db}\right) ..
$$


choosing a linear parameter $u=\alpha s + \beta$, the equation becomes 
$$
\frac{d^2x^a}{ds^2} + \left\{\begin{matrix}a\\bc\end{matrix}\right\} \frac{dx^{b}}{ds}\frac{dx^{c}}{ds} = 0
$$

> **Recall:**
>
> The affine geodesic
> $$
> \frac{d^2x^a}{ds^2} + \Gamma^{a}_{bc} \frac{dx^{b}}{ds}\frac{dx^{c}}{ds} = 0
> $$
> 

Comparing to the affine geodesic, define
$$
\left\{\begin{matrix}a\\bc\end{matrix}\right\} = \frac{1}{2}g^{ad}\left\{bc,d\right\}
= \frac{1}{2}g^{ad} \left(\partial_{b}g_{dc} + \partial_{c}g_{db} -\partial_{d}g_{bc}\right)
$$
That is we can deine a *metric connection* $\Gamma$ by the metric $g$ by
$$
\Gamma^{a}_{bc} = \frac{1}{2}g^{ad} \left(\partial_{b}g_{dc} + \partial_{c}g_{db} -\partial_{d}g_{bc}\right)
$$
called *Christoffel* symbols.

> HW: prove $\Gamma^{a}_{bc}$ is metric connection $\Leftrightarrow$ $\nabla_{c}g_{ab} = 0$

###  $\odot$ Affine flatness

#### Def: (metric flatness)

$\exists$ a special coordinate, s.t. $g_{ab}$ is constant everywhere, e.g.
$$
g_{ab} = \eta_{ab}
= \begin{pmatrix}
-1 & 0 & 0 & 0\\
 0 & 1 & 0 & 0\\
 0 & 0 & 1 & 0\\
 0 & 0 & 0 & 1\\
\end{pmatrix}
$$

#### Theorem: (metrix flatness)

A metric is flat $\Leftrightarrow$ $R^{a}_{bcd} = 0$













That is, once we identify
$$
\Gamma^{a}_{bc} = \left\{\begin{pmatrix}a\\bc\end{pmatrix}\right\}
$$
 then
$$
\text{affine flatness $(\Gamma^{a}_{bc}=0)$} = \text{metrix flateness $(g_{ab}=\text{constant})$}
$$

## Riemannian tensor

#### symmetry

- $R^{a}_{bcd}$​ has symmeties.
- So that $g_{ae}R^{e}_{bcd} = R_{abcd}$ has $4^{4}=256$ components?

In fact,
$$
\begin{aligned}
R_{abcd} &= - R_{bacd}\quad (a\leftrightarrow b)\\
R_{abcd} &= - R_{abdc}\quad (c\leftrightarrow d)\\
R_{abcd} &= - R_{cdab}\quad (ab\leftrightarrow cd)\\
\end{aligned}
$$

#### summation 

$$
R_{abcd} + R_{adbc} + R_{acbd} = 0
$$

we can check that in the geodesic equation.

>  **Ricci tensor**
> $$
> R_{ab} = R^{c}_{acb}
> $$
> 

> **Ricci scalar**
> $$
> g^{ab}R_{ab} = {R^{a}}_{a} = R
> $$

> **Einstein equations**
>
> - vacuum equation
>     $$
>     R_{ab} - \frac{1}{2} g_{ab}R = 0
>     $$
>     
>
> - with matter 
>     $$
>     R_{ab} - \frac{1}{2} g_{ab}R = \frac{8\pi G}{c^4} T_{ab}
>     $$
>     where $T_{ab}$ is energy-momentum tensor.