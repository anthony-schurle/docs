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
Let $A = \{cat, dog, bird, rat\}$, and let $R = \{(x, y) \in A \times A | \text{there is at least one letter that occurs in both of the words x and y}\}$. Draw a di-graph for the relation R. Is R reflexive? Symmetric? Transitive?
**Solution**


**Problem 3**
Let $A = \{1, 2, 3, 4\}$. Draw a directed graph for $i_A$.
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
Suppose r and s are two positive real numbers. Let $D_r:= \{(x, y) \in \mathbb{R}^2 | |x - y| < r\}$ and $D_s := \{(x, y) \in \mathbb{R}^2 | |x - y| < s \}$. What is $D_r \circ D_s$? Justify your answer with a proof.
**Solution**
$$
D_r \circ D_s = \{(x, y) \in \mathbb{R}^2 : \exists v \in \mathbb{R} (x, v) \in D_s \land (v, y) \in D_r\}
$$
$$
= \{(x, y) \in \mathbb{R}^2 : \exists v \in \mathbb{R} (|x - v| < s) \land (|v - y| < r)\}
$$
$\proofend$

**Problem 7**
Prove part 1 of Theorem 4.3.4.
**Solution**
Suppose R is a reflexive relation on set A. Now let $(x, x) \in i_A$ be arbitrary. By definition $x \in A$. But R is reflexive so because $x \in A$, we have $xRx$. In other words, $(x, x) \in R$. Hence $i_A \subseteq R$. Now suppose that $i_A \subseteq R$. Let $x \in A$. We see that $(x, x) \in i_A$ since $x \in A$. But $i_A \subseteq R$ so $(x, x) \in R$. Because $x \in A$ was arbitrary, we have $\forall x \in A (xRx)$ which is precisely the definition of a reflexive R. $\proofend$

**Problem 8**
Prove part 3 of theorem 4.3.4
**Solution**
Suppose R is transitive and let $(x, y) \in R \circ R$ be arbitrary. It follows that $xRv$ and $vRy$ for some $v \in R$. But R is transitive, so we get $xRy$. Hence, $(x, y) \in R$ meaning $R \circ R \subseteq R$. Now suppose that $R \circ R \subseteq R$ and let $xRp$, $pRy$ for arbitrary $x, p, y \in R$. Notice $(x, y) \in R \circ R$ by construction and since $R \circ R \subseteq R$, we get $(x, y) \in R$. So, $xRy$ which is the very definition of transitive. $\proofend$

**Problem 9**
Suppose A and B are sets.
a) Show that for every relation R from A to B, $R \circ i_A = R$.
b) Show that for every relation R from A to B, $i_B \circ R = R$.
**Solution**
a)
Suppose $(x, y) \in R \circ i_A$. Then $(x, v) \in i_A$ and $(v, y) \in R$ for some $v \in R$ by construction. But $(x, v) \in i_A$ means $x = v$. Hence $(x, y) \in R$. Therefore, $R \circ i_A \subseteq R$. Now suppose that $(a, b) \in R$. Then $a \in A$ and so $(a, a) \in i_A$. So $(a, b) \in R \circ i_A$ since $(a, a) \in i_A$ and $(a, b) \in R$. Therefore, $R \subseteq R \circ i_A$. $\proofend$

b)
Suppose $(x, y) \in i_B \circ R$. Then $(v, y) \in i_B$ and $(x, v) \in R$ for some $v \in R$ by construction. But $(v, y) \in i_B$ means $y = v$. Hence $(x, y) \in R$. Therefore, $i_B \circ R \subseteq R$. Now suppose that $(a, b) \in R$. Then $b \in B$ and so $(b, b) \in i_B$. So $(a, b) \in i_B \circ R$ since $(b, b) \in i_B$ and $(a, b) \in R$. Therefore, $R \subseteq i_B \circ R$. $\proofend$

**Problem 10**
Suppose S is a relation on A. Let $D = Dom(S)$ and $R = Ran(S)$. Prove that $i_D \subseteq S^{-1} \circ S$ and $i_R \subseteq S \circ S^{-1}$.
**Solution**
Suppose $(x, x) \in i_D$. Then $x \in D$, meaning there is some $y \in A$ such that $(x, y) \in S$. It follows that $(y, x) \in S^{-1}$ and so $(x, x) \in S^{-1} \circ S$. But x was arbitrary giving $i_D \subseteq S^{-1} \circ S$.

Suppose $(a, a) \in i_R$. Then $a \in R$, meaning there is some $b \in A$ such that $(b, a) \in S$. It follows that $(a, b) \in S^{-1}$. Hence $(a,a) \in S \circ S^{-1}$. Since $(a, a)$ was arbitrary we see that  $i_R \subseteq S \circ S^{-1}$. $\proofend$

**Problem 11**
Suppose R is a relation on A. Prove that if R is reflexive then $R \subseteq R \circ R$.
**Solution**
Let $(x, y) \in R$ be arbitrary and suppose R is reflexive. Then $x \in A$ and from reflexivity, we get $(x, x) \in R$. Because $(x, x) \in R$ and $(x, y) \in R$, we get $(x, y) \in R \circ R$. But $(x, y)$ was arbitrary so $R \subseteq R \circ R$. $\proofend$

