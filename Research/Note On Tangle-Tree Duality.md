# Notes on Abstract Separation Systems

## 2.1 Separations of Sets

This section introduces separations of sets as the concrete model motivating abstract separation systems.

**Definition 2.1.1 (Separation of a set).** A separation of a set $V$ is a set $\{A,B\}$ such that $A \cup B = V$. Here $A \cap B$ is allowed to be nonempty.

**Definition 2.1.2 (Orientation of a separation of a set).** For a separation $\{A,B\}$ of $V$, its orientations are $(A,B)$ and $(B,A)$. Informally, $(A,B)$ points toward $B$ and away from $A$.

**Definition 2.1.3 (Inverse orientation).** The inverse orientation is given by $f(A,B) = (B,A)$. The map $f$ is an involution, meaning $f(f(A,B)) = (A,B)$.

**Definition 2.1.4 (Order on oriented separations of a set).** The partial order on oriented separations of $V$ is defined by $(A,B) \le (C,D)$ if and only if $A \subseteq C$ and $D \subseteq B$.

**Proposition 2.1.5 (The inverse map reverses the order).** The inverse map $f(A,B) = (B,A)$ reverses the partial order from Definition 2.1.4.

**Proof.** Suppose $(A,B) \le (C,D)$. Then $A \subseteq C$ and $D \subseteq B$. Now $f(A,B) = (B,A)$ and $f(C,D) = (D,C)$. Since $D \subseteq B$ and $A \subseteq C$, we have $(D,C) \le (B,A)$. Therefore $f(C,D) \le f(A,B)$, so $f$ reverses the order. $\blacksquare$

**Definition 2.1.6 (Degenerate oriented separation of a set).** An oriented separation $(A,B)$ of $V$ is degenerate if $(A,B) = (B,A)$.

**Example 2.1.7 (The degenerate separation of a set).** The oriented separation $(V,V)$ is degenerate.

**Proposition 2.1.8 (Uniqueness of the degenerate separation of a set).** A set $V$ has exactly one degenerate oriented separation, namely $(V,V)$.

**Proof.** Existence is clear since $(V,V) = (V,V)$. For uniqueness, suppose $(A,B) = (B,A)$ is an oriented separation of $V$. Equality of ordered pairs gives $A = B$. Hence $(A,B) = (A,A)$. Since $(A,A)$ is a separation of $V$, we have $A \cup A = V$, so $A = V$. Therefore $(A,B) = (V,V)$. $\blacksquare$

---

## 2.2 Separation Systems

This section abstracts the order-theoretic structure of separations of sets.

**Definition 2.2.1 (Separation system).** A separation system is a triple $(\overrightarrow{S}, \le, *)$, where $\overrightarrow{S}$ is a partially ordered set and $*$ is an order-reversing involution. The elements of $\overrightarrow{S}$ are called oriented separations.

**Definition 2.2.2 (Inverse of an oriented separation).** For $\overrightarrow{s} \in \overrightarrow{S}$, we write $\overrightarrow{s}^{*} = \overleftarrow{s}$. Similarly, $\overleftarrow{s}^{*} = \overrightarrow{s}$. The condition that $*$ is order-reversing means that, for all $\overrightarrow{r}, \overrightarrow{s} \in \overrightarrow{S}$, $\overrightarrow{r} \le \overrightarrow{s}$ if and only if $\overleftarrow{r} \ge \overleftarrow{s}$.

**Definition 2.2.3 (Unoriented separation).** An unoriented separation is a set $s = \{\overrightarrow{s}, \overleftarrow{s}\}$. The elements $\overrightarrow{s}$ and $\overleftarrow{s}$ are called the orientations of $s$.

**Definition 2.2.4 (Set of unoriented separations).** The set of all unoriented separations is denoted $S$. Given $S' \subseteq S$, we write $\overrightarrow{S'} := \bigcup S' \subseteq \overrightarrow{S}$.

