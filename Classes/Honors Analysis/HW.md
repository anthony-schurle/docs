# HW 1
1) Show that $\mathbb{R}$ with the relation $<$ is an ordered set. 
We first show that if $t_k(x) < t_k(y)$ for some $k$, then for any $j > k$ we have $t_j(x) < t_j(y)$. Let $x = x_m...x_1x'_1...$ and $y = y_n...y_1.y'_1...$. Then $t_k(x) = x_m(10^{m-1}) + ... + x_1 + ... + x'_k(10^{-k})$ and similar for $t_k(y)$. Hence $t_k(y) - t_k(x) \ge 10^{-k}$. But $t_{k+1}(x) \le t_k(x) + 9(10^{-k-1})$ and so $t_k(y) > t_{k+1}(x)$. Since $t_{k+1}(y) \ge t_{k}(y)$, we have $t_{k+1}(y) > t_{k+1}(x)$. By repeated application we get the desired conclusion. The problem then follows by this property, since we can set $\lambda = \max(k, j)$ if $t_k(x) < t_k(y)$ and $t_j(y) < t_j(z)$ to get $t_\lambda(x) < t_\lambda(y) < t_\lambda(z)$. $\proofend$

2) Let $x$ be a real number with $x > 0$. Show that there is a real number $y > 0$ with $x > y > 0$.
Let $x = x_m...x_1.x'_1...$. Then we set $y = x_m...x_2.x_1x'_1...$ and let $k=1$. Then $t_k(x) = x_m (10^{m-1}) + ... x_1 + x'_1(10^{-1})$ and $t_k(y) = x_m(10^{m-2}) + ... x_2 + x_1 (10^{-1})$. Clearly, $t_k(x) > t_k(y)$ as desired. $\proofend$

3) Prove well-ordering principle for natural numbers.
We use induction. Clearly, this is true for any set of length 1. Now assume that for any nonempty set of length $\le n$ this is true. Let $V$ be some arbitrary natural number set of length $n+1$. Pick $y \in V$, so that $V \backslash y$ has a smallest element $x$ by the hypothesis. If $x < y$, then $x$ is the smallest element of $V$. Else $y$ is. Hence $V$ contains a smallest element. $\proofend$

4) Use problem 2 to show that the ordered set $\mathbb{R}$ satisfies LUB.
Let $A$ be a nonempty subset of $\mathbb{R}$ bounded above by $x$. If $x$ is the least upper bound then we are done, so suppose not. 

5) 




# HW 2

1) Let $F$ be an ordered field. Show that there is a subset $S \subseteq F$ which is also an ordered field and an isomorphism $f$ from $\mathbb{Q}$ to $S$.
Define $f(\frac{m}{n}) = (m \cdot 1_F)(n \cdot 1_F)^{-1}$. Then $f(\frac{a}{b} + \frac{a'}{b'}) = f(\frac{ab' + a'b}{bb'}) = ((ab' + a'b)\cdot 1_F)(bb' \cdot 1_F)^{-1}$. But $((ab' + a'b)\cdot 1_F)(bb' \cdot 1_F)^{-1} = (ab' \cdot 1_F + a'b \cdot 1_F)(bb' \cdot 1_F)^{-1} = (ab' \cdot 1_F)(bb' \cdot 1_F)^{-1} + (a'b \cdot 1_F)(bb' \cdot 1_F)^{-1}$. Since $(bb' \cdot 1_F)^{-1} = (b \cdot 1_F)^{-1}(b' \cdot 1_F)^{-1}$, we have $(a \cdot 1_F)(b \cdot 1_F)^{-1} + (a' \cdot 1_F)(b' \cdot 1_F)^{-1}$ giving $f(\frac{a}{b}) + f(\frac{a'}{b'})$ as desired. Multiplication follows similarly. Suppose $\frac{o}{p} < \frac{o'}{p'}$. 

Now we show injectivity. Let $f(\frac{c}{d}) = f(\frac{c'}{d'})$. Then $(c \cdot 1_F)(d \cdot 1_F)^{-1} = (c' \cdot 1_F)(d' \cdot 1_F)^{-1}$. Then by inverse multiplication, $(c \cdot 1_F)(d' \cdot 1_F) = (c' \cdot 1_F)(d \cdot 1_F)$. Hence $(cd' \cdot 1_F) = (c'd \cdot 1_F)$, meaning $(cd' - c'd)1_F = 0_F$. 

2) Let $F_1$ and $F_2$ be ordered fields and let $f : F_1 \to F_2$ be an ordered field isomorphism. Let $A \subseteq F_1$ have a lub $\alpha$. Show that $f(A)$ has $f(\alpha)$ as its lub.
Consider $f(a) \in f(A)$. By definition, $a \le \alpha$. But then by the order preserving and 1-1 properties of $f$, we have $f(a) \le f(\alpha)$. Hence $f(\alpha)$ is an upper bound. Similarly, one can show that for any upper bound $\beta$, it must satisfy $f(\alpha) \le f(\beta)$. Thus, $f(\alpha)$ is the lub. $\proofend$

