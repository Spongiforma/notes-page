+++
title = "Mechanics"
author = ["root"]
draft = false
+++

## Analytical mechanics {#analytical-mechanics}


### EL equations {#el-equations}

L = T - V

\\[
\dv{t}\left(\pdv{L}{\dot x}\right) = \pdv{L}{x}
\\]

-   Generalised momentum

\\[
\pdv{L}{\dot q} = p
\\]

-   Generalised force

\\[
\pdv{L}{q} = \dot{p}
\\]


#### Cyclic coordinate {#cyclic-coordinate}

When the Lagrangian does not depend on a coordinate qk:

\\[
\pdv{L}{\dot q\_k} = C
\\]

This is also generalised momentum.

q_k is thus a cyclic coordinate.


#### Energy conservation {#energy-conservation}

\\[
\pdv{E}{t} = -\pdv{L}{t}
\\]

\\[
E = \left(\sum\_{i=1}^N \pdv{L}{\dot q\_i}\dot{q\_i}\right) - L
\\]

If L has no time dependence, then E is conserved.

E is indeed total energy when the new coordinate q is not related to the old coordinate x with a time dependence \\(x = x(q,t)\\) or qdot dependence \\(x = x(q,\dot{q})\\).


#### Noether's theorem {#noether-s-theorem}

For each symmetry of the Lagrangian, there is a conserved quantity.

Let the Lagrangian be invariant to first order in the small number \\(\epsilon\\).

\\[
q\_i \to q\_i + \epsilon K\_i(q)
\\]

each K_i(q) may be a function of all the q_i and need not be constant.

The quantity:

\\[
P(q,\dot{q}) = \sum\_i \pdv{L}{\dot q\_i}K\_i(q)
\\]

does not change with time and has the generic name of consered momentum.

Example:

For \\(L = (m/2)(5\dot{x}^2 - 2\dot{x}\dot{y} + 2\dot{y}^2) + C(2x-y)\\), K_x = 1 and K_y = 2:

\\[
P = \pdv{L}{\dot{x}}K\_x + \pdv{L}{\dot y}K\_y = m(3\dot{x} + 3\dot{y})
\\]


### Constraints {#constraints}

When the constraint has the form,

\\[
f(\bm{r\_1},\bm{r\_2},\ldots,t) = 0
\\]

then it is said to be **holonomic**. Otherwise they are nonholonomic.

Equations of constraints which explicitly contain time as a variable are called **rheonomous** while those which don't are called **scleronomous**.


### Velocity-dependent potentials {#velocity-dependent-potentials}

\\[
Q\_j = -\pdv{U}{q\_j} + \dv{}{t} \pdv{U}{\dot{q}\_j}
\\]


### Dissipation forces {#dissipation-forces}

If not all the forces can be derivable from a potential, then EL equations can be written in the form,

\\[
\dv{}{t} \pdv{L}{\dot{q}\_j} - \pdv{L}{q\_j} = Q\_j
\\]

Often the frictional force is proportional to the velocity of the particle. e.g. \\(F\_{x} = -k\_xv\_x\\). Thus we may derive them from **Rayleigh's dissipation function**, \\(\mathcal{F}\\).

\\[
\mathcal{F} = \frac12 \sum\_i \left \left(k\_x v^2\_{ix} + k\_y v^2\_{iy} + k\_z v^2\_{iz}\right)
\\]

where the summation is over the particles of the system.

Thus, \\(F\_{x\_i} = - \pdv{\mathcal{F}}{v\_{x\_i}}\\).

Or symbolically,

\\[
\bm{F} = -\grad\_v\mathcal{F}
\\]

\\(2\mathcal{F}\\) is the also the rate of energy dissipation due to friction.

The generalized force is given by,

\\[
Q\_j = -\pdv{\mathcal{F}}{\dot{q}\_j}
\\]


## Central forces {#central-forces}

Only depends of radius from source. Motion takes place in a plane.


### Effective potential {#effective-potential}

Since L is conserved, express w as L/mr^2

