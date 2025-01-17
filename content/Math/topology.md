+++
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

**Definition**

A subset Y of X is convex in X if for each pair of points \\(a < b\\) of Y, the entire interval of points of X lies in Y.

**Theorem**

Let \\(X\\) be an ordered set in the order topology, let Y be a subset of X that is convex in X. Then the order topology on Y, is the same as the topology Y inherits as a subspace of X.


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

**Definition**

If \\(f\\) is an injective continuous map, and f' is the surjective function by restricting the range of f, f is a topological imbedding if f' is a homeomorphism of X with Z.


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

**Lemma (Sequence lemma)**

Let \\(X\\) be a topological space. Let \\(A \subset X\\). If there is sequence of points of \\(A\\) converging to \\(x\\), then \\(x \in \bar{A}\\). the converse holds if \\(X\\) is metrizable.

**Theorem**

Let \\(f : X \to Y\\). If the fucntion if is continuous, then for every convergent sequence \\(x\_n \to x\\) in X, the sequence \\(f(x\_n)\\) converges to \\(f(x)\\). The converse holds if \\(X\\) is metrizable.

**Theorem (Uniform limit theorem)**

Let \\(f\_n : X \to Y\\) be a sequence of continuous functions from the topological space \\(X\\) to the metric space \\(Y\\). If \\((f\_n)\\) converges uniformly to \\(f\\), then \\(f\\) is continuous.


### Quotient topology {#quotient-topology}

**Definition**

Let X and Y be topological spaces; let \\(p : X \to Y\\) be a surjective map. The map \\(p\\) is said to be a quotient map provided a subset \\(U\\) of \\(Y\\) is open in Y if and only if \\(p^{-1}(U)\\) is open in X.

(like a homeomorphism without being injective)

**Definition**

A subset \\(C\\) of \\(X\\) is saturated (with respect to the surjective map) if \\(C\\) contains every set \\(p^{-1}({y})\\) it intersects. Thus \\(C\\) is saturated if it equals the complete inverse image of a subset of \\(Y\\). To say that \\(P\\) is a quotient map is equivalent to saying that \\(p\\) is continuous and \\(p\\) maps saturated open sets of \\(X\\) of to open sets of \\(Y\\).

A map is an open set if for each open set in its domain, its image is also open, and likewise for closed maps. All open/closed maps are quotient maps.

**Definition**

If X is a space and A is a set and if \\(p:X\to A\\) is a surjective map, there is exactly one topology \\(\mathcal{T}\\) on A relative to which p is a quotient map, which is the **quotient topology** induced by p.

**Definition**

Let \\(X\\) be a topological space, and let \\(X^\*\\) be a partition of \\(X\\) into disjoint subsets whose union is \\(X\\). Let \\(p : X \to X^\*\\) be the surjective map that carries each point of \\(X\\) to the element of \\(X^\*\\) containing it. In the quotient topology induced by \\(p\\), the space \\(X^\*\\) is called a **quotient space** of X.

What concepts do quotient maps work well with?


#### Subspaces {#subspaces}

**Theorem**

Let \\(p : X \to Y\\) be a quotient map; let A be a subspace of X that is saturated with respect to p.; let \\(q: A \to p(A)\\) be the map obtained by restricting p.

1.  If A is either open or closed in X, then q is a quotient map
2.  If p is either an open map or a closed map, then q is a quotient map.


#### Composites {#composites}

Composites of quotient maps are quotient maps.


#### Products {#products}

Products of maps do not behave well, and one needs conditions such as local compactness, and that the two maps are open maps.


#### Hausdorff condition {#hausdorff-condition}

Does not behave well.

For \\(X^\*\\) to satisfy the \\(T\_1\\) axiom, one requires that each eleemtn of the partition \\(X^\*\\) be a closed subset of \\(X\\).


#### Continuous functions {#continuous-functions}

Similar to how we had a criterion for determining when a map into a product space was continuous, we wish to find when a map out of a quotient space is continuous.

**Theorem**

Let \\(p:X\to Y\\) be a quotient map. Let \\(Z\\) be a space and let \\(g : X \to Z\\) be a map that is constant on each set \\(p^{-1}({y})\\) for \\(y \in Y\\). Then \\(g\\) induces a map \\(f : Y \to Z\\) such that \\(f \circ p = g\\). The induced map \\(f\\) is continuous iff g is continuous; f is a quotient map iff g is a quotient map.

**Corollary**

Let \\(g : X \to Z\\) be a surjective continuous map. Let \\(X\*\\) be the following collection of subsets of \\(X\\):

