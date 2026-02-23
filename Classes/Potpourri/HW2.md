1) Prove or disprove: a graph on at least 3 vertices is bipartite iff no two adjacent vertices have the same distance from any other vertex.
Proving the entire statement false is fairly trivial, consider the graph $G = (\{v_1,v_2,v_3\}, \{\{v_1,v_2\}\})$ which has at least three vertices and can contains two partitions $(v_1)$ and $(v_2, v_3)$. Notice both $v_1$ and $v_2$ have infinite distance from $v_3$ and are also adjacent. Therefore, if a graph it bipartite, it does not imply that no two adjacent vertices have the same distance from any other vertex. (infinite distances are not necessary for the counterexample but easiest, it seems being connected is the primary constraint)

But the other direction is true:
Let G be a graph of at least three vertices and suppose no two adjacent vertices have the same distance from any other vertex. If G contains no edges then it is trivially bipartite, so suppose G has at least one edge. If there existed a disconnected vertex $v \in V(G)$, then we would have $x, y \in V(G)$ adjacent (there is at least one edge) and we same distance (infinite) from v which contradicts our assumption. Therefore, G is connected. Suppose G contained an odd cycle defined by $C := xPy + yx$. Then $xPy$ has even length so that C is odd. Then we can take the central vertex $v \in V(xPy)$, which exists because $|V(C)| \ge 3$. Because $xPy$ is even with x and y being the endpoints, we immediately see that both x and y are the same distance from v. However, because x and y are adjacent, we arrive at a contradiction of our assumptions. Therefore, G does not contain an odd cycle. Thus, it immediately follows by Proposition 1.6.1 that G is bipartite.

Connected bipartite graphs should have the forward implication?

Let G be a connected bipartite graph on at least three vertices, and so no infinite distances. Suppose $v_1, v_2 \in V(G)$ were adjacent with same distance, $d$,  from $v_3 \in V(G)$. Consider $v_1Pv_3$ and $v_2Pv_3$ paths defined by distance $d$. See that we can create a cycle $C := v_1Pv_3 + v_3Pv_2 + v_2v_1$ since $v_2$ and $v_1$ are adjacent. Notice, the length of such a cycle is $2d + 1$ which is an odd cycle. However, this is a contradiction of proposition 1.6.1 and so no two adjacent vertices have the same distance from any other vertex. $\blacksquare$

2) Let M be a matching in a bipartite graph G. Show that if M is sub-optimal, then G contains an augmenting path with respect to M. Does this generalize to non-bipartite graphs?
Let M* be a maximum matching such that $|M*| > |M|$. Define $H = M \Delta M*$. In H, every vertex has degree at most 2 by definition of a matching, so H is a union of paths and cycles. Since $|M*| > |M|$, there is a component with more M* edges than M edges. We can construct a path starting and ending with M* edges that alternates with M edges (no vertex can contain two M* or M edges). This path then starts and ends with unmatched vertices in M which makes an M-augmenting path.

This does generalize, the proof does not use the bipartite constraint. $\blacksquare$

3)
a) Find a bipartite graph with a set of preferences such that no matching of maximum size is stable and no stable matching has maximum size.
Consider the bipartite graph of $G = (\{a, b, 1, 2\}, \{\{a, 1\}, \{b, 2\}, \{a, 2\}\})$. Clearly, the only maximal matching is $M := \{\{a, 1\}, \{b, 2\}\}$. Let the set of preferences be $a1 \le_a a2$, $b2 \le_2 a2$. It follows that M is not stable since for edge $a2$, there is no edge in M that is more preferred by either vertex a or 2. Since there is only one maximal matching, we found a bipartite graph with a set of preferences such that no matching of maximum size is stable and no stable matching has maximum size. $\blacksquare$

b) Find a non-bipartite graph with a set of preferences that has no stable matching.
Consider $C_3$ with the vertex set $\{v_1, v_2, v_3\}$ and set of preferences $v_1v_3 \le_{v_1} v_1v_2$, $v_1v_2 \le_{v_2} v_2v_3$, and $v_2v_3 \le_{v_3} v_1v_3$. Clearly, $C_3$ is not bipartite because it is an odd cycle. Now we exhaustively consider every possible matching.
$\{v_1v_2\}$:
This is unstable because $v_2$ prefers the edge $v_2v_3$.

