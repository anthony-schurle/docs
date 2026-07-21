## 1. Every uniquely $3$-edge-colorable cubic graph is Hamiltonian

Let the unique $3$-edge-coloring of the cubic graph $G$ have color classes $M_1,M_2,M_3$. Since the coloring is proper and $G$ is cubic, each $M_i$ is a perfect matching. Then $G[M_1\cup M_2]$ is a spanning $2$-regular graph, hence a disjoint union of cycles, with colors alternating on each cycle. If there were more than one cycle, we could interchange colors $1$ and $2$ on just one of them, producing a different proper $3$-edge-coloring and hence a different color partition, contradicting uniqueness. Thus $G[M_1\cup M_2]$ is one spanning cycle, so it is a Hamilton cycle of $G$. $\proofend$

## 2. If $G$ is $2$-connected and $P_3$-free, then $G$ is Hamiltonian

Since $G$ is $2$-connected, it is connected and has at least three vertices. We claim $G$ is complete. If not, choose nonadjacent vertices $u,v$ and a shortest $u$-$v$ path $u=x_0,x_1,\dots,x_k=v$. Since $uv\notin E(G)$, $k\ge 2$, and by minimality $x_0x_2\notin E(G)$. Thus $x_0,x_1,x_2$ induce a $P_3$, contradiction. Hence $G\cong K_n$ for some $n\ge 3$, and $K_n$ has a Hamilton cycle. Therefore $G$ is Hamiltonian. $\proofend$

## 3. For any graph $G$, the line graph $L(G)$ is claw-free

Suppose $L(G)$ contains an induced claw with center corresponding to an edge $e=xy\in E(G)$ and leaves corresponding to edges $e_1,e_2,e_3\in E(G)$. Since each leaf is adjacent to the center in $L(G)$, each $e_i$ is incident with $e$, so each $e_i$ is incident with either $x$ or $y$. Among three such edges and two endpoints, two of the $e_i$ share an endpoint. Those two edges are incident in $G$, so their corresponding vertices are adjacent in $L(G)$, contradicting that the leaves of an induced claw are pairwise nonadjacent. Hence $L(G)$ is claw-free. $\proofend$

## 4. For constant $p\in(0,1)$, almost every graph in $G(n,p)$ has diameter $2$

Let $G\in G(n,p)$ with fixed $p\in(0,1)$. For distinct vertices $u,v$, the event $d(u,v)>2$ means $uv\notin E(G)$ and $u,v$ have no common neighbor, so $\Pr(d(u,v)>2)=(1-p)(1-p^2)^{n-2}$. By the union bound, $\Pr(\exists u,v:d(u,v)>2)\le \binom n2(1-p)(1-p^2)^{n-2}\to 0$, since $0<1-p^2<1$ is constant. Thus almost surely every pair of vertices has distance at most $2$. Also $\Pr(G=K_n)=p^{\binom n2}\to 0$, so almost surely $G$ is not complete and hence does not have diameter $1$. Therefore almost every graph $\operatorname{diam}(G)=2$. $\proofend$

## 5. Show that the Petersen graph is isomorphic to $\overline{L(K_5)}$

Label the vertices of $K_5$ by $\{1,2,3,4,5\}$. The vertices of $L(K_5)$ are the edges of $K_5$, so the vertices of $\overline{L(K_5)}$ may be identified with the $2$-element subsets of $\{1,2,3,4,5\}$. In $L(K_5)$, two such vertices are adjacent exactly when the corresponding $2$-subsets intersect, so in $\overline{L(K_5)}$, two vertices are adjacent exactly when the corresponding $2$-subsets are disjoint. Now list the five vertices $12,34,15,23,45$ as an outer cycle; consecutive pairs are disjoint, so they are adjacent. The remaining five vertices are $13,24,35,14,25$, and they form the inner star since $13$ is adjacent to $24$ and $25$, $24$ is adjacent to $13$ and $35$, $35$ is adjacent to $24$ and $14$, $14$ is adjacent to $35$ and $25$, and $25$ is adjacent to $14$ and $13$. Finally, the remaining adjacencies are the five $12$-$35$, $34$-$25$, $15$-$24$, $23$-$14$, and $45$-$13$. This is exactly the usual drawing of the Petersen graph. Hence the Petersen graph is isomorphic to $\overline{L(K_5)}$. $\proofend$