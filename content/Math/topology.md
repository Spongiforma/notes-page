+++
title = "Topology"
author = ["root"]
draft = false
+++

## Set theory {#set-theory}


### Inverse functions {#inverse-functions}

If f : A -> B,

\\[
f^{-1}(B\_0) = \\{a \vert f(a) \in B\_0\\}
\\]


### Relations {#relations}


#### Equivalence relations {#equivalence-relations}

If there is a equivalence relation C on A it has the following properties,

1.  Reflexivity: xCx for every x in A.
2.  Symmetry: if xCy, then yCx.
3.  Transitivity: if xCy and yCz, then xCz.

A **equivalence class** determined by x is given by:

\\[
E = \\{y \vert y \sim x\\}
\\]

**Lemma**: Two equivalence classes E and E' are either disjoint or equal.

**Partition**: Collection of disjoint nonempty subsets of A whose union is all of A.

Note that given any partition of A, there is exactly one equivalence relation from which it is derived.

**Example**: Define two points in the plane to be equivalent is they lie at the same distance from the origin. Then it is a equivalence relation and the collection of equivalence classes consists of all circles centered at the origin, along with the origin alone.


#### Order relation {#order-relation}

1.  (Comparability) For every x and y in A for which x != y, either xCy or yCx.
2.  (Nonreflexivity) For no x in A does the relation xCx hold.
3.  (Transitivity) If xCy and yCz, then xCz.

(a,b) is then the set {x | a < x < b}, which is an open interval. If the set is empty, a (b) is the immediate predecessor (sucessor) of b (a).

**Order type**: A and B have the same order type if there is a bijective correspondence between them that preserves order.

**Dictionary order**: A "lexicographic" order relation for cartesian products.

**Least upper bound property**: An ordered set A has the lub property if every nonempty subset A\_0 of A that is bounded above has a least upper bound. The greatest lowerbound property is defined similarly.


#### Size of set {#size-of-set}

1.  A is finite if \\(A \sim J\_n\\) for some n, where \\(J\_n\\) is the set whose elements are the integers 1 to n.
2.  A is infinite if A is not finite/ A is equivalent to one of its proper subsets.
3.  A is countable if \\(A \sim J\\)
4.  A is uncountable if A is neither finite nor countable
5.  A is at most countable if A is finite or countable

**Corollaries**:

-   Set of all integers is countable

**Proof**: The set of all integers is countable as we can set up a 1-1 correspondence: \\(f(n) = n/2\\) when n is even, and \\(f(n) = - (n-1)/2\\) when n is odd.

-   Every infinite subset of a countable set A is countable

-   The union of a sequence of countable sets is countable: Cantor diagonalisation

-   If \\(A\\) is a countable set, and \\(B\_n\\) is the set of all n-tuples \\((a\_1,\ldots,a\_n)\\), where \\(a\_k \in A (k = 1,\ldots,n)\\) and the elements \\(a\_1, \ldots, a\_n\\) need not be distinct. Then \\(B\_n\\) is countable

**Theorem**

The set of all sequences whose elements are the digits 0 and 1 is uncountable.


### Metric Spaces {#metric-spaces}

A set X, whose elements we shall call points, is said to be a metric space if any two points p,q of X there is associated a real number d(p,q), such that

1.  \\(d(p,q) > 0\\), if \\(p \neq q\\); \\(d(p,p) = 0\\);
2.  \\(d(p,q) = d(q,p)\\)
3.  \\(d(p,q) \leq d(p,r) + d(r,q)\\) for any \\(r \in X\\)

Any function with these properties is called a **distance function** or **metric**.

**Definition**

If  \\(a\_i < b\_i\\) for all i, then the set of points in euclidean space that satisfies the inequality \\(a\_i \leq x\_i \leq b\_i\\) for all i is called a **k-cell**.

If \\(x \in R^k\\) and \\(r > 0\\), the **open** or **closed ball** B, with center at x and radius r is defined to be the set of all \\(y \in R^k\\) such that \\(\vert y - x \vert < r\\) or likewise for closed balls.

A set \\(E \subset R^k\\) is **convex** if \\(\lambda \bm{x} + (1-\lambda)\bm{y} \in E\\), where \\(\bm{x},\bm{y} \in E\\) and \\(0 < \lambda < 1\\).

**Definition**

1.  A **neighbourhood** of p is a set \\(N\_r(p)\\) consisting of all q such that \\(d(p,q) < r\\), for some \\(r > 0\\). r is the **radius** of \\(N\_r(p)\\).
2.  A point p is a **limit point** of the set E if _every_ neighbourhood of p contains a point \\(q \neq p\\) such that \\(q \in E\\).
3.  If \\(p \in E\\) and p is not a limit point of E, then p is called an **isolated point** of E.
4.  E is **closed** if every limit point of E is a point of E.
5.  A point p is an **interior** point of E if there is a neighbourhood N of p such that \\(N \subset E\\).
6.  E is **open** if every point of E is an interior point of E.
7.  The **complement** of E (denoted by \\(E^c\\)) is the set of all points \\(p \in X\\) such that \\(p \notin E\\)
8.  E is **perfect** if E is closed and every point of E is a limit point of E. i.e. a point is a limit point of E iff \\(p \in E\\).
9.  E is **bounded** if there is a real number M and a point \\(q \in X\\) such that \\(d(p,q) < M \forall p \in E\\).
10. E is **dense** in X if every point of X is a limit point of E, or a point of E or both.

