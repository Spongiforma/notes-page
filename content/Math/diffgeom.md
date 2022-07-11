+++
title = "Smooth manifolds"
author = ["root"]
draft = false
+++

Adapted from Lee's ISM.


## Smooth manifolds {#smooth-manifolds}

A topological manifold is hausdorff, second-countable and locally euclidean.


## Smooth maps {#smooth-maps}

<div class="defn">

\\(f : M\to\mathbb{R}^K\\) is a **smooth function** if for every \\(p \in M\\), there exist a smooth chart \\((U,\varphi)\\) for M whose domain contains p and such that the composite function \\(f \circ \phi^{-1}\\) is smooth on the open subset \\(\hat{U} = \phi(U) \subseteq \mathbb{R}^n\\).

</div>


## Cotangent bundle {#cotangent-bundle}

The cotangent bundle is the dual space to the tangent bundle. i.e. the linear functionals which take in tangent vectors.


### Covectors {#covectors}

<div class="defn">

For a given vector space, a covector is a real-valued linear functional on V. The vector space of covectors on \\(V\\) form its dual space.

The basis of the dual space are the covectors \\(\epsilon^i(E\_j) = \delta^i\_j\\).

</div>

While vectors are expanded in terms of their bases like \\(v^iE\_i\\), covectors are expanded as \\(\omega\_i\varepsilon^i\\)

<div class="defn">

The **dual map** of a linear map \\(A : V\to W\\) is defined by

\\[
(A^\*\omega)(v) = \omega(Av)
\\]
for \\(\omega \in W^\*, v\in V\\).

</div>

It can be shown that '\*' operator is a contravariant functor from the category of real vector spaces to itself.


#### Second dual space {#second-dual-space}

For each vector space, there is a natural, basis-independent map \\(\xi: V \to V^{\*\*}\\), defined as follows. For each vector \\(v \in V\\), define a linear functional \\(\xi(v) : V^{ \* } \to \mathbb{R}\\) by

\\[
\xi(v)(\omega) = \omega(v)
\\] for \\(\omega \in V^\*\\)

Recall the following elementary result on second dual spaces.

<div class="prop">

For any finite-dimensional vector space V, the map \\(\xi: V\to V^{\*\*}\\) is an isomorphism

</div>

This proposition allows us to denote the the application of a covector t oa vector by either \\(\langle \omega, v \rangle\\) or \\(\langle \omega, v \rangle\\).


### Tangent covectors on manifolds {#tangent-covectors-on-manifolds}

The **cotangent space at p**, is the dual space to \\(T\_p M\\), denoted \\(T^\*\_p M\\). Given smooth local coordinates \\((x^i)\\), the coordinate basis \\((\partial\_i|\_p)\\) gives rise to a dual basis for \\(T^\*\_p M\\), which will be denoted as \\((dx^i|\_p)\\). Thus any such covector can be written uniquely as \\(\omega = \omega\_i dx^i|\_p\\), where \\(\omega\_i = \omega(\partial\_i|\_p)\\).

Recall from the discussion of tangent spaces that two different smooth coordinates transform into one another by the following transformation of their coordinate vector fields,

\\[
\pdv{}{x^i}\bigg\rvert\_p = \pdv{\tilde{x}^j}{x^i}(p) \pdv{}{\tilde{x}^j}\bigg\rvert\_p.
\\]

The components of a covector thus transform as follows

\\[
\omega\_i = \pdv{\tilde{x}^j}{x^i}(p)\tilde{\omega}\_j
\\]

Compare this with the transformation law of components tangent vectors,

\\[
\tilde{v}^j = \pdv{\tilde{x}^j}{x^i}(p) v^i
\\]

Thus, tangent covectors are **covariant** vectors because they transform in the same way as the partial derivatives, while tangent vectors are called **contravariant vectors**. This is due to the components of the vectors being the quantities of interest in the past, vectors being treated as n-tuples.


## Tensors {#tensors}

A map \\(F: V\_1 \times \ldots \times V\_k \to W\\) is multilinear if it is linear as a function of each variable when the others are held fixed. The set of all multilinear maps between a particular domain and codomain is a vector space.


### Tensor product {#tensor-product}

Let \\(V\\) be a vector space, and \\(\omega,\eta \in V^\*\\). Define a function \\(\omega \otimes \eta : V \times V \to \mathbb{R}\\)

\\[
\omega \otimes \eta(v\_1,v\_2) = \omega(v\_1)\eta(v\_2),
\\]

where the product is regular multiplications of real numbers. Generalising to arbitrary multilinear functionals acting on a product of vector spaces, we get the **tensor product**. Notice its bilinearity and associativity.

\#+ATTR_LATEX :options [Basis for multilinear functions]

<div class="prop">

