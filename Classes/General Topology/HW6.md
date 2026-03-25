**Problem 2:**
a)
Let $p : X \to Y$ be a continuous map. Show that if there is a continuous map $f: Y \to X$ such that $p \circ f$ equals the identity map of Y, then p is a quotient map.
b)
If $A \subseteq X$, a retraction of X onto A is a continuous map $r : X \to A$ such that $r(a) = a$ for each $a \in A$. Show that a retraction is a quotient map.
**Solution:**
a)
Suppose $p^{-1}(V)$ is open in X. Since f is continuous, we see that $f^{-1}(p^{-1}(V))$ must be open in Y. But this is equivalent to $(p \circ f)^{-1}(V)$ open in Y and since $p \circ f$ is just the identity map of Y, $(p \circ f)^{-1}(V) = V$. Therefore, V open in Y. Now consider arbitrary $y \in Y$. Define $x = f(y)$. We see that $p(f(y)) = y$ by assumption and so p is surjective since y was arbitrary. $\blacksquare$

b)
Consider arbitrary $a \in A$. We see that $r(a) = a$ and since a was arbitrary, r is surjective. Consider arbitrary open set $r^{-1}(V)$ of X where V is a subset of A. By definition of the subspace topology, $r^{-1}(V) \cap A$ is open in A. By the definition of r, $r^{-1}(V) \cap A = V$ and so V is open in A. But $r^{-1}(V)$ was arbitrary, and so r is a quotient map. $\blacksquare$

Note the notation could have used more parenthesis here, so assume $\cup$ and $\cap$ take precedence over $\times$.
**Problem 3:**
Let $\pi_1 : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ be projection on the first coordinate. Let A be the subspace of $\mathbb{R} \times \mathbb{R}$ consisting of all points $x \times y$ for which either $x \ge 0$ or $y = 0$ (or both); let $q : A \to \mathbb{R}$ be obtained by restricting $\pi_1$. We can show that q is a quotient map that is neither open nor closed.
**Solution:**
First we show q is a quotient map. Consider arbitrary $x \in \mathbb{R}$ and define $(x, 0) \in A$. Then $q(x, 0) = x$ and so q is surjective because x was arbitrary. We now show continuity. Consider arbitrary open basis element $(a, b)$ of $\mathbb{R}$. Case 1: $a \ge 0$. Then $q^{-1}(a, b) = (a, b) \times \mathbb{R} = A \cap (a, b) \times \mathbb{R}$ which is open in A because $(a, b), \mathbb{R}$ both open in $\mathbb{R}$. Case 2: $a < 0$. Sub-Case 1: $0 \not \in (a, b)$. Then $q^{-1}(a, b) = (a, b) \times 0 = A \cap (a, b) \times \mathbb{R}$ which is open because both $(a, b), \mathbb{R}$ open in $\mathbb{R}$. Sub-Case 2: $0 \in (a, b)$. Then $q^{-1}(a,b) = [(a, 0) \times 0] \cup [[0, b) \times \mathbb{R}]$. Continuing, $q^{-1}(a,b) = [A \cap (a, 0) \times \mathbb{R}] \cup [A \cap (-1, b) \times (\mathbb{R} - \{0\})]$. But $(a, 0), (-1, b), \mathbb{R}, (\mathbb{R} - \{0\} = (-\infty, 0) \cup (0, \infty))$ all open in $\mathbb{R}$ so $q^{-1}(a,b)$ is a union of two open sets of A which is open. Thus, q is continuous. Define $h(x) = (x, 0)$ for $h : \mathbb{R} \to A$. Then notice $q \circ h (x) = x$ which is the identity of $\mathbb{R}$ and so by problem 2a, q is a quotient map. Now we show q is not open. Notice $[0, 1) \times (0, 1) = A \cap (-1, 1) \times (0, 1)$ is an open set of A where $(-1, 1) \times (0, 1)$ open in $\mathbb{R} \times \mathbb{R}$. But $q([0, 1) \times (0, 1)) = [0, 1)$ which is not open in $\mathbb{R}$ and so q is not open. Finally, we show q is not closed. Define $U = (-\infty, -1) \cup [1, \infty) \times \{0\}$ and see that $A - U = [0, 1) \times \mathbb{R} - \{0\} = A \cap (-\infty, 1) \times (-\infty, 0) \cup (0, \infty)$ which is open because $(-\infty, 1), (-\infty, 0) \cup (0, \infty)$ both open in $\mathbb{R}$. Then $q(U) = (-\infty, -1) \cup [1, \infty)$ and $\mathbb{R} - q(U) = [-1, 1)$ which is not open in $\mathbb{R}$. Therefore, $q(U)$ is not closed in $\mathbb{R}$. Thus, q is not a closed map. We have shown q is a quotient map that is neither open nor closed. $\blacksquare$

