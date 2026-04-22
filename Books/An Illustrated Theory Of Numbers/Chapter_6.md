# Chapter 6: Modular Dynamics
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 6.0 Modular Dynamics
---
### Key Concepts
- **Concept Name**:
  - Subpoint or clarification.
### Definitions
- **Totient**
  - Let m be a positive integer and $\Phi(m)$ the set of numbers between 0 and $m-1$ which are coprime with m. The totient of m is the number $\phi(m)$ of elements in the set $\Phi(m)$.

### Algorithms
**Algorithm Name**
Description.
```pseudo
1. Step 1
2. Step 2
3. Step 3
```
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

### Visual Aids

![[Screenshot from 2026-04-08 10-08-01.png]]


### References
- *Book Title* — Chapter X, Pages Y–172
