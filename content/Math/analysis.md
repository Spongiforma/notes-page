+++
title = "Analysis"
author = ["root"]
draft = false
+++

## Real numbers {#real-numbers}

**Theorem**

There exists an ordered field R which has the least-upper-bound property. R contains Q as a subfield

**Theorem**
If \\(x \in R\\), \\(y \in R\\), and \\(x > 0\\), then there's a positive integer \\(n\\) such that \\(nx > y\\).
If \\(x < y\\), then there exists a \\(p \in Q\\) such that \\(x < p < y\\)

**Theorem**

For every positive real x and every positive integer n, there is only one positive real y such that \\(y^n = x\\)

**Defintion**

An ordered field is a field which is an ordered set, such that:

1.  \\(x + y < x + z\\) and  \\(y < z\\)
2.  \\(xy > 0\\) and \\(x > 0, y > 0\\)


## Sequences {#sequences}

A sequence converges if it fulfills epsilon-delta, i.e. for every \\(\epsilon > 0\\), there is an integer N, such that \\(n \geq N\\) implies \\(d(p\_n,p) < \epsilon\\).

**Other properties**

1.  Every neighbourhood of p contains \\(p\_n\\) for all but finitely many \\(n\\).
2.  If \\(E \subset X\\), and \\(p\\) is a limit point of E, then there is a sequence \\(\\{p\_n\\}\\) in \\(E\\) such that \\(p = \lim\_{n\to\infty} p\_n\\).

**Definition**

If a subsequence of a sequence converges, its limit is called a subsequential limit of the sequence. A sequence only converges iff every subsequence of \\(\left{p\_n\right}\\) converges to p.

**Theorem**

1.  If \\(\\{p\_n\\}\\) is sequence in a compact space X, the nsome subsequence of \\(\\{p\_n\\}\\) converges to a point of X.
2.  Every bounded sequence in \\(R^k\\) contains a convergent subsequence.

**Theorem**

The subsequential limits of a sequence \\(\\{p\_n\\}\\) in a metric space X form a closed subset of X.


### Cauchy sequences {#cauchy-sequences}

A sequence \\(\\{p\_n\\}\\) is a Cauchy sequence iff for every \\(\epsilon > 0\\) there is an integer N such that \\(d(p\_n,p\_m) < \epsilon\\) if \\(n,m \geq N\\).

Let E be a nonempty subset of a metric space X, and let S be the set of all real numbers of the form \\(d(p,q)\\), with \\(p\in E\\) and \\(q\in E\\). THe sup of S is called the diameter of E.

If \\(E\_N\\) is the set of all points \\(p\_{N+i}\\), then \\(\\{p\_n\\}\\) is a Cauchy sequence iff \\(\lim\_{N\to\infty} \text{diam} E\_N = 0\\).

**Theorem**

1.  If \\(\bar{E}\\) is the closure of a set \\(E\\) in a metric space X, then \\(\text{diam } \bar{E} = \text{diam } E\\).
2.  If \\(K\_n\\) is a sequence of compact sets in X such that \\(K\_{n+1} \subset K\_n\\), and its diameter tends to 0 with n, then the intersection consists of exactly one point.

**Theorem**

1.  In any metric space X, every convergent sequence is a Cauchy sequence.
2.  If X is a compact metric space and if \\(\\{p\_n\\}\\) is a Cauchy sequence in X, then \\(\\{p\_n\\}\\) converges to some point of X.
3.  In \\(R^k\\), every Cauchy sequence converges.

**Definition**

A metric space in which every Cauchy sequence converges is complete.

**Theorem**

A monotonic sequence converges iff it is bounded.


### Upper and lower limits {#upper-and-lower-limits}

**Definition**
Let E be the set of all subsequential limits of a sequence \\(s\_n\\).

\\[
s^\* = \sup E = \lim\_{n\to\infty} \sup s\_n
\\]

\\[
s\_\* = \inf E = \lim\_{n\to\infty} \inf s\_n
\\]

**Theorem**

1.  \\(s^\* \in E\\)
2.  If \\(x > s^\*\\), there is an integer, there is an integer \\(N\\) such that \\(n \geq N\\) implies \\(s\_n < x\\).

    Moreover, \\(s^\*\\) is the only number with the two properties.


### Convergence {#convergence}

**Definition**

Cauchy criterion:

\\(\sum a\_n\\) converges iff for every \\(\epsilon > 0\\), there is an integer \\(N\\) such that:

\\[
\left\vert \sum\_{k=n}^m a\_k \right\vert \leq \epsilon
\\]

if \\(m \geq n \geq N\\).

or when m equals n,

\\[
\vert a\_n \vert \leq \epsilon
\\]

**Theorem**

Suppose \\(a\_n\\) is non-negative monotonically decreasing sequence. Then its series converges iff the following series converges:

\\[
\sum\_{k=0}^\infty 2^ka\_{2^k} = a\_1 + 2a\_2 + 4a\_4 + 8a\_8 + \ldots
\\]

**Theorem**

\\[
\sum\_{n=2}^\infty  \frac{1}{n (\log n)^p}
\\]

converges when p is greater than one, and diverges otherwise.


### Root and ratio test {#root-and-ratio-test}

**Theorem (Root test)**
Given \\(\sum a\_n\\), put \\(\alpha = \lim\_{n\to\infty}\sup\sqrt[n]{|a\_n|}\\)

