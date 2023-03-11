# Relation and Function

## Relation

### definition of relation

A subset $R \subset A \times B$ is called a (binary) relation from $A$ to $B$. The domain and range of $R$ is given by

- $domian(R) := \lbrace x | \exists y (xRy) \rbrace$
- $range(R) := \lbrace y | \exists x (xRy) \rbrace$

If $A = B$, we say $R$ is a relation on $A$.

### notation of relation

- $(x, y) \in R \Leftrightarrow xRy$
- $(x, y) \notin R \Leftrightarrow x$$\not$$Ry$

### example of relation

- empty relation
  $R = \emptyset$, $domain(\emptyset) = range(\emptyset) = \emptyset$
- identity relation
  $R \subset A \times A$,
  $$id_A = \lbrace (a, a) | a \in A \rbrace$$
  $domain(id_A) = range(id_A) = A$
- $A \times B$ itself
  $domain(A \times B) = A$ and $range(A \times B) = B$

## Function

A function $F : A \to B$ is a triple $(A, F, B)$ where $F \subset A \times B$ is a relation such that
$$(\forall x \in A)(\exists !y(xFy))$$
where $A, B$ are domain and codomain of $F$.

## Partial function

A relation $R \subset A \times B$ is said to be functional (or right-unique) if
$$(\forall x \in domR)(\exists !y(xRy))$$

A partial function is a triple $(A, F, B)$ such that $F \subset A \times B$ is a functional relation.

## Operations on relations/functions

- inverse
  $F^\top = F^{-1} = \lbrace (y, x) | xFy \rbrace$
- composition
  $F \circ G = \lbrace (x, z) | \exists y (xGy \wedge yFz) \rbrace$
- restriction
  $F | A = \lbrace (x, y) | (xFy) \wedge (x \in A) \rbrace$
- image
  $F(A) = im(F | A) = \lbrace y | (\exists x \in A)(xFy) \rbrace$

## Matrix representation of a relation

Given finite sets $A = \lbrace a_1, a_2, \ldots, a_m \rbrace, B = \lbrace b_1, b_2, \ldots, b_n \rbrace$, and a relation $R \subset A \times B$, we define a $m \times n$ matrix $M_R = (m_{ij})$, where
$$m_{ij} =
\begin{cases}
1 & \text{if $(a_i, b_i) \in R$}\\
0 & \text{if $(a_i, b_i) \notin R$}
\end{cases}$$

## Composing relations

Let $A, B, C$ be sets, $R \subset A \times B, S \subset B \times C$ be relations, then $M_RM_S = M_{S \circ R}$

### theorem of composing relations

Given a set $A$, the triple $(\mathcal{P}(A \times A), \circ, id_A)$ is a monoid.

## Injection and surjection

Given a function $F: A \to B$, with $domF = A$ and $im(F) \subset B$, then

- $F$ is injective or one-to-one if $(\forall x, y \in A)(F(x) = F(y) \rightarrow x = y)$.
- $F$ is surjective or onto if $im(F) = B$.
- $F$ is bijective if it is both injective and surjective.

Given a function $F: A \to B, A \neq \emptyset$, then

- There exists a function $G: B \to A$ (a "left inverse") such that $G \circ F = id_A$ $\Leftrightarrow$ $F$ is one-to-one/injective.
- There exists a function $G: B \to A$ (a "right inverse") such that $F \circ G = id_B$ $\Leftrightarrow$ $F$ is onto/surjective.

Let $f: A \to B, g: B \to C$

- If $g \circ f$ is injective, then $f$ is injective.
- If $g \circ f$ is surjective, then $g$ is surjective.

## Relations as functions

Given a relation $R \subset A \times B$, the associated boolean function is given by
$$\phi_R: A \times B \to \lbrace \top, \bot \rbrace\\
(x, y) \mapsto
\lbrace
\begin{array}{lc}
\top, & xRy\\
\bot, & otherwise\\
\end{array}
$$

$$\alpha_R: A \to \mathcal{P}(B)\\
x \mapsto \lbrace y \in B | xRy \rbrace$$

$$\beta_R: B \to \mathcal{P}(A)\\
x \mapsto \lbrace y \in A | xRy \rbrace$$

## Properties of relations

For a binary relation $R$ on $A$,

- reflexive: if $(\forall x \in A)(xRx)$.
- irreflexive: if $(\forall x \in A)(xRx \rightarrow \bot)$
- strongly connected or total: if $(\forall x, y \in A)(xRy \vee yRx)$.
- transitive: if $(\forall x, y, z \in A)(xRy \wedge yRz \rightarrow xRz)$.
- symmetric: if $(\forall x, y \in A)(xRy \rightarrow yRx)$.
- anti-symmetric: if $(\forall x, y \in A)(xRy \wedge yRx \rightarrow x = y)$.
- asymmetric: if $(\forall x, y \in A)(xRy \wedge yRx \rightarrow \bot)$.

## Important relations

### non-strict partial order

- reflexive
- anti-symmetric
- transitive

### strict partial order

- irreflexive
- asymmetric
- transitive

### equivalence

- reflexive
- symmetric
- transitive

## Equivalence class

Given an equivalence relation on $A$, the equivalence class containing $x$ is the set
$$[x]_R := \lbrace t \in A | xRt \rbrace$$

Given an equivalence relation $R$ on $A$, then for $x, y \in A$,
$$[x]_R = [y]_R \Leftrightarrow xRy$$

## Partition

A partition $\Pi$ of a set $A$ is a set of nonempty subsets of $A$ that is disjoint and exhaustive,

- $(\forall a, b \in \Pi)(a \neq b \rightarrow a \cap b = \emptyset)$;
- $\bigcup \Pi = A$.

Given an equivalence relation $R$ on $A$, then the set $\lbrace [x]_R | x \in A \rbrace$ of all equivalence classes is a partition of A.

## Quotient set

Given an equivalence relation $R$ on $A$, the quotient set is given by
$$A/R := \lbrace [x]_R | x \in A\rbrace$$
where $A/R$ is read "A modulo R".
