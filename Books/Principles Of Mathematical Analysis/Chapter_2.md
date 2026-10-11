# Chapter 2: Basic Topology

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 2.1 Basic Topology

---

### Key Concepts

- **Integer Notation**: For positive integer $n$, let $J_n = \{1, 2, ..., n\}$ and $J = \mathbb{Z}^+$.

### Definitions

- **Image**: Let $f : X \to Y$ and $E \subseteq X$. The the image of $E$ under $f$ is $\{f(x) | x \in E\}$.
- **Onto**: Let $f : X \to Y$. $f$ is onto if $f(X) = Y$.
- **Inverse Image**: Let $f : X \to Y$ and $E \subseteq Y$. $f^{-1}(E)$ denotes the inverse image of $E$, $\{x \in X | f(x) \in E\}$.
- **One-to-One**: $f : X \to Y$ is called one-to-one if for each $y \in Y$, $f^{-1}(y)$ consists of at most one element of $X$.
- **Correspondence (Equivalent)**: If there is a 1-1 onto mapping from $A$ to $B$, they are said to be in a 1-1 correspondence and equivalence is denoted $A \sim B$. This is an equivalence relation.
- **Finite**: $A$ is finite if $A \sim J_m$, including the empty set.
- **Infinite**: $A$ is infinite if it is not finite.
- **Countable (enumerable)**: $A$ is countable if $A \sim J$.
- **Uncountable**: $A$ is uncountable if it is not finite nor countable.
- **Most Countable**: $A$ is at most countable if $A$ is finite or countable.
- **Sequence**: Function $f$ defined on $J$. If $f(n) = x_n$, then the sequence is denoted by $\{x_n\}$ or $x_1, x_2, ...$. Values of $f$ are its terms. If all terms of $f$ are contained in set $A$, then $f$ is called a sequence in $A$.
- **Metric Space**: Set $X$, whose elements are called points, if there is a metric associated with any two points of $X$. Subsets are also metric spaces, considering the metric.
- **Metric**: Function $d : X \times X \to R$ for set $X$ such that for $p, q \in X$:
	- $d(p, q) > 0$ if $p \ne q$; $d(p, p) = 0$;
	- $d(p, q) = d(q, p)$;
	- $d(p, q) \le d(p, r) + d(r, q)$ for any $r \in X$.
