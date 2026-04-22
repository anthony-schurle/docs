Definitions:  
A $\underline{\text{graph property}}$ is a class of graphs closed under isomorphism.  
Ex. “being connected”

Let $p = p(n)$ be a fixed function and $P$ a graph property. Consider how
$$
\mathbb{P}[G \in P]
$$
behaves for $G \in \mathcal{G}(n, p)$ as $n \to \infty$.

We say that $G \in P$ for $\underline{\text{almost all}}$ $G \in \mathcal{G}(n, p)$ if this probability tends to 1, or that $P$ holds almost surely.

We say that $G \in P$ for $\underline{\text{almost no}}$ $G \in \mathcal{G}(n, p)$ if this probability tends to 0.

**Proposition 11.3.1**  
For every constant $p \in (0, 1)$ and every graph $H$, almost every $G \in \mathcal{G}(n, p)$ contains an induced copy of $H$.

**Proof**  
Fix $H$ and let $k := |H|$. Fix $U \subseteq V(G)$ with $|U| = k$, where $n \ge k$. Then $G[U]$ is isomorphic to $H$ with some positive probability; call it $r$. This $r$ depends on $p$, but not on $n$, since once $U$ is fixed, only the $\binom{k}{2}$ possible edges inside $U$ determine whether $G[U]$ is isomorphic to $H$.

Now $G$ contains $\left\lfloor \frac{n}{k} \right\rfloor$ disjoint such sets $U$. Then the probability that none of the corresponding subgraphs $G[U]$ is isomorphic to $H$ is
$$
(1-r)^{\left\lfloor \frac{n}{k} \right\rfloor},
$$
since these events are independent by the disjointness of the corresponding edge sets. Thus,
$$
\mathbb{P}[H \not\subseteq G \text{ induced}] \le (1-r)^{\left\lfloor \frac{n}{k} \right\rfloor} \to_{n\to\infty} 0,
$$
since we are only considering some of the possible $k$-sets. As desired. $\blacksquare$

**Prop. 11.3.1**

- $p \in (0,1)$ constant
- $H$ fixed
- $k := |H|$

Take $U \subseteq V(G)$ with $|U| = k$.

$$
\mathbb{P}[G[U] \cong H] = r > 0
$$

$r$ depends on $p$, not on $n$.

There are $\left\lfloor \frac{n}{k} \right\rfloor$ disjoint $k$-sets $U$.

$$
\mathbb{P}[\text{none induces } H]
=
(1-r)^{\left\lfloor \frac{n}{k} \right\rfloor}
$$

$$
\mathbb{P}[H \not\subseteq G \text{ induced}]
\le
(1-r)^{\left\lfloor \frac{n}{k} \right\rfloor}
\to 0
$$

$$
\therefore\ \mathbb{P}[H \subseteq G \text{ induced}] \to 1
$$