**Problem 12**
Suppose R is a relation on A.
a) Prove that if R is reflexive, then so is $R^{-1}$.
b) Prove that if R is symmetric, then so is $R^{-1}$.
c) Prove that if R is transitive, then so is $R^{-1}$.
**Solution**
a)
Suppose so. Let $a \in A$ be arbitrary. Since R is reflexive, $(a, a) \in R$. By definition, $(a, a) \in R^{-1}$. Because a was arbitrary, $R^{-1}$ is reflexive.

b)
Suppose so. Let $xR^{-1}y$ for arbitrary $x, y \in A$. Then $(y, x) \in R$  by definition, and from symmetry $(x, y) \in R$. Hence $(y, x) \in R^{-1}$ making $R^{-1}$ symmetric from arbitrary $x, y \in A$.

c)
Suppose so. Let $xR^{-1}y$ and $yR^{-1}z$ for arbitrary $x, y, z \in A$. Then $yRx$ and $zRy$ by definition. So, by transitivity, $zRx$. Hence $xR^{-1}z$ meaning $R^{-1}$ is transitive. $\proofend$

**Problem 13**
Suppose $R_1$ and $R_2$ are relations on A. For each part, give either a proof or a counterexample to justify your answer.
a) If $R_!$ and $R_2$ are reflexive, must $R_1 \cup R_2$ be reflexive?
b) If $R_1$ and $R_2$ are symmetric, must $R_1 \cup R_2$ be symmetric?
c) If $R_1$ and $R_2$ are transitive, must $R_1 \cup R_2$ be transitive?
**Solution**
a)
Yes. Suppose so. Let $x \in A$ be arbitrary. Then $xR_1x$ and $xR_2x$ since both are reflexive. Hence $x(R_1 \cup R_2)x$ making $R_1 \cup R_2$ reflexive.

b)
Yes. Suppose so. Let $x(R_1 \cup R_2)y$ for arbitrary $x, y \in A$. Then either $xR_1y$ or $xR_2y$. Case 1: $xR_1y$. It follows that $yR_1x$ since $R_1$ is symmetric and so $y(R_1 \cup R_2)x$. Case 2: $xR_2y$. It follows that $yR_2x$ since $R_2$ is symmetric and so $y(R_1 \cup R_2)x$. Hence we always get $y(R_1 \cup R_2)x$ for arbitrary $x, y \in A$. Therefore, $R_1 \cup R_2$ is symmetric.

c)
No. Let,
$$
R_1 := \{(1, 2), (2, 3), (1, 3)\}, R_2 := \{(3, 1), (1, 2), (3, 2)\}
$$
with A defined according to these relations. Then $R_1$ and $R_2$ are both transitive. But,
$$
R_1 \cup R_2 = \{(1, 2), (2, 3), (1, 3), (3, 1), (3, 2)\}
$$
is not transitive since $(1, 3)$ and $(3, 1)$ are both contained while $(3, 3)$ is not. $\proofend$

**Problem 14**
Suppose $R_1$ and $R_2$ are relations on A. For each part, give either a proof or a counterexample to justify your answer.
**Solution**
a) If $R_1$ and $R_2$ are reflexive, must $R_1 \cap R_2$ be reflexive?
b) If $R_1$ and $R_2$ are symmetric, must $R_1 \cap R_2$ be symmetric?
c) If $R_1$ and $R_2$ are transitive, must $R_1 \cap R_2$ be transitive?
**Solution**
a)
Yes. Suppose so. Let $x \in A$ be arbitrary. Then $xR_1x$ and $xR_2x$ since both are reflexive. Hence $x(R_1 \cap R_2)x$ meaning $R_1 \cap R_2$ is reflexive.

b)
Yes. Suppose so. Let $x(R_1 \cap R_2)y$ for arbitrary $x, y \in A$. Then $xR_1y$ and $xR_2y$. But both are symmetric so $yR_1x$ and $yR_2x$. Hence $y(R_1 \cap R_2)x$ meaning $R_1 \cap R_2$ is symmetric.

c)
Yes. Suppose so. Let $x(R_1 \cap R_2)y$  and $y(R_1 \cap R_2)z$ for arbitrary $x, y, z \in A$. Then $xR_1y$, $xR_2y$, $yR_1z$, and $yR_2z$. Because $R_1$ and $R_2$ are transitive, $xR_1z$ and $xR_2z$. But then $x(R_1 \cap R_2)z$. Since $x, y, z \in A$ arbitrary, we get $R_1 \cap R_2$ transitive. $\proofend$

**Problem 15**
Suppose $R_1$ and $R_2$ are relations on A. For each part, give either a proof or a counterexample to justify your answer.
a) If $R_1$ and $R_2$ are reflexive, must $R_1 \backslash R_2$ be reflexive?
b) If $R_1$ and $R_2$ are symmetric, must $R_1 \backslash R_2$ be symmetric?
c) If $R_1$ and $R_2$ are transitive, must $R_1 \backslash R_2$ be transitive?
**Solution**
a)
No. Let,
$$
R_1 := \{(a, a)\}, R_2 = R_1, A := \{a\}
$$
so that $R_1$ and $R_2$ are reflexive. We see that $R_1 \backslash R_2 = \emptyset$ which is not reflexive.

b)
Yes. Suppose so. Then let $x(R_1 \backslash R_2)y$ for arbitrary $x, y \in A$. It follows that $xR_1 y$ but $(x, y) \not \in R_2$. Since $R_1$ is symmetric, $yR_1x$ as well. If $yR_2 x$, then by symmetry $x R_2 y$ which we said was impossible. Hence $(y, x) \not \in R_2$. Because $(y, x) \in R_1$ and $(y, x) \not \in R_2$, we have $y(R_1 \backslash R_2)x$. But $x, y \in A$ was arbitrary so $(R_1 \backslash R_2)$ is symmetric.

