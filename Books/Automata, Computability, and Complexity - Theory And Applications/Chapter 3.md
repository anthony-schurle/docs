# Chapter 3: The Big Picture: A Language Hierarchy

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 3.1 Defining The Task: Language Recognition

---

### Key Concepts

- **Decision Problem**: Problem requiring a "yes" or "no" answer.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 3.2 The Power Of Encoding

---

### Key Concepts

- **String Encodings**: $<X>$ denotes the string encoding of object $X$. $<X, Y>$ denotes the single string encoding of the two objects $X$ and $Y$.
- **Reduction**: Given two problems and a program to solve the second, we are able to solve the first. (Casting into decision problems)

### Notable Quotes

- **Example Author**: "The answer is yes and the key is encoding. With an appropriate encoding, other kinds of problems can be recast as the problem of deciding whether a string is in a language."
- **Example Author**: “In each of these examples, we have chosen an encoding that is expressive enough to make it possible to describe all of the instances of the problem we are interested in. But have we chosen a good encoding? Might there be another one? The answer to this second question is yes. And it will turn out that the encoding we choose may have a significant impact on what we can say about the difficulty of solving the original problem.”

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 3.3 A Machine-Based Hierarchy Of Language Classes

---

### Definitions

- **Decidable**: Language $L$ is decidable iff there exists a Turing machine that halts on all inputs, accepts strings that are in $L$, and rejects strings not in $L$.
- **Semidecidable**: Language $L$ is semideciable iff there exists a Turing machine that halts on all inputs, accepts strings that are in $L$, and fails to accept any strings not in $L$.

### Visual Aids

**Language Hierarchy [Diagram]**

![[Screenshot from 2026-09-06 13-46-41.png]]

### Notable Quotes

- **Example Author**: “There exist procedures to answer many useful questions about finite state machines. For example, does an FSM accept some particular string? Is an FSM minimal (i.e., is it the simplest machine that does the job it does)? Are two FSMs identical? A subset of those questions can be answered for pushdown automata. None of them can be answered for Turing machines.”

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 3.4 A Tractability Hierarchy Of Language Classes

---

### Definitions

- **P**: Languages that can be decided in polynomial time.
- **NP**: Languages that can be decided by a nondeterministic machine in polynomial time.
- **PSPACE**: Languages that can be decided in polynomial space.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