\\[
X^\* = \\{g^{-1}(\\{z\\}) \vert z \in Z\\}
\\]

Give it the quotient topology.

1.  The map g induces a bijective continuous map f, which is a homeomorphism iff g is a quotient map
2.  If \\(Z\\) is Hausdorff, so is \\(X^\*\\).kk


#### Topological Groups {#topological-groups}

A **topological group** G is a geoup that is also a topological space satisfying the \\(T\_1\\) axiom, such that the map of \\(G \times G\\) into \\(G\\) sending \\(x x y\\) into \\(x \dot y\\) and the map of G into G sending x into 1/x are continuous maps.


## Connectedness and compactness {#connectedness-and-compactness}


### Connected spaces {#connected-spaces}

**Definition**

Let \\(X\\) be a topological space. A **seperation** of X is a pair of disjoint nonempty open subsets of X whose union is X. The space is **connected** if there does not exist a seperation of X.

Note that connectedness is a topological property.

Another formulation of connectedness is that a space is connected iff the only subsets that are both open and closed in X are the empty set and X itself.

For a subspace of a topological space, there is another useful formulation.

**Lemma**

If Y is a subspace of X, a seperation of Y is a pair of disjoint nonempty sets A and B whose union is Y. neither of which contains a limit point of the other. The space Y is connected if there exists no seperation of Y.


#### Forming connected spaces from given ones {#forming-connected-spaces-from-given-ones}

**Lemma**

If the sets C and D form a seperation of X, and if Y is a connected subspace of X, then Y lies entirely within either C or D.

**Properties:**

1.  The union of a collection of connected subspaces of X that have a point in common is connected.
2.  Let A be a connected subspace of X. If \\(A \subset B \subset \bar{A}\\), then B is also connected.
3.  The image of a connected space under a continuous map is connected.
4.  A finite cartesian product of connected spaces is connected.


### Connected subspaces of the real line {#connected-subspaces-of-the-real-line}

A simply ordered set L having more than one element is called a **linear continuum** if the following hold:

1.  L has the least upper bound property
2.  If \\(x < y\\), there exists \\(z\\) such that \\(x < z < y\\)

**Theorem**

If L is a linear continuum in the order topology, then L is connected, and so are intervals and rays in L.

**Corollary**

The real line is connected and so are intervals and rays

**Theorem (Intermediate value theorem)**

Let \\(f : X \to Y\\) be a continuous map, where X is a connected space and Y is an ordered set in the order topology. If a and b are two points of X and if r is a point of Y lying between f(a) and f(b), then there exists a point c of X such that f(c) = r.


### Path connectedness {#path-connectedness}

**Definition**

Given points x and y of the space X, a **path** in X from x to y is a continuous map \\(f : [a,b] \to X\\) of some closed interval in the real line into X, such that f(a) = x and f(b) = y. A space X is said to be path connected if every pair of points of X can be joined by a path in X.

Although a path-connected space is connected, the converse may not hold (Such as the ordered square).


### Components and local connectedness {#components-and-local-connectedness}

**Definition**

Given X, define an equivalence relation on X by setting \\(x \tilde y\\) if there is a connected subspace of X containing both x and y. The equivalence classes are the components of X.

**Theorem**

The components of X are connected disjoint subspaces of X whose union is X. such that nonempty connected subspace of X intersects only one of them.

**Theorem**

the path components are defined similarly, with an equivalence relation when there is a path from x to y in X.

**Theorem**

The path components of X are path-connected disjoint subpaces of X whose union is X, such that each nonempty path-connected subspace of X intersects only one of them.

**Definition**

A space X is said to be **locally connected at x**, if for every neighbourhood U of x, there is a connected neighborhood V of x contained in U. If X is locally connected at each of its points, it is said simply to be locally connected. Similarly, a space is **locally path connected at x** if for every neighbourhood U of X, there is a path-connected neighborhood V of x contained in U.

**Theorem**

A space X is locally connected iff for every open set U of X, each component of U is open in X.

**Theorem**

A space X is locally path connected iff for every open set U of X, each path component of U is open in X.

**Theorem**

If X is a topological space, each path component of X lies in a component of X. If X is locally path connected, then the components and the path components of X are the same.


### Compact spaces {#compact-spaces}

**Definition**

A space X is **compact** if every open covering A of X contains a finite subcollection that also covers X.

**Theorem**

Every closed subspace of a compact space is compact.

**Theorem**

Every compact subspace of a Hausdorff space is closed

