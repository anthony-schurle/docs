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
- **Normal Tree (Depth-First-Trees)**
  - Rooted tree contained in a graph G where the ends of every T-path in G are comparable in the tree-order of T.
  - If T spans G, this requires that two vertices of T must be comparable when they are adjacent in G.

### Theorems & Proofs
**Theorem 1.5.1**
The following assertions are equivalent for a graph T:
(i) T is a tree;
(ii) Any two vertices of T are linked by a unique path in T;
(iv) T is maximally acyclic, i.e. T contains no cycle but $T + xy$ does, for any two non-adjacent vertices $x, y \in T$.

**Corollary 1.5.2**
A connected graph with n vertices is a tree iff it has $n - 1$ edges.

($\implies$) Enumerate the vertices of a tree T as in Proposition 1.4.1. As T is acyclic, every vertex is adjacent to only one earlier vertex. Now $||T|| = n - 1$ follows by induction on n. ($\Longleftarrow$) Let G be any connected graph with n vertices and $n - 1$ edges. Let T be a spanning tree in G. Since T has $n - 1$ edges by the first implication, it follows that $T = G$. $\blacksquare$

**Corollary 1.5.3**
If T is a tree and G is any graph with $\delta(G) \ge |T| - 1$, then T is isomorphic to a subgraph of G.

Map the vertices of T to G inductively, following their enumeration from Proposition 1.4.1 applied to T. $\blacksquare$

**Lemma 1.5.4**
Let T be a normal tree in G.
(i) Any two vertices x, y of T that are incomparable in its tree-order are separated in G by the set $\lceil x \rceil \cap \lceil y \rceil$.
(ii) If $V(T) = V(G) =: V$ and $S \subseteq V$ is down-closed, then the components of $G - S$ are spanned by the sets $\lfloor x \rfloor$ with x minimal in $V \backslash S$.

(i) As x and y are incomparable, neither of them lies in $\lceil x \rceil \cap \lceil y \rceil$. So it suffices to show that every $x-y$ path P in G meets $\lceil x \rceil \cap \lceil y \rceil$. Let Let $t_1,...,t_n$ be a minimal sequence of vertices in $P \cap T$ such that $t_1 = x$ and $t_n = y$ and $t_i$ and $t_{i+1}$ are comparable in the tree-order of T for all i. (Such a sequence exists: the set of all vertices in $P \cap T$, in their natural order as they occur on P, has this property because T is normal and every segment $t_iPt_{i+1}$ is either an edge of T or a $T-path$.) In our minimal sequence we cannot have $t_{i-1} < t_i > t_{i+1}$ for any i, since $t_{i-1}$ and $t_{i+1}$ would then be comparable, and deleting $t_i$ would yield a smaller sequence. Thus, our sequence has the form $x = t_1 > ... > t_k < ... < t_n = y$ for some $k \in \{1, ..., n\}$ (even with $k \le 3$, by the minimality of n). As $t_k \in \lceil x \rceil \cap \lceil y \rceil \cap V(P)$, our proof is complete.
(ii) Every set $\lfloor x \rfloor$ as in (ii) is connected in T, and hence in G. It lies in $V \backslash S$, because $x \not \in S$ and S is down-closed. As every vertex in $V \backslash S$ lies above some minimal such vertex x, these sets $\lfloor x \rfloor$ have union $V \backslash S$. For distinct x and x', the connected sets $\lfloor x \rfloor$ and $\lfloor x' \rfloor$ are disjoint, and not joined by an edge of G, because $\lceil x \rceil \cap \lceil x' \rceil \subseteq S$ separates x from x' in G, by (i). So the sets $\lfloor x \rfloor$ span maximal connected subgraphs, components, in G - S, and these are all its components.

**Proposition 1.5.5**
Every connected graph has a normal spanning tree.

Let G be a connected graph. Let T be any maximal normal tree in G; we show that $V(T) = V(G)$. Suppose not, and let C be a component of $G - T$. As T is normal, $N(C)$ is a chain in T. Let x be its greatest element, and let $y \in C$ be adjacent to x. Let $T'$ be the tree obtained from T by joining y to x; the tree-order of T' then extends that of T. We shall derive a contradiction by showing that T' is also normal in G. Let P be a $T'-path$ in G. If the ends of P both lie in T, then they are comparable in the tree-order of T, because then P is also a T-path and T is normal in G by assumption. If not, then y is one end of P, so P lies in C except for its other end z, which lies in $N(C)$. Then $z \le x$, by the choice of x. For our proof that y and z are comparable it thus suffices to show that $x < y$. This however, is clear since y is a leaf of $T'$ with neighbor x. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–16


## 0.5 Bipartite Graphs
---
### Definitions
- **R-Partite**
  - $r \ge 2$ where a graph G admits a partition into r classes such that every edge has its ends in different classes.
  - Complete iff every two vertices from different partitions classes are adjacent.
- **Complete Multipartite Graphs**
  - Complete iff every two vertices from different partitions classes are adjacent.
  - Denoted $K_{n_1,...,n_r}$ unless all $n_i$ is the same, instead we denote $K_{n}^r$.
  - Stars denoted $K_{1, n}$.

