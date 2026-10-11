# Chapter 8: Regular And Nonregular Languages

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 8.1 How Many Regular Languages Are There

---

### Results & Proofs

**Theorem: The Regular Languages Are Countably Infinite**
There is a countably infinite number of regular languages.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 8.2 Showing That A Language Is Regular

---

### Results & Proofs

**Theorem: Finite Languages Are Regular**
Every finite language is regular.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 8.3 Some Important Closure Properties Of Regular Languages

---

### Results & Proofs

**Theorem: Regular Language Trivial Closure**
The regular languages are closed under union, concatenation, and Kleene Star.

**Theorem: Regular Language Non-trivial Closure**
The regular languages are closed under complement, intersection, difference, reverse, and letter substitution.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 8.4 Showing That A Language Is Not Regular

---

### Results & Proofs

**Theorem: Long Strings Force Repeated States**
Let $M = (K, \Sigma, \delta, s, A)$ be any DFSM. If $M$ accepts any string of length $|K|$ or greater, then that string will force $M$ to visit some state more than once.

**Theorem: The Pumping Theorem**
If $L$ is a regular language, then $\exists k \ge 1 \forall w \in L (|w| \ge k \implies \exists x,y,z (w = xyz \land |xy| \le k \land y \ne \epsilon \land \forall q \ge 0 (xy^qz \in L)))$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
