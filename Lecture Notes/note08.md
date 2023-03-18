# Linear Recurrence Relation

A sequence $(a_n) = (a_0, a_1, a_2, \dots)$ satisfies a (homogeneous) linear recurrence relation of order $d$ if there exists constants $c_1, c_2, \dots, c_d$ with $c_d \neq 0$ such that
$$a_n = c_1a_{n - 1} + c_2a_{n - 2} + \dots + c_da_{n - d}$$
for all $n \ge d$.

## $d = 2$

$a_n = c_1 a_{n - 1} + c_2 a_{n - 2}$

we call $\chi (t) = t^2 - c_1 t - c_2$ the characteristic polynomial of the linear recurrence relation. Let $r_1$ and $r_2$ be the roots of $\chi$, $\chi (t) = (t - r_1)(t - r_2)$.

- $r_1 \neq r_2$
  there exist constants $\alpha_1, \alpha_2$ such that $a_n = \alpha r_1^n + \alpha_2 r_2^n$
- $r_1 = r_2 = r$
  there exist $\alpha_1, \alpha_2$ such that $a_n = (\alpha_1 + \alpha_2 n)r^n$

## Higher order

$\chi (t) = t^d - c_1 t^{d - 1} - c_2 d^{d - 2} - \dots - c_{d - 1} t - c_d$.

Let $r_1, r_2, \dots, r_d$ be the roots of $\chi$.

- all $r_1, r_2, \dots, r_d$ are distinct
  there exist $\alpha_1, \alpha_2, \dots, \alpha_d$ such that
  $$a_n = \alpha_1 r_1^n + \alpha_2 r_2^n + \dots + \alpha_d r_d^n$$
- the root $r_i$ appears with the multiplicity $m_i$
  the solution contains
  $$r_i^n, n r_i^n, n^2 r_i^n, \dots, n^{m_i - 1} r_i^n$$
  the final solution is their linear combination

## Inhomogeneous equation

Homogeneous solution + particular solution