c)
No. Let,
$$
R_1 := \{(1, 2), (2, 3), (1, 3)\}, R_2 := \{(1, 3), (3, 4), (1, 4)\}
$$
with $A$ defined accordingly. We see that $R_1$ and $R_2$ are transitive. But $R_1 \backslash R_2 = \{(1, 2), (2, 3), (3, 4), (1, 4)\}$ which is not transitive since $(1, 2)$ and $(2, 3)$ are contained while $(1, 3)$ is not contained. $\proofend$

**Problem 16**
Suppose R and S are reflexive relations on A. Prove that $R \circ S$ is reflexive.
**Solution**
Let $a \in A$ be arbitrary. Since R and S are reflexive, $aRa$ and $aSa$. Hence $a(R \circ S)a$. But a was arbitrary so $R \circ S$ is reflexive. $\proofend$

**Problem 17**
Suppose R and S are symmetric relations on A. Prove that $R \circ S$ is symmetric iff $R \circ S = S \circ R$.
**Solution**
Suppose $R \circ S$ is symmetric. Then let $(x, y) \in R \circ S$. Since $R \circ S$ is symmetric, $(y, x) \in R \circ S$. By definition, $ySv$ and $vRx$ for some $v \in A$. But R and S are symmetric, so $vSy$ and $xRv$. Hence $(x, y) \in S \circ R$. Therefore, $R \circ S \subseteq S \circ R$. Let $(i, j) \in S \circ R$. Then $iRa$ and $aSj$ for some $a \in A$. It follows by symmetry of R and S, $aRi$ and $jSa$. So $(j, i) \in R \circ S$. Since $R \circ S$ is symmetric, $(i, j) \in R \circ S$. Therefore, $S \circ R \subseteq R \circ S$. Because $R \circ S \subseteq S \circ R$ and $S \circ R \subseteq R \circ S$, we get $R \circ S = S \circ R$. Now suppose that $R \circ S = S \circ R$. Notice $(R \circ S)^{-1} = S^{-1} \circ R^{-1}$. But S and R are symmetric so $S^{-1} \circ R^{-1} = S \circ R$. Because $S \circ R = R \circ S$, we get $(R \circ S)^{-1} = R \circ S$. Hence $R \circ S$ is symmetric. $\proofend$

**Problem 18**
Suppose R and S are transitive relations on A. Prove that if $S \circ R \subseteq R \circ S$ then $R \circ S$ is transitive.
**Solution**
Suppose $S \circ R \subseteq R \circ S$. Let $x(R \circ S)y$ and $y(R \circ S)z$ for arbitrary $x, y, z \in A$. By definition, we have: $xSa$, $ySb$, $aRy$, $bRz$. Since $aRy$ and $ySb$, we get $a(S \circ R)b$. But $S \circ R \subseteq R \circ S$ so that $a(R \circ S)b$. Hence $aSc$ and $cRb$ for some $c \in A$. Because $xSa$, $aSc$, and S is transitive - $xSc$. Because $cRb$, $bRz$, and R is transitive - $cRz$. Since $xSc$ and $cRz$, $x(S \circ R)z$. But $S \circ R \subseteq R \circ S$, and so $x(R \circ S)z$. Thus, from arbitrary $x, y, z \in A$, $R \circ S$ is transitive. $\proofend$

**Problem 19**
Consider the following putative theorem. Theorem? Suppose R is a relation on A, and define a relation S on $\mathcal{P}(A)$ as follows: $S = \{(X, Y) \in \mathcal{P}(A) \times \mathcal{P}(A) | \exists x \in X \exists y \in Y (xRy)\}$. If R is transitive, then so is S.
a) What's wrong with the following proof of the theorem? Proof. Suppose R is transitive. Suppose $(X, Y) \in S$ and $(Y, Z) \in S$. Then by definition of S, $xRy$ and $yRz$, where $x \in X$, $y \in Y$, and $z \in Z$. Since $xRy$, $yRz$, and R is transitive, $xRz$. But then since $x \in X$ and $z \in Z$, it follows from the definition of S that $(X, Z) \in S$. Thus, S is transitive.
b) Is the theorem correct? Justify.
**Solution**
a)
The problematic line is "Then by definition of S, $xRy$ and $yRz$, where $x \in X$, $y \in Y$, and $z \in Z$". The definition only guarantees that $xRu$ and $vRz$ for some $u, v \in Y$. Not that $u = v$. 

b)
No. Let,
$$
R := \{(1, 2), (3, 4)\}, A := \{1, 2, 3, 4\}, X := \{1\}, Y := \{2, 3\}, Z := \{4\}
$$
We see that R is transitive and is clearly a relation on A. But notice $1R2$ for $1 \in X$ and $2 \in Y$, so that $(X, Y) \in S$. Similarly, $(Y, Z) \in S$. However, $(1, 4) \not \in R$, and so it is impossible for some $x \in X$ and some $z \in Z$ such that $xRz$. Hence, $(X, Z) \not \in S$. Thus, S is not transitive. $\proofend$

