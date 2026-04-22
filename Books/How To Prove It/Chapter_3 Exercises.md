$$
\require{unicode}
\newcommand{\proofend}{\Large\unicode{x263B}}
$$
## 3.0 Ordered Pairs And Cartesian Products

**Problem 1**
What are the truth sets of the following statements? List a few elements of each truth set.
a) "x is a parent of y", where x and y range over the set P of all people.
b) "There is someone who lives in x and attends y", where x ranges over the set C of all cities and y ranges over the set U of all universities.
**Solution**
a)
The truth set is $\{(x, y) \in P \times P : \text{x is a parent of y}\}$. A few elements are $(Anita, Anthony), (Julius, Alan), (Paul, Leonhard)$.

b)
The truth set is $\{(x, y) \in C \times U : \text{There is someone who lives in x and attends y}\}$. A few elements are $(Houston, Rice University), (Boston, MIT), (New Jersey, Princeton)$.
$\proofend$

**Problem 2**
What are the truth sets of the following statements? List a few elements of each truth set.
a) "x lives in y", where x ranges over the set P of all people and y ranges over the set C of all cities.
b) "The population of x is y", where x ranges over the set C of all cities and y ranges over $\mathbb{N}$.
**Solution**
a)
The truth set is $\{(x, y)  \in P \times C: \text{x lives in y}\}$. A few elements are $(Bob, Chicago), (Hilton, Houston), (Alice, Miami)$.

b)
The truth set is $\{(x, y) \in C \times \mathbb{N} : \text{x has population y}\}$. A few elements are $(Houston, 2390000), (Miami, 500000), (Chicago, 2750000)$.
$\proofend$

**Problem 3**
The truth sets of the following statements are subsets of $\mathbb{R}^2$. List a few elements of each truth set. Draw a picture showing all the points in the plane whose coordinates are in the truth set.
a) $y = x^2 - x - 2$.
b) $y < x$.
c) Either $y = x^2 - x - 2$ or $y = 3x - 2$.
d) $y < x$, and either $y = x^2 - x - 2$ or $y = 3x - 2$.
**Solution**
a)
A few points are $(1, -2), (2, 0), (3, 4)$.
![[graph1.png]]

b)
A few points are $(0, -1), (0, -2), (0, -3)$.
![[graph2.png]]

c)
A few points are $(1, -2), (2, 0), (3, 4)$.
![[graph3.png]]

d)
A few points are $(2, 0), (0, -2), (1, -2)$.
![[graph4.png]]

$\proofend$

**Problem 4**
Let $A = \{1, 2, 3\}$, $B = \{1, 4\}$, $C = \{3, 4\}$, and $D = \{5\}$. Compute all the sets mentioned in Theorem 4.1.3 and verify that all parts of the theorem are true.
**Solution**
We do this systematically:
1)
$$
A \times (B \cap C) = \{1, 2, 3\} \times \{4\} = \{(1, 4), (2, 4), (3, 4)\}
$$
$$
(A \times B) \cap (A \times C)
$$
$$
= \{(1, 1), (2, 1), (3, 1), (1, 4), (2, 4), (3, 4)\} \cap \{(1, 3), (2, 3), (3, 3), (1, 4), (2, 4), (3, 4)\}
$$
$$
= \{(1, 4), (2, 4), (3, 4)\}
$$
Equal.

2)
$$
A \times (B \cup C) = \{1, 2, 3\} \times \{1, 3, 4\}
$$
$$
(A \times B) \cup (A \times C)
$$
$$
= \{(1, 1), (2, 1), (3, 1), (1, 4), (2, 4), (3, 4)\} \cup \{(1, 3), (2, 3), (3, 3), (1, 4), (2, 4), (3, 4)\}
$$
Equal.

3)
$$
(A \times B) \cap (C \times D)
$$
$$
= \{(1, 1), (2, 1), (3, 1), (1, 4), (2, 4), (3, 4)\} \cap \{(3, 5), (4, 5)\} = \emptyset
$$
$$
(A \cap C) \times (B \cap D) = \{3\} \times \emptyset = \emptyset
$$
Equal.

4)
$$
(A \times B) \cup (C \times D) = \{(1, 1), (2, 1), (3, 1), (1, 4), (2, 4), (3, 4)\} \cup \{(3, 5), (4, 5)\}
$$
$$
= \{(1, 1), (2, 1), (3, 1), (1, 4), (2, 4), (3, 4), (3, 5), (4, 5)\}
$$
$$
(A \cup C) \times (B \cup D) = \{1, 2, 3, 4\} \times \{3, 4, 5\}
$$
$(A \times B) \cup (C \times D) \subseteq (A \cup C) \times (B \cup D)$.

5)
$$
A \times \emptyset = \{1, 2, 3\} \times \{\} = \{\}
$$
$$
\emptyset \times A = \{\} \times \{1, 2, 3\} = \{\}
$$
Equal.
$\proofend$