\\[
V\_{eff} = \frac{L^2}{2mr^2} + V( r)
\\]

the first term on RHS is often called the L barrier. This does not hold if v(r) goes to -infty faster than -1/r^2

\\[
F\_{eff} = \frac{L^2}{mr^3} - V'( r)
\\]

We may use it to find r(t) and theta(t) in terms of t:

\\[
\dv{r}{t} = \pm \sqrt{\frac{2}{m}} \sqrt{E - \frac{L^2}{2mr^2} - V( r)}
\\]

or r(theta):

\\[
\left(\frac{1}{r^2}\dv{r}{\theta}\right)^2 = \frac{2mE}{L^2} - \frac{1}{r^2} - \frac{2mV( r)}{L^2}
\\]

or Binet's equation:

\\[
\left(1+\dv[2]{}{\theta}\right)u = -\frac{m}{L^2u^2}F(u)
\\]

\\[
\dv[2]{u}{\theta} = -\frac{m}{L^2}U\_{eff}'(u)
\\]


### Gravitation {#gravitation}

The motion of particles is like (earth-sun model):

\\[
\frac{1}{r} = \frac{m\alpha}{L^2}(1+e\cos\theta)
\\]

Or in terms of specific angular momentum, h.

\\[
r = \frac{h^2 / \mu}{1+e\cos\theta}
\\]

where the eccentricity \\(e = \sqrt{1 + \frac{2EL^2}{m\alpha^2}} = \sqrt{1+\frac{2\epsilon h^2}{\mu^2}}\\) , and \\(\alpha = GMm\\), \\(\mu = GM\\).


#### Kepler's equation {#kepler-s-equation}

\\[
r = a(1-e\cos\psi)
\\]

**Kepler's equation**

\\[
\omega t =\psi - e \sin\psi
\\]


#### Eccentricity and orbits {#eccentricity-and-orbits}

<!--list-separator-->

-  Circle (e = 0)

<!--list-separator-->

-  Ellipse (0 &lt; e &lt; 1)

    WLOG, let a be the semi-major axis and b be the semi-minor axis. c is the distance of a focus to the centre.

    \\[
    e = \sqrt{1 - \frac{b^2}{a^2}}
    \\]

    From the geometrical definition of a ellipse and the above definition,

    \\[
    c = ae
    \\]

    \\[
    r = \frac{a(1-e^2)}{1+e\cos\theta}
    \\]

    <!--list-separator-->

    -  Orbits

        \\[
        \epsilon = -\frac{\mu}{2a}
        \\]

        \\[
        h = \sqrt{\mu a (1-e^2)}
        \\]

        Vis-viva equation:

        \\[
        v^2 = \mu\left( \frac{2}{r} - \frac{1}{a} \right)
        \\]

<!--list-separator-->

-  Parabola (e = 1)

    In polar coordinates, \\(r = \frac{p}{1+\cos\theta}\\)

    For a left facing parabola, \\(y^2 = -4ax\\), where a is the distance between the vertex and the focus of the parabola.

    \\[
    r = \frac{2a}{1+\cos\theta}
    \\]

    <!--list-separator-->

    -  Orbits

        \\[
        \epsilon = 0
        \\]

        \\[
        h = \sqrt{2a\mu}
        \\]

<!--list-separator-->

-  Hyperbola (e &gt; 1)

    \\[
    \frac{x^2}{a^2} - \frac{y^2}{b^2} = 1
    \\]

    \\[
    e = \sqrt{1+\frac{b^2}{a^2}}
    \\]

    \\[
    r = \frac{a(e^2-1)}{1+e\cos\theta}
    \\]

    \\[
    r\_{min} = \sqrt{\frac{\mu^2}{v\_0^4} + b^2} - \frac{\mu}{v\_0^2}
    \\]

    <!--list-separator-->

    -  Orbits

        \\[
        \epsilon = \frac{\mu}{2a}
        \\]
        \\[
        h = \sqrt{\mu a (e^2 - 1)}
        \\]


