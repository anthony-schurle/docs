# Chapter 1: The Real And Complex Number Systems

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 1.1 The Real And Complex Number Systems

---

### Key Concepts

- **Field Notation**: $x - y := x + (-y), \frac{x}{y} := x \cdot \frac{1}{y}, x + y + z := (x + y) + z, xyz := (xy)z, x^2 := xx, 2x := x + x$.
- **Complex Number Notation**: $x_1 + x_2 + ... + x_n = \sum_{j=1}^n x_j$.

### Definitions

- **Order**: Let $S$ be a set. An order ($<$) on $S$ is a relation satisfying (i) $\forall x,y \in S$ one and only one of the following is true $x < y$, $y < x$, or $x = y$ and (ii) $\forall x,y,z \in S(x < y \land y < z \implies x < z)$. $\le$ denotes $<$ or $=$.
- **Bounded Above**: Suppose $S$ is an ordered set and $E \subseteq S$. If $\exists \beta \in S$ such that $\forall x \in E(x \le \beta)$, $E$ is said to be bounded above by upper bound $\beta$.
- **Bounded Below**: Suppose $S$ is an ordered set and $E \subseteq S$. If $\exists \beta \in S$ such that $\forall x \in E(x \ge \beta)$, $E$ is said to be bounded below by lower bound $\beta$.
- **Least Upper Bound (Supremum)**: Suppose $S$ is an ordered set, $E \subseteq S$, and $E$ is bounded above. If $\exists \alpha \in S$ such that (i) $\alpha$ is an upper bound of $E$ and (ii) if $\gamma < \alpha$ then $\gamma$ is not an upper bound of $E$, then $\alpha$ is called the least upper bound written as $\alpha = \sup E$.
- **Greatest Lower Bound (Infimum)**: Suppose $S$ is an ordered set, $E \subseteq S$, and $E$ is bounded below. If $\exists \alpha \in S$ such that (i) $\alpha$ is a lower bound of $E$ and (ii) if $\gamma > \alpha$ then $\gamma$ is not a lower bound of $E$, then $\alpha$ is called the greatest lower bound written as $\alpha = \inf E$.
- **Least Upper Bound Property**: An ordered set $S$ has the least upper bound property if $E \subseteq S$, $E \ne \emptyset$, and $E$ is bounded above, then $\sup E$ exists in $S$.
- **Field**: Set $F$ with two operations, called addition and multiplication satisfying the axioms (A), (M), and (D).
- **Ordered Field**: Field $F$ that is also an ordered set such that:
	- (i) $x + y < x + z$ if $x, y, z \in F$ and $y < z$.
	- (ii) $xy > 0$ if $x, y \in F$ and $x, y > 0$.
- **Positive**: $x \in F$ for field $F$ such that $x > 0$.
- **Negative**: $x \in F$ for field $F$ such that $x < 0$.
- **Extended Real Number System**: Field $\mathbb{R}$ with $- \infty$ and $+ \infty$ such that $\forall x \in \mathbb{R} (- \infty < x < + \infty)$. Not a field. "finite" distinguishes the reals from these new symbols. Conventions:
	- $x + \infty = \infty$, $x - \infty = - \infty$, $\frac{x}{+\infty} = \frac{x}{-\infty} = 0$ if $x \in \mathbb{R}$.
	- If $x > 0$, then $x \cdot (+\infty) = + \infty$, $x \cdot (- \infty) = -\infty$.
	- If $x < 0$, then $x \cdot (+ \infty) = - \infty$, $x \cdot (- \infty) = + \infty$. 
