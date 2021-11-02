+++
title = "Fluid Dynamics"
author = ["root"]
draft = false
+++

Resources: math.nyu.edu/~childres/fluidsbook.pdf, Batchelor

Conventions:
subscript denotes differentiation
repeated indices are summed over


## Kinematics {#kinematics}


### Scale {#scale}

Random motion of liquid molecules: \\(10^{-7} - 10^{-8}\\) cm
gas Mean Free path: \\(10^{-3}\\) cm


### Stress {#stress}

Short range forces can be written as the vector

\\[
\bm{\Sigma}(\mathbf{n},\mathbf{x},t)\delta A
\\]

where \\(\Sigma\\) is the stress exerted by the fluid on the side of the surface element to which n points, on the fluid on the side which n points away from.


### Eulerian and Lagrangian descriptions {#eulerian-and-lagrangian-descriptions}

Let the independent variables of a fluid be a function of position, \\(\mathbf{x} = (x\_1,\ldots,x\_N)\\) in Euclidean sapce and time t.

We introduce the function

\\[
\mathbf{x} = \chi(\bm{a},t)
\\]

as the position of a fluid particle at a time t which was located at \\(\bm{a}\\) at time t=0.

In eulerian descriptions, we look at fixed points instead of parcels of fluid and properties are expressed as functions of \\(\mathbf{x}\\) and \\(t\\).

We can relate the two coordinates with velocity.

\\[
\mathbf{x}\_t = \pdv{\chi}{t}\Big\vert\_{\bm{a}} = \bm{u}(\mathbf{x(\bm{a},t),t})
\\]

Finding lagrangian coordinates given velocity field thus requires solving an ode.


### Streamlines {#streamlines}

Instantaneous streamlines are families of curves satisfying:

\\[
\frac{\dd{x}}{u} = \frac{\dd{y}}{v} = \frac{\dd{z}}{w}
\\]

given that \\(\bm{u}(\mathbf{x},t) = (u(x,y,z,t),v(x,y,z,t),w(x,y,z,t))\\).

Streaklines (consider labelling a particle with a dye and watching its path) can be described using the generalized Lagrangian coordinate \\(\mathbf{x} = \chi(\bm{a},t,t\_a)\\) defined to be the position at time t of a particle that was located at \\(\bm{a}\\) at time \\(t\_a\\).


### Jacobian matrix {#jacobian-matrix}

The jacobian of the Lagrangian map (\\(S\_t = M\_tS\_0\\) where S is an open set of \\(\mathbb{R}^N\\)) is defined by the matrix:

\\[
J\_{ij} = \pdv{x\_i}{a\_j}\Big\vert\_t
\\]

Thus \\(\dd{l\_i}  = J\_{ij}\dd{a\_j}\\) is a differential vector which can be visualized as connecting two nearby fluid particles whose labels differ by \\(\dd{a\_j}\\). If \\(\dd{a\_1}\ldots\dd{a\_N}\\) is the volume of a small fluid parcel, \\(\det(\bm{J})\dd{a\_1}\ldots\dd{a\_N}\\) is the volume of the parcel under the map \\(\mathcal{M}\_t\\). For incompressible liquids, Det(J) = constant = 1 when \\(\bm{a}\\) denotes initial position, independently of \\(\bm{a}\\),\\(t\\). It is usually assumed that Det(J) > 0, such that we can invert to express a as a function of x,t.


### Material Derivative {#material-derivative}

Suppose there is a certain scalar property \\(\mathcal{P}\\) of the liquid that can be attached to a fluid parcel such as temperature or density. If the property is invariant in time, we can express it as:

\\[
\pdv{\mathcal{P}}{t}\Big\vert\_{\bm{a}} = 0
\\]

i.e. time derivative is taken with label fixed. Such a scalar is material. To express it in eulerian form:

\\[
\pdv{\mathcal{P}(\mathbf{x}(\bm{a},t),t)}{t}\Big\vert\_{\bm{a}} = \mathcal{P}\_t + \bm{u}\cdot \grad\mathcal{P}
\\]