**Problem 20**
Suppose R is relation on A. Let $B = \{X \in \mathcal{P}(A) | X \ne \emptyset\}$, and define a relation S on B as follows: $S = \{(X, Y) \in B \times B | \forall x \in X \forall y \in Y (xRy)\}$. Prove that if R is transitive, so is S. Why did the empty set have to be excluded?
**Solution**
Suppose the empty set was not excluded and we have a transitive R. Then $(X, \emptyset) \in S$ and $(\emptyset, Y) \in S$ for distinct X and Y assuming a set A size larger than 1. The theorem would conclude that $(X, Y) \in S$ which is not necessarily true since the relation could be empty as well, though there are more complex cases where the relation is not empty.

Suppose R is transitive. Let $(X, Y) \in S$ and $(Y, Z) \in S$ for arbitrary $X, Y, Z \in B$. Consider arbitrary $x \in X$, $y \in Y$, and $z \in Z$ - all possible since they are not empty. Because $(X, Y) \in S$ and $(Y, Z) \in S$, we have $xRy$ and $yRz$. But R is transitive, meaning $xRz$. It follows that $(X, Z) \in S$ since $x$ and $z$ were arbitrary. Hence S is transitive. $\proofend$

**Problem 21**
Suppose R is a relation on A, and define a relation S on $\mathcal{P}(A)$ as follows: $S = \{(X, Y) \in \mathcal{P}(A) \times \mathcal{P}(A) | \forall x \in X \exists y \in Y (xRy)\}$. For each part, justify.
a) If R is reflexive, must S be reflexive?
b) If R is symmetric, must S be symmetric?
c) If R is transitive, must S be transitive?
**Solution**
a)
Yes. Suppose so. Then let $X \in \mathcal{P}(A)$ be arbitrary. If X is empty, then $(X, X) \in S$ vacuously. If X is not empty, let $x \in X$. Then $x \in A$ since $X \in \mathcal{P}(A)$, and from reflexivity of R we have $xRx$. Hence $(X, X) \in S$. Thus, S is reflexive.

b)
No. Let,
$$
R := \{(1, 1)\}, A := \{1, 2\}, X := \{1\}, Y := \{1,2\}
$$
Then R is symmetric and clearly a relation on A. Notice $(X, Y) \in S$ since $1R1$. However, $(Y, X) \not \in S$ since no relation in $R$ exists for $2 \in S$. Hence S is not symmetric.

c)
Yes. Suppose so. Let $(X, Y) \in S$ and $(Y, Z) \in S$ for arbitrary $X, Y, Z \in \mathcal{P}(A)$. If X is empty, then $(X, Z) \in S$ vacuously. So, suppose X is not empty. Pick any $x \in X$. Then $xRy$ for some $y \in Y$ since $(X, Y) \in S$. Also, $yRz$ for some $z \in Z$ since $(Y, Z) \in S$. By transitivity of R, $xRz$. But x was an arbitrary element of X, so $(X, Z) \in S$. Therefore, S is transitive. $\proofend$

**Problem 22**
Consider the following putative theorem. Theorem? Suppose R is a relation on A. If R is symmetric and transitive, then R is reflexive.
Is the following proof correct? If so, what proof strategies does it use? If not, can it be fixed? Is the theorem correct?
Proof. Let x be an arbitrary element of A. Let y be any element of A such that $xRy$. Since R is symmetric, it follows that $yRx$. But then by transitivity, since $xRy$ and $yRx$ we can conclude that $xRx$. Since x was arbitrary, we have shown that $\forall x \in A(xRx)$, so R is reflexive.
**Solution**
The proof is not correct. We do not know if $xRy$ exists. This is not fixable, the theorem fails when some element of A is not contained in the domain nor the range of R. $\proofend$

**Problem 23**
Suppose A is a set, and $F \subseteq \mathcal{P}(A)$. Let $R = \{(a, b) \in A \times A | \forall X \subseteq (A \backslash \{a, b\} (X \cup \{a\} \in F \implies X \cup \{b\} \in F))\}$. Show that R is transitive.
**Solution**
Let $(x, y) \in R$ and $(y, z) \in R$ for any $x, y, z \in A$. Pick any $X \subseteq (A \backslash \{x, z\})$ and suppose $X \cup \{x\} \in F$. Either $y \in X$ or $y \not \in X$. Case 1: $y \not \in X$. Then since $(x, y) \in R$, $X \subseteq (A \backslash \{x, y, z\}) \subseteq (A \backslash \{x, y\})$, and $X \cup \{x\} \in F$ we can conclude that $X \cup \{y\} \in F$. Because $(y, z) \in R$, $X \subseteq (A \backslash \{x, y, z\}) \subseteq (A \backslash \{y, z\})$, and $X \cup \{y\} \in F$ we can conclude that $X \cup \{z\} \in F$. Hence $(x, z) \in R$. Case 2: $y \in X$. Notice $X \backslash \{y\} \cup \{x\} \subseteq A \backslash \{y, z\}$, $X \backslash \{y\} \cup \{x\} \cup \{y\} = X \cup \{x\} \in F$, and $(y, z) \in R$ so that we can conclude $X \backslash \{y\} \cup \{x\} \cup \{z\} \in F$. Since $(x, y) \in R$, $X \backslash \{y\} \cup \{z\} \subseteq A \backslash \{x, y\}$, and $X \backslash \{y\} \cup \{z\} \cup \{x\} \in F$ we can conclude $X \backslash \{y\} \cup \{z\} \cup \{y\} = X \cup \{z\} \in F$. Hence $(x, z) \in R$. In either case, we get $(x, z) \in R$ for arbitrary $x, y, z \in A$. Thus, R is transitive. $\proofend$

