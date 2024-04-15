### Relativistic mass

- rest mass: $m_0$
- mass $m = m(u)$, where $m(0) = m_0$

here is a example

- In $S$​, we have 

    <u>Fig20 collision in S</u>

    - mass conservation: $m(u) + m_0 = M(U)$

    - momentum conservation: $m(u)\cdot u = M(u)\cdot U = (m(u)+m_0)U$​

    resulting that $\displaystyle \Rightarrow m(u) = m_0\left(\frac{U}{u-U}\right)$

- In $S'$ ( relative to $S$ by $U$ ), we have

    <u>Fig21 collision in S'</u>

    Using the addition formula for velocity 
    $$
    u = \frac{U+U}{1+UU/c^2} = \frac{2U}{1+U^2/c^2}
    $$
    solving that
    $$
    U = \frac{c^2}{u}\left(1 \pm \sqrt{1-u^2/c^2}\right)
    $$
    since  $U=U(u=0) = 0$, we choose the negative sign
    $$
    U = \frac{c^2}{u}\left(1 - \sqrt{1-u^2/c^2}\right)
    $$

so the mass we have
$$
\begin{aligned}
m(u) &= m_0 \cdot \frac{1}{u/U - 1}\\ 
&= \frac{m_0}{\frac{c^2}{u^2}\left(1-\sqrt{1-u^2/c^2}\right)-1}\\
&= ...\\
&= \frac{m_0}{\sqrt{1-u^2/c^2}}\\
&= \gamma m_0
\end{aligned}
$$
<u>Fig22 - mass of velocity</u>

### Relativistic energy

Notice the relativistic mass
$$
m(u) = \frac{m_0}{\sqrt{1-u^2/c^2}} = m_0 \left(1-u^2/c^2\right)^{-1/2}
$$
If now $u\ll c$ we have
$$
m = m_0 \left(1-u^2/c^2\right)^{-1/2} 
\simeq m_0 \left(1+\frac{1}{2}\frac{u^2}{c^2} + \mathcal{O}\left(\frac{u^4}{c^4}\right)\right)
$$
so that the energy $E=m(u)c^2$ is 
$$
E \simeq m_0c^2 + \frac{1}{2}m_0u^2 + \cdots
$$
where 

- $E_0 = m_0c^2$ is called rest energy 
- $m_0u^2/2$ is called kinetic energy

and $E(u) = m(u)\cdot c^2$ is called the energy of a moving particle with rest energy $E_0 = m_0c^2$.

Here, is another example

<u>Fig23 - two particle collides</u>

$m(v_1) \cdot v_1 + \bar{m}(\bar{v}_1) = m(v_2) \cdot v_2 + \bar{m}(\bar{v}_2)$

then approximately $u\ll c$
$$
m_0 v_1 + \bar{m}\bar{v}_1 = m_0 v_2 + \bar{m}\bar{v}_2
$$
it becomes the momentum conservation in classical mechanics.

### In summary
- Relativistic mass
    $$
    m(u) = \frac{m_0}{\sqrt{1-u^2/c^2}}
    $$

- Relativistic energy
    $$
    E(u) = m(u)c^2 = \frac{m_0c^2}{\sqrt{1-u^2/c^2}}
    $$
    
- Relativistic momentum
    $$
    \vec{p}(u) = m(u)\vec{u} = \frac{m_0\vec{u}}{\sqrt{1-u^2/c^2}}
    $$

> notice that $\displaystyle \vec{u} = \frac{\vec{p}c^2}{E}$

In fact 
$$
\begin{aligned}
E^2 - \vec{p}^2 c^2 
&= \frac{m_0^2c^4 - m_0^2\vec{u}^2c^2}{1-u^2/c^2}\\
&= m_0^2c^4 \frac{1 - u^2/c^2}{1-u^2/c^2}\\
&= m_0^2c^4
\end{aligned}
$$

It is a Lorentz invariant

- 4 momentum $P^{\mu} = \left(P^{0}, P^{1},P^{2},P^{3}\right) = \left(E/c, \vec{p}\right)$
    $$
    \left(\frac{E}{c}\right)^2 - \vec{p}^2 = m_0^2c^2
    $$