Let \\(V\_1,\ldots,V\_k\\) be real vector spaces of dimensions \\(n\_1,\ldots,n\_k\\) respectivley. Let \\((E^{(j)}\_i)\\) be a basis for \\(V\_j\\) and \\((\epsilon^i\_{(j)})\\) be the corresponding basis for \\(V^\*\_j\\). Then the set

\\[
\mathcal{B} = \left\\{ \epsilon^{i\_1}\_{(1)}\otimes\ldots\otimes\epsilon^{i\_k}\_{(k)} : 1\leq i\_1 \leq n\_1,\ldots,1\leq i\_k \leq n\_k \right\\}
\\]

is a basis for \\(L(V\_1,\ldots,V\_k:\mathbb{R})\\), which therefore has dimension equal to \\(n\_1\ldots n\_k\\).

</div>


### Abstract tensor products {#abstract-tensor-products}

<div class="defn">

A **formal linear combination** of elements of a set S is a function \\(f : S \to \mathbb{R}\\) such that \\(f(s) = 0\\) for all but finitely many elements of S. The **free (real) vector space on S**, denoted by \\(\mathcal{F}(S)\\) is the set of all formal linear combinations of elements of S.

</div>

Each element \\(f \in \mathcaL{F}(S)\\) can be written uniquely in the form \\(f = \sum^m\_{i=1} a\_i x\_i\\), where \\(x\_1,\ldots,x\_m\\) are the elements of S for which \\(f(x\_i) \neq 0\\), and \\(a\_i = f(x\_i)\\). We identify \\(x \in S\\) with the function \\(\delta\_x \in \mathcal{F}(S)\\) that takes the value 1 on \\(x\\) and zero on all other elements of S. Thus \\(S\\) is a basis for the free vector space.

\#+ATTR_LATEX :options [Characteristic Property of the Free Vector Space]

<div class="prop">

For any set \\(S\\) and any vector space \\(W\\), every map \\(A: S \rightarrow W\\) has a unique extension to a linear map \\(\bar{A}: \mathcal{F}(S) \rightarrow W\\)

</div>

Now let \\(\mathcal{R}\\) be the subspace of \\(\mathcal{F}(V\_1\times\ldots\times V\_k)\\) spanned by all the elements of the forms

\\[
\left(v\_{1}, \ldots, a v\_{i}, \ldots, v\_{k}\right)-a\left(v\_{1}, \ldots, v\_{i}, \ldots, v\_{k}\right)
\\]

\\[
\left(v\_{1}, \ldots, v\_{i}+v\_{i}^{\prime}, \ldots, v\_{k}\right)-\left(v\_{1}, \ldots, v\_{i}, \ldots, v\_{k}\right)-\left(v\_{1}, \ldots, v\_{i}^{\prime}, \ldots, v\_{k}\right)
\\]

with \\(v\_{j}, v\_{j}^{\prime} \in V\_{j}, i \in\\{1, \ldots, k\\}\\), and \\(a \in \mathbb{R}\\).

Define the tensor product of the spaces \\(V\_{1}, \ldots, V\_{k}\\), denoted by \\(V\_{1} \otimes \cdots \otimes V\_{k}\\), to be the following quotient vector space:

\\[
V\_{1} \otimes \cdots \otimes V\_{k}=\mathcal{F}\left(V\_{1} \times \cdots \times V\_{k}\right) / \mathcal{R},
\\]

and let \\(\Pi: \mathcal{F}\left(V\_{1} \times \cdots \times V\_{k}\right) \rightarrow V\_{1} \otimes \cdots \otimes V\_{k}\\) be the natural projection. The equivalence class of an element \\(\left(v\_{1}, \ldots, v\_{k}\right)\\) in \\(V\_{1} \otimes \cdots \otimes V\_{k}\\) is denoted by

\\[
v\_{1} \otimes \cdots \otimes v\_{k}=\Pi\left(v\_{1}, \ldots, v\_{k}\right),
\\]

and is called the **(abstract) tensor product** of \\(v\_{1}, \ldots, v\_{k}\\). It follows from the definition that abstract tensor products satisfy

\begin{aligned}
v\_{1} \otimes \cdots \otimes a v\_{i} \otimes \cdots \otimes v\_{k}= & a\left(v\_{1} \otimes \cdots \otimes v\_{i} \otimes \cdots \otimes v\_{k}\right) \\\\
v\_{1} \otimes \cdots \otimes\left(v\_{i}+v\_{i}^{\prime}\right) \otimes \cdots \otimes v\_{k}=&\left(v\_{1} \otimes \cdots \otimes v\_{i} \otimes \cdots \otimes v\_{k}\right) \\\\
&+\left(v\_{1} \otimes \cdots \otimes v\_{i}^{\prime} \otimes \cdots \otimes v\_{k}\right)
\end{aligned}

Note not every element of the tensor product space is of the form \\(v\_1 \otimes \ldots \otimes v\_k\\).

An analogue of the basis proposition for multilinear functions holds for abstract tensor product spaces.


## Differential forms {#differential-forms}