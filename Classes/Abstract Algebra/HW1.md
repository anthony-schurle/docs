**Problem 1**:
Use the euclidean algorithm to compute $gcd(252, 198), gcd(662, 414), gcd(12345, 6789)$.
In each case, display every division step. Then express each $GCD$ as an integer linear combination of the corresponding pair of integers.
**Solution**:
$gcd(252, 198)$ - 
$$
\begin{aligned}
252 &= 1(198) + 54 \\
198 &= 3(54) + 36 \\
54 &= 1(36) +18 \\
36 &= 2(18) + 0
\end{aligned}
$$
and so $gcd(252, 198) = 4(252) - 5(198) = 18$.
$gcd(662, 414)$ - 
$$
\begin{aligned}
662 &= 1(414) + 248 \\
414 &= 1(248) + 166 \\
248 &= 1(166) + 82 \\
166 &= 2(82) + 2 \\
82 &= 41(2) + 0
\end{aligned}
$$
and so $gcd(662, 414) = 8(414) - 5(662) = 2$.
$gcd(12345, 6789)$ -
$$
\begin{aligned}
12345 &= 1(6789) + 5556 \\
6789 &= 1(5556) + 1233 \\
5556 &= 4(1233) + 624 \\
1233 &= 1(624) + 609 \\
624 &= 1(609) + 15 \\
609 &= 40(15) + 9 \\
15 &= 1(9) + 6 \\
9 &= 1(6) + 3 \\
6 &= 2(3) + 0
\end{aligned}
$$
and so $gcd(12345, 6789) = 1642(6789) - 903(12345) = 3$. $\proofend$

___

**Problem 4**:
Let $p$ be a prime. Show that $\sqrt{p}$ is irrational.
**Solution**:
Suppose not. Then $\sqrt{p} = \frac{a}{b}$ where $gcd(a, b) = 1$ (else we can reduce to such a rational). It follows that $p = \frac{a^2}{b^2}$, and so $pb^2 = a^2$. Hence $p | a^2$, and by corollary 12, $p | a$. We then see that since $p = \frac{a^2}{b^2}$, it must be that $b^2 = \frac{a^2}{p}$. But $a = a'p$ for some $a' \in \mathbb{Z}$ since $p|a$. Thus, $b^2 = \frac{(a'p)^2}{p} = pa'^2$. And so $p | b^2$. By corollary 12, $p | b$. But now we have reached a contradiction since $p | a$, $p | b$, and $gcd(a, b) = 1$. Therefore, $\sqrt{p}$ is irrational. $\proofend$ 

---

**Problem 5**:
For a positive integer $n$, define Euler's totient function by $\phi(n) = \mid\{k \in \{1, 2, ..., n\} | gcd(k, n) = 1\}\mid$. Prove the following statements:
- If $m$ and $n$ are relatively prime positive integers, then $\phi(mn) = \phi(m)\phi(n)$.
- If $p$ is a prime and $a$ is a positive integer, determine $\phi(p^a)$.
- If $n = \prod_{i=1}^r p_i^{a_i}$ is the prime factorization of $n$, determine a formula for $\phi(n)$.
**Solution**:
Define $\Phi(n) = \{k \in \{1, 2, ..., n\} | gcd(k, n) = 1\}$.
(a) Suppose so. Let $x$ be a number between $0$ and $mn-1$. Then solving the equation $xy \equiv 1 \mod mn$ is equivalent to solving the pair of equations $xy \equiv [1, 1] \mod [m, n]$ by the CRT. Hence $x \in \Phi(mn)$ iff $x \equiv [a, b] \mod [m, n]$ for integers $a \in \Phi(m)$ and $b \in \Phi(n)$. The CRT gives a one-to-one correspondence between $\Phi(mn)$ and pairs $[a,b]$ in which the first term is in $\Phi(m)$ and the second term in $\Phi(n)$. Therefore,  $\phi(mn) = \phi(m)\phi(n)$. (I am relying on a lot of number theory from last year, not sure if I missed something in class)

(b) Suppose $p$ is prime and $a$ is a positive integer. We claim that $\phi(p^a) = p^a - p^{a-1}$. Consider any $\alpha \in \{1, 2, ..., p^a\} \backslash \Phi(p^a)$. By construction, there is some $d >1$ such that $d | p^a$ and $d | \alpha$. Then by prime decomposition on $d$, there is some prime $q$ such that $q | d$. Therefore, $q | p^a$ and $q | \alpha$. But by corollary 12, we must have $q = p$. Hence $p | \alpha$. Conversely, suppose $p | \alpha$ for $\alpha \in \{1, 2, ..., p^a\}$. Then $gcd(\alpha, p^a) \ge p > 1$, meaning that $\alpha \in \{1, 2, ..., p^a\} \backslash \Phi(p^a)$. In other words, every $\alpha \in \{1, 2, ..., p^a\} \backslash \Phi(p^a)$ is a multiple of $p$. Every such multiple is of the form $kp$ for $k \in \mathbb{N}$. But notice that $kp \le p^a \iff 1 \le k \le p^{a-1}$, meaning there are precisely $p^{a-1}$ multiples of $p$ in $\{1, 2, ..., p^a\}$. Thus, $\phi(p^a) = p^a - p^{a-1}$.

(c) Suppose so. Then $\phi(n) = \phi(\prod_{i=1}^r p_i^{a_i})$. Now consider any $p_j^{a_j}$ and $p_l^{a_l}$ where $p_j \ne p_l$. For the sake of contradiction, suppose that $gcd(p_j^{a_j}, p_l^{a_l}) = d > 1$. Then, by prime decomposition, there is some prime $q$ such that $q |d$. But $d | p_j^{a_j}$ and $d | p_l^{a_l}$, and so $q | p_j^{a_j}$ and $q | p_l^{a_l}$. By corollary 12, $q = p_j = p_l$ which is a contradiction. Since the prime powers $p_i^{a_i}$ are pairwise coprime, by applying property (a) repeatedly, we have $\phi(\prod_{i=1}^r p_i^{a_i}) = \prod_{i=1}^r \phi(p_i^{a_i})$. Then by property (b), $\prod_{i=1}^r \phi(p_i^{a_i}) = \prod_{i=1}^r (p_i^{a_i} - p_i^{a_i-1})$. $\proofend$
