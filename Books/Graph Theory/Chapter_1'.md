# Chapter 1: The Basics

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 1.1 Graphs

---

### Definitions

- **Graph**: Pair of sets $G = (V, E)$ such that $E \subseteq [V]^2$. The vertex set and edge set of $G$ referred to as $V(G)$ and $E(G)$ respectively. Empty graph $(\emptyset, \emptyset)$ denoted $\emptyset$.
- **Vertices**: Elements of the set $V$ of a graph. A graph is said to be on $V$.
- **Edges**: Elements of the set $E$ of a graph. Edge count denoted $||G||$. Edge $\{x, y\}$ usually written $xy$ or $yx$. If $x \in X$ and $y \in Y$, then $xy$ is an $X-Y$ edge. Set of all such $X-Y$ edges denoted $E(X, Y)$. Set of all edges at vertex $v$ denoted $E(v)$.
- **Order**: Number of vertices of a graph, denoted $|G|$.
- **Trivial:** Graph of order 0 or 1.
- **Incident**: Vertex $v$ is incident with edge $e$ if $v \in e$. $e$ is said to be an edge at $v$.
- **Endvertices (Ends)**: The two vertices incident with an edge. The edge is said to join its ends.
- **Neighbors (Adjacent)**: Vertices $x$ and $y$ are neighbors if $\{x, y\}$ is an edge.
- **Adjacent**: Edges $e \ne f$ are adjacent if they have an endvertex in common.
- **Complete**: Graph G is complete if all vertices of G re pairwise adjacent. Denoted $K^n$ where n is the vertex count of G.
- **Triangle**: $K^3$.
- **Independent (Stable)**: Set of vertices or edges that pairwise is non-adjacent.
- **Homomorphism**: Let $G = (V, E)$ and $G' = (V', E')$. $\phi : V \to V'$ is a homomorphism if $\{x, y\} \in E \implies \{\phi(x), \phi(y)\} \in E'$. 
- **Isomorphism**: Let $G = (V, E)$ and $G' = (V', E')$. $\phi : V \to V'$ is a isomorphism if $\{x, y\} \in E \iff \{\phi(x), \phi(y)\} \in E'$ and $\phi$ is bijective. We denote $G \cong G'$.
- **Automorphism**: Isomorphism from a graph $G$ to itself.
- **Abstract Graph**: Isomorphic type of a graph.
- **Graph Property**: Class of graphs closed under an isomorphism.
- **Graph Invariant**: Map taking graphs that assigns equal values to isomorphisms.
- **Disjoint**: Graphs $G$ and $G'$ are disjoint if $G \cap G' = \emptyset$. $G$ * $G'$ denotes the graph obtained from $G \cup G'$ by joining all the vertices of $G$ to all the vertices of $G'$.
- **Subgraph**: Let $G = (V, E)$ and $G' = (V', E')$. If $V \subseteq V'$ and $E \subseteq E'$, then $G$ is a subgraph of $G'$. Denoted $G \subseteq G'$.
- **Supergraph**: Let $G = (V, E)$ and $G' = (V', E')$. If $V \subseteq V'$ and $E \subseteq E'$, then $G'$ is a supergraph of $G$. Denoted $G \subseteq G'$.
- **Proper Subgraph**: $G$ is a proper subgraph of $G'$ if $G \ne G'$ and $G$ is a subgraph of $G'$.
- **Induced Subgraph**: If $G' \subseteq G$ and $G'$ contains all edges $xy \in E(G)$ with $x, y \in V(G')$, then $G'$ is an induced subgraph of $G$. It is said that $V'$ spans $G'$ in $G$ and is denoted $G[V'] := G'$. $G - U$, for vertex set $U$, denotes $G[V(G) \backslash U]$.
- **Spanning Subgraph**: $G'$ is a spanning subgraph of $G$ if it is a subgraph of $G$ and and $V(G')$ spans all of $G$.
- **Edge Maximal**: Graph $G$ is edge-maximal if $G$ has a graph property but no graph $(V, F)$ with $E(G) \subset F$ does.
- **Complement**: Denoted $\overline{G}$ for graph $G$, is the graph on $V(G)$ with edge set $[V(G)]^2 \backslash E(G)$.
- **Line Graph**: Denoted $L(G)$, is the graph on $E(G)$ where $x, y \in E(G)$ are adjacent as vertices iff they are adjacent as edges in $G$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -4


## 1.2 The Degree Of A Vertex

---

### Key Concepts

- **Neighbors Set**: For $U \subseteq V(G)$, the neighbors in $V(G) \backslash U$ of vertices in $U$ are denoted $N_G(U)$.

### Definitions

- **Degree**: Denoted $d_G(v) = |E(v)|$.
- **Isolated**: Vertex with degree 0.
- **Minimum Degree**: $\delta (G) := \min\{d_G(v)| v \in V(G)\}$ is the minimum degree of graph $G$.
- **Maximum Degree**: $\Delta := \max\{d_G(v) | v \in V(G)\}$ is the maximum degree of graph G.
- **k-Regular**: All vertices of graph G have the same degree k.
- **Cubic**: 3-regular graph.
- **Average Degree**: $d(G) := \frac{1}{|V(G)|} \times \sum_{v \in V(G)}d_G(v)$ is the average degree of graph $G$.
- **Edge-Vertex Ratio**: $\epsilon(G) := \frac{|E(G)|}{|V(G)|}$ is the edge-vertex ratio for graph $G$. Notice $\epsilon(G) = 0.5d(G)$.

### Results & Proofs

**Proposition: Proposition 1.2.1**
The number of vertices of odd degree in a graph is always even.
> **Proof**: As $|E| = 0.5 \sum_{v \in V(G)}d_G(v)$ is an integer, $\sum_{v \in V(G)}d_G(v)$ is even. $\proofend$

**Proposition: Proposition 1.2.2**
Every graph $G$ with at least one edge has a subgraph $H$ with $\delta(H) > \epsilon(H) \ge \epsilon(G)$.
> Define the sequence $G = G_0 \supseteq G_1 \supseteq ...$ of induced subgraphs of $G$ as follows. If $G_i$ has a vertex $v_i$ of degree $d_G(v_i) \le \epsilon(G_i)$, we let $G_{i+1} := G_i - v_i$; if not, we terminate our sequence and let $H := G_i$. By the choices of $v_i$, we have $\epsilon(G_{i+1}) \ge \epsilon(G_i)$ for all $i$, and hence $\epsilon(H) \ge \epsilon(G)$. Since $\epsilon(K^1) = 0 < \epsilon(G)$, none of the graphs in the sequence are trivial , so $H \ne \emptyset$. The construction of H implies that $\delta(H) > \epsilon(H)$. $\proofend$

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -6


## 1.3 Paths And Cycles

---

### Definitions

- **Path**: Non-empty graph $P = (V, E)$ of the form $V = \{x_0, x_1, ..., x_n\}$ and $E = \{x_0x_1, x_1x_2, ..., x_{n-1}x_n\}$ where each $x_i$ is distinct. $x_0$ and $x_n$ are called the ends of $P$ and $x_i \ne x_0,x_n$ are called its inner vertices. $P$ is said to link $x_0$ and $x_n$. Given vertex sets $A$ and $B$, $P$ is an $A-B$ path if $V(P) \cap A = \{x_0\}$ and $V(P) \cap B = \{x_n\}$.
- **Path Length**: $|E(P)|$ for a path $P$, denoted $P^k$.
- **Subpaths**: Let $0 \le i \le j \le n$. We denote $Px_i := x_0...x_i$, $x_iP := x_i...x_k$, $x_iPx_j := x_i...x_j$, $\mathring{P} := x_1...x_{n-1}$, $P\mathring{x_i} := x_0...x_{i-1}$, $\mathring{x_i}P := x_{i+1}...x_n$, $\mathring{x_i}P\mathring{x_j} := x_{i+1}...x_{j-1}$.
- **Independent**: $P$ and $P'$ paths are independent if they do not contain inner vertices of each other.
- **A-B Path**: Given vertex sets $A$ and $B$, $P$ is an $A-B$ path if $V(P) \cap A = \{x_0\}$ and $V(P) \cap B = \{x_n\}$.
- **A-Path**: If $A$ is a vertex set, non-trivial path P with its ends but no inner vertex in A is an $A$-path. If $A$ is a graph, $P$ is a $A$-path if it is a $V(A)$-path and when it is length 1, its edge does not lie in $E(A)$.
- **Cycle**: Denoted $C := P + x_{k-1}x_0$ where $P = x_0...x_{k-1}$ is a path and $k \ge 3$.
- **Cycle Length**: $|E(C)|$ for a cycle $C$, denoted $C^k$.
- **k-Cycle**: $C^k$.
- **Girth**: Minimum length of a cycle contained in a graph $G$, denoted $g(G)$. $\infty$ when no cycle is present.
- **Circumference**: The maximum length of a cycle contained in a graph $G$. $0$ when no cycle is present.
- **Chord**: An edge that joins two vertices of a cycle but is not itself an edge of the cycle.
- **Induced Cycle**: A cycle forming an induced subgraph.
- **Distance**: Denoted $d_G(x, y)$, is the length of a shortest $x-y$ path in $G$. If no path exists, we set $d_G(x, y) = \infty$.
- **Diameter**: Greatest distance between any two vertices in a graph, denoted $diam(G)$.
- **Central**: Vertex in a graph $G$ when its greatest distance from any other vertex is as small as possible.
- **Radius**: Distance of the central vertex, denoted $rad(G) = \min_{x \in V(G)}\max_{y \in V(G)}d_G(x, y)$. Useful property that $rad(G) \le diam(G) \le 2rad(G)$.
- **Walk**: Non-empty alternating sequence $v_0e_0v_1e_1...e_{k-1}v_k$ of vertices and edges in $G$ such that $e_i = \{v_i, v_{i+1}\}$ for all $i < k$. It's length is $k$.
- **Closed Walk**: Start vertex is the same as the end vertex of the walk.

### Results & Proofs

**Proposition: Proposition 1.3.1**
Every graph $G$ contains at least a path of length $\delta(G)$ and a cycle of length at least $\delta(G) + 1$ (provided that $\delta(G) \ge 2$).
> **Proof**: Let $x_0...x_k$ be the longest path in $G$. Then all the neighbors of $x_k$ lie on this path. Hence $k \ge d_G(x_k) \ge \delta(G)$. If $i$ is minimal with $x_ix_k \in E(G)$, then $x_i...x_kx_i$ is a cycle of length at least $\delta(G) + 1$. $\proofend$

**Proposition: Proposition 1.3.2**
Every graph $G$ containing a cycle satisfies $g(G) \le 2diam(G) + 1$.
> Let $C$ be a shortest cycle in $G$. If $g(G) \ge 2diam(G) + 2$, then $C$ has two vertices whose distance in C is at least $diam(G) + 1$. In $G$, these vertices have lesser distance; any shortest path $P$ between them is therefore not a subgraph of $C$. Thus, $P$ contains a $C$-path $xPy$. Together with the shorter of the two $x-y$ paths in $C$, this path $xPy$ forms a shorter cycle than $C$, a contradiction. $\proofend$

**Proposition: Proposition 1.3.3**
A graph $G$ of radius at most $k$ and maximum degree at most $d \ge 3$ has fewer than $\frac{d}{d-2}(d-1)^k$ vertices.
> Let $z$ be a central vertex in $G$, and let $D_i$ denote the set of vertices of $G$ at distance $i$ from $z$. Then $V(G) = \bigcup_{i = 0}^k D_i$. Clearly $|D_0| = 1$ and $|D_1| \le d$. For $i \ge 1$, we have $|D_{i+1}| \le (d-1)|D_i|$, because every vertex in $D_{i+1}$ is a neighbor of a vertex in $D_i$, and each vertex in $D_i$ has at most $d-1$ neighbors in $D_{i+1}$. Thus $|D_{i+1}| \le d(d-1)^i$ for all $i < k$ by induction, giving $|G| \le 1 + \sum_{i = 0}^{k-1}(d-1)^i = 1 + \frac{d}{d-2}((d-1)^k - 1) < \frac{d}{d-2}(d-1)^k$.

**Theorem: Theorem 1.3.4**
For $d \in \mathbb{R}$ and $g \in \mathbb{N}$, define $n_(d, g) := \begin{cases} 1 + d\sum_{i=0}^{r-1}(d-1)^i & 2r + 1 := g \text{ is odd} \\ 2\sum_{i=0}^{r-1}(d-1)^i & 2r := g \text{ is even}\end{cases}$. Let $G$ be a graph. If $d(G) \ge d \ge 2$ and $g(G) \ge g$ then $|G| \ge n_0(d, g)$.
> TO DO.

**Corollary: Corollary 1.3.5**
If $\delta(G) \ge 3$ then $g(G) < 2 \log|G|$.
> If $g := g(G)$ is even then $n_0(3, g) = 2\frac{2^{0.5g}-1}{2-1} > 2^{0.5g}$. Similar result when $g$ is odd. As $|G| \ge n_0(3, g)$ the result follows. $\proofend$

**Proposition: Walks Contain Paths**
Every walk between two vertices contains a path.
> If the vertices of the walk are distinct, we are done. So suppose not. Then our walk is of the form $v_0e_0v_1e_1 ... v_k$ where each $v_i$ may not be distinct. Define the sequence (just remove everything before the maximal non-distinct vertex) TO DO

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -10


## 1.4 Connectivity

---

### Definitions

- **Connected**: Graph $G$ that is non-empty and any two of its vertices are linked by a path in $G$. If $U \subseteq V(G)$ and $G[U]$ is connected, we also call $U$ itself connected in $G$.
- **Component**: Maximal connected subgraph of $G$.
- **Separates**: If $A, B \subseteq V(G)$ and $X \subseteq V(G) \cup E(G)$ are such that every $A-B$ path in $G$ contains a vertex or an edge from $X$, $X$ separates $A$ from $B$. $X$ separates two vertices if it separates their sets but does not contain them. $X$ separates a graph $G$ if it separates some two vertices in $G$.
- **Cutvertex**: Vertex that separates two other vertices of the same component.
- **Bridge**: Edge separating its ends.
- **Separation**: Unordered pair $\{A, B\}$ such that $A \cup B = V$ and $A \cap B$ separates $A$ from $B$. If $A \backslash B \ne \emptyset$ and $B \backslash A \ne \emptyset$, the separation is said to be proper.
- **Order**: $|A \cap B|$ for separation $\{A, B\}$.
- **Sides**: $A$ and $B$ for separation $\{A, B\}$.
- **K-connected**: For $k \in \mathbb{N}$, if $|G| > k$ and $G - X$ is connected for every set $X \subseteq V(G)$ with $|X| < k$. Every non-empty graph is 0-connected.
- **Connectivity**: Greatest integer $k$ such that a graph $G$ is $k$-connected, denoted $\kappa(G)$.
- **L-Edge-Connected**: If $|G| > 1$ and $G - F$ is connected for every set $F \subseteq E(G)$ of fewer than $l$ edges.
- **Edge-Connectivity**: Greatets integer $l$ such that $G$ is $l$-edge-connected, denoted $\lambda(G)$.

### Results & Proofs

**Proposition: Proposition 1.4.1**
The vertices of a connected graph $G$ can always be enumerated, say as $v_1, ..., v_n$, so that $G_i := G[v_1, ..., v_i]$ is connected for every $i$.
> **Proof**: Pick any vertex $v_1$, and assume inductively that $v_1, ..., v_i$ have been chosen for some $i \le |G|$. Now pick a vertex $v \in G - G_i$. As $G$ is connected, it contains a $v-v_1$ path $P$. Choose as $v_{i+1}$ the last vertex of $P$ in $G - G_i$; then $v_{i+1}$ has a neighbor in $G_i$. The connectedness of every $G_i$ follows by induction on $i$. $\proofend$

**Proposition: Proposition 1.4.2**
If $G$ is non-trivial then $\kappa(G) \le \lambda(G) \le \delta(G)$.
> **Proof:** The second inequality follows from the fact that all the edges incident with a fixed vertex separate $G$. Let $F$ be a set of$\lambda(G)$ edges such that $G-F$ is disconnected. Such a set exists by $\lambda$ and $F$ is a minimal separating set of edges in $G$. We show that $\kappa(A) \le |F|$. Case 1: $G$ has a vertex not incident with $F$. Let $C$ be the component of $G-F$ containing $v$. Then the vertices of $C$ incident with $F$ separate $v$ from $G-C$, giving $\kappa(G) \le |F|$ as desired. Case 2: Every vertex of $G$ is incident with $F$. Pick any $v$ and let $C$ be the component of $G-F$ containing it. Then the neighbors $w$ with $vw \not \in F$ lie in $C$ are incident with distinct edges of $F$. Since $N_G(v)$ separates $v$, $\kappa(G) \le |F|$. If no other vertices exist, we have $\kappa(G) = \lambda(G) = |G| - 1$ since $v$ was arbitrary - giving the complete graph. $\proofend$

**Theorem: Theorem 1.4.3**
TO DO

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -13


## 1.5 Trees And Forests

---

### Definitions

- **Acyclic**: Graph not containing cycles.
- **Forest**: Acyclic graph.
- **Tree**: Connected forest. Vertices of degree $1$ are called leaves, else called an inner vertex.
- **Chords**: For a spanning tree $T$ of a graph $G$, its cords are $E(G) \backslash E(T)$.
- **Rooted Tree**: A tree $T$ with a fixed vertex $r$, called the root.
- **Tree-Order**: Let $T$ be a rooted tree with root $r$. The tree order is a partial ordering on $V(T)$ defined by $x \le y$ for $x \in rTy$.
- **Down-Closure**: For a defined tree order, the down closure of $y$ is $\lceil y \rceil := \{x | x \le y\}$.
- **Up-Closure**: For a defined tree order, the up closure of $y$ is $\lfloor y \rfloor := \{x| x \ge y\}$.
- **Down-Set**: A set $X \subseteq V(T)$ satisfying $X = \lceil X \rceil := \bigcup_{x \in X} \lceil x \rceil$.
- **Up-Set**: A set $X \subseteq V(T)$ satisfying $X = \lfloor X \rfloor := \bigcup_{x \in X} \lfloor x \rfloor$.
- **Chain**: Set of pairwise comparable elements.
- **Height**: Vertices with distance $k$ from the root $r$ have height $k$.
- **Level**: Vertices at height $k$ are at level $k$ of the tree.
- **Normal**: Rooted tree $T$ contained in a graph $G$ is normal if the ends of every $T$-path in $G$ are comparable in the tree-order of $T$.
- **Depth-First Search Tree**: Normal spanning tree.

### Results & Proofs

**Theorem: Theorem 1.5.1**
The following assertions are equivalent for a graph $T$:
(i) $T$ is a tree;
(ii) Any two vertices of $T$ are linked by a unique path in $T$; ($xTy$ denotes the unique path between $x$ and $y$)
(iii) $T$ is minimally connected;
(iv) T is maximally acyclic;
> **Proof**: Straightforward.

**Corollary: Corollary 1.5.2**
A connected graph with $n$ vertices is a tree iff it has $n-1$ edges.
> Enumerate the vertices of a tree $T$ as in Proposition 1.4.1. As $T$ is acyclic, every vertex is adjacent to only one earlier vertex. Now $||T|| = n-1$ follows by induction on $n$. Now let $G$ be any connected graph with $n$ vertices and $n-1$ edges. Let $T$ be a spanning tree in $G$. Since $T$ has $n-1$ edges by the first implication, it follows that $T = G$. $\proofend$

**Corollary: Corollary 1.5.3**
If $T$ is a tree and $G$ is any graph with $\delta(G) \ge |T| - 1$, then $T$ is isomorphic to a subgraph of $G$.
> Map the vertices of $T$ to $G$ inductively, following their enumeration from Proposition 1.4.1 applied to $T$. $\proofend$

**Lemma: Lemma 1.5.4**
Let $T$ be a normal tree in $G$.
(i) Any two vertices $x, y \in T$ that are incomparable in its tree-order are separated in $G$ by the set $\lceil x \rceil \cap \lceil y \rceil$.
(ii) If $V(T) = V(G) =: V$ and $S \subseteq V$ is down-closed, then the components of $G-S$ are spanned by the sets $\lfloor x \rfloor$ with $x$ minimal in $V \backslash S$.
> **Proof.** i) By incomparability $x, y \not \in \lceil x \rceil \cap \lceil y \rceil$. So it suffices to show every $x-y$ path $P$ in $G$ meets $\lceil x \rceil \cap \lceil y \rceil$. Let $t_1, ..., t_n$ be a minimal sequence of vertices in $P \cap T$ such that $t_1 = x$ and $t_n = y$ and $t_i$ is comparable with $t_{i+1}$ in the tree-order of $T$ for all $i$. By minimality, we cannot have $t_{i-1} < t_i > t_{i+1}$ for any $i$. Thus, our sequence has the form $t_1 > ... > t_k < ... < t_n$ for some $k \in \{1, ..., n\}$.  As $t_k \in \lceil x \rceil \cap \lceil y \rceil \cap V(P)$, our proof is complete. In fact, $k = 2$ and $n = 3$ by minimality and incomparability.
> ii) Every set $\lfloor x \rfloor$ is connected in $T$ and hence in $G$. It lies in $V \backslash S$, because $x \not \in S$ and $S$ is down closed. As every vertex in $V \backslash S$ lies above some minimal such vertex $x$, these sets $\lfloor x \rfloor$ have union $V \backslash S$. For distinct $x$ and $x'$, the connected sets $\lfloor x \rfloor$ and $\lfloor x' \rfloor$ are disjoint, and not joined by an edge of $G$, because $\lceil x \rceil \cap \lceil x' \rceil \subseteq S$ separates $x$ from $x'$ in $G$ by i). $\proofend$