The Eulerian operator \\(\pdv{}{t} + \bm{u}\cdot\nabla\\) is the **material/substantive/convective derivative.**

The accleration of a fluid parcel is defined as teh amterial derivative of the velocity \\(\bm{u}\\). In Lagrangian variables, the accleration is \\(\pdv[2]{\mathbf{x}}{t}\vert\_{\bm{a}}\\).

\\[
\mdv{}{t}\det(\bm{J}) = \text{div}(\bm{u})\det(\bm{J})
\\]

In eulerian variables, an incompressible fluid is defined by div(u) = 0.


### Solenoidal velocity fields {#solenoidal-velocity-fields}


#### 2 dimensions {#2-dimensions}

The solenoidal condition in 2d is:

\\[
\pdv{u}{x} + \pdv{v}{y} = 0
\\]

\\[
u = \pdv{\psi}{y}, v = -\pdv{\psi}{x}
\\]

The function \\(\psi\\) is called the stream function of the velocity field. The lines of constant \\(\psi\\) are the instantaneous streamlines of \\((u,v)\\).

Given two streaklines \\(\psi\_1,\psi\_2\\), and any oriented simple contour (no self-crossings), connecting one streamline to another, the flux of liquid across the contour from left to right is given by the differnece in values of the stream function. This is because the integral of flux is:

\\[
\int (u,v) \cdot (\dd{y},-\dd{x}) = \int \dd{\psi} = \psi\_2 - \psi\_1
\\]


#### 3 dimensions {#3-dimensions}

From mass continuity, \\(\div \bm{u} = 0\\). Thus, the quantity in brackets can be represented by:

\\[
\bm{u} = \curl \bm{\Psi}
\\]

where \\(\Psi\\) is the vector potential which can be specified in terms of two scalar functions \\(\bm{\Psi} = \chi\grad\psi\\). This produces \\(\bm{u} =  \grad\chi \times \grad\psi\\). Thus 3D streamlines are te intersections of two stream surfaces.


### Convection theorem {#convection-theorem}

Suppose \\(S\_t\\) is a region of fluid particles and \\(f(\mathbf{x},t)\\) be a scalar function. Forming the volume integral over \\(S\_t\\), \\(F = \int\_{S\_t} f\dd{V\_\mathbf{x}}\\), we seek to compute \\(\dv{F}{t}\\). Using \\(\dd{V\_\mathbf{x}} = \dd{x\_1}\ldots\dd{x\_N} = \det(\bm{J})\dd{V\_\bm{a}}\\),

\begin{align\*}
\dv{F}{t} & = \int\_{S\_t} \mdv{f}{t} + f\text{div}(\bm{u}) \dd{V\_\mathbf{x}} \\\\
          & = \int\_{S\_t} \pdv{f}{t} + \text{div}(f\bm{u}) \dd{V\_\mathbf{x}} \\\\
\end{align\*}

Which is the convection theorem.
Also known as Reynold's Transport Theorem.


### Strain and rotation rates {#strain-and-rotation-rates}

Consider the relative motion between two neighbouring points.

A taylor expansion of \\(\mathbf{u}\\) about \\(\mathbf{x}\\) gives:

\\[
\dd{u\_i} = \pdv{u\_i}{x\_j}\dd{x\_j}
\\]

The derivative is called the velocity gradient tensor, and it can be decomposed into:

\\[
\pdv{u\_i}{x\_j} = S\_{ij} + \frac12 R\_{ij}
\\]

Where

\\[
S\_{ij} = \frac12 \left(\pdv{u\_i}{x\_j} + \pdv{u\_j}{x\_i}\right) = \frac12 (\grad \bm{u} + (\grad \bm{u})^T)
\\]

is the (symmetric) strain rate tensor

\\[
R\_{ij} = \pdv{u\_i}{x\_j} - \pdv{u\_j}{x\_i}
\\]
is the (antisymmetric) rotation tensor

The taylor expansion equation can thus be written:

\\[
\dd{u\_i} = \left(S\_{ij}-\frac12 \epsilon\_{ijk}\omega\_k\right)\dd{x\_j}
\\]

