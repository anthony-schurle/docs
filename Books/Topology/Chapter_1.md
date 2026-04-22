# Chapter 1: Connectedness And Compactness
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 1.0 Connected Spaces
---
### Definitions
- **Connected**
  - A space X is connected if there does not exist a separation on X - a pair U, V of disjoint nonempty open subsets of X whose union is X.
  - A space X is connected iff the only subsets of X that are both open and closed in X are the empty set and X itself.

### Theorems & Proofs
**Lemma 23.1**
If Y is a subspace of X, a separation of Y is a pair of disjoint nonempty sets A and B whose union is Y, neither of which contains a limit point of the other. The space Y is connected if there exists no separation of Y.

**Lemma 23.2**
If the sets C and D form a separation of X, and if Y is a connected subspace of X, then Y lies entirely within either C or D.

**Theorem 23.3**
The union of a collection of connected subspaces of X that have a point in common is connected.

**Theorem 23.4**
Let A be a connected subspace of X. If $A \subseteq B \subseteq \overline{A}$, then B is also connected.

**Theorem 23.5**
The image of a connected space under a continuous map is connected.

**Theorem 23.6**
A finite cartesian product of connected spaces is connected.

### References
- *Book Title* — Chapter X, Pages Y–152


## 1.1 Connected Subspaces Of The Real Line
---
### Definitions
- **Linear Continuum**
  - Simply ordered set L having more than one element where the following hold:
  - L has the least upper bound property.
  - If $x < y$, there exists z such that $x < z < y$.
- **Path**
  - Given $x,y \in X$, a path in X from x to y is a continuous map $f ; [a, b] \to X$ of some closed interval in the real into X, such that $f(a) = x$ and $f(b) = y$.
- **Path Connected**
  - Every pair of points of X can be joined by a path in X.
  - Space is then connected, trivially shown.
  - Examples: unit ball, punctured euclidean space when $n > 1$, unit sphere when $n > 1$.

### Theorems & Proofs
**Theorem 24.1**
If L is a linear continuum in the order topology, then L is connected, and so are the intervals and rays in L.

Use contradiction and the upper bound on one of the separators for a convex subspace.

**Corollary 24.2**
The real line is connected and so are the intervals and rays in it.

**Theorem 24.3**
Let $f: X \to Y$ be a continuous map, where X is a connected space and Y is an ordered set in the order topology. If a and b are two points of X and if r is a point of Y lying between $f(a)$ and $f(b)$, then there exists a point c of X such that $f(c) = r$.

### References
- *Book Title* — Chapter X, Pages Y–159


## 1.2 Components And Local Connectedness
---
### Key Concepts
- **Concept Name**:
  - Subpoint or clarification.
### Definitions
- **Components**
  - Equivalence classes of X where x ~ y if there is a connected subspace of X containing both x and y.
  - Symmetric, reflexive, and transitive.
  - Closed and (if finite components) open.
- **Path Components**
  - Equivalence classes of X where x ~ y if there is a path in X from x to y.
  - Equivalence relation.

### Theorems & Proofs
**Theorem 25.1**
The components of X are connected disjoint subspaces of X whose union is X, such that each nonempty connected subspace of X intersects only one of them.

**Theorem 25.2**
The path components of X are path-connected disjoint subspaces of X whose union is X, such that each nonempty path-connected subspace of X intersects only one of them.

### References
- *Book Title* — Chapter X, Pages Y–