**Proposition: Proposition 1.5.5**
Every connected graph has a normal spanning tree.
> **Proof.** Let $G$ be a connected graph. Let $T$ be any maximal normal tree in $G$; we show that $V(T) = V(G)$. Suppose not, and let $C$ be a component of $G-T$. As $T$ is normal, $N(C)$ is a chain in $T$. Let $x$ be its greatest element, and let $y \in C$ be adjacent to $x$. Let $T'$ be the tree obtained from $T$ by joining $y$ to $x$. We shall derive a contradiction. Let $P$ be a $T'$-path. If the ends of $P$ both lie in $T$, then they are comparable since $T$ is normal by assumption. If not, then $y$ is one end, so $P$ lies in $C$ except for its other end $z$ , which lies in $N(C)$. Then $z \le x$ by choice of x. $x < y$ since $y$ is a leaf with neighbor $x$, meaning $y$ and $z$ are comparable. $\proofend$

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -16


## 1.6 Bipartite Graphs

---

### Definitions

- **r-Partite**: For $r \ge 2$ and graph $G = (V, E)$, $V$ admits a partition into $r$ classes such that every edge has its ends in different classes.
- **Bipartite**: 2-partite.
- **Complete**: $r$-partite graph in which every two vertices from different partition classes are adjacent.
- **Complete Multipartite**: Complete r-partite graph $\overline{K^{n_1}} * ... * \overline{K^{n_r}}$ denoted by $K_{n_1, ..., n_r}$. If $n_1 = ... = n_r$, we abbreviate to $K_{n_1}^r$.
- **Stars**: Graphs of the form $K_{1, n}$.
- **Star's Centre**: Vertex in the singleton partition class of a star.