## Waves {#waves}


### Energy density {#energy-density}

In general.

\\[
\epsilon \propto A^2
\\]

For string waves:

KE:
\\[
\epsilon\_{KE} = \frac12 \mu \left(\pdv{\psi}{t}\right)^2
\\]\\
PE:

\\[
\dd{W} = T\Delta = T \frac12 \left(\pdv{\psi}{x}\right)^2 \dd{x} = \dd{U}
\\]

The total energy per unit length is thus:

\\[
\epsilon(x,t) = \frac{\mu}{2} \left(\left(\pdv{\psi}{t}\right)^2 + v^2\left(\pdv{\psi}{x}\right)^2 \right)
\\]

Further more, for a travelling wave, we can use the relationship \\(\psi\_t = \mp v \psi\_x\\) to get:

\\[
\epsilon(x,t) = \mu \psi\_t^2
\\]

Note that this implies that segments of string the possess the greatest KE also have the greatest PE.


### Power {#power}

Power is similarly proportional to the square of the amplitude.

For string waves, note that the transverse (vertical) force on a point Q on the string on the left of Q is \\(-T\sin\theta = -T\psi\_x\\). Power is thus:

\\[
P = -T\psi\_x\psi\_t
\\]

Again using \\(\psi\_t = \mp v \psi\_x\\) for a rightwards/leftwards travelling wave,

\\[
P = \pm \epsilon(x,t) v
\\]


### Sound waves {#sound-waves}

\\[
\psi^p = \dd{P} = -B\frac{\dd{V}}{V}
\\]

Taking a control small control volume that gets compressed,

\\[
\dd{V} = A[\psi(x+\dd{x}) - \psi(x)]
\\]

It can then be seen that:

\\[
-B\psi\_x = \psi^p
\\]

Using N2L:

\\[
-[\psi^p(x+\dd{x}) - \psi^p(x)] A = \rho A \dd{x} \psi\_{tt}
\\]

It can then be shown that both \\(\psi\\) and \\(\psi^p\\) obey the wave equation, though for sinusoidal equation for instance \\(\psi^p\\) leads \\(psi\\) by \\(\pi/2\\) in the direction of propogation (From the second last equation).

Due to collisions, heat flow is much slower than oscillation so the process is usually adiabatic and \\(B =\gamma p\_0\\).


#### Energy density {#energy-density}

\\[
\epsilon\_{KE} = \frac12 \rho (\psi\_t)^2
\\]

Since the potential energy is given by \\(-\int p \dd{V}\\) from \\(\p\_0\\) to \\(\p\_0 +\psi^p\\), using our \\(B\\) we can show:

\\[
\epsilon\_{PE} = \frac{B}{2} \psi\_x^2
\\]

Again for travelling waves:

\\[
\epsilon = \rho \psi\_t^2
\\]


#### Power {#power}

Same as strings but \\(Av\\) instead of \\(v\\).


### Plane waves {#plane-waves}

\\(\psi = \Re\left\\{ e^{\bm{k}\cdot\bm{r}-\omega t}\right\\}\\)

where \\(\norm{\bm{k}}^2 = { \omega^2 \over v^2 }\\)

For spherically symmetric waves, the general solution is:

\\[
\psi( r) = \frac{A}{r} \cos(kr-\omega t + \phi)
\\]


### Wave at boundary {#wave-at-boundary}

A wave is traveling towards a boundary from the left, which results in a reflected and transmitted wave. We impose a continuity constraint:

\\[
\psi^i(0,t) + \psi^r(0,t) = \psi^t(0,t)
\\]

Furthermore, transverse tension must cancel.

\\[
T\_1[ \psi^i\_x(0,t) + \psi^r\_x(0,t) ] = T\_2 \psi\_x^t(0,t)
\\]

Then defining the impedence \\(Z = \frac{T}{v} = \sqrt{T\mu}\\), we get:

\\[
Z\_1 \psi^i(0,t) - Z\_1 \psi^r(0,t) = Z\_2 \psi^t(0,t)
\\]

