+++
title = "Electrodynamics"
author = ["root"]
draft = false
+++

## Electrostatics {#electrostatics}


### Relations {#relations}

V -&gt; rho

\\[
\laplacian V = -\frac{\rho}{\epsilon\_0}
\\]
rho -&gt; V

\\[
V = \frac{1}{4\pi\epsilon\_0}\int\frac{\rho}{r}\dd{\tau}
\\]

E -&gt; rho

\\[
\div{E} = \frac{\rho}{\epsilon\_0}
\\]

rho -&gt; E

\\[
E = \frac{1}{4\pi\epsilon\_0}\int\frac{\rho{\bf \hat{r}}}{r^2}\dd{\tau}
\\]

V -&gt; E

\\[
E = -\grad{V}
\\]

E -&gt; V
\\[
V = -\int{E \cdot \dd{l}}
\\]


### Potential energy {#potential-energy}

For a configuration,

\begin{align\*}
W & = \frac{1}{8\pi\epsilon\_0}\sum\_{i=1}^n\sum\_{j\neq i}^n \frac{q\_iq\_j}{r\_{ij}} \\\\
& = \frac12 \sum\_{i=1}^n q\_i V(\bf r\_i) \\\\
\end{align\*}

For a continuous charge distribution,

\begin{align\*}
W & = \frac12 \int \rho V \dd{\tau} \\\\
& = \frac{\epsilon\_0}{2}\left(\int\_V E^2 \dd{\tau} + \oint\_S VE\cdot\dd{\bf a}\right) \\\\
& = \frac{\epsilon\_0}{2}\int E^2 \dd{\tau} \text{(all space)}
\end{align\*}

For compount systems:

\\[
W = W\_1 + W\_2 + \epsilon\_0 \int{E\_1 \cdot E\_2}\dd{\tau}
\\]


### Capacitors {#capacitors}


#### Breakdown voltage {#breakdown-voltage}

Series:

\\[
V\_{max} = \sum\_j \frac{1}{C\_j} \min\_i C\_iV\_{bi}
\\]

Parallel:

\\[
V\_{max} = \min\_i(V\_{bi})
\\]


## Potentials {#potentials}

Laplace's equations tolerates no local maxima and minima and at a point it can often be expressed as the average of the surrounding potential.

The potential at the center of a sphere is equal to the average potential at the surface due to an external charge located a distance from the center of the sphere. v_ave = V_center + kQ_enc/R


### Boundary conditions and uniqueness theorems {#boundary-conditions-and-uniqueness-theorems}


#### First uniqueness theorem {#first-uniqueness-theorem}

The solution to Laplace's equation in some volume is uniquely determined if potential is specified on the boundary surface S and the charge density throughout the region is specified.


#### 2nd uniqueness theorem {#2nd-uniqueness-theorem}

In a volume surrounded by conductors and containing a specifed charge density, the electric field is uniquely determined if the total charge on each conductor is given.


### Method of images {#method-of-images}

Suppose a point charge q is held a distance d above an infinite grounded conducting plane. What is the potential (which is affected by the accumulation of charge on the plane).

Solution: Pretend there is a charge at -z. Many quantities end up being the same though energy isn't. Note you cannot put image charges where yuo are calculating V as it would change charge density.


#### Circle of apollonius {#circle-of-apollonius}

{{< figure src="pics/apollocircle.png" >}}


### Seperation of variables {#seperation-of-variables}

Set boundary conditions and you will get hyperbolic (suited for boundary conditions at infinity) and trig functions. then find fourier coeffs


#### Spherical coordinates {#spherical-coordinates}

\\[
V(r,\theta) = \sum^\infty\_{l=0}\left(A\_lr^l + \frac{B\_l}{r^{l+1}}\right) P\_l(\cos\theta)
\\]

where P are the legendre polynomials:

\\[
P\_l(x) = \frac{1}{2^l l!} \left(\dv{x}\right)^l (x^2 - 1)^l
\\]

~~---~~-------------------------+

| l | Polynomial              |
|---|-------------------------|
| 0 | 1                       |
| 1 | x                       |
| 2 | (3x^2 - 1)/2            |
| 3 | (5x^3-3x)/2             |
| 4 | (35x^4-30x^2+3)/8       |
| 5 | (63x^5 - 70x^3 + 15x)/8 |


