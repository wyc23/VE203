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

## Conditional statement

If $p$, then $q$.

- $p$: hypothesis
- $q$: thesis

> note that this statement is only false when $p$ is true and $q$ is false, otherwise it is true.
