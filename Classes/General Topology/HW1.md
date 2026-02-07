Let X be a topological space; let A be a subset of X. Suppose that for each x in A
there is an open set U containing x such that $U \subseteq A$. Show that A is open in X.

Define topology $\Gamma$ of the set X and the set $Z := \{U \in \Gamma : U \subseteq A\}$. By definition of a topology, $\bigcup Z \in \Gamma$. Now we show $\bigcup Z = A$. ($\implies$) Let a be arbitrary and suppose $a \in A$. By our hypothesis, there is an open set Y where $a \in Y$ and $Y \subseteq A$. It follows that $Y \in Z$. But then because $a \in Y$ and $Y \in Z$ for arbitrary a, we see that $A \subseteq \bigcup Z$. ($\Longleftarrow$) Let a be arbitrary and suppose $a \in \bigcup Z$. Then there is some $Y \in Z$ where $a \in Y$. For $Y \in Z$, it must be that Y is an open set with $Y \subseteq A$. It follows that $a \in A$. But a was arbitrary, so $\bigcup Z \subseteq A$. Therefore, we have shown $\bigcup Z  = A$. We know $\bigcup Z \in \Gamma$ and so $A \in \Gamma$. Thus, A is open in X. **Q.E.D**

Show that the collection $\Gamma_c$ given in Example 4 of §12 is a topology on the set X ($\Gamma_c = \{U : U \subseteq X \land (X - U = X \lor X - U \text{ is countable}\}$). Is the collection $\Gamma_{\infty} = \{U : X - U \text{ is infinite or empty or all of X}\}$ a topology on X?

Trivially, $\emptyset \subseteq X$ and $X - \emptyset = X$ and so $\emptyset \in \Gamma_c$. Also trivially, $X \subseteq X$ and $X - X = \emptyset$ and because the empty set is finite, $X \in \Gamma_c$. Define arbitrary non-empty family $\{U_\alpha \}_{\alpha \in J} \subseteq \Gamma_c$. Notice, $X - \bigcup_{\alpha \in J}U_\alpha = \bigcap_{\alpha \in J}(X - U_{\alpha})$. But $X - U_{\alpha}$ is countable or X itself for all $\alpha \in J$ according to our definition. Two cases exist, there is some $\alpha_0 \in J$ such that $X - U_{\alpha_0}$ is countable or $\forall \alpha \in J (X - U_\alpha)$ is X itself. Case 1: there is some $\alpha_0 \in J$ such that $X - U_{\alpha_0}$ is countable. It follows that $\bigcap_{\alpha \in J}(X - U_{\alpha}) \subseteq X - U_{\alpha_0}$ and so $\bigcap_{\alpha \in J}(X - U_{\alpha})$ is also countable. Case 2: $\forall \alpha \in J (X - U_\alpha)$ is X itself. But this just means $\bigcap_{\alpha \in J}(X - U_{\alpha}) = X$. Therefore, $\bigcap_{\alpha \in J}(X - U_{\alpha})$ is either countable or X itself and so it is contained in $\Gamma_c$ by definition. Suppose $\{U_\alpha \}_{\alpha \in J} \subseteq \Gamma_c$ was finite. Notice $X - \bigcap_{\alpha \in J}U_\alpha = \bigcup_{\alpha \in J}(X - U_\alpha)$. Two cases exist, there is some $\alpha_0 \in J$ such that $X - U_{\alpha_0}$ is X or $\forall \alpha \in J (X - U_\alpha)$ is countable. Case 1: there is some $\alpha_0 \in J$ such that $X - U_{\alpha_0}$ is X. We know $\forall \alpha \in J (X - U_\alpha \subseteq X)$ and so $\bigcup_{\alpha \in J}(X - U_\alpha) = X$. Case 2: $\forall \alpha \in J (X - U_\alpha)$ is countable. It follows that the finite union of countable sets is also countable. Therefore, we know $\bigcup_{\alpha \in J}(X - U_\alpha)$ is either X itself or countable and so in $\Gamma_c$. Thus, we have shown $\Gamma_c$ is a topology.

False. Suppose $X = \mathbb{R}$. It follows that $\emptyset, \mathbb{R} \in \Gamma_\infty$. By definition, we see that $\mathbb{R}^+ \in \Gamma_\infty$ since $\mathbb{R} - \mathbb{R}^+$ is infinite. Similarly, $\mathbb{R}^- \in \Gamma_\infty$. Now define the family $\{\mathbb{R}^+, \mathbb{R}^-\} \subseteq \Gamma_\infty$. Notice, $\mathbb{R} - \bigcup \{\mathbb{R}^+, \mathbb{R}^-\} = \{0\}$ which is finite, not empty, and not equal to X meaning $\bigcup \{\mathbb{R}^+, \mathbb{R}^-\} \not \in \Gamma_\infty$.  **Q.E.D**

Consider the following topologies on $\mathbb{R}$:
$\Gamma_1 = \text{standard topology}$,
$\Gamma_2 = \text{topology of } \mathbb{R}_K$,
$\Gamma_3 = \text{finite complement topology}$,
$\Gamma_4 = \text{upper limit topology, having all sets (a, b] as basis}$,
$\Gamma_5 = \text{topology having all sets } (- \infty, a) = \{x : x < a\} \text{ as basis}$.
Determine which of the others, for each, it contains.

$(\Gamma_1)$

Trivially $\Gamma_1$ contains itself.

By Lemma 13.4, $\Gamma_2$ is not contained within.

Let $U = \mathbb{R} \setminus F$ be an arbitrary basis element for $\Gamma_3$, where $F$ is finite, containing element $x \in \mathbb{R}$. Since $F$ is finite and $x \notin F$, we can choose $\epsilon$ smaller than the distance from $x$ to the nearest point in $F$. The basis element $(x - \epsilon, x + \epsilon)$ for $\Gamma_1$ contains $x$ and lies in $U$. Therefore, $\Gamma_1$ contains $\Gamma_3$.

Given the basis element $(d, x]$ for $\Gamma_4$, we see there is no open interval that contains $x$ and lies in $(d, x]$. Therefore, $\Gamma_4$ is not contained within $\Gamma_1$.

Let $(-\infty, a)$ be arbitrary basis element for $\Gamma_5$ containing element $x \in \mathbb{R}$. The basis element $(x - 1, a)$ for $\Gamma_1$ contains $x$ and lies in $(-\infty, a)$. Therefore, $\Gamma_1$ contains $\Gamma_5$.

($\Gamma_2$) 
By Lemma 13.4, $\Gamma_1$ is contained within.

Trivially $\Gamma_2$ contains itself.

Since $\Gamma_2$ contains $\Gamma_1$ and $\Gamma_1$ contains $\Gamma_3$, it follows that $\Gamma_2$ contains $\Gamma_3$.

Given $x = 1$ and the basis element $(a, x]$ for $\Gamma_4$, we see there is no open interval that contains $x$ and lies in $(a, x]$. Also, since $1 \in K$, there is no basis element of the form $(c, d) \setminus K$ that includes $x$. Therefore, $\Gamma_4$ is not contained in $\Gamma_2$.

Since $\Gamma_2$ contains $\Gamma_1$ and $\Gamma_1$ contains $\Gamma_5$, it follows that $\Gamma_2$ contains $\Gamma_5$.

($\Gamma_3$) 
Let $(x - 1, x + 1)$ be a basis element of $\Gamma_1$ containing $x$. No basis element of $\Gamma_3$ lies in $(x - 1, x + 1)$ because any open set in $\Gamma_3$ is either $\mathbb{R}$ itself or has finite complement, and $(x - 1, x + 1)$ has infinite complement. Therefore, $\Gamma_3$ does not contain $\Gamma_1$.

Since $\Gamma_3$ does not contain $\Gamma_1$ and $\Gamma_1$ is contained in $\Gamma_2$, it follows that $\Gamma_3$ does not contain $\Gamma_2$.

Trivially $\Gamma_3$ contains itself.

Let $(a, x]$ be a basis element of $\Gamma_4$ containing $x$. No basis element of $\Gamma_3$ lies in $(a, x]$ because any open set in $\Gamma_3$ is either $\mathbb{R}$ itself or has finite complement, and $(a, x]$ has infinite complement. Therefore, $\Gamma_3$ does not contain $\Gamma_4$.

Let $(-\infty, a)$ be a basis element of $\Gamma_5$ containing $x$. No basis element of $\Gamma_3$ lies in $(-\infty, a)$ because any open set in $\Gamma_3$ is either $\mathbb{R}$ itself or has finite complement, and $(-\infty, a)$ has infinite complement. Therefore, $\Gamma_3$ does not contain $\Gamma_5$.

($\Gamma_4$)
Let $(a, b)$ be arbitrary basis element for $\Gamma_1$ containing element $x \in \mathbb{R}$. The basis element $(a, x]$ for $\Gamma_4$ contains x and lies in $(a, b)$. Therefore, $\Gamma_4$ contains $\Gamma_1$.

Consider the basis element $(-1, 1) \setminus K$ for $\Gamma_2$ containing element $x = 0$. Any basis element of $\Gamma_4$ containing $0$ has the form $(a, b]$ where $a < 0 \leq b$. For $(a, b] \subseteq (-1, 1) \setminus K$, we need $(a, b] \cap K = \emptyset$. Since all elements of $K$ are positive and $b > 0$, we have $K \cap (0, b] \neq \emptyset$ for any $b > 0$ (as $K$ contains $\frac{1}{n}$ for arbitrarily large $n$). Therefore, $(a, b]$ contains elements of $K$, so $(a, b] \not\subseteq (-1, 1) \setminus K$. Thus, $\Gamma_4$ does not contain $\Gamma_2$.

Since $\Gamma_4$ contains $\Gamma_1$ and $\Gamma_1$ contains $\Gamma_3$, it follows that $\Gamma_4$ contains $\Gamma_3$.

Trivially, $\Gamma_4$ contains itself.

Let $(-\infty, a)$ be an arbitrary basis element of $\Gamma_5$ that contains $x \in \mathbb{R}$. Then there is some basis element of $\Gamma_4$, $(x - 1, x]$, that contains $x$ and lies in $(-\infty, a)$. Therefore, $\Gamma_4$ contains $\Gamma_5$.

($\Gamma_5$) 
Let $(a, x + 1)$ be a basis element of $\Gamma_1$ containing $x$. Any basis element of $\Gamma_5$ containing $x$ has the form $(-\infty, b)$ where $b > x$. But $(-\infty, b)$ contains all negative numbers and thus does not lie in $(a, x + 1)$. Therefore, $\Gamma_5$ does not contain $\Gamma_1$.

Since $\Gamma_5$ does not contain $\Gamma_1$ and $\Gamma_1$ is contained in $\Gamma_2$, it follows that $\Gamma_5$ does not contain $\Gamma_2$.

Consider $U = \mathbb{R} \setminus {0}$, which is open in $\Gamma_3$. For any $x > 0$ in $U$, any basis element $(-\infty, a)$ of $\Gamma_5$ containing $x$ must have $a > x > 0$. But then $0 \in (-\infty, a)$, so $(-\infty, a)$ does not lie in $U$. Therefore, $\Gamma_5$ does not contain $\Gamma_3$.

Since $\Gamma_5$ does not contain $\Gamma_1$ and $\Gamma_1$ is contained in $\Gamma_4$, it follows that $\Gamma_5$ does not contain $\Gamma_4$.

Trivially, $\Gamma_5$ contains itself.
**Q.E.D**

Show that the collection $\{\{a\} \times (b, c) \subseteq \mathbb{R}^2 : a,b,c \in \mathbb{R}\}$ of vertical intervals in the plane is a basis for a topology on $\mathbb{R}^2$.

Lets call $\beta := \{\{a\} \times (b, c) \subseteq \mathbb{R}^2 : a,b,c \in \mathbb{R}\}$. Define arbitrary $(f, g) \in \mathbb{R}^2$. Let $B = \{f\} \times (g - 1, g + 1)$. It follows that $B \subseteq \mathbb{R}^2$ and so $B \in \beta$. But $(f, g) \in B$ also and since $(f, g)$ was arbitrary, $\forall x \in \mathbb{R}^2 \exists B \in \beta (B \subseteq \mathbb{R}^2 \land x \in B)$. 
Define arbitrary $(f, g) \in \mathbb{R}^2$ and $B_1, B_2 \in \beta$. Suppose $(f, g) \in B_1 \cap B_2$. It follows that $B_1 = \{f\} \times (y, z)$ for some y and z and $B_2 = \{f\} \times (n, m)$ for some n and m such that $(f, g) \in \{f\} \times (y, z)$ and $(f, g) \in \{f\} \times (n, m)$. Let $B_3 = \{f\} \times (max(y, n), min(z, m))$. Notice, $B_3 \in \beta$. Also, by definition, $y < g < z$ and $n < g < m$, so $max(y, n) < g < min(z, m)$ giving $(f, g) \in B_3$. Suppose arbitrary $(j, k) \in B_3$. It follows that $j = f$ and $max(y, n) < k < min(z, m)$. Then $y < k < z$ and $n < k < m$ indicating $(j, k) \in B_1 \cap B_2$. But $(j, k)$ was arbitrary and so $B_3 \subseteq B_1 \cap B_2$. Therefore, we have shown $\forall x \in \mathbb{R}^2 \forall B_1, B_2 \in \beta (x \in B_1 \cap B_2 \implies \exists B_3 \in \beta (x \in B_3 \land B_3 \subseteq B_1 \cap B_2))$. Thus, we have shown that $\beta$ is a basis for a topology on $\mathbb{R}^2$. **Q.E.D**

Show that if A is a basis for a topology on X, then the topology generated by A equals the intersection of all topologies on X that contain A. Prove the same if A is a subbasis.

Suppose A is a basis for a topology on X. It follows that $\Gamma := \{U \subseteq X : \forall x \in U\exists a \in A (x \in a \land a \subseteq U)\}$ is the topology generated by A. Now define $\Gamma_A := \{\lambda : (X, \lambda) \text{ is a topological space} \land A \subseteq \lambda\}$. ($\implies$) Suppose $y \in \Gamma$ for arbitrary y and let $\Gamma_{A_0} \in \Gamma_A$ be arbitrary. By Lemma 13.1, there exists and index set $I$ and a family $\{A_\alpha\}_{\alpha \in I} \subseteq A$ such that $y = \bigcup_{\alpha \in I} A_\alpha$. But $\bigcup_{\alpha \in I} A_\alpha \in \Gamma_{A_0}$ because $A \subseteq \Gamma_{A_0}$ and by applying axiom 2 of topologies to the family $\{A_\alpha\}_{\alpha \in I}$. Therefore, $y \in \Gamma_{A_0}$, and since y and $\Gamma_{A_0}$ was arbitrary, $\Gamma \subseteq \bigcap \Gamma_A$. ($\Longleftarrow$) Suppose $y \in \bigcap \Gamma_A$ for arbitrary y. It follows that $y \in \Gamma$ since $\Gamma \in \Gamma_A$. Therefore, because y was arbitrary, $\bigcap \Gamma_A \subseteq \Gamma$. Thus, if A is a basis for a topology on X, then the topology generated by A equals the intersection of all topologies on X that contain A.
Suppose A is a subbasis for a topology on X. Define $\beta$ as the collection of all finite intersections of elements of A. Given $x \in X$, it belongs to an element of A and hence to an element of $\beta$. Let $B_1 = A_1 \cap ... \cap A_m$ and $B_2 = A_1' \cap ... \cap A_n'$ be two elements of $\beta$. Their intersection is also a finite intersection of elements of A, so it belongs to $\beta$. Thus, $\beta$ is a basis for a topology on X. Now let $\Gamma$ be the topology generated by the subbasis A, which equals the topology generated by the basis $\beta$. Define $\Gamma_A := \{\lambda : (X, \lambda) \text{ is a topological space} \land A \subseteq \lambda\}$. Let $\lambda \in \Gamma_A$ be arbitrary. Since $A \subseteq \lambda$ and $\lambda$ is a topology, all finite intersections of elements of A belong to $\lambda$ by axiom 3 of topologies. Therefore, $\beta \subseteq \lambda$. By the basis case already proven, the topology generated by $\beta$ equals the intersection of all topologies containing $\beta$. Since $\beta \subseteq \lambda$ for all $\lambda \in \Gamma_A$, we have $\Gamma \subseteq \bigcap \Gamma_A$. Conversely, $\Gamma \in \Gamma_A$ since $A \subseteq \beta \subseteq \Gamma$, so $\bigcap \Gamma_A \subseteq \Gamma$. Thus, if A is a subbasis for a topology on X, then the topology generated by A equals the intersection of all topologies on X that contain A. **Q.E.D**