**Problem 4:**
a)
Define an equivalence relation on the plane $X = \mathbb{R}^2$ as follows:
$$
x_0 \times y_0 R x_1 \times y_1 \text{ if } x_0 + y_0^2 = x_1 + y_1^2
$$
Let X* be the corresponding quotient space. It is homeomorphic to a familiar space; what is it?
b)
Repeat (a) for the equivalence relation
$$
x_0 \times y_0 R x_1 \times y_1 \text{ if } x_0^2 + y_0^2 = x_1^2 + y_1^2
$$
**Solution:**
a)
Define the map $g : X \to \mathbb{R}$ where $g(x \times y) = x + y^2$. It suffices to show g is a quotient map, so by corollary 22.3 we see that $X*$ is homeomorphic to $\mathbb{R}$. Consider arbitrary $c \in \mathbb{R}$. Notice $g(c \times 0) = c + 0^2 = c$ and since c was arbitrary, g is surjective. g is a polynomial and so is continuous, and implies the topological definition of continuity as shown earlier in the book. Define $h : \mathbb{R} \to X$ by $h(x) = (x, 0)$. Notice $g \circ h (x) = x$ which is just the identity map of $\mathbb{R}$ and so g is a quotient map by problem 2a. Lastly, we verify the construction of X* as a collection of $\{g^{-1}(\{z\}) : z \in \mathbb{R}\}$. Consider arbitrary $z \in X*$. By construction of X*, $z = \{(x, y) : x + y^2 = c\}$ for some fixed c. But $\{(x, y) : x + y^2 = c\} = \{g^{-1}(\{c\}): c \in \mathbb{R}\}$ and since z was arbitrary, any element of $X*$ is defined by the construction of corollary 22.3.
$\blacksquare$

b)
Define the map $g : X \to [0, \infty)$ where $g(x \times y) = x^2 + y^2$. It suffices to show g is a quotient map, so by corollary 22.3 we see that $X*$ is homeomorphic to $[0, \infty)$. Consider arbitrary $c \in [0, \infty)$. Notice $g(\sqrt{c} \times 0) = c + 0^2 = c$ and since c was arbitrary, g is surjective. g is a polynomial and so is continuous, and implies the topological definition of continuity as shown earlier in the book. Define $h : [0, \infty) \to X$ by $h(x) = (\sqrt{x}, 0)$. Notice $g \circ h (x) = x$ which is just the identity map of $[0, \infty)$ and so g is a quotient map by problem 2a. Lastly, we verify the construction of X* as a collection of $\{g^{-1}(\{z\}) : z \in [0, \infty)\}$. Consider arbitrary $z \in X*$. By construction of X*, $z = \{(x, y) : x^2 + y^2 = c\}$ for some fixed c. But $\{(x, y) : x^2 + y^2 = c\} = \{g^{-1}(\{c\}): c \in [0, \infty)\}$ and since z was arbitrary, any element of $X*$ is defined by the construction of corollary 22.3.
$\blacksquare$

