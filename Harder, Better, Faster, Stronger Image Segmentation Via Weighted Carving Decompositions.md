**Proposition 1**
Let $G$ be a graph constructed from an image $I$. Let $G^*$ be the geometric dual of $G$ such that $w_{G^*}(e) = \frac{1}{EB(e)}$ for all $f \in E(G^*)$ such that $f$ crosses $e$. Define $\mathcal{C}$ to be the collection of all minimal cycles in $G^*$. Then the first separation formed by removing edges of $G$ in ascending inverse order of edge betweenness is equivalent to the separation formed by $G \backslash S$, where $S$ is the set of edges crossed by a minimum cycle $C \in \mathcal{C}$ in $G^*$. 

**Proof**. 


**Proposition 2**
The cycle $C$ produced from *Proposition 1* satisfies $C = \max_{c \in \mathcal{C}}\min_{e \in c} EB(e)$.

**Proposition 3**
Let $e_j$ be the edge that first separates $A$ from $B$ as in *Proposition 1*. 

Let $e_1, e_2, ..., e_n$ be the edge sequence produced by priority queue $F$ in *Proposition 1*. Define $G'$ to be the complement of $G$. Then there is a edge sequence $f_1, f_2, ..., f_k$ of $e_1, e_2, ..., e_n$ such that $\{f_1, f_2, ..., f_k\} \cup G'$ is connected. Indeed $(\{e_1, e_2, ..., e_n\} - \{f_1, f_2, ..., f_k\}) \cup f_k$ is equivalent to the edges removed to form a separation in *Proposition 1*.

**Proof**.

**Theorem 1**
The carving width of $H$ produced in the algorithm is bounded by the optimal carving width in a certain way...
