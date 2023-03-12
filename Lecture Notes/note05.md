# Numbers and Equinumerosity

## Integer

Let $\sim$ be the following equivalence relation on $\mathbb{N}^2$,

$$(a, b) \sim (c, d) \Leftrightarrow a + d = b + c.$$

Define $\mathbb{Z} = \mathbb{N} \times \mathbb{N} / \sim$.

Well-defined operations on the equivalence classes

- $[(a, b)] + [(c, d)] := [(a + c, b+ d)]$.
- $[(a, b)] \times [(c, d)] := [(ac + bd, ad + bc)]$.
- $[(a, b)] < [(c, d)]$ if $a + d < b + c$.

## Rational number

Let $\mathbb{Z}^+ = \lbrace z \in \mathbb{Z} | z > 0 \rbrace$, let $\sim$ be the following equivalence relation on $\mathbb{Z} \times \mathbb{Z}^+$,

$$(a, b) \sim (c, d) \Leftrightarrow a \times d = b \times c.$$

Define $\mathbb{Q} := \mathbb{Z} \times \mathbb{Z}^+ / \sim$.

Well-defined operations on the equivalence classes

- $[(a, b) + (c, d)] := [(ad + bc, bd)]$.
- $[(a, b) \times (c, d)] := [(ac, bd)]$.
- $[(a, b)] < [(c, d)]$ if $ad < bc$.

## Real number

A Cauchy sequence is a function $s: \mathbb{N} \to \mathbb{Q}$ such that:

$$(\forall \varepsilon \in \mathbb{Q}, \varepsilon > 0)(\exists k \in \mathbb{N})(\forall m, n > k)(|s_m - s_n| < \varepsilon).$$

Let $C$ be the set of all Cauchy sequence. For $r, s \in C$, $r$ and $s$ are equivalent $(r \sim s)$ if

$$(\forall \varepsilon \in \mathbb{Q}, \varepsilon > 0)(\exists k \in \mathbb{N})(\forall n > k)(|r_n - s_n| < \varepsilon).$$

Define $\mathbb{R}$ to be the quotient set $C / \sim$.

A Dedekind cut is a set $x \subset \mathbb{Q}$ such that

- $x \neq \emptyset$ and $x \neq \mathbb{Q}$
- $x$ is closed downward, $(\forall p, q \in \mathbb{Q})(p < q \rightarrow (q \in x \rightarrow p \in x))$
- $x$ has no largest element

Define $\mathbb{R}$ to be the set of all Dedekind cuts.

Let $x < y$ if $x \subset y$.

Every subset $A \subset \mathbb{R}$ that is bounded above admits a least upper bound.

## Equinumerosity

A set $A$ is equinumerous to a set $B$ (written $A \approx B$) if there is a bijection from $A$ to $B$.

Note that for any sets $A, B, C$

- $A \approx A$
- $A \approx B \Rightarrow B \approx A$
- $(A \approx B \wedge B \approx C) \Rightarrow A \approx C$

However, this is **NOT** an equivalence relation.

$\mathbb{Z} \approx \mathbb{N}$

### $\mathbb{N} \times \mathbb{N} \approx \mathbb{N}$

Cantor's pairing function:

$J: \mathbb{N}^2 \to \mathbb{N}$,
$J(x, y) = $ $x + y + 1 \choose 2$ $+ y$

The only quadratic pairing function are Cantor polynomials, but it is unknown whether this is the only polynomial pairing function.

### $\mathbb{Q} \approx \mathbb{N}$

## Cantor's theorem

- $\mathbb{R} \not \approx \mathbb{N}$.
- For every set $A$, $A \not \approx \mathcal{P}(A)$.

The set $\mathbb{R}^2$ of all ordered pairs of real numbers has the same size as $\mathbb{R}$.
