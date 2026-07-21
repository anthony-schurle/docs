# Chapter 7: Infinite Sets
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## 7.0 Equinumerous Sets
---
### Definitions
- **Equinumerous**
  - Suppose A and B are sets. If there is a function $f : A \to B$ that is one-to-one and onto, then A is equinumerous to B. Denoted A~B.
- **Finite & Infinite**
  - $\forall n \in \mathbb{N}$, let $I_n = \{i \in \mathbb{Z}^+ | i \le n \}$. 
  - Set A is finite if $\exists n \in \mathbb{N}$ such that $I_n$ ~ A.
  - Set A is infinite if not finite.
- **Cardinality**
  - Denoted $|A|$ and is the number of elements of finite set A found by $I_n$.
- **Denumerable**
  - Set A is called denumerable if $\mathbb{Z}^+$ ~ $A$.
- **Countable**
  - Set A is countable if finite or denumerable.
  - Else, called uncountable.

### Theorems & Proofs
**Theorem 8.1.2**
Suppose A ~ B and C ~ D. Then:
1. $A \times C$ ~ $B \times D$.
2. If A and C are disjoint and B and R are disjoint, then $A \cup C$ ~ $B \cup D$.

**Theorem 8.1.3**
Equinumerous is an equivalence relation.

**Theorem 8.1.5**
Suppose A is a set. Then the following statements are equivalent:
1. A is countable.
2. Either $A = \emptyset$ or there is a function $f : \mathbb{Z}^+ \to A$ that is onto.
3. There is a function $f : A \to \mathbb{Z}^+$ that is one-to-one.

**Theorem 8.1.6**
$\mathbb{Q}$ is denumerable.

**Theorem 8.1.7**
Suppose A and B are disjoint finite sets. Then $A \cup B$ is finite, and $|A \cup B| = |A| + |B|$.

### References
- *Book Title* — Chapter X, Pages Y–381


## 7.1 Countable And Uncountable Sets
---
### Definitions
- **Finite Sequence**
  - Suppose A is a set. Function $f : I_n \to A$ is called a finite sequence of elements of $A$ with length $n$.

### Theorems & Proofs
**Theorem 8.2.1.**
Suppose A and B are countable sets. Then:
1. $A \times B$ is countable.
2. $A \cup B$ is countable.

**Theorem 8.2.2.**
The union of countably many countable sets is also countable.

**Theorem 8.2.4.**
Suppose A is a countable set. Then the set of all finite sequences of elements of A is also countable.

**Theorem 8.2.5. (Cantor's Theorem)**
$\mathcal{P}(\mathbb{Z}^+)$ is uncountable.

**Theorem 8.2.6.**
$\mathbb{R}$ is uncountable.

### References
- *Book Title* — Chapter X, Pages Y–389


## 7.2 The Cantor-Schroder-Bernstein Theorem
---
### Definitions
- **Dominates**
  - Suppose A and B are sets.
  - B dominates A, denoted $A \preceq B$, if $\exists f : A \to B$ that is injective.
  - If $A \preceq B$ and $A \not \sim B$, then B strictly dominates A and is denoted $A \prec B$.

### Theorems & Proofs
**Theorem 8.3.2. (Cantor-Schroder-Bernstein Theorem)**
Suppose A and B are sets. If $A \preceq B$ and $B \preceq A$, then $A \sim B$.

**Theorem 8.3.3.**
$\mathbb{R} \sim \mathcal{P}(\mathbb{Z}^+)$.

**Lemma 8.3.4**
Suppose x and y are real numbers and $x < y$. Then there is a rational number q such that $x < q < y$.

### References
- *Book Title* — Chapter X, Pages Y–394