Problem 2 (Supp):
A topological group $G$ is a group that is also a topological space satisfying the $T_1$ axiom, such that the map of $G \times G$ into $G$ sending $x \times y$ into $x \cdot y$, and the map of $G$ into $G$ sending $x$ into $x^{-1}$, are continuous maps. Throughout the following exercises, let $G$ denote a topological group.
Show that the following are topological groups:
a) $(\mathbb{Z}, +)$
b) $(\mathbb{R}, +)$
c) $(\mathbb{R}_{+}, \cdot)$
d) $(S^1, \cdot)$, where $S^1$ is the space of all complex numbers $z$ for which $|z| = 1$.
e) $GL(n)$ under matrix multiplication. ($GL(n)$ is the set of all nonsingular $n \times n$ matrices, topologized by considering it as a subset of euclidean space of dimension $n^2$ in the obvious way).
Solution:
a)
We use the order topology. By Theorem 17.11, every simply ordered set is a Hausdorff space in the order topology and so the order topology on $\mathbb{Z}$ satisfies the $T_1$ axiom. Notice the order topology on $\mathbb{Z}$ coincides with its discrete topology as we can get any single point $n \in \mathbb{Z}$ by the basis element $(n - 1, n + 1)$ and unions of these single points create any subset of $\mathbb{Z}$. It follows that $h : \mathbb{Z} \to \mathbb{Z}$ defined by $h(x) = -x$ is trivially continuous because $h^{-1}(V)$ for any set $V$ of $\mathbb{Z}$ is open by the definition of the discrete topology and the definition of $h$. Define $g : \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z}$ by $g(x, y) = x + y$. Once again, this is trivially continuous because $g^{-1}(V)$ for any set $V$ of $\mathbb{Z}$ is open by the definition of the discrete topology, product topology, and the definition of $g$. Therefore, $(\mathbb{Z}, +)$ is a topological group. $\blacksquare$

b)
We use the order topology on $\mathbb{R}$. Since $\mathbb{R}$ is a simply ordered space, it is Hausdorff, which implies it satisfies the $T_1$ axiom. Define the inversion map $h : \mathbb{R} \to \mathbb{R}$ by $h(x) = -x$. This is a simple linear polynomial, and polynomials are everywhere continuous. Define the group operation map $g : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ by $g(x, y) = x + y$. This is a polynomial in two variables, which implies the topological definition of continuity as shown earlier in the book. Therefore, $(\mathbb{R}, +)$ is a topological group. $\blacksquare$

c)
We use the subspace topology inherited from $\mathbb{R}$. Since $\mathbb{R}$ is Hausdorff, any subspace of a Hausdorff space is also Hausdorff, so $\mathbb{R}_+$ satisfies the $T_1$ axiom. Define the inversion map $h : \mathbb{R}_+ \to \mathbb{R}_+$ by $h(x) = 1/x$. Since $0 \notin \mathbb{R}_+$, this rational function is continuous on its entire domain. Define the group operation map $g : \mathbb{R}_+ \times \mathbb{R}_+ \to \mathbb{R}_+$ by $g(x, y) = x \cdot y$. Since this is simply a polynomial in two variables restricted to the domain $\mathbb{R}_+ \times \mathbb{R}_+$, it is continuous. Therefore, $(\mathbb{R}_+, \cdot)$ is a topological group. $\blacksquare$

d)
Let $S^1$ have the subspace topology inherited from the complex plane $\mathbb{C}$ (which is homeomorphic to $\mathbb{R}^2$). Since $\mathbb{C}$ is a metric space and thus Hausdorff, the subspace $S^1$ is also Hausdorff, satisfying the $T_1$ axiom. Define the inversion map $h : S^1 \to S^1$ by $h(z) = z^{-1}$. Since elements in $S^1$ have a magnitude of 1 ($|z| = 1$), it follows that $z^{-1} = \bar{z}$ (the complex conjugate). Complex conjugation is simply a reflection across the real axis, which is an isometry and therefore continuous. Define the group operation map $g : S^1 \times S^1 \to S^1$ by $g(z_1, z_2) = z_1 \cdot z_2$. Complex multiplication is defined by polynomials combining the real and imaginary components, so it is continuous. Therefore, $(S^1, \cdot)$ is a topological group. $\blacksquare$

