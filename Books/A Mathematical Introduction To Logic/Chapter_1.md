# Chapter 1: Sentential Logic
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 1.0 Informal Remarks On Formal Languages
---
### Key Concepts
- **Formal Logic Description**:
  - 1. Set of symbols.
  - Well-formed formulas rules.
  - Translations to natural language.

### References
- *Book Title* — Chapter X, Pages 11–13


## 1.1 The Language Of Sentential Logic
---
### Key Concepts
- **Assumptions**:
  - Infinite sequence of symbols.
  - No symbol is a finite sequence of other symbols.

### Definitions
- **Sentential Connective Symbols**
  - $\neg, \land, \lor, \implies, \iff$.

- **Logical Symbols**
  - $\neg, \land, \lor, \implies, \iff, (, )$.

- **Non-Logical Symbols**
  - Sentence symbols.

- **Expression**
  - Finite sequence of symbols.
  - Specified by concatenating names of symbols or sequences.

- **Well-Formed Formulas(wffs)**
  - a) Every sentence symbol is a wff.
  - b) If $\alpha,\beta$ are wffs, then so are $(\neg \alpha), (\alpha \land \beta), (\alpha \lor \beta), (\alpha \implies \beta), (\alpha \iff \beta)$.
  - c) No expression is a wff unless compelled to be by a) and b).
  - Can be built up from sentence symbols by applying formula-building operations finitely many times defined by the equations (excludes empty sequence):
  - $\xi_\neg(\alpha) = (\neg \alpha)$.
  - $\xi_\land(\alpha, \beta) = (\alpha \land \beta)$.
  - $\xi_\lor(\alpha,\beta) = (\alpha \lor \beta)$.
  - $\xi_{\implies}(\alpha, \beta) = (\alpha \implies \beta)$.
  - $\xi_{\iff}(\alpha, \beta) = (\alpha \iff \beta)$.

- **Construction Sequence**
  - Finite sequence $<\epsilon_1, ..., \epsilon_n>$ of expressions such that for each $i \le n$: $\epsilon_i$ is a sentence symbol, $\epsilon_i = \xi_\neg (\epsilon_j)$ for some $j < i$, or $\epsilon_i = \xi_{\blacksquare}(\epsilon_j, \epsilon_k)$ for some $j, k < i$ and $\blacksquare = \land, \lor, \implies, \iff$.
  - Construction sequence ending with $\alpha$ determines $\alpha$ as a wff.

### Theorems & Proofs
**Induction Principle**
If S is a set of wffs containing all the sentence symbols and closed under all five formula-building operations, then S is the set of all wffs.

### Visual Aids

**Sentential Logic Symbols**
Sentence(propositions) symbols may sometimes be represented as one infinite sequence sentence symbol instead.

| Symbol     | Name              |
| ---------- | ----------------- |
| (          | left parenthesis  |
| )          | right parenthesis |
| $\neg$     | negation          |
| $\land$    | conjunction       |
| $\lor$     | disjunction       |
| $\implies$ | conditional       |
| $\iff$     | biconditional     |
| $A_1$      | first sentence    |
| $A_2$      | second sentence   |
| ...        |                   |
| $A_n$      | nth sentence      |
| ...        |                   |

### Notable Quotes
> “One note of caution: Do not confuse a sentence in the English language (Roses are red) with a translation of that sentence in the formal language (such as R). These are different. The English sentence is presumably either true or false. But the formal expression is simply a sequence of symbols. It may indeed be interpreted in one context as a true (or false) English sentence, but it can have other interpretations in other contexts."
### Common Pitfalls
- Names of symbols differ from their logical being, $\implies$ is a name for logical implication.

### References
- *Book Title* — Chapter X, Pages Y–19