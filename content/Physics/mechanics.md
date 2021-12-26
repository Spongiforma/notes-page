+++
title = "Mechanics"
author = ["root"]
draft = false
+++

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