If \\(\alpha < 1\\), it converges, if \\(\alpha > 1\\), it diverges.

**Theorem (Ratio test)**

A series converges if \\(\lim\_{n\to\infty} \vert\frac{a\_{n+1}}{a\_n}\vert < 1\\), and diverges if the sequence is monotonically increasing at some finite point.

**Theorem**

\\[
\lim\_{n\to\infty} \frac{c\_{n+1}}{c\_n} \leq \lim\_{n\to\infty} \inf \sqrt[n]{c\_n}
\\]

\\[
\lim\_{n\to\infty} \sup \sqrt[n]{c\_n} \leq \lim\_{n\to\infty} \sup \frac{c\_{n+1}}{c\_n}
\\]

**Theorem**

Given a power series \\(\sum c\_n z^n\\), put \\(\alpha = \lim\_{n\to\infty}\sup \sqrt[n]{|c\_n|}\\), and \\(R = \alpha^{-1}\\). Then the series converges if \\(|z| < R\\), and diverges if \\(|z| > R\\).


#### Summation by parts {#summation-by-parts}

\\[
\sum\_{n=p}^q a\_n b\_n = \sum\_{n=p}^{q-1} A\_n (b\_n - b\_{n+1}) + A\_q b\_q - A\_{p-1}b\_p
\\]

**Theorem**

If:

1.  The partial sums of \\(A\_n\\) of \\(a\_n\\) form a bounded sequence.
2.  \\(\\{b\_n\\}\\) is monotonoically decreasing
3.  \\(\lim\_{n\to\infty}b\_n = 0\\)

Then \\(\sum a\_n b\_n\\) converges.

**Theorem**
If:

1.  \\(\\{|c\_n|\\}\\) is a monotonically decreasing sequence.
2.  \\(\\{c\_n\\}\\) is an alternating series.
3.  \\(\lim\_{n\to\infty}c\_n = 0\\).

    Then \\(\sum c\_n\\) converges.


#### Absolute convergence {#absolute-convergence}

If a series converges absolutely, then it converges regularly. But a convergent series may not converge absolutely. Consider \\((-1)^n / n\\).

**Theorem**

If \\(\sum a\_n\\) converges absolutely, and \\(c\_n = \sum\_{k=0}^n a\_k b\_{n-k}\\), then \\(\sum\_{n=0}^\infty c\_n = AB\\)

This theorem also holds if no assumption is made iwth absolute convergence.


#### Rearrangements {#rearrangements}

**Theorem (Riemann)**

Let \\(\sum a\_n\\) be a series of real numbers which converges but not absolutely. Suppose \\(-\infty \leq \alpha \leq \beta \leq \infty\\). Then there exists a rearrangement \\(\sum a'\_n\\) with partial sums \\(s'\_n\\) such that:

\\[
\lim\_{n\to\infty}\inf s'\_n = \alpha
\\]

\\[
\lim\_{n\to\infty}\sup s'\_n = \beta
\\]

If \\(\sum a\_n\\) is a series of complex numbers which converges absolutely, then every rearrangement of \\(\sum a\_n\\) converges, and they all converge to the same sum.


## Continuity {#continuity}

**Definition**

Let X and Y be metric spaces, suppose \\(E \subset X\\), f maps E into Y, and p is a limit point of E.

We say $ lim<sub>x&rarr; p</sub>f(x) = q$, if there is a point \\(q \in Y\\) with the property:

For every \\(\epsilon > 0\\), there exists a \\(\delta > 0\\) such that \\(d\_Y(f(x),q) < \epsilon\\) for all points \\(x\in E\\) for which \\(0 < d\_X(x,p) < \delta\\).

**Theorem**

\\(\lim\_{x \to p} f(x) = q\\) iff \\(\lim\_{n \to \infty} f(p\_n) = q\\) for every sequence \\(\\{p\_n\\}\\) in E such that \\(p\_n \neq p\\), \\(\lim\_{n \to \infty} p\_n = p\\).

This also says that this limit is unique.

**Definition**

f is continuous at p if for every \\(\epsilon > 0\\), there exists a \\(delta > 0\\) such that \\(d\_Y(f(x),f(p)) < \epsilon\\) for all points \\(x \in E\\) for which \\(d\_X(x,p) < \delta\\).

If p is also a limit point of E, then f is continuous at p iff \\(\lim\_{x \to p} f(x) = f(p)\\).

**Theorem**

A mapping f of a metric space X into a metric space Y is continous on X iff \\(f^{-1}(V)\\) is open/closed in X for every open/closed set V in Y.


### Compactness {#compactness}

A mapping into \\(R^n\\) is bounded if there is a real number M such that \\(| \bm{f}(x) | \leq M\\) for all x.

**Theorem**

If f is a continuous mapping of a compact metric space X into a metric space Y, then f(X) is compact.

**Theorem**

If f is a continuous mapping of a compact metric space X into \\(R^n\\), then f(X) is closed and bounded, thus f is bounded.

**Theorem**

Suppose f is a continous real function on a compact metric space X, and:

\\[
M = \sup\_{p\in X} f(p)
\\]

\\[
m = \inf\_{p\in X}f(p)
\\]

Then there exists points \\(p,q \in X\\) such that \\(f(p) = M\\) and \\(f(q) = m\\).

**Theorem**

