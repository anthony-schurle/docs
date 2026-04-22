## 1. Show that
$$
\lim_{n\to\infty}\frac{t_{r-1}(n)}{\binom{n}{2}}=\frac{r-2}{r-1}.
$$

Suppose $n=(r-1)m$ for some $m\in\mathbb N$. Then $T_{r-1}(n)$ is the complete $(r-1)$-partite graph with all vertex classes of size $m$. Hence
$$
t_{r-1}((r-1)m)=\binom{r-1}{2}m^2.
$$
Therefore
$$
\frac{t_{r-1}((r-1)m)}{\binom{(r-1)m}{2}}
=\frac{\binom{r-1}{2}m^2}{\binom{(r-1)m}{2}}
=\frac{\frac{(r-1)(r-2)}{2}m^2}{\frac{(r-1)m((r-1)m-1)}{2}}
=\frac{(r-2)m}{(r-1)m-1}.
$$
As $m\to\infty$, this tends to $\frac{r-2}{r-1}$.
Now let
$$
a_n:=(r-1)\left\lfloor\frac{n}{r-1}\right\rfloor
\qquad\text{and}\qquad
b_n:=(r-1)\left\lceil\frac{n}{r-1}\right\rceil.
$$
By the hint,
$$
t_{r-1}(a_n)\leq t_{r-1}(n)\leq t_{r-1}(b_n).
$$
Also $a_n\leq n\leq b_n$, and $0\leq b_n-a_n\leq r-1$, so $a_n/n\to1$ and $b_n/n\to1$.
Hence
$$
\frac{t_{r-1}(a_n)}{\binom{n}{2}}
\leq
\frac{t_{r-1}(n)}{\binom{n}{2}}
\leq
\frac{t_{r-1}(b_n)}{\binom{n}{2}}.
$$
For the left-hand term,
$$
\frac{t_{r-1}(a_n)}{\binom{n}{2}}
=
\frac{t_{r-1}(a_n)}{\binom{a_n}{2}}\cdot\frac{\binom{a_n}{2}}{\binom{n}{2}}.
$$
Now
$$
\frac{\binom{a_n}{2}}{\binom{n}{2}}
=
\frac{a_n(a_n-1)}{n(n-1)}
=
\frac{a_n}{n}\cdot\frac{a_n-1}{n-1}\to1,
$$
since $a_n/n\to1$. Because $a_n$ is a multiple of $r-1$, we also have
$$
\frac{t_{r-1}(a_n)}{\binom{a_n}{2}}\to\frac{r-2}{r-1}.
$$
Therefore
$$
\frac{t_{r-1}(a_n)}{\binom{n}{2}}\to\frac{r-2}{r-1}.
$$
The same argument gives
$$
\frac{t_{r-1}(b_n)}{\binom{n}{2}}\to\frac{r-2}{r-1}.
$$
Thus, by the squeeze theorem,
$$
\lim_{n\to\infty}\frac{t_{r-1}(n)}{\binom{n}{2}}=\frac{r-2}{r-1}.
$$
$\blacksquare$

## 2. Show that a connected graph is countable if all its vertices have countable degrees.

Let $G$ be a connected graph in which every vertex has countable degree. Fix a vertex $v\in V(G)$, and for each $n\in\mathbb N_0$ define
$$
V_n:=\{x\in V(G):d(v,x)=n\}.
$$
We show by induction that every $V_n$ is countable.

Clearly $V_0=\{v\}$ is finite, hence countable. Now suppose $V_n$ is countable. Every vertex in $V_{n+1}$ is adjacent to some vertex in $V_n$, so
$$
V_{n+1}\subseteq\bigcup_{x\in V_n}N(x).
$$
Each neighborhood $N(x)$ is countable by assumption, and a countable union of countable sets is countable. Therefore $V_{n+1}$ is countable.
Thus every $V_n$ is countable. Since $G$ is connected, every vertex lies at finite distance from $v$, so
$$
V(G)=\bigcup_{n=0}^{\infty}V_n.
$$
This is a countable union of countable sets, hence countable. Therefore $G$ is countable. $\blacksquare$

## 3. Use the Infinity Lemma to show that a rayless connected graph of minimum degree $d$ has a finite subgraph of minimum degree $d$.

