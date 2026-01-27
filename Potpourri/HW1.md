1)Let $n \in \mathbb{N}$ and $V = \{0, 1\}^n$ ; thus, V is the set of all 0 − 1 sequences of length n. The graph on V in which two such sequences form an edge iff they differ in exactly one position is called the n-dimensional cube or n-dimensional hypercube, and is sometimes denoted $H_n$. Determine the average degree, number of edges, diameter, girth, and circumference of this graph. (Hint for the circumference: induct on n.)

($d(H_n)$)
$d(H_n) = n$
Let $v \in V(H_n)$. By definition $d(v) = n$ because there are n potential elements of v that can differ, and only one can at a time. It follows that because v was arbitrary, all vertices have degree n. Therefore, $d(H_n) = \frac{\sum_{v \in V(H_n)}d(v)}{|V(H_n)|} = \frac{|V(H_n)|d(v)}{|V(H_n)|} = d(v) = n$.

($||H_n||$)
We show $|V(H_n)| = 2^n$. Let $n = 1$. We see that the only possible 0-1 sequences of length 1 are $\{0\}$ and $\{1\}$. Now suppose $|V(H_n)| = 2^n$. For each $v \in V(H_n)$, append 0 at the end of the sequence. This is a combination of length n + 1. Each such combination is still unique because the first n digits of all sequences are unique. Similar reasoning follows for appending 1 at the end of each sequence. The group of 0s appended and the group of 1s appended are also unique from each other because of the last appended digit. But we have then doubled our total sequences and so $|V(H_{n+1})| = 2 \times 2^n = 2^{n+1}$. Therefore, $|V(H_n)| = 2^n$. It follows that $||H_n|| = 0.5d(H_n)|V(H_n)| = 0.5n2^{n} = n2^{n-1}$.

($diam(G)$)
Take arbitrary $x := \{x_1, x_2, ..., x_n\}, y := \{y_1, y_2, ..., y_n\} \in V(H_n)$. We first find a path $xPy$ and then show it is shortest. Find the first $x_i \ne y_i$ for $i \le n$. Move to a neighbor of x such that $x_i = y_i$, which exists by definition of the edges in the graph. Continue for the next $x_i \ne y_i$ until y is reached. Then $xPy$ has been found. A vertex was traversed for each $x_i \ne y_i$ and so $xP^ky$ where $k := \sum_{i = 1}^n (x_i + y_i)mod(2)$. Suppose a shorter path T existed such that $xTy$. Then T at least one element in P where $x_i \ne y_i$ was not traversed.  But this is not possible by definition of edges and so T does not exist. k is maximized clearly when $x_i$ and $y_i$ are different for all i which sums to 1. So $k = n(1) = n$. Therefore, $diam(G) = n$.

($g(H_n)$)
Case 1: $n \ge 2$. Take $x := \{0, 0, ..., 0\} \in V(H_n)$. There is a neighbor $y := \{0, 1, 0, ..., 0\}$ of x. Also, there is a neighbor $z := \{1, 1, 0, 0, ..., 0\}$ of y. Continuing, there is a $f := \{1, 0, 0, ..., 0\}$ of z. Notice f is a neighbor of x. So we have a cycle $xyzfx$ and its length is 4. Suppose we had a shorter cycle with length 3. Then it can be defined by the vertices vnmv. Then there is some k such that $v_k \ne n_k$. Continuing, there is some $l \ne k$ - else we return to v - such that $n_l \ne m_l$. It follows that there is some $p \ne l$ - else we return to m - such that $m_p \ne v_p$ and m is a neighbor of v. But this is a contradiction because m differs from v by at least two digits and so can not be neighbors. Thus, $g(H_n) = 4$.

(Circumference)

2)Let G be a graph. If $\delta(G) = d \ge 2$ and $g(G) = g \in \mathbb{N}$, prove that
$$
|G| \ge \begin{cases} 1 + d\sum_{i = 0}^{r - 1}(d - 1)^i & \text{if } 2r + 1 := g,\\ 2\sum_{i = 0}^{r - 1}(d - 1)^i  & \text{if } 2r := g. \end{cases}
$$

Suppose $\delta(G) = d \ge 2$ and $g(G) = g \in \mathbb{N}$. Suppose $2r = g$ for $r \in \mathbb{N}$, meaning g is even. 

3)Determine $\kappa(G)$ and $\lambda(G)$ for $G = P_n, C_n, K_n, K_{m, n}$, and $H_n$ where $n, m \ge 3$.

($P_n$)
Let $P_n$ be represented by $x_1x_2...x_n$.
Define arbitrary set $X \subseteq V(P_n) \land |X| = 0$. Clearly, $P_n - X$ is connected because $P_n$ is connected. So $P_n$ is 1-connected. Define $X := \{x_2\}$. $P_n - X$ isolates $x_1$ which now no longer has any neighbors. This means, no path exists between $x_1$ and $x_3$ and so $P_n - X$ is disconnected. Therefore, $P_n$ is not 2-connected. Thus, $\kappa(P_n) = 1$.




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






4)
a) Show that every 2-connected graph contains a cycle.

Call the graph G. Take arbitrary $x, y \in V(G)$. 
Case 1: x and y are not neighbors. Because G is 2-connected, there is some path $xPy$ linking x and y. Now pick $v \in xPy$ where $v \ne  x \land v \ne y$. Consider the graph $G - v$ which must have a path $xWy$ because G is 2-connected. Notice $xWy \ne xPy$ because $v \not \in V(G - v)$. We then found cycle $C := xPyWx$.
Case 2: x and y are neighbors. Pick arbitrary $v \in V(G)$ where $v \ne \land v \ne y$. By connectivity there exists a path $xPv$ and $vWy$. But then we found cycle $C := xPvWyx$.
Thus, every 2-connected graph contains a cycle.

b)Show the (i) $\iff$ (iv) implication of Theorem 1.5.1.

($\implies$) Suppose T is a tree which is acyclic by definition. Pick arbitrary non-adjacent $t_1, t_2 \in T$. There exists $t_1Pt_2$ by definition. But then $T + t_1t_2$ creates cycle $t_1Pt_2t_1$ and since $t_1,t_2$ were arbitrary, T is maximally acyclic. ($\Longleftarrow$) Suppose T is maximally acyclic. Now suppose T was not connected. Then there exists some $t_1, t_2 \in V(T)$ with infinite distance. Now consider $T + t_1t_2$, which is a graph with a subgraph containing the bridge $t_1t_2$. This subgraph does not contain a cycle because a bridge does not lie on a cycle and it was acyclic to begin with. But T was maximally acyclic and so this is a contradiction. Therefore, T is connected, and by definition a tree.
