# Chapter 1: Matching, Covering, and Packing
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## 1.0 Matching In Bipartite Graphs
---
### Key Concepts
- **Packing Problem**:
  - Find in a given graph as many disjoint subgraphs as possible belonging to a given class of graphs.
- **Covering Problem**:
  - How few vertices of G suffice to meet all its subgraphs isomorphic to a graph class.
### Definitions
- **Matching**
  - Set of independent edges in a graph.
  - M is a matching of $U \subseteq V(G)$ if every vertex in U is incident with an edge in M.
  - Vertices incident with an edge in M are said to be matched.
- **K-Factor**
  - k-regular spanning subgraph.
- **Alternating Path**
  - Starts at an unmatched vertex and contains, alternately, edges from $E \backslash M$ and from matching M.
- **Augmenting Path**
  - Alternating path that ends in an unmatched vertex of the other partition set.
  - $M \Delta E(P)$ is again a matching and set of matched vertices increases by two, the ends of P.
- **Vertex Cover**
  - $U \subseteq V(G)$ where every edge of G is incident with a vertex in U.
- **Set Of Preferences**
  - Family $(\le_v)_{v\in V}$ of linear orderings $\le_v$ on $E(v)$.
- **Stable Matching**
  - For every edge $e \in E \backslash M$ there is an edge $f \in M$ such that e and f have a common vertex v with $e <_v f$.

### Theorems & Proofs
**Theorem 2.1.1**
The maximum cardinality of a matching in bipartite graph with partitions $\{A, B\}$ is equal to the minimum cardinality of a vertex cover of its edges.

Let M be a matching in G of maximum cardinality. From every edge in M let us choose one of its ends: its end in B if some alternating path ends in that vertex, and its end in A otherwise. We shall prove that the set U of these $|M|$ vertices covers E; since any vertex cover of E must cover M, there can be none with fewer than $|M|$ vertices, and so the theorem will follow. Note that if an alternating path P ends in a vertex $b \in B$, then $b \in U$: as M is a largest matching, P is not an augmenting path, so b is matched to some $a \in A$ and was put in U when we considered the edge $ab \in M$ while constructing U. To show that U covers E, let an edge $ab \in E$ be given. If $a \in U$ we are done, so assume $a \not \in U$. To prove $b \in U$, it suffices to show that some alternating path ends in b. If a is unmatched, then ab is such a path. If not, we have $ab' \in M$ for some $b' \in B$. Since $a \not \in U$, there exists an alternating path P ending in $b'$. Depending on whether or not $b \in P$, either $Pb$ or $Pb'ab$ is an alternating path ending in b. $\blacksquare$

**Theorem 2.1.2**
G contains a matching of A iff $|N(S) \ge |S|$ for all $S \subseteq A$ of bipartite graph G with partitions $\{A, B\}$.

The forward direction is clear, just unpack the definition.
First proof:
We show that for every matching M of G that leaves a vertex $a \in A$ unmatched there is an augmenting path with respect to M. Let $A'$ and $B'$ be the sets of vertices in A and B that can be reached by an alternating path from a. Any such path ending at an unmatched $b' \in B'$ is augmenting, so we may assume that all $b' \in B'$ are matched. Their M-neighbors clearly lie in $A'$, but $a \in A'$ is not among these. Hence by the marriage condition, $A'$ also sends an edge $a'b$ to a vertex $b \not \in B'$. Appending this edge to an alternating $a-a'$ path yields an alternating $a-b$ path. This places b in $B'$, contradicting its choice. $\blacksquare$

**Corollary 2.1.3**
Every k-regular ($k \ge 1$) bipartite graph has a 1-factor.

If G is k-regular, then clearly $|A| = |B|$; it thus suffices to show by theorem 2.1.2 that G contains a matching of A. Now every set $S \subseteq A$ is joined to $N(S)$ by a total of $k|S|$ edges, and these are among the $k|N(S)|$ edges of G incident with $N(S)$. Therefore $k|S| \le k|N(S)|$, so G does indeed satisfy the marriage condition. $\blacksquare$

**Theorem 2.1.4**
For every set of preferences, a bipartite graph has a stable matching.

Call a matching

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