**Problem 5**
Prove parts 2 and 3 of Theorem 4.1.3.
**Solution**
Let $(x, y) \in A \times (B \cup C)$ be arbitrary. Then $x \in A$ and $y \in B$ or $y \in C$. If $y \in B$, we see that $(x, y) \in A \times B$ and so in particular $(x, y) \in (A \times B) \cup (A \times C)$. If $y \in C$, we see that $(x, y) \in A \times C$ and so in particular $(x, y) \in (A \times B) \cup (A \times C)$. Therefore, because $(x, y)$ was arbitrary, $A \times (B \cup C) \subseteq (A \times B) \cup (A \times C)$. Let $(a, b) \in (A \times B) \cup (A \times C)$ be arbitrary. Then $(a, b) \in A \times B$ or $(a, b) \in A \times C$. If $(a, b) \in A \times B$ then $a \in A$ and $b \in B \subseteq B \cup C$. It follows that $(a, b) \in A \times (B \cup C)$. If $(a, b) \in A \times C$ then $a \in A$ and $b \in C \subseteq B \cup C$. It follows that $(a, b) \in A \times (B \cup C)$. Thus, because $(a, b)$ was arbitrary, $(A \times B) \cup (A \times C) \subseteq A \times (B \cup C)$. Finally, $A \times (B \cup C) = (A \times B) \cup (A \times C)$ as desired.

Let $(x, y) \in (A \times B) \cap (C \times D)$ be arbitrary. By definition of $(x, y) \in A \times B$ and $(x, y) \in C \times D$, we see that $x \in A$, $x \in C$, $y \in B$, and $y \in D$. Then $x \in A \cap C$ and $y \in B \cap D$. it follows that $(x, y) \in (A \cap C) \times (B \cap D)$. Therefore, $(A \times B) \cap (C \times D) \subseteq (A \cap C) \times (B \cap D)$. Let $(a, b) \in (A \cap C) \times (B \cap D)$. By definition, $a \in A \cap C$ and $b \in B \cap D$. Then $a \in A$, $a \in C$, $b \in B$, and $b \in D$. So $(a, b) \in A \times B$ and $(a, b) \in C \times D$. Finally, $(a, b) \in (A \times B) \cap (C \times D)$. Therefore, $(A \cap C) \times (B \cap D) \subseteq (A \times B) \cap (C \times D)$. We get $(A \times B) \cap (C \times D) = (A \cap C) \times (B \cap D)$ as desired.
$\proofend$

**Problem 6**
What is wrong with the following proof that for any sets A, B, C, and D, $(A \cup C) \times (B \cup D) \subseteq (A \times B) \cup (C \times D)$? Proof: Suppose $(x, y) \in (A \cup C) \times (B \cup D)$. Then $x \in A \cup C$ and $y \in B \cup D$, so either $x \in A$ or $x \in C$, and either $y \in B$ or $y \in D$. We consider these cases separately. Case 1. $x \in A$ and $y \in B$. Then $(x, y) \in A \times B$. Case 2. $x \in C$ and $y \in D$. Then $(x, y) \in C \times D$. Thus, either $(x, y) \in A \times B$ or $(x, y) \in C \times D$, so $(x, y) \in (A \times B) \cup (C \times D)$.
**Solution**
The cases are not exhaustive. The proof fails to check case 3, $x \in A$ and $y \in D$, and case 4, $x \in C$ and $y \in B$.
$\proofend$

**Problem 7**
If A has m elements and B has n elements, how many elements does $A \times B$ have?
**Solution**
$A \times B$ has $m \cdot n$ elements. Consider $a \in A$. By definition of $A \times B$, $(a, b) \in A \times B$ for each $b \in B$. There are n such $b's$. Therefore, each $a \in A$ is the first coordinate in n distinct tuples of $A \times B$. But there are m distinct $a's$ of A. Then there are m possible tuples with distinct 1st coordinates, and each n distinct 2nd coordinates for each m-th tuple.
$\proofend$

**Problem 8**
Is it true that for any sets A, B, and C, $A \times (B \backslash C) = (A \times B) \backslash (A \times C)$?
**Solution**
Yes. Let $(x, y) \in A \times (B \backslash C)$. By definition, $x \in A$ and $y \in B \backslash C$, implying $y \in B$ and $y \not \in C$. Then $(x, y) \in A \times B$ and $(x, y) \not \in A \times C$. So $(x, y) \in (A \times B) \backslash (A \times C)$, meaning $A \times (B \backslash C) \subseteq (A \times B) \backslash (A \times C)$. Let $(a, b) \in (A \times B) \backslash (A \times C)$. By definition, $(a, b) \in A \times B$ and $(a, b) \not \in A \times C$. Then $a \in A$, $b \in B$, and $a \not \in A \lor b \not \in C$. Since $a \in A$ and $a \not \in A \lor b \not \in C$, we see that $b \not \in C$. It follows that $b \in B \backslash C$. Therefore, $(a, b) \in A \times (B \backslash C)$. Finally, $(A \times B) \backslash (A \times C) \subseteq A \times (B \backslash C)$. Thus, $A \times (B \backslash C) = (A \times B) \backslash (A \times C)$.
$\proofend$

