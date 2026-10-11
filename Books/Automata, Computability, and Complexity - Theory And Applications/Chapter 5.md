# Chapter 5: Finite State Machines

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 5.1 Deterministic Finite State Machines

---

### Definitions

- **Finite State Machine (Finite State Automata)**: Computational device whose input is a string and whose output is one of two values called Accept or Reject. Input is read on symbol at a time, left to right. Accepting states return accept, else reject. Always halts, since strings are finite.
- **Deterministic FSM**: $M = (K, \sum, \delta, s, A)$ where $K$ is a finite set of states, $\sum$ is the input alphabet, $s \in K$ is the start state, $A \subseteq K$ is the set of accepting states, $\delta : K \times \sum \to K$.
- **DFSM Configuration**: Element of $K \times \sum^*$.
- **DFSM Initial Configuration**: $(s_M, w)$ where $s_M$ is the start state of $M$ and $w$ is the input string.
- **Yields-In-One-Step**: Let $c \in \sum$ and $w \in \sum^*$. Relation $\vdash_M$ such that $(q_1, cw) \vdash_M (q_2, w) \iff ((q_1, c), q_2) \in \delta$.
- **Yields**: Relation $\vdash_M^*$ is the closure of $\vdash_M$ under transitivity and reflexivity.
- **Computation:** Finite sequence of configurations $C_0, C_1, .., C_n$ for some $n \ge 0$ such that:
	- $C_0$ is an initial configuration.
	- $C_n = (q, \epsilon)$. 
	- $C_0 \vdash_M C_1 \vdash_M C_2 \vdash_M ... \vdash_M C_n$.
- **Accepting Configuration**: $(q, \epsilon)$ where $q \in A_M$ for DFSM $M$.
- **Rejecting Configuration**: $(q, \epsilon)$ where $q \not \in A_M$ for DFSM $M$.
- **DSFM Accepts**: Let $w \in \sum^*$. $M$ accepts $w$ iff $(s, w) \vdash_M^* (q, \epsilon)$ where $(q, \epsilon)$ is an accepting configuration.
- **DFSM Rejects**: Let $w \in \sum^*$. $M$ rejects $w$ iff $(s, w) \vdash_M^* (q, \epsilon)$ where $(q, \epsilon)$ is a rejecting configuration.
- **DFSM Accepted Language**: Denoted $L(M)$ for machine $M$, is the set of all strings accepted by $M$.
- **Halt**: Configuration of the form $(q, \epsilon)$.
- **Dead State**: State without transition to another distinct state.

### Results & Proofs

**Theorem: DFSMs Halt**
Every DFSM $M$, on input $w$, halts after $|w|$ steps.

### Visual Aids

**Visualizing A DFSM [Diagram]**

![[Screenshot from 2026-09-02 10-40-40.png]]

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 5.2 Regular Languages

---

### Definitions

- **Regular Languages**: Languages accepted by a DSFM.

### Common Pitfalls

- **Empty Transition Convention**: When no transition for $\delta(q, x)$ exists in a DFSM diagram, it is assumed that it maps to a dead state.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 5.3 Designing Deterministic Finite State Machines

---

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 5.4 Nondeterministic Finite State Machines

---

### Definitions

- **Nondeterministic FSM**: $M = (K ,\sum, \Delta, s, A)$ where:
	- $K$ is a finite set of states.
	- $\sum$ is an alphabet.
	- $s \in K$ is the start state.
	- $A \subseteq K$ is the set of final states.
	- $\Delta \subseteq (K \times (\sum \cup \{\epsilon\})) \times K$ and is finite.
- **NFSM Configuration**: Element of $K \times \sum^*$.
- **NFSM Initial Configuration**: $(s_M, w)$ where $s_M$ is the start state of $M$ and $w$ is the input string.
- **Yields-In-One-Step**: Let $c \in \sum \cup \{\epsilon\}$ and $w \in \sum^*$. Relation $\vdash_M$ such that $(q_1, cw) \vdash_M (q_2, w) \iff ((q_1, c), q_2) \in \Delta$.
- **Yields**: Relation $\vdash_M^*$ is the closure of $\vdash_M$ under transitivity and reflexivity.
- **Computation:** Finite sequence of configurations $C_0, C_1, .., C_n$ for some $n \ge 0$ such that:
	- $C_0$ is an initial configuration.
	- $C_n = (q, \epsilon)$. 
	- $C_0 \vdash_M C_1 \vdash_M C_2 \vdash_M ... \vdash_M C_n$.
- **Accepting Configuration**: $(q, \epsilon)$ where $q \in A_M$ for NFSM $M$.
- **Rejecting Configuration**: $(q, \epsilon)$ where $q \not \in A_M$ for NFSM $M$. (maybe not)
- **NFSM Accepts**: Let $w \in \sum^*$. $M$ accepts $w$ iff at least one of its computations accepts.
- **NFSM Rejects**: Let $w \in \sum^*$. $M$ accepts $w$ iff none of its computations accepts.
- **NFSM Language Accepted**: Denoted $L(M)$ for machine $M$, is the set of all strings accepted by $M$.
- **$\epsilon$-Transition Function**: $eps(q) = \{p \in K | (q, w) \vdash_M^* (p, w)\}$.
- **$\epsilon$-loop**: Traversable loop of only $\epsilon$ transitions.

### Algorithms

**$\epsilon$-Transition Function Computation**
Computes $eps: K_M \to \mathcal{P}(K_M)$.
> `eps((q): state)`
> 1. `result = {q}`
> 2. While there exists some $p \in \text{result}$, some $r \notin \text{result}$, and some transition $(p,\epsilon,r)\in\Delta$
> 	 Insert r into `result`.
> 3. Return `result`.

