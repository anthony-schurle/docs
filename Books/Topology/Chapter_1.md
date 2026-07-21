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
### Definitions
- **Components**
  - Equivalence classes of X where x ~ y if there is a connected subspace of X containing both x and y.
  - Symmetric, reflexive, and transitive.
  - Closed and (if finite components) open.
- **Path Components**
  - Equivalence classes of X where x ~ y if there is a path in X from x to y.
  - Equivalence relation.
- **Locally Connected**
  - Space X is locally connected at x if for every neighborhood U of x, $\exists$ connected neighborhood V of x contained in U. If X is locally connected at each of its points, its said to be locally connected.
  - Each real interval is both connected and locally connected.
  - $[-1, 0) \cup (0, 1]$ of $\mathbb{R}$ is not connected, but it is locally connected.
  - The topologist's sine curve is connected but not locally connected.
  - The rationals are neither connected nor locally connected.
- **Locally Path Connected**
  - Space X is locally path connected at x if for every neighborhood U of x, $\exists$ a path-connected neighborhood V of x contained in U. If X is locally path connected at each of its points, then it is said to be locally path connected.

### Theorems & Proofs
**Theorem 25.1**
The components of X are connected disjoint subspaces of X whose union is X, such that each nonempty connected subspace of X intersects only one of them.

**Theorem 25.2**
The path components of X are path-connected disjoint subspaces of X whose union is X, such that each nonempty path-connected subspace of X intersects only one of them.

**Theorem 25.3**
A space is locally connected iff $\forall$ open set U of X, each component of U is open in X.

**Theorem 25.4**
A space X is locally path connected iff $\forall$ open set U of X, each path component of U is open in X.

**Theorem 25.5**
If X is a topological space, each path component of X lies in a component of X. If X is locally path connected, then the components and the path components of X are the same.

### References
- *Book Title* — Chapter X, Pages Y–163


## 1.3 Compact Spaces
---
### Definitions
- **Cover**
  - Collection $A$ of subsets of a space X covers X, or is a covering of X, if $\bigcup A = X$. It is called an open covering if its elements are open subsets of X.
  - If Y is a subspace of X, a collection $A$ of subsets of X is said to cover Y if $Y \subseteq \bigcup A$.
- **Compact**
  - Space X is compact if every open covering $A$ of X contains a finite subcollection that also covers X.
- **Finite Intersection Property**
  - A collection $C$ of subsets of X is said to have this property if for every finite subcollection $\{C_1, ..., C_n\}$ of C, the intersection $C_1 \cap ... \cap C_n$ is nonempty.

### Theorems & Proofs
**Lemma 26.1**
Let Y be a subspace of X. Then Y is compact iff every covering of Y by sets open in X contains a finite subcollection covering Y.

**Theorem 26.2**
Every closed subspace of a compact space is compact.

**Theorem 26.3**
Every compact subspace of a Hausdorff space is closed.

**Lemma 26.4**
If Y is a compact subspace of the Hausdorff space X and $x_0$ is not in Y, then there exist disjoint open sets U and V of X containing $x_0$ and Y, respectively.

**Theorem 26.5**
The image of a compact space under a continuous map is compact.

**Theorem 26.6**
Let $f: X \to Y$ be a bijective continuous function. If X is compact and Y is Hausdorff, then f is a homeomorphism.

**Theorem 26.7**
The product of finitely many compact spaces is compact.

**Lemma 26.8**
Consider the product space $X \times Y$, where $Y$ is compact. If N is an open set of $X \times Y$ containing the slice $x_0 \times Y$ of $X \times Y$, then N contains some tube $W \times Y$ about $x_0 \times Y$, where W is a neighborhood of $x_0$ in X.

**Theorem 26.9**
Let X be a topological space. Then X is compact iff for every collection C of closed sets in X having the finite intersection property, the intersection $\bigcap_{c \in C}c$ of all elements of C is nonempty.

### References
- *Book Title* — Chapter X, Pages Y–172


## 1.4 Compact Subspaces Of The Real Line
---
### Definitions
- **Distance**
  - Let $(X, d)$ be a metric space; let A be a nonempty subset of X. For each $x \in X$, we define the distance from x to A by $d(x, A) = inf\{d(x, a) | a \in A\}$.
- **Isolated Point**
  - A point x of space X such that the one point set $\{x\}$ is open.

### Theorems & Proofs
**Theorem 27.1**
Let X be a simply ordered set having the least upper bound property. In the order topology, each closed interval in X is compact.

**Corollary 27.2**
Every closed interval in $\mathbb{R}$ is compact.

**Theorem 27.3**
A subspace A of $\mathbb{R}^n$ is compact iff it is closed and is bounded in the euclidean metric d or the square metric p.

**Theorem 27.4**
Let $f : X \to Y$ be continuous, where Y is an ordered set in the order topology. If X is compact, then there exist points c and d in X such that $f(c) \le f(x) \le f(d)$ for every $x \in X$.

**Theorem 27.7**
Let X be nonempty compact Hausdorff space. If X has no isolated points, then X is uncountable.

**Corollary 27.8**
Every closed interval in $\mathbb{R}$ is uncountable.

### References
- *Book Title* — Chapter X, Pages Y–178


## 1.5 Limit Point Compactness
---
### Definitions
- **Limit Point Compact**
  - Space X is limit point compact if every infinite subset of X has a limit point.

### Theorems & Proofs
**Theorem 28.1**
Compactness implies limit point compactness, but not conversely.

### References
- *Book Title* — Chapter X, Pages Y–
