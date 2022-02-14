+++
title = "Algebra"
author = ["root"]
draft = false
+++

## Monoids {#monoids}

A **monoid** is a triple (M,p,1), in which M is a non-vacuous set, p is an associative binary composition in M, and 1 is an element of M such that p(1,a) = a = p(a,1) for all \\(a \in M\\).

A monad without an associative p is sometimes called a **monad**. If there is no requirement on 1, then its a **semigroup** (M,p).

A **submonoid** of a set M, contains 1 and N is closed under the product in M.

A submonoid of the monoid M(S) of all transformations of the set S is a **monoid of transformations** of S.


### Cayley's theorem {#cayley-s-theorem}

1.  Any monoid is isomorphic to a monoid of transformations.
2.  Any group is isomorphic to a transformation group.


### Centralizer {#centralizer}

If \\(a \in M\\), the **centralizer** \\(C\_M(a)\\) is the subset of M of elements of b which commute with a. It can be shown to be a submonoid (or subgroup). The centralizer of a subset of M is defined similarly but take the intersection. C(M) is the **center** of M.


## Groups {#groups}

A group is an ordered pair (G,\*), where G is a set (closed under \*) and \* is a binary operation satisfying the following axioms.

1.  \* is associative
2.  There exists an identity element
3.  For each a in G, there is an (double-sided) inverse element

If the operation is commutative within the group, then the group is abelian.

The order of an element x is the smallest positive integer n such that \\(x^n = 1\\).

A group is also a monoid all of whose elements has an inverse element.


### Dihedral groups {#dihedral-groups}

D_2n is the set of symmetries of a regular n-gon via moving it in rigid motion. |D_2n| = 2n.

The elements are r^i and s, where s is a reflection and r is a rotation

Properties:

1.  1, r, \\(r^2\\) ..., \\(r^{n-1}\\) are all distinct and \\(r^n\\) = 1, so \\(|r| = n\\).
2.  |s| = 2
3.  s != r^i for any i
4.  \\(sr^i \neq sr^j\\) for all i!=j, 0 &lt;= i,j &lt;= n-1.
5.  rs = sr^-1
6.  \\(r^i s = s r^{-i}\\)


### Generators and relations {#generators-and-relations}

Groups can be described with generators which is a subset of G such that every element of G can be written as a finite product of elements of S. G = &lt;S&gt;.

D_2n = &lt;r,s&gt;

Relations are any equations satisfied by the generators. Groups can be represented by a presentation of G.

D_2n = &lt; \\(r,s | r^n = s^2 = 1, rs = sr^{-1}\\)&gt;


### Symmetric groups {#symmetric-groups}

Let \\(\Omega\\) be any nonempty set and \\(S\_\Omega\\) to be the set of all bijections from \\(\Omega\\) to itself. Then \\(S\_\Omega\\) is a group under function composition.

Elements of a symmetric group S can be written in terms of its cycle decomposition.

A **group of transformations** is a subgroup of the symmetric group of S.

The order is the lcm of the size of the group's disjoint cycles.


### Fields {#fields}

A Field is a set F together with two binary operations \\(+\\) and \\(\cdot\\) on F such that \\((F,+)\\) is an abelian group and \\((F - \\{0\\},\cdot)\\) is also an abelian group, and the distributive law holds.

\\[
F^\times = F - \\{0\\}
\\]

\\[
GL\_n(F) = \\{ A \vert \text{A is an $n \times n$ matrix with entries from F and det(A) $\neq$ 0} \\}
\\]

is called the general linear group of degree n.

\\[
\mathbb{Z}/p\mathbb{Z} = \mathbb{F}\_p
\\]

which is a finite field.


#### Properties {#properties}

1.  if F is a field and \\(|F| < \infty\\), then \\(| F | = p^m\\) for some prime p and integer m.
2.  if \\(|F| = q < \infty\\), then \\(|GL\_n(F)| = (q^n-1)(q^n-q)(q^n-q^2)\ldots(q^n-q^{n-1})\\)


### Quaternion group {#quaternion-group}

\\[
Q\_8 = \\{1,-1,i,-i,j,-j,k,-k\\}
\\]


### Homomorphisms and Isomorphisms {#homomorphisms-and-isomorphisms}

Let \\((G,\star)\\) and \\((H,\diamond)\\) be groups. A map \\(\psi : G \mapsto H\\) such that

\\[
\psi(x \star y) = \psi(x) \diamond \psi(y) \text{  for all $x,y \in G$}
\\]

is called a homomorphism.

The map \\(\psi : G \mapsto H\\) is called an isomorphism and G and H are said to be isomorphic or of the same isomorphism type, written \\(G \cong H\\), if

1.  \\(\psi\\) is a homeomorphism and
2.  \\(\psi\\) is a bijection

If \\(\psi : G \mapsto H\\), then

1.  |G| = |H|
2.  G is abelian iff H is abelian
3.  for all \\(x \in G\\), \\(|x| = |\psi(x)|\\)

Any two cyclic groups of the same order are isomorphic


### Group properties {#group-properties}

1.  Any subgroup of a cyclic group is cyclic. If &lt;a&gt; is infinite, the subgroups not equal to 1 are infinite and \\(s \to \langle a^s\rangle\\) is a bijective map of \\(\mathbb{N}\\) with the set of subgroups of \\(\langle a \rangle\\). If \\(\langle a \rangle\\) is finite of order \\(r\\), then the order of every subgroup is a divisor of r and for every positive divisor q of r, there is exactly one subgroup of order q.
2.  Let g and h be elements of an abelian group G having finite relatively prime orders m and n respectively. Then o(gh) = mn.
3.  Let g be an element of a finite abelian group of maximal order. Then \\(\exp G = o(g)\\)
4.  Let \\(\exp G\\) be the smallest integer \\(e\\) such that \\(x^e = 1\\) for all \\(x \in G\\). A finite abelian group is cyclic iff \\(\exp G = |G|\\).


### Group actions {#group-actions}

A group action of a group G acting on a set A is a map from \\(G \times A\\) to A (written \\(g \cdot a\\) for all \\(g \in G\\) and \\(a \in A\\)) satisfying the following properties:

1.  \\(g\_1 \cdot (g\_2 \cdot a) = (g\_1g\_2)\cdot a\\), for all g1,g2 in G, a in A
2.  \\(1 \cdot a  = a\\), for all a in A.


### Orbits &amp; cosets {#orbits-and-cosets}

Let G be a group of transformations of a set S. Then G defines an equivalence relation on S of \\(x \sim\_G y\\) if \\(y = \alpha(x)\\) for some \\(\alpha \in G\\). The G-orbit of \\(x \in S\\) is the set \\(Gx = \\{\alpha(x) \vert \alpha \in G\\}\\). When there is just one orbit, that is, \\(S = Gx\\) for some x, G is a **transitive** group of transformations of the set S. e.g. \\(S\_n\\) is transitive on \\(\\{1,2,\ldots,n\\}\\).


### Congruences {#congruences}

A congruence is an equivalence relation which can be multiplied.