### Results & Proofs

**Proposition: Proposition 1.6.1**
A graph is bipartite iff it contains no odd cycle.
> **Proof**: Let $G = (V, E)$ be a graph without odd cycles. Clearly a graph is bipartite if all its components are bipartite or trivial, so we may assume $G$ is connected. Let $T$ be a spanning tree in $G$, pick a root $r \in T$, and denote the associated tree order by $\le_T$. For each $v \in V$, the unique path $rTv$ has odd or even length. This defines a bipartition of $V$. Let $e = xy$ be an edge of $G$. If $e \in T$, with $x <_T y$ say, then $rTy = rTxy$ and so x and y lie in different partition classes. If $e \not \in T$, then $C_e := xTy + e$ is a cycle. Since $C_e$ must be even, $x$ and $y$ lie in different classes. $\proofend$

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -18


## 1.7 Contraction And Minors

---

### Definitions

- **Subdivision (TX)**: $G$ is a subdivision of the graph $X$, denoted $TX$, if if it is obtained by replacing edges of $X$ with new paths with no inner vertex in $V(X)$ or another new path.
- **Branch Vertices**: Original vertices of $X$ in a $TX$.
- **Subdividing Vertices**: New vertices of a $TX$ from $X$.
- **Topological Minor**: $X$ is a topological minor of $Y$ if $Y$ contains a $TX$.
- **IX**: A graph $G$ is an $IX$ if its vertex set admits a partition $P = \{V_x | x \in V(X)\}$ into connected subsets $V_x$ such that $x, y \in X$ are adjacent in $X$ iff $G$ contains a $V_x - V_y$ edge. We write $G / P := X$ unless only one $U \in P$ is not a singleton, then we write $G / U$ and $v_u$ for the corresponding contracted vector.
- **Branch Sets**: The sets $V_x$ of an $IX$.
- **Contraction Minor**: If $G$ is an $IX$, $X$ arises from $G$ by contracting the subgraphs $V_x$ and is called a contraction minor.
- **Minor**: If graph $Y$ contains an $IX$, then $X$ is a minor of $Y$, denoted $X \preceq Y$. Formally, $X \preceq Y$ iff $\exists \sigma : C \to V(X)$ where $C \subseteq V(Y)$ such that for every $x \in X$ we have $\sigma^{-1}(x)$ connected in $Y$ and for every edge $xx' \in X$ there is an edge in $Y$ between the branch sets $\sigma^{-1}(x)$ and $\sigma^{-1}(x')$.
- **Model**: If $Y$ contains and $IX$, the $IX$ is said to be a model of $X$ in $Y$.
- **Contraction**: A map $\sigma : V(Y) \to V(X)$ such that $Y$ is an $IX$.
- **Edge Contraction**: $G / e$ for some edge $e$.
- **Embedding**: Injective map $\phi : V(G) \to V(H)$ is an embedding of $G$ in $H$ if it preserves some desired structure. Can be defined on edges as well to define things like topological minor. Minors would map vertices to vertex sets.

