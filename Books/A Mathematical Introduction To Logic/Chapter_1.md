# Chapter 1: Sentential Logic
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 1.0 Informal Remarks On Formal Languages
---
### Key Concepts
- **Formal Language Description**:
  - 1. Set of symbols.
  - 2. Well-formed formulas (rules of grammar for finite sequences).
  - 3. Translations to natural language.

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
  - Sentence symbols (propositional symbols).

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


## 1.2 Truth Assignments
---
### Key Concepts
- **Selected Tautologies**:
  - Associative and commutative laws for $\land, \lor, \iff$.
  - Distributive laws: $\vDash (A \land (B \lor C)) \iff ((A \land B) \lor (A \land C))$, $(A \lor (B \land C)) \iff ((A \lor B) \land (A \lor C))$.
  - Negation: $\vDash (\neg (\neg A)) \iff A$, $(\neg (A \implies B)) \iff (A \land (\neg B))$, $(\neg (A \iff B)) \iff ((A \land (\neg B)) \lor ((\neg A) \land B))$.
  - De Morgan's Laws: $\vDash (\neg (A \land B)) \iff ((\neg A) \lor (\neg B))$, $(\neg (A \lor B)) \iff ((\neg A) \land (\neg B))$.
  - Excluded Middle: $\vDash (A \lor (\neg A))$.
  - Contradiction: $\vDash \neg (A \land (\neg A))$.
  - Contraposition: $\vDash (A \implies B) \iff ((\neg B) \implies (\neg A))$.
  - Exportation: $\vDash ((A \land B) \implies C) \iff (A \implies (B \implies C))$.
### Definitions
- **Truth Values**
  - Set of two distinct points $\{T, F\}$ where F denotes falsity and T truth.
  - No relevance given to what the points themselves are.
  - This is two-valued logic.
- **Truth Assignment**
  - Function $v : S \to \{F, T\}$ for a set S of sentence symbols.
  - Let $\overline{S}$ be the set of wffs that can be built up from S by the five formula-building operations. Define $\overline{v} : \overline{S} \to \{F, T\}$ as the extension meeting the following conditions:
  - 0. $\forall A \in S (\overline{v}(A) = v(A))$.
  - $\forall \alpha, \beta \in \overline{S}$:
  - 1. $\overline{v}((\neg \alpha)) = \begin{cases} T & \text{if } \overline{v}(\alpha) = F \\ F & \text{otherwise} \end{cases}$.
  - 2. $\overline{v}((\alpha \land \beta)) = \begin{cases} T & \text{if } \overline{v}(\alpha) = T \text{ and } \overline{v}(\beta) = T \\ F & \text{otherwise } \end{cases}$.
  - 3. $\overline{v}((\alpha \lor \beta)) = \begin{cases} T & \text{if } \overline{v}(\alpha) = T \text{ or } \overline{v}(\beta) = T \\ F & \text{otherwise } \end{cases}$.
  - 4. $\overline{v}((\alpha \implies \beta)) = \begin{cases} F & \text{if } \overline{v}(\alpha) = T \text{ and } \overline{v}(\beta) = F \\ T & \text{otherwise} \end{cases}$.
  - 5. $\overline{v}((\alpha \iff \beta)) = \begin{cases} T & \text{if } \overline{v}(\alpha) = \overline{v}(\beta) \\ F & \text{otherwise} \end{cases}$.
  - Conditions 1-5 can be represented by a truth table.
- **Satisfies**
  - Truth assignment v satisfies $\phi$ iff $\overline{v}(\phi) = T$.
- **Tautologically Implies**
  - Let $\sum$ be a set of wffs and $\tau$ another wff.
  - $\sum$ tautologically implies $\tau$ ($\sum \vDash \tau$) iff $\forall v (\forall \sigma \in \sum (\overline{v}(\sigma) = T) \implies \overline{v}(\tau) = T)$.
  - Special case when $\sum = \emptyset$, denoted $\vDash \tau$, and we call $\tau$ a tautology.
  - If $\sum$ is a singleton, notation leaves out set notation.
- **Tautologically Equivalent**
  - If $\sigma \vDash \tau$ and $\tau \vDash \sigma$, then $\sigma \tauteq \tau$.

### Theorems & Proofs
**Theorem 12A**
For any truth assignment v for a set S there is a unique function $\overline{v} : \overline{S} \to \{F, T\}$ meeting conditions 0-5 of the truth assignment extension.

**Compactness Theorem**
Let $\sum$ be an infinite set of wffs such that for any finite subset $\sum_0$ of $\sum$, there is a truth assignment that satisfies every member of $\sum_0$. Then there is a truth assignment that satisfies every member of $\sum$.