Suppose f is a continous, injective mapping of a copmact metric space X onto a metric space Y. The inverse mapping is a continous mapping of Y onto x.

**Theorem**

A mapping f is _uniformly continuous_ on X if for every \\(\epsilon > 0\\), there exists \\(\delta > 0\\) such that:

\\[
d\_Y(f(p),f(q)) < \epsilon
\\]

for all p,q in X for which \\(d\_X(p,q) < \delta\\)

**Theorem**

Let f be a continuous mapping of a compact metric space X into a metric space Y. Then f is uniformly continuous on X.

**Theorem** - Compactness is essential

Let E be a noncompact set in \\(R^1\\). Then:

1.  There exists a continuous function on E which is not bounded.
2.  There exists a continuous and bounded function on E which has no maximum.

If in addition E is bounded, then:

1.  There exists a continuous function on E which is not uniformly continuous.

**Theorem**

If f is a continuous mapping of a metric space X into a metric space Y, and if E is a connected subset of X, then f(E) is connected.

**Theorem** - Intermediate value theorem

Let f be a continuous real function on the interval [a,b]. If f(a) &lt; f(b), and if c is a number such that f(a) &lt; c f(b), then there exists a point \\(x \in (a,b)\\) such that \\(f(x) = c\\)


### Monotonic functions {#monotonic-functions}

**Theorem**

f(x+) and f(x-) exist at every point for monotonic functions. That is, monotonic functions have no discontinuities of the second kind.

**Theorem**

Let f be monotonic on (a,b). Then the set of points at which f is discontinuous is at most countable. (you can establish a 1-1 correspondence between E and a subset of the rational numbers)


## Differentiation {#differentiation}


### Mean value theorems {#mean-value-theorems}

**Theorem** - Generalised mean theorem

If f and g are continuous real functions on [a,b] which are differential in (a,b), then there is a point \\(x\in(a,b)\\) at which:

\\[
[f(b)-f(a)]g'(x) = [g(b)-g(a)]f'(x)
\\]

Since when defining \\(h(t) =[f(b)-f(a)]g(x) = [g(b)-g(a)]f(x)\\), \\(h(a) = h(b)\\).


### Continuity of derivatives {#continuity-of-derivatives}

**Theorem**