where \\(\epsilon\_{ijk}\omega\_k\dd{x\_j}\\) is the ith component of the cross product \\(-\bm{\omega} \times \dd{\mathbf{x}}\\).


#### Strain rate tensor {#strain-rate-tensor}

The diagonal terms of \\(S\_{ij}\\) represent elongation and contraction per unit length in various coordinate directions and are called linear strain rates. \\(S\_{11}\\) represents the rate of change of fluid element length in the $x\_1$-direction per unit length. The off diagonal terms represent shear deformations that change the relative orientations of material line segments initially parallel to the i- and j-directions of the flow. Thus, \\(S\_{ij}\\) represents the average rate at which material line segments parallel to the i- and j-directions rotate toward each other.

The average rate at which the initially perpendicular segments rotate toward each other is \\(S\_{12} = S\_{21}\\)

\\(S\\) is independent of the frame of reference in which it is observed as it is zero for rigid body motion composed of translation at a spatially uniform velocity and rotation at a constant angular velocity.

\\(S\_{ii}\\) is the _volumetric strain rate_ or _bulk strain rate_. It thus specifies the rate of volume change per unit volume and does not depend on the orientation of the coordinate system.


#### Rotation tensor {#rotation-tensor}

Diagonal elements are zero and off-diagonal elements are equal and opposite.

\\[
R\_{ij} = -\epsilon\_{ijk}\omega\_k = \mqty[ 0 & -\omega\_3 & \omega\_2 \\\ \omega\_3 & 0 & -\omega\_1 \\\ - \omega\_2 & \omega\_1 & 0]
\\]
where

\\[
\omega\_1 = \pdv{u\_3}{x\_2}-\pdv{u\_2}{u\_3}
\\]

and cyclic permutations hold.

The vector \\(\bm{\omega}\\) is the vorticity, \\(\bm{\omega} = \curl \mathbf{u}\\)

Fluid rotation is called irrotational if \\(\bm{\omega} = \bm{0}\\). In this case, the fluid velocity \\(\mathbf{u}\\) can be written as the gradient of a scalar function.

The _circulation_ \\(\Gamma\\) is the amount of fluid rotation within a closed contour.

\\[
\Gamma \equiv \oint\_C \bm{u}\cdot\dd{\bm{s}} = \int\_S \bm{\omega}\cdot\dd{\bm{A}}
\\]


## Conservation of mass and momentum {#conservation-of-mass-and-momentum}


### Conservation of mass {#conservation-of-mass}


#### Eulerian form {#eulerian-form}

\\[
\pdv{\rho}{t} + \text{div}(\bm{u}\rho) = q
\\]

\\[
\mdv{\rho}{t} + \rho\text{div}(\bm{u}) = q
\\]


#### Lagrangian form {#lagrangian-form}

When q = 0 (no mass sinks/sources),

\\[
\det\bm{J}(\bm{a},t) = \frac{\rho\_0}{\rho}
\\]
otherwise:

\\[
\pdv{}{t}\Big\vert\_{\bm{a}} \rho\det(\bm{J}) = \det(\bm{J})q(\mathbf{x}(\bm{a},t),t)
\\]

Both forms can be reconcilled with:

Assuming q=0,

\\[
\mdv{\rho}{t} + \rho\div \bm{u} = 0 = \frac{1}{\det(\bm{J})} \mdv{}{t}(\rho\det(\bm{J}))
\\]


#### Integral form {#integral-form}

For a material volume,

\\[
\dv{}{t} \int\_{V(t)} \rho(\bm{\mathbf{x}},t)\dd{V} = 0
\\]

or

\\[
\int\_{V(t)} \pdv{\rho(\bm{\mathbf{x}},t)}{t} \dd{V} + \int\_{A(t)} \rho(\bm{\mathbf{x}},t)\bm{u}(\bm{\mathbf{x}},t) \cdot \dd{\bm{A}} = 0
\\]

For an arbitrarily moving control volume,

Although the time derivative of the total mass is not the same as for a material volume, the above relation still holds and at the moment of intertia we pick \\(V(t) = V^\*(t)\\) and \\(A(t) = A^\*(t)\\). Thus:

\\[
\dv{}{t}\int\_{V^\*(t)} \rho(\bm{\mathbf{x}},t)\dd{V} + \int\_{A^\*(t)} \rho(\bm{\mathbf{x}},t)(\bm{u}(\bm{\mathbf{x}},t)-\bm{b})\cdot\dd{\bm{A}} = 0
\\]


#### Densities per unit mass {#densities-per-unit-mass}

When f is a density per unit mass, then, \\(\rho f\\) is "f per unit volume", which can be plugged into the convection theorem. When q = 0.

\\[
\dv{}{t} \int\_{S\_t} \rho f \dd{V\_{\mathbf{x}}} = \int\_{S\_t} \rho \mdv{f}{t} \dd{V\_\mathbf{x}}
\\]


### Conservation of momentum {#conservation-of-momentum}

Momentum of a fluid is defined as: \\(\rho \bm{u}\\), per unit volume.

In this case, sources and sinks of momentum are forces. If \\(F(\mathbf{x},t)\\) is the force acting on the liquid, per unit volume, then we have **Cauchy's equation of motion**:

\\[
\rho \mdv{\bm{u}}{t} = \bm{F}
\\]

in eulerian form.

The force \\(\bm{F}\\) is assumed to take the form:

\\[
F\_i = f\_i + \pdv{\sigma\_{ij}}{x\_j}
\\]
where \\(\bm{f}\\) is a body force, and \\(\sigma\\) is the stress tensor. When integrated for a material volume, it gives:

\\[
\dv{}{t} \int\_{V(t)}\rho(\mathbf{x},t)\bm{u}(\mathbf{x},t)\dd{V} = \int\_\mathcal{R} \bm{F} \dd{V\_{\mathbf{x}}} = \int\_{\mathcal{R}} \rho\bm{g} \dd{V\_{\mathbf{x}}} + \int\_{\partial{\mathcal{R}}} \sigma\cdot \bm{n}\dd{S\_{\mathbf{x}}}
\\]

Using convection theorem, this can be expanded into:

\\[
\int\_{V(t)} \pdv{}{t}(\rho\bm{u}) \dd{V} + \int\_{A(t)} \rho\bm{u}(\bm{u}\cdot\dd{\bm{A}}) = \int\_{V(t)} \rho\bm{g}\dd{V} + \int\_{A(t)}\bm{\sigma}(\bm{n},\bm{x},t) \dd{A}
\\]

For control volumes:

\\[
\int\_{V(t)} \pdv{}{t}(\rho\bm{u}) \dd{V} + \int\_{A(t)} \rho\bm{u}(\bm{u} - \bm{b})\cdot\dd{\bm{A}}) = \int\_{V(t)} \rho\bm{g}\dd{V} + \int\_{A(t)}\bm{\sigma}(\bm{n},\bm{x},t) \dd{A}
\\]


### Constitutive equation for a newtonian fluid {#constitutive-equation-for-a-newtonian-fluid}

An ideal fluid (or a fluid at rest) is defined by a stress tensor of the form:

\\[
T\_{ij} = -p\delta\_{ij} = \mqty(\dmat{-p,-p,-p})
\\]

Thus when pressure is positive, the force is opposite the outer normal. Note:

\\[
\div \sigma = -\grad p
\\]

When a fluid is moving, there is aditional stress components due to viscosity.

\\[
T\_{ij} = -p\delta\_{ij} + \tau\_{ij}
\\]

This decomposition of stress into fluid static and fluid dynamics contributions is approximate as \\(p\\) is only well defined for equilibrium conditions, but most of the time fluid particles reach local thermodynamic equilibrium in most fluid flows.
Here, tau is the **deviatoric stress tensor**. Since it is invariant under galilean transformations, it can only depend on the velocity gradient tensor. Since stresses only develop in fluid elements that change shape, only the symmetric part matters, as the other part corresponds to pure rotation. The most general relation that produces \\(\tau\_{ij} = 0\\) when \\(S\_{ij} = 0\\) is: \\(\tau\_{ij} = K\_{ijmn} S\_{mn}\\). Since the relationship is independent of the orientation of the coordinate system, \\(K\_{ijmn}\\) must be an isotropic tensor. All fourth order isotropic tensors must be of the form:

