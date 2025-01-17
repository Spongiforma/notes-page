+++
title = "Abstract Algebra"
author = ["root"]
draft = false
+++

## Groups {#groups}

A group is an ordered pair (G,\*), where G is a set (closed under \*) and \* is a binary operation satisfying the following axioms.

1.  \* is associative
2.  There exists an identity element
3.  For each a in G, there is a double-sided inverse element

    If the operation is commutative within the group, then the group is abelian.

The order of an element x is the smallest positive integer n such that \\(x^n = 1\\).


### Dihedral groups {#dihedral-groups}

D\_2n is the set of symmetries of a regular n-gon via moving it in rigid motion. |D\_2n| = 2n.

The elements are r^i and s, where s is a reflection and r is a rotation

Properties:

1.  1, r, \\(r^2\\) ..., \\(r^{n-1}\\) are all distinct and \\(r^n\\) = 1, so \\(|r| = n\\).
2.  |s| = 2
3.  s != r^i for any i
4.  \\(sr^i \neq sr^j\\) for all i!=j, 0 <= i,j <= n-1.
5.  rs = sr^-1
6.  \\(r^i s = s r^{-i}\\)


### Generators and relations {#generators-and-relations}

Groups can be described with generators which is a subset of G such that every element of G can be written as a finite product of elements of S. G = <S>.

D\_2n = <r,s>

Relations are any equations satisfied by the generators. Groups can be represented by a presentation of G.

D\_2n = < \\(r,s | r^n = s^2 = 1, rs = sr^{-1}\\)>


### Symmetric groups {#symmetric-groups}

Let \\(\Omega\\) be any nonempty set and \\(S\_\Omega\\) to be the set of all bijections from \\(\Omega\\) to itself. Then \\(S\_\Omega\\) is a group under function composition.

Elements of a symmetric group S can be written in terms of its cycle decomposition.


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


### Group actions {#group-actions}

A group action of a group G acting on a set A is a map from \\(G \times A\\) to A (written \\(g \cdot a\\) for all \\(g \in G\\) and \\(a \in A\\)) satisfying the following properties:

1.  \\(g\_1 \cdot (g\_2 \cdot a) = (g\_1g\_2)\cdot a\\), for all g1,g2 in G, a in A
2.  \\(1 \cdot a  = a\\), for all a in A.