**Lemma**

If Y is a compact subspace of the Hausdorff space X and \\(x\_0\\) is not in Y, then there exist disjoint open sets U and V of X containing \\(x\_0\\) and Y, respectively.

**Theorem**

The image of a compact space under a continuous map is compact.

**Theorem**

Let \\(f : X \to Y\\) is a bijective continuous function. If X is a compact and Y is Hausdorff, then f is a homeomorphism

Useful for proving a map is a homeomorphism.

**Theorem**

The product of finitely many compact spaces is compact.

**Lemma (The tube lemma)**

Consider the product space \\(X \times Y\\), where Y is compact. If N is an open set of \\(X \times Y\\) containing the slice \\(x\_0 \times Y\\) of \\(X \times Y\\), then N contains some tube \\(W \times Y\\) about \\(x\_0 \times Y\\), where \\(W\\) is a neighbourhood of \\(x\_0\\) in X.

For infinite products, we require the Tychanoff theorem.


#### Finite intersection {#finite-intersection}

Following is another formulation of compactness.

**Definition**

A collection \\(\mathcal{C}\\) of subsets of X is said to have the **finite intersection property** if for every finite subcollection, its intersection is nonempty.

**Theorem**

Let X be a topological space. Then X is compact iff for every collection of closed sets in X having the finite intersection property, the intersection of all its elements is nonempty.


### Compact subspaces of the real line {#compact-subspaces-of-the-real-line}

**Theorem**

Let X be a simply ordered set having the least upper bound property. In the order topology, each closed interval in X is compact.

**Corollary**

Every closed interval in \\(\mathbb{R}\\) is compact

**Theorem**

A subspace A of \\(R^n\\) is compact iff it is closed and bounded in the euclidean or square metric.

**Theorem (EVT)**

Let \\(f : X \to Y\\) be continuous, where Y is an ordered set in the order topology. If X is compact, then there exist points c and d in X such that \\(f( c) \leq f(x) \leq f(d)\\) for every \\(x \in X\\).


#### Uniform continuity theorem {#uniform-continuity-theorem}

**Definition**

Let (X,d) be a metric space. let A be a nonempty subst of X. For each \\(x \in X\\), we define the distance from x to A by the equation:

\\[
d(x,A) = \inf \\{d(x,a) \vert a \in A\\}
\\]

**Lemma (The Lebesgue number lemma)**

Let \\(\mathcal{A}\\) be an open covering of the metric space (X,d). If X is compact, there is a \\(\delta > 0\\) such that for each subset of X having diameter less that \\(\delta\\), there exists an element of \\(\mathcal{A}\\) containing it.

\\(\delta\\) is known as the **Lebesgue number**.

**Definition**

A function f fomr the metric space \\((X,d\_X)\\) to the metric space \\((Y,d\_Y)\\) is said to be **uniformly continuous** if given \\(\epsilon > 0\\), there is a \\(\delta > 0\\) such that for every pair of points \\(x\_0,x\_1\\) of X.

**Theorem (Uniform continuity theorem)**

Let \\(f : X \to Y\\) be a continuous map of the compact metric space (X,dx) to the metric space (Y,dy). Then f is uniformly continuous.


#### Uncountability of real numbers {#uncountability-of-real-numbers}

**Definition**

A point x of a space X is said to be an **isolated point** of X if the one-point set \\(\\{x\\}\\) is open in X.

**Theorem**

Let X be a nonempty compact Hausdorff space. If X has no isolated points, then X is uncountable.

**Corollary**

Every closed interval in \\(\mathbb{R}\\) is uncountable.


### Limit point compactness {#limit-point-compactness}

Also known as **Frechet compactness**, or **Bolzano-Weierstrass property**, and was the former definition of compactness whereas the covering formulation was called "bicompactness".

**Theorem**

Compactness implies limit point compactness, but not conversely.

**Definition**

Let X be a topological space. It is **sequentially compact** if every sequence of points of X has a convergent subsequence.

But metrizable spaces are very nice so:

**Theorem**

Let \\(X\\) be a metrizable space. Then the three defintions of compactness are equivalent.


### Local compactness {#local-compactness}

We wish to prove the basic theorem that any locally compact Hausdorff space can be imbedded in a certain compact Hausdorff space that is called its **one-point compactification.**

**Definition**

A space X is said to be **locally compact at x** if there is some compact subspace C of X that contains a neighbourhood of x.

Metrizable spaces and compact Hausdorff spaces are very well behaved. A subspace of a metrizable space is also metrizable but the subspace of a compact Hausdorff space need not be compact.

