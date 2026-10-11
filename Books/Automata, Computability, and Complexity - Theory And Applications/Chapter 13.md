# Chapter 13: Context-Free And Noncontext-Free Languages

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 13.1 Where Do The Context-Free Languages Fit In The Big Picture?

---

### Results & Proofs

**Theorem: Context-Free Language Hierarchy**
The regular languages are a proper subset of the context-free languages.

**Theorem: Number Of Context-Free Languages**
There is a countably infinite number of context-free languages.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 13.2 Showing That A Language Is Context-Free

---

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 13.3 The Pumping Theorem For Context-Free Languages

---

### Key Concepts

- **Cross Serial Dependency**: Relationship dependencies requiring line crossing in nested languages. Typically not context-free.

### Results & Proofs

**Theorem: Bounded Yield**
The length of the yield of any tree $T$ with height $h$ and branching factor $b$ is $\le b^h$.

**Theorem: Pumping Theorem For Context-Free Languages**
If $L$ is a context-free language, then $\exists k \ge 1 \forall w \in L (|w| \ge k \implies \exists u,v,x,y,z (w = uvxyz, vy \ne \epsilon, |vxy| \le k, \forall q \ge 0 (uv^qxy^qz \in L)))$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 13.4 Some Important Closure Properties Of Context-Free Languages

---

### Algorithms

**Intersect PDA And FSM**
Intersects a PDA language with a DFSM language.
	`intersectPDAandFSM(`$M_1$`: PDA,`$M_2$`: FSM) =`
		1. Set $\Delta_3 = \{\}$.
		2. For each $((q_1, a, \beta), (p_1, \gamma)) \in \Delta_1$ and $((q_2, a), p_2) \in \Delta_2$ do:
			1. Add $(((q_1, q_2), a, \beta), ((p_1, p_2), \gamma))$ to $\Delta_3$.
		3. For each $((q_1, \epsilon, \beta), (p_1, \gamma)) \in \Delta_1$ and $q_2 \in K_2$ do:
			1. Add $(((q_1, q_2), \epsilon, \beta), ((p_1, q_2), \gamma))$ to $\Delta_3$.
		4. Return $(K_1 \times K_2, \Sigma, \Gamma_1, \Delta_3, (s_1, s_2), A_1 \times A_2)$.

### Results & Proofs

**Theorem: Context-Free Closures**
The context-free languages are closed under union, concatenation, Kleene Star, reverse, and letter substitution.

**Theorem: Context-Free Nonclosure**
The context-free languages are not closed under intersection, complement, or difference.

**Theorem: Context-Free Intersection Regular Closure**
The context-free languages are closed under intersection with the regular languages.

**Theorem: Context-Free Difference Regular Closure**
The difference $L_1 - L_2$ between context-free language $L_1$ and regular language $L_2$ is context-free.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 13.5 Deterministic Context-Free Languages

---

### Definitions

- **Deterministic Context-Free**: Context-free language $L$ such that $L\$$ can be accepted by some deterministic PDA.

### Algorithms

**EOF Removal**
Constructs a PDA for a deterministic language without its end-of-string marker.
	`without$(M: PDA) =`
		1. Set $M' = M$.
		2. For every $q \in K$, add to $M'$ the state $q'$.
		3. For every transition $((q, \epsilon, \gamma_1), (p, \gamma_2)) \in \Delta_M$ do:
			1. Add to $\Delta_{M'}$ the transition $((q', \epsilon, \gamma_1), (p', \gamma_2))$.
		4. For every transition $((q, \$, \gamma_1), (p, \gamma_2)) \in \Delta_M$ do:
			1. Add to $\Delta_{M'}$ the transition $((q, \epsilon, \gamma_1), (p', \gamma_2))$.
			2. Remove $((q, \$, \gamma_1), (p, \gamma_2))$ from $\Delta_{M'}$.
		5. Set $A_{M'} = \{q' | q \in A\}$.
		6. Return $M'$.

### Results & Proofs

**Theorem: Deterministic Context-Free Is Context-Free**
Every deterministic context-free language is context-free.

**Theorem: Deterministic Context-Free Complement Closure**
The deterministic context-free languages are closed under complement.

**Theorem: Deterministic Nonclosure Under Union**
The deterministic context-free languages are not closed under union.

**Theorem: Deterministic Nonclosure Under Intersection**
The deterministic context-free languages are not closed under intersection.

**Theorem: Some Context-Free Languages Are Not Deterministic**
The class of deterministic context-free languages is a proper subset of the class of context-free languages. Thus, there exist nondeterministic PDAs for which no equivalent deterministic PDA exists.

**Theorem: Regular Languages Are Deterministic Context-Free**
Every regular language is deterministic context-free.

**Theorem: Deterministic Context-Free Language Not Ambiguous**
For every deterministic context-free language, there exists an unambiguous grammar.

### Visual Aids

**Language Hierarchy [Diagram]**

![[Screenshot from 2026-10-05 23-51-27.png]]

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
