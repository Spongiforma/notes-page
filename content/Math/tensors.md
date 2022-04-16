+++
title = "Tensors"
author = ["root"]
draft = false
+++

## Cartesian tensors {#cartesian-tensors}


### Change of basis {#change-of-basis}

When basis vectors change by:

\\[
\bm{e}\_j' = S\_{ij}\bm{e}\_i
\\]

\\[
\bm{x}' = S^{-1}x
\\]

As components change inversely with the basis vectors. Thus a linear operator \\(\mathcal{A}\\) represented by \\(A\\) in a given coordinate system is represented by \\(A' = S^{-1}AS\\) in a new coordinate system.

For rigid body rotations, the transformation matrix \\(L\\) is orthogonal (since it must preserve inner products).

The transformation matrix is given by \\(L\_{ij} = \bm{e}\_i'\cdot\bm{e}\_j = \partial{x\_j}/\partial{x\_i'}\\). The following orthogonality relations hold:

\\[
L\_{ik}L\_{jk} = \delta\_{ij}
\\]
\\[
L\_{ki}L\_{kj} = \delta\_{ij}
\\]


### First and zero-order cartesian tensors {#first-and-zero-order-cartesian-tensors}

Consider any set of three quantities \\(v\_i\\) which are functions of coordinates \\(x\_i\\).

