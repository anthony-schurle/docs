# Chapter 0: Chapter Title
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 0.0 Graphs
---
### Definitions
- **Graph**
  - Pair of sets $G = (V, E)$ such that $E \subseteq [V]^2$.
  - Assume $V \cap E = \emptyset$.
  - Vertices are elements of V and the vertex set is notated by $V(G)$.
  - A graph is said to be on V.
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
  - Vertex v is incident with an edge e if $v \in e$ and edge e is at v.
  - Set of all the edges E at a vertex v is denoted by $E(v)$.
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
  - $V' \subseteq V \land E' \subseteq E$, then $G' \subseteq G$ which can be written as $G[V(G')]$.
  - $G' \subseteq G \land G' \ne G$, then $G' \subset G$ which can be written as $G[V(G')]$.
- **Induced Subgraph**
  - If $G' \subseteq G$ contains all edges $xy \in E$ with $x, y \in V'$, then V' induces or spans G' in G such that $G[V'] := G'$.
- **Spanning Subgraph**
  - If $G' \subseteq G$ and V' spans all of G.
- **Edge Maximal**
  - Graph that holds a property but no other graph $(V, F)$ with $E \subset F$ does.
- **Maximal\Minimal**
  - Graph that holds a property no other subgraph relation, with ordering specified by "maximal" or "minimal", holds it. For edges and vertices, this is determined by set inclusion.
- **Complement Graph**
  - $\overline{G} = (V(G), [V]^2 \backslash V(E))$.
- **Line Graph**
  - $L(G)$ of G is the graph on E in which $x, y \in E$ are adjacent as vertices iff they are adjacent as edges in G.

### References
- *Book Title* — Chapter X, Pages Y–4


## 0.1 The Degree Of A Vertex
---
### Definitions
- **Neighbors**
  - Set of neighbors for vertex v denoted by $N_G(v)$.
  - For $U \subseteq V$, the neighbors in $V \backslash U$ of vertices in U are neighbors of U denoted $N(U)$.
- **Degree**
  - $d_G(v)$ of vertex v is $|E(v)|$ which is the same as neighbors of v.
  - Vertex with degree 0 is called isolated.
  - $\delta (G) := min\{d(v) : v \in V \}$ is the minimum degree of a graph.
  - $\Delta (G) := max\{d(v) : v \in V \}$ is the maximum degree of a graph.
  - $\epsilon(G) := \frac{|E|}{|V|}$.
  - $|E| = 0.5\sum_{v \in V}d(v) = 0.5d(G)|V|$ and so $\epsilon(G) = 0.5d(G)$.
  - Average degree of a graph is $d(G) := \frac{1}{|V|}\sum_{v \in V}d(v)$.
  - Clearly, $\delta(G) \leq d(G) \le \Delta(G)$.
- **K-Regular**
  - All vertices of G has degree k.
  - 3-regular is called cubic.

### Theorems & Proofs
**Proposition 1.2.1**
The number of odd degree vertices in a graph is always even.

As $|E| = 0.5\sum_{v \in V}d(v)$ is an integer, $\sum_{v \in V}d(v)$ is even. $\blacksquare$

**Proposition 1.2.2**
Every graph G with at least one edge has a sub-graph H with $\delta(H) > \epsilon(H) \ge \epsilon(G)$.

Construct a sequence $G = ... \subseteq G_1 \subseteq G_0$ of induced subgraphs of G as follows. If $G_i$ has a vertex $v_i$ of degree $d(v_i) \le \epsilon(G_i)$, we let $G_{i+ 1} := G_i - \{v\}$; if not, we terminate our sequence and set $H := G_i$. By the choices of $v_i$ we have $\epsilon (G_{i + 1}) \ge \epsilon(G_i)$ for all i, and hence $\epsilon(H) \ge \epsilon(G)$. Since $\epsilon(K^1) = 0 < \epsilon(G)$, none of the graphs in our sequence is trivial, so in particular $H \ne \emptyset$. This implies $\delta(H) > \epsilon(H)$. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–6


## 0.2 Paths And Cycles
---
### Key Concepts
- **Bounding Order**:
  - $n_0(d, g) := \begin{cases} 1 + d\sum_{i = 0}^{r - 1}(d - 1)^i & \text{if } 2r + 1 := g,\\ 2\sum_{i = 0}^{r - 1}(d - 1)^i  & \text{if } 2r := g. \end{cases}$ where $d \in \mathbb{R}$ and $g \in \mathbb{N}$.
  - $|G| \ge n_0(\delta, g)$.
### Definitions
- **Path**
  - Non-empty graph $P = (V, E)$ of the form $V = \{x_0, x_1, ..., x_k\}$ and $E = \{x_0x_1, x_1x_2, ..., x_{k-1}x_k\}$ where all $x_i$ are distinct.
  - $x_0$ and $x_k$ linked by P and are the ends.
  - $x_1, x_2, ..., x_{k-1}$ are the inner vertices.
  - $P^k$ denotes path length of k, measured by number of edges.
  - Notated by vertices with $P = x_0x_1...x_k$.
  - $Px_i := x_0...x_i$.
  - $x_iP := x_i...x_k$.
  - $x_iPx_j := x_i...x_j$.
  - $\mathring{P} := x_1...x_{k-1}$.
  - $P\mathring{x_i} := x_0...x_{i - 1}$.
  - $\mathring{x_i}P := x_{i+1}...x_{k}$.
  - $\mathring{x_i}P\mathring{x_j} := x_{i+1}...x_{j-1}$.
  - P is an A-B path if $V(P) \cap A = \{x_0\}$ and $V(P) \cap B := \{x_k\}$.
  - Non-trivial path P is an A-Path for vertex set A if P has its A-path ends but no inner vertex in A.
  - Non-trivial path P is an H-Path for graph H if it is a $V(H)$-Path and, if it has length 1, its edges do not lie in H.
- **Independent Paths**
  - None of the paths contain an inner vertex of the other.
- **Cycle**
  - $C := P + \{x_{k-1}x_0\}$ where $k \ge 3$.
  - Denoted by vertices with $x_0...x_{k-1}x_0$.
- **Girth**
  - $g(G)$ is the minimum length of a cycle contained in graph G.
  - The value is $\infty$ if G does not contain a cycle.
- **Circumference**
  - Maximum length of a cycle contained in graph G.
  - The value is 0 if G does not contain a cycle.
- **Chord**
  - Edge that joins two vertices of a cycle but is not an edge in the cycle.
- **Induced Cycle**
  - A cycle in a graph forming an induced subgraph, has no cords.
- **Distance**
  - $d_G(x, y)$ is the length of the shortest x-y path in G.
  - If no path exists, distance is infinite.
- **Diameter**
  - Greatest distance between any two vertices in a graph denoted $diam(G)$.
- **Central**
  - Vertex is central in G if its greatest distance from any other vertex is as small as possible.
- **Radius**
  - Greatest distance of central vertex to any other vertex.
  - $rad(G) = min_{x \in V(G)}max_{y \in V(G)}d_G(x, y)$.
  - $rad(G) \le diam(G) \le 2rad(G)$.
- **Walk**
  - Non-empty alternating sequence $v_0e_0v_1e_1...e_{k-1}v_k$ of vertices and edges such that $e_i = \{v_i, v_{i + 1}\}$ for all $i < k$.
  - Walk is closed if $v_0 = v_k$. 
  - If the vertices are distinct, defines a path.
  - Every walk between two vertices contains a path between these vertices.

### Theorems & Proofs
**Proposition 1.3.1**
Every graph G contains a path of length $\delta(G)$ and a cycle of length at least $\delta(G) + 1$ (provided that $\delta(G) \ge 2$).

Let $x_0...x_k$ be the longest path in G. Then all the neighbors of $x_k$ lie on this path. Hence $k \ge d(x_k) \ge \delta(G)$. If $i < k$ is minimal with $x_ix_k \in E(G)$, then $x_i...x_kx_i$ is a cycle of length at least $\delta(G) + 1$. $\blacksquare$

**Proposition 1.3.2**
Every graph G containing a cycle satisfies $g(G) \le 2diam(G) + 1$.

Let C be a shortest cycle in G. If $g(G) \ge 2diam(G) + 2$, then C has two vertices whose distance in C is at least $diam(G) + 1$. In G, these vertices have a lesser distance; any shortest path P between them is therefore not a subgraph of C. Thus, P contains a C-path xPy. Together with the shorter of the two x-y paths in C, this path xPy forms a shorter cycle than C, a contradiction. $\blacksquare$

**Proposition 1.3.3**
A graph of radius at most k and maximum degree at most $d \ge 3$ has fewer than $\frac{d}{d - 2}(d- 1)^k$ vertices.

Let z be a central vertex in G, and let $D_i$ denote the set of vertices of G at distance i from z. Then $V(G) = \bigcup_{i = 0}^k D_i$. Clearly, $|D_0| = 1$ and $|D_1| \le d$. For $i \ge 1$ we have $|D_{i + 1}| \le (d-1)|D_i|$, because every vertex in $D_{i + 1}$ is a neighbor of a vertex in $D_i$, and each vertex in $D_i$ has at most $d - 1$ neighbors in $D_{i + 1}$. Thus $|D_{i + 1}| \le d(d- 1)^i$ for all $i < k$ by induction, giving
$$
|G| \le 1 + d\sum_{i = 0}^{k - 1}(d - 1)^i = 1 + \frac{d}{d-2}((d - 1)^k - 1) < \frac{d}{d - 2}(d - 1)^k
$$
$\blacksquare$

**Theorem 1.3.4**
Let G be a graph. If $d(G) \ge d \ge 2$ and $g(G) \ge g \in \mathbb{N}$ then $|G| \ge n_0(d, g)$ where $n_0(d, g) := \begin{cases} 1 + d\sum_{i = 0}^{r - 1}(d - 1)^i & \text{if } 2r + 1 := g,\\ 2\sum_{i = 0}^{r - 1}(d - 1)^i  & \text{if } 2r := g. \end{cases}$.

**Corollary 1.3.5**
If $\delta(G) \ge 3$ then $g(G) < 2log|G|$.

If $g := g(G)$ is even then ,
$$
n_0(3, g) = 2\frac{2^{0.5g}- 1}{2 - 1} = 2^{0.5g} + (2^{0.5g} - 2) > 2^{0.5g}
$$
while if g is odd then,
$$
n_0(3, g) = 1 + 3\frac{2^{0.5(g - 1)} - 1}{2 - 1} = \frac{3}{\sqrt{2}}2^{0.5g} - 2 > 2^{0.5g}
$$
As $|G| \ge n_0(3, g)$, the result follows. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–10


## 0.3 Connectivity
---
### Definitions
- **Connected**
  - Graph is non-empty and any two of its vertices are linked by a path in G.
  - If $U \subseteq V(G)$ and $G[U]$ is connected, U it connected in G.
- **Component**
  - Maximal connected subgraph of G.
  - Clearly, these are induced subgraphs and their vertex set partition V.
- **Separates**
  - If $A,B \subseteq V$ and $X \subseteq V \cup E$ are such that every $A-B$ path in G contains a vertex or an edge from X, we say that X separates the sets A and B in G.
  - Implies $A \cap B \subseteq X$.
  - X separates a graph if it separates some two vertices in the graph.
  - $\{A, B\}$ is a separation of G if $A \cup B = V$ and G has no edge between $A \backslash B$ and $B \backslash A$, the separation is proper if both $A \backslash B$ and $B \backslash A$ are non-empty.
  - The order of separation $\{A, B\}$ is $|A \cap B|$ and the sets A, B are its sides.
- **Cutvertex**
  - Vertex separates two other vertices of the same component.
- **Bridge**
  - Edge separates its ends of the same component.
  - Do not lie on any cycle.
- **K-Connected**
  - If $|G| > k$ and $G - X$ is connected for every set $X \subseteq V$ with $|X| < k$.
  - Every (non-empty) graph is 0-connected.
  - Non-trivial connected graphs are 1-connected.
- **Connectivity**
  - Greatest integer k such that G is k-connected denoted $\kappa(G)$.
  - $\kappa(K^n) = n - 1$ for all $n \ge 1$.
- **l-edge-connected**
  - If $|G| > 1$ and $G - F$ is connected for every set $F \subseteq E$ with $|F| < l$.
- **Edge-Connectivity**
  - Greatest integer l such that G is l-edge-connected denoted $\lambda(G)$.
  - If G is disconnected $\lambda(G) = 0$.

### Theorems & Proofs
**Proposition 1.4.1**
The vertices of a connected graph G can always be enumerated, say as $v_1, ..., v_n$, so that $G_i := G[v_1,...,v_i]$ is connected for every i.

Pick any vertex as $v_1$, and assume inductively that $v_1, ..., v_i$ have been chosen for some $i < |G|$. Now pick a vertex $v \in G - G_i$. As G is connected, it contains a $v-v_1$ path P. Choose as $v_{i + 1}$ the last vertex of P in $G -G_i$; then $v_{i+1}$ has a neighbor in $G_i$. The connectedness of every $G_i$ follows by induction on i. $\blacksquare$

**Proposition 1.4.2**
If G is non-trivial then $\kappa(G) \le \lambda(G) \le \delta(G)$.

The second inequality follows from the fact that all edges incident with a fixed vertex separate G. For the first, let F be a set of $\lambda(G)$ edges such that $G- F$ is disconnected. Such a set exists by definition of $\lambda$; note that F is a minimal separating set of edges in G. We show that $\kappa(G) \le |F|$. Suppose that G has a vertex v that is not incident with an edge in F. Let C be the component of $G - F$ containing v. Then the vertices of C that are incident with an edge in F separate v from $G - C$. Since no edge in F has both ends in C (by minimality of F), there are at most $|F|$ such vertices, giving $\kappa(G) \le |F|$ as desired. Suppose now that every vertex is incident with an edge in F. Let v be any vertex, and let C be the component of $G - F$ containing v. Then the neighbors w of v with $vw \not \in F$ lie in C and are incident with distinct edges in F, giving $d_G(v) \le |F|$. As $N_G(v)$ separates v from any other vertices in G, this yields $\kappa(G) \le |F|$ - unless there are no other vertices. But v was an arbitrary vertex. So we may assume that G is complete, giving $\kappa(G) = \lambda(G) = |G| - 1$. $\blacksquare$

**Theorem 1.4.3**
Let $0 \ne k \in \mathbb{N}$. Every graph G with $d(G) \ge 4k$ has a k-connected subgraph. In fact, every such G has $(k +1)$-connected subgraph H such that $d(H) > d(G) - 2k \ge 2k$.

Put $\gamma := \epsilon(G) (\ge 2k)$, and consider the subgraphs $G' \subseteq G$ such that,
$$
|G'| \ge 2k \land ||G'|| > \gamma(|G'|- k)
$$
Such graphs $G'$ exist since G is one; let H be one of smaller order. No graph $G'$ can have order exactly 2k, since this would imply that $||G'|| > \gamma k \ge 2k^2 > \begin{pmatrix} |G'| \\ 2 \end{pmatrix}$. The minimality of H therefore implies that $\delta(H) > \gamma$: otherwise we could delete a vertex of degree at most $\gamma$ and obtain a graph $G' \subseteq H$ still satisfying the above conditions. In particular we have $|H| \ge \gamma$. Dividing the inequality of $||H|| > \gamma |H| - \gamma k$ from the conditions by $|H|$ therefore yields $\epsilon(H) > \gamma - k$ as desired. If H is not $k+1$-connected, then H has a proper separation $\{U_1, U_2\}$ of order at most k; put $H_i := H[U_i]$. Since any vertex $v \in U_1 \backslash U_2$ has all its $d(v) \ge \delta(H) > \gamma$ neighbors from H in $H_1$, we have $|H_1| \ge \gamma \ge 2k$. Similarly, $|H_2| \ge 2k$. As by the minimality of H neither $H_1$ nor $H_2$ satisfies the conditions, we thus have $||H_i|| \le \gamma(|H_i| - k)$ for $i = 1,2$. But then $||H|| \le ||H_1|| + ||H_2 \le \gamma(|H_1| + |H_2| - 2k) \le \gamma (|H| - k)$ which contradicts the conditions for H. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–13


## 0.4 Trees And Forests
---
### Key Concepts
- **Concept Name**:
  - Subpoint or clarification.
### Definitions
- **Forest**
  - Acyclic graph.
  - Components are trees.
- **Tree**
  - Connected forest.
  - Leaves are vertices with degree 1.
  - Vertices that are not leaves are inner vertices.
  - Has at least one leaf if non-trivial.
  - $xTy$ is the unique path in a tree T between vertices x and y.
  - When taking a spanning tree, the chords of T in G are the edges $E(G) \backslash E(T)$.
  - root is a special vertex.
- **Rooted Tree**
  - Fixed root r.
- **Tree-Order**
  - Partial ordering of $V(T)$ defined by $x \le y$ where $x \in rTy$.
  - Symbolic of height of a tree.
  - If $x < y$, x lies below y in T.
  - root of T is the least element in the partial ordering.
  - Down-closure: $\lceil y \rceil := \{x : x \le y \}$.
  - Up-closure: $\lfloor y \rfloor := \{y : y \ge x \}$.
  - Closures are comparable chains.
  - Closed-Upwards: $X = \lfloor X \rfloor := \bigcup_{x \in X}\lfloor x \rfloor$.
  - Closed-Downwards: $X = \lceil X \rceil := \bigcup_{x \in X}\lceil x \rceil$.
- **Tree Height**
  - Distance k from the root of a tree have height k.
  - Vertices at height k form the kth level of a tree.

### Theorems & Proofs
**Theorem 1.5.1**
The following assertions are equivalent for a graph T:
(i) T is a tree;
(ii) Any two vertices of T are linked by a unique path in T;
(iii) T is minimally connected, i.e. T is connected but $T - e$ is disconnected for every edge $e \in T$.
(iv) T is maximally acyclic, i.e. T contains no cycle but $T + xy$ does, for any two non-adjacent vertices $x, y \in T$.

**Corollary 1.5.2**
A connected graph with n vertices is a tree iff it has $n - 1$ edges.

($\implies$) Enumerate the vertices of a tree T as in Proposition 1.4.1. As T is acyclic, every vertex is adjacent to only one earlier vertex. Now $||T|| = n - 1$ follows by induction on n. ($\Longleftarrow$) Let G be any connected graph with n vertices and $n - 1$ edges. Let T be a spanning tree in G. Since T has $n - 1$ edges by the first implication, it follows that $T = G$. $\blacksquare$

**Corollary 1.5.3**
If T is a tree and G is any graph with $\delta(G) \ge |T| - 1$, then T is isomorphic to a subgraph of G.

Map the vertices of T to G inductively, following their enumeration from Proposition 1.4.1 applied to T. $\blacksquare$

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