What if you break the infinite set into an infinite collection of finite sets and "merge" the truth assignments.

### Formulas
**Truth Table Assignments**
Number of truth assignments for $n$ variables.
$$
2^n
$$
### Visual Aids

#### Truth Table
![[Screenshot from 2026-06-28 19-02-13.png]]

#### Truth Computation Tree
![[Screenshot from 2026-06-28 19-08-40.png]]

### Notable Quotes
> “The more generally applicable a procedure it is, the less efﬁcient it is likely to be."

### References
- *Book Title* — Chapter X, Pages Y–29


## 1.3 A Parsing Algorithm
---
### Definitions
- **Polish Notation**
  - Five formula building operations given by:
  - $D_\neg(\alpha) = \neg \alpha$.
  - $D_\land(\alpha, \beta) = \land \alpha \beta$.
  - $D_\lor(\alpha,\beta) = \lor \alpha \beta$.
  - $D_{\implies}(\alpha, \beta) = \implies \alpha \beta$.
  - $D_{\iff}(\alpha, \beta) = \iff \alpha \beta$.
  - For further simplicity, $N, K, A, C, E$ substituted for $\neg, \land, \lor, \implies, \iff$ respectively.
### Algorithms
**A Parsing Algorithm**
Parses a wff into a tree. For any expression, the algorithm is bounded by the length of the given expression. The choices are forced in the procedure, giving the only possible tree. Any rejection must have meant the expression is not a wff. Else, the expression was a wff.
1. If all minimal vertices have sentence symbols, then the procedure is complete. Otherwise, select a minimal vertex having an expression that is not a sentence symbol.
2. The first symbol must be (, else reject the wff. If the second symbol is $\neg$, jump to step 4.
3. Scan the expression from the left until reaching $(\alpha$ where $\alpha$ is a nonempty expression with balanced parentheses, else reject. The next symbol must be $(\land, \lor, \implies, \iff)$. The remainder of the expression must consist of $\beta)$. Create two children vertices with $\alpha$ and $\beta$. Return to step 1.
4. The first two symbols are $(\neg$. The remainder of the expression must consist of $\beta )$. Create a child vertex with $\beta$.

### Theorems & Proofs
**Lemma 13A**
Every wff has the same number of left as right as right parentheses.

**Lemma 13B**
Any proper initial segment of a wff contains an excess of left parentheses. Thus no proper initial segment of a wff can itself be a wff.

### References
- *Book Title* — Chapter X, Pages Y–34


## 1.4 Induction And Recursion
---
### Key Concepts
- **Induction**:
  - Let U be some set of elements, $B \subseteq U$, and $F = \{f : U \times U \to U, g : U \to U\}$ ($F$ not need be finite).
  - Top Down: $C^* = \bigcap \{P \subseteq U | \text{P is inductive}\}$. $C^*$ is then inductive and the smallest such set (trivial to check).
  - Bottom Up: Define a construction sequence to be $<x_1, ..., x_n>$ such that for each $i \le n$ we have $x_i \in U$ and at least one of $x_i \in B$, $x_i = f(x_j, x_k)$, $x_i = g(x_j)$ where $j, k < i$. Let $C_n = \{x | \text{some construction sequence of length n ends with x} \}$. Then $C_1 \subseteq C_2 \subseteq ...$ and $C_* = \bigcup_n C_n$.
  - $C^* = C_*$, so we refer to the set as C and is said to be generated from B by the functions in F.

### Definitions
- **Inductive**
  - S is inductive iff $B \subseteq S$ and S is closed under f and g.
- **Freely Generated**
  - C is freely generated from B by $F$ if if C is generated from B by $F$, the restriction of functions in $F$ to C are one-to-one, and B along with the ranges of the restricted functions are pairwise disjoint.

### Theorems & Proofs
**Induction Principle**
Assume that C is the set generated from B by the functions in F. If $B \subseteq S \subseteq C$ and S is closed under the functions of F, then $S = C$.
> Proof: $S \subseteq C$ given. S is inductive, and hence $C = C^* \subseteq S$. Thus, $S = C$. $\proofend$

**Recursion Theorem**
Assume that $C \subseteq U$ is freely generated from B by f and g, where $f : U \times U \to U$ and $g : U \to U$. Further assume that V is a set and F, G, and h are functions such that $h : B \to V$, $F : V \times V \to V$, $G : V \to V$. Then $\exists !$ function $\overline{h} : C \to V$ such that $\forall x \in B (\overline{h}(x) = h(x))$ and $\forall x, y \in C (\overline{h}(f(x, y)) = F(\overline{h}(x), \overline{h}(y))) \land (\overline{h}(g(x)) = G(\overline{h}(x)))$.
> Proof: Call a function v acceptable iff $dom(v) \subseteq C$, $ran(v) \subseteq V$, and for $x, y \in C$ i') $x \in B \cap dom(v) \implies v(x) = h(x)$ and ii') $f(x, y) \in dom(v) \implies x, y \in dom(v) \land v(f(x, y)) = F(v(x), v(y))$ with $g(x) \in dom(v) \implies x \in dom(v) \land v(g(x)) = G(v(x))$. Let K be the collection of all acceptable functions and $\overline{h} = \bigcup K$. It can be shown that $\overline{h}$ is a function by $\{x \in C | \text{for at most one z, } (x, z) \in \overline{h}\} = C$. Also, $\overline{h} \in K$ can be shown. Continuing, $dom(\overline{h})$ can be shown to be inductive through free generation to show that $\overline{h}$ is defined throughout $C$. To show uniqueness, show that $\{x \in C | \overline{h_1}(x) = \overline{h_2}(x)\}$ is inductive.