**Problem 9**
Prove that for any sets A, B, and C, $A \times (B \Delta C) = (A \times B) \Delta (A \times C)$.
**Solution**
Suppose $(x, y) \in A \times (B \Delta C)$. By definition, $x \in A$ and $y \in B \Delta C$, meaning $y \in B \backslash C$ or $y \in C \backslash B$. Case 1: $y \in B \backslash C$. It follows that $(x, y) \in A \times B$ and $(x, y) \not \in (A \times C)$. Therefore, $(x, y) \in (A \times B) \Delta (A \times C)$. Case 2: $y \in C \backslash B$. It follows that $(x, y) \in A \times C$ and $(x, y) \not \in A \times B$. Therefore, $(x, y) \in (A \times B) \Delta (A \times C)$. In both cases, $A \times (B \Delta C) \subseteq (A \times B) \Delta (A \times C)$. Suppose $(a, b) \in (A \times B) \Delta (A \times C)$. Then $(a, b) \in A \times B$ and $(a, b) \not \in A \times C$ or $(a, b) \in (A \times C)$ and $(a, b) \not \in A \times B$. Case 1: $(a, b) \in A \times B$ and $(a, b) \not \in A \times C$. It follows that $a \in A$, $b \in B$, and $a \not \in A \lor b \not \in C$. Clearly, it must be that $b \not \in C$. So $b \in B \backslash C \subseteq B \Delta C$. Therefore, $(a, b) \in A \times (B \Delta C)$. Case 2: $(a, b) \in (A \times C)$ and $(a, b) \not \in A \times B$. Then $a \in A$, $b \in C$, and $a \not \in A \lor b \not \in B$. Clearly, it must be that $b \not \in B$. But then $b \in C \backslash B \subseteq B \Delta C$. So $(a, b) \in A \times (B \Delta C)$. In all cases, $(a, b) \in A \times (B \Delta C)$. Thus, $(A \times B) \Delta (A \times C) \subseteq A \times (B \Delta C)$ meaning $A \times (B \Delta C) = (A \times B) \Delta (A \times C)$.
$\proofend$

**Problem 10**
Prove that for any sets A, B, C, and D, $(A \backslash C) \times (B \backslash D) \subseteq (A \times B) \backslash (C \times D)$.
**Solution**
Let $(x, y) \in (A \backslash C) \times (B \backslash D)$. By definition, $x \in A \backslash C$ and $y \in B \backslash D$. Then $(x, y) \in A \times B$ and $(x, y) \not \in C \times D$. Therefore, $(x, y) \in (A \times B) \backslash (C \times D)$. Finally, because $(x, y)$ was arbitrary, $(A \backslash C) \times (B \backslash D) \subseteq (A \times B) \backslash (C \times D)$.
$\proofend$

**Problem 11**
Prove that for any sets A, B, C, and D, $(A \times B) \backslash (C \times D) = [A \times (B \backslash D)] \cup [(A \backslash C) \times B]$.
**Solution**
Suppose $(x, y) \in (A \times B) \backslash (C \times D)$. By definition, $(x, y) \in A \times B$ and $(x, y) \not \in (C \times D)$. Then $x \in A$, $y \in B$, and $x \not \in C \lor y \not \in D$. Case 1: $x \not \in C$. It follows that $x \in A \backslash C$ and so $(x, y) \in (A \backslash C) \times B \subseteq [A \times (B \backslash D)] \cup [(A \backslash C) \times B]$. Case 2: $y \not \in D$. It follows that $y \in B \backslash D$, and so $(x, y) \in A \times (B \backslash D) \subseteq [A \times (B \backslash D)] \cup [(A \backslash C) \times B]$. We can conclude $(A \times B) \backslash (C \times D) \subseteq [A \times (B \backslash D)] \cup [(A \backslash C) \times B]$. Suppose $(x, y) \in [A \times (B \backslash D)] \cup [(A \backslash C) \times B]$.  Case 1: $(x, y) \in A \times (B \backslash D)$. Then $(x, y) \in A \times B$ and $(x, y) \not \in  C \times D$ since $y \not \in D$. Therefore, $(x, y) \in (A \times B) \backslash (C \times D)$. Case 2: $(x, y) \in (A \backslash C) \times B$. Then $(x, y) \in A \times B$ and $(x, y) \not \in C \times D$ since $x \not \in C$. Therefore, $(x, y) \in (A \times B) \backslash (C \times D)$. So we see that $[A \times (B \backslash D)] \cup [(A \backslash C) \times B] \subseteq (A \times B) \backslash (C \times D)$. Thus, $(A \times B) \backslash (C \times D) = [A \times (B \backslash D)] \cup [(A \backslash C) \times B]$.
$\proofend$

**Problem 12**
Prove that for any sets A, B, C, and D, if $A \times B$ and $C \times D$ are disjoint, then either A and C are disjoint or B and D are disjoint.
**Solution**
Suppose A and C are not disjoint, and B and D are not disjoint. Then there is some $x \in A \cap C$ and some $y \in B \cap D$. It follows that $(x, y) \in A \times B$ and $(x, y) \in C \times D$. So $(x, y) \in (A \times B) \cap (C \times D)$ meaning $(A \times B)$ is not disjoint from $(C \times D)$ as desired.
$\proofend$

**Problem 13**
Suppose $I \ne \emptyset$. Prove that for any indexed family of sets $\{A_i | i \in I\}$ and any set $B$, $(\bigcap_{i \in I} A_i) \times B = \bigcap_{i \in I}(A_i \times B)$. Where in the proof does the assumption that $I \ne \emptyset$ get used?
**Solution**
$I \ne \emptyset$ is by definition, an existential statement. When assuming $(x, y) \in (\bigcap_{i \in I} A_i) \times B$ or $(x, y) \in \bigcap_{i \in I}(A_i \times B)$, we claim there is a $z \in I$ such that $x \in A_z$. If $I$ is empty, there is no such z. Therefore, it is assumed $I \ne \emptyset$. Notice that the statement is vacuously true when $I = \emptyset$.
$\proofend$