Suppose $G$ is a connected rayless graph of minimum degree $d$, and suppose for contradiction that $G$ has no finite subgraph of minimum degree $d$.

Choose any vertex $x_0\in V(G)$, and set $X_0:=\{x_0\}$. Recursively, having chosen a finite set $X_n$ such that $G[X_n]$ is connected, consider the induced subgraph $G[X_n]$. By assumption, $G[X_n]$ does not have minimum degree $d$, so there exists a vertex $u_n\in X_n$ such that
$$
d_{G[X_n]}(u_n)<d.
$$
But $\delta(G)\geq d$, so $u_n$ has at least one neighbor outside $X_n$. Choose one such neighbor $x_{n+1}\notin X_n$, and define
$$
X_{n+1}:=X_n\cup\{x_{n+1}\}.
$$
Since $x_{n+1}$ is adjacent to $u_n\in X_n$, the induced subgraph $G[X_{n+1}]$ is connected. Also $|X_{n+1}|=|X_n|+1$, so we obtain a strictly increasing sequence of finite connected induced subgraphs.

Now define a graph $T$ on the vertex set $\{x_0,x_1,x_2,\dots\}$ by joining $u_n$ to $x_{n+1}$ for each $n$. Since $u_n\in X_n=\{x_0,\dots,x_n\}$, each new vertex $x_{n+1}$ is joined by exactly one edge to an earlier vertex. Also, for each $n$, the edge $u_nx_{n+1}$ is an edge of $G$, since $x_{n+1}$ was chosen to be a neighbor of $u_n$ in $G$. Hence $T$ is a subgraph of $G$. It follows that $T$ is connected. Also $T$ contains no cycle, because at each stage a new vertex is added with exactly one edge to the existing graph. Therefore $T$ is a tree rooted at $x_0$.

We claim that every vertex of $T$ has at most $d$ children. Let $u$ be any vertex of $T$. Each time $u$ is chosen as some $u_n$, we add a new vertex $x_{n+1}\notin X_n$ adjacent to $u$, so in passing from $X_n$ to $X_{n+1}$ the induced degree of $u$ increases by at least $1$:
$$
d_{G[X_{n+1}]}(u)\ge d_{G[X_n]}(u)+1.
$$
Once this induced degree reaches $d$, the vertex $u$ can no longer be chosen again. Hence $u$ can be chosen at most $d$ times altogether, so $u$ has at most $d$ children in $T$.

Thus $T$ is an infinite rooted tree with finite branching. Let $L_n$ be the set of vertices of $T$ at distance $n$ from the root $x_0$. Since every vertex has at most $d$ children, each $L_n$ is finite. Also, an infinite finitely branching rooted tree cannot have bounded height, so $L_n\neq\emptyset$ for every $n$. Every vertex in $L_{n+1}$ has a neighbor in $L_n$, its parent. We now apply the Infinity Lemma in the form: if $V_0,V_1,\dots$ are nonempty finite sets in a graph and every vertex of $V_{n+1}$ has a neighbor in $V_n$, then there exists a ray meeting every $V_n$. Applied to the levels $L_0,L_1,\dots$ of $T$, this yields a ray in $T$.

Since $T\subseteq G$, this ray is also a ray in $G$. But $G$ is rayless, so this is a contradiction. Therefore, $G$ must contain a finite subgraph of minimum degree $d$. $\blacksquare$

## 4. Show that in a $k$-connected locally finite infinite graph, any vertex $v$ is the starting vertex of $k$ rays that are vertex-disjoint except at $v$.

Let $G$ be a $k$-connected locally finite infinite graph, and fix $v\in V(G)$. We show that $v$ is the initial vertex of $k$ rays that are pairwise vertex-disjoint except at $v$.

For each $n\geq1$, let
$$
S_n:=\{x\in V(G):d(v,x)=n\}.
$$
Because $G$ is locally finite, every ball of finite radius around $v$ is finite, so each $S_n$ is finite. Since $G$ is infinite and connected, $S_n\neq\emptyset$ for every $n$; otherwise all vertices would lie in a finite ball around $v$, contradicting infinitude.

Also, $|S_n|\geq k$ for every $n$. $S_n$ separates $v$ from every vertex at distance greater than $n$, so if $|S_n|<k$, then deleting $S_n$ would disconnect $G$ by removing fewer than $k$ vertices, contradicting $k$-connectedness.