e)
We consider $GL(n)$ as a subspace of the Euclidean space $\mathbb{R}^{n^2}$. As a subspace of a Hausdroff space (order topology), $GL(n)$ is Hausdorff and therefore satisfies the $T_1$ axiom. Define the group operation $g : GL(n) \times GL(n) \to GL(n)$ by $g(A, B) = A \cdot B$. By the definition of matrix multiplication, each entry of the product matrix $A \cdot B$ is a finite sum of products of the entries of $A$ and $B$ (which forms a polynomial). Since polynomials are continuous, $g$ is continuous. Define the inversion map $h : GL(n) \to GL(n)$ by $h(A) = A^{-1}$. It is well known that $A^{-1} = \frac{1}{det(A)}C^T$ where $C^T$ is the coefficient matrix for A, so $A^{-1}$ is represented by  rational functions of the entries of $A$, where the denominator is always $\det(A)$. By the definition of $GL(n)$, $\det(A) \neq 0$, so the denominator is never zero on this subspace. Because rational functions with non-zero denominators are continuous, $h$ is continuous. Therefore, $GL(n)$ is a topological group. $\blacksquare$


Recall that if X is a topological space and G is a group, then a map G ˆ X Ñ X, denoted pg, xq ÞÑ g ¨ x is an group action if (a) g ¨ ph ¨ xq “ pghq ¨ x for all g, h P G and x P X, (b) e ¨ x “ x for all x P X, where e P G is the identity, and (c) Lg : X Ñ X defined by Lgpxq “ g ¨ x is continuous. If x P X, the orbit of x is the set G ¨ x “ tg ¨ x | g P Gu. The set of orbits, denoted X{G is the collection of subsets of X defined by X{G “ tG ¨ x | x P Xu.

**Problem 5:**
Suppose $G \times X \to X$ is a group action on a space $X$.
a) Prove that $L_g : X \to X$ is a homeomorphism for all $g \in G$.
b) Prove that $X / G$ is a partition of $X$.
c) Let $p : X \to X / G$ be the map sending $x$ to $G \cdot x$, and give $X / G$ the quotient topology. Prove that $p$ is an open map.
**Solution:**
a)
Consider an arbitrary $g \in G$. By the definition of a topological group action, the map $L_g : X \to X$ is continuous.  To show $L_g$ is a homeomorphism, we must find a continuous inverse as demonstrated by problem 2a. Consider $L_{g^{-1}} : X \to X$ which is continuous by the definition of a group action. By the properties of a group action, for any $x \in X$, $L_g(L_{g^{-1}}(x)) = g \cdot (g^{-1} \cdot x) = (gg^{-1}) \cdot x = e \cdot x = x$. Similarly, $L_{g^{-1}} \circ L_g(x) = g^{-1} \cdot (g \cdot x) = (g^{-1}g) \cdot x = e \cdot x = x$, showing $L_{g^{-1}}$ is a two-sided continuous inverse. Thus, $L_g$ is a homeomorphism. $\blacksquare$

b)
Consider arbitrary $x \in X$. By the definition of a group action, $e \cdot x = x$. Then $x \in G \cdot x$. This means every orbit is non-empty and every element of $X$ belongs to at least one orbit (their union is $X$). Next, suppose two orbits intersect, meaning $G \cdot x \cap G \cdot y \neq \emptyset$. Then there exists some element $z \in G \cdot x \cap G \cdot y$. By definition, there exist $g_1, g_2 \in G$ such that $z = g_1 \cdot x$ and $z = g_2 \cdot y$. Setting these equal yields $g_1 \cdot x = g_2 \cdot y$. Applying $g_1^{-1}$ to both sides gives $x = g_1^{-1} \cdot (g_2 \cdot y) = (g_1^{-1}g_2) \cdot y$. Now, consider any element $w \in G \cdot x$. Then $w = h \cdot x$ for some $h \in G$. Substituting our expression for $x$, we get $w = h \cdot ((g_1^{-1}g_2) \cdot y) = (h g_1^{-1}g_2) \cdot y$. Since $h g_1^{-1}g_2 \in G$, it follows that $w \in G \cdot y$, meaning $G \cdot x \subseteq G \cdot y$. By symmetry, $G \cdot y \subseteq G \cdot x$, so $G \cdot x = G \cdot y$. Thus, $X / G$ forms a valid partition of $X$. $\blacksquare$

