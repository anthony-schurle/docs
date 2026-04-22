## 1) Show that each of the following operations performed on the Rado graph $R$ leaves a graph isomorphic to $R$:

Note: The book states that the Rado graph is unique in satisfying property $*$. Therefore, it suffices to show a graph satisfies $*$ to show isomorphism.

### a) taking the complement of $R$

Let $U, V \subseteq V(\overline{R})$ be finite and disjoint. We want to find a vertex $x$ in $\overline{R}$ adjacent to every vertex in $U$ and adjacent to no vertex in $V$. But adjacency in $\overline{R}$ is exactly non-adjacency in $R$, so this is equivalent to finding a vertex $x$ in $R$ adjacent to every vertex in $V$ and adjacent to no vertex in $U$. Since $R$ has the $*$ property as defined in the book, such a vertex exists. Therefore, $\overline{R}$ also has the $*$ property. Since $\overline{R}$ is countable and satisfies the $*$ property, it follows that $\overline{R} \cong R$. $\proofend$

### b) deleting finitely many vertices of $R$

Let $F \subseteq V(R)$ be finite, and consider the graph $R - F$. Let $U, V \subseteq V(R)\setminus F$ be finite and disjoint. We want a vertex $x \in V(R)\setminus (F \cup U \cup V)$ adjacent to every vertex in $U$ and adjacent to no vertex in $V$. First, since $R$ has the $*$ property, there exists some vertex $x_1$ adjacent to every vertex in $U$ and adjacent to no vertex in $V$. Next, apply the $*$ property again to the sets $U \cup \{x_1\}$ and $V$. Then there exists a vertex $x_2$ adjacent to every vertex in $U \cup \{x_1\}$ and adjacent to no vertex in $V$. In particular, $x_2 \neq x_1$, and $x_2$ is also adjacent to every vertex in $U$ and adjacent to no vertex in $V$. Continuing in this way, we obtain infinitely many distinct vertices $x_1, x_2, x_3, \dots$ each adjacent to every vertex in $U$ and adjacent to no vertex in $V$. Since $F$ is finite, at least one of these vertices is not in $F$. Hence there exists a vertex in $R-F$ adjacent to every vertex in $U$ and adjacent to no vertex in $V$. Therefore, $R-F$ satisfies the $*$ property. Since $R-F$ is countable and satisfies the $*$ property, it follows that $R-F \cong R$. $\proofend$

## 2) How many different 2-edge-colorings are there of $K_3$? $K_4$? Isomorphic graphs considered equal (same coloring).

$K_3$ has precisely 4 unique colorings while $K_4$ has 11 unique colorings. All work shown in the following image:

![[IMG_1586.jpg]]

$\proofend$

## 3) Prove that $R(K_{1, 3}, K_{1, 3}) = 6$.

First, we show $R(K_{1, 3}, K_{1, 3}) \ge 6$. Define
$H := (\{1, 2, 3, 4, 5\}, \{\{1, 2\}, \{1, 5\}, \{2, 3\}, \{3, 4\}, \{4, 5\}\})$.
Then $H$ is a 5-cycle, so every vertex in $H$ has degree 2. Therefore, $K_{1, 3} \not\subseteq H$, since $K_{1, 3}$ has a vertex of degree 3 but $H$ does not. Now consider $\overline{H}$. Since the complement of a 5-cycle is again a 5-cycle, every vertex in $\overline{H}$ also has degree 2. Thus $K_{1, 3} \not\subseteq \overline{H}$ as well. It follows that there exists a graph on 5 vertices such that neither it nor its complement contains $K_{1, 3}$. Therefore, $R(K_{1, 3}, K_{1, 3}) > 5$, so $R(K_{1, 3}, K_{1, 3}) \ge 6$. Now we show that $R(K_{1, 3}, K_{1, 3}) \le 6$. Let $G$ be any graph with $|V(G)| = 6$. Pick any vertex $v \in V(G)$, and label the remaining vertices $v_1, v_2, \dots, v_5$. Consider the two possibilities for each of these five vertices: either it is adjacent to $v$, or it is not adjacent to $v$. By the pigeonhole principle, at least three of $v_1, \dots, v_5$ must fall into one of these two classes. Case 1: $v$ has at least 3 neighbors in $G$. Then $v$ together with any three of those neighbors forms a copy of $K_{1, 3}$, so $K_{1, 3} \subseteq G$. Case 2: $v$ has at least 3 non-neighbors in $G$. Then in $\overline{G}$, the vertex $v$ is adjacent to at least 3 vertices, so again $v$ together with any three of those vertices forms a copy of $K_{1, 3}$. Thus $K_{1, 3} \subseteq \overline{G}$. Therefore, for every graph $G$ with 6 vertices, either $K_{1, 3} \subseteq G$ or $K_{1, 3} \subseteq \overline{G}$. Hence $R(K_{1, 3}, K_{1, 3}) \le 6$. Since we have shown both $R(K_{1, 3}, K_{1, 3}) \ge 6$ and $R(K_{1, 3}, K_{1, 3}) \le 6$, we conclude that $R(K_{1, 3}, K_{1, 3}) = 6$. $\proofend$

## 4) Prove that $R(mK_2, mK_2) = 3m - 1$.
Note: I refer to $mK_2$ as a matching throughout.