Now fix $n$. We claim that there exist $k$ internally vertex-disjoint $v$-$S_n$ paths with distinct endpoints in $S_n$.

Form a graph $H_n$ from $G$ by adding one new vertex $z$ and joining $z$ to every vertex of $S_n$. We first show that no set of fewer than $k$ vertices in $V(H_n)\setminus\{v,z\}$ separates $v$ from $z$ in $H_n$.

Suppose to the contrary that some set $X\subseteq V(H_n)\setminus\{v,z\}$ with $|X|<k$ separates $v$ from $z$ in $H_n$. Since $|S_n|\geq k$, there exists some vertex $s\in S_n\setminus X$. Now if there were a $v$-$s$ path in $G-X$, then in $H_n-X$ we could extend it by the edge $sz$ to obtain a $v$-$z$ path, contrary to the choice of $X$. Thus $X$ separates $v$ from $s$ in $G$. But $s\neq v$, and this contradicts the $k$-connectedness of $G$, since $|X|<k$.

Therefore no set of fewer than $k$ vertices separates $v$ from $z$ in $H_n$. By Menger's Theorem, there exist $k$ internally vertex-disjoint $v$-$z$ paths in $H_n$. Deleting the final vertex $z$ from each of these paths yields $k$ internally vertex-disjoint $v$-$S_n$ paths. Their endpoints in $S_n$ are distinct: if two of them ended at the same vertex $s\in S_n$, then the corresponding $v$-$z$ paths in $H_n$ would both contain $s$ as an internal vertex, contradicting internal disjointness.

Thus there exists an ordered $k$-tuple
$$
(P_1,\dots,P_k)
$$
of pairwise internally disjoint $v$-$S_n$ paths with distinct endpoints in $S_n$, each meeting $S_n$ only in its endpoint.

Let $\mathcal P_n$ be the set of all ordered $k$-tuples
$$
(P_1,\dots,P_k)
$$
of this kind. This set is nonempty by the preceding paragraph. It is also finite, because every such path lies entirely in the ball of radius $n$ around $v$: if a path first meets $S_n$ at its endpoint, then every earlier vertex on the path has distance at most $n-1$ from $v$. Since that ball is finite, only finitely many such paths exist, and therefore $\mathcal P_n$ is finite.

Now construct a graph $H$ whose vertex set is
$$
V(H):=\bigcup_{n\geq1}\mathcal P_n.
$$
For $\mathbf Q\in\mathcal P_{n+1}$ and $\mathbf P\in\mathcal P_n$, join $\mathbf Q$ to $\mathbf P$ in $H$ if, after some permutation of the coordinates of $\mathbf Q$, truncating each path at its first vertex in $S_n$ yields exactly the corresponding path of $\mathbf P$.

We check that every vertex of $\mathcal P_{n+1}$ has a neighbor in $\mathcal P_n$. Let
$$
\mathbf Q=(Q_1,\dots,Q_k)\in\mathcal P_{n+1}.
$$
For each $i$, let $x_i$ be the first vertex of $Q_i$ that lies in $S_n$, and let $Q_i'$ be the initial segment of $Q_i$ from $v$ to $x_i$. Then each $Q_i'$ is a $v$-$S_n$ path meeting $S_n$ only in its endpoint.

Moreover, the paths $Q_1',\dots,Q_k'$ are pairwise internally disjoint, because any internal vertex common to $Q_i'$ and $Q_j'$ would also be an internal vertex common to $Q_i$ and $Q_j$. Their endpoints are distinct: if $x_i=x_j$ for some $i\neq j$, then this common vertex lies in $S_n$, is different from $v$, and is not the endpoint of either $Q_i$ or $Q_j$, since those endpoints lie in $S_{n+1}$. Hence it would be an internal vertex common to $Q_i$ and $Q_j$, contradicting internal disjointness. Therefore, after some ordering,
$$
\mathbf P:=(Q_1',\dots,Q_k')\in\mathcal P_n,
$$
and by construction $\mathbf Q$ is adjacent in $H$ to $\mathbf P$.

