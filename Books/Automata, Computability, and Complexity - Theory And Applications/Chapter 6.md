# Chapter 6: Regular Expressions

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 6.1 What is a Regular Expression

---

### Definitions

- **Regular Language**: Contains an alphabet $\Sigma$ which itself contains $\{\emptyset, \cup, \epsilon, (, ), *, +\}$. Properties:
	- $\emptyset$ is a regular expression.
	- $\epsilon$ is a regular expression.
	- Every element in $\Sigma$ is a regular expression.
	- Given regular expressions $\alpha$ and $\beta$, $\alpha \beta$ is a regular expression.
	- Given regular expressions $\alpha$ and $\beta$, $\alpha \cup \beta$ is a regular expression.
	- Given regular expression $\alpha$, $\alpha^*$ is a regular expression.
	- Given a regular expression $\alpha$, $\alpha^+$ is a regular expression.
	- Given a regular expression $\alpha$, $(\alpha)$ is a regular expression.
- **Regular Expression Semantic Interpretative Function**: Properties of function $L$, which maps regular expressions to languages:
	- $L(\emptyset) = \emptyset$. 
	- $L(\epsilon) = \{\epsilon\}$.
	- For any $c \in \Sigma$, $L(c) = \{c\}$.
	- $L(\alpha\beta) = L(\alpha)L(\beta)$.
	- $L(\alpha \cup \beta) = L(\alpha) \cup L(\beta)$.
	- $L(\alpha^*) = L(\alpha)^*$.
	- $L(\alpha^+) = L(\alpha)L(\alpha^*)$.
	- $L((\alpha)) = L(\alpha)$.
	- Precedence orders is $*, \alpha\beta, \cup$ respectively.
- **Describes (Defines)**: If the meaning regular expression $\alpha$ is $L$, then it is said to describe or define $L$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 6.2 Kleene's Theorem

---

### Algorithms

**Regex To FSM**
Creates a FSM from a regular expression.
	`regextofsm(`$\alpha$`: regular expression) =`
	Beginning with the primitive subepxressions of $\alpha$ and working outwards until all FSM for all of $\alpha$ has been built do:
		If $\beta$ is the regular expression $\gamma \cup \zeta$ with $L(\gamma)$ and $L(\zeta)$ regular, such that $M_1$ and $M_2$ accepts these languages, rename $K_1$ and $K_2$ so that $K_1 \cap K_2 = \emptyset$. Create $M_3 = (\{s_3\} \cup K_1 \cup K_2, \Sigma, \Delta_3, s_3, A_1 \cup A_2)$, where $\Delta_3 = \Delta_1 \cup \Delta_2 \cup \{((s_3, \epsilon), s_1), ((s_3, \epsilon), s_2)\}$.
		If $\beta$ is the regular expression $\gamma\zeta$ with $L(\gamma)$ and $L(\zeta)$ regular, such that $M_1$ and $M_2$ accepts these languages, rename $K_1$ and $K_2$ so that $K_1 \cap K_2 = \emptyset$. Create $M_3 = (K_1 \cup K_2, \Sigma, \Delta_3, s_1, A_2)$, where $\Delta_3 = \Delta_1 \cup \Delta_2 \cup \{((q, \epsilon), s_2) | q \in A_1\}$.
		If $\beta$ is the regular expression $\gamma^*$ with $L(\gamma)$ regular, such that $M_1$ accepts this languages, create $M_2 = (\{s_2\} \cup K_1, \Sigma, \Delta_2, s_2, \{s_2\} \cup A_1)$, where $\Delta_2 = \Delta_1 \cup \{((s_2, \epsilon), s_1)\} \cup \{((q, \epsilon), s_1) | q \in A_1\}$.
		If $\alpha = c \in \Sigma$, then construct $M_1 = (\{s_1, s_2\}, \Sigma, \{((s_1, c), s_2)\}, s_1, \{s_2\})$.
		If $\alpha = \emptyset$, then construct $M_1 = (\{s_1\}, \Sigma, \emptyset, s_1, \emptyset)$.

