# Chapter 2: Languages And Strings

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 2.1 Strings

---

### Key Concepts

- **Common String Functions**: Common operations on strings. Let $s$ and $t$ be strings.
	- $|s|$, the length of a string, is the total character count in string $s$.
	- $\#_x(s)$, the total amount of times character $x$ occurs in $s$.
	- $s||t$ or $st$, is the concatenation of $s$ to $t$. $\epsilon$ functions as an identity, and concatenation is associative.
	- $s^i$, string replication, is defined as $s^0 = \epsilon$ and $s^{i+1} = s^i s$ for natural number $i$.
	- $s^R$, string reversal, is defined by $s^R = s = \epsilon$ when $|s| = 0$. If $|s| \ge 1$, then $\exists a \in \sum \exists u \in \sum^* (s = ua)$ and we define $s^R = au^R$.
- **Common Language Functions**: Common operations on languages. Let $L_1$ and $L_2$ be languages over $\sum$.
	- $L_1L_2$, concatenation, is $\{w \in \sum^* | \exists s \in L_1 \exists t \in L_2 (w = st)\}$. $\{\epsilon\}$ functions as the identity language. Associative property.
	- $L_1^*$, the Kleene Star of $L_1$, is $\{\epsilon\} \cup \{w \in \sum^* | \exists k \ge 1 \exists w_1, w_2, ..., w_k \in L_1 (w = w_1w_2...w_k)\}$.
	- $L_1^+$, closure under concatenation, is $L_1L_1^*$.
	- $L_1^R$, reverse, is $\{w \in \sum^* | \exists x \in L_1(w = x^R)\}$.

### Definitions

- **Alphabet**: Finite set denoted by $\sum$.
- **Characters (Symbols)**: Members of an alphabet.
- **String**: Finite sequence of characters from some alphabet $\sum$. Empty string denoted $\epsilon$. Set of all possible strings denoted $\sum^*$.
- **Substring**: $s$ is a substring of $t$ iff $s$ occurs contiguously as part of $t$.
- **Proper Substring**: Let $s, t \in \sum^*$. $s$ is a proper substring of $t$ iff $s \ne t$ and s is a substring of t. 
- **Prefix**: Let $s, t \in \sum^*$. $s$ is a prefix of $t$ iff $\exists x \in \sum^*(t = sx)$.
- **Proper Prefix**: Let $s, t \in \sum^*$. $s$ is a proper prefix of $t$ if $s \ne t$ and $s$ is a prefix of $t$.
- **Suffix**: Let $s, t \in \sum^*$. $s$ is a suffix of $t$ iff $\exists x \in \sum^* (t = xs)$.
- **Proper Suffix**: Let $s, t \in \sum^*$. $s$ is a proper suffix of $t$ if $s \ne t$ and $s$ is a suffix of $t$.
- **Language**: $L \subseteq \sum^*$ for alphabet $\sum$ is a language. $\sum_L$ denotes the alphabet from which the strings in $L$ are formed.
- **Lexicographic Order**: If there exists a total order $D$ on $\sum_L$, a lexicographic total ordering $<_L$ is defined on $L$ by $D$ where $\forall x \forall y (|x| < |y| \implies x <_L y)$ and if $|x| = |y|$ then $D$ determines $<_L$.
- **Lexicographic Enumeration**: Program enumerates elements in lexicographic order.
- **Semantic Interpretation Function**: Function that assigns semantics to strings.
- **Compositional Semantic Interpretation Function**: Semantic interpretation function that composes the meanings of simpler constituents.

### Results & Proofs

**Theorem: Reversal Of Strings**
If $w$ and $s$ are strings, then $(ws)^R = s^Rw^R$.

**Theorem: The Cardinality Of $\sum^*$**
If $\sum \ne \emptyset$ then $\sum^*$ is countably infinite.

**Theorem: Uncountably Infinite Number Of Languages**
If $\sum \ne \emptyset$ then the set of languages over $\sum$ is uncountably infinite.

**Theorem: Reversal Of Languages**
If $L_1$ and $L_2$ are languages, then $(L_1L_2)^R = L_2^RL_1^R$.

### Common Pitfalls

- **Empty Language And The Empty String**: The empty language is distinct from a language just containing $\epsilon$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]