Thus the sets $\mathcal P_1,\mathcal P_2,\dots$ are finite nonempty levels in a graph in which every vertex of level $n+1$ has a neighbor in level $n$. By the Infinity Lemma, there exist vertices
$$
\mathbf Q^1,\mathbf Q^2,\mathbf Q^3,\dots
$$
with $\mathbf Q^n\in\mathcal P_n$ and $\mathbf Q^n\mathbf Q^{n+1}\in E(H)$ for every $n$.

Write
$$
\mathbf Q^n=(Q_1^n,\dots,Q_k^n).
$$
We now choose orderings of these tuples inductively so that the $i$th path at level $n$ is the truncation of the $i$th path at level $n+1$.

Keep the ordering of $\mathbf Q^1$ as given, and call it
$$
\mathbf P^1=(P_1^1,\dots,P_k^1).
$$
Suppose for some $n\geq1$ that we have already chosen an ordering
$$
\mathbf P^n=(P_1^n,\dots,P_k^n)
$$
of $\mathbf Q^n$. Since $\mathbf Q^{n+1}$ is adjacent to $\mathbf Q^n$ in $H$, by definition there exists a permutation of the coordinates of $\mathbf Q^{n+1}$ such that, after reordering,
$$
\mathbf P^{n+1}=(P_1^{n+1},\dots,P_k^{n+1})
$$
has the property that for each $i\in\{1,\dots,k\}$, truncating $P_i^{n+1}$ at its first vertex in $S_n$ gives exactly $P_i^n$. In particular, $P_i^n$ is an initial segment of $P_i^{n+1}$.

Proceeding inductively, we obtain tuples
$$
\mathbf P^1,\mathbf P^2,\mathbf P^3,\dots
$$
such that for every $n$ and every $i$,
$$
P_i^n
\text{ is an initial segment of }
P_i^{n+1}.
$$

For each $i$, define
$$
R_i:=\bigcup_{n=1}^{\infty}P_i^n.
$$
Since the paths are nested by initial segments, $R_i$ is a path starting at $v$. It is infinite, because $P_i^n$ ends in $S_n$, so its length is at least $n$. Hence $R_i$ is a ray.

Finally, at each stage the paths $P_1^n,\dots,P_k^n$ are pairwise internally disjoint. Therefore no vertex other than $v$ can lie on two different rays $R_i$ and $R_j$: if such a vertex lay on both, then it would already lie on both $P_i^n$ and $P_j^n$ for all sufficiently large $n$, contradicting internal disjointness at level $n$.

Therefore $R_1,\dots,R_k$ are $k$ rays starting at $v$ and pairwise vertex-disjoint except at $v$. $\blacksquare$

## 5. Show that the infinite grid graph $\mathbb Z\times\mathbb Z$ has exactly one end.

Let $G=\mathbb Z\times\mathbb Z$. We show that $G$ has exactly one end by proving that for every finite set $S\subseteq V(G)$, the graph $G-S$ has exactly one infinite component.

Let $S\subseteq \mathbb Z^2$ be finite. Choose $N\in\mathbb N$ such that
$$
S\subseteq [-N,N]\times[-N,N].
$$
Set
$$
Q_N := [-N,N]\times[-N,N], \quad C := G - Q_N.
$$

We claim that $C$ is connected. Let $(a,b)\in V(C)$. Then either $|a|>N$ or $|b|>N$. If $|a|>N$, we can move vertically to $(a,\pm(N+1))$ while staying outside $Q_N$, and then horizontally to the boundary of the square $[-(N+1),N+1]\times[-(N+1),N+1]$. Similarly, if $|b|>N$, we first move horizontally and then vertically to reach the same boundary. Hence every vertex of $C$ can be joined within $C$ to this boundary, which is connected. Therefore $C$ is connected. Since $Q_N$ is finite, $C$ is infinite.

Now $C\subseteq G-S$, so $G-S$ has at least one infinite component. If a component of $G-S$ does not meet $C$, then it is contained in the finite set $Q_N\setminus S$, and hence is finite. Thus every infinite component of $G-S$ meets $C$. Since $C$ is connected, all its vertices lie in a single component of $G-S$, so this is the unique infinite component.

Therefore $G-S$ has exactly one infinite component for every finite set $S\subseteq V(G)$, and hence $\mathbb Z\times\mathbb Z$ has one end. $\blacksquare$