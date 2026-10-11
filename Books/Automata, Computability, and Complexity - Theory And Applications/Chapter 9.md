# Chapter 9: Algorithms And Decision Procedures For Regular Languages

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 9.1 Fundamental Decision Procedures

---

### Key Concepts

- **Bounded Simulation**: Simulation guaranteed to halt and only finite number of strings needed for analysis.

### Results & Proofs

**Theorem: Membership Decision Procedure**
Given a regular language $L$ and a string $w$, there exists a decision procedure that answers the question, is $w \in L$?

**Theorem: Decidability Of Emptiness**
Given an FSM $M$, there exists a decision procedure that answers the question is $L(M) = \emptyset$?

**Theorem: Decidability Of Totality**
Given an FSM $M$, there exists a decision procedure that answers the question, is $L(M) = \Sigma^*$.

**Theorem: Decidability Of Finiteness**
Given an FSM $M$, there exists a decision procedure that answers the questions, "Is $L(M)$ finite?" and "Is $L(M)$ infinite?".

**Theorem: Decidability Of Equivalence**
Given two FSMs $M_1$ and $M_2$, there exists a decision procedure that answers the question, "Is $L(M_1) = L(M_2)$".

**Theorem: Decidability Of Minimality**
Given a DFSM $M$, there exists a decision procedure that answers the question, "Is $M$ minimal?".

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