- **Segment**: $(a, b) = \{x \in R | a < x < b\}$.
- **Interval**: $[a, b] = \{x \in R | a \le x \le b\}$. Half-open intervals denoted $[a, b) = \{x \in R | a \le x < b\}$ and $(a, b] = \{x \in R | a < x \le b\}$.
- **K-Cell**: Set of points $(x_1, x_2, ..., x_k) \in R^k$ and $a_i < b_i$ for $i = 1, ..., k$ such that $a_i \le x_i \le b_i$.
- **Open Ball**: For $x \in R^k$ and $r > 0$ is the set of $y \in R^k$ such that $|y - x| < r$.
- **Closed Ball**: For $x \in R^k$ and $r > 0$ is the set of $y \in R^k$ such that $|y - x| \le r$.
- **Convex**: Set $E \subseteq R^k$ such that $\lambda x + (1 - \lambda)y \in E$ when $x \in E$, $y \in E$, and $0 < \lambda < 1$.
- **Neighborhood**: Denoted $N_r(p)$ for point $p$ of metric space $X$, is the set of all points $q$ such that $d(p, q) < r$ for some $r > 0$. $r$ is called the radius.
- **Limit Point**: $p$ is a limit point of a $E \subseteq X$ for metric space $X$ if every neighborhood of $p$ contains a point $q \ne p$ such that $q \in E$.
- **Isolated Point**: For $E \subseteq X$ where $X$ is a metric space, $p \in E$ is an isolated point if $p$ is not a limit point of $E$.
- **Closed**: $E \subseteq X$ for metric space $X$ such that every limit point of $E$ is a point of $E$.
- **Interior Point**: Point $p$ is an interior point of $E \subseteq X$ for metric space $X$ if there is a neighborhood $N$ of $p$ such that $N \subseteq E$.
- **Open**: $E \subseteq X$ for metric space $X$ where every point of $E$ is an interior point of $E$.
- **Complement**: For $E \subseteq X$ where $X$ is a metric space, its complement $E^c$ contains all points $p \in X$ such that $p \not \in E$.
- **Perfect**: For $E \subseteq X$ where $X$ is a metric space, $E$ is closed and every point of $E$ is a limit point of $E$.
- **Bounded**: For $E \subseteq X$ where $X$ is a metric space, there is a real number $M$ and a point $q \in X$ such that $d(p, q) < M$ for all $p \in E$.
- **Dense**: For $E \subseteq X$ where $X$ is a metric space, $E$ is dense in $X$ if every point of $X$ is a limit point of $E$ or a point of $E$.
- **Closure**: For metric space $X$, $E \subseteq X$, and $E'$ denoting the set of limit points of $E$, the closure of $E$ is $\overline{E} = E \cup E'$.
- **Open Cover**: For $E \subseteq X$ where $X$ is a metric space, a collection of open subsets $\{G_\alpha\}$ of $X$ is an open cover of $E$ if $E \subseteq \bigcup_\alpha G_\alpha$.
- **Compact**: $K \subseteq X$ for metric space $X$ is called compact if every open cover of $K$ contains a finite subcover.
- **Cantor Set**: Let $E_0 = [0,1]$ and then for $E_n$, we have $E_{n+1}$ with removal of middle third segments. The set $\bigcap_{n=1}^\infty E_n$ is the Cantor set which is clearly compact and nonempty. Does not intersect segments of the form $(\frac{3k + 1}{3^m}, \frac{3k + 2}{3^m})$.
- **Separated**: $A, B \subseteq X$ for metrix space $X$ are said to be separated if $A \cap \overline{B} = \overline{A} \cap B = \emptyset$.
- **Connected**: $E \subseteq X$ for metric space $X$ is connected if it is not the union of two nonempty separating sets.

### Examples

**Basic Example**
The metric of $R^k$. Let $x, y \in R^k$. Then
> $d(x, y) = |x - y|$.

### Results & Proofs

**Theorem: Subset Countability**
Every infinite subset of a countable set $A$ is countable.

**Theorem: Countable Union Of Countable Sets**
Let $\{E_n\}, n = 1, 2, ...$ be a sequence of countable sets, and put $S = \bigcup_{n=1}^\infty E_n$. Then $S$ is countable.

**Corollary: Union of At Most Countable**
Suppose $A$ is at most countable, and, for every $\alpha \in A$, $B_\alpha$ is at most countable. Put $T = \bigcup_{\alpha \in A}B_\alpha$. Then $T$ is at most countable.

**Theorem: n-Tuples Countable**
Let $A$ be a countable set, and let $B_n$ be the set of all n-tuples $(a_1, ..., a_n)$, where $a_k \in A$, and the elements $a_1, ..., a_n$ need not be distinct. Then $B_n$ is countable.

**Corollary: Rational Numbers**
The set of all rational numbers is countable.

**Theorem: Uncountable Set**
Let $A$ be the set of all sequences whose elements are the digits $0$ and $1$. This set $A$ is uncountable. 

**Theorem: Open Neighborhoods**
Every neighborhood is an open set.

**Theorem: Limit Points Related To Infinity**
If $p$ is a limit point of a set $E$, then every neighborhood of $p$ contains infinitely many points of $E$.

**Corollary: Finite Point Sets**
A finite point set has no limit points.

**Theorem: De Morgan's Law**
Let $\{E_\alpha\}$ be a collection of sets $E_\alpha$. Then $(\bigcup_\alpha E_\alpha)^c = \bigcap_\alpha (E_\alpha^c)$.

