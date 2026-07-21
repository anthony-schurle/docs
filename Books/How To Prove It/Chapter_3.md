# Chapter 3: Relations
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 3.0 Ordered Pairs And Cartesian Products
---
### Definitions
- **Ordered Pair**
  - $(a, b)$ with first coordinate a.
- **Cartesian Product**
  - $A \times B = \{(a, b) | a \in A \land b \in B\}$.
- **Truth Set**
  - Subset of cartesian product which make a statement true.

### Theorems & Proofs
**Theorem 4.1.3**
Suppose A, B, C, and D are sets.
a) $A \times (B \cap C) = (A \times B) \cap (A \times C)$.
b) $A \times (B \cup C) = (A \times B) \cup (A \times C)$.
c) $(A \times B) \cap (C \times D) = (A \cap C) \times (B \cap D)$.
d) $(A \times B) \cup (C \times D) \subseteq (A \cup C) \times (B \cup D)$.
e) $A \times \emptyset = \emptyset \times A = \emptyset$.

### References
- *Book Title* — Chapter X, Pages Y–181


## 3.1 Relations
---
### Definitions
- **Relation**
  - $R \subseteq A \times B$ is a relation from A to B.
- **Domain**
  - $Dom(R) = \{a \in A | \exists b \in B((a, b) \in R)\}$.
- **Range**
  - $Ran(R) = \{b \in B | \exists a \in A((a, b) \in R)\}$.
- **Inverse**
  - $R^{-1} = \{(b,a) \in B \times A | (a, b) \in R\}$.
- **Composition**
  - $S \circ R = \{(a, c) \in A \times C | \exists b \in B((a,b) \in R) \land (b,c) \in S\}$.

### Theorems & Proofs
**Theorem 4.2.5**
Suppose R is a relation from A to B, S is a relation from B to C, and T is a relation from C to D. Then:
a) $(R^{-1})^{-1} = R$.
b) $Dom(R^{-1}) = Ran(R)$.
c) $Ran(R^{-1}) = Dom(R)$.
d) $T \circ (S \circ R) = (T \circ S) \circ R$.
e) $(S \circ R)^{-1} = R^{-1} \circ S^{-1}$.

### References
- *Book Title* — Chapter X, Pages Y–190


## 3.2 More About Relations
---
### Definitions
- **Related**
  - a related to b by relation R denoted $aRb$.
- **Binary Relation**
  - R is a relation on A iff $R \subseteq A \times A$.
  - Identity relation is $i_A = \{(x, x) | x \in A\}$.
- **Reflexive**
  - R is reflexive on A if $\forall x \in A (xRx)$.
- **Symmetric**
  - R is symmetric if $\forall x \in A \forall y \in A (xRy \implies yRx)$.
- **Transitive**
  - R is transitive if $\forall x \in A \forall y \in A \forall z \in A ((xRy \land yRz) \implies xRz)$.

### Theorems & Proofs
**Theorem 4.3.4**
Suppose R is a relation on a set A.
a) R is reflexive iff $i_A \subseteq R$, where $i_A$ is the identity relation on A.
b) R is symmetric iff $R = R^{-1}$.
c) R is transitive iff $R \circ R \subseteq R$.

### References
- *Book Title* — Chapter X, Pages Y–200


## 3.3 Ordering Relations
---
### Definitions
- **Antisymmetric**
  - Suppose R is a relation on a set A. Then R is antisymmetric if $\forall x \in A \forall y \in A ((xRy \land yRx) \implies x = y)$.
- **Order**
  - Suppose R is a relation on a set A. R is a partial order on A if it is reflexive, transitive, and antisymmetric.
  - R is a total order on A if it is a partial order and $\forall x \in A \forall y \in A (xRy \lor yRx)$.
  - Sometimes symbols used instead of letters to identity the relation, such as $\ge$.
- **R-Smallest**
  - Suppose R is a partial order on set A, $B \subseteq A$, and $b \in B$. b is called R-smallest element of B if $\forall x \in B (bRx)$.
  - When comparing smallest subsets with a desired property, it is implicit this is the smallest with relation $\{(X, Y) \in \mathcal{P}(A) \times \mathcal{P}(A) | X \subseteq Y\}$.
