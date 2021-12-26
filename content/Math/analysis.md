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

Then \\(\sum a\_n b\_n\\).

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