**Definition 2.2.5 (Pointing toward and away).** The oriented separation $\overrightarrow{r}$ points toward $s$ if $\overrightarrow{r} \le \overrightarrow{s}$ or $\overrightarrow{r} \le \overleftarrow{s}$. In this case, $\overleftarrow{r}$ points away from $s$.

**Definition 2.2.6 (Degenerate separation).** A separation $s$ is degenerate if $\overrightarrow{s} = \overleftarrow{s}$. In this case, both $s$ and $\overrightarrow{s}$ are called degenerate.

**Definition 2.2.7 (Universe of separations).** A universe of separations is a structure $(\overrightarrow{S}, \le, *, \lor, \land)$, where $\lor$ is the least upper bound operation and $\land$ is the greatest lower bound operation. Equivalently, $\overrightarrow{r} \lor \overrightarrow{s}$ is the supremum of $\overrightarrow{r}$ and $\overrightarrow{s}$, while $\overrightarrow{r} \land \overrightarrow{s}$ is their infimum.

**Example 2.2.8 (Universe of separations of a set).** The oriented separations of a set $V$ form a universe of separations. If $\overrightarrow{r} = (A,B)$ and $\overrightarrow{s} = (C,D)$, then $(A,B) \lor (C,D) = (A \cup C, B \cap D)$, and $(A,B) \land (C,D) = (A \cap C, B \cup D)$.

**Proposition 2.2.9 (De Morgan law).** In a universe of separations, $(\overrightarrow{r} \lor \overrightarrow{s})^{*} = \overleftarrow{r} \land \overleftarrow{s}$.

**Proof.** Let $\overrightarrow{x} = \overrightarrow{r} \lor \overrightarrow{s}$. Then $(\overrightarrow{r} \lor \overrightarrow{s})^{*} = \overleftarrow{x}$. Since $\overrightarrow{x}$ is an upper bound for $\overrightarrow{r}$ and $\overrightarrow{s}$, we have $\overrightarrow{r} \le \overrightarrow{x}$ and $\overrightarrow{s} \le \overrightarrow{x}$. Since $*$ is order-reversing, $\overleftarrow{r} \ge \overleftarrow{x}$ and $\overleftarrow{s} \ge \overleftarrow{x}$. Hence $\overleftarrow{x}$ is a lower bound for $\overleftarrow{r}$ and $\overleftarrow{s}$. Now let $\overrightarrow{y}$ be any lower bound of $\overleftarrow{r}$ and $\overleftarrow{s}$. Then $\overrightarrow{y} \le \overleftarrow{r}$ and $\overrightarrow{y} \le \overleftarrow{s}$. Applying $*$ gives $\overleftarrow{y} \ge \overrightarrow{r}$ and $\overleftarrow{y} \ge \overrightarrow{s}$. Thus $\overleftarrow{y}$ is an upper bound of $\overrightarrow{r}$ and $\overrightarrow{s}$. Since $\overrightarrow{x} = \overrightarrow{r} \lor \overrightarrow{s}$ is the least upper bound, we have $\overrightarrow{x} \le \overleftarrow{y}$. Applying $*$ again gives $\overleftarrow{x} \ge \overrightarrow{y}$. Therefore every lower bound $\overrightarrow{y}$ of $\overleftarrow{r}$ and $\overleftarrow{s}$ lies below $\overleftarrow{x}$. Hence $\overleftarrow{x}$ is the greatest lower bound of $\overleftarrow{r}$ and $\overleftarrow{s}$. So $\overleftarrow{x} = \overleftarrow{r} \land \overleftarrow{s}$. Therefore $(\overrightarrow{r} \lor \overrightarrow{s})^{*} = \overleftarrow{r} \land \overleftarrow{s}$. $\blacksquare$

---

## 2.3 Small and Trivial Separations

This section introduces two special kinds of oriented separations: small separations and trivial separations.

### Small Separations