### Multipole expansion {#multipole-expansion}

\\[
V(\bm{r}) = \frac{1}{4\pi\epsilon\_0}\sum\_{n=0}^\infty \frac{1}{r^{n+1}}\int(r')^n P\_n(\cos\alpha)\rho(\bm{r}')\dd{\tau'}
\\]

where \\(\alpha\\) is the angle between r and r'

The first non-zero dipole is independent of translation of coordinates.


#### Dipole {#dipole}

Dipole moment:

\\[
\bm{p} \equiv \int \bm{r}' \rho(\bm{r}') \dd{\tau}
\\]

or \\(\sum\_i q\_i\bm{r}'\_i\\). or \\(\bm{p} - Q\bm{a}\\) for a shift in coordiantes.

\\[
V\_{dip}( r) = \frac{1}{4\pi\epsilon\_0}\frac{\bm{p}\cdot\hat{\bm{r}}}{r^2}
\\]

for a pure dipole (as opposed to a physical one), qd = constant but d -&gt; 0.


## Electric fields in matter {#electric-fields-in-matter}


### Induced dipole {#induced-dipole}

An atom which is placed in an electric field gets polarised and forms a dipole. the dipole moment is given by.

\\[
\bm{p} = \alpha \bm{E}
\\]


### Alignment of polar molecules {#alignment-of-polar-molecules}

A dipole in a uniform field \\(E\\) experiences a torque

\\[
\bm{N} = \bm{p} \times \bm{E}
\\]

If the field is nonuniform, such that the force on the positive part does not balance the force on the negative part, then

\\[
\bm{F} = (\bm{p} \cdot \nabla)\bm{E}
\\]

\\[
U = - \bm{p} \cdot \bm{E}
\\]


### Polarisation {#polarisation}

When an object gets polarised, we get a bunch of little dipoles pointing in the direction of the field, so we can call this:

\\[
\bm{P} \equiv \text{dipole moment per unit volume}
\\]

which is the polarisation.


### Field of polarised object {#field-of-polarised-object}

Since the total potential of polarised object is:

\\[
V(\bm{r}) = \frac{1}{4\pi\epsilon\_0} \int\_\mathcal{V} \frac{\bm{P}(\bm{r'})\cdot \bm{\hat\gamma} }{\gamma^2} \dd{\tau'}
\\]

This can be shown to be equivalent to defining:

\\[
\sigma\_b \equiv \bm{P} \cdot \bm{\hat{n}}
\\]

\\[
\rho\_b \equiv - \div P
\\]

and expressing above as:

\\[
V(\bm{r}) = \frac{1}{4\pi\epsilon\_0} \oint\_\mathcal{S} \frac{\sigma\_b}{\gamma} \dd{a'} + \frac{1}{4\pi\epsilon\_0} \int\_\mathcal{V} \frac{\rho}{\gamma} \dd{\tau'}
\\]


### Electric Displacement {#electric-displacement}

Since we have found that the effect of polarization is to produce accumulations of bound charge within the dielectric and on the surface, we will now put it all together with the field attributable to bound charge plus the field due to everything else, which we will call **free charge.**

Gauss' law reads:

\\[
\epsilon\_0 \div \bm{E} = \rho\_b + \rho\_f = -\div \bm{P} + \rho\_f
\\]

It is convenient to combine the two divergence terms:

\\[
\div (\epsilon\_0 \bm{E} + \bm{P}) = \rho\_f
\\]

and call the expression in parentheses \\(\bm D\\), the **electric displacement**. Thus:

\\[
\div \bm{D} = \rho\_f
\\]

\\[
\oint \bm{D} \cdot \dd{\bm{a}} = Q\_{f\_{enc}}
\\]

One must be careful not to draw a direct parallel between E and D such as trying to prescribe a coulomb's law for D.

By helmholtz' theorem, the divergence alone is insufficient to determine a vector field, as one would need to know the curl as well. However, the curl of D is not always zero as while curl E is zero, curl P isn't always.
Thus, D is not determined exculsively by the free charge.


### Boundary conditions {#boundary-conditions}


#### Perpendicular component {#perpendicular-component}

D above - D below = \\(\sigma\_f\\)


#### Parallel component {#parallel-component}

D above - D below = P above - P below


### Linear dielectrics {#linear-dielectrics}

If the E field is not too strong, the polarisation is proportional to the field. They will be called **Linear dielectrics**.

\\[
\bm{P} = \epsilon\_0 \chi\_e \bm{E}
\\]

where \\(\chi\_e\\) (dimensionless) is called the electric susceptibility of the medium.
Note: E is the total field, so in order to calculate P, E must be found, and in order to find contribution from P (by finding P), one must find E. Thus, gauss' law in dielectrics should be used first to find D.

From definition of electric displacement, we have:

\\[
\bm{D} = \epsilon\_0(1 + \chi\_e)\bm{E} = \epsilon \bm{E}
\\]

where \\(\epsilon\\) is the permittivity of the material. The relative permittivity, or dielectric constant is given by \\(\epsilon\_r\\) or \\(\kappa\\).

It is also possible to derive an expression for bound charge from \\(D\\).

\\[
\rho\_b = -\div P = - \frac{\chi\_e}{1 + \chi\_e} \rho\_f
\\]


#### Energy {#energy}

\\[
W = \frac{\epsilon\_0}{2} \int \epsilon\_r E^2\dd{\tau} = \frac12 \int \bm{D}\cdot\bm{E} \dd{\tau}
\\]


## Magnetostatics {#magnetostatics}

Lorentz' force law

\\[
\bm{F} = q(\bm{E} + \bm{v} \times \bm{B})
\\]

\\[
\bm{F} = I \int (\dd{\bm l}\times \bm{B})
\\]


### Current {#current}

Current can also be written as a vector:

\\[
\bm{I} = \lambda \bm{v}
\\].

Surface Charge density is defined as:

\\[
\bm{K} = \dv{\bm I}{l}
\\]

Volume current density is defined as:

\\[
\bm{J} = \dv{\bm I}{a}
\\]

Continuity equation:

\\[
\div \bm{J} = - \pdv{\rho}{t}
\\]


### Steady Currents {#steady-currents}

Steady currents produce constant magnetic fields. Thus:

\\[
\pdv{\rho}{t} = 0
\\]

\\[
\pdv{\bm{J}}{t} = \bm{0}
\\]


#### Biot-Savart law {#biot-savart-law}

\\[
\bm{B}(\bm{r}) = \frac{\mu\_0}{4 \pi} \int \frac{\bm{I} \times \bm{\hat\gamma}}{\gamma^2} \dd{l'}
\\]

<!--list-separator-->

-  Magnetic field around wire

    \\[
    \bm{B} = \frac{\mu\_0 I}{2\pi s} \bm{\hat\phi}
    \\]

<!--list-separator-->

-  force per unit length of two parallel wires

    \\[
    f = \frac{\mu\_0}{2\pi} \frac{I\_1I\_2}{d}
    \\]

<!--list-separator-->

-  Magnetic field above a circular loop

    \\[
    B(z) = \frac{\mu\_0 I}{2} \frac{R^2}{(R^2 + z^2)^{3/2}}
    \\]


#### Curl and div of B {#curl-and-div-of-b}

\\[
\oint \bm{B} \cdot \dd{\bm{l}} = \mu\_0 I\_{enc}
\\]

\\[
\curl \bm{B} = \mu\_0 \bm{J}
\\]

\\[
\div \bm{B} = 0
\\]


### Vector potential {#vector-potential}

\\[
\bm{B} = \curl \bm{A}
\\]

We can limit forms of the vector potential by making it divergenceless.

Thus, ampere's law becomes

\\[
\laplacian \bm{A} =-\mu\_0 \bm{J}
\\]

which is Poisson's equations in three coordinates.

The solution is:

\\[
\bm{A}(\bm{r}) = \int \frac{\bm{J}(\bm{r}')}{\mathpcz{|\bm{r - r'}|}} \dd{\tau'}
\\]


## Electrodynamics {#electrodynamics}

Ohm's law

\\[
\bm{J} = \sigma \bm{f}
\\]

where \\(\bm{f}\\) is the force per unit charge. since this is equal to the lorentz force, and the velocity of the charge is usually small,

\\[
\bm{J} = \sigma \bm{E}
\\]

Faraday's law

\\[
\curl \bm{E} = - \pdv{B}{t}
\\]

Parallels between faraday's law and ampere's law can be used to solve problems with analogy, in finding electric fields induced by changing magnetic fields.

For instance, biot-savart law for electric fields:

\\[
\bm{E} = -\frac{1}{4\pi} \pdv{}{t} \int \frac{\bm{B} \times \hat{w}}{w^2} \dd{\tau'}
\\]


### Inductance {#inductance}

Since flux is proportional to current, we can call this proportionality constant **inductance.**


#### Neumann's formula for mutual inductance {#neumann-s-formula-for-mutual-inductance}

\\[
M = \frac{\mu\_0}{4\pi}\oint \oint \frac{\dd{\bm{I\_1}}\cdot \bm{I\_2}}{|\bm{r - r'}|}
\\]


### Energy in magnetic fields {#energy-in-magnetic-fields}

\\[
W = \frac12 L I^2 = \frac12 \int\_V (\bm{A} \cdot \bm{J})\dd{\tau} = \frac{1}{2\mu\_0}\int B^2 \dd{\tau}
\\]

The second term is sometimes a better way to find self-inductance.


### Maxwell's equations {#maxwell-s-equations}

A changing electric field also produces a changing magnetic field.

\\[
\curl \bm{B} = \mu\_0 \bm{J} + \mu\_0 \epsilon\_0 \pdv{\bm{E}}{t}
\\]

\\(\epsilon\_0 \pdv{\bm{E}}{t}\\) is often called **displacement current**.


## Conservation laws {#conservation-laws}

Recall

\\[
\pdv{\rho}{t} = - \div \bm{J}
\\]

\\[
u = \frac12 (\epsilon\_0 E^2 + \frac{1}{\mu\_0} B^2)
\\]


### Poynting's theorem {#poynting-s-theorem}

Based on lorentz' force, the work done on a charge \\(q\\) is:

\\[
\bm{F\cdot }\dd{\bm{l}} = q\bm{E} \cdot \bm{v}\dd{t}
\\]

The rate at which work is done on all charges in a volume by the electromagnetic forces is thus:

\\[
\dv{W}{t} = \int\_V \bm{E}\cdot \bm{J} \dd{\tau}
\\]

Using Maxwell's equations, this can be written in terms of just the fields as such:

\\[
\dv{W}{t} = - \dv{}{t} \int\_V u \dd{\tau} - \oint\_S \bm{S} \cdot \dd{\bm{a}}
\\]

where \\(\bm{S}\\) is the poynting vector (energy per unit time, per unit area or energy flux density ) given by

\\[
\bm{S} \equiv \frac{1}{\mu\_0} \bm{E}\times\bm{B}
\\]

When no work is done on the charges, we get the 'continuity equation' for energy

\\[
\pdv{u}{t} = - \div \bm{S}
\\]


### Maxwell's stress tensor {#maxwell-s-stress-tensor}

The net force per unit volume is

\\[
\bm{f} = \rho (\bm{E} + \bm{v}\times\bm{B})
\\]

Expressing it in terms of the fields using maxwell's equations,

\begin{align\*}
\bm{f} =  & \epsilon\_0[(\div \bm{E})\bm{E} + (\bm{E} \cdot \grad)E] \\\\
  & + \frac{1}{\mu\_0}[(\div \bm{B})\bm{B} + (\bm{B} \cdot \grad)B] \\\\
  & - \grad u - \epsilon\_0\mu\_0\pdv{S}{t}
\end{align\*}

We may condense the first three terms by introducing maxwell's stress tensor

\\[
T\_{ij} = \epsilon\_0(E\_i E\_j - \frac12 \delta\_{ij} E^2) + \frac{1}{\mu\_0} (B\_i B\_j - \frac12 \delta\_{ij} B^2)
\\]

Thus,

\\[
\bm{f} = \div T - \epsilon\_0\mu\_0 \pdv{\bm{S}}{t}
\\]

\\[
\bm{F} = \dv{\bm{p}}{t} = - \epsilon\_0\mu\_0 \pdv{}{t}\int\_V \bm{S} \dd{\tau} + \oint\_S T \cdot \dd{\bm{a}}
\\]

The momentum stored in the fields is thus

\\[
\bm{p} = \frac{1}{c^2} \int\_V \bm{S} \dd{\tau}
\\]

while the second term is the momentum per unit time flowing in through the surface.

When mechanical momentum is not changing,

\\[
\pdv{\bm{g}}{t} = \div T
\\]