**Theorem: Open And Closed Complements**
A set $E$ is open iff its complement is closed.

**Corollary: Open And Closed Complements Extended**
A set $F$ is closed iff its complement is open.

**Theorem: Union And Intersection Of Open Or Closed Sets**
a) For any collection $\{G_\alpha\}$ of open sets, $\bigcup_\alpha G_\alpha$ is open.
b) For any collection $\{F_\alpha\}$ of closed sets, $\bigcap_\alpha F_\alpha$ is closed.
c) For any finite collection $G_1, ..., G_n$ of open sets, $\bigcap_{i=1}^n G_i$ is open.
d) For any finite collection $F_1, ..., F_n$ of closed sets, $\bigcup_{i=1}^n F_i$ is closed.

**Theorem: Closure Properties**
Let $X$ be a metric space with $E \subseteq X$, then:
a) $\overline{E}$ is closed;
b) $E = \overline{E}$ iff $E$ is closed;
c) $\overline{E} \subseteq F$ for every closed set $F \subseteq X$ such that $E \subseteq F$.

**Theorem: Closure Upper Bound**
Let $E$ be a nonempty set of real numbers which is bounded above. Let $y = \sup E$. Then $y \in \overline{E}$. Hence $y \in E$ if $E$ is closed.

**Theorem: Open Relative**
Suppose $Y \subseteq X$. A subset $E$ of $Y$ is open relative to $Y$ iff $E = Y \cap G$ for some open subset $G$ of $X$.

**Theorem: Compact Relative**
Suppose $K \subseteq Y \subseteq X$. Then $K$ is compact relative to $X$ iff $K$ is compact relative to $Y$.

**Theorem: Compact Subsets**
Compact subsets of metric spaces are closed.

**Theorem: Compact Under Subsets**
Closed subsets of compact sets are compact.

**Corollary: Compact Intersection**
If $F$ is closed and $K$ is compact, then $F \cap K$ is compact.

**Theorem: Intersection Of Compact Spaces**
If $\{K_\alpha\}$ is a collection of compact subsets of a metric space $X$ such that the intersection of every finite subcollection of $\{K_\alpha\}$ is nonempty, then $\bigcap K_\alpha$ is nonempty.

**Corollary: Intersection Of Compact Space Sequence**
If $\{K_n\}$ is a sequence of nonempty compact sets such that $K_{n+1} \subseteq K_n$, then $\bigcap_{n=1}^\infty K_n$ is not empty.

**Theorem: Infinite Subset Of Compact**
If $E$ is an infinite subset of a compact set $K$, then $E$ has a limit point in $K$.

**Theorem: Sequence Of Intervals**
If $\{I_n\}$ is a sequence of intervals in $R^1$, such that $I_{n+1} \subseteq I_n$, then $\bigcap_1^\infty I_n$ is not empty.

**Theorem: Sequence Of K-Cells**
Let $k$ be a positive integer. If $\{I_n\}$ is a sequence of k-cells such that $I_{n+1} \subseteq I_n$, then $\bigcap_1^\infty I_n$ is not empty.

**Theorem: K-Cells Are Compact**
Every k-cell is compact.

**Theorem: Heine-Borel Theorem**
If a set $E$ in $R^k$ has one of the following three properties, then it has the other two:
a) $E$ is closed and bounded.
b) $E$ is compact.
c) Every infinite subset of $E$ has a limit point in $E$.

**Theorem: Weierstrass**
Every bounded infinite subset of $R^k$ has a limit point in $R^k$.

**Theorem: Uncountable Perfect Sets**
Let $P$ be a nonempty perfect set in $R^k$. Then $P$ is uncountable.

**Corollary: Uncountable Intervals**
Every interval $[a, b]$ is uncountable. In particular, the set of all real numbers is uncountable.

**Theorem: Connected Real Subsets**
A subset $E$ of the real line is connected iff $x, y \in E$ and $x < z < y$, then $z \in E$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