**Problem 24**
Let $R = \{(m, n) \in \mathbb{N} \times \mathbb{N} | |m - n| \le 1 \}$, which is a relation on $\mathbb{N}$. Note that $R \subseteq \mathbb{Z} \times \mathbb{Z}$, so R is also a relation on $\mathbb{Z}$.
a) Is R reflexive on $\mathbb{N}$?
b) Is R reflexive on $\mathbb{Z}$?
**Solution**
a)
Yes. Pick any $n \in \mathbb{N}$. Then $(n, n) \in \mathbb{N} \times \mathbb{N}$ and $|n - n | = 0 \le 1$ so that $nRn$. Hence, R is reflexive.

b)
No. Notice $(-1, -1) \not \in R$ since $-1 \not \in \mathbb{N}$. Hence R is not reflexive here. $\proofend$

## 3.3 Ordering Relations

**Problem 1**
In each case, say whether or not R is a partial order on A. If so, is it a total order?
a) $A = \{a, b, c\}, R = \{(a, a), (b, a), (b, b), (b, c), (c, c)\}$.
b) $A = \mathbb{R}, R = \{(x, y) \in \mathbb{R} \times \mathbb{R} | |x| \le |y|\}$.
c) $A = \mathbb{R}, R = \{(x, y) \in \mathbb{R} \times \mathbb{R} | |x| < |y| \lor x = y\}$.
**Solution**
a)
It is reflexive, transitive, and anti-symmetric - so a partial order. However, $(a, c) \not \in R$ and $(c, a) \not \in R$ so R is not a total order.

b)
R is not a partial order, and so not a total order either; it fails to be anti-symmetric. For $-1, 1 \in A$ we have $-1R1$ and $1R-1$ but $1 \ne -1$.

c)
R is a total order. It is reflexive, transitive, anti-symmetric, and for any $x, y \in A$ we have $xRy$ or $yRx$. $\proofend$

**Problem 2**
In each case, say whether or not R is a partial order on A. If so, is it a total order?
a) 
$A = \text{set of all words of English},$
$R = \{(x, y) \in A \times A | \text{word y occurs at least as late in alphabetical order as word x}\}$.
b)
$A = \text{set of all words of English},$
$R = \{(x, y) \in A \times A | \text{first letter of word y occurs at least as late in alphabet as first letter of word x}\}$.
c)
$A = \text{set of all countries in the world},$
$R = \{(x, y) \in A \times A | \text{population of country y is as least as large as population of country x}\}$.
**Solution**
a)
R is a total order; it is reflexive, transitive, anti-symmetric, and for any $x, y \in A$ we have $xRy$ or $yRx$.

b)
R is not a partial order; it fails to be anti-symmetric.

c)
If populations are distinct, R is a total order. If not, R fails to be a partial order. The difference lies in anti-symmetry. In either case, R is reflexive, transitive, and for any $x, y \in A$ we have $xRy$ or $yRx$. However, when population are not distinct having $xRy$ and $yRx$ does not imply $x = y$. $\proofend$

**Problem 3**
In each case, find all minimal and maximal elements of B. Also find, if they exist, the largest and smallest elements of B, and the least upper bound and greatest lower bound of B.
a) $R =$ relation in the graph, $B = \{2, 3, 4\}$.
![[Screenshot from 2026-05-12 13-00-08.png]]

b) $R = \{(x, y) \in \mathbb{R}^2 | x \le y\}, B = \{x \in \mathbb{R} | 1 \le x < 2\}$.
c) $R = \{(x, y) \in \mathcal{P}(\mathbb{N}) \times \mathcal{P}(\mathbb{N}) | x \subseteq y\}, B = \{x \in \mathcal{P}(\mathbb{N}) | \text{x has at most 5 elements}\}$.
**Solution**
a)
2 is the only minimal element of B since $2R3$ and $2R4$. Both 3 and 4 are maximal elements of B since $2R3$. 2 is the smallest element of B, since $2Rx$ for every $x \in B$. No largest element exists in B. The lower bounds for B are 1 and 2. Hence the g.l.b is 2. No upper bounds exist for B and so no l.u.b.

b)
1 is the only minimal element of B. B does not have a maximal element however. The smallest element of B is 1. B does not have a largest element. The lower bounds of B are $\{x \in \mathbb{R} | x \le 1\}$. Clearly, the g.l.b. is 1. The upper bounds of B are $\{x \in \mathbb{R} | x \ge 2\}$. Clearly, the l.u.b. is 2.

c)
The empty set is the only minimal element of B. The maximal elements of B are $\{x \in \mathcal{P}(\mathbb{N}) | \text{x has 5 elements}\}$. The smallest element of B is the empty set. There is no largest element of B. The lower bound for B is the empty set and it is also the g.l.b.. The only upper bound for B is $\mathbb{N}$ and so it is also the l.u.b.. $\proofend$

**Problem 4**
Suppose R is a relation on A. Prove that R is both anti-symmetric and symmetric iff $R \subseteq i_A$.
**Solution**
Suppose R is both symmetric and anti-symmetric. Let $xRy$ for $x, y \in A$. Since R is symmetric, we also have $yRx$. But R is anti-symmetric, $xRy$, and $yRx$ meaning $y = x$. Hence $(x, y) \in i_A$. Therefore, $R \subseteq i_A$. Suppose $R \subseteq i_A$. Let $xRy$ for $x, y \in A$. If $x \ne y$, then $(x, y) \not \in i_A$ which is impossible since $(x, y) \in R$ and $R \subseteq i_A$. So $x = y$. It follows that $xRy = yRx$. Since $x, y \in A$ was arbitrary, R is symmetric. Now let $mRn$ and $nRm$ for $m, n \in A$. But we know that $m = n$ and so R is anti-symmetric. Thus,  R is both anti-symmetric and symmetric iff $R \subseteq i_A$. $\proofend$