**Problem 14**
Suppose $\{A_i | i \in I\}$ and $\{B_i | i \in I\}$ are indexed families of sets.
a) Prove that $\bigcup_{i \in I}(A_i \times B_i) \subseteq (\bigcup_{i \in I}A_i) \times (\bigcup_{i \in I}B_i)$.
b) For each $(i, j) \in I \times I$ let $C_{(i, j)} = A_i \times B_j$, and let $P = I \times I$. Prove that $\bigcup_{p \in P}C_p = (\bigcup_{i \in I} A_i) \times (\bigcup_{i \in I} B_i)$.
**Solution**
a)
Suppose $(x, y) \in \bigcup_{i \in I}(A_i \times B_i)$. Then there is some $a \in I$ such that $(x, y) \in A_a \times B_a$. Therefore, $x \in A_a$ and $y \in B_a$, implying that $x \in \bigcup_{i \in I}A_i$ and $y \in \bigcup_{i \in I}B_i$. By definition, $(x, y) \in (\bigcup_{i \in I}A_i) \times (\bigcup_{i \in I}B_i)$. Thus, $\bigcup_{i \in I}(A_i \times B_i) \subseteq (\bigcup_{i \in I}A_i) \times (\bigcup_{i \in I}B_i)$ as desired.

b)
Let $(x, y) \in \bigcup_{p \in P}C_p$, so that $(x, y) \in C_{(u, v)}$ for some $(u, v) \in P$. Then $x \in A_u$ and $y \in B_v$, meaning $x \in \bigcup_{i \in I}A_i$ and $y \in \bigcup_{i \in I}B_i$. Therefore, $(x, y) \in (\bigcup_{i \in I} A_i) \times (\bigcup_{i \in I} B_i)$. We can conclude $\bigcup_{p \in P}C_p \subseteq (\bigcup_{i \in I} A_i) \times (\bigcup_{i \in I} B_i)$. Suppose $(r, t) \in (\bigcup_{i \in I} A_i) \times (\bigcup_{i \in I} B_i)$. Then $r \in \bigcup_{i \in I}A_i$ and $t \in \bigcup_{i \in I}B_i$, meaning $r \in A_a$ and $t \in B_b$ for some $a, b \in I$. By definition, $(r, t) \in C_{(a, b)}$. It follows that $(r, t) \in \bigcup_{p \in P}C_p$. Therefore, $(\bigcup_{i \in I} A_i) \times (\bigcup_{i \in I} B_i) \subseteq \bigcup_{p \in P}C_p$. We can conclude that $\bigcup_{p \in P}C_p = (\bigcup_{i \in I} A_i) \times (\bigcup_{i \in I} B_i)$.
$\proofend$

**Problem 15**
Consider the following putative theorem. Theorem? For any sets A, B, C, and D, if $A \times B \subseteq C \times D$ then $A \subseteq C$ and $B \subseteq D$. Is the following proof correct? If so, what strategies are used? If not, can it be fixed? Is the theorem correct? Proof: Suppose $A \times B \subseteq C \times D$. Let a be an arbitrary element of A and let b be an arbitrary element of B. Then $(a, b) \in A \times B$, so since $A \times B \subseteq C \times D$, $(a, b) \in C \times D$. Therefore, $a \in C$ and $b \in D$. Since a and b were arbitrary elements of A and B, respectively, this shows that $A \subseteq C$ and $B \subseteq D$.
**Solution**
This proof is correct. It commonly uses implication proof strategies throughout and universal instantiation. Hence, the theorem is correct.
$\proofend$

## 3.1 Relations

**Problem 1**
Find the domains and ranges of the following relations.
a) $\{(p, q) \in P \times P : \text{the person p is a parent of the person q}\}$, where P is the set of all living people.
b) $\{(x, y) \in \mathbb{R}^2 : y > x^2\}$.
**Solution**
a)
Domain -
$\{p \in P : \exists q \in P (\text{the person p is a parent of the person q})\}$.
Range -
$\{q \in P : \exists p \in P (\text{the person p is a parent of the person q})\}$.

b)
Domain -
$\{x \in \mathbb{R} : \exists y \in \mathbb{R} (y > x^2)\}$.
Range - 
$\{y \in \mathbb{R} : \exists x \in \mathbb{R} (y > x^2)\}$.
$\proofend$

**Problem 2**
Find the domains and ranges of the following relations.
a) $\{(p, q) \in P \times P : \text{the person p is a brother of the person q}\}$, where P is the set of all living people.
b) $\{(x, y) \in \mathbb{R}^2 : y^2 = 1 - \frac{2}{(x^2 + 1)}\}$.
**Solution**
a)
Domain -
$\{p \in P : \exists q \in P (\text{the person p is a brother of the person q})\}$.
Range -
$\{q \in P : \exists p \in P (\text{the person p is a brother of the person q})\}$.

b)
Domain -
$\{x \in \mathbb{R} : \exists y \in \mathbb{R} (y^2 = 1 - \frac{2}{(x^2 + 1)})\}$.
Range -
$\{y \in \mathbb{R} : \exists x \in \mathbb{R} (y^2 = 1 - \frac{2}{(x^2 + 1)})\}$.
$\proofend$

