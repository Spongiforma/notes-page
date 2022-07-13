+++
title = "Measure theory"
author = ["root"]
draft = false
+++

## Borel algebra {#borel-algebra}

If A and B are any two sets, let \\(A- B\\) be the set of all elements in A that are not in B (This does not imply \\(B\subset A\\)).

<div class="defn">

A family \\(\mathcal{R}\\) of sets is called a ring if \\(A,B \in \mathcal{R}\\) implies

\\[
A\cap B \in \mathcal{R}
\\],

.
\\[
A-B \in \mathcal{R}
\\].

Notice that the conditions imply \\(A \cap B \in \mathcal{R}\\) if its a ring.

A ring is called a $&sigma;$-ring if

\\[
\cup\_{n=1}^\infty  A\_n \in \mathcal{R}
\\],

for any countable sequence of sets \\(A\_n \in \mathcal{R}\\).

If this condition is fulfilled, then

\\[
\cap\_{n=1}^\infty  A\_n \in \mathcal{R}
\\]

also holds.

</div>

<div class="defn">

A set function \\(\phi\\) defined on \\(\mathcal{R}\\) assigns to every element of a number \\(\phi(A)\\) of the extended number system. \\(\phi\\) is **additive** if \\(A \cap B = 0\\) implies

\\[
\phi(A\cup B) = \phi(A)+ \phi(B)
\\],

and it is **countably additive** if \\(A\_i \cap A\_j = 0\\) (\\(i \neq j\\)) implies

\\[
\phi(\cap^\infty\_{n=1}A\_n) = \sum^\infty\_{n=1}\phi(A\_n).
\\]

</div>

Notice that nonnegative additive set functions are monotonic by inclusion. In addition, for additive set functions,

\\[
\phi(A-B) = \phi(A) -\phi(B)
\\]

if \\(B\subseteq A\\) and \\(|\phi B| < +\infty\\).

<div class="thrm">

Suppose \\(\phi\\) is countably additive on a ring \\(\mathcal{R}\\). If \\(A\_n \in \mathcal{R}\\) and \\(A\_n\subseteq A\_{n+1}\\),\\(A \in \mathcal{R}\\) and

\\[
A = \cup\_{n=1}^\infty A\_n,
\\]

Then as \\(n\to \infty\\),

\\[
\phi(A\_n) \to \phi(A)
\\]

</div>

A borel set is a set that can be obtained by a countable number of unions,intersectoins or complements starting from open sets. The collection of all Borel sets is a \\(\sigma\\) -ring.


## Lebesgue measure {#lebesgue-measure}

An **elementary set** is a union of a finite element of intervals. The family of all elementary subsets of \\(\mathbb{R}^p\\) is denoted \\(\mathcal{E}\\).

The following properties may be verified,

1.  \\(\mathcal{E}\\) is a ring but not a $&sigma;$-ring.
2.  \\(m\\) defined by \\(m([a,b]) = \Pi\_{i=1}^p (b\_i-a\_i)\\) is well defined and additive on \\(\mathcal{E}\\).

<div class="defn">

A nonnegative additive set function is **regular** if for every \\(A \in \mathcal{E}\\) and to every \\(\varepsilon > 0\\) there exist sets \\(F,G \in \mathcal{E}\\) such that \\(F\\) is closed, \\(G\\) is open, \\(F \subset A \subset G\\), and

\\[
\phi(G) - \varepsilon \leq \phi(A) \leq \phi(F)+\varepsilon
\\]

</div>

<div class="eg">

\\(m\\) is regular, \\(\mu(a,b) = \alpha(b) - \alpha(a)\\) where \\(\alpha\\) is monotonically increasing is regular on the real line.

</div>

Every regular set function on \\(\mathcal{E}\\) can be extended to a countably additive set function on a \\(\sigma\\) -ring which contains \\(\mathcal{E}\\).

<div class="defn">

Let \\(\mu\\) be additive, regular, nonnegative and finite on \\(\mathcal{E}\\). Consider countable coverings of any set \\(E\subseteq \mathbb{R}^p\\) by open elementary sets \\(A\_n\\):

\\[
E \subseteq \cup\_{n=1}^\infty A\_n
\\]

Define
\\[
\mu^\*(E) = \inf \sum\_{n=1}^\infty \mu(A\_n),
\\]
the inf being taken over all countable coverings of \\(E\\) by open elementary sets. \\(\mu^\*(E)\\) is called the **outer measure** of \\(E\\), corresponding to \\(\mu\\).

</div>

<div class="prop">

Properties of an outer measure.

1.  The outer measure is nonnegative for all \\(E\\).
2.  It is monotonic by inclusion.
3.  Its restriction to elementary set is equivalent to the original measure.
4.  **Subadditivity**: If \\(E = \cup\_1^\infty E\_n\\), then

\\[
\mu^\*(E) \leq \sum\_{n=1}^\infty \mu^\*(E\_n)
\\]

</div>


### Distances between sets {#distances-between-sets}

<div class="defn">

For any \\(A,B\subseteq\mathbb{R}^p\\), we define the symmetric difference and the distance functions

\\[
S(A,B) = (A-B)\cup(B-A)
\\],
\\[
d(A,B) = \mu^\*(S(A,B)).
\\]

We write \\(A\_n \to A\\) if \\(\lim\_{n\to\infty} d(A,A\_n) = 0\\).

1.  If there is a sequence of elementary sets converging to \\(A\\), we say its **finitely $&mu;$-measurable**

and write \\(A \in \mathfrak{M}\_F(\mu)\\).

1.  If \\(A\\) is the union of a countable collection of finitely $&mu;$-measurable sets, then \\(A\\) is $&mu;$-measureable and write \\(A \in \mathfrak{M}(\mu)\\).

</div>

<div class="prop">

Properties of the symmetric difference and the distance function.

1.  \\(S(A,B)\subseteq S(A,C)\cup S(C,B)\\).
2.  \\(S(A\_1 \cup A\_2,B\_1\cup B\_2), S(A\_1 \cap A\_2,B\_1\cap B\_2), S(A\_1 - A\_2,B\_1- B\_2) \subseteq S(A\_1,B\_1) \cup S(A\_2,B\_2)\\)

The distance function follow analagous relations with the relevant set operations becoming the appropriate arithmetic operations.

There is also the property

\\[
 \vert \mu^\*(A) - \mu^\*(B) | \leq d(A,B)
\\]

if at least one of \\(\mu^\*(A),\mu^\*(B)\\) is finite.

</div>

The distance function is almost a true metric but different sets can have zero distance. Thus we may instead define equivalence in terms of vanishing distance. This equivalence relation makes \\(\mathfrak{M}\_F(\mu)\\) to be the closure of \\(\mathcal{E}\\).j

<div class="prop">

\\(\mathfrak{M}(\mu)\\) is a $&sigma;$-ring and \\(\mu^\*\\) is countably additive on \\(\mathfrak{M}(\mu)\\).

</div>

The extended set function is called a measure, and the Lebesgue measure on \\(\mathbb{R}^p\\) is thus the special case \\(\mu = m\\).