**Problem 1**
For $A \subseteq G$, define its normalizer by $N_G(A) = \{g \in G | gAg^{-1} = A\}$.
a) If $H \le G$, prove $H \le N_G(H)$.
b) Give an example of group $G$ and $A \subseteq G$ for which $A \not \subseteq N_G(A)$.
c) If $\phi : G \to K$ is a homomorphism, prove $\ker \phi \unlhd G$.
d) Prove $\text{im} \phi \le K$.
e) Must $\text{im} \phi \unlhd K$? Justify.
**Solution**
a)
Suppose so. Then $H \ne \emptyset$ and $g_1, g_2 \in H \implies g_1g_2^{-1} \in H$. We show that $H \subseteq N_G(H)$. Consider any $h \in H$. See that $hH = eH = H$ since $h \in H = eH$. It also follows that $Hh^{-1} = He^{-1} = H$ because $hH = eH$. Therefore, $hHh^{-1} = H$ for any $h \in H$ meaning $h \in N_G(H)$. Thus, $H \le N_G(H)$. $\proofend$ 

b)
Set $G = GL_2(\mathbb{R})$ and $A = \{\begin{pmatrix} 0 & 1 \\ 1 & 0\end{pmatrix}, \begin{pmatrix} 1 & 2 \\ 3 & 4\end{pmatrix}\} \subset G$. We see that $\begin{pmatrix} 0 & 1 \\ 1 & 0\end{pmatrix}^{-1} = \begin{pmatrix} 0 & 1 \\ 1 & 0\end{pmatrix}$. But $\begin{pmatrix} 0 & 1 \\ 1 & 0\end{pmatrix} \begin{pmatrix} 1 & 2 \\ 3 & 4\end{pmatrix} \begin{pmatrix} 0 & 1 \\ 1 & 0\end{pmatrix} = \begin{pmatrix} 0 & 1 \\ 1 & 0\end{pmatrix} \begin{pmatrix} 2 & 1 \\ 4 & 3\end{pmatrix} = \begin{pmatrix} 4 & 3 \\ 2 & 1\end{pmatrix} \not \in A$. Hence $\begin{pmatrix} 0 & 1 \\ 1 & 0\end{pmatrix} \not \in N_G(A)$ giving $A \not \subseteq N_G(A)$. $\proofend$

c)
Suppose so. Since $\phi(e_G) = e_K$, $\ker \phi \ne \emptyset$ (where $e_G$ is the identity in $G$ and $e_K$ the identity in $K$). Let $g_1, g_2 \in \ker \phi$. Then $\phi(g_1 g_2^{-1}) = \phi(g_1)\phi(g_2^{-1}) = e_K \phi(g_2)^{-1} = e_K^{-1} = e_K$ meaning $g_1g_2^{-1} \in \ker \phi$ and so $\ker \phi \le G$. Let $g \in G$. Now take $gkg^{-1} \in g \ker \phi g^{-1}$ for some $k \in \ker \phi$. See that $\phi(gkg^{-1}) = \phi(g)\phi(k)\phi(g^{-1}) = \phi(g)e_K\phi(g)^{-1} = \phi(g)\phi(g)^{-1} = e_K$ giving $gkg^{-1} \in \ker \phi$. Therefore, $g\ker \phi g^{-1} \subseteq \ker \phi$. Setting $g = g^{-1}$, we get $g^{-1}\ker \phi g \subseteq \ker \phi$. Continuing, $g(g^{-1}\ker \phi g)g^{-1} \subseteq g \ker \phi g^{-1}$. But $g(g^{-1}\ker \phi g)g^{-1} = \{g(g^{-1}j g)g^{-1} | j \in \ker \phi\} = \ker \phi$. Hence $\ker \phi \subseteq g \ker \phi g^{-1}$ giving $\ker \phi = g \ker \phi g^{-1}$ for all $g \in G$ so that $\ker \phi \unlhd G$. $\proofend$

d)
Taking $e_G$ and $e_K$ from part (c) to have their respective meanings. We see $\phi(e_G) = e_K$ and so $\text{im} \phi \ne \emptyset$. Let $k_1, k_2 \in \text{im} \phi$. Then $\phi(g_1) = k_1$ and $\phi(g_2) = k_2$ for some $g_1, g_2 \in G$. It follows that $g_1g_2^{-1} \in G$ so that $\phi(g_1g_2^{-1}) = \phi(g_1)\phi(g_2^{-1}) = k_1 \phi(g_2)^{-1} = k_1k_2^{-1}$. Hence $k_1k_2^{-1} \in \text{im} \phi$. Thus, $\text{im} \phi \le K$. $\proofend$