3) dhdnhdh

4) jjdjdj

5) Let $A$ be a finite nonempty set which we think of as an alphabet for a language. Every word in the language is a finite string $a_1a_2 . . . a_m$ which is a finite ordered list of elements of the alphabet. Suppose the language contains at least one word. Show that the set of words of the language is either finite or countably infinite.
It suffices to show that $\Sigma^*$, the set of all possible words, is countable since any language must be a subset of this set (and is either finite or an infinite subset and so countable). We can define some total ordering $D$ on $A$. Then enumerate the elements of $E^*$ by their lexicographical ordering, giving an enumeration. Hence $\Sigma^*$ is countable. $\proofend$

6) Show that the set of real numbers having two different decimal expansions (see problem set 1) is countably infinite.
Let $D$ be the set containing such numbers. We show that $D \subseteq Q$ and infinite, so countably infinite. Clearly, $D$ contains all numbers of the form $0.1, 0.01, 0.001, ...$ and so is infinite. Now consider any $d \in D$. If $d$ is identified with $0$, then this is clear. Else, $d$ is terminating and not identified with $0$. So $d = a_m ...a_1.b_1...b_k$. But this is identified with a rational number as well. Hence $D$ is countable. $\proofend$

7) Show that there is a bijection from $R$, the set of real numbers to the set of distinct decimal expansions.
Define $D$ to be the set of real numbers having two different decimal expansions, consisting of $d_0, d_1, d_2, ...$. Let $a_k, a_{k+1}$ correspond to the two decimal expansions of $d_k$ (assignment ordering being arbitrary). Finally, let $f(r) = \begin{cases} r & r \not \in D \\ a_{2k} & \exists k \in \mathbb{N} \cup \{0\} (r = d_{2k}) \\ a_{k+1} &  \exists k \in \mathbb{N} \cup \{0\} (r = d_{k + 1}) \end{cases}$. We show that $f$ is bijective. But this is mostly obvious. $\proofend$

8) Let $C$ be a countably infinite set, show that $\mathcal{P}(C)$, the collection of subsets of $C$ is uncountable.
Let $A \subseteq \mathcal{P}(C)$ be countable and consisting of $a_1, a_2, ...$. Since $C$ is countable, we can enumerate its elements as $c_1, c_2, ...$. Define $D = \{p \in C | \exists n \in \mathbb{N} (c_n \not \in a_n \land p = c_n)\}$. Clearly, $D \in \mathcal{P}(C)$ but $D \not \in A$. Hence every countable subset of $\mathcal{P}(C)$ is proper, making $\mathcal{P}(C)$ uncountable. $\proofend$

9) Show that for any set $S$ (it is even true for the empty set!) the collection of subsets of $S$ which we denote $\mathcal{P}(S)$ is not bijective to $S$.
Suppose it were. Then there is some bijection function $f : S \to \mathcal{P}(S)$. Define $D = \{s \in S | s \not \in f(s)\}$. Since $D \in \mathcal{P}(S)$ and $f$ is onto, there is some $s'$ such that $f(s') = D$. By construction of $D$, $s' \not \in D$. But then since $s' \not \in D = f(s')$, it must be that $s' \in D$ which is a contradiction. $\proofend$

10) Let $A$ and $B$ be sets. Let $A' \subseteq A$ and $B' \subseteq B$. Suppose there is a bijection from $A$ to $B'$ and that there is a bijection from $A'$ to $B$. Show that there is a bijection from $A$ to $B$.


