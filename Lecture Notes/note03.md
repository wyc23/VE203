# Induction

## Mathematical induction

Mathematical induction works by establishing two statements:

1. the base case: $P(n_0)$ is true
2. the inductive case: $P(n+1)$ is true whenever $P(n)$ is true for $n \geq n_0$

   In the inductive case, $P(n)$ is called inductive hypothesis, abbreviated as **IH**.

## Monoid

### definition of monoid

A monoid is a triple $(M, e, \star)$, where M is a set, together with an identity element $e \in M$, and a function $M \times M \to M$, such that for all $m, n, p \in M$, the following monoid laws hold,

- $m \star e = m$ and $e \star m = m$
- $(m \star n) \star p = m \star (n \star p)$

### remark of monoid

- the monoid laws can also be written as:
  - $\star (m, e) = m$ and $\star (e, m) = m$
  - $\star (\star (m, n), p) = \star (m, \star (n, p))$
- we can prove the identity element is unique

## Recursively defined structure

### arithmetic expression

An arithmetic expression is any of the following:

- any integer $n$;
- $-E$, where $E$ is an arithmetic expression;
- $E \odot F$, where $E$ and $F$ are arithmetic expressions and $\odot = \lbrace +, -, \cdot, / \rbrace$ is an operator.

### sentence of propositional logic

A sentence propositional logic (also know as well-formed formula, or wff) over propositional variables X is one of the following:

- $x$, for some $x \in X$;
- $\neg P$, where $P$ is a wwf over $X$;
- $P \vee Q$, $P \wedge Q$, or $P \rightarrow Q$, where $P$ and $Q$ are wffs over $X$.

### natural numbers, recursively defined

A natural number is either:

- zero, denoted by 0; or
- the successor of a natural number $n$, denoted by succ($n$) or $n^+$ for a natural number $n$.

## Recursion theorem on $\mathbb{N}$

Let $A$ be a set, $a \in A$, and $g: A \to A$. Then there **exists** a **unique** function $f: \mathbb{N} \to A$ such that

- $f(0) = a$
- $f(n^+) = g(f(n))$ for all $n \in \mathbb{N}$.

### example of $A_k$

For fixed $k \in \mathbb{N}$, consider the function $A_k: \mathbb{N} \to \mathbb{N}$ given by

- $A_k(0) := k$
- $A_k(n^+) := A_k(n)^+$

### example of $M_k$

For fixed $k \in \mathbb{N}$, consider the function $M_k: \mathbb{N} \to \mathbb{N}$ given by

- $M_k(0) := 0$
- $M_k(n^+) := A_k(M_k(n))$

## Arithmetic and order on $\mathbb{N}$

- $0 := \lbrace \rbrace = \emptyset$
- $n + 1 = n^+ := n \cup \lbrace n \rbrace, n \in \mathbb{N}$
- $n + k = A_K(n)$
- $n \times k = M_k(n)$
- $n < m$ if $n \in m$

## Structural induction

Structural induction establish statement on a recursively defined set. The elements specifically included in the set are basis elements of the set, the structural induction works in the following two steps:

1. Establish the statement for the basis elements.
2. Show that if the statement is true for each elements used to construct new elements in the recursive step of the definition, the statement holds for these new elements.

## Propositional logic using $\neg$ and $\wedge$

This is a good example of structural induction, refer to the sides 109-110 of partI.

## String

A string is a finite sequence with entries in a finite set $\Sigma$, called alphabet. The length of a string is the length of the sequence. There is a unique string with length 0, denoted by $\lambda$ or $\varepsilon$.

The set $\Sigma^*$ of string over the alphabet $\Sigma$ is defined recursively by

- $\varepsilon \in \Sigma^*$,
- If $a \in \Sigma$ and $x \in \Sigma^*$, then $ax \in \Sigma^*$, where $ax := (a, x)$ is an ordered pair.

The concatenation of two string, denoted by $\cdot: \Sigma^*\times \Sigma^* \to \Sigma^*$, is defined recursively as follows

- If $z \in \Sigma^*$, then $\varepsilon \cdot z = z$,
- If $w, z \in \Sigma^*$ and $w = ax$, then $w \cdot z = a(x \cdot z)$.

Given a set $\Sigma$, the triple $(\Sigma^*, \varepsilon, \cdot)$ is a monoid.

The length of a string, $l: \Sigma^* \to \mathbb{N}, w \mapsto l(w)$, can be recursively defined as

- $l(\varepsilon) = 0$,
- $l(ax) = 1 + l(x)$ if $a \in \Sigma$ and $x \in \Sigma^*$.

## Weak induction as special case of structural induction

Since $\mathbb{N}$ is a recursively defined set, structural induction can be applied to prove statement on $\mathbb{N}$.

## Well-ordered principle

Every nonempty collection of natural numbers has a least element.