**Unique Readability Theorem**
The set of wffs is freely generated from the set of sentence symbols by the five operations.
> Proof: Consider deletions of the results from operations, showing one-to-one. Similar argument reaches a contradiction on symbols being distinct, showing disjoint. No sentence symbol begins with '(', so disjoint from operation ranges.

### References
- *Book Title* — Chapter X, Pages Y–44


## 1.5 Sentential Connectives
---

### Key Concepts
- **Disjunctive Normal Form**: A wff that is a disjunction of conjunctions of sentence symbols or (inclusive) negated sentence symbols.

### Definitions
- **k-place Boolean Function**: Function from $\{F, T\}^k$ into $\{F, T\}$. F and T allowed to be 0-place boolean functions. The boolean function $B_\alpha^n$ realized by the wff $\alpha$ with sentence symbols $A_1, A_2, ..., A_n$, must satisfy $B_\alpha^n(X_1, ..., X_n) = \overline{v}(\alpha)$ when $v(A_i) = X_i$. 
- **Complete**: Every k-place Boolean function with $k \ge 1$ realizable using only the **complete** connective symbol set $\tau$.

### Examples

**Realized Boolean Functions**
Frequently used boolean functions.
> $B_{A_i}^n, B_{\neg A_1}^1, B_{A_1 \land A_2}^2, B_{A_1 \lor A_2}^2, B_{A_1 \implies A_2}^2, B_{A_1 \iff A_2}^2$.

**Complete Sets**
Common complete sets.
> $\{\land, \lor, \neg\}$, $\{\neg, \land\}$, $\{\neg, \lor\}$, $\{\downarrow\}$, $\{|\}$.

### Results & Proofs

**Theorem: Theorem 15A**
Let $\alpha$ and $\beta$ be wffs whose sentence symbols are among $A_1, ..., A_n$. Impose an ordering on $\{F, T\}$ by defining $F < T$. Then
(a) $\alpha \vDash \beta$ iff $\forall \vec{X} \in \{F, T\}^n (B_\alpha(\vec{X}) \le B_\beta(\vec{X}))$.
(b) $\alpha \tauteq \beta$ iff $B_\alpha = B_\beta$.
(c) $\vDash \alpha$ iff $B_\alpha$ is the constant function with value T.

> **Proof**: Fairly trivial to think about.

**Theorem: Theorem 15B**
Let G be an n-place Boolean function, $n \ge 1$. We can find a wff $\alpha$ such that $G = B_\alpha^n$.

> **Proof:** Consider "gluing" the satisfied sentence assignments with $\lor$.

**Corollary: Corollary 15C**
For any wff $\phi$, we can find a tautologically equivalent wff $\alpha$ in DNF.

**Theorem: Theorem 15D**
Both $\{\neg, \land\}$ and $\{\neg, \lor\}$ are complete.

> Apply De-Morgan's Laws.


### Formulas

**k-place Boolean Function Count**
For a fixed $k$, there are this many unique k-place Boolean functions.

$$
2^{2^k}
$$

### Visual Aids

**Realized Boolean Function Truth Table [Diagram]**

![[Screenshot from 2026-07-13 23-08-20.png]]

**0-ary Connectives [Table]**

| Boolean Function | Connective Symbol |
| ---------------- | ----------------- |
| F                | $\bot$            |
| T                | $\top$            |

**Unary Connectives**

| Boolean Function | Connective Symbol | Equivalent |
| ---------------- | ----------------- | ---------- |
| Constant F       |                   | $\bot$     |
| Constant T       |                   | $\top$     |
| Identity         |                   |            |
| Negation         | $\neg$            |            |

**Binary Connectives**