\\[
K\_{ijmn} = \lambda \delta\_{ij}\delta\_{mn} + \mu\delta\_{im}\delta\_{jn} + \gamma\delta\_{in}\delta\_{jm}
\\]

Since tau is symmetric in i and j, K must also be symmetric in i and j.
Thus:

\\[
\tau = 2\mu S\_{ij} + \lambda S\_{mm}\delta\_{ij}
\\]

where recall that \\(S\_{mm} = \div \bm{u}\\) is the volumetric strain rate.

Thus:

\\[
T\_{ij} = -p\delta\_{ij} + 2\mu S\_{ij} + \lambda S\_{mm}\delta\_{ij}
\\]

For compressible flow, On contraction:

\\[
T\_{ii} = -3p + (2\mu + 3\lambda)S\_{mm}
\\]

from which pressure is found to be:

\\[
p = -\frac{1}{3}T\_{ii} + (\frac{2}{3}\mu + \lambda)\div \bm{u}
\\]

Defining mean pressure as \\(\bar{p} = - \frac{1}{3} T\_{ii}\\),

\\[
p - \bar{p} = \left(\frac{2}{3}\mu + \lambda \right)\div\bm{u}
\\]

The quantity in brackets is the **coefficient of bulk viscosity**, \\(\mu\_v\\). But the stokes assumption \\(\mu\_v = 0\\) is found to be accurate in many situation as itself or the flow's dilatation rate is small.

But for incompressible fluids,

\\[
T\_{ij} = -p\delta\_{ij} + 2\mu S\_{ij}
\\]

The linear relation between \\(\bm{T}\\) and \\(\bm{S}\\) is consistent with Newton's defintion of the viscosity coeffient in a simple parallel flow.


### Navier stokes momentum equation {#navier-stokes-momentum-equation}

Combining the stress tensor with Cauchy's equation gives:

\\[
\rho\left(\pdv{u\_j}{t} + u\_i\pdv{u\_i}{x\_i}\right) = -\pdv{p}{x\_i} + \rho g\_j + \pdv{}{x\_i}\left[\mu\left(\pdv{u\_j}{x\_j} + \pdv{u\_i}{x\_j}\right) + \left(\mu\_v - \frac{2}{3}\mu\right)\pdv{u\_m}{x\_m}\delta\_{ij} \right]
\\]

When temperature differences are small, the viscosities can be taken outside the spatial derivative.

\\[
\rho\mdv{u\_j}{t} = -\pdv{p}{x\_i} + \rho g\_j + \mu\pdv[2]{u\_j}{x\_i} + \left(\mu\_v + \frac{1}{3}\mu\right)\pdv{}{x\_j}\pdv{u\_m}{x\_m}
\\]

For incompressible flow,

\\[
\rho\mdv{\bm{u}}{t} = -\grad p + \rho \bm{g} + \mu\laplacian \bm{u}
\\]

The last term can be obtained from the curl of the vorticity, \\(\mu\laplacian\bm{u} = - \mu\curl\bm{\omega}\\).

When viscous effects are negligible for exterior flows away from solid boundaries, you get Euler's equation:

\\[
\rho \mdv{\bm{u}}{t} = - \grad p + \rho\bm{g}
\\]

An ideal fluid with no mass addition satisfies:

\\[
\rho\mdv{\bm{u}}{t} + \grad p = 0
\\]

and:

\\[
\mdv{\rho}{t} + \rho\div \bm{u} = 0
\\]

These are referred to as Euler's equations, which gives N+1 equations for the N+2 unknowns, \\(u\_1,\ldots,u\_N,\rho,p\\). The additional equation can be the incompressible assumption \\(\div \bm{u} = 0\\), or to assume constant density, or use conservation of energy.

In Lagrangian form,

\\[
\grad\_{\mathbf{x}} p = \bm{J}^{-1} \grad\_{\bm{a}} p
\\]


### Non-intertial frames {#non-intertial-frames}

While the continuity equation is unchanged, the momentum equation must be modified.