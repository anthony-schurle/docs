# Chapter 7: Assembling The Modular Worlds
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## #.# Subsection Title
---
### Key Concepts
- **Chinese Remainder Theorem**:
  - Can be used to determine $x \in \Phi(N)$ for any x by $xy \equiv 1 \mod N$.
### Definitions
- **Bracket Notation**
  - $N \equiv [x_1, x_2, ..., x_n] \mod [y_1, y_2, ..., y_n]$ represents $N \equiv x_i \mod y_i$ for all i.
- **Descends**
  - If $m | n$, then $x \equiv a \mod n$ descends to $x \equiv a \mod m$.
- **Lifts**
  - $m | n \land x \equiv b \mod m \implies x \equiv b \lor b + m \lor b + (\frac{n}{m} - 1)m \mod n$.
- **Square Root**
  - Square root of a is a solution to $x^2 \equiv a \mod m$.

### Theorems & Proofs
**Theorem 7.2 (Chinese Remainder Theorem)**
Suppose that d and e are coprime positive integers. There is a one-to-one correspondence between
- the set of pairs $[a, b]$ with $0 \le a < d$ and $0 \le b < e$;
- the set of numbers N with $0 \le N < de$;
such that the solutions to $x \equiv [a, b] \mod [d, e]$ are the same as the solutions to $x \equiv N \mod de$.

**Proposition 7.5**
Suppose that d and e are coprime positive integers. Then the solutions to the congruence $x^2 \equiv a \mod de$ are in one-to-one correspondence with pairs of solutions (u, v) to the congruence $u^2 \equiv a \mod d$ and $v^2 \equiv a \mod e$.

**Corollary 7.6**
Suppose that d and e are coprime positive integers. A number a is a square, modulo $de$, iff a is a square modulo d and a is a square modulo e.

**Corollary 7.7**
Let m be a positive integer with at least 2 distinct odd prime factors. Then there are at least 4 solutions to the congruence $x^2 \equiv 1 \mod m$.

**Theorem 7.9**
Let d and e be positive coprime integers. Then $\phi(de) = \phi(d)\phi(e)$.

**Proposition 7.10**
Let p be a prime number, and let e be a positive integer. Then $\phi(p^e) = p^e - p^{e-1}$.

**Lemma 7.16**
Suppose that $xy \equiv 1 \mod p^e$. Let r be the integer satisfying $xy = 1 +rp^e$. Define $z = y - yrp^e$. Then $xz \equiv 1 \mod p^{2e}$.

**Lemma 7.18**
Let p be a prime number and e a positive integer. The square roots of 1, modulo $p^e$ are,
$$
\begin{cases} 1 & if, p=2 \land e=1 \\ 1 \lor p^e - 1 & \text{p is an odd prime} \\ 1 \lor 3 & if, p = 2 \land e = 2 \\ 1 \lor p^{e-1} - 1 \lor p^{e-1} + 1 \lor p^e - 1 & if, p=2 \land e \ge 3\end{cases}
$$

**Proposition 7.19**
Suppose that p is a prime and $GCD(a, p) = 1$. If a has a square root modulo $p^e$, then the number of square roots of a equals the number of square roots of 1: either 1, 2, or 4.

**Theorem 7.20**
Suppose that p is an odd prime, $e \ge 1$, $GCD(a, p) = 1$, and $x^2 \equiv a \mod p^e$. Let r be the integer for which $x^2 = a + rp^e$. Let b be a multiplicative inverse of $2x$, modulo $p^e$. Define $z = x - brp^e$. Then $z^2 \equiv a \mod p^{2e}$.

**Corollary 7.21**
Suppose that p is an odd prime and $GCD(a, p) = 1$. Then a is a square root modulo p iff a is a square modulo every power of p.

**Proposition 7.22**
Suppose that $e \ge 3$, a is odd, and $x^2 \equiv a \mod 2^e$. Then either $x^2 \equiv a \mod 2^{e+1}$ or $(x + 2^{e-1})^2 \equiv a \mod 2^{e+1}$.

**Corollary 7.23**
Let a be an odd number. Then $a \equiv 1 \mod 8$ iff a is a square modulo 8, 16, 32, 64, ... .

### References
- *Book Title* — Chapter X, Pages Y–191