$\{v_1v_3\}$:
This is unstable because $v_1$ prefers the edge $v_1v_2$.

$\{v_2v_3\}$:
This is unstable because $v_3$ prefers the edge $v_1v_3$.

So, every possible matching is unstable. Thus, we found a non-bipartite graph with a set of preferences that has no stable matching. $\blacksquare$

c) Find a cubic graph without a 1-factor.
Consider the graph, G with vertex set $\{1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16\}$ and edge set,
$$
\begin{aligned}
\{&
1-2,1-4,1-3,2-3,3-4,2-5, \\ &
4-5,5-16,6-16,11-16,6-7, \\ &
6-9,7-8,8-9,7-10,8-10,9-10, \\ &
11-12,11-15,12-13,13-15, \\ &
12-14,13-14,15-14\}
\end{aligned}
$$
I will also attach an image for easier visualization (with vertex 16 being the cut vertex of the three odd components):
![[IMG_1402.jpg]]

Let $S := \{16\} \subseteq V(G)$. Notice $q(G - S) = 3 > |S| = 1$. Therefore, by theorem 2.2.1, G does not have a 1-factor. Because G is a cubic graph, we found a cubic graph without a 1-factor. $\blacksquare$


4) Show that if G is an (r − 1)-edge connected r-regular graph of even order, then G has a 1-factor.
Lemma: In an r-regular graph , if C is a component of $G-S$ with $|V(C)|$ odd, then $|\{uv \in E(G) : u \in V(C), v \in S\}| \ne r-1$. (In other words the edge count between any odd component and a subset of V(G) is not equal to $r - 1$).

Suppose $|\{uv \in E(G) : u \in V(C), v \in S\}| = r-1$. The degree sum in C gives $r|V(C)| = 2E(C) + |\{uv \in E(G) : u \in V(C), v \in S\}| = 2E(C) + (r - 1)$.  Therefore, $2E(C) = r(|V(C)| - 1) + 1$. But $|V(C)|$ is odd which suggests $2E(C)$ is odd. This is a contradiction and so the lemma follows.

We verify Tutte's condition, $q(G - S) \le |S|$ for all $S \subseteq V(G)$. Case 1: If $S = \emptyset$ then $q(G) = 0$ since G has even order. Case 2: If $S \ne \emptyset$, let C be an odd component of $G - S$. Because G is $(r-1)$-edge-connected and by our lemma, we see that there are r or more edges between the component and S. The summation of all such edges for all odd components is greater than or equal to $r \times q(G - S)$. But these edges must come from S, which has total degree $r|S|$. We see that $r \times q(G - S) \le r|S|$. Thus, by Tutte's theorem, G has a 1-factor. $\blacksquare$

5) Show that the block graph of any connected graph is a tree.
Let $B_1$ and $B_2$ be any two blocks of G. Since G is connected, there is a path P in G from some vertex in $B_1$ to some vertex in $B_2$. As we traverse P, we pass through a sequence of blocks. When P leaves one block and enters another, it must pass through a cut vertex (blocks are maximal). We then have the path $B_1c_1B_3c_2...c_kB_2$ where each $c_i$ is a cut vertex. Therefore, we have shown the block graph is connected. Suppose a cycle existed in the block graph, $C := B_1c_1B_2c_2...c_kB_!$. Consider the subgraph H in G formed by the union of all these blocks. Take any two vertices v and w in H. Since the blocks form a cycle, we can find two distinct paths from v to w (going in either direction of the cycle formed by cut vertices and by the 2-connectivity of each individual block). But then H is 2-connected contradicting maximality of each individual block. Therefore, the block graph has no cycles. (a block graph of one or no vertices is trivially a tree). Thus, the block graph is a tree because it is connected and acyclic. $\blacksquare$