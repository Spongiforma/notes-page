+++
title = "Topology"
author = ["root"]
draft = false
+++

## Set theory {#set-theory}


### Inverse functions {#inverse-functions}

If f : A -&gt; B,

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

(a,b) is then the set {x | a &lt; x &lt; b}, which is an open interval. If the set is empty, a (b) is the immediate predecessor (sucessor) of b (a).

**Order type**: A and B have the same order type if there is a bijective correspondence between them that preserves order.

**Dictionary order**: A "lexicographic" order relation for cartesian products.

**Least upper bound property**: An ordered set A has the lub property if every nonempty subset A_0 of A that is bounded above has a least upper bound. The greatest lowerbound property is defined similarly.


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


## Topological spaces {#topological-spaces}

**Definition**

A topology on a set X is a collection \\(\mathcal{T}\\) of subsets of X having the following properties.

1.  \\(\emptyset\\) and X are in \\(\mathcal{T}\\)
2.  The union of the elements of any subcollection of \\(\mathcal{T}\\) is in \\(\mathcal{T}\\)
3.  The intersection of the elements of any finite subcollection of \\(\mathcal{T}\\) is in \\(\mathcal{T}\\)

If X is a topological space with topology \\(\mathcal{T}\\), we say that a subset U of X is an **open set** of X if U belongs to the collection \\(\mathcal{T}\\).

The collection of all subsets of X is called the **discrete topology**. The collection consisting of X and \\(\emptyset\\) only is the **indiscrete/trivial topology**.

Let \\(\mathcal{T}\_f\\) be the collection of all subsets U of X such that X-U either is at most countable or is all of X. Then \\(\mathcal{T}\_f\\) is the **finite complement topology**.

**Definition**

Suppose that \\(\mathcal{T}\\) and \\(\mathcal{T}'\\) are two topologies. If \\(\mathcal{T}' \supset \mathcal{T}\\), we say \\(\mathcal{T}'\\) is **finer** than \\(\mathcal{T}\\). If it proper contains \\(\mathcal{T}\\), we say strictly finer than \\(\mathcal{T}\\). The reverse is called coarser. \\(\mathcal{T}\\) is comparable with \\(\mathcal{T}'\\) if one is the subset of the other.


### Basis {#basis}

A **basis** for a topology on X is a collection \\(\mathcal{B}\\) of subsets of X (called **basis elements**) such that:

1.  For each \\(x \in X\\), there is at least one basis element B containing x. (B is a cover)
2.  If x belongs to the intersection of two basis elements \\(B\_1\\) and \\(B\_2\\), then there is a basis element \\(B\_3\\) containing x such that  \\(B\_3 \subset B\_1 \cap B\_2\\).

If \\(\mathcal{B}\\) satisfies these conditions, we define the topology generated by \\(\mathcal{B}\\) as: A subset U of X is said to be open in X if for each \\(x \in U\\), there is a basis element \\(B \in \mathcal{B}\\) such that \\(x \in B\\) and \\(B \subset U\\). Note each element is an element of \\(\mathcal{T}\\).

**Lemma**

\\(\mathcal{T}\\) equals the collection of all unions of elements of \\(\mathcal{B}\\).

**Lemma**

Let X be a topological space. Suppose that \\(\mathcal{C}\\) is a collection of open sets of X such that for each open set U of X and each x in U, there is an element \\(C\\) of \\(\mathcal{C}\\) such that \\(x \in C \subset U\\). Then \\(\mathcal{C}\\) is a basis for the topology of X. (C make up a cover and open set of X is a superset of some C).