### Results & Proofs

**Proposition: Proposition 1.7.1**
The minor and topological minor relations are partial orderings on the class of finite graphs.
> **Proof**: TO DO

**Corollary: Corollary 1.7.2**
Let $X$ and $Y$ be finite graphs. $X$ is a minor of $Y$ iff there are graphs $G_0, ..., G_n$ such that $G_0 = Y$ and $G_n = X$ and each $G_{i+1}$ arises from $G_i$ by deleting an edge, contracting an edge, or deleting a vertex.
> **Proof.** TO DO

**Proposition: Proposition 1.7.3**
(i) Every $TX$ is also an $IX$
(ii) If $\Delta(X) \le 3$, then every $IX$ contains a $TX$.
> **Proof.** TO DO

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -21


## 1.8 Euler Tours

---

### Definitions

- **Euler Tour**: Closed walk that traverses every edge once.
- **Eulerian**: Graph that admits a Euler tour.

### Results & Proofs

**Theorem: Theorem 1.8.1**
A connected graph is Eulerian iff every vertex has even degree.
> **Proof.** TO DO

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -23


## 1.9 Some Linear Algebra

---

### Key Concepts

- **Example Concept**: A concise explanation of a foundational concept.

### Definitions

- **Cut**: Set $F$ of edges is a cut if there exists partition $\{V_1, V_2\}$ of the vertices such that $F = E(V_1, V_2)$.
- **Bond**: Minimal non-empty cut.
- **Atomic**: Cuts or bonds of the form $E(v)$ where $v$ is a single vertex.

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