**Definition 2.3.1 (Small separation).** An oriented separation $\overrightarrow{r} \in \overrightarrow{S}$ is small if $\overrightarrow{r} \le \overleftarrow{r}$.

**Example 2.3.2 (Small separations of a set).** For separations of a set $V$, the small separations are precisely those of the form $(A,V)$.

**Proof.** Consider some separation $(A, B)$ of $V$. By definition, $A \cup B = V$. Since $(A, B)$ is small, we must have $(A, B) \le (B, A)$ which indicates that $A \subseteq B$. Hence $A \cup B = B$, giving $B = V$. Thus, we see that all small separations of $V$ must be of the form $(A, V)$ for some set $A \subseteq V$. $\proofend$

**Proposition 2.3.3 (Small separations are closed downward).** If $\overrightarrow{s}$ is small, then every $\overrightarrow{r} \le \overrightarrow{s}$ is small.

**Proof.** Suppose $\overrightarrow{r} \le \overrightarrow{s}$. Since $*$ is order-reversing, $\overleftarrow{s} \le \overleftarrow{r}$. Since $\overrightarrow{s}$ is small, $\overrightarrow{s} \le \overleftarrow{s}$. Therefore $\overrightarrow{r} \le \overrightarrow{s} \le \overleftarrow{s} \le \overleftarrow{r}$. Hence $\overrightarrow{r} \le \overleftarrow{r}$, so $\overrightarrow{r}$ is small. $\blacksquare$

### Trivial Separations

**Definition 2.3.4 (Trivial separation).** An oriented separation $\overrightarrow{r} \in \overrightarrow{S}$ is trivial in $S$ if there exists some $s \in S$ such that $\overrightarrow{r} < \overrightarrow{s}$ and $\overrightarrow{r} < \overleftarrow{s}$.

**Definition 2.3.5 (Witness of triviality).** If $s \in S$ satisfies $\overrightarrow{r} < \overrightarrow{s}$ and $\overrightarrow{r} < \overleftarrow{s}$, then $s$ is called a witness of $\overrightarrow{r}$ and its triviality.

**Definition 2.3.6 (Co-trivial separation).** If $\overrightarrow{r}$ is trivial, then its inverse $\overleftarrow{r}$ is called co-trivial.

**Example 2.3.7 (Trivial separations of a set).** For separations of a set $V$, the trivial separations are those of the form $\overrightarrow{r} = (X,V)$ for which there exists $s = \{A,B\} \in S \setminus \{r\}$ with $X \subseteq A \cap B$.

**Proposition 2.3.8 (Trivial separations are small and nondegenerate).** Every trivial separation is small and not degenerate.

**Proof.** Suppose $\overrightarrow{r}$ is trivial, witnessed by $s \in S$. Then $\overrightarrow{r} < \overrightarrow{s}$ and $\overrightarrow{r} < \overleftarrow{s}$. By order-reversal, $\overrightarrow{r} < \overrightarrow{s}$ implies $\overleftarrow{r} > \overleftarrow{s}$. Thus $\overrightarrow{r} < \overleftarrow{s} < \overleftarrow{r}$. Therefore $\overrightarrow{r} < \overleftarrow{r}$, so $\overrightarrow{r}$ is small. Since $\overrightarrow{r} < \overleftarrow{r}$ is strict, we have $\overrightarrow{r} \ne \overleftarrow{r}$. Hence $\overrightarrow{r}$ is not degenerate. $\blacksquare$

**Remark 2.3.9 (Small but nontrivial separations).** Small but nontrivial separations can exist, but only maximal small separations can be nontrivial. Indeed, if $\overrightarrow{s}$ is small and $\overrightarrow{r} < \overrightarrow{s}$, then $\overrightarrow{r} < \overrightarrow{s} \le \overleftarrow{s}$. Thus $\overrightarrow{r}$ is trivial, witnessed by $s$.

