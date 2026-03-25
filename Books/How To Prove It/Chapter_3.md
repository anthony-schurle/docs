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

### Examples
**Example Title**
**Problem 1:**
What are the truth sets of the following statements? List a few elements of each truth set.
a) "x is a parent of y", where x and y both range over the set P of all people.
**Solution:**
a)
$\{(x, y) \in P^2 | \text{x is a parent of y}\}$.

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

### Examples
**Example Title**
**Problem 1:**
Find the domains and ranges of the following relations.
a) $\{(p, q) \in P^2 | \text{the person p is a parent of the person q}\}$, where P is the set of all living people.
b) $\{(x, y) \in \mathbb{R}^2 | y > x^2\}$.
**Solution:**
a)
Domain -
$\{p \in P | \text{p is a parent of someone}\}$.
Range -
$\{q \in P | \text{q has some parent}\}$.

b)
Domain -
$\{x \in \mathbb{R} | \exists y (y > x^2)\}$.
Range -
$\{y \in \mathbb{R} | \exists x (y > x^2)\}$.

**Problem 2:**
Find the domains and ranges of the following relations.
a) $\{(p, q) \in P^2 | \text{the person p is a brother of the person q}\}$, where P is the set of all living people.
b) $\{(x, y) \in \mathbb{R}^2 | y^2 = 1 - \frac{2}{x^2 + 1}\}$.
**Solution:**
a)
Domain -
$\{p \in P | \text{p is the brother of some person}\}$.
Range -
$\{q \in P | \text{q has some brother} \}$.

b)
Domain -
$\{x \in \mathbb{R} | \exists y (y^2 = 1 - \frac{2}{x^2 + 1})\}$.
Range -
$\{y \in \mathbb{R} | \exists x (y^2 = 1 - \frac{2}{x^2 + 1})\}$.

**Problem 3:**
Let $L = \{(s, r) \in S \times R | \text{the student s lives in the dorm room r}\}$ and $E = \{(s, c) \in S \times C \ \text{the student s is enrolled in the course c}\}$ where S is the set of all students at a school, R is the set of all dorm rooms, and C is the set of all courses.
Describe the following relations:
a) $L^{-1} \circ L$.
b) $E \circ (L^{-1} \circ L)$.
**Solution:**
a)
This is a S to S relation defined by $\{(s, t) \in S^2 | \exists c \in R ((s, c) \in L \land (c, t) \in L^{-1})\} = \{(s, t) \in S^2 | \exists c \in R ((s, c) \in L \land (t, c) \in L)\}$. In other words, student s is related to student c iff both live in the same dorm room.
b)

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

### Examples
**Example Title**
**Problem 1:**
Problem Statement.
**Solution:**
Solution Statement.

### References
- *Book Title* — Chapter X, Pages Y–200


## 3.3 Ordering Relations
---
### Key Concepts
- **Concept Name**:
  - Subpoint or clarification.
### Definitions
- **Antisymmetric**
  - Suppose R is a relation on a set A. Then R is antisymmetric if $\forall x \in A \forall y \in A ((xRy \land yRx) \implies x = y)$.
- **Order**
  - Suppose R is a relation on a set A. R is a partial order on A if it is reflexive, transitive, and antisymmetric.
  - R is a total order on A if it is a partial order and $\forall x \in A \forall y \in A (xRy \lor yRx)$.
### Algorithms
**Algorithm Name**
Description.
```pseudo
1. Step 1
2. Step 2
3. Step 3
```
### Code Snippets
**Snippet Name**
Description.
```program
// code
```
### Theorems & Proofs
**Theorem Name**
Proof.
### Formulas
**Formula Name**
Description.
$$
Equation
$$
### Visual Aids
| Header | Header |
| - | - |
| Content | Content |
![Diagram]()
### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.
### Notable Quotes
> “Notable quote."
### Common Pitfalls
- Pitfall 1.
### Related Links
- [Link]()
### References
- *Book Title* — Chapter X, Pages Y–Z

- [Author(s), "Paper or Article Title," Journal or Conference Name, Year]() 

- [Related Chapter in This Wiki]()  

- [Official Specification or Standard Document (PDF/URL)]()  

- Class Lecture ([Link]())
