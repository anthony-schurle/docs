# Chapter 5: The Modular Worlds
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## #.# The Modular Worlds
---
### Definitions
- **Congruence**
  - Let m be a positive integers (the modulus). $x \equiv y$ modulo m if their difference is a multiple of m.
- **System Of Representatives**
  - Every number n mod m is congruent to an element of the system.
  - No two elements of the system are congruent to each other.
  - Natural representatives are typically natural numbers
  - Minimal representatives include negative numbers to have lowest absolute value members.
- **Polynomials**
  - Degree determined by modulus on coefficients.
  - Roots determined by congruence to 0, and so are all equivalent.
  - Polynomial A divides B if there exists C such that $B \equiv AC$ mod p.
  - The absolute value of polynomial A for prime modulus p is $|A| = p^{deg(A)}$, and $|0| = 0$.
  - Units are constant polynomials.
- **Irreducible Polynomials**
  - Polynomial P such that $deg(P) \ne 0$ and if A and B are polynomials with $AB \equiv P$ mod p, then A or B is a constant.

### Theorems & Proofs
**Proposition 5.3**
If $x \equiv x'$ and $y \equiv y'$ mod m, then $x \pm y \equiv x' \pm y'$ and $x \cdot y \equiv x' \cdot y'$ mod m.

**Proposition 5.9**
Let N be a positive integer. Let S be the sum of the base-ten digits of N. Then $N \equiv S$ mod 3 and $N \equiv S$ mod 9.

**Corollary 5.10**
Let N be a positive integer. Then N is divisible by 3 or 9 iff the sum of the digits of N is divisible by 3 or 9.

**Proposition 5.14**
Let (E ) be an equation, involving only integers, variables, addition, multiplication, and equality. If (E) has an integer solution, then the congruence (E mod m) has a solution for every modulus m.

**Theorem 5.15**
Every natural number can be expressed as the sum of four squares.

**Proposition 5.18**
The congruence $ax \equiv b$ mod m has a solution iff $GCD(a, m)$ divides b.

**Theorem 5.20**
Let m be a positive integer. Let a be an integer. Then a has a multiplicative inverse, mod m, iff $GCD(a, m) = 1$. Moreover, any two multiplicative inverses of a, mod m, are congruent mod m.

**Corollary 5.21**
Let p be a prime number and a an integer. Then a has a multiplicative inverse, mod p, iff $a \not \equiv 0$ mod p.

**Corollary 5.23**
Let m be a positive integer and a an integer satisfying $GCD(a, m) = 1$. Then for all integers x and y, $ax \equiv ay$ mod m implies $x \equiv y$ mod m.

**Corollary 5.24**
Let p be a prime number. If $a \not \equiv 0$ mod p then for all integers x and y, $ax \equiv ay$ mod p implies $x \equiv y$ mod p.

**Proposition 5.26**
Let $F = a + bT$ be a polynomial, and p be a prime number. If $b \not \equiv 0$ mod p, then there exists a unique root of F, mod p. If $b \equiv 0$ mod p, and $a \not \equiv 0$ mod p, then F has no roots, mod p.

**Theorem 5.28**
If A and B are nonzero polynomials mod p, then $deg(AB) = deg(A) + deg(B)$.

**Corollary 5.29**
If A and B are polynomials mod p, then $|AB| = |A| \cdot |B|$.

**Corollary 5.30**
If A and B are polynomials and $B \ne 0$, then $|A| \le |AB|$. Equivalently, $deg(A) \le deg(AB)$.

**Proposition 5.31**
$|A| = 1$ iff there exists a polynomial B such that $A \cdot B \equiv 1$ mod p.

**Ultrametric Triangle Inequality**
If A and B are polynomials mod p, then $|A + B | \le max(|A|, |B|)$.

**Lemma 5.33**
Let B be a nonzero polynomial mod p. Suppose that $Q_1, Q_2$ and $R_1, R_2$ are polynomials, with $|R|_1 < |B|$ and $|R|_2 < |B|$. If $Q_1B + R_1 \equiv Q_2B + R_2$ mod p, then $Q_1 \equiv Q_2$ mod p and $R_1 \equiv R_2$ mod p.

**Lemma 5.34**
If A is a polynomial, then the number of polynomials P mod p satisfying $|P| < |A|$ is equal to $|A|$.

**Theorem 5.35**
If A and B are polynomials, and $B \ne 0$, then there exist polynomials Q, R, such that $A \equiv QB + R$ mod p and $|R| < |B|$.

**Theorem 5.36**
If A is a nonzero polynomial, then A can be decomposed uniquely into irreducible polynomials.

**Proposition 5.37**
If $deg(P) = 1$, then P is irreducible.

**Lemma 5.38**
Suppose that x is a root of a polynomial P, mod p. Then the irreducible polynomial $(T - x)$ is a factor of P.

**Theorem 5.39**
Let P be a nonzero polynomial, mod p. The number of roots of P (mod p) is less than or equal to the degree of P.

**Theorem 5.40**
The number of irreducible polynomials mod p is infinite.

**Theorem 5.41**
Let d be a positive integer. The number of irreducible monic polynomials of degree d, mod p, satisfy the estimate: $|\pi(p;d) - \frac{p^d}{d} | \le 2 \frac{p^{0.5d}}{d}$.

### References
- *Book Title* — Chapter X, Pages Y–152