**Problem 5**
Suppose R is a partial order on A and $B \subseteq A$. Prove that $R \cap (B \times B)$ is a partial order on B.
**Solution**
Let $(x, x) \in i_B$. Then $(x, x) \in B \times B$. Since R is a partial order, it is reflexive. We know $x \in B$ and from $B \subseteq A$, we get $x \in A$. Hence $(x, x) \in R$. Because $(x, x) \in R$ and $(x, x) \in B \times B$, we have $(x, x) \in R \cap (B \times B)$. Therefore, $i_B \subseteq R \cap (B \times B)$ meaning $R \cap (B \times B)$ is reflexive. Now let $(a, b) \in R \cap (B \times B)$ and $(b, c) \in R \cap (B \times B)$ for $a, b, c \in B$. We know $(a, c) \in B \times B$ since $a, c \in B$. Notice $aRb$ and $bRc$, where R is transitive since it is a partial order. It follows that $aRc$. But then $(a, c) \in R$ and $(a, c) \in B \times B$ so that $(a, c) \in R \cap (B \times B)$. Because $a, b, c \in B$ was arbitrary, $R \cap (B \times B)$ is transitive. Finally, let $(m, n) \in R \cap (B \times B)$ and $(n, m) \in R \cap (B \times B)$ for $n, m \in B$. Then $mRn$ and $nRm$. But R is a partial order and so anti-symmetric. Hence $m = n$. Since $m, n \in B$ was arbitrary, $R \cap (B \times B)$ is anti-symmetric. Thus, $R \cap (B \times B)$ is a partial order. $\proofend$

**Problem 6**
Suppose $R_1$ and $R_2$ are partial orders on A. For each part, give either a proof or a counterexample to justify your answer.
a) Must $R_1 \cap R_2$ be a partial order on A?
b) Must $R_1 \cup R_2$ be a partial order on A?
**Solution**
a)
Yes. Let $(x, x) \in i_A$. We see that $(x, x) \in R_1$ and $(x, x) \in R_2$ since $R_1$ and $R_2$ are both reflexive. So $(x, x) \in R_1 \cap R_2$ meaning $i_A \subseteq R_1 \cap R_2$. Hence $R_1 \cap R_2$ is reflexive. Now let $(a, b) \in R_1 \cap R_2$ and $(b, c) \in R_1 \cap R_2$ for $a, b, c \in A$. Then $aR_1b$ and $bR_1c$ for transitive $R_1$, giving $aR_1c$. Similarly, $aR_2c$. Therefore, $(a, c) \in R_1 \cap R_2$. But $a, b, c \in A$ was arbitrary so that $R_1 \cap R_2$ is transitive. Finally, let $(m, n) \in R_1 \cap R_2$ and $(n, m) \in R_1 \cap R_2$ for $m, n \in A$. We see that $nR_1m$ and $mR_1n$ for anti-symmetric $R_1$, meaning $m = n$. It follows that $R_1 \cap R_2$ is anti-symmetric. Thus, $R_1 \cap R_2$ is a partial order on A.

b)
No. Both anti-symmetry and transitivity can fail for $R_1 \cup R_2$. Let,
$$
R_1 := \{(1, 1), (2, 2), (1, 2)\}, R_2 := \{(1, 1), (2, 2), (2, 1)\}, A := \{1, 2\}
$$
We see that $R_1$ and $R_2$ are both partial orders on A. However, $R_1 \cup R_2 = \{(1, 1), (2, 2), (1, 2), (2, 1)\}$ which is not a partial order since it contains $(1, 2)$ and $(2, 1)$ where $1 \ne 2$. $\proofend$