_Proof._ We will show why every element in \\(\mathcal{T}\\) belongs in the topology generated by the basis, \\(\mathcal{T}'\\). Since for \\(x \in C \subset U\\), there exists a union of C which equals U. The converse follows from the previous lemma.

**Lemma (Fineness)**

Let \\(\mathcal{B}\\) and \\(\mathcal{B}'\\) be the bases for topologies \\(\mathcal{T}\\) and \\(\mathcal{T}'\\) respectively on X. Then the following are equivalent.

1.  \\(\mathcal{T}'\\) is finer than \\(\mathcal{T}\\)
2.  For each \\(x \in X\\), and each basis element \\(B \in \mathcal{B}\\) containing \\(x\\), there is a basis element \\(B' \in \mathcal{B}'\\) s.t. \\(x \in B' \subset B\\).


#### Common topologies {#common-topologies}

| Topology    | Basis               | Symbol              |
|-------------|---------------------|---------------------|
| Standard    | (a,b)               | \\(\mathbb{R}\\)    |
| Lower-limit | [a,b]               | \\(\mathbb{R}\_l\\) |
| K-topology  | (a,b) and (a,b) - K | \\(\mathbb{R}\_K\\) |

Note: K is the set of all numbers \\(1/n\\) for each positive integer n.

**Lemma**
Topologies of \\(\mathbb{R}\_l\\) and \\(\mathbb{R}\_K\\) are strictly finer than the standard topology on \\(\mathbb{R}\\), but are not comparable with one another.


#### Subbasis {#subbasis}

What if you extend the basis to also take finite intersections?

**Definition**

A subbasis \\(\mathcal{S}\\) for a topology on X is a collection of subsets of \\(X\\) whose union equals X. The topology generated by the subbasis is defined to be the collection \\(\mathcal{T}\\) of all unions of finite intersections of elements of \\(\mathcal{S}\\).


### Order topology {#order-topology}

**Definition**

Let \\(X\\) be a set with a simple order relation. The collection of all sets of the following types:

1.  All open intervals
2.  All intervals of the form \\([a\_0,b]\\) where \\(a\_0\\) is the smallest element if any
3.  All intervals of the form \\([a,b\_0]\\) where \\(b\_0\\) is the largest element if any

is the basis for the **order topology** on X.


### Product topology {#product-topology}

**Definition**

Let X and Y be topological spaces. The **product topology** on \\(X \times Y\\) is the topology having as basis the collection of all sets of the form \\(U \times V\\), where \\(U \in X, V \in Y\\).

**Theorem**

If \\(\mathcal{B}\\) is the basis for the topology of \\(X\\) and \\(\mathcal{C}\\) is a basis topology of Y, then the collection:

\\[
\mathcal{D} = \\{B \times C \vert B \in \mathcal{B}, C \in \mathcal{C}\\}
\\]

is a basis for the topology of \\(X \times Y\\).

We are also interested in a subbasis.

**Theorem**

\\[
\mathcal{S} = \\{\pi\_1^{-1}(U) \vert U \text{ open in } X \\} \cup \\{\pi\_2^{-1}(V) \vert V \text{ open in } Y \\}
\\]


### Subspace topology {#subspace-topology}

**Definition**

Let X be a topological space with topology \\(\mathcal{T}\\). If \\(Y \subset X\\),

\\[
\mathcal{T}\_Y = \\{Y \cap U \vert U \in \mathcal{T}\\}
\\]

is the **subspace topology** on \\(Y\\). Y is then a **subspace** of X,

**Lemma**

A basis can be derived in a similar form. (replace Y with B).

**Lemma**

If \\(U\\) is open in \\(Y\\) and \\(Y\\) is open in \\(X\\), then \\(U\\) is open in \\(X\\).


### Closed sets {#closed-sets}

Defining topological space with closed sets.

**Theorem**

In a topological space,

1.  the empty set and the whole set are closed
2.  Arbitrary intersections of closed sets are closed
3.  Finite unions of closed sets are closed


#### Closures {#closures}

**Theorem**

Let A be a subset of the topological space X.

1.  Then \\(x \in \bar{A}\\) iff every neighbourhood of x intersects A.
2.  If X is given by a basis, \\(x \in \bar{A}\\) iff every basis element containing x intersects A.


### Hausdorff spaces {#hausdorff-spaces}

Usually it is nicer to have one-point sets closed like in euclidean space, as this means that sequences don't converge to multiple values for instance.

**Definition**

A topological space X is a **Hausdorff space**, if for each pair of distinct points in X, there exist neighborhoods of each point that are disjoint.

**Theorem**

Every finite point set in a hausdorff space is closed.

The Hausdorff space condition is stronger than the condition that finite point sets be closed (\\(T\_1\\) axiom) but that's fine. But for fun:

**Theorem**

Let X be a space satisfying the \\(T\_1\\) axiom. Let A be a subset of X, then the point x is a limit point of A iff every neighbourhood of x contains infinitely many points of A.

Back to hausdorff spaces:

**Theorem**

Every simply ordered set is a Hausdorff space in the order topology. Product and subspaces of hausdorff spaces are hausdorff spaces.


### Continuous functions {#continuous-functions}

**Definition**

A function \\(f : X \to Y\\) is continuous if for each open subset V of Y, the set \\(f^{-1}(V)\\) is an open subset of X.

It also suffices to show that the inverse image of each basis/subbasis element is open.

Other definitions:

**Theorem**

1.  For every subset of X, one has \\(f(\bar{A}) \subset \bar{f}(A)\\).
2.  For every closed set of B of Y, the set \\(f^{-1}(B)\\) is closed in X.
3.  For every \\(x \in X\\) and each neighbourhood \\(V\\) of f(x), there is a neighbourhood \\(U\\) of x such that \\(f(U) \subset V\\).


#### Homeomorphisms {#homeomorphisms}

Let \\(f : X \to Y\\) be a bijection. If both \\(f\\) and its inverse function are continuous, \\(f\\) is called a homeomorphism.

Another way to define it is to say it is a bijective correspondence such that \\(f(U)\\) is open iff U is open.


### Metric topology {#metric-topology}

**Definition**

The collection of all $&epsilon;$-balls \\(B\_d(x,\epsilon)\\) is a basis for a topology on X, called the **metric topology**, induced by d.

**Definition (alt)**

A set U is open in the metric topology induced by d iff for each \\(y \in U\\), there is a \\(\delta > 0\\) s.t. \\(B\_d(y,\delta) \subset U\\).

**Definition**

A topological space X is **metrizable** if there exists a metric on X that induces the topology of X. A **metric space** is a metrizable space together with a specific metric that gives the topology of X.