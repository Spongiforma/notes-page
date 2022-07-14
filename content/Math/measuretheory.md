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
A\cup B \in \mathcal{R}
\\],

.
\\[
A-B \in \mathcal{R}
\\].

Notice that the conditions imply \\(A \cap B \in \mathcal{R}\\) if its a ring.

A ring is called a \\(\sigma\\) ring if

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


### Lebesgue measure {#lebesgue-measure}

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

1.  If there is a sequence of elementary sets converging to \\(A\\), we say its **finitely \\(\mu\\) measurable**

and write \\(A \in \mathfrak{M}\_F(\mu)\\).

1.  If \\(A\\) is the union of a countable collection of finitely \\(\mu\\) measurable sets, then \\(A\\) is \\(\mu\\) measureable and write \\(A \in \mathfrak{M}(\mu)\\).

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

The distance function is almost a true metric but different sets can have zero distance. Thus we may instead define equivalence in terms of vanishing distance. This equivalence relation makes \\(\mathfrak{M}\_F(\mu)\\) be the closure of \\(\mathcal{E}\\).j

<div class="prop">

\\(\mathfrak{M}(\mu)\\) is a $&sigma;$-ring and \\(\mu^\*\\) is countably additive on \\(\mathfrak{M}(\mu)\\).

</div>

The extended set function is called a measure, and the Lebesgue measure on \\(\mathbb{R}^p\\) is thus the special case \\(\mu = m\\).


### Borel sets {#borel-sets}

A borel set is a set that can be obtained by a countable number of unions,intersectoins or complements starting from open sets. The collection of all Borel sets is a \\(\sigma\\) -ring, in fact the smallest one which contains all open sets. An element of a borel set is \\(\mu\\) measureable. Every \\(\mu\\) measurable set is the union of a Borel set and a set of measure zero.


## Measure spaces {#measure-spaces}

<div class="defn">

A set \\(X\\) is a **measure space** if there exists a \\(\sigma\\) ring \\(\mathfrak{M}\\) of subsets of \\(X\\) (the measurable sets) and a non-negative countably additive measure defined on \\(\mathfrak{M}\\). If, in adddition, \\(X \in \mathfrak{M}\\), then \\(X\\) is said to be a **measurable space**.

</div>


### Measurable functions {#measurable-functions}

<div class="defn">

A function is **measurable** if the set \\(\\{x | f(x) > a\\}\\) is measurable for every real \\(a\\). Equality can be included.

</div>

<div class="prop">

Making more measurable functions.

1.  If \\(f\\) is measurable, then \\(|f|\\) is measurable.
2.  Let \\(\\{f\_n\\}\\) be a sequence of measurable functions. For \\(x \in X\\), put

\\[
g(x) = \sup f\_n(x)
\\]

\\[
h(x) = \lim\_{n\to\infty}\sup f\_n(x)
\\],
Then \\(g\\) and \\(h\\) are measurable.

This results in the following corollaries,

1.  If \\(f\\) and \\(g\\) are measurable, then \\(\max(f,g)\\) and \\(\min(f,g)\\) are measurable
2.  The limit of a convergent sequence of measurable functions is measurable.

</div>

Common binary operations are also preserve measurability.

<div class="thrm">

Let \\(f\\) and \\(g\\) be measurable real-valued functions defiend on \\(X\\), let \\(F\\) be real and continuous on \\(\mathbb{R}^2\\). Then \\(F(f(x),g(x))\\) is measurable.

</div>

Thus common operations of analysis can be applied to measurable functions to give measurable functions. An example where measurability doesn't carry over is \\(h(x) = f(g(x))\\), where \\(f\\) is measurable and \\(g\\) is continuous, but \\(h\\) is not necessarily measurable. Interestingly, we were able to define measurable functions without referencing any particular measure. Thus, the class of measurable functions on \\(X\\) depends on the \\(\sigma\\) ring \\(\mathfrak{M}\\).


### Simple functions {#simple-functions}

<div class="defn">

Let \\(s\\) be a real-valued function defined on \\(X\\). If the range of \\(s\\) is finite, then \\(s\\) is a **simple function**. Let \\(E \subseteq X\\) and put define \\(K\_E(x) = 1\\)  when \\(x\in E\\) and zero otherwise as the **characteristic function** of \\(E\\). Denoting \\(E\_i = s^{-1}(\\{c\_i\\})\\) where \\(c\_i\\) make up the range of \\(s\\), we can decompose any simple function into a linear combinations of characteristic functions,
\\[
s = \sum\_{i=1}^n c\_i K\_{E\_i}.
\\]

