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