**Theorem**

Every neighbourhood is an open set.

**Theorem**

If p is a limit point of a set E, then every neighbourhood of p contains infinitely many point of E.

**Corollary**

A finite point set has no limit points.

{{< figure src="/static/flopen.png" >}}

**Theorem**

Let \\(\left{E\_\alpha \right}\\) be a collection of sets. Then

\\[
\left(\bigcup\_\alpha E\_\alpha \right)^c = \bigcap\_\alpha (E\_\alpha^c)
\\]

**Theorem**

A set is open iff its complement is closed

A set F is closed iff its complement is open.

**Theorem**

1.  For any collection of open sets, \\(\\{G\_\alpha\\}\\), \\(\cup\_\alpha G\_\alpha\\) is open.
2.  For any collection of closed sets, \\(\\{F\_\alpha\\}\\), \\(\cap\_\alpha G\_\alpha\\) is closed.
3.  For any finite collection of open sets, \\(\cap\_i G\_i\\) is open.
4.  For any finite collection of closed sets, \\(\cup\_i F\_i\\) is closed.

**Definition**

If X is a metric space, E is a subset of X and if E' is the set of limit points of E in X, then the **closure** of E is the set \\(\bar{E} = E \cup E'\\).
in
**Theorem**

1.  \\(\bar{E}\\) is closed.
2.  \\(E = \bar{E}\\) iff E is closed.
3.  \\(\bar{E} \subset F\\) for every closed set \\(F \subset X\\) such that \\(E \subset F\\).

**Theorem**
Let E be a nonempty set of real numbers which is bounded above. Let \\(y = \sup E\\), then \\(y \in \bar{E}\\). Hence, \\(y \in E\\) if E is closed.

**Theorem**

Suppose \\(Y \subset X\\). A subset E of Y is open relative to Y iff \\(E = Y \cap G\\) for some open subset G of X.

(???)


### Compact sets {#compact-sets}

**Definition**

An **open cover** of a set E in a metric space X, we mean a collection of open subsets of X such that \\(E \subset \cup\_\alpha G\_\alpha\\).

**Definition**

A subset K of of a metric space X is said to be **compact** if every open cover of K contains a subcover. i.e. if \\(\left\\{G\_\alpha \right\\}\\) is an open cover of K, then there are finitely many indices \\(\alpha\_1, \ldots, \alpha\_n\\), such that:

\\[
K \subset G\_{\alpha\_1} \cup \ldots \cup G\_{\alpha\_n}
\\]

**Theorem**

Suppose \\(K \subset Y \subset X\\). Then K is compact relative to X iff K is compact relative to Y.

**Theorem**

Compact subsets of metric spaces are closed.

**Theorem**

Closed subsets of compact sets are compact.
**Corollary**: If F is closed and K is compact, then \\(F \cap K\\) is compact.

**Theorem**

If \\(\\{K\_\alpha\\}\\) is a collection of compact subsets of a metric space X such that the intersection of every finite subcollection of \\(\\{\K\_alpha\\}\\) is non-empty, then \\(\cap K\_\alpha\\) is nonempty.
**Corollary**: If \\(\\{K\_n\\}\\) is a sequence of nonempty compact sets such that \\(K\_n \supset K\_{n+1}\\) then \\(\cap\_1^\infty K\_n\\) is not empty.

**Theorem**
If E is an infinite subset of a compact set K, then E has a limit point in K.

**Theorem**
If \\(\\{I\_n\\}\\) is a sequence of intervals in \\(R^1\\), such that \\(I\_n \supset I\_{n+1}\\) then \\(\cap^\infty\_1 I\_n\\) is not empty.

**Theorem**
If \\(\\{I\_n\\}\\) is sequence of k-cells such that \\(I\_n \superset I\_{n+1}\\), then \\(\cap^\infty\_1 I\_n\\) is not empty.

**Theorem**
Every k-cell is compact.

**Theorem**
If a set in \\(R^k\\) has one of the following three properties, it has the other two.

1.  E is closed and bounded
2.  E is compact
3.  Every infinite subset of E has a limit point in E.

    (b) and (c) are equivalent in any metric space but (a) does not in general imply (b) and (c).

**Theorem (Weierstrass)**

Every bounded infinite subset of \\(R^k\\) has a limit point in \\(R^k\\).


### Perfect sets {#perfect-sets}

**Theorem**

A nonempty perfect set in \\(R^k\\) is uncountable.


### Connected sets {#connected-sets}

Two subsets A,B of a metric space X are _seperated_ if \\(A \cap \bar{B}\\) and \\(\bar{A}\cap B\\) are empty. A subset of X is connected if it is not a union of two nonempty seperated sets.

**Theorem**

A subset E of the real line \\(R^1\\) is connected iff it has the following property: If \\(x,y \in E\\), \\(x < z < y\\), then \\(z \in E\\).