# HW 3

1) Let $X$ be a metric space and $K$ a compact subset of $X$. Show that for any real number $\epsilon > 0$, the set $K$ is covered by a finite number of $\epsilon$-neighborhoods $N_\epsilon(x)$ of points of $x \in X$. If any set $E \subset X$ has the property that for any $\epsilon > 0$, it can be covered by a finite number of $\epsilon$-neighborhoods, we say that $E$ is totally bounded in $X$. So you are showing that compact sets in a metric space are totally bounded
Let $\epsilon > 0$. Clearly, $V = \{N_\epsilon(x) | x \in K\}$ forms an open cover of $K$. Since $K$ is compact, there is a finite set $U \subset V$ that forms an open cover of $K$. But this corresponds to $N_\epsilon(x)$ for finitely many $x \in K$. Hence $K$ is totally bounded. $\proofend$

2) We say that a metric space $X$ is complete if any sequence $\{x_j\}$ of points in $X$ has a limit point if it has the property that $d(x_j, x_k) < 2^{-\max(j, k)}$. Show that if $X$ is a complete metric space and $E \subset X$ is totally bounded then $E$ is compact iff $E$ is closed.
Suppose $X$ is complete and let $E \subset X$ be totally bounded and compact. 

3) Let $X$ be a metric space and let $K_1 \supset K_2 \supset K_3 . . .$ be a nested sequence of nonempty compact subsets of $X$, show that $\bigcap_{n=1}^\infty K_j \ne \emptyset$.
It suffices to show that for any collection of compact spaces $\{K_\alpha\}$, if a finite subcollection intersection is non-empty, then we get $\bigcap K_n$ not empty. Define $G_n = K_n^c$, which is clearly open. Now suppose that the conclusion is false, so $K_t$ does not have a point in every $K_\alpha$. Then the collection of all $G_n$ forms an open cover of $K_1$. But $K_t$ is compact so there is a finite covering of $G_{\alpha_1}, G_{\alpha_2}, ..., G_{\alpha_n}$. Hence $K_1 \cap G_{\alpha_1} \cap ... \cap G_{\alpha_n}$ is empty, a contradiction. $\proofend$ 

4) jsjsjsjs

5) Let X be a compact metric space and let F be a collection of closed subsets of X with the property that any finite intersection of the sets of F is nonempty, show that there must be a point of X in all sets F ∈ F.
Every element of that collection is compact, since they are closed subsets of a compact space. Since any finite intersection is non-empty, we refer to problem 3 to see that $\bigcap F_i$ is not empty. But $\bigcap F_i \subseteq X$ and so $x \in \bigcap F_i$ also satisfies $x \in X$. $\proofend$

6) Let X and Y be metric spaces. Let dX be the metric on X and dy be the metric on Y . Define the product of X and Y to be the set X × Y of ordered pairs (x, y) with x ∈ X and y ∈ Y . Define the metric dX×Y ((x1, y1),(x2, y2)) = dX(x1, x2) + dY (y1, y2). Show that dX×Y is a metric and thus X × Y a metric space under this metric.
Fairly trivial, just unpack the definition of metric in $X$ and $Y$. $\proofend$

7) With X and Y as in problem 6, let E ⊂ X be compact and let K = E × S with S ⊂ Y . Show that K is compact in X × Y if and only if S is compact in Y .
Suppose $S$ is compact in $Y$. Then consider any limit point $(q, p)$ of $E \times S$. 

8) Let X be a compact metric space. Show that there is a countable subset C of X which is dense in X
Define $C = C_1 \cup C_2 \cup C_3 \cup ...$. which is countable since it is a countable union of finite elements. By problem 1, we can cover $X$ by finite $N_{\frac{1}{n}}(x)$. We let $x \in C_n$ if $x$ is the center of one of those neighborhoods. Now let $y \in X$. If $y \in C$ we are done so suppose not. Consider any $N_\epsilon(y)$. Choose $N$ so that $\frac{1}{N} < \epsilon$. Then $C_N$  intersects $N_\epsilon(y)$ since the open balls of the points in $C_N$ cover $X$ and have radius less than $\epsilon$. $\proofend$

9) jdjdj
   
   
   
   
