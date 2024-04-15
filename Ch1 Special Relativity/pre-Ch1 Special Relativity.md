# Ch.1 Special Relativity (Review)

space time $(t,\vec{x})\to$ event 

for (1+1)-dim space time

<u>Fig1 - world line</u>

An observer : with a clock and a ruler

Constitutes and inertial frame

## Newtonian theory

- two observer:  $(t,x,y,z)$ and $(t',x',y',z')$

- relative speed $v$ in $x$-direction

### Galilean transformation

$$
\left\{\begin{aligned}
x &= x' + vt\\
y &= y'\\
z &= z'\\
t &= t'\quad \text{(time is absolute)}\\
\end{aligned}\right.
$$

### Principle of equivalence in Newton's theory

1. For the event in $S$ and $S'$, time is absolute
    $$
    \begin{aligned}
    S  &: (t,x,y,z)\\
    S' &: (t',x',y',z')
    \end{aligned}
    $$
    If we want to measure the length of a moving object

    > We need to measure the coordinates of ends simutaneously.
    >
    > <u>Fig2 - measure ends</u>

2. speed 

    $$
    \begin{cases}
    \dot{x} = \dot{x}' + v\\
    \dot{y} = \dot{y}'\\
    \dot{z} = \dot{z}'\\
    \end{cases}
    $$

3. accerleration 

    $$
    \ddot{x} = \ddot{x}',
    \quad \ddot{y} = \ddot{y}',
    \quad \ddot{z} = \ddot{z}'
    $$

## Special Relativity

> Einstein: Two postitulates of S.R.
>
> P1. All inertial observers are eqivalent.
>
> P2. The speed of light of light $c$ is the smae for all observers ($c=299792458\,\mathrm{m/s}$).

If we set $c=1$ (relativistic unit)

<u>Fig 3 - xt diagram</u>

### $\odot$ Lorentz transformation (*Bondi* $k$-factor)

> $k$ factor characterize the difference between Newton's theory and S.R.

<u>Fig4 - xt diagram with AB</u>

so that $k=k(v)$, and it must be a linear relation between $(t,x)$ and $(t',x')$ since the free motion must be the same, i.e.
$$
\text{free motion:}\quad
\begin{cases}
x = x_0 + u t\\
x' = x_0' + u' t'
\end{cases}
$$
<u>Fig5 - triangle</u> 

then if $t_1=T$ and $t_2=k^2T$ (see Fig5 - t1t2), we have
$$
\begin{cases}
t = (k^2+1)T/2\\
x = (k^2-1)T/2\\
\end{cases}
$$
since $v=x/t=(k^2-1)/(k^2+1)<1$ we have the factor
$$
k=\sqrt{\frac{1+v}{1-v}}
$$

> Rmk (Relativistic Doppler effect):
>
> The frequence $\omega = 2\pi/T$, we have
> $$
> \begin{aligned}
> T\to T'=kT\\
> \omega \to \omega' = \omega/k
> \end{aligned}
> $$
> If $v>0\Rightarrow k>1$: $\omega'<\omega$ (red shift)
>
> If $v<0\Rightarrow k<1$: $\omega'<\omega$ (blue shift)

In Newton's theory 
$$
\begin{cases}
x=x'+vt\\
\dot{x} = \dot{x}' + v\quad\text{(Additoin formula)}
\end{cases}
$$
<u>Fig6 - ABC world line</u>
$$
\begin{aligned}
k_{AB} &= \sqrt{\frac{1+v_{AB}}{1-v_{AB}}}\\
k_{BC} &= \sqrt{\frac{1+v_{BC}}{1-v_{BC}}}\\
k_{AC} &= \sqrt{\frac{1+v_{AC}}{1-v_{AC}}} 
        = \sqrt{\frac{(1+v_{AB})(1+v_{BC})}{(1-v_{AB})(1-v_{BC})}}\\
\end{aligned}
$$
solving that 
$$
v_{AC} = \frac{v_{AB}+v_{BC}}{1+v_{AB}v_{BC}} = \frac{v_{AB}+v_{BC}}{1+v_{AB}v_{BC}/c^2}
$$

> example: 
>
> if $v_{BC} = c$​, we have $\displaystyle v_{AC}=\frac{c+v_{BC}}{1+v_{BC}c/c^2} = c$
>
> if $v_{AC} = c$, we have $\displaystyle v_{AC}=\frac{v_{AC}+c}{1+cv_{BC}/c^2} = c$

In fact,
$$
v_{AV}-1 = \frac{(v_{AC}-1)(1-v_{BC})}{1+v_{AB}v_{BC}} < 0
$$
when $v_{AB},v_{BC}<1$: S.R. $\to$ Newton

> Rmk:
>
> 1. massive particles $m\neq 0$: $v<1$ or $v<c$
>
> 2. Massless particle $m=1$: $v=1$ or $v=c$
>
>     e.g. *photon*, *graviton*, ~~*neutrino*~~

What about the Relation between two space time coordinate of the same event $P$:

<u>Fig7 lorentz - transformation</u>

by $k$-factor

1. $t'-x'=k(t-x)$
2. $t+x=k(t'+x')$

solving that
$$
\begin{aligned}
t' = \frac{t-vx}{\sqrt{1-v^2}}\\
x' = \frac{x-vt}{\sqrt{1-v^2}}
\end{aligned},\quad\text{where $(c=1)$}.
$$

> Rmk:
>
> 1. $t^2-x^2 = (t')^2 - (x')^2$ (Nom-Euclidean) It's called *Minkkowski space*.
>
> 2. comparision
>
>     | Galilean  | Lorentz                        |
>     | --------- | ------------------------------ |
>     | $t'=t$    | $t'=\frac{t-vx}{\sqrt{1-v^2}}$ |
>     | $x'=x-vt$ | $x'=\frac{x-vt}{\sqrt{1-v^2}}$ |
>     | $y'=y$    | $y'=y$                         |
>     | $z'=z$    | $z'= z$                        |
>
>     <u>Fig8 -moving frame</u> 
>
> 3. **Definition**: interval between two event $P_1$ and $P_2$:
>
>     - fiinite Interval
>
>     $$
>     s^2 = (t_2-t_1)^2 - (x_2-x_1)^2 - (y_2-y_1)^2 - (z_2-z_1)^2
>     $$
>
>     - infenitestmall interval
>     $$
>     (ds)^2 = (dt)^2 - (dx)^2 - (dy)^2 - (dz)^2
>     $$
>
> 4. revise the order
>     $$
>     \begin{aligned}
>     t' = \frac{t-vx/c^2}{\sqrt{1-v^2/c^2}}\\
>     x' = \frac{x-vt/c^2}{\sqrt{1-v^2/c^2}}
>     \end{aligned}
>     $$

### $\odot$ **Lorentz transformation**

> Einstein: Two postitulates of S.R.
>
> PI. All inertial observers are eqivalent.
> PII. The speed of light of light $c$ is the smae for all observers

By PI, if a particle is free in $S$
$$
\vec{r} = \vec{r}_0 + \vec{u} t \quad\Rightarrow\quad \vec{r}' = \vec{r}_0' + \vec{u}' t'
$$
so the transform is linear
$$
\begin{pmatrix}
ct'\\ x'\\ y'\\ z'
\end{pmatrix}
= L \begin{pmatrix}
ct\\ x\\ y\\ z
\end{pmatrix},
\quad\text{ where } L = 
\begin{pmatrix}
\gamma & -\gamma\beta & 0 & 0\\ 
-\gamma\beta & \gamma & 0 & 0\\ 
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1\\
\end{pmatrix} \text{ and }
\gamma = \frac{1}{\sqrt{1-\beta^2}}, \quad \beta = \frac{v}{c}
$$
By PII, 

<u>FIg9 - sphere</u>
$$
\begin{aligned}
I(t,x,y,z) &= (ct)^2 - x^2 - y^2 - z^2 = 0\\
I(t',x',y',z') &= (ct')^2 - x'^2 - y'^2 - z'^2 = 0
\end{aligned}\quad\Rightarrow\quad I = I'
$$


From boost in $x$-direction, we have $(xt')^2 - x'^2 = (xt)^2 - x^2$

Introducing imaginary time $T = ict$, the equation become 
$$
x^2+T^2 = x'^2 + T'^2,\quad \text{(Euclidean)}
$$
Now we can using a rotation to relate two coordinates
$$
\begin{pmatrix}
x' \\ T'
\end{pmatrix}
=
\begin{pmatrix}
\cos\theta & \sin\theta \\
-\sin\theta & \cos\theta
\end{pmatrix}\begin{pmatrix}
x \\ T
\end{pmatrix}
$$
<u>Fig10 - rotation of coordinates</u>
$$
\vec{r} = x\hat{x} + T\hat{t} = x' \hat{x}' + T' \hat{t}'
$$
then check
$$
\begin{aligned}
\hat{x}' = \cos\theta \hat{x} + \sin \theta \hat{t}\\
\hat{T}' = -\sin\theta \hat{x} + \cos \theta \hat{t}\\
\end{aligned}
$$
First we have $S'$ at rest $0'$ ($x'=0$) $\Rightarrow$ world line is $T'$-axis  $\Rightarrow$ $x\cos\theta + T\sin\theta=0$
$$
v = \frac{x}{t} = \frac{icx}{T} = -ic\tan\theta
$$
Then we can get
$$
\cos \theta = \frac{1}{\sqrt{1+\tan^2\theta}} = \frac{1}{\sqrt{1+(iv/c)^2}} = \frac{1}{\sqrt{1-v^2/{c^2}}} = \gamma
$$
and 
$$
\sin \theta = \tan\theta \cdot \cos\theta = \gamma \cdot \frac{iv}{c}
$$
so the transformation become
$$
\begin{pmatrix}
x' \\ T'
\end{pmatrix}
=
\begin{pmatrix}
\gamma & \gamma iv/c \\
-\gamma iv/c  & \gamma
\end{pmatrix}\begin{pmatrix}
x \\ T
\end{pmatrix}
$$
that is 
$$
\begin{aligned}
x' 
&= \cos\theta x + \sin \theta T = \cos\theta (x+\tan T)\\
&= \gamma \left(x + \frac{iv}{c}T\right) = \gamma (x-vt)\\
t' &= \gamma (t - vx/c^2)
\end{aligned}
$$

> Rmk:
>
> 1. in $x-T$ system, L.T. can be viewedas a rotation with $\theta$ where $\tan\theta = iv/c$
>
> 2. when $v\ll c$ , L.T. $\to$ G.T.
>
> 3. L.T. $L( v )$ forms a group
>     1. Identity $L(0) = \mathbb{I}$
>     
>     2. Inverse $L^{-1}(v) = L(-v)$ $\Rightarrow$ $L(v) L(-v) = \mathbb{I}$
>     
>     3. Closure $L(v')L(v) = L(v'')$: ex:
>         $$
>         \begin{aligned}
>         \tan\theta'' &= \tan(\theta+\theta') = \frac{\tan\theta + \theta'}{1- \tan\theta \tan\theta'}\\
>         &= \frac{\frac{i(v+v')}{c}}{1+\frac{vv'}{c^2}} = \frac{iv''}{c}
>         \Rightarrow v'' = \frac{v" v'}{1+vv'/c^2}
>         \end{aligned}
>         $$
>     
>     4. associativity
>         $$
>         L_3\cdot (L_2\cdot L_2) = (L_3\cdot L_2)\cdot L_1
>         \quad\Leftrightarrow\quad
>         \theta_3 + (\theta_2 + \theta_1) = \cdot (\theta_3 + \theta_2) + \theta_1
>         $$

### $\odot$ Length contraction
measure the length in $S$ and $S'$ frame
Let $\ell_0 = x'_B - x'_A$ at real in $S'$ called *proper length*

<u>Fig11 - length contraction</u>

measure $x_A$ and $x_B$ in $S$ at the same time $t_A=t_B$, then
$$
\ell = (x_B-x_A)
$$
and 
$$
\begin{aligned}
x_A' = \gamma (x_A - vt)\\
x_B' = \gamma (x_B - vt)\\
\end{aligned}
\quad\Rightarrow\quad
(x_B'-x_A') = \gamma (x_B-x_A)
\quad\Rightarrow\quad
\ell_0 = \gamma \ell,\quad (\gamma>1\Rightarrow \ell<\ell_0)
$$

### $\odot$ time dialation

Let $t_0$ proper-time (co-miving time) in $S'$, which means the clock is moving with the obsever.

So that in $S$ we have the time interval
$$
\Delta t = \gamma (\Delta t' + v\Delta '/c^2)
\quad\Rightarrow\quad
T = \gamma T_0 > T_0
$$

> Rmk experiment 1: the particle from the universe have more life time
>
> <u>Fig12 - particle from universe</u>
>
> Rmk experiment 2: clock moving very fast

### $\odot$ velocity

We define the velocity to be 
$$
\vec{u} = \frac{d\vec{x}}{dt} = \left(u_x,u_y,u_z\right)
= \left(\frac{du_x}{dt},\frac{du_y}{dt},\frac{du_z}{dt}\right)
$$

The L.T. result that 
$$
\begin{cases}
dt' = \gamma (dt - vdx/c^2)\\
dx' = \gamma (dx - vdt/c^2)\\
dy' = dy\\
dz' = dz
\end{cases}
$$
so the velocity 
$$
u_x' = \frac{dx'}{dt'} 
= \frac{\gamma (dx-vdt)}{\gamma (dt-vdx/c^2)}
= \frac{u_x-v}{1-vu_x/c^2}
$$
also 
$$
u_y = \frac{u_y}{\gamma (1-u_xv/c^2)}
,\quad
u_z = \frac{u_z}{\gamma (1-u_xv/c^2)}
$$

### $\odot$ accerleration 

$$
{du_x} = \gamma^{-2} \frac{1}{(1+u_x'v/c^2)} du_x
,\quad 
dt' = \gamma (dt-vdx/c^2)
$$

and 
$$
dt = \gamma (dt' + vdx'/c^2) = \gamma (1+v\frac{dx'}{dt'}/c^2) dt' 
= \gamma (1+vu_x/c^2) dt'
$$
solving that 
$$
a_x = \frac{du_x}{dt} = \gamma^{-3} \frac{1}{\left(1+u_x'v/c^2\right)^3} a_x'
$$

### $\odot$ Simultaneity (同時性)

Simultaneity is not exist ? train 

<u>Fig13 - train</u>

light cone

<u>Fig14 - light cone</u>

### $\odot$ spacetime diagram  (real time)

$$
\begin{aligned}
t' &= \gamma (t-vx/c^2) &&\to ct' = \gamma (ct-vx/c)\\
x' &= \gamma (x-vt) &&\to x' = \gamma \left(x-\frac{v}{c}(ct)\right)
\end{aligned}
$$

> Recall: in $S'$
>
> - $x'$-axis ($t'=0$) $\Rightarrow$ $\displaystyle ct=\left(\frac{v}{c}\right)x$
> - $t'$-axis ($x'=0$) $\Rightarrow$ $\displaystyle x=\left(\frac{v}{c}\right)ct$

<u>FIg15 - spacetime diagram</u>

- For $v>0$, folding the axis toward
- For $v<0$, expanding the axis outward

<u>FIg16 - spacetime diagram simultaneity</u>

> Rmk:
>
> <u>Fig17 - contracton in space time diagram</u>

### $\odot$ Calibration of length and time scale

<u>Fig18 - hyperbola in space time diagram </u>

How to calibration rule and clock $\Rightarrow$ using invariant
$$
x^2 - (ct)^2 = x'^2 - (ct')^2
$$
