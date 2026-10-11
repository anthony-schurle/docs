# Chapter 12: Pushdown Automata

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 12.1 Definition of a (Nondeterministic) PDA

---

### Key Concepts

- **Stack Push Convention**: If $s$ is at the top of the stack and $c_1c_2...c_n$ is pushed, then the value of the stack becomes $c_1c_2...c_ns...$.

### Definitions

- **Pushdown Automata (PDA)**: $M = (K, \Sigma, \Gamma, \Delta, s, A)$ where:
	- $K$ is a finite set of states;
	- $\Sigma$ is the input alphabet;
	- $\Gamma$ is the stack alphabet;
	- $\Delta \subseteq (K \times (\Sigma \cup \{\epsilon\}) \times \Gamma^*) \times (K \times \Gamma^*)$ and is finite;
	- $s \in K$ is the start state;
	- $A \subseteq K$ is the set of accepting states.
	- $L(M)$, language accepted by $M$, is the set of all strings accepted by $M$.
- **PDA Configuration**: Element of $K \times \Sigma^* \times \Gamma^*$.
- **PDA Initial Configuration**: For input $w$, $(s, w, \epsilon)$.
- **PDA Yields-In-One-Step**: Let $c \in \Sigma \cup \{\epsilon\}$, $\gamma_1, \gamma_2, \gamma \in \Gamma^*$, and $w \in \Sigma^*$. Denote the relation by $\vdash$. Then $(q_1, cw, \gamma_1 \gamma) \vdash_M (q_2, w, \gamma_2 \gamma) \iff ((q_1, c, \gamma_1), (q_2, \gamma_2)) \in \Delta$. 
- **PDA Yields**: Reflexive, transitive closure of $\vdash_M$ denoted $\vdash_M^*$.
- **PDA Computation**: Finite sequence of configurations $C_0, C_1, ..., C_n$ for some $n \ge 0$ such that:
	- $C_0$ is the initial configuration.
	- $C_n = (q, \epsilon, \gamma)$ for $q \in K$ and $\gamma \in \Gamma^*$.
	- $C_0 \vdash_M C_1 \vdash_M ... \vdash_M C_n$.
- **PDA Accepting Computation**: $C$, a computation, is accepting iff $C = (s, w, \epsilon) \vdash_M^* (q, \epsilon, \epsilon)$ for some $q \in A$.
- **PDA Rejecting Computation**: $C$, a computation, is rejecting iff $C = (s, w, \epsilon) \vdash_M^* (q, w', \alpha)$ where $C$ is not accepting and $M$ has no moves it can make from $(q, w', \alpha)$.
- **PDA Accepts**: Let $w \in \Sigma^*$, $M$ accepts $w$ iff at least one of its computations accepts.
- **PDA Rejects**: Let $w \in \Sigma^*$, $M$ rejects $w$ iff all of its computations rejects.

### Visual Aids

**Stack Notation Convention [Diagram]**

![[Screenshot from 2026-10-04 11-13-25.png]]

**PDA Drawing [Diagram]**

![[Screenshot from 2026-10-04 11-54-30.png]]

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 12.2 Deterministic And Nondeterministic PDAs

---

### Key Concepts

- **Empty Stack Nondeterminism**: $PDA$ Nondeterminism that arises from a pathway with acceptance limited to an empty stack. Can be made deterministic with an empty stack symbol pushed at the start.
- **Empty String Nondeterminism**: PDA Nondeterminism that arises from a pathway with acceptance limited to an empty string. Can be made deterministic with a end-of-string marker appended to the end of a language.

### Definitions

- **Deterministic PDA**: Non-deterministic PDA $M$ satisfying:
	- $\Delta_M$ has at most one transition for any configuration.
	- If $q \in A_M$, then $((q, \epsilon, \epsilon), (p, a)) \not \in \Delta_M$ for any p or a.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 12.3 Equivalence Of Context-Free Grammars And PDAs

---

### Key Concepts

- **Top Down Parser**: Attempts to generate a string by seeing if it can be derived from rule applications.
- **Bottom Up Parser**: Verifies a string by working backwards to reach the start symbol from rule applications.
- **Shift-Reduce Parser**: Shifts input onto a stack and reduces by rule applications.

### Definitions

- **Restricted Normal Form PDA**: Let $M$ be a PDA. It must satisfy:
	- $M$ has a start state $s'$ that only pushes a symbol, call it $\#$, onto the stack and transfers to another state. There must be no transition back to $s'$ and we require $s' \not \in \Gamma_M$.
	- $M$ has one accepting state, call it $a$. All transitions into $a$ pop $\#$ and read no input.
	- Every transition in $M$, except the one out of $s'$, pops exactly one symbol from the stack.

### Algorithms

**CFG To PDA (Top Down)**
Constructs a PDA from a context-free grammar using a top-down approach.
	`cfgtoPDAtopdown(G: CFG) =`
		1. Set $\Delta = \{((p, \epsilon, \epsilon), (q, S))\}$.
		2. For each $(X, \lambda_1 \lambda_2 \ldots \lambda_n) \in R_G$, add $((q, \epsilon, X), (q, \lambda_1 \lambda_2 \ldots \lambda_n))$ to $\Delta$.
		3. For each $c \in \Sigma_G$, add $((q, c, c), (q, \epsilon))$ to $\Delta$.
		4. Return $(\{q, p\}, \Sigma_G, V_G, \Delta, p, \{q\})$.