**Problem 3**
Let L and E be the relations defined by $L := \{(s, r) \in S \times R : \text{the student s lives in the dorm room r}\}$ and $E := \{(s, c) \in S \times C : \text{the student s is enrolled in the course c})\}$ where S is the set of all students at your school, R is the set of all dorm rooms, and C is the set of all courses.
Describe the following relations.
a) $L^{-1} \circ L$.
b) $E \circ (L^{-1} \circ L)$.
**Solution**
a)
$\{(x, y) \in S \times S : \exists r \in R (\text{students x and y both live in the dorm room r})\}$.
b)
$\{(a, b) \in S \times C : \exists s \in S (\text{students s and a live in the same dorm room, and s is enrolled in course b})\}$.
$\proofend$

**Problem 4**
Let E and C be defined as in problem 3. Also, define $T := \{(c, p) \in C \times P : \text{the course c is taught by the professor p}\}$, $D := \{Monday, Tuesday, Wednesday, Thursday, Friday\}$, and $M := \{(c, d) \in C \times D : \text{the course c meets on the day d}\}$. Describe the following relations:
a) $M \circ E$.
b) $M \circ T^{-1}$.
**Solution**
a)
$\{(x, y) \in S \times D : \exists c \in C (\text{the student x is enrolled in the course c} \land \text{the course c meets on the day y})\}$.

b)
$\{(x, y) \in P \times D : \exists c \in C (\text{the course c is taught by professor x} \land \text{the course c meets on day y})\}$.
$\proofend$

**Problem 5**
Suppose that $A = \{1, 2, 3\}$, $B = \{4, 5, 6\}$, $R = \{(1, 4), (1, 5), (2, 5), (3, 6)\}$, and $S = \{(4, 5), (4, 6), (5, 4), (6, 6)\}$. Note that R is a relation from A to B and S is a relation from B to B. Find the following relations:
a) $S \circ R$.
b) $S \circ S^{-1}$.
**Solution**
a)
$$
\{(x, y) \in A \times B : \exists b \in B ((x, b) \in R \land (b, y) \in S)\}
$$
$$
= \{(1, 5), (1, 6), (1, 4), (2, 4), (3, 6)\}
$$

b)
$$
\{(x, y) \in B \times B : \exists b \in B ((x, b) \in S^{-1} \land (b, y) \in S) \}
$$
$$
= \{(x, y) \in B \times B : \exists b \in B ((b, x) \in S \land (b, y) \in S)\}
$$
$$
= \{(5, 6), (6, 5)\}
$$
$\proofend$

**Problem 6**
Suppose that $A = \{1, 2, 3\}$, $B = \{4, 5\}$, $C = \{6, 7, 8\}$, $R = \{(1, 7), (3, 6), (3, 7)\}$, and $S = \{(4, 7), (4, 8), (5, 6)\}$. Note that R is a relation from A to C and S is a relation from B to C. Find the following relations:
a) $S^{-1} \circ R$.
b) $R^{-1} \circ S$.
**Solution**
a)
$$
\{(x, y) \in A \times B : \exists c \in C ((x, c) \in R \land (c, y) \in S^{-1})\}
$$
$$
= \{(x, y) \in A \times B : \exists c \in C ((x, c) \in R \land (y, c) \in S)\}
$$
$$
= \{(1, 4), (4, 1), (3, 4), (4, 3), (3, 5), (5, 3)\}
$$

b)
$$
\{(x, y) \in B \times A : \exists c \in C ((x, c) \in S \land (c, y) \in R^{-1})\}
$$
$$
= \{(x, y) \in B \times A : \exists c \in C ((x, c) \in S \land (y, c) \in R)\}
$$
$$
= \{(1, 4), (4, 1), (3, 4), (4, 3), (3, 5), (5, 3)\}
$$
$\proofend$

**Problem 7**
Let R be a relation from A to B, S a relation from B to C, and T a relation from C to D.
a) Prove $Ran(R^{-1}) = Dom(R)$ by a chain of iff statements.
b) Give an alternative proof of $Ran(R^{-1}) = Dom(R)$ by showing that it follows from $(R^{-1})^{-1} = R$ and $Dom(R^{-1}) = Ran(R)$.
c) Complete the proof of $T \circ (S \circ R) = (T \circ S) \circ R$.
d) Prove $(S \circ R)^{-1} = R^{-1} \circ S^{-1}$.
**Solution**
a)
Let $a \in A$ be arbitrary. $a \in Ran(R^{-1})$ iff $\exists b \in B ((b, a) \in R^{-1})$ iff $\exists b \in B((a, b) \in R)$ iff $a \in Dom(R)$.

b)
We see that $Dom(R) = Dom((R^{-1})^{-1})$ since $(R^{-1})^{-1} = R$. Then $Dom((R^{-1})^{-1}) = Ran(R^{-1})$ since $Dom(R^{-1}) = Ran(R)$. Therefore, $Ran(R^{-1}) = Dom(R)$ as desired.

c)
Let $(a, d)$ be an arbitrary element of $A \times D$. First, suppose $(a, d) \in T \circ (S \circ R)$. By the definition of composition, this means that we can choose some $c \in C$ such that $(a, c) \in S \circ R$ and $(c, d) \in T$. Since $(a, c) \in S \circ R$, we can again use the definition of composition and choose some $b \in B$ such that $(a, b) \in R$ and $(b, c) \in S$. Now since $(b, c) \in S$ and $(c, d) \in T$, we can conclude that $(b, d) \in T \circ S$. Similarly, since $(a, b) \in R$ and $(b, d) \in T \circ S$, it follows that $(a, d) \in (T \circ S) \circ R$. Now suppose $(a, d) \in (T \circ S) \circ R$. By definition, there is some $b \in B$ such that $(a, b) \in R$ and $(b, d) \in T \circ S$. Again, by definition there is some $c \in C$ such that $(b, c) \in S$ and $(c, d) \in T$. Now since $(a, b) \in R$ and $(b, c) \in S$, we can conclude that $(a, c) \in S \circ R$. Again, since $(a, c) \in S \circ R$ and $(c, d) \in T$, we can conclude that $(a, d) \in T \circ (S \circ R)$. Thus, $T \circ (S \circ R) = (T \circ S) \circ R$.

