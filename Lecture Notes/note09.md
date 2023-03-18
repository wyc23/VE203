# Formal power series

$A(x) = \sum_{n \ge 0}a_n x^n$

## Properties

- equality: $A(x) = B(x) \Leftrightarrow a_n = b_n$ for all $n \in \mathbb{N}$
- addition: $A(x) + B(x) = \sum_{n \ge 0}(a_n + b_n)x^n$
- multiplication: $A(x)B(x) = \sum_{n \ge 0}(\sum^{n}_{i = 0} a_ib_{n - i})$

## Inverse

A formal power series $A(x)$ is invertible if there exists $B(x)$ such that $A(x)B(x) = 1$. We write
$$B(x) = A(x)^{-1} = \frac{1}{A(x)}$$

A formal power series $A(x)$ is invertible iff $a_0 \neq 0$

### example

$A(x) = \sum_{n \ge 0}x^n, B(x) = 1 - x$, we have $A(x)B(x) = 1$.

$$\frac{1}{1 - x} = \sum_{n \ge 0}x^n$$

## Composition

Let $A(x), B(x)$ be formal power series, $a_0 = 0$ or $B$ is polynomial, then the composition is given by
$$(B \circ A)(x) = B(A(x)) = \sum_{n \ge 0}b_nA(x)^n.$$

## Derivative

$$DA(x) = \sum_{n > 0}na_nx^{n - 1} = \sum_{n \ge 0}(n + 1)a_{n + 1}x^n$$
