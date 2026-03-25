# Chapter 1: Quantification Logic
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 1.0 Quantifiers
---
### Definitions
- **Universal Quantifier**
  - $\forall x P(x)$ signifies $P(x)$ for all x.
- **Existential Quantifier**
  - $\exists x P(x)$ signifies $P(x)$ for some x.

### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.

### References
- *Book Title* — Chapter X, Pages Y–67

## 1.1 Equivalences Involving Quantifiers
---
### Key Concepts
- **Multiple Quantifiers**:
  - Can be interchanged without effecting logic, if all the same type.

### Definitions
- **Unique Existential Quantifier**
  - $\exists ! x P(x) \equiv \exists x (P(x) \land \neg \exists y (P(y) \land y \ne x))$.
- **Bounded Quantifiers**
  - $\forall x \in A P(x) \equiv \forall x (x \in A \implies P(x))$.
  - $\exists x \in A P(x) \equiv \exists x (x \in A \land P(x))$.
  - $\forall x \in A (P(x) \land Q(x)) \equiv \forall x P(x) \land \forall x Q(x)$.
- **Vacuously True**
  - $\forall x \in A P(x)$ true because $A = \emptyset$.

### Theorems & Proofs
**Quantifier Negation Laws**
$\neg \exists P(x) \equiv \forall x \neg P(x)$.
$\neg \forall x P(x) \equiv \exists \neg P(x)$.

**Subset Equivalence**
$A = B \equiv A \subseteq B \land B \subseteq A$.

### References
- *Book Title* — Chapter X, Pages Y–77

## 1.2 More Operations On Sets
---
### Definitions
- **Indexed Family**
  - Set defined by indexing such as $P = \{p_i | i \in I\}$.
  - I is called the index set.
- **Families Of Sets**
  - Set only containing sets.
- **Power Set**
  - $\mathcal{P}(A) = \{x | x \subseteq A\}$.
- **Family Intersection**
  - $\bigcap F = \{x | \forall A \in F(x \in A)\} = \bigcap_{i \in I}A_i = \{x | \forall i \in I (x \in A_i)\}$ is the intersection of all sets in F.
- **Family Union**
  - $\bigcup F = \{x | \exists A \in F(x \in A)\} = \bigcup_{i \in I}A_i = \{x | \exists i \in I (x \in A_i)\}$ is the union of all sets in F.

### Examples
**Example Title**
**Problem 1:**
Problem Statement.
**Solution:**
a)
$$
F \subseteq \mathcal{P}(A) \equiv \forall x \in F (x \in \mathcal{P}(A)) \equiv \forall x \in F(x \subseteq A) \equiv \forall x \in F \forall y \in x (y \in A)
$$

b)
$$
A \subseteq \{2n + 1 | n \in \mathbb{N}\} \equiv \forall x \in A(x \in \{2n + 1 | n \in \mathbb{N}\}) \equiv \forall x \in A \exists n \in \mathbb{N}(x = 2n + 1)
$$
...
### References
- *Book Title* — Chapter X, Pages Y–88
