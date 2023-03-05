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

## Relations as functions

## Properties of relations