e)
No. Consider $\phi : GL_2(\mathbb{R}) \to GL_3(\mathbb{R})$ where $\phi(\begin{pmatrix} a & b \\ c & d\end{pmatrix}) = \begin{pmatrix} a & b & 0 \\ c & d & 0 \\ 0 & 0 & 1 \end{pmatrix}$ (the determinant of this matrix is non-zero by construction). First we verify this is a homomorphism. All $GL_n(\mathbb{R})$ for $n \in \mathbb{N}$ are groups. Also, $\phi$ is clearly well defined since if $\begin{pmatrix} a & b \\ c & d\end{pmatrix} = \begin{pmatrix} e & f \\ g & h\end{pmatrix}$ then $a=e, b=f, c=g, d=h$. Lastly, $\phi(\begin{pmatrix} a & b \\ c & d\end{pmatrix}\begin{pmatrix} e & f \\ g & h\end{pmatrix}) = \phi(\begin{pmatrix} ae + bg & af + bh \\ ce + dg & cf + dh \end{pmatrix})$ and $\phi(\begin{pmatrix} a & b \\ c & d\end{pmatrix})\phi(\begin{pmatrix} e & f \\ g & h\end{pmatrix}) = \begin{pmatrix} a & b & 0 \\ c & d & 0 \\ 0 & 0 & 1\end{pmatrix} \begin{pmatrix} e & f & 0 \\ g & h & 0 \\ 0 & 0 & 1\end{pmatrix} = \begin{pmatrix} ae + bg & af + bh & 0 \\ ce + dg & cf + dh & 0 \\ 0 & 0 & 1\end{pmatrix} = \phi(\begin{pmatrix} ae + bg & af + bh \\ ce + dg & cf + dh \end{pmatrix})$. Hence $\phi$ is a homomorphism. But now take $M = \phi(\begin{pmatrix} 0 & 1 \\ 1 & 0\end{pmatrix}) = \begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1\end{pmatrix}$. Notice $W = \begin{pmatrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 0\end{pmatrix} = \begin{pmatrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 0\end{pmatrix}^{-1} = W^{-1}$. Computing $WMW^{-1}$ for $M \in \text{im} \phi$ and $W \in GL_3(\mathbb{R})$ gives $WMW^{-1} = \begin{pmatrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 0\end{pmatrix}\begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1\end{pmatrix}\begin{pmatrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 0\end{pmatrix} = \begin{pmatrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 0\end{pmatrix}\begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0\end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 1 & 0\end{pmatrix} \not \in \text{im} \phi$. Thus, $\text{im} \phi$ is not normal. $\proofend$

**Problem 2**
Let $G$ be a finite group, and let $S_G$ be the group of all permutations of the set $G$, with compositions as its operation. For $g \in G$, define $\pi(g) : G \to G$ where $\pi(g)(y) = gy$.
a) Prove that $\pi(g)$ is a permutation of $G$ for every $g \in G$.
b) Prove that $\pi : G \to S_G$ is an injective group homomorphism.
c) Suppose $x \in G$ has order $n$ and $|G| = nm$. Prove that $\pi(x)$ is a product of $m$ disjoint n-cycles, counting fixed points as 1-cycles.
d) Deduce that $\pi(x)$ is odd iff $n$ is even and $m$ is odd.
**Solution**
a)
Fix $g$. Suppose $\pi(g)(g_1) = \pi(g)(g_2)$. Then $gg_1 = gg_2$. Hence $g_1 = g_2$. So $\pi(g)$ is injective. Now let $g' \in G$. We see that ($g \in G$ implies $g^{-1} \in G$) $\pi(g)(g^{-1}g') = gg^{-1}g' = e_Gg' = g'$ for identity $e_G$, meaning $\pi(g)$ is surjective. Thus, $\pi(g)$ is a permutation for all $g \in G$. $\proofend$