Suppose f is real differentiable function on [a,b] and suppose \\(f'(a) < \lambda < f'(b)\\), then there exists a point where \\(f'(x) = \lambda\\).

It also means f' does not have any simple discontinuities.


### Taylor's theorem {#taylor-s-theorem}

The error of a taylor expansion about \\(\alpha\\) up to the n-1th derivative at \\(\beta\\) is equal to:

\\[
R(\beta) = \frac{f^{(n)}(x)}{n!} (\beta - \alpha)^n
\\]

for some x between \\(\beta - \alpha\\)


## Riemann-Stieltjes Integral {#riemann-stieltjes-integral}

**Definition**

Let \\([a,b]\\) be a given interval. By a _partition_ P of [a,b], we mean a finite set of points \\(a=x\_0,x\_1,\ldots,x\_n=b\\), where \\(x\_i < x\_{i+1}\\).

Suppose f is a bounded real function defined on \\([a,b]\\). Corresponding to each partition, we put:

\\[
M\_i = \sup f(x), x\in [x\_{i-1},x\_i]
\\]
\\[
m\_i = \inf f(x), x\in [x\_{i-1},x\_i]
\\]

\\[
U(P,f) = \sum\_{i=1}^n M\_i \Delta x\_i
\\]

\\[
L(P,f) = \sum\_{i=1}^n m\_i \Delta x\_i
\\]

\\[
\overline{\int\_a^b} f \dd{x} = \inf U(P,f)
\\]

\\[
\underline{\int\_a^b} f \dd{x} = \sup L(P,f)
\\]

where inf and sup are taken over all partitions P of [a,b].

When the upper and lower integrals are equal, we say that f is Riemann-integrable on \\([a,b]\\), we write \\(f \in \mathcal{R}\\), where \\(\mathcal{R}\\) denotes the set of Riemann-integrable functions.

Let \\(\alpha\\) be a monotonically increasing function on [a,b]. Letting \\(\Delta\alpha\_i = \alpha(x\_i) - \alpha(x\_{i-1})\\). Replacing \\(x\\) with \\(\alpha\\), we get the Stieltjes integral.


### Refinement {#refinement}

**Definition**

A partition \\(P^\*\\) is a refinement of P if \\(P^\* \supset P\\). Given two partitions \\(P\_1\\) and \\(P\_2\\), \\(P^\*\\) is their common refinement if \\(P^\* = P\_1 \cup P\_2\\).

**Theorem**

\\[
L(P,f,\alpha) \leq L(P^\*,f,\alpha)
\\]

\\[
U(P^\*,f,\alpha) \leq U(P,f,\alpha)
\\]

**Theorem**

\\(f \in \mathcal{R}(\alpha)\\) on [a,b] iff for every \\(\epsilon > 0\\) there exists a partition P such that:

\\[
U(P,f,\alpha) - L(P,f,\alpha) < \epsilon
\\]

Additional properties:

1.  If the equation holds for some P and \\(\epsilon\\), then it holds (with the same \\(\epsilon\\)) for every refinement of P.
2.  If it holds for \\(P = \\{x\_0,\ldots,x\_n\\}\\), and if \\(s\_i,t\_i\\) are arbitrary points in \\([x\_{i-1},x\_i]\\), then:

\\[
\sum\_{i=1}^n \vert f(s\_i) - f(t\_i) \vert \Delta \alpha\_i < \epsilon
\\]

1.  If \\(f \in \mathcal{R}(\alpha)\\) and the hypotheses of 2. hold, then:

\\[
\left\vert \sum\_{i=1}^n f(t\_i)\Delta\alpha\_i - \int\_a^b f\dd{\alpha} \right\vert < \epsilon
\\]

**Theorem**

If f is continuous on \\([a,b]\\), then \\(f \in \mathcal{R}(\alpha)\\) on [a,b].

**Theorem**

If f is monotonic on [a,b], and if \\(\alpha\\) is continuous on [a,b], then \\(f \in \mathcal{R}(\alpha)\\).

**Theorem**

If f is bounded on [a,b], f has only finitely many points of discontinuity on [a,b], and \\(\alpha\\) is continuous at every point at which f is discontinuous. Then \\(f \in \mathcal{R}(\alpha)\\).


## Sequences and series of functions {#sequences-and-series-of-functions}


### Uniform convergence {#uniform-convergence}

A sequence of functions \\(\\{f\_n\\}\\) converges uniformly on E to a function f if for every \\(\epsilon > 0\\), there is an integer N such that \\(n \geq N\\) implies:

\\[
\vert f\_n(x) - f(x) \vert \leq \epsilon
\\]

for all \\(x \in E\\).

Whereas if the sequence converges pointwise on E, there is an N depending on \\(\epsilon\\) and \\(x\\) such that epsilon-delta holds. If it converges uniformly on E, there is an N that will do for all \\(x \in E\\).

**Theorem** - Cauchy criterion

The sequence of functions \\(\\{f\_n\\}\\) definde on E converges uniform;y on E iff for every \\(\epsilon > 0\\) there exists an integer N such that \\(m,n \geq N\\), \\(x \in E\\) implies:

\\[
\vert f\_n(x) - f\_m(x) \vert \leq \epsilon
\\]

**Theorem**

Suppose \\(f\_n(x) \to f(x)\\). Let:

\\[
M\_n = \sup\_{x\in E}\vert f\_n(x) - f(x) \vert
\\]

Then \\(f\_n \to f\\) uniformly on E iff \\(M\_n \to 0\\) as \\(n \to \infty\\).

**Theorem** - Weierstrass

Suppose \\(\\{f\_n\\}\\) is a sequence of functions defined on E, and suppose:

\\[
\vert f\_n(x) \vert \leq M\_n
\\]

for all x and n.

Then \\(\sum f\_n\\) converges uniformly on E if \\(\sum M\_n\\) converges.

Note that the converse is not true.

**Theorem**

Suppose \\(f\_n \to f\\) uniformly on a set E in a metric space. Let \\(x\\) be a limit point of \\(E\\) and suppose that:

\\[
\lim\_{t\to x}f\_n(t) = A\_n
\\]

Then \\(\\{A\_n\\}\\) converges, and:

\\[
\lim\_{t\to x}f(t) = \lim\_{n\to\infty}A\_n$
\\]

That is to say:

\\[
\lim\_{t\to x} \lim\_{n\to\infty} f\_n(t) = \lim\_{n\to\infty}\lim\_{t\to x}f\_n(t)
\\]

**Theorem**

If \\(\\{f\_n\\}\\) is a sequence of continuous functions on E, and if \\(f\_n \to f\\) uniformly on E, then if f is continuous on E.

**Theorem**

Suppose K is compact,

1.  \\(\\{f\_n\\}\\) is a sequence of continuous functions on K
2.  \\(\\{f\_n\\}\\) converges pointwise to a continuous function f on K.
3.  \\(\\{f\_n\\}\\) is a monotonically decreasing sequence.

Then \\(f\_n \to f\\) uniformly on K.

**Definition**

If X is a metric space, \\(\mathcal{C}(X)\\) denotes the set of all complex-valued, continuous, bounded functions with domain X.

A supremum norm metric makes it into a metric space.


### Integration {#integration}

**Theorem**

If \\(f\_n \to f\\) uniformly.

\\[
\int\_a^b f \dd{\alpha} = \lim\_{n\to\infty}\int\_a^b f\_n \dd{\alpha}
\\]

if f is a series, then this implies we can integrate term by term if it converges uniformly on the closed integration interval.


### Differentiation {#differentiation}

**Theorem**

On a closed interval, if \\(\\{f'\_n\\}\\) converges uniformly, then \\(\\{f\_n\\}\\) converges uniformly and:

\\[
f'(x) = \lim\_{n\to\infty}f'\_n(x)
\\].


### Equicontinuity {#equicontinuity}


#### Motivating examples {#motivating-examples}

1.  If a sequence of functions are pointwise bounded on \\(E\\) and \\(E\_1\\) is a countable subset of \\(E\\), it is always possible to find a subsequence such that the sequence converges for all \\(x\inE\_1\\).
2.  But even if a sequence of continuous functions are uniformly bounded on a compact set \\(E\\), there need not exist a subsequence that converges pointwise on \\(E\\).
3.  Every convergent sequence need not contain a uniformly convergent subsequence.


#### Equicontinuity {#equicontinuity}

**Definition**

A familly of complex functions is said to be **equicontinuous** on E if for every \\(\epsilon > 0, \exists \delta > 0\\) such that:

\\[
\vert f(x) - f(y) \vert < \epsilon
\\]

whenevery \\(d(x,y) < \delta, \forall x,y\\).

**Theorem**

If \\(\\{f\_n\\}\\) is a pointwise bounded sequence of complex functions on a countable set \\(E\\), then \\(\\{f\_n\\}\\) has a subsequence that converges for every \\(x \in E\\).

**Theorem**

If \\(K\\) is a compact metric space, \\(f\_n \in \mathcal{C}(K)\\) and \\(\\{f\_n\\}\\) converges uniformly on \\(K\\), then \\(\\{f\_n\\}\\) is equicontinuous on K.

**Theorem**

If \\(K\\) is compact, \\(f\_n \in \mathcal{C}(K)\\) and \\(\\{f\_n\\}\\) is pointwise bounded and equicontinuous,

1.  \\(\\{f\_n\\}\\) is uniformly bounded on \\(K\\). (all \\(f\_i\\) are bounded by a single \\(M\\))
2.  \\(\\{f\_n\\}\\) contains a uniformly convergent subsequence.


### Stone-Weierstrass theorem {#stone-weierstrass-theorem}

**Theorem (Weierstrass theorem)**

If \\(f\\) is a continuous complex function on \\([a,b]\\), there exists a sequence of polynomials \\(P\_n\\) such that \\(\lim\_{n\to\infty} P\_n(x) = f(x)\\) uniformly on [a,b].

**Corollary**

For every interval \\([-a,a]\\) there is a sequence of real polynomials \\(P\_n\\) such that \\(P\_n(0) = 0\\) and such that \\(\lim\_{n\to\infty}P\_n(x) = |x|\\) uniformly on \\([-a,a]\\).


#### Algebras {#algebras}

**Definition**

A family of complex functions defined on a set is said to be an **algebra** if it is clsoed under addition, muilitplication and scalar multiplication. Its **uniform closure** is the set of all functions which are the limits of uniformly convergent sequences of members of that algebra. An algebra is **uniformly closed** if \\(f \in \mathcal{A}\\) whenever \\(f\_n \in \mathcal{A}\\) and they converge uniformly.

For example, the set of all polynomials is an algebra, and the Weierstrass theorem says that the set of all continuous functions is the uniform closure of the set of polynomials on [a,b].

**Theorem**

A uniform closure of an algebra of bounded functions is a uniformly closed algebra.

**Definition**

A family of functions \\(\mathcal{A}\\) on a set \\(E\\) is said to **seperate points** on \\(E\\) if to every pair of distinct points \\(x\_1,x2 \in E\\), there corresponds a function \\(f \in \mathcal{A}\\) such that \\(f(x\_1) \neq f(x\_2)\\). If to each \\(x \in E\\) there corresponds a function in \\(\mathcal{A}\\) which does not vanish at \\(x\\), we say **\\(\mathcal{A}\\) vanishes at no point of \\(E\\)**.

**Theorem**

If an algebra of functions seperates points on and vanishes at no point of a set, then it contains a function such that \\(f(x\_1) = c\_1\\) and \\(f(x\_2) = c\_2\\).

**Theorem (Stone's extension)**

Let \\(\mathcal{A}\\) be an algebra of real continuous functions on a compact set \\(K\\). If \\(\mathcal{A}\\) seperates points on \\(K\\) and if \\(\mathcal{A}\\) vanishes at no point of \\(K\\), then the uniform closure of \\(\mathcal{A}\\) consists of all real continous functions on \\(K\\).

Note: The conclusion of this theorem holds for complex algebra only if the algebra is self-adjoint (it contains its complex conjugates).

**Theorem**

Let \\(\mathcal{A}\\) be a self-adjoint algebra of complex continuous functions on a compact set \\(K\\). If \\(\mathcal{A}\\) seperates points on \\(K\\) and if \\(\mathcal{A}\\) vanishes at no point of \\(K\\), then the uniform closure of \\(\mathcal{A}\\) consists of all complex continous functions on \\(K\\), i.e. \\(\mathcal{A}\\) is dense \\(\mathcal{C}(K)\\).


## Special functions {#special-functions}


### Power series {#power-series}

Power series converge uniformly on a closed interval within the radius of convergence.

**Theorem (Abel's theorem)**

\\[
\lim\_{x\to 1} \sum\_{n=0}^\infty c\_n x^n = \sum\_{n=0}^\infty c\_n
\\]

**Theorem**

Given a double sequence \\(\\{a\_{ij}\\}\\), suppose \\(\sum\_{j=1}^\infty |a\_{ij}| = b\_i\\) and \\(\sum b\_i\\) converges. Then double summations of \\(a\_{ij}\\) can be reversed.

**Theorem**

Let \\(E\\) be the set of all \\(x \in S\\) at which:

\\[
\sum^\infty\_{n=0} a\_n x^n = \sum\_{n=0}^\infty b\_n x^n
\\]

if \\(E\\) has a limit point in S, then \\(a\_n = b\_n\\).


## Multivariate functions {#multivariate-functions}

**Theorem**

A linear operator on a vector space is one-to-one iff its range is all of that vector space.

**Theorem**

Let \\(\Omega\\) be the set of all invertible linear operators on \\(R^n\\).

1.  If \\(A \in \Omega, B \in L(R^n)\\) and:

\\[
\norm{B - A}\cdot \norm{A^{-1}} < 1
\\]

then \\(B \in \Omega\\).

2.\\(\Omega\\) is an open subset of \\(L(R^n)\\) and the mapping \\(A \to A^{-1}\\) is continuous on \\(\Omega\\).


### Differentiation {#differentiation}

**Theorem**

Suppose \\(\bm{f}\\) maps a convex open set \\(E \subset R^n\\) into \\(R^m\\), \\(\bm{f}\\) is differentiable in \\(E\\), and there is a real number \\(M\\) such that:

\\[
\norm{\bm{f}'(\bm{x})} \leq M
\\]

for every \\(\bm{X} \in E\\). Then:

\\[
\vert \bm{f(b) - f(a)} \vert \leq  M \vert \bm{b - a} \vert
\\]

for all \\(a,b \in E\\).

**Corollary**

If \\(\bm{f'(x) = 0}\\) for all \\(x \in E\\), then \\(\bm{f}\\) is constant.

**Definition**

A differentiable mapping \\(\bm{f}\\) of an open set \\(E \subset R^n\\) into \\(R^m\\) is said to be **continuously differentiable** in \\(E\\) if \\(\bm{f'}\\) is a continuous mapping of \\(E\\) into \\(L(R^n,R^m)\\).

We also say that \\(\bm{f} \in \mathcal{C}'(E)\\) or it is a $\mathcal{C}'$-mapping.

**Theorem**

Suppose \\(\bm{f}\\) maps an open set \\(E \subset R^n\\) into \\(R^m\\). Then \\(\bm{f}\in\mathcal{C}'(E)\\) iff all the partial derivatives of \\(f\\) exist and are continuous on \\(E\\).


### Contraction {#contraction}

**Definition**

Let \\(X\\) be a metric space. If \\(\phi\\) maps \\(X \to X\\), and if there is a number \\(c < 1\\), such that:

\\[
d(\phi(x),\phi(y)) \leq c d(x,y)
\\]

for all \\(x,y\in X\\), then \\(\phi\\) is a a contraction of \\(X\\) into \\(X\\).

**Theorem**

If \\(X\\) is a complete metric space, then there exists only one \\(x \in X\\) such that \\(\phi(x) = x\\)


### Inverse function theorem {#inverse-function-theorem}

**Theorem**

Suppose \\(\bm{f}\\) is a \\(\mathcal{C}'\\) -mapping of an open set \\(E \subset R^n \to R^n\\), \\(\bm{f'(a)}\\) is invertible for some \\(\bm{a} \in E\\) and \\(\bm{b = f(a)}\\). Then:

1.  There exists open sets \\(U,V \subset R^n\\) such that \\(\bm{a} \in U, \bm{b} \in V\\), \\(\bm{f}\\) is one-to-one on \\(U\\), and \\(f(U) = V\\).
2.  If \\(\bm{g}\\) is the inverse of \\(\bm{f}\\) (which exists by (1)), defined in \\(V\\), then \\(\bm{g} \in \mathcal{C}'(V)\\)

As a consequence of (1),

**Theorem**

IF \\(\bm{f}\\) is a \\(\mathcal{C}'\\) -mapping of an open set \\(E \subset R^n \to R^n\\), \\(\bm{f'(a)}\\) is invertible for some \\(\bm{a} \in E\\), then \\(\bm{f}(W)\\) is an open subset of \\(R^n\\) for every open set \\(W \subset E\\). i.e. \\(\bm{f}\\) is an open mapping of \\(E\\) into \\(R^n\\).


### Implicit function theorem {#implicit-function-theorem}

**Theorem**

Let \\(\bm{f}\\) be a \\(\mathcal{C}'\\) -mapping of \\(E \subset R^n \to R^m\\), such that \\(\bm{f(a,b)}\\) vanishes for some point \\(\bm{(a,b)} \in E\\). Put \\(A = \bm{f'(a,b)}\\) and assume \\(A\_x\\) is invertible. Then there exists open sets \\(U \subset R^{n+m}\\) and \\(W \subset R^m\\) with the property, To every \\(\bm{y}\in W\\), corresponds a unique \\(\bm{x}\\) such that \\(\bm{f}(\bm{x,y})\\) vanishes. If this \\(\bm{x}\\) is defined to be \\(\bm{g(y)}\\), \\(\bm{g'(b)} = -(A\_x)^{-1}A\_y\\).


### Rank theorem {#rank-theorem}

**Theorem**

Suppose \\(m,n,r\\) are nonnegative integers, \\(m,n \geq r\\),\\(\bm{F}\\) is a \\(\mathcal{C}'\\) -mapping of an open set \\(E \subset R^n \to R^m\\), and \\(\bm{F'(x)}\\) has rank \\(r\\) for every for every \\(\bm{x}\in E\\). Fix \\(\bm{a}\in E\\), put \\(A = \bm{F'(a)}\\), and let \\(Y\_1\\) be the range of \\(A\\), and let \\(P\\) be a projection in \\(R^m\\) whose range is \\(Y\_1\\). Let \\(Y\_2\\) be the null space of \\(P\\).
Then there are open sets \\(U,V \in R^n\\), with \\(\bm{a} \in U \subset E\\) and there is a 1-1 $\mathcal{C}'$-mapping \\(\bm{H}\\) of \\(V\\) onto \\(U\\), (whose inverse is also of class \\(\mathcal{C}'\\)) such that:

\\[
\bm{F(H(x))} = A\bm{x} + \phi(Ax)
\\]

for all \\(x\in V\\), where \\(\phi\\) is a \\(\mathcal{C}'\\) - mapping of the open set \\(A(V) \subset Y\_1\\) into \\(Y\_2\\).

**Theorem**

When \\(f \in \mathcal{C}''(E)\\)

\\[
D\_{21} f = D\_{12} f
\\]


### Differentiation of Integrals {#differentiation-of-integrals}

**Theorem**

To insert an derivative into an integral, note that the integrand has to continuous wrt the differentiation variable.


## Integration of differential forms {#integration-of-differential-forms}

**Theorem**

For every \\(f\in\mathcal{C}(I\_k)\\), \\(L(f) = L'(f)\\).

**Definition**

The support of a complex function on \\(R^k\\) is the closure of the set of all points \\(\bm{x} \in R^k\\) at which \\(f(\bm{x})\neq 0\\).


### Primitive mappings {#primitive-mappings}

**Definition**

If \\(\bm{G}\\) maps on a open set \\(E \subset R^n \to R^n\\), and if there is an integer \\(m\\) and a real function \\(g\\) with domain \\(E\\) such that \\(G(x) = \sum\_{i\neq m} x\_i \bm{e}\_i + g(\bm{x})\bm{e}\_m\\), then \\(\bm{G}\\) is primitive. (i.e. it changes at most one coordinate)

The jacobian of \\(\bm{G}\\) at \\(\bm{a}\\) is given by \\(J\_{\bm{G}} (\bm{a}) = \det \bm{G}'(\bm{a}) = (D\_m g)(\bm{a})\\).

**Definition**

A linear operator that interchanges some members of the standard basis is called a **flip**.

**Theorem**

Suppose \\(\bm{F}\\) is a \\(\mathcal{C}'\\) mapping of an open set \\(\E \subset R^n \to R^n\\), \\(\bm{0} \in E\\), \\(\bm{F(0)=0}\\), and \\(\bm{F'(0)}\\) is invertible. Then there is a neighbourhood of \\(\bm{0}\\) in \\(R^n\\) in which a representation:

\\[
\bm{F(x)} = B\_1\ldots B\_{n-1} G\_n \circ\ldots\circ G\_1 (x)
\\]

is valid.

Each \\(\bm{G}\_i\\) is a primitive \\(\mathcal{C}'\\) is a primitive \\(\mathcal{C}'\\) -mapping in some neighborhood of \\(\bm{0}\\) ; \\(\bm{G\_i(0)=0}\\), \\(\bm{G\_i'(0)}\\) is invertible and each \\(B\_i\\) is either a flip or identity operator.


### Partitions of unity {#partitions-of-unity}

**Theorem**

Suppose \\(K\\) is a compact subset of \\(R^n\\) and \\(\\{V\_\alpha\\}\\) is an open cover of \\(K\\). Then there exists functions \\(\psi\_1,\ldots,\psi\_s \in \mathcal{C}'(R^n)\\) such that:

1.  \\(0 \leq \psi\_i \leq 1\\)
2.  each \\(\psi\_i\\) has its support in some \\(V\_\alpha\\), and
3.  \\(\sum\_i \psi\_i(\bm{x}) = 1\\) for every \\(\bm{x} \in K\\)

Thus, \\(\\{\psi\_i\\}\\) is called a **parition of unity** and (b) is expressed by saying that \\(\\{\psi\_i\\}\\) is **subordinate** to the cover \\(\\{V\_\alpha\\}\\).


### Differential forms {#differential-forms}

**Definition**

To say that \\(\bm{f}\\) is a \\(\mathcal{C}'\\) -mapping of a compact set \\(D \subset R^k\\) into \\(R^n\\) means that there is a \\(\mathcal{C}'\\) mapping \\(g\\) of an open set \\(W \subset R^k, D\subset W\\) into \\(R^n\\) such that \\(\bm{g(x)= f(x)}\\) for all \\(\bm{x} \in D\\).

**Definition**

Suppose \\(E\\) is an open set in \\(R^n\\). A **k-surface** in \\(E\\) is a \\(\mathcal{C}'\\) mapping \\(\Phi\\) from a compact set \\(D \subset R^k\\) into \\(E\\).  \\(D\\) is called the **parameter domain** of \\(\Phi\\). (Points of \\(D\\) will be denoted by \\(\bm{u}\\)).

For example, 1-surfaces are the same as continuously differentiable curves.

**Definition**

Suppose \\(E\\) is an open set in \\(R^n\\). A differential form of order \\(k \geq 1\\) in \\(E\\) (a k-form in E) is a function \\(\omega\\):

\\[
\omega = \sum a\_{i\_1 \ldots i\_k}(\bm{x}) \dd{x\_{i\_1}} \wedge \ldots \wedge \dd{x\_{i\_k}}
\\]

which assigns to each k-surface \\(\phi\\) in E a number \\(\omega(\Phi) = \int\_\Phi \omega\\), according to the rule:

\\[
\int\_\Phi \omega = \int\_D \sum a\_{i\_1 \ldots i\_k}(\Phi(\bm{u})) \frac{\partial(x\_i\_1,\ldots,x\_i\_k)}{\partial(u\_1,\ldots,u\_k)}  \dd{\bm{u}}
\\]


#### Examples {#examples}

A k-form is said to be of class \\(\mathcal{C}'\\) or \\(\mathcal{C}''\\) if the functions \\(a\_{i\_k\ldots i\_k}\\) are all of class \\(\mathcal{C}'\\) or \\(\mathcal{C}''\\).

A 0-form in \\(E\\) is defined to be continuous function in \\(E\\).

Integrals of 1-forms are called line integrals.


#### Standard presentation {#standard-presentation}

\\[
\omega = \sum\_j b\_{I}(\bm{x}) \dd{x\_I}
\\]

where the \\(I\\) is a set of increasing k-indices.

**Theorem**

If \\(\omega = 0\\) in \\(E\\), then \\(b\_{I}(\bm{x}) = 0\\) for every increasing k-inex \\(I\\) for every \\(\bm{x} \in E\\)


#### Product of forms {#product-of-forms}

\\[
\dd{x\_I} \wedge \dd{X\_J} = (-1)^\alpha \dd{x\_{[I,J]}}
\\]

where \\(\alpha\\) is the number of differences \\(j\_t - i\_s\\) that are _negative_.

**Theorem**

1.  If \\(\omega\\) and \\(\lambda\\) are k- and m- forms respectively, of class \\(\mathcal{C}'\\) in E, then:

\\[
d(\omega \wedge \lambda) = \dd{\omega} \wedge \lambda + (-1)^k \omega \wedge \dd{\lambda}
\\]


#### Change of variables {#change-of-variables}

Suppose \\(E\\) is an open set in \\(R^n\\), T is an \\(\mathcal{C}'\\) mapping of E into an open set \\(V \subset R^m\\), and \\(\omega\\) is a k-form in \\(V\\), whose standard presentation is:

\\[
\omega = \sum\_I b\_I(y) \dd{y}\_I
\\]
Let \\(t\_1,\ldots,t\_m\\) be the components of \\(T\\); If:

\\[
\bm{y} = (y\_1,\ldots,y\_m) = T(\bm{x})
\\]

then \\(y\_i = t\_i(\bm{x})\\).

\\[
\dd{t\_i} = \sum\_{j=1}^n (D\_j t\_i)(\bm{x})\dd{x\_j}
\\]

Thus each \\(\dd{t\_i}\\) is a 1-form in \\(E\\).

The mapping \\(T\\) transforms \\(\omega\\) into a k-form \\(\omega\_T\\) in \\(E\\), whose definition is:

\\[
\omega\_T = \sum\_I b\_I(T(\bm{x})) \dd{t\_{i\_1}} \wedge \ldots\wedge \dd{t\_{i\_k}}
\\]

**Theorem**

Let \\(\omega,\lambda\\) be k- and m-forms respectively.

1.  \\((\omega + \lambda)\_T = \omega\_T + \lambda\_T\\) if \\(k=m\\)
2.  \\((\omega \wedge \lambda)\_T = \omega\_T \wedge \lambda\_T\\)
3.  \\(\dd{\omega\_T} = (\dd{\omega})\_T\\) if \\(\omega\\) is of class \\(\mathcal{C}'\\) and \\(T\\) is of class \\(\mathcal{C}''\\).

**Theorem**

Suppose \\(\omega\\) is a k-form in an open set \\(E \subset R^n\\), \\(\Phi\\) is a k-surface in \\(E\\), with parameter domain \\(D \subset R^k\\), and \\(\Delta\\) is the k-surface in \\(R^k\\), with paramter domain \\(D\\), definde by \\(\Delta(\bm{u}) = \bm{u}(u\in D)\\). Then:

\\[
\int\_\Phi \omega = \int\_\Delta \omega\_\Phi
\\]

Proof by using jacobian.

**Theorem**

Suppose \\(T\\) is a \\(\mathcal{C}'\\) mapping of an open set \\(E \subset R^n\\) into an open set \\(V \subset R^m\\), \\(\Phi\\) is a k-surface in \\(E\\), and \\(\omega\\) is a k-form in \\(V\\). Then:

\\[
\int\_{T\Phi} \omega = \int\_\Phi \omega\_T
\\]

Proof by using the previous theorems


#### Simplex and chains {#simplex-and-chains}

**Definition (Affine simplexes)**

A mapping \\(\bm{f}\\) that carries a vector space \\(X\\) into a vector space \\(Y\\) is said to be **affine** if \\(\bm{f} - \bm{f(0)}\\) is linear. i.e.

\\[
\bm{f(x) = f(0)} + A \bm{x}
\\]

for some \\(A \in L(X,Y)\\).

We define the **standard simplex** \\(Q^k\\) to be the set of all \\(\bm{u} \in R^k\\) of the form:

\\[
\bm{u} = \sum\_{i=1}^k \alpha\_i \bm{e}\_i
\\]

such that \\(\alpha\_i \geq 0\\) and \\(\sum\alpha\_i \leq 1\\).

The **oriented affine k-simplex**:

\\[
\sigma = [\bm{p\_0,p\_1,\ldots,p\_k}]
\\]

is defined to be the k-surface in \\(R^n\\) with parameter domain \\(Q^k\\) which is given by t