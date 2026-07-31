# Chapter Number: Matching Covering And Packing

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 2.1 Matching In Bipartite Graphs

---

### Key Concepts

- **Packing Problem**: Find in a given graph as many disjoint subgraphs as possible that are each isomorphic to a given class of graphs.
- **Covering Problem**: How few vertices of a graph are needed to all its subgraphs isomorphic to a graph in a class.

### Definitions

- **Matching**: Set $M$ of independent edges of graph $G$.
- **Matched**: If every vertex of $U \subseteq V(G)$ is incident with an edge in $M$, then $U$ is matched by $M$. Similar notion given to unmatched.
- **k-Factor**: k-regular spanning subgraph.
- **Alternating Path**: Path starting at an unmatched vertex in a bipartite graph and alternates between matching edges and edges not in the matching.
- **Augmented Path**: Alternating path ending at an unmatched vertex not in the same partition as the start vertex.
- **Vertex Cover**: For a graph $G$, $U \subseteq V(G)$ is a vertex cover of $E(G)$ if every edge of $G$ is incident with a vertex in $U$.
- **Set Of Preferences**: Family $(\le_v)_{v \in V(G)}$ of linear orderings $\le_v$ on $E(v)$ for graph $G$.
- **Stable**: Matching $M$ is stable in graph $G$ if for every edge $e \in E(G) \backslash M$ there $\exists f \in M$ such that $e$ and $f$ have common vertex $v$ with $e <_v f$. 

### Results & Proofs

**Theorem: Theorem 2.1.1**
The maximum cardinality of a matching in $G$, a bipartite graph, is equal to the minimum cardinality of a vertex cover of its edges.

**Theorem: Marriage Theorem**
A bipartite graph contains a matching of $A$ iff $|N(S)| \ge |S|$ for all $S \subseteq A$.

**Corollary: Corollary 2.1.3**
Every k-regular bipartite graph has a 1-factor.

**Theorem: Stable Marriage Theorem**
For every set of preferences, a bipartite graph has a stable matching.

**Corollary: Corollary 2.1.5**
Every regular graph of positive even degree has a 2-factor.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -43


## 2.2 Matching In General Graphs

---

### Key Concepts

- **Example Concept**: A concise explanation of a foundational concept.

### Definitions

- **Odd Component**: Component of odd order, sometimes denoted $q(G)$ for a graph $G$.
- **Factor Critical**: Non-empty graph $G$ with no 1-factor but for every $v \in V(G)$, $G-v$ has a 1-factor.
- **Matchable**: Vertex set $S \subseteq V(G)$ is matchable to the components of $G-S$ if the bipartite graph $G_S := (S \cup \mathcal{C}_{G-S}, \{sC | \exists C \in \mathcal{C}_{G-S} \exists c \in C (sc \in E(G))\})$ contains a matching of $S$.

### Examples

**Basic Example**
Present a simple case that demonstrates the preceding definitions or concepts.
> Presented example...

### Axioms

- **Example Axiom**: A foundational assumption used within the subject area.

### Results & Proofs

**Theorem: Tutte's Theorem**
A graph $G$ has a 1-factor iff $q(G - S) \le |S|$ for all $S \subseteq V(G)$.

**Corollary: Corollary 2.2.2**
Every bridgeless cubic graph has a 1-factor.

**Theorem: Theorem 2.2.3**
Every graph $G$ has a set $S$ of vertices with the following two properties:
(i) $S$ is matchable to $\mathcal{C}_{G-S}$
(ii) Every component of $G-S$ is factor-critical.
Given any such set $S$, the graph $G$ contains a 1-factor iff $|S| = |\mathcal{C}_{G-S}|$.

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