d)
Suppose $(c, a) \in (S \circ R)^{-1}$. By definition, $(a, c) \in S \circ R$ and so there is some $b \in B$ such that $(a, b) \in R$ and $(b, c) \in S$. Then $(b, a) \in R^{-1}$ and $(c, b) \in S^{-1}$, and so $(c, a) \in R^{-1} \circ S^{-1}$. Now suppose that $(c, a) \in R^{-1} \circ S^{-1}$. Then there is some $b \in B$ such that $(c, b) \in S^{-1}$ and $(b, a) \in R^{-1}$. By definition of the inverse, $(b, c) \in S$ and $(a, b) \in R$. It follows that $(a, c) \in S \circ R$, meaning $(c, a) \in (S \circ R)^{-1}$ as desired. Thus, $(S \circ R)^{-1} = R^{-1} \circ S^{-1}$.
$\proofend$

**Problem 8**
Let $E = \{(p, q) \in P \times P : \text{the person p is an enemy of the person q}\}$, and $F = \{(p, q) \in P \times P : \text{the person p is a friend of the person q}\}$, where P is the set of all people. What does saying "an enemy of one's enemy is one's friend" mean about the relations E and F?
**Solution**
An enemy of one's enemy is simply $E \circ E$. All such ordered pairs are considered friends, so $E \circ E \subseteq F$.
$\proofend$

**Problem 9**
Suppose R is a relation from A to B and S is a relation from B to C.
a) Prove that $Dom(S \circ R) \subseteq Dom(R)$.
b) Prove that if $Ran(R) \subseteq Dom(S)$ then $Dom(S \circ R) = Dom(R)$.
c) Formulate and prove similar theorems about $Ran(S \circ R)$.
**Solution**
a)
Suppose $a \in Dom(S \circ R)$. By definition, there is some $c \in C$ such that $(a, c) \in S \circ R$. Again, by definition there is some $b \in B$ such that $(a, b) \in R$ and $(b, c) \in S$. So, by definition of domain, we see that $a \in Dom(R)$. Thus, $Dom(S \circ R) \subseteq Dom(R)$.

b)
Suppose $Ran(R) \subseteq Dom(S)$. $Dom(S \circ R) \subseteq Dom(R)$ shown in part a. Now suppose $a \in Dom(R)$. By definition, there is some $b \in B$ such that $(a, b) \in R$. So, $b \in Ran(R)$ and since $Ran(R) \subseteq Dom(S)$, we have $b \in Dom(S)$. It follows that there is some $c \in C$ such that $(b, c) \in S$. But then $(a, b) \in R$ and $(b, c) \in S$, so $(a, c) \in S \circ R$. By definition of domain, $a \in Dom(S \circ R)$ as desired. Thus, $Dom(S \circ R) = Dom(R)$.

c)
Statement: $Ran(S \circ R) \subseteq Ran(S)$.
Suppose $c \in Ran(S \circ R)$. By definition, there is some $a \in A$ such that $(a, c) \in S \circ R$. By definition of composition, there is some $b \in B$ such that $(a, b) \in R$ and $(b, c) \in S$. Therefore, $c \in Ran(S)$. Thus, we conclude that $Ran(S \circ R) \subseteq Ran(S)$.

Statement: if $Dom(S) \subseteq Ran(R)$ then $Ran(S \circ R) = Ran(S)$.
Suppose $Dom(S) \subseteq Ran(R)$. Let $c \in Ran(S)$. Then there is some $b \in B$ such that $(b, c) \in S$. So, $b \in Dom(S)$ and since $Dom(S) \subseteq Ran(R)$, we have $b \in Ran(R)$. By definition, there is some $a \in A$ such that $(a, b) \in R$. Bu then $(a, b) \in R$ and $(b, c) \in S$ so that $(a, c) \in S \circ R$. By definition of range, we see that $c \in Ran(S \circ R)$. Therefore, $Ran(S \circ R) = Ran(S)$.
$\proofend$

**Problem 10**
Suppose R and S are relations from A to B. Must the following statements be true? Justify your answers with proofs or counterexamples.
a) $R \subseteq Dom(R) \times Ran(R)$.
b) If $R \subseteq S$ then $R^{-1} \subseteq S^{-1}$.
c) $(R \cup S)^{-1} = R^{-1} \cup S^{-1}$.
**Solution**
a)
True. Suppose $(a, b) \in R$. Then $a \in Dom(R)$ and $b \in Ran(R)$ by definition. Therefore, $R \subseteq Dom(R) \times Ran(R)$.

b)
True. Suppose $R \subseteq S$ and let $(b, a) \in R^{-1}$. Then $(a, b) \in R$ and since $R \subseteq S$, we have $(a, b) \in S$. It follows that $(b, a) \in S^{-1}$ as desired. Therefore, $R^{-1} \subseteq S^{-1}$.