**Problem 7**
Suppose $R_1$ is a partial order on $A_1$, $R_2$ is a partial order on $A_2$, and $A_1 \cap A_2 = \emptyset$.
a) Prove that $R_1 \cup R_2$ is a partial order on $A_1 \cup A_2$.
b) Prove that $R_1 \cup R_2 \cup (A_1 \times A_2)$ is a partial order on $A_1 \cup A_2$.
c) Suppose that $R_1$ and $R_2$ are total orders. Are the partial orders in parts (a) and (b) also total orders?
**Solution**
a)
Let $(x, x) \in i_{A_1 \cup A_2}$. Then $x \in A_1$ or $x \in A_2$. Case 1: $x \in A_1$. Then $(x, x) \in R_1$ since $R_1$ is reflexive over $A_1$, meaning $(x, x) \in R_1 \cup R_2$. Hence $i_{A_1 \cup A_2} \subseteq R_1 \cup R_2$. Case 2: $x \in A_2$. Then $(x, x) \in R_2$ since $R_2$ is reflexive over $A_2$, meaning $(x, x) \in R_1 \cup R_2$. Hence $i_{A_1 \cup A_2} \subseteq R_1 \cup R_2$. In either case, $i_{A_1 \cup A_2} \subseteq R_1 \cup R_2$ implies $R_1 \cup R_2$ is reflexive. Now let $(a, b) \in R_1 \cup R_2$ and $(b, c) \in R_1 \cup R_2$ for $a, b, c \in A_1 \cup A_2$. Notice four cases exist, $(a, b) \in R_1$ and $(b, c) \in R_1$; $(a, b) \in R_2$ and $(b, c) \in R_2$; $(a, b) \in R_1$ and $(b, c) \in R_2$; $(a, b) \in R_2$ and $(b, c) \in R_1$. Case 1: $(a, b) \in R_1$ and $(b, c) \in R_1$. By transitivity of $R_1$, we have $(a, c) \in R_1$ and so $(a, c) \in R_1 \cup R_2$. Case 2: $(a, b) \in R_2$ and $(b, c) \in R_2$. By transitivity of $R_2$, we have $(a, c) \in R_2$ and so $(a, c) \in R_1 \cup R_2$. Case 3-4: $(a, b) \in R_1$ and $(b, c) \in R_2$ or $(a, b) \in R_2$ and $(b, c) \in R_1$. Then $b \in A_1$ and $b \in A_2$ by definition of $R_1$ and $R_2$. Hence $b \in A_1 \cap A_2$, a contradiction since $A_1 \cap A_2 = \emptyset$. Therefore, these cases are not possible. So in any of the cases, we have $(a, c) \in R_1 \cup R_2$. It follows that $R_1 \cup R_2$ is transitive. Finally, let $(m, n) \in R_1 \cup R_2$ and $(n, m) \in R_1 \cup R_2$ for $n, m \in A_1 \cup A_2$. By similar reasoning of transitivity, it is not possible for $(m, n) \in R_1 \land (n, m) \in R_2$ or $(m, n) \in R_2 \land (n, m) \in R_1$. Hence we consider only the two cases $(m, n), (n, m) \in R_1$ and $(m, n), (n, m) \in R_2$. Case 1: $(m, n), (n, m) \in R_1$. Then by anti-symmetry of $R_1$ we get $m = n$. Case 2: $(m, n), (n, m) \in R_2$. Then by anti-symmetry of $R_2$, we get $m = n$. In either case $m = n$. Therefore, $R_1 \cup R_2$ is anti-symmetric. Thus, $R_1 \cup R_2$ is a partial order on $A_1 \cup A_2$.

b)


## 3.4 Equivalence Relations

**Problem 1**
Find all partitions of the set $A = \{1, 2, 3\}$.
**Solution**
$$
\{\{1\}, \{2\}, \{3\}\}, \{\{1, 2\}, \{3\}\}, \{\{1\}, \{2, 3\}\}, \{A\}
$$
$\proofend$

**Problem 2**
Find all equivalence relations on the set $A = \{1, 2, 3\}$.
**Solution**
$$
\{(1, 1), (2, 2), (3, 3)\}, \{(1, 1), (2, 2), (3, 3), (1, 2), (2, 1)\}, \{(1, 1), (2, 2), (3, 3), (2, 3), (3, 2)\},
$$
$$
\{(1, 1), (2, 2), (3, 3), (1, 2), (2, 1), (1, 3), (3, 1), (2, 3), (3, 2)\}
$$
$\proofend$

**Problem 3**
Let $W =$ the set of all words in the English Language. Which of the following relations on W are equivalence relations? For those that are equivalence relations, what are the equivalence classes?
a) $R = \{(x, y) \in W \times W | \text{the words x and y start with the same letter}\}$.
b) $S = \{(x, y) \in W \times W | \text{the words x and y have at least one letter in common}\}$.
c) $T = \{(x, y) \in W \times W | \text{the words x and y have the same number of letters}\}$.
**Solution**
a)
R is reflexive, symmetric, and transitive - so an equivalence relation. There are 26 equivalence classes corresponding to words that start with the same letter in the english language.

b)
S is not transitive, consider $(a, and) \in S$ and $(and, no) \in S$ but $(a, no) \not \in S$. Hence S is not an equivalence relation.

c)
T is reflexive, symmetric, and transitive - so an equivalence relation. The equivalence classes consist of words with a fixed number of letters. $\proofend$

**Problem 4**
Which of the following relations on $\mathbb{R}$ are equivalence relations? For those that are equivalence relations, what are the equivalence classes?
a) $R = \{(x, y) \in \mathbb{R}^2 | x-y \in \mathbb{N}\}$.
b) $S = \{(x, y) \in \mathbb{R}^2 | x-y \in \mathbb{Q}\}$.
c) $T = \{(x, y) \in \mathbb{R}^2 | \exists n \in \mathbb{Z}(y = x \cdot 10^n)\}$.
**Solution**
a)
R is not symmetric, and so not an equivalence relation. Consider $(5, 1) \in R$ but $(1, 5) \not \in R$.

b)
S is reflexive, symmetric, and transitive (addition of quotients is closed) - so S is a equivalence relation. The equivalence classes consist of the real numbers that differ by a multiple of some fixed quotient.

c)
T is reflexive, symmetric, and transitive - so an equivalence relation. The equivalence classes are all reals differing by $10^n$ for some fixed $n \in \mathbb{Z}$. Reflexivity: $y = x \cdot 10^0$. Symmetry: $x = y \cdot 10^{-n}$. Transitivity: For $(x, y) \in T$ and $(y, z) \in T$, we have $y = x \cdot 10^n$ and $z = y \cdot 10^m$. Hence $z = x \cdot 10^{m + n}$. $\proofend$

