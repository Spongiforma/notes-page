+++
title = "Linear Momentum"
author = ["root"]
draft = false
+++

## Linear Momentum {#linear-momentum}

\\[
\overrightarrow{p} = m\overrightarrow{v}
\\]

Since \\(m\\) is a scalar \\(\overrightarrow{p}\\) always has the same direction as
\\(\overrightarrow{v}\\).


### Newton's second law {#newton-s-second-law}

"The rate of change of the momentum of a particle is equal to the net force
acting on the particle and in the direction of that force"


### For a system of particles {#for-a-system-of-particles}

\\[
\overrightarrow{P} = M\overrightarrow{v}\_{com},
\\]
\\[
\overrightarrow{F}\_{net} = \dv{\overrightarrow{p}}{t}
\\]


## Impulse {#impulse}

When a bat collides with a ball, the ball experiences a \\(\overrightarrow{F}(t)\\)
which varies during the collision and changes the linear momentum of the ball.

From this, impulse \\(\overrightarrow{J}\\) is defined as follows.

\\[
\overrightarrow{J} = \int\_{t\_i}^{t\_f} \overrightarrow{F}(t) dt
\\]

(also the area under a graph of \\(F\\) against \\(t\\))
thus, the change in an object's momentum is equal to the impulse on the object

\\[
\Delta\overrightarrow{p} = \overrightarrow{J}  \text{(linear momentum-impulse
theorem)}
\\]

If we know the average magnitude of the force and duration of the collision:

\\[
J = F\_{avg}\Delta t.
\\]


### Why is landing in snow safer than landing on bare ground? {#why-is-landing-in-snow-safer-than-landing-on-bare-ground}

The change in linear momentum is the same in both scenarios and thus the impulse
of both collisions are equivalent. Thus, since landing in snow results in a
greater \\(t\\), \\(\rightoverarrow{F}\\) should be less in order to achieve the same
impulse.


## Series of collisions {#series-of-collisions}

Let's consider the force on a body when it undergoes a series of identical,
repeated collisions. For instance, a tennis ball firing machine rapidly
firing at a wall. Each collision would produce a force on the wall, but what we
see is the average force on the wall during the bombardment.

A steady stream of projectile bodies, with identical mass \\(m\\) and linear momenta
\\(m\overrightarrow{v}\\) moves along an \\(x\\) axis and collides with the target body
\\(n\\) times in a time interval \\(\Delta t\\).  Thus, each projectile has initial
momentum \\(mv\\) and undergoes a change \\(\Delta p\\) in linear momentum because of
the colision. The total change in linear momentum for n particles for \\(n\\)
projectiles during interval \\(\Delta t\\) is \\(n \Delta p\\).  The resulting impulse
\\(\overrightarrow{J}\\) on the target during \\(\Delta t\\) is along the \\(x\\) axis and
has the same magnitude of \\(n \Delta p\\) but is in the opposite direction.

This results in the following relation:

\\[
J = -n \Delta p.
\\]

where the minus sign indicates that \\(J\\) and \\(\Delta p\\) have opposite directions.


### Average force {#average-force}

We find the average force acting on the target as follows:

\\[
F\_{avg} = - \frac{n}{\Delta t}m\Delta v.
\\]

If the projectiles stop upon impact, we can write substitute for \\(\Delta v\\),

\\[
\Delta v = v\_f - v\_i = -v.
\\]

if the projectiles rebound directly back with no change in speed, then \\(v\_f =
-v\\) and thus,

\\[
\Delta v = -2v.
\\]

instead.


## Conservation of linear momentum {#conservation-of-linear-momentum}

In a closed, isolated csystem,

\\[
\overrightarrow{P} = constant
\\]

or

\\[
\overrightarrow{P\_i} = \overrightarrow{P\_f}
\\].


## Momentum and KE in collisions {#momentum-and-ke-in-collisions}