First, we show that $R(mK_2, mK_2) \ge 3m - 1$. Consider the complete graph on $3m-2$ vertices, and partition its vertex set into two parts $A$ and $B$ with $|A| = 2m-1$ and $|B| = m-1$. Now color every edge with both endpoints in $A$ red, and color every other edge blue. Any red matching must lie entirely inside $A$, since the only red edges are those with both endpoints in $A$. But $A$ has only $2m-1$ vertices, so the largest possible matching in $A$ has size $\left\lfloor \frac{2m-1}{2} \right\rfloor = m-1$. Thus there is no red copy of $mK_2$. On the other hand, every blue edge is incident to at least one vertex of $B$, since the only non-blue edges are those inside $A$. Therefore, any blue matching uses distinct vertices of $B$, so its size is at most $|B| = m-1$. Thus there is no blue copy of $mK_2$. So we have shown a 2-edge-coloring of $K_{3m-2}$ with no monochromatic copy of $mK_2$. Hence $R(mK_2, mK_2) > 3m-2$, and therefore $R(mK_2, mK_2) \ge 3m-1$. Now we show that $R(mK_2, mK_2) \le 3m-1$. Let $G$ be any graph on $3m-1$ vertices. Assume that $G$ does not contain $mK_2$. Let $M = \{u_1v_1, u_2v_2, \dots, u_kv_k\}$ be a maximum matching in $G$. Since $G$ contains no $mK_2$, we have $k \le m-1$. Let $U$ be the set of vertices not covered by $M$. Then $|U| = (3m-1) - 2k$. Since $M$ is a maximum matching, there cannot be any edge in $G$ with both endpoints in $U$; otherwise, we could enlarge $M$. Therefore, $U$ is an independent set in $G$, which means that $U$ is a clique in $\overline{G}$. Now fix one matching edge $u_iv_i \in M$. If both $u_i$ and $v_i$ had at least two neighbors in $G$ inside $U$, then we could choose distinct vertices $x,y \in U$ such that $u_ix$ and $v_iy$ are edges of $G$, and then replacing the edge $u_iv_i$ in $M$ by $u_ix$ and $v_iy$ would produce a larger matching in $G$, contradicting the maximality of $M$. So for each $i$, choose one endpoint $w_i \in \{u_i, v_i\}$ that has at most one neighbor in $G$ inside $U$. Then $w_i$ is adjacent in $\overline{G}$ to all but at most one vertex of $U$. We now choose distinct vertices $x_1, x_2, \dots, x_k \in U$ such that $w_ix_i$ is an edge of $\overline{G}$ for each $i$. This can be done greedily: when choosing $x_i$, at most $i-1$ vertices of $U$ have already been used, and at most one more vertex of $U$ is forbidden because it may fail to be adjacent to $w_i$ in $\overline{G}$. Since $|U| = 3m-1-2k \ge k+2$, there is always a vertex of $U$ available for the choice of $x_i$. Thus $\overline{G}$ contains the matching $\{w_1x_1, w_2x_2, \dots, w_kx_k\}$. Now remove $x_1, \dots, x_k$ from $U$, and call the remaining set $U'$. Since $U$ is a clique in $\overline{G}$, $U'$ is also a clique in $\overline{G}$. Moreover, $|U'| = |U| - k = (3m-1-2k)-k = 3m-1-3k = 3(m-k)-1$. Since $m-k \ge 1$, we have $3(m-k)-1 \ge 2(m-k)$, so the clique $U'$ contains a matching of size $m-k$. Therefore, $\overline{G}$ contains a matching of size $k + (m-k) = m$. Thus $\overline{G}$ contains $mK_2$. We have shown that for every graph $G$ on $3m-1$ vertices, either $G$ contains $mK_2$ or $\overline{G}$ contains $mK_2$. Hence $R(mK_2, mK_2) \le 3m-1$. Since we have shown both $R(mK_2, mK_2) \ge 3m-1$ and $R(mK_2, mK_2) \le 3m-1$, we conclude that $R(mK_2, mK_2) = 3m-1$. $\proofend$

## 5) What is the expected number of edges in $G \in \mathcal{G}(n, p)$?

Let $X$ be the number of edges in $G$, and for each possible edge $e$, define
$$
X_e =
\begin{cases}
1 & \text{if } e \in E(G), \\
0 & \text{if } e \notin E(G).
\end{cases}
$$
By definition, the expected value of each $X_e$ is exactly $p$, since each edge is present with probability $p$. In addition, $X = \sum_e X_e$, where the sum is taken over all possible edges of the graph. So by linearity of expectation, the expected number of edges in $G$ is the sum of the expectations of all the $X_e$. There are $\binom{n}{2}$ possible edges in a graph on $n$ vertices, so there are $\binom{n}{2}$ such random variables $X_e$. Therefore, $\mathbb{E}[X] = \sum_e \mathbb{E}[X_e] = \binom{n}{2}p$. Hence the expected number of edges in $G$ is $\binom{n}{2}p$. $\proofend$

## 6) What is the expected number of $K_r$-subgraphs in $G \in \mathcal{G}(n, p)$?

Let $X$ be the number of $K_r$-subgraphs in $G$. For each set $S$ of $r$ vertices, define
$$
X_S =
\begin{cases}
1 & \text{if the vertices in } S \text{ span a copy of } K_r, \\
0 & \text{otherwise.}
\end{cases}
$$
Then $X = \sum_S X_S$, where the sum is taken over all $r$-element subsets $S$ of $V(G)$. Now fix one such subset $S$. In order for $S$ to span a copy of $K_r$, every possible edge among those $r$ vertices must be present. There are exactly $\binom{r}{2}$ such edges, and each is present independently with probability $p$. Therefore, $\mathbb{E}[X_S] = p^{\binom{r}{2}}$. There are $\binom{n}{r}$ choices for the set $S$. So by linearity of expectation, $\mathbb{E}[X] = \sum_S \mathbb{E}[X_S] = \binom{n}{r} p^{\binom{r}{2}}$. Hence the expected number of $K_r$-subgraphs in $G$ is $\binom{n}{r} p^{\binom{r}{2}}$. $\proofend$