**Problem 5**
Let L be the set of all nonvertical lines in the plane. Which of the following relations on L are equivalence relations? For those that are equivalence relations, what are the equivalence classes?
a) $R = \{(k, l) \in L \times L | \text{the lines k and l have the same slope}\}$.
b) $S = \{(k, l) \in L \times L | \text{the lines k and l are perpendicular}\}$.
c) $T = \{(k, l) \in L \times L | k \cap x = l \cap x \land k \cap y = l \cap y\}$, where x and y are the x-axis and the y-axis.
**Solution**
a)
R is reflexive, symmetric, and transitive - so an equivalence relation. The equivalence classes are groupings of lines with the same slope.

b)
S is not reflexive, and so not an equivalence relation.

c)
T is reflexive, symmetric, and transitive - so an equivalence relation. The equivalence classes are groupings of lines that intersect the x-axis and y-axis at the same points. $\proofend$

**Problem 6**
What assumption is needed to prove $P / B = \{P_d | d \in D\}$, where P is the set of all people, $B = \{(p, q) \in P \times P | \text{the person p has the same birthday as q}\}$, and $P_d = \{p \in P | \text{p was born on day d}\}$.
**Solution**
TO DO

**Problem 7**
Let T be the set of all triangles, and let $S = \{(s, t) \in T \times T | \text{the triangles s and t are similar}\}$. Verify that S is an equivalence relation.
**Solution**
Let $t \in T$. All triangles are similar to themselves, so that $tSt$. Hence S is reflexive. Now let $aSb$ for $a, b \in T$. We see that a and b are similar triangles, meaning b and a are similar triangles - $bSa$. Therefore, S is symmetric. Finally, let $iSj$ and $jSk$ for $i, j, k \in S$. It follows that i is similar to j and j is similar to k, making i similar to k. Hence S is transitive. Thus, S is an equivalence relation. $\proofend$

**Problem 8**
Prove Lemma. Suppose A is a set and F is a partition of A. Let $R = \bigcup_{X \in F}(X \times X)$. Then R is an equivalence relation on A. We call R the equivalence relation determined by F.
**Solution**
Let $x \in A$. Since F is a partition of A, $\bigcup F = A$, so $x \in \bigcup F$. Therefore, we can choose some $X \in F$ such that $x \in X$. But then $(x, x) \in X \times X$, so $(x, x) \in \bigcup_{X \in F} (X \times X) = R$. It follows that R is reflexive. Now let $nRm$ for $n, m \in A$. Since $R = \bigcup_{X \in F}(X \times X)$, there is some $O \in F$ such that $(n, m) \in O \times O$. Hence $n, m \in O$, meaning $(m, n) \in O \times O$ as well. Therefore, $(m, n) \in \bigcup_{X \in F} (X \times X) = R$. We conclude R is symmetric. Finally, let $aRb$ and $bRc$ for $a, b, c \in A$. Then there is some $Y \in F$ such that $(a, b) \in Y \times Y$ and some $Z \in F$ such that $(b, c) \in Z \times Z$. Hence $a, b \in Y$ and $b, c \in Z$. But F is a partition, and so pairwise disjoint. Since $b \in Y$ and $b \in Z$, it must be that $Y = Z$. Continuing, $a, b, c \in Y$ so that $(a, c) \in Y \times Y$. Because $Y \in F$ and $(a, c) \in Y \times Y$, $(a, c) \in \bigcup_{X \in F} (X \times X) = R$. Therefore, R is transitive. Thus, R is an equivalence relation. $\proofend$

**Problem 9**
Suppose R and S are equivalence relations on A and $A / R = A / S$. Prove that $R = S$.
**Solution**
Let $uRv$ for $u, v \in A$. Then $v \in [u]_R$. By definition $[u]_R \in A / R$, and since $A / R = A / S$ we have $[u]_R \in A / S$. From $[u]_R \in A / S$ and $v \in [u]_R$, we see that $vSu$ by definition. But S is symmetric, so $uSv$. Hence $R \subseteq S$. Now let $iSj$ for $i, j \in A$. Then $j \in [i]_S$. By definition $[i]_S \in A / S$, and since $A / R = A / S$ we have $[i]_S \in A / R$. From $[i]_S \in A / R$ and $j \in [i]_S$, we see that $jRi$ by definition. But R is symmetric, so $iRj$. Therefore, $S \subseteq R$. Thus, we conclude $R = S$. $\proofend$

**Problem 10**
Suppose R is an equivalence relation on A. Let $F = A / R$, and let S be the equivalence relation determined by F. In other words, $S = \bigcup_{X \in F} (X \times X)$. Prove that $S = R$.
**Solution**
Let $aSb$ for $a, b \in A$. Then there is some $X \in F$ such that $(a, b) \in X \times X$. By definition of $(a, b) \in X \times X$, $a, b \in X$. Hence $[b]_S = X$. Because $F = A / R$ and $X \in F$, we see that $X \in A / R$. In other words, $[b]_S \in A / R$. From $aSb$ we get $a \in [b]_S$. It follows that because $a \in [b]_S$ and $[b]_S \in A / R$ we have $aRb$. Therefore, $S \subseteq R$. Now let $uRv$ for $u, v \in A$. By definition, $[v]_R \in A / R$ and $u, v \in [v]_R$. But $F = A / R$ so $[v]_R \in F$. Hence $(u, v) \in [v]_R \times [v]_R$ with $[v]_R \in F$, meaning $(u, v) \in \bigcup_{X \in F} (X \times X) = S$. Therefore, $R \subseteq S$. Thus, $S = R$ $\proofend$

**Problem 11**
 