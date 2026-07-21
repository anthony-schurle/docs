# Chapter 6: Modular Dynamics
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 6.0 Modular Dynamics
---
### Definitions
- **Totient**
  - Let m be a positive integer and $\Phi(m)$ the set of numbers between 0 and $m-1$ which are coprime with m. The totient of m is the number $\phi(m)$ of elements in the set $\Phi(m)$.
- **FLT**
  - Property of all prime numbers implied by Fermat-Euler Theorem.
  - If $a \ne 0 \mod p$, then $a^{p-1} \equiv 1 \mod p$.
- **Witness**
  - a witnesses the nonprimality of p in FLT when $a \not \equiv 0 \mod p$ and  $a^{p-1} \ne 1 \mod p$.
  - Called perceptive when checked for both FLT and ROO.
- **Carmichael Number**
  - Composite number N which satisfies $GCD(a, N) = 1$ implies $a^{N-1} \equiv 1 \mod N$.
  - Hard to find a witness for.
- **Cycles in Multiplication**
  - If $GCD(a, p) = 1$ for prime p, cycle length $l(a)$ is the length of the cycle of powers of a.
  - If $GCD(a, p) = 1$ for prime p, cycle number $c(a)$ is the number of cycles obtained in the dynamics of multiplication by $a \mod p$, amongst the numbers $\Phi(p) = \{1, ..., p-1\}$. We know $l(a) c(a) = p - 1$.
- **Primitive Root**
  - a is a primitive root if $l(a) = p -1$ for prime p.

### Theorems & Proofs
**Proposition 6.2**
Let m be a positive integer and a an integer. Then the dynamics of addition of a, mod m, consist of $\frac{m}{l}$ cycles of length l, where cycle length is $l = \frac{m}{GCD(a, m)}$.

**Corollary 6.3**
Proposition 6.2 with $GCD(a, m) = 1$.

**Proposition 6.6**
A positive integer p is prime iff $\phi(p) = p -1$.

**Proposition 6.7**
Given an integer a between 0 and $m-1$, we have $a \in \Phi(m)$ iff multiplication by a, mod m, is reversible.

**Proposition 6.8**
If $a \in \Phi(m)$ and $b \in \Phi(m)$, then there exists $c \in \Phi(m)$ such that $a \cdot b \equiv c$ mod m.

**Lemma 6.9**
Let m be a positive integer, and suppose that $GCD(a, m) = 1$. Then the dynamics of multiplication by a, mod m, within $\Phi(m)$, consist only of cycles, all of the same length.

**Theorem 6.10 (The Fermat-Euler Theorem)**
Let m be a positive integer. Let a be an integer coprime to m. Then $a^{\phi(m)} \equiv 1 \mod m$. *Fermat's Little Theorem* is the specific case when m is prime.

**Corollary 6.14**
Let m be a positive integer, and a an integer coprime to m. Let x and y be natural numbers. Then $x \equiv y \mod \phi(m)$ implies $a^x \equiv a^y \mod m$.

**Proposition 6.20**
Pingala's algorithm for computing $a^e \mod m$ requires at most $2\lfloor log_2(e)\rfloor$ multiplications, each modulo m.

**Proposition 6.21**
Let be a prime number. Then (ROO) $x^2 \equiv 1 \mod p$ implies $x \equiv \pm 1 \mod p$.

**Proposition 6.22**
If $N < 25,326,001$, and N is not prime, then either 2, 3, or 5 will witness the nonprimality of N via the Miller-Rabin test.

**Lemma 6.23**
Let $\lambda$ be a positive integer. Then the number of elements of $\Phi(p)$ of cycle length $\lambda$ is either 0 or $\phi(\lambda)$.

**Lemma 6.24 (Totient Sum Formula)**
Let N be a positive integer. Then the sum of the totients of the divisors of N equals N itself.

**Theorem 6.26**
If p is a prime number, then there exists a primitive root mod p. Their number is $\phi(p - 1)$.

### Visual Aids

![[Screenshot from 2026-04-08 10-08-01.png]]

**Pingala's Algorithm**
![[Screenshot from 2026-05-03 23-06-22.png]]

**Miller-Rabin Primality Test**
![[Screenshot from 2026-05-03 23-23-07.png]]

**Diffie-Hellman Protocol**
![[Screenshot from 2026-05-04 00-51-53.png]]

![[Screenshot from 2026-05-04 00-52-31.png]]

![[Screenshot from 2026-05-04 00-52-54.png]]

![[Screenshot from 2026-05-04 00-53-19.png]]

Requires Discrete logarithm problem to solve.

### References
- *Book Title* — Chapter X, Pages Y–172
