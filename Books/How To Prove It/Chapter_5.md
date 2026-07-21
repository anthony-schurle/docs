# Chapter #: Mathematical Induction
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 5.0 Proof By Mathematical Induction
---
### Formulas
**Prove $\forall n \in \mathbb{N} (n_0 \le n \implies P(n))$**
Prove $P(n_0)$ and $\forall n \ge n_0 \in \mathbb{N} (P(n) \implies P(n+1))$.

### References
- *Book Title* — Chapter X, Pages Y–280


## 5.1 More Examples
---
### Key Concepts
- **Expanded Induction**:
  - Lots of problems have statements following the form of induction subtly.

### References
- *Book Title* — Chapter X, Pages Y–293


## 5.2 Recursion
---
### Definitions
- **Recursive Definition**
  - Define a function with domain $\mathbb{N}$ in terms of $f(0)$ and $f(n+1)$.
  - Summation, factorials, and exponentiation can all be defined this way.

### References
- *Book Title* — Chapter X, Pages Y–303


## 5.3 Strong Induction
---
### Definitions
- **Strong Recursive Definition**
  - Define a function with domain $\mathbb{N}$ in terms of base cases and $f(n+1)$, which uses multiple past values.
  - Fibonacci numbers take this form.

### Theorems & Proofs
**Theorem 6.4.1**
$\forall n, m \in \mathbb{N}$, if $m > 0$ then $\exists q, r \in \mathbb{N} (n = qm + r \land r < m)$.

**Theorem 6.4.2**
Every integer $n > 1$ is either prime or a product of two or more primes.

**Theorem 6.4.4 (Well-ordering Principle)**
Every nonempty set of natural numbers has a smallest element.

**Theorem 6.4.5**
$\sqrt{2}$ is irrational.

### Formulas
**Prove $\forall n \in \mathbb{N} P(n)$**
Prove $\forall n \in \mathbb{N} (\forall k < n P(k) \implies P(n))$.

### References
- *Book Title* — Chapter X, Pages Y–316


## 5.4 Closures Again
---
### Theorems & Proofs
**Theorem 6.5.1**
Suppose $f : A \to A$ and $B \subseteq A$. Let the sets $B_0, B_1, B_2, ...$ be defined recursively as follows: $B_0 = B$; $\forall n \in \mathbb{N} (B_{n+1} = f(B_n))$. Then the closure of B under $f$ is the set $\bigcup_{n \in \mathbb{N}}B_n$.

**Theorem 6.5.2**
$\forall a, b \in \mathbb{Z}_+ [(2^b - 1) \cdot \sum_{k=0}^{a-1}2^{kb} = 2^{ab}-1]$.

### References
- *Book Title* — Chapter X, Pages Y–323
