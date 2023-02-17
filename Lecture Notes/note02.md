# Logic

## Propositional logic

### definition of proposition

A proposition is a declared sentence that is either true or false.

## Notation

### propositional variables

Denoted by $p,q,r,...$

### booleans variables

- true, 1, $\top$
- false, 0, $\bot$

### connectives

- negation, $\neg$
- and, $\wedge$
- or, $\vee$
- implies, $\rightarrow$
- iff, $\leftrightarrow$

## CNF and DNF

Conjunctive Normal Form (CNF) is a conjunction of one or more clauses, where a clauses is a disjunction of literals.

Disjunctive Normal Form (DNF) is a disjunction of one or more clauses, where a clauses is a conjunction of literals.

- examples
  - CNF: $(\neg p \vee q \vee r) \wedge (\neg q \vee \neg r) \wedge (r)$
  - DNF: $(\neg p \wedge q \wedge r) \vee (\neg q \wedge \neg r) \vee (r)$

### theorem of DNF

For any proposition $\varphi$, there is a proposition $\varphi_{dnf}$ over the same Boolean variables and in DNF such that $\varphi \Leftrightarrow \varphi_{dnf}$.

### theorem of CNF

For any proposition $\varphi$, there is a proposition $\varphi_{cnf}$ over the same Boolean variables and in CNF such that $\varphi \Leftrightarrow \varphi_{cnf}$.

## Conditional statement

If $p$, then $q$.

- $p$: hypothesis
- $q$: thesis

> note that this statement is only false when $p$ is true and $q$ is false, otherwise it is true.

That is to say $p \rightarrow q$ is equivalent to $\neg p \vee q$.

## Converse/Inverse/Contrapositive/Negation

Given $p \rightarrow q$,

- converse: $q \rightarrow p$
- inverse: $\neg p \rightarrow \neg q$
- contrapositive: $\neg q \rightarrow \neg p$
- negation: $\neg (p \rightarrow q)$

> example: p-value

## Biconditional Statement

> if and only if (iff)

## Compound proposition

### order of operations

- $\neg$
- $\wedge$
- $\vee$
- $\rightarrow$
- $\leftrightarrow$

## Tautology and Contradiction

- tautology: all cases evaluates to 1.
- contradiction all cases evaluates to 0.

### equivalence

$p$ and $q$ are called equivalent iff $p \leftrightarrow q$ is a tautology, denoted by $p \Leftrightarrow q$.

## Tautological equivalence

### commutativity

$p \wedge q \Leftrightarrow q \wedge p$

$p \vee q \Leftrightarrow q \vee p$

### associativity

$(p \oplus q) \oplus r \Leftrightarrow p \oplus (q \oplus r)$

### distributivity

$p \vee (q \wedge r) \Leftrightarrow (p \vee q) \wedge (p \vee r)$

$p \wedge (q \vee r) \Leftrightarrow (p \wedge q) \vee (p \wedge r)$

### negation

$\neg \neg p \Leftrightarrow p$

$p \rightarrow q \Leftrightarrow (\neg q) \rightarrow (\neg p)$

$\neg (p \vee q) \Leftrightarrow (\neg p) \wedge (\neg q)$

$\neg (p \wedge q) \Leftrightarrow (\neg p) \vee (\neg q)$

### identity

$p \vee 0 \Leftrightarrow p$
$p \wedge 1 \Leftrightarrow p$

### null

$p \wedge 0 \Leftrightarrow 0$
$p \vee 1 \Leftrightarrow 1$

### idempotent

$p \wedge p \Leftrightarrow p$
$p \vee p \Leftrightarrow q$

### absorption

$p \wedge (p \vee q) \Leftrightarrow p$
$p \vee (p \wedge q) \Leftrightarrow p$

### cases

$(p \rightarrow q) \wedge (p \rightarrow r) \Leftrightarrow p \rightarrow (q \wedge r)$

$(p \rightarrow q) \vee (p \rightarrow r) \Leftrightarrow p \rightarrow (q \vee r)$

$(p \rightarrow r) \wedge (q \rightarrow r) \Leftrightarrow (p \vee q) \rightarrow r$
$(p \rightarrow r) \vee (q \rightarrow r) \Leftrightarrow (p \wedge q) \rightarrow r$

### added premise

$(p \wedge q) \rightarrow r \Leftrightarrow p \rightarrow (q \rightarrow r) \Leftrightarrow q \rightarrow (p \rightarrow r)$

## Rules of inference/formal implication/deduction

- detachment: $(p \rightarrow q) \wedge p \Rightarrow q$
- indirect reasoning: $(p \rightarrow q) \wedge \neg q \Rightarrow \neg p$
- disjunctive addition: $p \Rightarrow (p \vee q)$
- conjunctive simplification: $(p \wedge q) \Rightarrow p$
- disjunctive syllogism: $(p \vee q) \wedge \neg p \Rightarrow q$
- hypothetical syllogism: $(p \rightarrow q) \wedge (q \rightarrow r) \Rightarrow p \rightarrow r$
- resolution: $(p \vee q) \wedge (\neg p \vee r) \Rightarrow q \vee r$
  
### proof by contrapositive

$p \rightarrow q \Leftrightarrow (\neg q \rightarrow \neg p)$

### proof by contradiction

$p \rightarrow q \Leftrightarrow (p \wedge \neg q) \rightarrow 0$

### definition of formal implication

$p$ formally implies $q$ if $p \rightarrow q$ is a tautology, denoted by $p \Rightarrow q$.

> note that $p \Leftrightarrow q$ iff $p \Rightarrow q$ and $q \Rightarrow p$

## The natural numbers

Let $m,n \in \mathbb{N}$ be natural numbers.

1. $n \geq m \Leftrightarrow \exists k \in \mathbb{N}, n = m + k$.
2. $m | n \Leftrightarrow \exists k \in \mathbb{N}, n = m \cdot k$.
3. $2 | n \Rightarrow n$ is even.
4. $\exists k \in \mathbb{N}, n = 2k + 1 \Rightarrow n$ is odd.
5. $(n\in \mathbb{N}, n > 1) \wedge \neg(\exists k, 1 < k < n, k | n) \Rightarrow n$ is prime.

## Infinitude of primes

### theorem of infinitude of primes

There are infinitely many prime numbers.

### proof of infinitude of primes (by Euclid)

Consider a finite set of primes $\lbrace p_1, ..., p_k \rbrace$. Let $N = p_1p_2 \cdot \cdot \cdot p_k + 1$, so

- either N is a prime
- or N is not a prime, so N must admit a prime factor, which is not in $\lbrace p_1, ..., p_k \rbrace$. Call this new prime $p_{k+1}$.

In this way, we can always generate a new prime from a finite set of primes.