c)
True. $(\implies)$ Suppose $(b, a) \in (R \cup S)^{-1}$. Then $(a, b) \in (R \cup S)$. Case 1: $(a, b) \in R$. It follows that $(b, a) \in R^{-1}$ and so $(b, a) \in R^{-1} \cup S^{-1}$. Case 2: $(a, b) \in S$. It follows that $(b, a) \in S^{-1}$ and so $(b, a) \in R^{-1} \cup S^{-1}$. Therefore, $(R \cup S)^{-1} \subseteq R^{-1} \cup S^{-1}$. $(\Longleftarrow)$ Suppose $(b, a) \in R^{-1} \cup S^{-1}$. 
$\proofend$

**Problem 11**
Suppose R is a relation from A to B and S is a relation from B to C. Prove that $S \circ R = \emptyset$ iff $Ran(R)$ and $Dom(S)$ are disjoint.
**Solution**
$S \circ R = \emptyset$ iff $\forall (a, c) \in A \times C ((a, c) \not \in S \circ R)$ iff $\forall (a, c) \in A \times C \forall b \in B ((a, b) \not \in R \lor (b, c) \not \in S)$ iff $\forall (a, c) \in A \times C \forall b \in B \neg ((a, b) \in R \land (b, c) \in S)$ iff $\forall (a, c) \in A \times C \forall b \in B \neg (b \in Ran(R) \land b \in Dom(S))$ iff $Ran(R) \cap Dom(S) = \emptyset$.
$\proofend$

**Problem 12**
Suppose R is a relation from A to B and S and T are relations from B to C.
a) Prove that $(S \circ R) \backslash (T \circ R) \subseteq (S \backslash T) \circ R$.
b) What's wrong with the following proof that $(S \backslash T) \circ R \subseteq (S \circ R) \backslash (T \circ R)$?
Proof: Suppose $(a, c) \in (S \backslash T) \circ R$. Then we can choose some $b \in B$ such that $(a, b) \in R$ and $(b, c) \in S \backslash T$, so $(b, c) \in S$ and $(b, c) \not \in T$. Since $(a, b) \in R$ and $(b, c) \in S$, $(a, c) \in S \circ R$. Similarly, since $(a, b) \in R$ and $(b, c) \not \in T$, $(a, c) \not \in T \circ R$. Therefore, $(a, c) \in (S \circ R) \backslash (T \circ R)$. Since $(a, c)$ was arbitrary, this shows that $(S \backslash T) \circ R \subseteq (S \circ R) \backslash (T \circ R)$.
c) Must it be true that $(S \backslash T) \circ R \subseteq (S \circ R) \backslash (T \circ R)$?
**Solution**
a)
Suppose $(a, c) \in (S \circ R) \backslash (T \circ R)$. Then, since $(a, c) \in (S \circ R)$, there is some $b \in B$ such that $(a, b) \in R$ and $(b, c) \in S$. Also, since $(a, c) \not \in T \circ R$, we see that $(b, c) \not \in T$ because $(a, b) \in R$. But then $(b, c) \in S \land (b, c) \not \in T \equiv (b, c) \in S \backslash T$. Now we have $(a, b) \in R$ and $(b, c) \in S \backslash T$, meaning $(a, c) \in (S \backslash T) \circ R$. Therefore, $(S \circ R) \backslash (T \circ R) \subseteq (S \backslash T) \circ R$ as desired.

b)
The problematic statement is "Similarly, since $(a, b) \in R$ and $(b, c) \not \in T$, $(a, c) \not \in T \circ R$". b is some particular value whereas to claim $(a, c) \not \in T \circ R$, b must be arbitrary.

c)
False. Define (with appropriate A, B, and C),
$$
R := \{(1, 2), (1,3)\}, S := \{(2, 1)\}, T := \{(3, 1)\}
$$
We see that,
$$
(S \backslash T) \circ R = \{(1,1)\}, (S \circ R) \backslash (T \circ R) = \{(1, 1)\} \backslash \{(1,1)\} = \emptyset
$$
and so $(S \backslash T) \circ R \not \subseteq (S \circ R) \backslash (T \circ R)$.
$\proofend$

**Problem 13**
Suppose R and S are relations from A to B and T is a relation from B to C. Must the following statements be true?
a) If R and S are disjoint, then so are $R^{-1}$ and $S^{-1}$.
b) If R and S are disjoint, then so are $T \circ R$ and $T \circ S$.
c) If $T \circ R$ and $T \circ S$ are disjoint, then so are R and S.
**Solution**
a)
True. Suppose R and S are disjoint. Then let $(b, a) \in R^{-1}$ be arbitrary. It follows that $(a, b) \in R$ and since R is disjoint with S, $(a, b) \not \in S$. So, $(b, a) \not \in S^{-1}$. Therefore, $R^{-1}$ and $S^{-1}$ are disjoint.

b)
False. Define (with an appropriate A, B, and C),
$$
R := \{(1, 2)\}, S := \{(1, 4)\}, T := \{(2, 1), (4, 1)\}
$$
Notice R and S are disjoint. Now see that,
$$
T \circ R = \{(1, 1)\}, T \circ S = \{(1, 1)\}
$$
which are not disjoint.

c)
False. Define (with an appropriate A, B, and C),
$$
T := \emptyset, R := \{(1, 1)\}, S := \{(1, 1)\}
$$
Notice R and S are not disjoint. Now see that,
$$
T \circ R = \emptyset = T \circ S
$$
which are disjoint vacuously.
$\proofend$

