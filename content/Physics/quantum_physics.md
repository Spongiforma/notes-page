+++
title = "Quantum mechanics"
author = ["root"]
draft = false
+++

this is in gaussian units


## Postulates {#postulates}

1.  Associated to any isolated physical system is a hilbert space which is completely described by its state vector.
2.  The evolution of a closed quantum system is described by a unitary transformation. i.e. the shrodinger equation


## Hamiltonian formalism {#hamiltonian-formalism}


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

q\_k is thus a cyclic coordinate.


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

each K\_i(q) may be a function of all the q\_i and need not be constant.

The quantity:

\\[
P(q,\dot{q}) = \sum\_i \pdv{L}{\dot q\_i}K\_i(q)
\\]

does not change with time and has the generic name of consered momentum.

Example:

For \\(L = (m/2)(5\dot{x}^2 - 2\dot{x}\dot{y} + 2\dot{y}^2) + C(2x-y)\\), K\_x = 1 and K\_y = 2:

\\[
P = \pdv{L}{\dot{x}}K\_x + \pdv{L}{\dot y}K\_y = m(3\dot{x} + 3\dot{y})
\\]


### Hamiltonian {#hamiltonian}

We may write E as:

\\[
E(q,\dot{q}) \equiv \pdv{L(q,\dot{q})}{\dot{q}}\dot{q} - L(q,\dot{q})
\\]

and we wish to exchange all  \\(\dot{q}\\) for \\(p\\) in E.

\\[
p \equiv \pdv{L}{\dot{q}}
\\]

When written in this way, we define it as the Hamiltonian.

\\[
H(q,p) \equiv p\_i\dot{q\_i}(q,p) - L(q,\dot{q}(q,p))
\\]


#### Hamiltonian equations {#hamiltonian-equations}

\\[
\pdv{H}{p} = \dot{q}
\\]

\\[
\pdv{H}{q} = -\dot{p}
\\]


#### Cyclic coordinates {#cyclic-coordinates}

Same as Lagrange.
if q is cyclic, p is conserved.

Let w(p,q) be some function of the state variables with no explicit dependence on t.

\\[
\dot{\omega} = \\{\omega,\mathcal{H}\\}
\\]

where the Poisson brackets (PB) between two variables is:

\\[
\left\\{\omega,\lambda\right\\} = \sum\_i \left(\pdv{\omega}{q\_i}\pdv{\lambda}{p\_i} - \pdv{\omega}{p\_i}\pdv{\lambda}{q\_i}\right)
\\]

<!--list-separator-->

-  Poisson bracket Identities

    Any variable whose PB with \\(\mathcal{H}\\) vanishes is constant in time.

    {a,b} = -{b,a}
    {a,b+c} = {a,b} + {a,c}
    {a,bc} = {a,b}c + b{a,c}

    (similar to commutators)

    \\[
    $\\{q\_i,q\_j\\} = \\{p\_i,p\_j\\} = 0
    \\]

    \\[
    \\{q\_i,p\_j\\}=\delta\_{ij}
    \\]

    as \\(\partial{q\_i}/\partial{q\_j} = \delta\_{ij}, \partial{q\_i}/\partial{p\_k}=0\\)

    Hamiltonian equations may be written as:

    \begin{align\*}
    \dot{q\_i} = \\{q\_i,\mathcal{H}\\} \\\\
    \dot{p\_i} = \\{p\_i,\mathcal{H}\\}
    \end{align\*}


#### Legendre transform {#legendre-transform}

Say that we wish to 'invert':

\\[
\dv{F(x)}{x} = s(x)
\\]

by constructing a function G(s) which is the Legendre transform of F(x):

\\[
\dv{G(s)}{s} = x(s).
\\]

By noting \\(d(F+G) = s \dd{x} + x \dd{s} = d(sx)\\), we may write:

\\[
G = sx-F = F'x - F
\\].

Or

\\[
G(s) = sx(s) - F(x(s))
\\]


## Statevectors {#statevectors}

Statevector expressed in certain basis.

\\[
\ket{\psi} = \ket{ + z}\braket{+ z}{\psi} + \ket{-z}\braket{-z}{\psi} = c\_+\ket{+ z} + c\_- \ket{-z}
\\]