\\(s\\) is measurable iff \\(E\_i\\) are measurable.

</div>

This allows us to approximate every function by simple functions.

<div class="thrm">

Let \\(f\\) be a real function on \\(X\\). There exists a sequence \\(\\{s\_n\\}\\) of simple funcitons such that \\(s\_n(x) \to f(x)\\) as \\(n \to \infty\\), for every \\(x \in X\\). If \\(f\\) is measurable, \\(\\{s\_n\\}\\) may be chosen to be a sequence of measurable functions. If \\(f\geq 0\\), \\(\\{s\_n\\}\\) may be chosen to be a monotonically increasing sequence.

</div>

\\(s\_n\\) can be constructed as

\\[
s\_n = \sum\_{i=1}^{n2^n}\frac{i-1}{2^n} K\_{E\_{ni}} + n K\_{F\_n}
\\]

for non-negative \\(f\\). For general functions, the function can be split into the difference between its positive and negative components. The sequence converges uniformly to \\(f\\) if \\(f\\) is bounded.


## Lebesgue Integration {#lebesgue-integration}

<div class="defn">

Suppose \\((x \in X, c\_i > 0)\\)
\\[
s(x) = \sum\_{i=1}^n c\_i K\_{E\_i}(x)
\\]
is measurable and \\(E \in \mathfrak{M}\\). We define

\\[
I\_E(s) = \sum\_{i=1}^n c\_i \mu(E \cap E\_i).
\\]
If \\(f\\) is measurable and non-negative, we define

\\[
\int\_E f \dd{\mu} = \sup I\_E(s),
\\]

where the sup is taken over all measurable simple functions \\(s\\) such that \\(0 \leq s \leq f\\).

</div>

The integral may have the value \\(+ \infty\\). If the integral of each of the positive and negative components of a function is finite, then \\(f\\) is said to be **integrable**, or \\(f \in \mathcal{L}(\mu)\\). Integrability carries over to subsets.

<div class="thrm">

Suppose \\(f\\) is measurable and non-negative on \\(X\\). For \\(A \in \mathfrak{M}\\), define

\\[
\phi(A) = \int\_A f\dd{\mu}.
\\]

Then \\(\phi\\) is countably additive on \\(\mathfrak{M}\\). The same conclusion holds for any \\(f \in \mathcal{L}(\mu)\\).

</div>

<div class="thrm">

Suppose \\(E\in\mathfrak{M}\\). Let \\(\\{f\_n\\}\\) be a sequence of measurable functions such that \\(0 \leq f\_1(x) \leq f\_2(x) \leq \ldots\\). Let \\(f\\) be defined by \\(f\_n(x) \to f(x)\\) as \\(n\to\infty\\). Then

\\[
\int\_E f\_n \dd{\mu} \to \int\_E f\dd{\mu}
\\]

</div>

A corollary of the result is that the lebesgue integral and summation of a sequence of measurable functions commute.

<div class="thrm">

Suppose \\(E \in \mathfrak{M}\\). If \\(\\{f\_n\\}\\) is a sequence of non-negative measurable functions and

\\[
f(x) = \lim\_{n\to\infty}\inf f\_n(x),
\\]

then

\\[
\int\_E f \dd{\mu} \leq \lim\_{n\to\infty} \inf \int\_E f\_n \dd{\mu}
\\]

</div>

<div class="thrm">

Suppose \\(E \in \mathfrak{M}\\). Let \\(\\{f\_n\\}\\) be a sequence of measurable functions such that
\\[
f\_n(x) \to f(x)
\\]
as \\(n\to\infty\\). If there exists a function \\(g \in \mathcal{L}(\mu)\\) such that

\\[
\vert f\_n(x) | \leq g(x)
\\]

for all \\(n\\), then,

\\[
\lim\_{n\to\infty} \int\_E f\_n \dd{\mu} = \int\_E f \dd{\mu}
\\]

</div>

In summary, the limits of measurable functions are always measurable, whereas the limits of Riemann-integrable functions may fail to be Riemann-integrable.