**NDFSM Simulation Algorithm**
Simulates a NFSM.
	`ndfsmsimulate(M : NFSM, w : string)` =
	1. `current-state = eps(s)`
	2. While any input symbols in `w` remain to be read do:
		2.1. `c = get-next-symbol(w)`
		2.2 `next-state =` $\emptyset$
		2.3. For each state `q` in `current-state` do:
			For each state `p` such that $(q, c, p) \in \Delta$ do:
				`next-state =` $\text{next-state} \cup eps(p)$
		2.4 `current-state = next-state`
	3. If `current-state` contains any states in $A$, accept. Else reject.

**DFSM Construction Algorithm**
Constructs an equivalent $DFSM$ from a $NDFSM$.
	`ndfsmtodfsm(M: NDFSM)`
	1. For each state $q$ in $K$ do:
		Compute $eps(q)$
	2. $s' = eps(s)$
	3. Compute $\delta'$:
		3.1 $\text{active-states} = \{s'\}$
		3.2 $\delta' = \emptyset$
		3.3 While there exists some element $Q$ of $\text{active-states}$ for which $\delta'$ has not yet been computed do:
			For each character $c \in \sum$ do:
				$\text{new-state} = \emptyset$
				For each state $q \in Q$ do:
					For each state $p$ such that $(q, c, p) \in \Delta$ do:
						$\text{new-state} = \text{new-state} \cup esp(p)$
				Add $(Q, c, \text{new-state})$ to $\delta'$
				If $\text{new-state} \notin \text{active-states}$ then insert it into $\text{active-states}$
	4. $K' = \text{active-states}$
	5. $A' = \{Q \in K' | Q \cap A \ne \emptyset\}$.

### Results & Proofs

**Theorem: DFSM Implies NDFSM**
For every $DFSM$, there is an equivalent $NDFSM$.

**Theorem: NDFSM Implies DFSM**
Given an $NDFSM$ $M = (K, \sum, \Delta, s, A)$ that accepts some language $L$, there exists an equivalent $DFSM$ that accepts $L$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 5.7 Minimizing FSMs

---

### Definitions

- **Minimal DFSM**: DFSM $M$ is minimal iff $\not \exists$ DFSM $M'$ such that $L(M) = L(M')$ and $M'$ has fewer states than $M$.
- **Indistinguishable**: Denoted $x \approx_L y$, $x$ is indistinguishable from $y$ with respect to $L$ iff $\forall z \in \sum^* (xz \in L \iff yz \in L)$. Equivalence relation.
- **Distinguishable**: Not indistinguishable.
- **Contains**: State $q$ of a DFSM $M$ contains the set of strings called $s$ such that $M$ lands in $q$ after reading $s$ from its start state.
- **Equivalent**: States $q, p$ of DFSM $M$ are equivalent, $q \equiv p$, iff $\forall w \in \Sigma^*$ either $w$ drives $M$ to an accepting state from both $q$ and $p$ or to a rejecting state from both. $\equiv$ is an equivalence relation. $\equiv_n$ for $n \ge 0$ denotes equivalence for strings of length $n$. In other words, $p \equiv^0 q$ iff both are accepting or both rejecting states and $p \equiv^n q$ for $n \ge 1$ iff $p \equiv^{n-1} q$ and $\forall a \in \Sigma (\delta(p, a) \equiv^{n-1} \Sigma(q, a))$.

### Algorithms

**Minimal DFSM Construction**
Constructs a minimal DFSM from an existing DFSM.
	`minDFSM(M : DFSM) =`
	1. $\text{classes} = \{A, K - A\}$
	2. Repeat until a pass at which no change to $\text{classes}$ has been made:
		2.1 $\text{newclasses} = \emptyset$
		2.2 For each equivalence class $e$ in $\text{classes}$, if $e$ contains more than one state, see if it needs to be split:
			For each state $q$ in $e$ do:
				For each character $c$ in $\Sigma$ do:
					Determine which element of $\text{classes}$ $q$ goes to if $c$ is read.
			If there are any two states $p$ and $q$ such that there is any character $c$ such that, when $c$ is read, $p$ goes to one element of $\text{classes}$ and $p$ goes to another, then $p$ and $q$ must be split. Create as many new equivalent classes as necessary. Insert those classes into $\text{newclasses}$.
			If there are no states whose behaviour differs, insert $e$ into $\text{newclasses}$.
		2.3 $\text{classes} = \text{newclasses}$.
	3. Return $M' = (\text{classes}, \Sigma, \delta_{M'}, \{[q] | q \in A_m\})$ where if $\delta_M(q, c) = p$, then $\delta_{M'} = ([q], c) = [p]$.

### Results & Proofs

**Theorem: $\approx_L$ Lower Bound**
Let $L$ be a regular language and let $M = (K, \sum, \delta, s, A)$ be a DFSM that accepts $L$. The number of states in $M$ is greater than or equal to the number of equivalence classes of $\approx_L$.

**Theorem: Unique Minimal DFSM**
Let $L$ be a regular language over some alphabet $\sum$. Then there is a DFSM $M$ that accepts $L$ and that has precisely $n$ states where $n$ is the number of equivalence classes of $\approx_L$. Any other DFSM that accepts $L$ must either have more states than $M$ or it must be equivalent to $M$ except for state names. $(\text{equivalence classes of } \approx_L, \Sigma, \delta([x], a) = [xa], [\epsilon], \{[x] | x \in A\})$.

**Theorem: Myhill-Nerode Theorem**
A language is regular iff the number of equivalence classes of $\approx_L$ is finite.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