**Problem 14**
Suppose R is a relation from A to B, and S and T are relations from B to C. Must the following statements be true?
a) If $S \subseteq T$ then $S \circ R \subseteq T \circ R$.
b) $(S \cap T) \circ R \subseteq (S \circ R) \cap (T \circ R)$.
c) $(S \cap T) \circ R = (S \circ R) \cap (T \circ R)$.
d) $(S \cup T) \circ R = (S \circ R) \cup (T \circ R)$.
**Solution**
a)
True. Suppose $S \subseteq T$ and let $(a, c) \in S \circ R$ be arbitrary. Then, for some $b \in B$, $(a, b) \in R$ and $(b, c) \in S$. Because $(b, c) \in S$ and $S \subseteq T$, we see that $(b, c) \in T$. Now $(b, c) \in T$ and $(a, b) \in R$ so that $(a, c) \in T \circ R$. Therefore, $S \circ R \subseteq T \circ R$.

b)
True. Suppose $(a, c) \in (S \cap T) \circ R$. Then there is some b such that $(a, b) \in R$ and $(b, c) \in S \cap T$. It follows that $(a, c) \in S \circ R$ and $(a, c) \in T \circ R$. So, $(a, c) \in (S \circ R) \cap (T \circ R)$. Therefore, $(S \cap T) \circ R \subseteq (S \circ R) \cap (T \circ R)$.

c)
False. We show $(S \circ R) \cap (T \circ R) \not \subseteq (S \cap T) \circ R$. Define (with appropriate A, B, and C),
$$
R := \{(1, 3), (1, 2)\}, S := \{(3, 1)\}, T := \{(2, 1)\}
$$
We see that,
$$
(S \circ R) \cap (T \cap R) = (\{(1,1)\}) \cap (\{(1,1)\}) = \{(1,1)\}
$$
but
$$
(S \cap T) \circ R = \emptyset \circ R = \emptyset
$$

d)
True. $(\implies)$ Suppose $(a, c) \in (S \cup T) \circ R$. Then there is some $b \in B$ such that $(a, b) \in R$ and $(b, c) \in S \cup T$. We divide this into two cases. Case 1: $(b, c) \in S$. It follows that $(a, c) \in S \circ R$. Case 2: $(b, c) \in T$. It follows that $(a, c) \in T \circ R$. Therefore, $(a, c) \in (S \circ R) \cup (T \circ R)$.
$\proofend$

**Problem 15**
Suppose R is a relation from A to B and S is a relation from C to D. Show that there is a set E such that R is a relation from A to E and S is a relation from E to D, and therefore the definition of $S \circ R$ can be applied. Furthermore, the definition gives the same result no matter which such set E is used.
**Solution**
Define $E := Ran(R) \cup Dom(S)$. Now consider arbitrary $(a, b) \in R$. We see that, by definition, $a \in A$ and $b \in Ran(R) = E$. Therefore, $R \subseteq A \times E$, making it a relation from A to E. Let $(c, d) \in S$ be arbitrary. Then $c \in Dom(S) = E$ and $d \in D$ so that $S \subseteq E \times D$. Therefore, S is a relation from E to D. Now $S \circ R$ is properly defined. (E can be empty)
$\proofend$

## 3.2 More About Relations

**Problem 1**
Let $L = \{a, b, c, d, e\}$ and $W = \{bad, bed, cab\}$. Let $R = \{(l, w) \in L \times W\ | \text{the letter l occurs in the word w}\}$. Draw a diagram of R.
**Solution:**

**Problem 2**
jfj
**Solution**

**Problem 3**
hjgdvbdnv
**Solution**

**Problem 4**
List the ordered pairs in the relations represented by the directed graphs in the Figure. Determine whether each relation is reflexive, symmetric, or transitive.
![[Screenshot from 2026-04-05 18-19-53.png]]
**Solution**
a)
$$
\{(a, c), (c, c), (d, a), (b, d), (d, b)\}
$$
This is not reflexive as it does not contain $(a, a)$. It is also not symmetric as it does not contain $(c, a)$, but contains $(a, c)$. It is also not transitive as it does not contain $(d, c)$, but contains $(d, a)$ and $(a, c)$.

b)
$$
\{(a, b), (b, a), (a, d), (b, d)\}
$$
This is not reflexive as it does not contain $(a, a)$. It is also not symmetric as it does not contain $(d, b)$, but contains $(b, d)$. It is transitive.

c)
$$
\{(a, a), (c, c), (b, b), (d, d), (b, d), (d, b)\}
$$
This is reflexive, symmetric, and transitive.

d)
$$
\{(a, c), (a, d), (a, b), (b, d), (c, d)\}
$$
It is not reflexive, not symmetric, and is transitive. Trivial to verify.
$\proofend$

**Problem 5**
The Figure shows two relations R and S. Find $S \circ R$.
![[Screenshot from 2026-04-05 18-35-39.png]]
**Solution**
$$
\{(a, y), (a, z), (b, x), (c, z), (c, y)\}
$$

$\proofend$

**Problem 6**
Suppose r and s are two positive real numbers. Let $D_r:= \{(x, y) \in \mathbb{R}^2 | ||x - y|| < r\}$ and $D_s := \{(x, y) \in \mathbb{R}^2 | ||x - y|| < s \}$. What is $D_r \circ D_s$? Justify your answer with a proof.
**Solution**