If the total KE is unchanged by a collision, then the collision is "elastic"
otherwise, it is considered inelastic.


### Inelastic collisions {#inelastic-collisions}

A collision of a wet putty ball with a bat is inelastic as the putty sticks to
the bat.

\\[
\overrightarrow{p\_{1i}} + \overrightarrow{p\_{2i}} = \overrightarrow{p\_{1f}} + \overrightarrow{p\_{2f}}
\\] (conservation of linear momentum)


#### Completely inelastic collision {#completely-inelastic-collision}

In a Completely inelastic collision, the objects stick together.
Take the body with mass \\(m\_2\\) to be initially at rest and the body with mass
\\(m\_2\\) to be the projectile. After the collision, the stuck-together bodies move
with velocity V. For this situation, we can write the above equation as

\\[
m\_1v\_{1i} = (m\_1+m\_2)V
\\]

or

\\[
V = \frac{m\_1}{m\_1+m\_2}v\_{1i}.
\\]

In a closed,isolated system, the velocity \rightoverarrow{v<sub>com</sub>} cannot be
changed by a collision because with the system isolated, there is no net
external force to change it.

To find \\(v\_{com}\\), we can relate it to the total linear momentum
\\(\overrightarrow{P}\\) .

\\[
\overrightarrow{P} = M\overrightarrow{v}\_{com} = (m\_1+m\_2)\overrightarrow{v}\_{com}.
\\]

Thus,

\\[
\overrightarrow{v}\_{com} = \frac{\overrightarrow{P}}{m\_1+m\_2} =
\frac{\overrightarrow{p\_1}+\overrightarrow{p\_2}}{m\_1+m\_2}
\\]


### Elastic collisions {#elastic-collisions}

In an elastic collision, the total KE of the system does not change.


#### Stationary target {#stationary-target}

\\[
m\_1v\_{1i} = m\_1v\_{1f} + m\_2v\_{2f}
\\]
(conservation of momentum)

\\[
\frac{1}{2}m\_1v\_{1i}^2 = \frac{1}{2}m\_1v\_{1f}^2 + \frac{1}{2}m\_2v\_{1f}^2
\\]

(Total KE of system does not change)

which can be rewritten as

\\[
v\_{1f} = \frac{m\_1-m\_2}{m\_1+m\_2}v\_{1i}
\\]

\\[
v\_{2f} = \frac{2m\_1}{m\_1+m\_2}v\_{1i}
\\]

<!--list-separator-->

-  Equal masses

    If \\(m\_1 = m\_2\\), the equations reduce to:

    \\[
    v\_{1f} = 0 \text{ and } v\_{2f} = v\_{1i}
    \\]

    similar to billiard balls.

<!--list-separator-->

-  A massive target

    If \\(m\_2 \gg m\_1\\),

    \\[
    v\_{1f} \approx -v\_{1i} \text{ and } v\_{2f} \approx \left( \frac{2m\_1}{m\_2} \right) v\_{1i}
    \\].

    This tells us the projectile simply bounces back while the target moves forward
    at a low speed as the quantity in parentheses is much less than unity

<!--list-separator-->

-  A massive projectile

    If \\(m\_1 \gg m\_2\\)

    \\[
    v\_{1f} \approx v\_{1i} \text{ and } v\_{2f} \approx 2v\_{1i}.
    \\]

    The projectile just keeps on moving. The target moves at twice the speed similar
    to how there is a change of velocity of \\(2v\\) as the projectile in the previous
    scenario as it bounces back.


#### Moving targets {#moving-targets}

The equations develop into

\\[
v\_{1f} = \frac{m\_1-m\_2}{m\_1+m\_2}v\_{1i} + \frac{2m\_2}{m\_1+m\_2}v\_{2i}.
\\]

\\[
v\_{2f} = \frac{2m\_1}{m\_1+m\_2}v\_{1i} + \frac{m\_2-m\_1}{m\_1+m\_2}v\_{2i}
\\]