| Boolean Function     | Connective Symbol | Equivalent                          |
| -------------------- | ----------------- | ----------------------------------- |
| Constant F           |                   | $\bot$                              |
| Constant T           |                   | $\top$                              |
| Project First        |                   | A                                   |
| Project Second       |                   | B                                   |
| Negate First         |                   | $\neg A$                            |
| Negate Second        |                   | $\neg B$                            |
| And                  | $\land$           | $A \land B$                         |
| Or                   | $\lor$            | $A \lor B$                          |
| Conditional          | $\implies$        | $A \implies B$                      |
| Bi-conditional       | $\iff$            | $A \iff B$                          |
| Reversed Conditional | $\Leftarrow$      | $A \Leftarrow B$                    |
| Exclusive or         | $\oplus$          | $(A \lor B) \land \neg (A \land B)$ |
| Nor                  | $\downarrow$      | $\neg (A \lor B)$                   |
| Nand                 | \|                | $\neg (A \land B)$                  |
| Less than            | <                 | $(\neg A) \land B$                  |
| Greater than         | >                 | $A \land (\neg B)$                  |

### Common Pitfalls

* **0-ary Connectives Truth Assignment**: $\overline{v}(\bot) = F$ and $\overline{v}(\top) = T$ always.

### Related Links & References

* **Core Text [Book]**: *Book* — Chapter X, Pages -54


## 1.6 Switching Circuits

---
### Visual Aids

**Circuit As A Boolean Function [Diagram]**

![[Screenshot from 2026-07-14 15-35-20.png]]

**Circuit As A Wff [Diagram]**

![[Screenshot from 2026-07-14 15-36-01.png]]

**Finding A Wff For A Circuit [Diagram]**

![[Screenshot from 2026-07-14 15-36-26.png]]

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -59


## 1.7 Compactness And Effectiveness

---

### Key Concepts

- **\* Effective Procedure**: Exact instructions finite in length, possible to be mechanically implemented in finite steps, and is an algorithm. Since infinite sentence symbols requires infinite memory, we restrict such symbols to just $A$ and $'$.

### Definitions

- **Satisfiable**: Set $\sum$ is satisfiable iff $\exists$ a truth assignment that satisfies every member of $\sum$.
- **\* Decidable**: A set of expressions $\sum$ is decidable iff $\exists$ an effective procedure that, given an expression $\alpha$, will decide whether or not $\alpha \in \sum$.
- **\* Effectively Enumerable**: Set A of expressions is effectively enumerable iff $\exists$ an effective procedure that lists the members of A. List can be infinite but any member must be reachable in finite length.
- **\* Semidecidable**: A set A of expressions is semideciable iff $\exists$ an effective procedure that, given any expression $\epsilon$, produces the answer "yes" iff $\epsilon \in A$.
- **\* Effectively Computable**: Function f is effectively computable iff $\exists$ an effective procedure, given input x, that will eventually produce $f(x)$.

### Results & Proofs

**Theorem: Compactness Theorem**
A set of wffs is satisfiable iff every finite subset is satisfiable.
> **Proof**: Create a maximal set and give it a truth assignment.

**Corollary: Corollary 17A**
If $\sum \vDash \tau$, then $\exists$ finite $\sum_0 \subseteq \sum$ such that $\sum_0 \vDash \tau$.
> **Proof**: $\forall \text{finite } \sum_0 \subseteq \sum( \sum_0 \not \vDash \tau) \implies \sum \not \vDash \tau$.

**Theorem: \* Theorem 17B**
$\exists$ an effective procedure, that given any expression $\epsilon$, will decide whether or not it is a wff.
> Algorithm in section 1.3.

**Theorem: \* Theorem 17C**
$\exists$ an effective procedure that, given a finite $\sum \cup \tau$ of wffs, will decide whether or not $\sum \vDash \tau$.
> Truth-table procedure in section 1.2.

**Corollary: \* Corollary 17D**
For a finite set $\sum$, the set of tautological consequences of $\sum$ is decidable.

**Theorem: \* Theorem 17E**
A set A of expressions is effectively enumerable iff $\exists$ an effective procedure that, given any expression $\epsilon$, produces the answer "yes" iff $\epsilon \in A$.
> $(\implies)$ Continue to look at the next item in the list. $(\impliedby)$ Keep running the procedure on an enumerated list of expressions, budgeting time.

**Theorem: \* Kleene's Theorem**
A set of expressions is decidable iff both it and its complement are effectively enumerable.
> TBD

**Theorem: \* Theorem 17G**
If $\sum$ is a decidable set of wffs, then the set of tautological consequences of $\sum$ is effectively enumerable.
> Enumerate the members of $\sum$ and then induct on those members for any wff $\tau$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -66