Expectation value: \\(\langle\Omega\rangle\\)
Square of uncertainty: \\((\Delta \Omega)^2 = \langle\Omega^2\rangle - \langle\Omega\rangle^2\\)

Two states that differ by an overall phase are the same state.


### Rotation Operators {#rotation-operators}

Rotate anticlockwise about z-axis can be defined as:

\\[
\hat{R}(\dd{\phi} \bm{k}) = 1 - \frac{i}{\hbar}\hat{J\_z}\dd{\phi}
\\]
where \\(\hat{J\_z}\\) is a hermitian operator and has |+- z> as an eigenvector with +-hbar/2 as eigenvalues.

\\[
\hat{R}(\phi \bm{k}) = \lim\_{N\to\infty}\left[1-\frac{i}{\hbar}\hat{J}\_z\left(\frac{\phi}{N}\right)\right]^N
= \exp(-i\hat{J}\_z\phi/\hbar)
\\]

\\[
\hat{R}(\phi \bm{k})\ket{\pm z} = e^{\mp i \phi/2} \ket{\pm z}
\\]

Notice that rotating by 360deg causes the state to pick up an overall minus sign.


### Matrix representation {#matrix-representation}

The matrix representation of \\(\hat{A}\\) in basis x is \\(A\_{ij} = \bra{i}\hat{A}\ket{j}\\) where i j are the bases of x.


### Passive and active transform {#passive-and-active-transform}

passive: rotating the axes
active: rotating the vector expressed in the same axes.


## Stern-Gerlach {#stern-gerlach}

The intrinsic spin angular momentum of a particle, we write

\\[
\bm{\mu} = \frac{gq}{2mc}\bm{S}
\\]

The force by the magnet equals:

\\[
F\_z = \mu\_B \pdv{B}{z}
\\]

where u\_b is the bohr magneton


## Angular momentum {#angular-momentum}

In general:

\\[
\hat{R}(\phi \bm{n}) = e^{-i \bm{\hat{J}\cdot n} \phi / \hbar}
\\]

We can represent 2d rotation in the cartesian plane like this:

\begin{bmatrix}
\bra{x}\hat{R}(\phi \bm{k})\ket{x} & \bra{x}\hat{R}(\phi \bm{k})\ket{y} \\\\
\bra{y}\hat{R}(\phi \bm{k})\ket{x} & \bra{y}\hat{R}(\phi \bm{k})\ket{y} \\\\
\end{bmatrix}

which just gives:

\begin{bmatrix}
\cos\phi & -\sin\phi \\\\
\sin\phi & \cos\phi \\\\
\end{bmatrix}

Note that rotations and generators don't commute as:

\\[
[\hat{J}\_x,\hat{J}\_y] = i\hbar \hat{J}\_z
\\]

which holds for cyclic permutations


### Commuting operators {#commuting-operators}

Consider two linear Hermitian operators \\(\Omega, \Lambda\\) which commute.

Suppose only a single state \\(\ket{\omega}\\) that is an eigenstate of \\(\Omega\\) with eigenvalue \\(\omega\\).

Then from the commutativity relation: \\(\Lambda\ket{\omega}\\) is also an eigenstate of operator \\(\Omega\\).
Since we presumed there is only one such state, this shows that \\(\Lambda\ket{\omega} = \lambda\ket{\omega}\\).

We can then label the eigenvector as \\(\ket{\omega,\lambda}\\).


#### Degeneracy {#degeneracy}

If there is more than one eigenstate of the operator \\(\Omega\\) with eigenvalue \\(\omega\\), we say there is degeneracy.


### Eigenvalues and eigenstates of angular momentum {#eigenvalues-and-eigenstates-of-angular-momentum}

Although the generators of rotations about different axes do not commute, the following operator commutes with each of the gneerators.

\\[
\bm{\hat{J}}^2 = \hat{J}\_x^2 + \hat{J}\_y^2 + \hat{J}\_z^2
\\]

Since it commutes with each generator, these operators have simulataneous eigenstates in common.

\\[
\bm{\hat{J}}^2\ket{\lambda,m} = \lambda \hbar^2 \ket{\lambda,m}
\\]

\\[
\hat{J}\_z\ket{\lambda,m} = m \hbar \ket{\lambda,m}
\\]