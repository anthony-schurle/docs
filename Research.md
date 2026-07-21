Definitions:
Branch Decomposition -
Let G be a graph and T a tree with $|E(G)|$ leaves where every non-leaf node has degree 3. Let v be a bijection from the edges of G to the leaves of T. The pair $(T, v)$ is called branch decomposition of G. Called optimal if width equals $\beta(G)$.

Middle set -
An edge of T, call it e, partitions the edges of G into two subsets $A_e$ and $B_e$. The middle set, $mid(e)$, is the set of nodes of G that are incident with $A_e$ and $B_e$.

Width -
Width of $(T, v)$ is the maximum cardinality of any middle set of T.

Branchwidth -
Denoted $\beta(G)$. Minimum width of any branch decomposition of G.

Separation -
Let G be a graph. A separation is $(G_1, G_2)$ of subgraphs of G with $G_1 \cup G_2 = G$ and $E(G_1) \cap E(G_2) = \emptyset$.

Tangle -
Tangle of G of order k is the set T corresponding to separations of G, each of order $< k$ such that:
T1: For each separation $(A, B)$ of $G$ of order $<k$, either A or B is an element of T.
T2: 
