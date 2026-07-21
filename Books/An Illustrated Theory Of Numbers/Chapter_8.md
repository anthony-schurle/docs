# Chapter 8: Quadratic Residues
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## #.# Subsection Title
---
### Definitions
- **Squares (Quadratic Residues)**
  - For mod p, its squares are $0^2, 1^2, ..., (p-1)^2 \mod p$.
- **Partners**
  - Let p be prime and $a, x, y \in \Phi(p)$. x and y are a-partners if $xy \equiv a \mod p$.
- **Legendre Symbol**
  - Let p be an odd prime and a an integer. A legendre symbol is:
  - $\frac{a}{p} = \begin{cases} 1 & \text{if a is a nonzero square mod p} \\ 0 & if, a \equiv 0 \mod p \\ -1 & \text{if a is nonsquare mod p} \end{cases}$.
  - Euler's criterion tells us $\frac{a}{p} = a^{0.5(p-1)} \mod p$.
  - $(\frac{ab}{p}) = (\frac{a}{p})(\frac{b}{p})$.
- **Permutation**
  - Bijection from a set to itself.
  - Graphs are cycles.
  - Transposition is a special case that only switches two elements.
  - Adjacent transposition is a transposition that switches consecutive numbers.
- **Permutation Sign**
  - Cycle of length l has sign $(-1)^{l+1}$.
  - Sign of permutation is the product of signs of its cycles.
- **Inversion**
  - Let S be a set of numbers and f a permutation. An inversion of f is an ordered pair (s, t) in S such that $s < t$ and $f(s) > f(t)$.
  - $Inv(f)$ denotes the number of inversions of a permutation.

### Theorems & Proofs
**Theorem 8.2 (Wilson's Theorem)**
If p is a prime number, then $(p-1)! \equiv -1 \mod p$.

**Proposition 8.3**
Let p be an odd prime number. Then among the set $\Phi(p)$, half the number are squares mod p and half are non-squares.

**Theorem 8.5 (Euler's Criterion)**
Let p be an odd prime number, and let a be an integer coprime to p. Then,
- a is square mod p, iff $a^{0.5(p-1)} \equiv 1 \mod p$.
- a is nonsquare mod p, iff $a^{0.5(p-1)} \equiv -1 \mod p$.

**Corollary 8.6**
Let p be an odd prime. Then $-1$ is a square mod p, iff $p \equiv 1 \mod 4$. (Even subproduct is square root of -1 modulo p)

**Theorem 8.7 (Fermat's Christmas Theorem)**
Let p be a prime number with $p \equiv 1 \mod 4$. Then the Diophantine equation $x^2 + y^2 = p$ has a solution. In other words, p can be expressed as the sum of two squares.

**Proposition 8.8**
Consider a grid of parallelograms in the plane, with the origin at a grid-point, and a circle centered at the origin. If the area of the circle is greater than 4 times the area of a parralelogram, then the circle contains a grid-point besides the origin.

**Theorem 8.10**
When p is an odd prime number, 
$$
(\frac{2}{p}) = \begin{cases} 1 & if, p \equiv 1 \lor 7 \mod 8 \\ -1 & if, p \equiv 3 \lor 5 \mod 8 \end{cases}
$$

**Proposition 8.12**
Every permutation may be constructed by composing transpositions.

**Lemma 8.13**
Let f be a permutation of a finite set S. Let g be a transposition of the set S. Then $sgn(g \circ f) = -sgn(f)$.

**Theorem 8.14**
Suppose that f is a permutation of a finite set S. If f can be constructed by composing n transpositions, then $sgn(f) = (-1)^n$.

**Lemma 8.18**
Let f be a permutation of $\{1, 2, ..., n\}$. Let g be an adjacent transposition of S. Then $Inv(g \circ f) = Inv(f) \pm 1$.

**Theorem 8.19**
Let f be a permutation of a finite set S of numbers. Then $sgn(f) = (-1)^{Inv(f)}$.

**Proposition 8.20**
For every integer a, $sgn(add(a \mod p)) = 1$ for odd prime p.

**Lemma 8.21 (Zolotarev's Lemma)**
Let p be an odd prime number, and suppose $GCD(a, p) = 1$. Then $(\frac{a}{p})$ equals the sign of $mult(a \mod p)$.

**Theorem 8.22 (Quadratic Reciprocity)**
If p and q are distinct odd primes, then $(\frac{p}{q})(\frac{q}{p}) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}$.
So, $(\frac{p}{q})(\frac{q}{p}) = \begin{cases} -1 & if, p \equiv 3 \land q \equiv 3 \mod 4 \\ 1 & \text{otherwise} \end{cases}$.

### References
- *Book Title* — Chapter X, Pages Y–