If the form of \\(v\_i'\\) in new variables can be obtained from old ones as follows,

\\[
v\_i' = L\_{ij}v\_j
\\]

\\(v\_i\\) are said to form the components of a _vector_ or _first-order Cartesian tensor_ \\(\bm{v}\\), such that \\(\bm{v} = v\_i\bm{e}\_i = v\_i'\bm{e}\_i'\\).


#### Example: Do the following form the components of a first-order Cartesian tensor? {#example-do-the-following-form-the-components-of-a-first-order-cartesian-tensor}

Denoting \\(\sin\theta\\) by \\(s\\) and \\(\cos\theta\\) by \\(c\\),

1.  \\(v = (x\_2,-x\_1)\\)

\\[
v\_1' = x\_2' = -sx\_1 + cx\_2
\\]

\\[
v\_2' = -x\_1' = -cx\_1 - sx\_2
\\]

For a cartesian tensor,

\\[
v\_1' = L\_{11}v\_1 + L\_{12}v\_2 = cx\_2 + s(-x\_1)
\\]

\\[
v\_2' = L\_{21}v\_1 + L\_{22}v\_2 = -s(x\_2) + c(-x\_1)
\\]

Since the expressions are the same regardless of \\(\theta\\), the pair \\((x\_2,-x\_1)\\) is a first-order cartesian tensor.


#### Zero-order tensors {#zero-order-tensors}

Scalars or tensors of zero-order contain only one element. An example is the square of the distance of a point from the origin. In fact, any scalar product of two first-order tensors is a zero-order tensor (can be shown using orthogonality of transformation matrix).


### Second- and higher-order Cartesian tensors {#second-and-higher-order-cartesian-tensors}

\\[
T\_{ij}' = L\_{ik}L\_{jl}T\_{kl}
\\]
\\[
T\_{ij} = L\_{kl}L\_{lj}T\_{kl}'
\\]

For higher orders;

\\[
T\_{ij\ldots k}' = L\_{ip}L\_{jq}\ldots L\_{kr}T\_{pq\ldots r}
\\]
\\[
T\_{ij\ldots k} = L\_{pi}L\_{qj}\ldots L\_{rk}T\_{pq\ldots r}'
\\]

In three dimensions, an Nth order Cartesian tensor has \\(3^{N}\\) components. Linear operators are not always tensors as the two subscripts in the 2nd order tensor must refer to the same coordinate system.


#### Outer product {#outer-product}

\\[
T\_{ij} = u\_iv\_j
\\]

Denoted as:

\\[
\bm{T} = \bm{u}\otimes\bm{v}
\\]


#### Gradient of vector {#gradient-of-vector}

\\[
T\_{ij} = \pdv{v\_i}{x\_j}
\\]

Denoted as:

\\[
\bm{T} = \nabla\bm{v}
\\]


#### Levi-Civita symbol {#levi-civita-symbol}

\\(\epsilon\_{ijk}\\) is totally antisymmetric (swapping indices turns it negative), and is the only three-subscript quantity with the property.

It can be turned into a Laplace (cofactor) expansion for finding the determinant of a 3x3 matrix by choosing l,m,n. (Sarrus' law)

\\[
\vert A \vert \epsilon\_{lmn} = A\_{li}A\_{mj}A\_{nk}\epsilon\_{ijk}
\\]

Note:

\\[
\epsilon\_{lmn}' = L\_{li}L\_{mj}L\_{nk}\epsilon\_{ijk} = |L|\epsilon\_{lmn}
\\]

Since \\(|L|\\) is unity as \\(L\\) is orthogonal,it is a third order Cartesian tensor.

Upon contraction:

\\[
\epsilon\_{ijk}\epsilon\_{ijk} = 6
\\]

Cross product \\(\bm{a} = \bm{b}\times\bm{c}\\), can be represented as:

\\[
a\_i = \epsilon\_{ijk}b\_jc\_k
\\]

<!--list-separator-->

-  Curl

    \\[
    (\curl \bm{v})\_i = \epsilon\_{ijk}\pdv{v\_k}{x\_j}
    \\]

<!--list-separator-->

-  Grad of div

    \\[
    [\grad(\div \bm{v})]\_i = \pdv{}{x\_i}\left(\pdv{v\_j}{x\_j}\right) = \delta\_{jk} \pdv{v\_j}{x\_i,x\_k}
    \\]

<!--list-separator-->

-  Curl of curl

    \\[
    [\curl (\curl \bm{v})]\_i = \epsilon\_{ijk}\pdv{}{x\_j}\left(\epsilon\_{klm}\pdv{v\_m}{x\_l}\right) = \epsilon\_{ijk}\epsilon\_{klm}\pdv{v\_m}{x\_j,x\_l}
    \\]

<!--list-separator-->

-  Scalar triple product

    \\[
    (\bm{a} \times \bm{b}) \cdot \bm{c} = \delta\_{ij}c\_i\epsilon\_{jkl}a\_kb\_l = \epsilon\_{ikl}c\_ia\_kb\_l
    \\]

<!--list-separator-->

-  Relationship with kronecker delta

    \\[
    \epsilon\_{ijk}\epsilon\_{klm} = \delta\_{il}\delta\_{jm} - \delta\_{im}\delta\_{jl}
    \\]

    \\[
    \epsilon\_{ijk}\epsilon\_{pqr} = \mqty|\delta\_{ip} & \delta\_{iq} & \delta\_{ir} \\\ \delta\_{jp} & \delta\_{jq} & \delta\_{jr} \\\ \delta\_{kp} & \delta\_{kq} & \delta\_{kr}|
    \\]

    Variations:

    \\[
    \epsilon\_{ijk}\epsilon\_{ilm} = \delta\_{jl}\delta\_{km} - \delta\_{jm}\delta\_{kl}
    \\]


### Isotropic tensors {#isotropic-tensors}

Tensors whose component values are independent of coordinate frames are called isotropic (or invariant) tensors. Kronecker delta and Levi-civita (and scalar multiples) are the only second and third order isotropic tensors.


### Operations {#operations}


#### Contraction {#contraction}

You set two indices to be the same.


#### Quotient law {#quotient-law}

It can be shown that if:

\\[
A\_{ij..k..m}B\_{np..k..t} = C\_{ij..mnp..t}
\\]

and B and C are tensors, then A is also a tensor.


### Parity {#parity}

If we include improper rotations, \\(|L| = -1\\), which is equivalent to shifting from a right-handed to left-handed coordinate system under a passive transformation, we must distinguish pseudotensors, which change parity under improper rotations, and tensors which always maintain parity under all rotations.

When looking at active transforms, then you have axial (maintain direction under inversion of coordinate system) and polar vectors (which don't).

No physical quantity can be described with pseudotensors.

The levi-civita tensor is an example of a pseudotensor.


### Dual tensors {#dual-tensors}

Pseudotensors have their uses.

We may associate every _antisymmetric_ second-order tensor \\(A\_{ij}\\) with a pseudovector \\(p\_i\\) given by:

\\[
p\_i = \frac12 \epsilon\_{ijk}A\_{jk}
\\]

For example,

The dual of the antisymmetric tensor \\(A\\):

\\[
\text{A} = [A\_{ij}] = \mqty( 0 & A\_{12} & -A\_{31} \\\ -A\_{12} & 0 & A\_{23} \\\ A\_{31} & -A\_{23} & 0)
\\]

is \\((A\_{23},A\_{31},A\_{12})\\).

Notice that the following identity holds:

\\[
A\_{ij} = \epsilon\_{ijk}p\_k
\\]


#### Third rank {#third-rank}

We may extend this to associate a dual pseudoscalar \\(s\\) with every totally antisymmetric third-rank tensor \\(A\_{ijk}\\). \\(s\\) is given by:

\\[
s = \frac{1}{3!}\epsilon\_{ijk}A\_{ijk}
\\]

Similarly,

\\[
A\_{ijk} = s \epsilon\_{ijk}
\\]


### Integral theorems {#integral-theorems}

The usual integral theorems can be extended trivially to tensor fields


## Non-Cartesian coordinates {#non-cartesian-coordinates}

A position of a point in space may be expressed in terms of three curvilinear coordinates \\(u\_1,u\_2,u\_3\\). if \\(\bm{r}(u\_1,u\_2,u\_3)\\) is the position vector of the point P then at P there exist two sets of basis vectors.

\\[
\bm{e}\_i = \pdv{\bm{r}}{u\_i}
\\]

and

\\[
\bm{\epsilon}\_i = \grad u\_i
\\]

these sets are reciprocal systems of vectors so:

\\[
\bm{e}\_i \cdot \bm{\epsilon}\_j = \delta\_{ij}
\\]

Introducing superscripts, this can be written:

\\[
\bm{e}\_i \cdot \bm{e}^j = \delta\_i^j
\\]

When we write a general vector \\(\bm{a}\\) in terms of either basis:

\\[
\bm{a} =  a^i\bm{e}\_i = a\_i\bm{e}^i
\\]

\\(a^i\\) are called the **contravariant** components and \\(a\_i\\) the **covariant** components.

For Cartesian coordinates, two two sets are identical.


### Metric tensor {#metric-tensor}

Any particularly curvilinear coordinate system is completely characterized by the nine quantities:

\\[
g\_{ij} = \bm{e}\_i \cdot \bm{e}\_j
\\]

which are the covariant components of a symmetric second-order tensor called the metric tensor.

\\[
(\dd{s})^2 = g\_{ij}\dd{u}^i\dd{u}^j
\\]

\\[
\dd{V} = \sqrt{g}\dd{u}^1\dd{u}^2\dd{u}^3
\\]

where g is the determinant of the tensor \\([g\_{ij}]\\).

The metric tensor is diagonal for orthogonal coordinate systems, with the diagonal elements being equal to the squares of the scale factors of the coordinate system.

The metric tensor can be used to lower or raise an index:

\\[
g\_{ij}b^j = b\_i
\\]

\\[
g^{ij}b\_j = b^i
\\]

It may also be shown that:

\\[
\vert\bm{e}\_1 \cdot (\bm{e}\_2 \times \bm{e}\_3)\vert = \sqrt{g}
\\]

\\[
g^{ij}g\_{jk} = \delta\_k^i
\\]


### Coordinate transforms {#coordinate-transforms}

The defining property for a set of quantities \\(a^i\\) to form the contravariant components of a vector is:

\\[
a'^i = \pdv{u'^i}{u^j}a^j
\\]

The relation for basis vectors is this relation's inverse.

Analagously for covariant components of a vector, the relation is the inverse of that of contravariant components. (the prime is on the denominator of the partial derivative)


### Relative tensors {#relative-tensors}

Similar to the discussion on pseudotensors, we are led to the notion of relative tensors for arbitrary coordinate transformations.

We may define the Jacobian of the transformation as the determinant of the transformation matrix \\([\partial u'^i / \partial u^j]\\). Interchanging the primed and unprimed coordinates gives \\(1/J\\).

We define a relative tensor of weight \\(w\\) as one whose components transform as:

\\[
T'^i\_j = \pdv{u'^i}{u^a}\pdv{u^j}{u'^b}T^a\_b \left\vert \pdv{u}{u'} \right\vert^w
\\]

and so on for higher rank tensors.

-   A **true** (or **absolute**) general tensor is a relative tensor of weight 0.
-   If \\(w = -1\\), the relative tensor is a general \*pseudotensor
-   If \\(w = 1\\), it's a **tensor density**.


#### Properties {#properties}

The levi cevita tensor is a relative tensor of weight -1. If you define a contravariant version, it is numerically equal to its covariant counterpart but it has weight +1.

If two relative tensors have weights \\(w\_1\\) and \\(w\_2\\), the outer product or any contraction of them is a relative tensor of weight \\(w\_1 + w\_2\\).


### Derivatives of basis vectors &amp; Christoffel symbols {#derivatives-of-basis-vectors-and-christoffel-symbols}

In general curvilinear coordinates, the basis vectors can change and are a functions of the coordiantes. In general, derivatives can be written as so.

\\[
\pdv{\bm{e}\_i}{u^j} = \Gamma^k\_{ij}\bm{e}\_k
\\]

Using the reciprocity relation:

\\[
\Gamma^k\_{ij} = \bm{e}^k \cdot \pdv{\bm{e}\_i}{u^j}
\\]

Similarly for contravariant basis vectors:

\\[
\pdv{\bm{e}^i}{u^j} = -\Gamma^i\_{kj}\bm{e}^k
\\]

The symbol \\(\Gamma^k\_{ij}\\) is a **Christoffel symbol** (of the second kind). Note that these quantities do not form the components of a third-order tensor.

Note that the Christoffel symbol is symmetric with respect to interchange of its two subscripts.

The quickest way to find the Christoffel symbol is by using the metric tensor.

\\[
\Gamma^m\_{ij} = \frac12 g^{mk}\left(\pdv{g\_{jk}}{u^i} + \pdv{g\_ki}{u^j} - \pdv{g\_ij}{u^k}\right)
\\]


### Covariant differentiation {#covariant-differentiation}

In general, the derivative of a scalar is a covariant vector.

\\[
\dd{\phi} = \pdv{\phi}{u^i}\dd{u^i}
\\]

By quotient law, the quantities \\(\partial \phi / \partial u^i\\) must form the components of a covariant vector.

However, the derivative of the components of a general tensor does not in general result in the components of another tensor, e.g. \\(\partial v^i / \partial u^j\\).

However, we may define a new _covariant_ derivative that does result in the components of another tensor.

We find in general:

\\[
\pdv{\bm{v}}{u^j} = \pdv{v^i}{u^j}\bm{e}\_i + v^i \pdv{\bm{e}\_i}{u^j}
\\]

This can be rewritten:

\\[
\pdv{\bm{v}}{u^j} = \left(\pdv{v^i}{u^j} + v^k \Gamma^i\_{kj}\right) \bm{e}\_i.
\\]

The quantity in parentheses is the **covariant derivative**:

\\[
v^i\_{;j} \equiv \pdv{v^i}{u^j} + v^k \Gamma^i\_{kj}
\\]

For covariant components of a vector, the corresponding result is:

\\[
v\_{i;j} = \pdv{v\_i}{u^j} -  \Gamma^k\_{ij}v\_k
\\]