**Proposition 2.3.10 (Trivial separations are closed downward).** If $\overrightarrow{s}$ is trivial and $\overrightarrow{r} \le \overrightarrow{s}$, then $\overrightarrow{r}$ is trivial.

**Proof.** Suppose $\overrightarrow{s}$ is trivial, witnessed by $t \in S$. Then $\overrightarrow{s} < \overrightarrow{t}$ and $\overrightarrow{s} < \overleftarrow{t}$. If $\overrightarrow{r} \le \overrightarrow{s}$, then $\overrightarrow{r} \le \overrightarrow{s} < \overrightarrow{t}$ and $\overrightarrow{r} \le \overrightarrow{s} < \overleftarrow{t}$. Thus $\overrightarrow{r} < \overrightarrow{t}$ and $\overrightarrow{r} < \overleftarrow{t}$. Therefore $\overrightarrow{r}$ is trivial, witnessed by $t$. $\blacksquare$

---

## 2.4 Nestedness and Consistency

This section introduces nested separations, crossing separations, orientations, and consistency.

### Nestedness

**Definition 2.4.1 (Nested separations).** Separations $r,s \in S$ are nested if they have comparable orientations. That is, $r$ and $s$ are nested if some orientation of $r$ is comparable with some orientation of $s$.

**Definition 2.4.2 (Nested oriented separations).** Oriented separations $\overrightarrow{r}$ and $\overrightarrow{s}$ are nested if the underlying unoriented separations $r$ and $s$ are nested.

**Definition 2.4.3 (Nested set of separations).** A set of separations is nested if every two of its elements are nested.

**Definition 2.4.4 (Crossing separations).** Two separations cross if they are not nested.

**Proposition 2.4.5 (Nested oriented separations have three possible configurations).** If $\overrightarrow{r}$ and $\overrightarrow{s}$ are nested, then they are comparable, point towards each other, or point away from each other.

**Proof.** Suppose $\overrightarrow{r}$ and $\overrightarrow{s}$ are nested. Then $r$ and $s$ have comparable orientations. There are eight possible comparisons: $\overrightarrow{r} \le \overrightarrow{s}$, $\overrightarrow{s} \le \overrightarrow{r}$, $\overleftarrow{r} \le \overleftarrow{s}$, $\overleftarrow{s} \le \overleftarrow{r}$, $\overrightarrow{r} \le \overleftarrow{s}$, $\overleftarrow{s} \le \overrightarrow{r}$, $\overleftarrow{r} \le \overrightarrow{s}$, or $\overrightarrow{s} \le \overleftarrow{r}$. By order-reversal, these reduce to four cases: $\overrightarrow{r} \le \overrightarrow{s}$, $\overrightarrow{s} \le \overrightarrow{r}$, $\overrightarrow{r} \le \overleftarrow{s}$, or $\overleftarrow{r} \le \overrightarrow{s}$. In the first two cases, $\overrightarrow{r}$ and $\overrightarrow{s}$ are comparable. If $\overrightarrow{r} \le \overleftarrow{s}$, then $\overrightarrow{r}$ points toward $s$. By order-reversal, $\overrightarrow{s} \le \overleftarrow{r}$, so $\overrightarrow{s}$ points toward $r$. Hence $\overrightarrow{r}$ and $\overrightarrow{s}$ point towards each other. If $\overleftarrow{r} \le \overrightarrow{s}$, then $\overrightarrow{r}$ points away from $s$. By order-reversal, $\overleftarrow{s} \le \overrightarrow{r}$, so $\overrightarrow{s}$ points away from $r$. Hence $\overrightarrow{r}$ and $\overrightarrow{s}$ point away from each other. $\blacksquare$

### Orientations and Consistency

**Definition 2.4.6 (Antisymmetric set of oriented separations).** A set $O \subseteq \overrightarrow{S}$ is antisymmetric if, for every nondegenerate $s \in S$, the set $O$ does not contain both $\overrightarrow{s}$ and $\overleftarrow{s}$. Equivalently, $O$ is antisymmetric if $\overrightarrow{s} \in O$ and $s$ is nondegenerate imply $\overleftarrow{s} \notin O$.

