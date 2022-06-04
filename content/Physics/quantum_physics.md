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

    In general,

    \\[
    [X,P] = i\hbar\\{x,p\\}
    \\]


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


### Operators {#operators}


#### Differential operator {#differential-operator}

\\[
D\ket{f} = \ket{\dv{f}{x}}
\\]

implies

In the |x&gt; basis,
\\[
\bra{x}D\ket{x'} = D\_{x,x'}=\delta'(x-x')=\delta(x-x')\dv{x'}
\\]

where it is integrated over the second index (x') and pulls out the derivative of f at the first index (x).

We can turn it hermitian by turning it into the form:

\\[
K = -iD
\\]

but in infinite dimensions, K^t = K is not sufficient to be hermitian. It is only hermitian in the space of functions that obey:

\\[
-ig^\*(x)f(x) | \given\_a^b = 0
\\]

so that &lt;g|K|f&gt; = &lt;f|K|g&gt;\*.

<!--list-separator-->

-  eigeneverything

    X-basis

    \\[
    K\ket{k} = k\ket{k}
    \\]

    \\[
    -i\dv{x}\psi\_k(x) = k\psi\_k(x)
    \\]

    where \\(\psi\_k(x) = \braket{x}{k}\\).

    the solution is:

    \\[
    \psi\_k(x) = Ae^{ikx}
    \\]

    where we choose \\(A = (1/2\pi)^{-1/2}\\)

    and &lt;k|k&gt;


#### X basis {#x-basis}

X|x&gt; = x|x&gt;

\\[
\bra{x'}X\ket{x} = x\delta(x'-x)
\\]

Action on functions:

X|f&gt; = |F&gt;

F(x) = xf(x)

\\[
\bra{k}X\ket{k'} = i\delta'(k-k')
\\]

[X,K] = iI


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
where \\(\hat{J\_z}\\) is a hermitian operator and has |+- z&gt; as an eigenvector with +-hbar/2 as eigenvalues.

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


## 1D problems {#1d-problems}

\\[
i \hbar\ket{\dot{\psi}} = H\ket{\psi}
\\]

Steps for problem:

1.  Find the classical hamiltonian. Then find the quantum hamiltonian operator analogue.
2.  Expand the H in terms of its eigenbasis to solve the time-independent problem, \\(H\ket{E} = E\ket{E}\\) by solving the differential equation in some basis.
3.  To find the state as it evolves over time, we expand \\(\ket{\psi(t)}\\) in terms of E. and find that the propogator is given by \\(\sum\_E \ketbra{E}{E}e^{-i E t / \hbar}\\). The propogator is also given by \\(U(t) = e^{-i H t/\hbar}\\), which can be expanded.


### Ehrenfest's theorem {#ehrenfest-s-theorem}

\\[
\dv{}{t} \langle \Omega \rangle = \frac{1}{i\hbar}\langle [\Omega,H]\rangle
\\]


### Particle in a box {#particle-in-a-box}

n odd,positive:

\\[
\psi\_n(x) = \sqrt{\frac{2}{L}} \cos(\frac{n\pi x}{L})
\\]

n even,positive:

\\[
\psi\_n(x) = \sqrt{\frac{2}{L}} \sin(\frac{n\pi x}{L})
\\]

\\[
E\_n = \frac{\hbar^2 k\_n^2}{2m} = \frac{\hbar^2 \pi^2 n^2}{2mL^2}
\\]


### Probability continuity {#probability-continuity}

\\[
\pdv{(\psi^\* \psi)}{t} = -\div \frac{\hbar}{2mi}(\psi^\* \grad\psi - \psi\grad\psi^\*)
\\]


### Theorems {#theorems}

1.  There is no degeneracy in 1D bound states. \\(\psi(x\to\infty) \to 0\\)
2.  The eigenfunctions of H can always be chosen pure real in the coordinate basis.


### Harmonic oscillator {#harmonic-oscillator}

\\[
H = \frac{P^2}{2m} + \frac12 m\omega^2 X^2
\\]

Step 1. Introduce dimensionless variables natural to the problem.
Step 2. Extract the asymptotic behavior of \\(\psi\\).
Step 3. Write iv as a product of the asymptotic form and an unknown function \\(u\\).
The function \\(u\\) will usually be easier to find than \\(\psi\\).
Step 4. Try a power series to see if it will yield a recursion relation.

Solving the time independent shrodinger's equation using series solutions with hermite polynomials, we get:

\\[
E\_n = (n+\frac12)\hbar \omega
\\]

\\[
\psi\_n = \left(\frac{m\omega}{\pi\hbar 2^{2n} (n!)^2}\right)^{1/4} \exp(-\frac{m\omega x^2}{2\hbar})H\_n\left[\left(\frac{m\omega}{\hbar}\right)^{1/2} x\right]
\\]

\\[
U(x,t;x',t') = \sqrt{\frac{m\omega}{2\pi i \hbar\sin\omega T}\right} \exp\left[\frac{im\omega}{\hbar} \frac{(x^2 + x'^2)\cos\omega T -2xx'}{2\sin\omega T}\right]
\\]

where \\(T = t-t'\\)

The energies can also be found using heisenberg's uncertainty principle, gaussian packets which saturate the relation, and trying to find the minimize energy for the minimal state.


#### Method of factorization {#method-of-factorization}

Introducing the operator,

\\[
a = \sqrt{\frac{m\omega}{2\hbar}}X + i \sqrt{\frac{1}{2m\omega\hbar}}P
\\]

and its adjoint which satisfy \\([a,a^\dagger] = 1\\),

(notice \\(m\omega \leftrightarrow \frac{1}{m\omega}\\) as \\(X \leftrightarrow P\\))

Since \\(a^\dagger a = \frac{H}{\hbar \omega} - \frac12\\), define an operator \\(\hat{H}\\):

\\[
\hat{H} = \frac{H}{\hbar\omega} = (a^\dagger a+1/2)
\\]

which has the properties,

\\[
[a,\hat{H}] = a
\\]
\\[
[a^\dagger,\bar{H}] = -a^\dagger.
\\]

We wish to solve the eigenvalue equation for \\(\hat{H}\\), \\(\hat{H}\ket{\epsilon} = \epsilon\ket{\epsilon}\\).

It can then be shown that \\(a\ket{\epsilon}\\) is an eigenstate with eigenvalue \\(\epsilon -1\\) and so is \\(a^\dagger \ket{\epsilon}\\) with eigenvalue \\(\epsilon +1\\).

There is a lower bound to the energy, \\(\epsilon\_0 = \frac{1}{2}\\), and thus we get back the energy levels we derived earlier.

In addition, we have,

\\[
a\ket{n} = \sqrt{n}\ket{n-1}
\\]
\\[
a^\dagger\ket{n}=\sqrt{n+1}\ket{n+1}
\\]
\\[
a^\dagger a\ket{n} = n\ket{n}
\\]

These relations allow us to compute the matrix elements of operators in the \\(\ket{n}\\) basis by inverting the earlier relations for \\(X\\) and \\(P\\).

We can also express

\\[
\ket{n} = \frac{(a^\dagger)^n}{\sqrt{n}}\ket{0}
\\]

<!--list-separator-->

-  X-basis

    \\[
    \braket{x}{n} = \frac{1}{\sqrt{n!}}\left[\frac{1}{\sqrt{2}}\left(y-\dv{}{y}\right)\right]^n\left(\frac{m\omega}{\pi\hbar}\right)^{1/4} e^{-y^2/2}
    \\]

    where \\(y = \sqrt{\frac{\hbar}{m\omega}}x\\)


## Path integral formulation {#path-integral-formulation}

Finding propogators has been hard.


## Stern-Gerlach {#stern-gerlach}

The intrinsic spin angular momentum of a particle, we write

\\[
\bm{\mu} = \frac{gq}{2mc}\bm{S}
\\]

The force by the magnet equals:

\\[
F\_z = \mu\_B \pdv{B}{z}
\\]

where u_b is the bohr magneton


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