**FSM To Regex Heuristic**
Creates a regular expression from a FSM via a heuristic.
	`fsmtoregexheuristic(M: FSM) =`
	1. Remove from $M$ any states that are unreachable from the start state.
	2. If $M$ has no accepting states, then halt and return $\emptyset$.
	3. If the start state $s_M$ of $M$ is part of a loop, create a new start state $s'$ and add transition $((s', \epsilon), s_M)$.
	4. If there is more than one accepting state or if there is one accepting state with any transition out, create a new accepting state and connect each of $M$'s accepting states via an $\epsilon$-transition. Remove the old accepting states from the set of accepting states.
	5. If $M$ has one state, then return $\epsilon$.
	6. Until only the start state and accepting state remain do:
		6.1. Select some state $\text{rip}$ from $M$ that is not the start state nor the accepting state.
		6.2. Remove $\text{rip}$ from $M$.
		6.3. Modify the transitions among the remaining states so that $M$ accepts the same strings. The labels on the rewritten transitions may be any regular expression.
	7. Return the regular expression that labels the one remaining transition from the start state to the accepting state.

**FSM To Regex**
Creates a regular expression from a FSM. 
	`fsmtoregex(M : FSM) = `
	1. $\text{M}' =$ `standardize(M : FSM)`.
	2. Return `buildregex(M')`.

Standardizes the FSM.
	`standardize(M : FSM) =`
	1. Remove from $M$ any states that are unreachable from the start state. 
	2. If the start state of $M$ is part of a loop, create a new start state $s$ and connect $s$ to $M$'s start state via an $\epsilon$-transition.
	3. If there is more than one accepting state of $M$ or if there is one with any transition out of it, create a new accepting state and connect each of $M$'s accepting states to it via an $\epsilon$-transition. Remove the old accepting states from the set of accepting states.
	4. If there is more than one transition between states $p$ and $q$, collapse them into a single transition with $\cup$.
	5. If there is a pair of states $p, q$ and there is no transition between them and $p$ is not the accepting state and $q$ is not the start state, then create a transition from $p$ to $q$ labeled $\emptyset$.
	6. Return $M$.

Builds a regular expression into a single transition from a standardized FSM.
	`buildregex(M : FSM) =`
	1. If $M$ has no accepting states, then halt and return the regular expression $\emptyset$.
	2. If $M$ has only one state, then halt and return $\epsilon$.
	3. Until only the start state and the accepting state remain do:
		3.1. Select some state $\text{rip}$ from $M$ that is not the start or accepting state.
		3.2. For every transition from some state $p$ to some state $q$, if both $p$ and $q$ are not $\text{rip}$ then, then using the current labels given by the expressions $R$, compute the new label $R'$ for the transition from $p$ to $q$ using: $R'(p, q) = R(p, q) \cup R(p, \text{rip})R(\text{rip}, \text{rip})^*R(\text{rip}, q)$.
		3.3. Remove $\text{rip}$ and all transitions into and out of it. 
	4. Return the regular expression labeling the one transition remaining.

**Keywords To DFSM**
Constructs a DFSM that accepts strings containing keywords.
	`buildkeywordFSM(K : set of keywords)`
	1. Create a start state $q_0$.
	2. For each element $k$ of $K$ do:
		2.1. Create a branch corresponding to $k$.
	3. Create a set of transitions that describe what to do when a branch dies, either because its complete pattern has been found or because the next character is the not the correct one to continue the pattern.
	4. Make the states at the ends of each branch accepting.

### Results & Proofs

**Theorem: For Every Regular Expression There Is An Equivalent FSM**
Any language that can be defined with a regular expression can be accepted by some FSM.

**Theorem: For Every FSM There Is An Equivalent Regular Expression**
Every regular language can be defined with a regular expression.

**Theorem: Kleene's Theorem**
The class of languages that can be defined with regular expressions is exactly the class of regular languages.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