b)
We first check that $\pi$ is well defined. Suppose $g_1 = g_2 \in G$. Then for all $g \in G$ we have $\pi(g_1) = g_1g = g_2g = \pi(g_2)$. Now we check injectivity. Suppose $\pi(k_1) = \pi(k_2)$ for $k_1, k_2 \in G$. Clearly, for $e_G \in G$ we get $\pi(k_1)(e_G) = k_1$ and $\pi(k_2)(e_G) = k_2$. Hence $k_1 = k_2$. Therefore, $\pi$ is injective. Take $\lambda_1, \lambda_2 \in G$. Continuing ($\forall p \in G$), $\pi(\lambda_1 \lambda_2)(p) = \lambda_1 (\lambda_2 p) = \lambda_1 (\pi(\lambda_2)(p)) = \pi(\lambda_1)(\pi(\lambda_2) (p)) = \pi(\lambda_1) \pi(\lambda_2)$. Thus, we conclude that $\pi$ is an injective homomorphism. $\proofend$

c)
Define $Y_1 = \{(\pi(x))^k(e_G) : k \ge 0\}$. If $Y_1 \ne G$, choose $j \in G \setminus Y_1$ and define $Y_2 = \{(\pi(x))^k(j) : k \ge 0\}$. Continue in this manner, each time choosing an element outside the union of all previously constructed sets. These are distinct orbits of the permutation $\pi(x)$, so they are pairwise disjoint. Since $G$ is finite, this process ends with $G = \bigsqcup_{i=1}^r Y_i$. Now define $\sigma_i(y) = \pi(x)(y)$ for $y \in Y_i$ and $\sigma_i(y) = y$ otherwise. Then $\pi(x) = \sigma_1\sigma_2\cdots\sigma_r$ is a product of disjoint cycles, counting fixed points as $1$-cycles. Fix any $y_i \in Y_i$. By repeated application of the definition, $(\pi(x))^t(y_i) = x^t y_i$. Let $t$ be the smallest positive integer such that $(\pi(x))^t(y_i) = y_i$. Thus, $t$ is the length of the cycle $\sigma_i$. But $(\pi(x))^t(y_i) = y_i \iff x^t y_i = y_i \iff x^t = e_G$. Since $\operatorname{ord}(x) = n$, the smallest positive integer satisfying this equation is $n$. Hence $t = n$, so every $\sigma_i$ is an $n$-cycle and $|Y_i| = n$. Since the $Y_i$ partition $G$, we have $|G| = \sum_{i=1}^r |Y_i| = rn$. But $|G| = nm$, so $r = m$. Therefore, $\pi(x)$ is a product of exactly $m$ disjoint $n$-cycles, as desired. $\proofend$

d)
By part (c), $\pi(x)$ is a product of $m$ disjoint $n$-cycles. Each $n$-cycle can be written as a product of $n-1$ transpositions, with a $1$-cycle contributing zero transpositions. Therefore, $\pi(x)$ can be written as a product of $m(n-1)$ transpositions, giving $\operatorname{sgn}(\pi(x)) = (-1)^{m(n-1)}$. Hence $\pi(x)$ is odd if and only if $m(n-1)$ is odd. This occurs if and only if both $m$ and $n-1$ are odd, which is equivalent to $m$ being odd and $n$ being even. Thus, $\pi(x)$ is odd if and only if $n$ is even and $m$ is odd. $\proofend$




**Problem 4**
The center of a group $G$ is $Z(G) = \{z \in G | \forall g \in G(zg = gz)\}$.
a) Prove that $Z(G) \unlhd G$.
b) Prove $G / Z(G)$ cyclic implies $G$ is abelian.
c) Suppose $|G| = p^2$ for some prime $p$ and that $|Z(G)| > 1$. Prove that $G$ is abelian.
**Solution**
a)
Clearly, $Z(G) \subseteq G$. Also, $Z(G) \ne \emptyset$ since for any $g \in G$ we have $e_G g = g e_G$ meaning $e_G \in Z(G)$ (where $e_G$ is the identity in $G$). Let $g_1, g_2 \in Z(G)$ and consider arbitrary $p \in G$. We see that $(pg_2^{-1})^{-1} = g_2 p^{-1}$, and by $g_2 \in Z(G)$, $g_2p^{-1} = p^{-1}g_2$. It follows that $pg_2^{-1} = ((pg_2^{-1})^{-1})^{-1} = pg_2^{-1} = g_2^{-1}p$. Hence $g_2^{-1} \in Z(G)$. Continuing, $g_1g_2^{-1}p = g_1pg_2^{-1} = pg_1g_2^{-1}$. But then $g_1 g_2^{-1} \in Z(G)$ making $Z(G) \le G$. Take any $nmn^{-1} \in nZ(G)n^{-1}$ for $n \in G$. It is easy to see that for arbitrary $q \in G$, $nmn^{-1}q = nm(n^{-1}q)$, and by $m \in Z(G)$, $nm(n^{-1}q) = n(n^{-1}q)m = e_G qm = qm$. Similarly, $qnmn^{-1} = (qn)mn^{-1} = m(qn)n^{-1} = mqe_G = mq$. But again by $m \in Z(G)$, $qm = mq$. Therefore, $nmn^{-1}q = qnmn^{-1}$ meaning $nZ(G)n^{-1} \subseteq Z(G)$ for arbitrary $n \in G$. Thus, $n^{-1}(n Z(G)n^{-1})n = Z(G) \subseteq n^{-1}Z(G)n$ for any $n \in G$. Setting $n = n^{-1}$ gives $Z(G) \subseteq nZ(G)n^{-1}$. So $nZ(G)n^{-1} = Z(G)$ for any $n \in G$. Since $Z(G) \le G$ as well, $Z(G) \unlhd G$ as desired. $\proofend$