- **Complex Number**: Ordered pair $(a, b)$ of real numbers. $(x, y) = (t, j) \iff x = t \land y = j$. We then define $(x, y) + (t, j) = (x + t, y + j)$ and $(x, y)(t, j) = (xt - yj, xj + yt)$.
- **Imaginary Unit**: $i = (0, 1)$.
- **Conjugate**: If $a, b \in \mathbb{R}$ and $z = a + bi$, then $\overline{z} = a - bi$ is the conjugate of $z$. The numbers $a$ and $b$ are the real and imaginary part of $z$ respectively.
- **Real Part**: For $z = (a, b)$, the real part is defined by $Re(z) = a$.
- **Imaginary Part**: For $z = (a, b)$, the imaginary part is defined by $Im(z) = b$.
- **Absolute Value**: If $z$ is a complex number, then $|z| = (z\overline{z})^\frac{1}{2}$.
- **Euclidean k-Space**: For $R^k$, let an element (also called a vector/point) $x = (x_1, x_2, ..., x_k)$ for real numbers $x_i$ (called the coordinates of $x$). We define $x + y = (x_1 + y_1, x_2 + y_2, ..., x_k + y_k)$ and $\alpha x = (\alpha x_1, \alpha x_2, ..., \alpha x_k)$ for real $\alpha$. $0 = (0, ..., 0)$. Inner product defined by $x \cdot y = \sum_{i=1}^k x_iy_i$ and norm by $|x| = \sqrt{x \cdot x}$.
- **Cut**: Set $\alpha \subseteq Q$ such that:
	- $\alpha \ne \emptyset$ and $\alpha \ne Q$;
	- If $p \in \alpha$, $q \in Q$, and $q < p$, then $q \in \alpha$;
	- If $p \in \alpha$, then $p < r$ for some $r \in \alpha$.
	- $\alpha < \beta$ iff $\alpha \subset \beta$ (defines an ordering).
	- Satisfies LUB (consider $\bigcup A$ for $A \subset R$)
	- For $\alpha, \beta \in R$, we define $\alpha + \beta = \{r + s | r\in \alpha s \in \beta\}$.
	- $0^* = \{q < 0 | q \in Q\}$ is a cut and is $0$.
	- $-x = \{p | \exists r > 0 (-p - r \not \in x)\}$.
	- $1^* = \{p | p < 1\}$.
	- For $\alpha, \beta \in R^+$, $\alpha\beta = \{p | \forall r> 0 \in \alpha \forall s > 0 \in \beta (p \le rs)\}$.
	- $\alpha 0^* = 0^*\alpha = 0^*$ and $\alpha\beta = \begin{cases} (-\alpha)(-\beta) & \alpha < 0^*, \beta < 0^* \\ -[(-\alpha)\beta] & \alpha < 0^*, \beta > 0^* \\ -[\alpha(-\beta)] & \alpha > 0^*, \beta < 0^* \\ \alpha\beta & \alpha > 0^*, \beta > 0^* \end{cases}$.
	- $r^* = \{p | p < r\}$ for $r \in Q$. Satisfies $r^* + s^* = (r + s)^*$, $r^*s^* = (rs)^*$, and $r^* < s^* \iff r < s$.

### Axioms

- **(A) Axioms For Addition**:
	- (A1) If $x,y \in F$, then $x + y \in F$.
	- (A2) Addition is commutative.
	- (A3) Addition is associative.
	- (A4) $\exists 0 \in F$ such that $0 + x = x$ for every $x \in F$.
	- (A5) $\forall x \in F \exists (-x) \in F$ such that $x + (-x) = 0$.
- **(M) Axioms For Multiplication**:
	- (M1) $\forall x,y \in F(xy \in F)$.
	- (M2) Multiplication is commutative.
	- (M3) Multiplication is associative.
	- (M4) $\exists 1 \in F$ such that $1 \ne 0 \land 1x = x$ for every $x \in F$.
	- (M5) If $x \in F$ and $x \ne 0$, then $\exists \frac{1}{x} \in F$ such that $x \cdot \frac{1}{x} = 1$.
- **(D) Distributive Law**:
	- (D) $\forall x,y,z \in F(x(y + z) = xy + xz)$.

### Results & Proofs

**Theorem: Upper Bounds Related To Lower Bounds (LUB Implies GLB)**
Suppose $S$ is an ordered set with the least upper bound property, $B \subseteq S$, $B \ne \emptyset$, and $B$ is bounded below. Let $L$ be the set of all lower bounds of $B$. Then $\alpha = \sup L$ exists in $S$, and $\alpha = \inf B$. 

**Proposition: Expanded Addition Field Axioms**
The field axioms for addition further imply:
(a) $x + y = x + z \implies y = z$.
(b) $x + y = x \implies y = 0$.
(c) $x + y = 0 \implies y = -x$.
(d) $-(-x) = x$.

**Proposition: Expanded Multiplication Field Axioms**
The field axioms for multiplication further imply:
(a) $x \ne 0 \land xy = xz \implies y = z$.
(b) $x \ne 0 \land xy = x \implies y = 1$.
(c) $x \ne 0 \land xy = 1 \implies y = \frac{1}{x}$.
(d) $x \ne 0 \implies \frac{1}{\frac{1}{x}} = x$.