**CFG To PDA (Bottom Up)**
Constructs a PDA from a context-free grammar using a bottom-up approach.
	`cfgtoPDAbottomup(G: CFG) =`
		1. Set $\Delta = \{((p, \epsilon, S), (q, \epsilon))\}$.
		2. For each $c \in \Sigma$, add $((p, c, \epsilon), (p, c))$ to $\Delta$.
		3. For each $(X, \lambda_1 \lambda_2 \ldots \lambda_n) \in R_G$, add $((p, \epsilon, (\lambda_1 \lambda_2 \ldots \lambda_n)^R), (p, X))$ to $\Delta$.
		4. Return $(\{q, p\}, \Sigma_G, V_G, \Delta, p, \{q\})$.

**Convert PDA To Restricted Form**
Converts arbitrary PDA into is restricted normal form.
	`convertpdatorestricted(M: PDA) =`
		1. Let $M' = M$.
		2. Create a new start state $s'$.
		3. Add the transition $((s', \epsilon, \epsilon), (s, \#))$.
		4. Create a new accepting state $a$.
		5. For each accepting state $q$ in $M$ do:
			1. Create a new transition $((q, \epsilon, \#), (a, \epsilon))$.
			2. Remove $q$ from the set of accepting states.
		6. For every transition $t$ that pops $k > 1$ symbols do:
			1. Let $qq_1, qq_2, ..., qq_{k-1}$ be new state names.
			2. Then, replace $((q_1, c, \gamma_1 \gamma_2 \ldots \gamma_n), (q_2, \gamma_p))$ with $((q_1, \epsilon, \gamma_1), (qq_1, \epsilon)), ((qq_1, \epsilon, \gamma_2), (qq_2, \epsilon)), \ldots ((qq_{k-1}, c, \gamma_n), (q_2, \gamma_p))$.
		7. For every transition $t = ((q_1, c, \epsilon), (q_2, \gamma))$ do:
			1. Replace $t$ with $|\Gamma_M'|$ transitions of the form $((q_1, c, \alpha), (q_2, \gamma \alpha))$.
		8. Return $M'$.

**Build Grammar From Restricted Form PDA**
Constructs a grammar given a PDA in restricted normal form.
	`buildgrammar(M: PDA in restricted normal form) =`
		1. Set $\Sigma_G = \Sigma_M$.
		2. Set the start symbol of $G$ to S.
		3. Build $R$ as follows:
			1. Insert the rule $S \to <s, \#, a>$. 
			2. For every transition $((q, a, \gamma), (r, \epsilon))$, except the one from $s'$, and every state $w$, except $s'$, in $M$ do:
				1. Insert the rule $<q, \gamma, w> \to a<r, \epsilon, w>$.
			3. For every transition $((q, a, \gamma), (r, \alpha))$, except the one from $s'$, and every state $w$, except $s'$, in $M$ do:
				1. Insert the rule $<q, \gamma, w> \to a<r, \alpha, w>$.
			4. For every transition $((q, a, \gamma), (r, \alpha \beta))$, except the one from $s'$, and every pair of states $v$ and $w$, except $s'$, in $M$ do:
				1. Insert the rule $<q, \gamma, w> \to a<r, \alpha, v><v, \beta, w>$.
			5. In a similar way, create rules for transitions that push more than two symbols.
			6. For every state $q$, except $s'$, in $M$ do:
				1. Insert the rule $<q, \epsilon, q> \to \epsilon$.
			7. Set $V_G$ to $\Sigma_M \cup \{\text{nonterminal symbols mentioned in the rules inserted into R}\}$.

### Results & Proofs

**Theorem: CFG To PDA**
Given a context-free grammar $G = (V, \Sigma, R, S)$, $\exists$ a PDA $M$ such that $L(M) = L(G)$.

**Theorem: PDA To CFG**
Given a PDA $M = (K, \Sigma, \Gamma, \Delta, s, A)$, there exists a CFG $G = (V, \Sigma, R, S)$ such that $L(G) = L(M)$.

**Theorem: PDAs and CFGs Equivalent**
A language is context-free iff it is accepted by some PDA.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 12.4 Nondeterminism And Halting

---

### Key Concepts

- **Decidability PDA Limits**: Minimal PDAs, deterministic PDAs for every context-free language, and no guarantee of a PDA halting are all theoretical limits of PDAs.

### Definitions

- **PDA Computation Halt**: Computation $C$ of a PDA halts iff $C$ is accepting or $C$ ends in a configuration from which no transition can be taken.
- **PDA Halt**: PDA $M$ halts on $w$ iff every computation of $M$ on $w$ halts. If a computation on $w$ halts but does not accept, we say $M$ rejects $w$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 12.5 Alternative Equivalent Definitions Of A PDA

---

### Key Concepts

- **Alternative PDA Definitions**: In all, $M = (K, \Sigma, \Gamma, \Delta, s, A)$. Some definitions require only one pop, or only one pop and one push. Some definitions of accept allow for a nonempty stack or accept when stack and input are both consumed (regardless of finished state). These alternatives are, in fact, equivalent.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 12.6 Alternatives That Are Not Equivalent To The PDA

---

### Key Concepts

- **Tag Systems (Post machines)**: FIFO queue replaces the stack.
- **Two Stacks**: Two stacks instead of one stack.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