b)
Suppose so. Let $a, b \in G$. Since $G / Z(G)$ is cyclic, pick generator $xZ \in G /Z(G)$ so that $G/Z(G) = <xZ(G)>$. But then $aZ(G) = x^rZ(G)$ and $bZ(G) = x^sZ(G)$ for $r,s \in \mathbb{Z}$. Hence $a = x^rz_1$ and $b = x^s z_2$ for some $z_1, z_2 \in Z(G)$. It is now easy to see that $ab = x^rz_1 x^s z_2$, and by $z_1, z_2 \in Z(G)$, $x^rz_1x^sz_2 = z_1x^rz_2x^s = z_1z_2x^rx^s$. Similarly, $ba = x^sz_2x^rz_1 = z_2x^sz_1x^r = z_2z_1x^sx^r = z_1z_2x^sx^r = z_1z_2x^{s+r} = z_1z_2x^{r+s} = z_1z_2x^rx^s = ab$. Thus, $G$ is abelian. $\proofend$  

c)
By Lagrange's Theorem, $|G| = |Z(G)|[G : Z(G)]$ since $Z(G) \le G$. Hence $p^2 = |Z(G)|[G : Z(G)]$. But only $p | p^2$ and $1 | p^2$ and $p^2 | p^2$, else if $a | p^2$ where $a \ne 1,p, p^2$ we would have $a | p$ since $gcd(a, p) = 1$ (p is coprime with every number not $1$ or a multiple of $p$ by definition) which is a contradiction. Therefore, because $|Z(G)| > 1$, either $|Z(G)| = p^2$ or $|Z(G)| = p$. Case 1: $|Z(G)| = p^2$. Then because $|Z(G)| = |G|$ and $Z(G) \subseteq G$, we have $Z(G) = G$. So for any $g_1, g_2 \in G$, we have $g_1, g_2 \in Z(G)$ meaning $g_1g_2 = g_2g_1$ making $G$ abelian. Case 2: $|Z(G)| = p$. It follows that $[G : Z(G)] = p$ and so $G / Z(G)$ is cyclic. By part b, $G$ is abelian. $\proofend$

**Problem 5**
a) If $G$ is a finite group and a prime $p | |G|$, then $G$ contains an element of order $p$.
**Solution**
a)
Since $p | |G|$ with $p, |G| > 0$, it must be that $1 < p \le |G|$. Pick $g \in G$ then where $g$ is not the identity $e_G$. By Lagrange and Euclid, $p | |<g>|$ or $p | [G : <g>]$. Case 1: $p | |<g>| = ord(g)$. So $ord(g) = np$ for $n \in \mathbb{N}$. See that $ord(g^n) = \frac{np}{gcd(np, n)}$. Clearly, $n | n$ and $n | np$ meaning $n | gcd(np, n)$. If $m > n$ and $m = gcd(np, n)$, then $m | n$ which is not possible. Since $n, gcd(np, n) > 0$, $gcd(np, n) \ge n$. It follows that $gcd(np,n) = n$. Thus, $ord(g^n) = p$ as desired. Case 2: $p | [G : <g>]$. Then $[G : <g>] = kp$ for $k \in \mathbb{N}$. 