We obtain the transmission and reflection relations:

\\[
\psi^r(0,t) = \frac{Z\_1 - Z\_2}{Z\_1 + Z\_2}\psi^i(0,t)
\\]

\\[
\psi^t(0,t) = \frac{2Z\_1}{Z\_1 + Z\_2} \psi^i(0,t)
\\]

(Notice the analogy with elastic collisions, with impedence being analagous to mass)

We call each coefficient the reflection and transmission coefficients (\\(R\\) and \\(T\\)) respectively, where \\(T = 1 + R\\).

To find the resultant waves after collision, we makes use of the fact that the waves are travelling (like in _method of characteristics_).

\\[
\psi^t(x,t) = T\psi^i\left(\frac{v\_1}{v\_2}x,t\right)
\\]

(the wavelength is broadened by \\(v\_2/v\_1\\))

\\[
\psi^r(x,t) = R\psi^i(-x,t)
\\]


### Limiting cases of impedences {#limiting-cases-of-impedences}

For non-negative impedences,

\\[
\abs{R} \leq 1
\\]

\\[
0 \leq T \leq 2
\\]


#### z2 &gt; z1 {#z2-z1}

The large force at the ring wrests the incoming wave down.

\\[
-1 \leq R < 0
\\]

\\[
0 \leq T < 1
\\]

Since R is negative, it goes through a $&pi;$-radian phase shift.

At the extreme, the entire incident wave is reflected


#### z2 &lt; z1 {#z2-z1}

\\[
0 < R \leq 1
\\]

\\[
1 < T \leq 2
\\]

There is no longer a phase shift. At the extreme, the displacement at the origin is twice the displacement than what would have been produced by incident wave alone.


#### z2=z1 {#z2-z1}

\\[
T = 1, R=0
\\]

Fully transmitted. Can occur even when the string is inhomogenous by scaling tension and mass density equally.


#### Sound waves {#sound-waves}

For sound waves

\\(Z = \frac{p\_0}{v} = \sqrt{\frac{\rho p\_0}{\gamma}} = \frac{\rho v}{\gamma}\\)


## Special relativity {#special-relativity}


### Loss of simultaneity {#loss-of-simultaneity}

Last car first: The clock on the back of a moving train is ahead of the front clock.


### Time dilation {#time-dilation}

Lorentz factor:

\\[
\gamma = \frac{1}{\sqrt{1-v^2/c^2}} \geq 1
\\]

\\[
t\_B = \gamma t\_A
\\]


#### Identities {#identities}

\\[
\gamma^2 - 1 = \gamma^2\beta^2
\\]

\\[
\gamma(1-\beta) = \sqrt{\frac{1-\beta}{1+\beta}}
\\]

\\[
\gamma(1 + \beta) = \sqrt{\frac{1+\beta}{1-\beta}}
\\]


### Length contraction {#length-contraction}

For distances along the direction of relative velocity.

\\[
l = \frac{l'}{\gamma}
\\]


### Lorentz tranform {#lorentz-tranform}

If S' is a coordinate system moving at speed v wrt S.

\\[
x = \gamma(x' + vt')
\\]

\\[
t = \gamma(t' + vx'/c^2)
\\]

The inverse Lorentz transforms are given by the tranformation v-&gt; v'.

\\[
\mqty(x \\\ ct) = \mqty(\gamma & \gamma \beta \\\ \gamma\beta & \gamma ) \mqty(x' \\\ ct')
\\]

where \\(\beta = v/c\\).


### Velocity addition {#velocity-addition}

S' moves \\(v\_2\\) wrt to frame S. An object moves \\(v\_1\\) wrt to frame S'. The velocity of the object wrt S is:

\\[
u = \frac{v\_1 + v\_2}{1+v\_1v\_2/c^2}
\\]

This scenario is equivalent to A moving \\(v\_1\\) wrt C to the right and B moving \\(v\_2\\) wrt C to the left, and we ask the velocity of A wrt to B.