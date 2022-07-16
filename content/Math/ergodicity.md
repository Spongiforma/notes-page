+++
title = "Analysis"
author = ["root"]
draft = false
+++

## Measure theory {#measure-theory}

<div class="defn">

A **measure-preserving transformation** is a measurable transformation \\(T\\) such that \\(m\_1(T^{-1}(B\_2)) = m\_2(B\_2)\\) for all \\(B\_2 \in \mathcal{B}\_2\\).

</div>


## Ergodic hypotheses {#ergodic-hypotheses}

1.  A measure-preserving system \\((X,\mathcal{B},m ,T)\\) is called **ergodic** if \\(T^{-1}(B) =B\\) implies that \\(m(B) = 0\\) or \\(m(B) = 1\\).
2.  \\(T\\) is an ergodic transformation iff every \\(T\\) invariant function is constant almost everywhere.


### Birkhoff equality {#birkhoff-equality}

<div class="thrm">

If \\(T\\) is a measure-preserving transformation on a probability space \\((X,\mathcal{B},m)\\), then for any \\(f \in L^1(X)\\), the time average of \\(f\\) converges almost everywhere to a function \\(f^\* \in L^1\\). Furthermore, \\(f^\*\\) is \\(T\\) invariant almost everywhere and \\(\int\_X f^\* \dd{m} = \int\_X f \dd{m}\\).

</div>

Thus, \\(T\\) is ergodic iff the time average converges to the space average almost everywhere.


## Alternate properties {#alternate-properties}

Consider the irrational rotations of a circle, which don't mix up a set but merely translate it. Irrational rotations are ergodic because we can expect that the intersection of \\(T^{-n}(A)\\) and B should overlap with measure \\(\mu(A)\mu(B)\\) for random \\(n\\). But since irrational rotations dense, there will be cases where the sets overlap almost completely or don't intersect at all. How may we characterise transformations which "scatter" a set uniformly?


### Strong-mixing {#strong-mixing}

<div class="defn">

A measure-preserving system \\((X,\mathcal{B}, m , T)\\) is **strong-mixing** if for all \\(A,B \in \mathcal{B}\\), we have that
\\[
\lim\_{n\to\infty} m(T^{-n}(A) \cap B) = m(A)m(B)
\\]

</div>

<div class="defn">

A measure-preserving system \\((X,\mathcal{B}, m , T)\\) is **weak-mixing** if for all \\(A,B \in \mathcal{B}\\), we have that

\\[
\lim\_{n\to\infty}  \frac{1}{n} \sum\_{i=0}^{n-1} |
m(T^{-i}(A) \cap B) - m(A)m(B)| = 0
\\]

</div>

For comparison, a transformation is ergodic iff for any \\(A,B \in \mathcal{B}\\), we have that

\\[
\lim\_{n\to\infty} \frac{1}{n} \sum\_{i=0}^{n-1} m(T^{-i}(A) \cap B) = m(A)m(B).
\\]


## Major results in Poincare recurrence {#major-results-in-poincare-recurrence}