c)
Suppose U is an open set of X. By the definition of the quotient topology, $p(U)$ is open in $X / G$ iff $p^{-1}(p(U))$ is open in $X$.  The set $p^{-1}(p(U))$ is the union of all orbits that intersect $U$: $p^{-1}(p(U)) = \bigcup_{g \in G} g \cdot U = \bigcup_{g \in G} L_g(U)$. From part (a), we know $L_g$ is a homeomorphism for every $g \in G$. Since homeomorphisms are open maps, $L_g(U)$ is an open set in $X$ for every $g \in G$. Because the arbitrary union of open sets is open in a topological space, $\bigcup_{g \in G} L_g(U)$ is an open set in $X$. Since $p^{-1}(p(U))$ is open in $X$, it follows by the quotient topology that $p(U)$ is open in $X / G$. Thus, $p$ is an open map. $\blacksquare$

**Problem 6:**
Consider the map $p : \mathbb{R} \to S^1$ given by $p(x) = (\cos(2\pi x), \sin(2\pi x))$, which is continuous. For $0 < \epsilon < 0.5$ and $t \in \mathbb{R}$, $p$ maps $(t - \epsilon, t + \epsilon)$ to the intersection of $S^1$ with the open sector between rays making angles $2\pi (t - \epsilon)$ and $2\pi(t + \epsilon)$, and is thus open.
a) Prove that $p$ is an open map.
b) Prove that $p_2 : \mathbb{R}^2 \to T^2 = S^1 \times S^1$, given by $p_2(x, y) = (p(x), p(y))$ is a continuous, open map.
**Solution:**
a)
To prove $p$ is an open map, it suffices to show that the image of any basis element of the standard topology on $\mathbb{R}$ is open in $S^1$. Consider an arbitrary open interval $(a, b) \subseteq \mathbb{R}$. We have two cases: Case 1: $b - a > 1$. Because the function $p(x)$ is periodic with period 1, the interval $(a, b)$ is longer than one full period. Thus, $p((a, b)) = S^1$. The entire space $S^1$ is always open in itself. Case 2: $b - a \le 1$. Let $t = (a + b) / 2$ and $\epsilon = (b - a) / 2$. Notice that because $b - a \le 1$, we have $0 < \epsilon \le 0.5$. The interval $(a, b)$ is exactly $(t - \epsilon, t + \epsilon)$. By the given property in the problem description, $p((t - \epsilon, t + \epsilon))$ is the intersection of $S^1$ with an open sector of $\mathbb{R}^2$. Since an open sector is an open set in $\mathbb{R}^2$, its intersection with $S^1$ is open in the subspace topology of $S^1$. Therefore, $p$ is an open map. $\blacksquare$

b)
First, we show $p_2$ is continuous. The map $p_2 : \mathbb{R}^2 \to S^1 \times S^1$ is defined by component functions $p_2(x, y) = (p(x), p(y))$. Since $p : \mathbb{R} \to S^1$ is given to be continuous, both component functions are continuous, making $p_2$ a continuous map. Next, we show $p_2$ is an open map. Once again, it suffices to show that the image of any basis element for the topology of the domain $\mathbb{R}^2$ is open in $T^2$. Consider an arbitrary basis element $U \times V \subseteq \mathbb{R}^2$. The image of this basis element under $p_2$ is: $p_2(U \times V) = p(U) \times p(V)$. From part (a), we know that $p$ is an open map, which means $p(U)$ is open in $S^1$ and $p(V)$ is open in $S^1$. By the definition of the product topology on $T^2 = S^1 \times S^1$, the Cartesian product of open subsets $p(U) \times p(V)$ is an open set in $T^2$. Therefore, $p_2$ is an open map. $\blacksquare$