**Proposition: Field Axiom Implications**
The field axioms imply the following statements for any $x, y, z \in F$.
(a) $0x = 0$.
(b) $x \ne 0 \land y \ne 0 \implies xy \ne 0$.
(c) $(-x)y = -(xy) = x(-y)$.
(d) $(-x)(-y) = xy$.

**Proposition: Ordered Field Statements**
The following statements are true in every ordered field.
(a) If $x > 0$ then $-x < 0$, and vice versa.
(b) If $x > 0$ and $y < z$, then $xy < xz$.
(c) If $x < 0$ and $y < z$ then $xy > xz$.
(d) If $x \ne 0$ then $x^2 > 0$.
(e) If $0 < x < y$ then $0 < \frac{1}{y} < \frac{1}{x}$.

**Theorem: Real Field Existence**
There exists an ordered field $R$ which has the least upper bound property. Moreover, $R$ contains $\mathbb{Q}$ as a subfield. Members of $\mathbb{R}$ are called real numbers.

**Theorem: Real Field Properties**
(a) If $x, y \in R$ with $x > 0$, then there is a $n \in \mathbb{Z}^+$ such that $nx > y$. (Archimedean Property)
(b) If $x, y \in R$ with $x < y$, then there is a $p \in \mathbb{Q}$ such that $x < p < y$. ($\mathbb{Q}$ is called dense in $R$)

**Theorem: Nth Roots in The Reals**
$\forall x \in \mathbb{R}$ where $x > 0$ and $\forall n \in \mathbb{N}$ where $n > 0$, $\exists ! y \in \mathbb{R}^+$ such that $y^n = x$. $y$ denoted by $x^{\frac{1}{n}}$ or $\sqrt[n]{x}$.

**Corollary: Nth Roots Of Multiples**
If $a, b \in \mathbb{R}^+$ and $n \in \mathbb{Z}^+$, then $(ab)^{\frac{1}{n}} = a^{\frac{1}{n}}b^{\frac{1}{n}}$.

**Theorem: Complex Number Field**
All the complex numbers along with the definition of addition and multiplication, where $0 = (0, 0)$ and $1 = (1, 0)$, is a field.

**Theorem: Real Field As A Subfield Of Complex**
For any reals $a, b$ we have $(a, 0) + (b, 0) = (a + b, 0)$ and $(a, 0)(b, 0) = (ab, 0)$. (So we can identify $(a, 0)$ with the real number $a$)

**Theorem: Square Root Of $-1$**
$i^2 = -1$.

**Theorem: Complex Field Is Representative Of Imaginary Numbers**
If $a, b$ are real, then $(a, b) = a + bi$. 

**Theorem: Complex Properties**
If $z$ and $w$ are complex, then
a) $\overline{z + w} = \overline{z} + \overline{w}$.
b) $\overline{zw} = \overline{z} \cdot \overline{w}$.
c) $z + \overline{z} = 2Re(z), z - \overline{z} = 2iIm(z)$.
d) $z\overline{z}$ is real and positive (except when $z = 0$).

**Theorem: Absolute Value Properties**
Let $z$ and $w$ be complex numbers. Then
a) $|z| > 0$ unless $z = 0$, $|0| = 0$.
b) $|\overline{z}| = |z|$.
c) $|zw| = |z||w|$.
d) $|Re(z)| \le |z|$.
e) $|z + w|  \le |z| + |w|$.

**Theorem: Schwarz Inequality**
If $a_1, ..., a_n$ and $b_1, ..., b_n$ are complex numbers, then $|\sum_{j=1}^n a_j \overline{b_j}|^2 \le \sum_{j=1}^n |a_j|^2 \sum_{j=1}^n |b_j|^2$.

**Theorem: Properties Of The Euclidean Space**
Suppose $x, y, z \in R^k$ and $\alpha$ is real. Then
a) $|x| \ge 0$;
b) $|x| = 0 \iff x = 0$;
c) $|\alpha x| = |\alpha||x|$;
d) $|x \cdot y| \le |x||y|$;
e) $|x+y| \le |x| + |y|$;
f) $|x - z| \le |x - y| + |y - z|$.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
