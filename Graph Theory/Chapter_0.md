# Chapter 0: Chapter Title
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 0.0 Graphs
---
### Key Concepts
- **Concept Name**:
  - Subpoint or clarification.
### Definitions
- **Graph**
  - Pair of sets $G = (V, E)$ such that $E \subseteq [V]^2$.
  - Assume $V \cap E = \emptyset$.
  - Vertices are elements of V and the vertex set is notated by $V(G)$.
  - Edges are elements of E written typically as $\{x, y\}$ or $xy$ and the edge set is notated by $E(G)$.
  - All edges at vertex v denoted by $E(v)$.
  - $E(X, Y) = \{xy \in E(G) : x \in X, y \in Y\}$.
  - Empty graph $(\emptyset, \emptyset$) denoted by $\emptyset$.
- **Order**
  - Number of vertices in a graph, denoted by $|G|$.
  - Determines if a graph is finite, infinite, or countable.
- **Graph Edge Count**
  - Denoted by $||G||$.
- **Trivial Graph**
  - Order 0 or 1.
- **Incident**
  - Vertex v is incident with an edge e if $v \in e$.
  - Both vertices incident with an edge are its ends and the edge joins these vertices.
- **Neighbors**
  - For $x, y \in G$, x and y are neighbors if $\{x, y\} \in E(G)$.
- **Adjacent Edges**
  - For $e, f \in E(G) \land e \ne f$, e and f are adjacent if $\exists v \in V(G) (v \in e \land v \in f)$.
- **Complete Graph**
  - All vertices of a graph are pairwise adjacent.
  - Notated as $K^n$ for n vertices.
  - $K^3$ specifically is called a triangle.
- **Independent**
  - Set of non-adjacent vertices or edges.
  - Independent vertex sets called stable.
- **Homomorphic**
  - Define $G = (V, E)$ and $G' = (V', E')$. Let $\phi: V \to V'$. If $\{\phi(x), \phi(y)\} \in E'$ whenever $\{x, y\} \in E$.
  - $\forall x' \in Im(\phi)$, $Im(\phi^{-1}(x'))$ is an independent set of vertices in G.
- **Isomorphic**
  - If $\phi$ is bijective and $\phi^{-1}$ is also a homomorphism, notated with $\cong$.
  - Automorphism arises from applying an isomorphism of a graph to itself.
  - Abstract graph is considered up to isomorphism.
- **Graph Property**
  - Class of graphs closed under isomorphism.
- **Graph Invariant**
  - Map takes graphs as arguments and assigns equal values to isomorphic graphs.
- **Graph Operations**
  - $G \cup G' := (V \cup V', E \cup E')$.
  - $G \cap G' := (V \cap V', E \cap E')$.
  - $G - U := G[V \backslash U]$. ($G - V(G') \equiv G - G'$)  ($\forall F \subseteq [V]^2 (G - F := (V, E \backslash F))$)
  - $\forall F \subseteq [V]^2 (G + F := (V, E \cup F)$).
  - If G and G' are disjoint, $G * G' := G \cup G' + \{uv : u \in V(G), v \in V(G')$.
- **Disjoint Graphs**
  - $G \cap G' = \emptyset$.
- **Subgraph, Supergraph, and Proper Subgraph**
  - $V' \subseteq V \land E' \subseteq E$, then $G' \subseteq G$ which is also written as $
  - $G' \subseteq G \land G' \ne G$, then $G' \subset G$.
- **Induced Subgraph**
  - If $G' \subseteq G$ contains all edges $xy \in E$ with $x, y \in V'$, then V' induces or spans G' in G such that $G[V'] := G'$.
- **Spanning Subgraph**
  - If $G' \subseteq G$ and V' spans all of G.
- **Edge Maximal**
  - Graph that holds a property but no other graph $(V, F)$ with $E \subset F$ does.
- **Maximal\Minimal**
  - Graph that holds a property no other subgraph relation, with ordering specified by "maximal" or "minimal", holds it.
- **Complement Graph**
  - $\overline{G} = (V(G), [V]^2 \backslash V(E))$.
- **Line Graph**
  - $L(G)$ of G is the graph on E in which $x, y \in E$ are adjacent as vertices iff they are adjacent as edges in G.
### Algorithms
**Algorithm Name**
Description.
```pseudo
1. Step 1
2. Step 2
3. Step 3
```
### Code Snippets
**Snippet Name**
Description.
```program
// code
```
### Theorems & Proofs
**Theorem Name**
Proof.
### Formulas
**Formula Name**
Description.
$$
Equation
$$
### Visual Aids
| Header | Header |
| - | - |
| Content | Content |
![Diagram]()
### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.
### Notable Quotes
> “Notable quote."
### Common Pitfalls
- Pitfall 1.
### Related Links
- [Link]()
### References
- *Book Title* — Chapter X, Pages Y–Z

- [Author(s), "Paper or Article Title," Journal or Conference Name, Year]() 

- [Related Chapter in This Wiki]()  

- [Official Specification or Standard Document (PDF/URL)]()  

- Class Lecture ([Link]())