**Definition 2.4.7 (Consistent set of oriented separations).** A set $O \subseteq \overrightarrow{S}$ is consistent if there do not exist distinct $r,s \in S$ with orientations $\overrightarrow{r}$ and $\overrightarrow{s}$ such that $\overrightarrow{r} < \overrightarrow{s}$ and $\overleftarrow{r}, \overrightarrow{s} \in O$. Informally, $O$ is consistent if no two of its elements point away from each other.

**Definition 2.4.8 (Orientation of a set of separations).** An orientation of $S$ is a set $O \subseteq \overrightarrow{S}$ that contains exactly one orientation of every $s \in S$. Equivalently, for every $s \in S$, exactly one of $\overrightarrow{s}$ and $\overleftarrow{s}$ lies in $O$.

**Definition 2.4.9 (Partial orientation).** A partial orientation of $S$ is an orientation of some subset $U \subseteq S$. Equivalently, a partial orientation is an antisymmetric subset of $\overrightarrow{S}$.

**Proposition 2.4.10 (Consistent orientations contain trivial separations).** Every consistent orientation of $S$ contains all separations $\overrightarrow{r}$ that are trivial in $S$.

**Proof.** Let $O$ be a consistent orientation of $S$, and suppose $\overrightarrow{r}$ is trivial in $S$. Let $s \in S$ witness the triviality of $\overrightarrow{r}$. Then $\overrightarrow{r} < \overrightarrow{s}$ and $\overrightarrow{r} < \overleftarrow{s}$. Since $O$ is an orientation of $S$, it contains exactly one of $\overrightarrow{r}$ and $\overleftarrow{r}$. Suppose for contradiction that $\overleftarrow{r} \in O$. Since $O$ is an orientation, it contains either $\overrightarrow{s}$ or $\overleftarrow{s}$. If $\overrightarrow{s} \in O$, then $\overrightarrow{r} < \overrightarrow{s}$ and $\overleftarrow{r}, \overrightarrow{s} \in O$, contradicting consistency. If $\overleftarrow{s} \in O$, then $\overrightarrow{r} < \overleftarrow{s}$ and $\overleftarrow{r}, \overleftarrow{s} \in O$, again contradicting consistency. Therefore $\overleftarrow{r} \notin O$. Since $O$ orients $r$, it must contain $\overrightarrow{r}$. $\blacksquare$

**Proposition 2.4.11 (Extension of consistent partial orientations).** Every consistent partial orientation of $S$ containing no co-trivial separation $\overleftarrow{r} \in \overrightarrow{S}$ extends to a consistent orientation of all of $S$.

**Proof.** Deferred.

--- 

## 2.5 Stars Of Separations

**Definition 2.5.1 (Multistar Of Separations)**
A family $(\overrightarrow{s}_i | i \in I)$ of nondegenerate oriented separations such that $\forall i, j \in I (\overrightarrow{s}_i \le \overleftarrow{s}_j)$.

**Definition 2.5.2 (Stars)**
Multistars in which each element occurs only once. Stars considered as obvious sets rather than families, and multistar $(\overrightarrow{s}_i | i \in I)$ induces the star $\{\overrightarrow{s}_i | i \in I\}$ by "forgetting" multiplicity.

**Proposition 2.5.3.**
Multistars of separations are nested and consistent.

