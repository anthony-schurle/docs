# Chapter 1: Connectedness And Compactness
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 1.0 Connected Spaces
---
### Definitions
- **Connected**
  - A space X is connected if there does not exist a separation on X - a pair U, V of disjoint nonempty open subsets of X whose union is X.
  - A space X is connected iff the only subsets of X that are both open and closed in X are the empty set and X itself.

### Theorems & Proofs
**Lemma 23.1**
If Y is a subspace of X, a separation of Y is a pair of disjoint nonempty sets A and B whose union is Y, neither of which contains a limit point of the other. The space Y is connected if there exists no separation of Y.

**Lemma 23.2**
If the sets C and D form a separation of X, and if Y is a connected subspace of X, then Y lies entirely within either C or D.

**Theorem 23.3**
The union of a collection of connected subspaces of X that have a point in common is connected.

**Theorem 23.4**
Let A be a connected subspace of X. If $A \subseteq B \subseteq \overline{A}$, then B is also connected.

**Theorem 23.5**
The image of a connected space under a continuous map is connected.

**Theorem 23.6**
A finite cartesian product of connected spaces is connected.

### Examples
**Example Title**
**Problem 1:**
Let $\Gamma$ and $\Gamma '$ be two topologies on X. If $\Gamma \subseteq \Gamma '$, what does connectedness of X in one topology imply about connectedness in the other?
**Solution:**
We show that connectedness in $\Gamma '$ implies connectedness in $\Gamma$. Suppose X is not connected in $\Gamma$, such there there are two disjoint, open sets U and V where $X = U \cup V$. Since $\Gamma \subseteq \Gamma '$, U and V are also disjoint, open sets of $\Gamma '$ whose union is X. By definition, X is connected under $\Gamma '$. We not show that connectedness in $\Gamma$ does not imply connectedness in $\Gamma'$ with a counterexample. Let $X = \{a,b\}$ and define $\Gamma$ to be the indiscrete topology while $\Gamma '$ is the discrete topology. $\Gamma$ is connected by construction and X is separated by $\{a\}, \{b\}$ in $\Gamma '$ so that $\Gamma '$ is not connected. $\blacksquare$

**Problem 2:**
Let $\{A_n\}$ be a sequence of connected subspaces of X, such that $A_n \cap A_{n+1} \ne \emptyset$ for all n. Show that $\bigcup A_n$ is connected.
**Solution:**
We show by induction for the finite case that $U_k = \bigcup_{n=1}^k A_n$ is connected for all k. $U_1 = A_1$ is trivially connected. Now suppose $U_k$ is connected and consider $U_{k+1} = U_k \cup A_{k+1}$. By assumption, $A_k \cap A_{k+1} \ne \emptyset$ and since $A_k \subseteq U_k$, it follows that $U_k \cap A_{k+1} \ne \emptyset$. By Theorem 23.3, $U_{k+1}$ must be connected. Therefore, $U_k$ is connected for all k. Notice that $A_1 \subseteq U_1 \subseteq U_2 \subseteq ...$ and so all $U_k$ share a point in common. Thus, by theorem 23.3, the union of all $U_k$ for all k is connected. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–152