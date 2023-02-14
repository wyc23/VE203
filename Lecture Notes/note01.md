# Set

## Definition

A set is an unordered collection of distinct objects.

## Notation

### number system

common number sets like natural number, real number and so on.

### cardinality

The size of a set is called its cardinality, denoted by $|A|$, $\#A$ or $card A$.

> note that a set is either a finite set or an infinite set.

## Operation

- inclusion
  > note that $A = B$ iff $A \subset B$ and $B \subset A$.
- proper subset/superset
- union
  we denote the union of a collection of sets $\mathcal{C}$ as
  $$\bigcup\mathcal{C} = \{x|\exist X \in \mathcal{C} \space s.t. \space x \in X \} = \bigcup\{X|X \in \mathcal{C}\} = \bigcup_{X \in \mathcal{C}} X$$
- intersection
  We denote the intersection of a nonempty collection of sets $\mathcal{C}$ as
  $$\bigcap \mathcal{C} = \{x|\forall X \in \mathcal{C} \space s.t. \space x \in X\} = \bigcap \{X|X \in \mathcal{C}\} = \bigcap_{X \in \mathcal{C}} X$$

  > note that $\bigcap \emptyset$ is undefined
- set difference
  The set difference of A and B, denoted by A - B or A \ B, is the set of elements that are in A but not in B.
- symmetric difference
  $$A \triangle B = (A-B)\cup (B-A)$$
- power set
  The power set of a set A is the set of all subsets of A, denoted by $\mathcal{P}(A)$.
- cardinality of power set
  $$|\mathcal{P}(A)| = 2^{|A|}$$

## Venn diagram and Euler diagram

![img of venn and euler diagram](https://media.springernature.com/lw785/springer-static/image/art:10.1186%2Fs12859-016-1281-5/MediaObjects/12859_2016_1281_Fig1_HTML.gif)

## Set algebra

- commutative laws
- associative laws
- distribution laws
- De Morgen's law

## Cartesian product

### definition of Cartesian product

The Cartesian product of set A and B is the set of **ordered pairs**, such that

$$A \times B = \{(a,b)|a \in A, b \in B\}$$

### definition of ordered pair

An ordered pair (a,b) is defined as

$$(a,b) := \{\{a\},\{a,b\}\}$$

### theorem

1. If $a \in \mathcal{C}$ and $b \in \mathcal{C}$, then $(a,b) \in \mathcal{P}(\mathcal{P}(C))$.

2. (x,y) = (a,b) iff x = a and y = b.

## Cartesian product of sets

The n-fold Cartesian product $A_1 \times A_2 \times \cdot \cdot \cdot \times A_n$ of sets $A_k$ is the set of ordered n-tuple $(a_1,a_2,\cdot \cdot \cdot,a_n)$.

## Associative set operations

- intersection
- union
- Cartesian product
- symmetric difference

## Simple graphs

### k-element subsets

Let $X$ be a finite set. For positive integer $k$, let $\begin{pmatrix}X\\k\\
\end{pmatrix}$ denotes the set of all k-element subsets.

> note that $\Big\lvert\begin{pmatrix}X\\k\\
\end{pmatrix}\Big\rvert$ = $\begin{pmatrix}|X|\\k\\
\end{pmatrix}$

### definition of simple graph

A finite simple graph is a pair $(V,E)$ where $V$ is a non-empty finite set and $E$ is a set of 2-element subsets of $V$.

Elements of $V$ are called vertices and elements of $E$ are called edges.

We call $V$ the vertex set, $E$ the edge set.

## Directed graph

A directed graph is a quadruple $G = (V,E,s,t)$, where $s,t: E \to V$ to be the source function and target function.