**Theorem**

Let X be a space. Then X is locally compact hausdorff iff there exists a space Y satisfying the following conditions:

1.  X is a subspace of Y.
2.  The set Y - X consists of a single point.
3.  Y is a compact Hausdorff space.

If there are two spaces satisfying these conditions, then there is a homeomorphism between them that equals the identity map on X.

**Definition**

If Y is a compact Hausdorff space and X is a proper subspace of Y whose closure equals Y, then Y is said to be a **compactification** of X. If Y-X equals a single point, then Y is called the **one-point compactification** of X.

But our definition of local compactness does not involve arbitrarily small neighbourhoods like the other definitions. Thus, here is a definition which is equivalent when X is Hausdorff.

**Theorem**

Let X be a Hausdorff space. Then X is locally compact iff given x in X, and given a neighborhood U of x, there is a neighbourhood V of x such that \\(\bar{V}\\) is compact and \\(\bar{V}\subset U\\).

**Corollary**

Let X be locally compact Hausdorff; Let A be a subspace of X. If A is closed/open in X, then A is locally compact.

If A is closed, we don't need the Hausdorff condition.

**Corollary**

A space X is homeomorphic to an open subspace of a compact Hausdorff space iff X is locally compact Hausdorff.

This follows from the previous corollary and the second last theorem.


## Countability and Seperation axioms {#countability-and-seperation-axioms}

We wish to prove the Urysohn metrization theorem, which says that if a topological space satisfies a certain countability axiom (the second) and a certain seperation axiom (the regularity axiom), then X can be imbedded in a metric space and is thus metrizable.

Another imbedding theorem useful in geometry is that given a space that is a compact manifold, we show that it can be imbedded in some finite dimensional euclidean space.


### Countability Axioms {#countability-axioms}

**Definition**

A space X is said to have a **countable basis at x** if there is a countable collection \\(\mathcal{B}\\) of neighbourhoods of x such that each neighbourhood of x contains at least one of the elements of \\(\mathcal{B}\\). A space that has a countable basis at each of its points is said to satisfy the **first countability axiom**, or be **first-countable**.

**Theorem**

Let X be a topological space.

1.  Let A be a subset of X. If there is a sequence of points A converging to x, then \\(x\in \bar{A}\\). The converse holds if X is first-countable.
2.  Let \\(f: X \to Y\\). If f is continuous, then for every convergent sequence \\(x\_n \to x\\) in X, the sequence \\(\\{x\_n\\}\\) converges to \\(f(x)\\). The converse holds if X is first-countable.

**Definition**

If a space X has a countable basis for its topology, then X is said to satisfy the **second countability axiom**, or to be **second-countable**.

This axiom implies the first, and is usually satisfied by familiar spaces.

**Theorem**

A subspace of a first-countable space is first-countable, and a countable product of first-countable spaces if first-countable. A subspace of a second-countable space is second-countable, and a countable product of second-countable spaces is second-countable.

**Definition**

A subset A of X is said to be **dense** in X if \\(\bar{A} = X\\).

**Theorem**

Suppose X has a countable basis. Then:

1.  Every open covering of X contains a countable subcollection covering X. (**Lindelof space**)
2.  There exists a countable subset of X that is dense in X. (**seperable**)


### Seperation axioms {#seperation-axioms}

We will introduce seperation axioms stronger than Hausdorff.

**Definition**

Suppose that one-point sets are closed in X. Then X is said to be **regular** if for each pair consisting of a point x and a closed set B disjoint from X, there exist disjoint open sets containing x and B, respectively. The space X is said to be **normal** if for each pair A,B of disjoint closed sets of X, there exist disjoint open sets containing A and B, respectively.

A regualar space is Hausdorff and a normal space is regular (Though we need to include the condition that one-point sets be closed. See the two-point space in the indiscrete topology satisfies the other parts of the definitions of regularity and normality without being Hausdorff).

**Lemma**

Let X be a topological space. Let one-point sets in X be closed.

1.  X is regular iff given a point x of X and a neighbourhood U of x, there is a neighbourhood V of x such that \\(\bar{V}\subset U\\).
2.  X is normal iff given a closed se A and an open set U containing A, there is an open set V containing A such that \\(\bar{V} \subset U\\).

**Theorem**

1.  A subspace of a Hausdorff space is Hausdorff; a product of Hausdorff spaces is Hausdorff.
2.  A subspace of a regular space is regular; a product of regular spaces is regular

But there is no analagous theorem for normal spaces