- **R-Minimal**
  - Suppose R is a partial order on set A, $B \subseteq A$, and $b \in B$. Then b is called R-minimal if $\neg \exists x \in B (xRb \land x \ne b)$.
- **R-Largest**
  - Suppose R is a partial order on A, $B \subseteq A$, and $b \in B$. b is called R-largest of B if $\forall x \in B (xRb)$.
- **R-Maximal**
  - Suppose R is a partial order on A, $B \subseteq A$, and $b \in B$. b is called R-maximal of B if $\neg \exists x \in B (bRx \land b \ne x)$.
- **Bounds**
  - Suppose R is a partial order on A, $B \subseteq A$, and $a \in A$.
  - a is called a lower bound for B if $\forall x \in B (aRx)$.
  - a is called an upper bound for B if $\forall x \in B (xRa)$.
- **Least Upper Bound (l.u.b.)**
  - Suppose R is a partial order on A and $B \subseteq A$. Let U be the set of all upper bounds for B.
  - If U has a smallest element, then this element is called the least upper bound on B.
- **Greatest Lower Bound (g.l.b.)**
  - Suppose R is a partial order on A and $B \subseteq A$. Let L be the set of all lower bounds.
  - If L has a largest element, it is called the greatest lower bound on B.

### Theorems & Proofs
**Theorem 4.4.6**
Suppose R is a partial order on a set A, and $B \subseteq A$.
a) If B has a smallest element, then this smallest element is unique.
b) Suppose b is the smallest element of B. Then b is also a minimal element of B, and it is the only minimal element.
c) If R is a total order and b is a minimal element of B, then b is the smallest element of B.

**Theorem 4.4.11**
Suppose A is a set, $F \subseteq \mathcal{P}(A)$, and $F \ne \emptyset$. Then the least upper bound of F (in the subset partial order) is $\bigcup F$ and the greatest lower bound of F is $\bigcap F$.

### References
- *Book Title* — Chapter X, Pages Y–215


## 3.4 Equivalence Relations
---
### Definitions
- **Equivalence Relation**
  - Suppose R is a relation on a set A. R is an equivalence relation if it is reflexive, symmetric, and transitive.
- **Pairwise Disjoint**
  - F is pairwise disjoint if $\forall X \in F \forall Y \in F (X \ne Y \implies X \cap Y = \emptyset)$. 
- **Partition**
  - Suppose A is a set and $F \subseteq \mathcal{P}(A)$. F is a partition of A if:
  - $\bigcup F = A$.
  - F is pairwise disjoint.
  - $\forall X \in F (X \ne \emptyset)$.
- **Equivalence Class**
  - Suppose R is an equivalence relation on a set A, and $x \in A$. The equivalence class of x with respect to R is $[x]_R = \{y \in A | yRx\}$.
  - A modulo R denoted $A / R = \{[x]_R | x \in A\}$.
- **Congruent**
  - Suppose m is a positive integers. For any integers x and y, x is congruent to y modulo m if $m | (x - y)$. Denoted $x \equiv y \mod m$.

### Theorems & Proofs
**Theorem 4.5.4**
Suppose R is an equivalence relation on a set A. Then $A / R$ is a partition of A.

**Lemma 4.5.5**
Suppose R is an equivalence relation on A. Then:
1. $\forall x \in A (x \in [x])$.
2. $\forall x \in A \forall y \in A (y \in [x] \iff [y] = [x])$.

**Theorem 4.5.6**
Suppose A is a set and F is a partition of A. Then there is an equivalence relation R on A such that $A / R = F$.

**Lemma 4.5.7**
Suppose A is a set and F is a partition of A. Let $R = \bigcup_{X \in F}(X \times X)$. Then R is an equivalence relation on A. We call R the equivalence relation determined by F.

**Lemma 4.5.8**
Suppose A is a set and F is a partition of A. Let R be the equivalence relation determined by F. Suppose $X \in F$ and $x \in X$. Then $[x]_R = X$.

**Theorem 4.5.10**
For every positive integer $m$, $\equiv_m$ is an equivalence relation on $\mathbb{Z}$.

### References
- *Book Title* — Chapter X, Pages Y–228