- space time $x^{\mu} = (ct,\vec{x})$
    $$
    ct^2 - \vec{x}^2 = \mathrm{constant.}
    $$

> Rmk (Lorentz transformation):
> $$
> \begin{cases}
> ct' = \gamma (ct - vx/c)\\ 
> x' = \gamma (x-vt)
> \end{cases}
> \leftrightarrow
> \begin{cases}
> E'/c = \gamma (E/c - p_xv/c)\\ 
> p_x' = \gamma (p_x - vE/c^2)
> \end{cases}\text{ or }
> \begin{cases}
> E/c = \gamma (E'/c + p_xv/c)\\ 
> p_x = \gamma (p_x + vE/c^2)
> \end{cases}
> $$
> If $v=u$​
> $$
> \begin{cases}
> E/c = \gamma (E'/c + 0) = m(u)c^2\\ 
> p_x = \gamma (0 + vE/c^2) = m(u)u
> \end{cases}
> $$

Here is a example for massive particle $m_0 \neq 0$
$$
E = \pm \sqrt{\vec{p}^2c^2 + m_0^2 c^4}
$$
<u>Fig24 - dispersion of energy</u>

Here is a example for photon
$$
E = pc
$$
notice $T' = kT_0$ and $T = 1/\nu$
$$
T' = kT_0,\quad k>1
\quad\Rightarrow\quad \frac{1}{\nu} 
= \sqrt{\frac{1+v/c}{1-v/c}} \frac{1}{\nu_0}
$$
so the ratio between two frequence
$$
\frac{v_0}{v} = \sqrt{\frac{1+v/c}{1-v/c}}
$$
and the energy
$$
\begin{aligned}
E &= \gamma (E_0 - vp_0)\\
&= \gamma (E_0 - vE_0/c)\\ 
&= \gamma E_0 \left(1-v/c\right)\\ 
&= E_0 \sqrt{\frac{1+v/c}{1-v/c}}
\end{aligned}
$$
And the ratio between two enrgy
$$
\frac{E_0}{E} = \sqrt{\frac{1+v/c}{1-v/c}} = \frac{\nu_0}{\nu} > 1
$$
Then we also have 
$$
\frac{E_0}{\nu_0} = \frac{E}{\nu} = \mathrm{constant.}
$$
**Example: (uniform proper acceleration)**

at any time $t$, the speed of rocket $u(t)$ in $v = u(t)$ frame $S'$

> Uniform: $u'(t) = 0$ and $a'(t') = a = \mathrm{constant.}$

Recall that: $\displaystyle \frac{du'}{dt'} = a$, by L.T.
$$
\frac{du}{dt} = \frac{1}{\gamma^3(1+u'u/c^2)} = \frac{du'}{dt'} = a\cdot (1-u^2/c^2)^{3/2}
$$
integral both side, 
$$
\frac{1}{(1-u^2/c^2)^{3/2}} du = a dt
$$
solving that
$$
u(t) = \frac{a(t-t_0)}{\sqrt{1+a^2(t-t_0)^2/c^2}}
$$
when $t\to \infty$，$u(t) = const$​

If $u = u_0 + at$, when $t \to \infty$ , $u(t)\to\infty$

Also, if we calculate the trajectory
$$
\frac{dx}{dt} = u(t) = \frac{a(t-t_0)}{\sqrt{1+a^2(t-t_0)^2/c^2}}
$$
Solving that
$$
x - x_0 = \frac{c}{a}\sqrt{c^2+a^2(t-t_0)^2} - \frac{c^2}{a}
$$
in other form
$$
\frac{(x-x_0+c^2/a)^2}{(c^2/a)^2} - \frac{(ct-ct_0)^2}{(c^2/a)^2} = 1
$$
 choose $x_0 - x^2/a = t_0 = 0$​

<u>Fig25 - uniformly accelerating observer</u>

If the observer in the rocket emmit a photon or a wave signal (speed: $c$)

<u>Fig25 - uniformly accelerating observer shoot a photon</u>

the light cone cone be viewed as information barrier.
