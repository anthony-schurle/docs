# Chapter 0: Sentential Logic
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## 0.0 Deductive Reasoning And Logical Connectives
---
### Key Concepts
- **Deductive Reasoning**:
  - Conclusion forced from true premises.
### Definitions
- **Valid Argument**
  - Conclusion must be true if the premises are true. 

### Visual Aids
**Connective Symbols**

| Symbol  | Meaning           |
| ------- | ----------------- |
| $\lor$  | or (disjunction)  |
| $\land$ | and (conjunction) |
| $\neg$  | not (negation)    |

### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.

### Common Pitfalls
- Logical symbol to english word translation is not one-to-one always

### References
- *Book Title* — Chapter X, Pages Y–14


## 0.1 Truth Tables
---
### Definitions
- **Truth Value**
  - True or false label given to a statement.
  - Every statement has $n!$ different combinations of truth values assigned to its variables.
- **Equivalent Formulas**
  - Same truth table, truth value composition.
- **Tautologies**
  - Formulas that are always true.
- **Contradictions**
  - Formulas that are always false.

### Visual Aids
| P   | Q   | $P \land Q$ |
| --- | --- | ----------- |
| F   | F   | F           |
| F   | T   | F           |
| T   | F   | F           |
| T   | T   | T           |

| P   | $\neg P$ |
| --- | -------- |
| F   | T        |
| T   | F        |

| P   | Q   | $P \lor Q$ |
| --- | --- | ---------- |
| F   | F   | F          |
| F   | T   | T          |
| T   | F   | T          |
| T   | T   | T          |

![[Screenshot from 2026-02-07 11-43-53.png]]

![[Screenshot from 2026-02-07 12-27-49.png]]

### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.

### References
- *Book Title* — Chapter X, Pages Y–26


## 0.2 Variables And Sets
---
### Definitions
- **Variable**
  - Stands for a value.
  - $P(x)$ notates that P stands for variable x, up to arbitrary variable count.
- **Truth Sets**
  - Defines truth for variable dependent statements by set membership.
- **Set**
  - Collection of objects, called elements.
  - Unordered with no sense of multiplicity.
  - Elementhood test determines which elements reside in a set.
  - Free variables tested in elementhood whereas bound variables describe the set.
  - Empty set denoted $\emptyset$.
- **Universe Of Discourse**
  - Set of all possible values for variables.

### Visual Aids
**Standard Sets**

| Set Name     | Set Membership   |
| ------------ | ---------------- |
| $\mathbb{R}$ | Real numbers     |
| $\mathbb{Q}$ | Rational numbers |
| $\mathbb{Z}$ | Integers         |
| $\mathbb{N}$ | Natural Numbers  |

### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.

### References
- *Book Title* — Chapter X, Pages X-35


## 0.3 Operations On Sets
---
### Key Concepts
- **Operations On Sets**:
  - $A \cap B$ denotes $\{x | x \in A \land x \in B\}$ (intersection).
  - $A \cup B$ denotes $\{x | x \in A \lor x \in B\}$ (union).
  - $A \backslash B$ denotes $\{x | x \in A \land x \not \in B\}$ (difference).
  - $A \Delta B$ denotes $(A \backslash B) \cup (B \backslash A)$ (symmetric difference).

### Definitions
- **Subset**
  - $A \subseteq B$ if every element of A is in B.
- **Disjoint**
  - $A \cap B = \emptyset$.

### Theorems & Proofs
**Set Distributive Laws**
$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$.
$A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$.

**Theorem 1.4.7**
For any sets A and B, $(A \cup B) \backslash B \subseteq A$.

### Visual Aids
**Venn Diagram**
![[Screenshot from 2026-03-17 00-25-30.png]]

### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.

### References
- *Book Title* — Chapter X, Pages Y–45
  
## 0.4 The Conditional And Biconditional Connectives
---
### Key Concepts
- **English Expressions For Conditional**:
  - P implies Q.
  - Q, if P.
  - P only if Q.
  - P is sufficient for Q.
  - Q is necessary for P.

### Definitions
- **Converse**
  - $Q \implies P$ is converse to $P \implies Q$.
- **Contrapositive**
  - $\neg Q \implies \neg P$ is contrapositive to $P \implies Q$.
  - Equivalent to conditional.

### Visual Aids
**Conditional**

| P   | Q   | $P \implies Q$ | $\neg P \lor Q$ |
| --- | --- | -------------- | --------------- |
| F   | F   | T              | T               |
| F   | T   | T              | T               |
| T   | F   | F              | F               |
| T   | T   | T              | T               |

**Biconditional**

| P   | Q   | $P \iff Q$ |
| --- | --- | ---------- |
| F   | F   | T          |
| F   | T   | F          |
| T   | F   | F          |
| T   | T   | T          |

### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.

### References
- *Book Title* — Chapter X, Pages Y–57