**Proof.**
Let $(\overrightarrow{s_i} \mid i \in I)$ be a multistar. First, we show that it is nested. Let $\overrightarrow{s_i}$ and $\overrightarrow{s_j}$ be two elements of the multistar. If $i = j$, then the two elements are comparable. If $i \ne j$, then by the multistar property, $\overrightarrow{s_i} \le \overleftarrow{s_j}$. Hence $s_i$ and $s_j$ have comparable orientations, so they are nested. Now we show that the multistar is consistent. Suppose for contradiction that it is not consistent. Then there exist distinct separations $r,s \in S$ such that $\overrightarrow{r} < \overrightarrow{s}$ and both $\overleftarrow{r}$ and $\overrightarrow{s}$ lie in the multistar. Since $\overleftarrow{r}$ and $\overrightarrow{s}$ are elements of the multistar, and since $r \ne s$, the multistar property gives $\overrightarrow{s} \le (\overleftarrow{r})^* = \overrightarrow{r}$. Therefore, $\overrightarrow{r} < \overrightarrow{s} \le \overrightarrow{r}$, which contradicts antisymmetry of the partial order. Hence the multistar is consistent. $\blacksquare$

**Proposition 2.5.4**
Let $\sigma$ be a multistar. If $\{\overrightarrow{s}, \overleftarrow{s}\} \subseteq \sigma$, then any other $\overrightarrow{r} \in \sigma$ will be trivial - witnessed by s.

**Definition 2.5.5 (Natural Partial Ordering)**
Given a tree T, its natural partial ordering on the set $\overrightarrow{E}(T) := \{(x, y) : \{x, y\} \in E(T)\}$ of its oriented edges defined by letting $(x, y) < (u, v)$ if $\{x, y\} \ne \{u, v\}$ and the unique $\{x, y\}-\{u, v\}$ path in T joins y to u.

**Definition 2.5.6 (Oriented Star)**
$\forall t \in V(T)$, the oriented star at t in T is given by $\overrightarrow{F}_t := \{(x, y) : xt \in E(T)\}$. This is a star in separation system $(\overrightarrow{E}(T), \le, * := (x, y) \to (y, x))$.

---

## 2.6 S-Trees

**Definition 2.6.1 (S-Tree)**
Let $(\overrightarrow{S}, \le, *)$ be a separation system. An S-Tree is a pair $(T, \alpha)$ of a tree T and function $\alpha : \overrightarrow{E}(T) \to \overrightarrow{S}$ that satisfies $\alpha(\overleftarrow{e}) = \alpha(\overrightarrow{e})*$. If T has an edge rooted at a leaf x, then its oriented edge emanating from x is given by $\overrightarrow{e}$.

**Definition 2.6.2 (Associated)**
Let $(\overrightarrow{S}, \le, *)$ be a separation system and $(T, \alpha)$ an S-Tree. For every $t \in V(T)$, $(\alpha(\overrightarrow{e}) | \overrightarrow{e} \in \overrightarrow{F_t})$ and $\alpha(\overrightarrow{F_t})$ in $\overrightarrow{S}$ are said to be associated with t in $(T, \alpha)$.

**Definition 2.6.3 (Over F)**
Let $(T, \alpha)$ be an S-Tree. If all $\alpha(\overrightarrow{F_t})$ associated with t in T are contained in set $F$, then $(T, \alpha)$ is an S-Tree over $F$. If the elements of $F$ are stars, then $(T, \alpha)$ is an S-Tree over stars.

**Definition 2.6.4 (Order-Respecting)**
Let $(T, \alpha)$ be an S-Tree. If $\forall \overrightarrow{e}, \overrightarrow{f} \in \overrightarrow{E}(T) (\overrightarrow{e} \le \overrightarrow{f} \implies \alpha(\overrightarrow{e}) \le \alpha(\overrightarrow{f}))$ then  $(T, \alpha)$ is called order-respecting.

**Proposition 2.6.5**
Order-respecting S-Trees are over stars but S-Trees over stars need not be order-respecting.

**Proof.**
$T_3$ example to be shown...

**Definition 2.6.6 (Redundant)**
Let $(T, \alpha)$ be an S-Tree. If $\exists t \in V(t)$ with distinct neighbors $t'$ and $t''$ such that $\alpha(t', t) = \alpha(t'', t)$, then the S-Tree is called redundant. Otherwise, the S-Tree is called irredundant.