## 1.10 Other Notions Of Graphs

---

### Key Concepts

- **Multigraph Conventions**: Loops contribute 2 degree, ends of loops and parallel edges considered as separators of those edges, never 2-connected if contains a loop, normal graph if 3-connected, edge contractions do not delete edges (minor contractions generally besides loops)

### Definitions

- **Hypergraph**: Pair $(V, E)$ of disjoint sets, where the elements of $E$ are non-empty subsets of $V$.
- **Digraph**: Pair $(V, E)$ of disjoint sets with two maps $init: E \to V$ and $ter: E \to V$ assigning to every edge $e$ an initial vertex $init(e)$ and a terminal vertex $ter(e)$.
- **Multiple Edges**: Several edges between two vertices in a digraph.
- **Parallel**: Multiple edges with same direction.
- **Loop**: $ter(e) = init(e)$ for some edge $e$ in a digraph.
- **Orientation**: Digraph $D$ is an orientation of graph $G$ if $V(D) = V(G)$, $E(D) = E(G)$, and $\{init(e), ter(e)\} = \{x, y\}$ for every edge $e = xy$.
- **Multigraph**: Pair $(V, E)$ of disjoint sets together with map $E \to V \cup [V]^2$ assigning to every edge either one or two vertices.
- **Suppressing**: A vertex $v$ of degree 2 is suppressed in a multigraph when removed and an edge is added between its neighbors.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages -29
