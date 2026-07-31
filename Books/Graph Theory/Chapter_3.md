# Chapter 3: Connectivity

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 3.1 2-Connected Graphs And Subgraphs

---

### Definitions

- **k-connected**: Any two vertices can be joined by $k$ independent paths.
- **Block**: Maximal connected subgraph without a cutvertex. So either a maximal 2-connected subgraph, bridge with its ends, or an isolated vertex.
- **Block Graph**: If $A$ is the set of cutvertices and $\mathcal{B}$ the set of blocks for graph $G$, the block graph of $G$ is made of vertex set $A \cup \mathcal{B}$ with edges $aB$ when $a \in B$.

### Results & Proofs

**Proposition: Proposition 3.1.1.**
A graph is 2-connected iff it can be constructed from a cycle by successively adding $H$-paths to graphs $H$ already constructed.

**Lemma: Lemma 3.1.2**
Let $G$ be any graph.
(i) The cycles in $G$ are precisely the cycles in its blocks.
(ii) The bonds of $G$ are precisely the bonds of its blocks.

**Lemma: Lemma 3.1.3**
The following statements are equivalent for distinct edges $e, f$ of a graph $G$:
(i) The edges $e, f$ belong to a common block of $G$.
(ii) The edges $e, f$ belong to a common cycle in $G$.
(iii) The edges $e, f$ belong to a common bond of $G$.

**Lemma: Lemma 3.1.4**
The block graph of a connected graph is a tree.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -66


## 3.2 The Structure Of 3-Connected Graphs

---

### Key Concepts

- **Example Concept**: A concise explanation of a foundational concept.

### Definitions

- **Example Definition**: A precise definition of a term introduced in this section.

### Examples

**Basic Example**
Present a simple case that demonstrates the preceding definitions or concepts.
> Presented example...

### Axioms

- **Example Axiom**: A foundational assumption used within the subject area.

### Algorithms

**Example Algorithm**
A brief explanation of the algorithm’s purpose, expected inputs, and output.
_Time Complexity: $\mathcal{O}(\text{time bound})$_  
_Space Complexity: $\mathcal{O}(\text{space bound})$_
```pseudo
1. Initialize the required variables or data structures.
2. Process the input according to the algorithm’s main rule.
3. Repeat until the termination condition is satisfied.
4. Return the resulting value or structure.
```

### Code Snippets

**Example Implementation**
A brief description of the implementation, language, and design approach.
```python
def example_function(input_data):
    # Implementation logic goes here
    pass
```

### Results & Proofs

**Proposition: Example Proposition**
State a preliminary result or narrowly scoped mathematical claim.
> **Proof**: Provide a proof using relevant definitions, axioms, previously established results, or direct reasoning.

**Lemma: Example Lemma**
State an intermediate result that supports a later theorem or proposition.
> **Proof**: Provide the logical steps required to establish the lemma.

**Theorem: Example Theorem**
State the principal theorem or major result of the section.
> **Proof**: Provide the complete argument, including assumptions, intermediate steps, and the conclusion.

**Corollary: Example Corollary**
State a result that follows directly from the preceding theorem.
> **Proof**: Explain how the corollary follows from the theorem, noting any additional assumptions or substitutions.

### Formulas

**Example Formula**
Describe the relationship expressed by the formula and define its variables.
$$  
\text{Example expression}  
$$

### Visual Aids

**Example Comparison [Table]**

|Criterion|Example Case A|Example Case B|
|---|---|---|
|Property 1|Value or description|Value or description|
|Property 2|Value or description|Value or description|
|Property 3|Value or description|Value or description|

**Example Process or Structure [Diagram]**

> Insert a diagram illustrating the relevant process, structure, hierarchy, mapping, or relationship.

### Notable Quotes

- **Example Author**: “Insert a relevant quotation here.”

### Common Pitfalls

- **Example Pitfall**: Describe a common misconception, invalid assumption, implementation error, or misuse of a method.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