**Lemma 2.1**
Every irredundant S-Tree $(T, \alpha)$ over stars is order-respecting. In particular, $\alpha(\overrightarrow{E}(T))$ is a nested set of separations in $\overrightarrow{S}$.

**Proof.**
As $(T, \alpha)$ is irredundant, our assumption that the sets $\alpha(\overrightarrow{F_t})$ are stars is tantamount to saying that the families $(\alpha(\overrightarrow{e}) | \overrightarrow{e} \in \overrightarrow{F_t})$ are multistars. In other words, the S-trees which $(T, \alpha)$ induces on its maximal stars, the subtrees consisting of a fixed node t and the neighbors of t, are order-respecting. As the relation $\le$ is transitive, this propogates through $\overrightarrow{E}(T)$ to make the entire $(T, \alpha)$ order-respecting. $\blacksquare$

**Personal Note**
Lemma 2.1 can be slightly weakened to,
Every S-Tree $(T, \alpha)$ over stars with families $(\alpha(\overrightarrow{e}) | \overrightarrow{e} \in \overrightarrow{F_t})$ that are multistars is order-respecting.

The S-Tree does not need global irredundancy, the maximal stars can be irredundant or if $\exists \overrightarrow{n} \in \overrightarrow{F_t} \exists \overrightarrow{m} \in \overrightarrow{F_t} (\overrightarrow{n} = \overrightarrow{m})$ then $\overrightarrow{n}$ is small.

**Proof.**
Similar to **Lemma 2.1**.

**Proposition 2.6.7**
Order-respecting S-trees over stars can be redundant.

**Proof.**
Follows immediately from the weakened lemma.

**Lemma 2.2**
Let $(T, \alpha)$ be an irredundant S-tree over a set $F$ of stars. Let $e, f$ be distinct edges of T with orientations $\overrightarrow{e} < \overrightarrow{f}$ such that $\alpha(\overrightarrow{e}) = \alpha(\overleftarrow{f}) =: \overrightarrow{r}$. Then $\overrightarrow{r}$ is trivial. In particular, $T$ cannot have distinct leaves associated with the same star $\{\overleftarrow{r}\}$ unless $\overrightarrow{r}$ is trivial. 

**Personal Proof.**
By Lemma 2.1, $(T,\alpha)$ is order-respecting. Let $\vec e=\vec g_0<\vec g_1<\cdots<\vec g_k=\vec f$ be the oriented edge sequence along the path from $\vec e$ to $\vec f$. First note that $k\ne 1$. Indeed, if $k=1$, then $e$ and $f$ are adjacent, so $\vec e$ and $\overleftarrow f$ are distinct incoming oriented edges at their common node. Since $\alpha(\vec e)=\vec r=\alpha(\overleftarrow f)$, this contradicts irredundancy. Hence $k\ge 2$. Set $a_i:=\alpha(\vec g_i)$. Since $(T,\alpha)$ is order-respecting, $a_0\le a_1\le\cdots\le a_k$. By hypothesis, $a_0=\alpha(\vec e)=\vec r$ and $\alpha(\overleftarrow f)=\vec r$. Since $\alpha$ commutes with involution, $a_k=\alpha(\vec f)=\overleftarrow r$. Thus $\vec r=a_0\le a_1\le\cdots\le a_k=\overleftarrow r$. We claim that there is some index $i$ with $1\le i<k$ such that $a_i\ne\vec r$. Suppose not. Then $a_i=\vec r$ for every $1\le i<k$, and in particular $a_{k-1}=\vec r$. But $\vec g_{k-1}$ and $\overleftarrow f$ are distinct incoming oriented edges at the node between $g_{k-1}$ and $f$, and $\alpha(\vec g_{k-1})=a_{k-1}=\vec r=\alpha(\overleftarrow f)$, contradicting irredundancy. Hence such an index exists. Let $i$ be the least index with $1\le i<k$ such that $a_i\ne\vec r$. Then $a_{i-1}=\vec r$, and since $a_{i-1}\le a_i$, we have $\vec r<a_i$. Also, $a_i\le a_k=\overleftarrow r$. Applying the order-reversing involution gives $a_i^*\ge \vec r$, so $\vec r\le a_i^*$. This inequality is strict. If $a_i^*=\vec r$, then $\alpha(\overleftarrow{g_i})=a_i^*=\vec r=\alpha(\vec g_{i-1})$. But $\vec g_{i-1}$ and $\overleftarrow{g_i}$ are distinct incoming oriented edges at their common node, contradicting irredundancy. Hence $\vec r<a_i^*$. Therefore $\vec r<a_i$ and $\vec r<a_i^*$. Thus the separation $s=\{a_i,a_i^*\}$ witnesses that $\vec r$ is trivial. $\blacksquare$