### Theorems & Proofs
**Proposition 1.6.1**
A graph is bipartite iff it contains no odd cycle.

Let $G = (V, E)$ be a graph without odd cycles; we show that G is bipartite. Clearly, a graph is bipartite if all its components are bipartite or trivial, so we may assume that G is connected. Let T be a spanning tree in G, pick a root $r \in T$, and denote the associated tree-order on V by $\le_T$. For each $v \in V$, the unique path $rTv$ has odd or even length. This defines a bipartition of V; we show that G is bipartite with this partition. Let $e = xy$ be an edge of G. If $e \in T$, with $x <_T y$ say, then $rTy = rTxy$ and so x and y lie in different partition classes. If $e \not \in T$ then $C_e := xTy + e$ is a cycle, and by the case treated already the vertices along $xTy$ alternate between the two classes. Since $C_e$ is even by assumption, x and y again lie in different classes. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–18


## 0.6 Contraction And Minors
---
### Definitions
- **Subdivision**
  - TX subdivision of X replaces some edges in X with new paths between their ends.
  - Original vertices of X are the branch vertices, original degree.
  - New vertices called subdividing vertices, degree 2.
- **Topological Minor**
  - Graph Y contains a TX as a subgraph makes X a topological minor of Y.
- **Contraction Minor**
  - X is a contraction minor of G if G is an IX where its vertex set admits a partition $\{V_X : x \in V(x)\}$ into connected subsets $V_x$ such that distinct vertices $x,y \in V(X)$ are adjacent in X iff G contains a $V_x - V_y$ edge.
  - Sets $V_x$ are the branch sets of the IX.
- **Minor**
  - If Y contains IX, then X is a minor of Y and IX is a model of X in Y denoted by $X \le Y$?
  - X is a minor of Y iff there is $A \subseteq V(Y)$ where $\phi : A \to V(X)$ such that $\forall x \in X$, $\phi^{-1}(x)$ is connected in Y and $\forall xx' \in E(X)$ there is an edge in Y between the branch sets $\phi^{-1}(x)$ and $\phi^{-1}(x')$ of its ends.
  - $\phi$ is a contraction of Y onto X if $\phi : V(Y) \to V(X)$ and $xx' \in E(X)$ whenever $x \ne x'$ and Y has an edge between $\phi^{-1}(x)$ and $\phi^{-1}(x')$.
  - Since branch sets can be singletons, every subgraph of a graph is also its minor.
  - $P = \{V_x : x \in X\}$ for a partition of $V(G)$ where X is a minor. Contraction minor denoted $G / P := X$. If $U = V_x$ is the only non-singleton branch, we denote $G / U := X$ and $v_U$ for the vertex $x \in X$ to which U contracts. Rest of X thought as induced subgraph.
- **Embedding**
  - Embedding of G in H is an injective $\phi : V(G) \to V(H)$ that preserves structure.

### Theorems & Proofs
**Proposition 1.7.1**
The minor relation and the topological-minor relation are partial orderings on the class of finite graphs.

**Corollary 1.7.2**
Let X and Y be finite graphs. X is a minor of Y iff the are graphs $G_0, ..., G_n$ such that $G_0 = Y$ and $G_ n = X$ and each $G_{i+1}$ arises from $G_I$ by deleting an edge, contracting an edge, or deleting a vertex.

Induction on $|Y| + ||Y||$. $\blacksquare$

**Proposition 1.7.3**
i) Every $TX$ is also an $IX$; thus every topological minor of a graph is also its ordinary minor.
ii) IF $\Delta (X) \le 3$, then every IX contains a TX; thus, every minor with maximum degree at most 3 of a graph is also its topological minor. $\blacksquare$

### Visual Aids
![[Screenshot from 2026-02-11 10-39-17.png]]

### References
- *Book Title* — Chapter X, Pages Y–21


## 0.7 Euler Tours
---
### Definitions
- **Euler Tour**
  - Closed walk that traverses every edge of a graph exactly once.
  - Graph is said ti be Eulerian if it contains a Euler Tour.

### Theorems & Proofs
**Theorem 1.8.1**
A connected graph is Eulerian iff every vertex has even degree.

The degree condition is clearly necessary; a vertex appearing k times in an Euler tour (or k + 1 for the start/end vertex) must have degree 2k. Conversely, we show by induction on $||G||$ that every connected graph G with all degrees even has an Euler tour. THe induction starts trivially with $||G|| = 0$. Now let $||G|| \ge 1$. Since all degrees are even, we can find in G a non-trivial closed walk that contains no edge more than once. Let W be such a walk of maximal length, and write F for the set of its edges. If $F = E(G)$, then W is an Euler tour. Suppose, therefore, that $G' := G - F$ has an edge. For every vertex $v \in G$, an even number of the edges of G at v lies in F, so the degrees of $G'$ are again all even. Since G is connected, $G"$ has an edge e incident with a vertex on W. By the induction hypothesis, the component C of $G'$ containing e has an Euler tour. Concatenating this with W, we obtain a closed walk in G that contradicts the maximal length of W. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–23

Skipped 1.9 and 1.10, please finish later.