**Lemma 2.3**
If $(T, \alpha)$ is an S-tree over $F$, possibly redundant, then T has a subtree $T'$ such that $(T', \alpha')$ is an irredundant S-tree over $F$, where $\alpha'$ is the restriction of $\alpha$ to $\overrightarrow{E}(T')$. If $(T, \alpha)$ is rooted at a leaf x and $T$ has an edge, then $T'$ can be chosen so as to contain $x$ and $e_x$.

**Proposition 2.6.8**
An S-tree $(T, \alpha)$ over a set $F$ of stars can be contracted to an S-tree $(T', \alpha ')$ over the subset $F' \subseteq F$ of its antisymmetric stars.

**Proof.**
TO DO

**Definition 2.6.9 (Tight S-tree)**
S-tree $(T, \alpha)$ is tight if all sets $\alpha(\overrightarrow{F_t})$ for $t \in T$ are antisymmetric.

**Lemma 2.4**
Let $(T, \alpha)$ be an S-tree over a set of F of stars, rooted at a leaf x. Assume that T has an edge, and that $\overrightarrow{r} = \alpha(\overrightarrow{e_x})$ is nontrivial. Then T has a minor $T'$ containing x and $e_x$ such that $(T', \alpha')$, where $\alpha' = \alpha | \overrightarrow{E}(T')$, is a tight and irredundant S-tree over $F$. For every such $(T', \alpha ')$ the edge $\overrightarrow{e_x}$ is the only edge $\overrightarrow{e} \in \overrightarrow{E}(T')$ with $\alpha(\overrightarrow{e}) = \overrightarrow{r}$.

**Proof.**
TO DO

---

## 3.1 Weak Duality

**Definition 3.1.1 (Avoids)**
Partial orientation P of separations S avoids $F \subseteq 2^{\overrightarrow{S}}$ if $2^P \cap F = \emptyset$.

**Lemma 3.2**
Let $(\overrightarrow{S}, \le, *)$ be a separation system and $F \subseteq 2^{\overrightarrow{S}}$. If there exists an S-tree over F, then no orientation of S avoids F.

**Proof.**
Let $(T, \alpha)$ be an S-tree over F, and let O be an orientation of S. Let $t \in V(T)$ be a sink in the orientation of the edges of T that O induces via $\alpha$. Then $\alpha(\overrightarrow{F_t}) \subseteq O$. Since $\alpha(\overrightarrow{F_t}) \in F$, as $(T, \alpha)$ is an S-tree over F, this means that O does not avoid F. $\blacksquare$

**Theorem 3.1 (Weak Duality)**
Let $(\overrightarrow{S}, \le, *)$ be a finite separation system and $F \subseteq 2^{\overrightarrow{S}}$ a set of stars. Then exactly one of the following assertions holds:
1. There exists an S-tree over F.
2. There exists an orientation of S that avoids F.

**Proof.**

- Strong duality, shifting for merging S-tree stuck because concrete branchwidth motivates
- Notice simalarity to what Diestel considers essential tangles in the merge and essential tangles in practical algorithm for branch-decompositions
