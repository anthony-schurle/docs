1) Find a number between 0 and 90, such that $x \equiv [4, 8]$ mod $[7, 13]$.

Take $x=60$. Then $60\equiv 4 \pmod 7$ and $60\equiv 8 \pmod {13}$. $\proofend$

2) List all numbers x such that $0 \le x < 100$ and $x \equiv [3, 1]$ mod $[4, 5]$.

We require $x=3+4k$. Then $3+4k\equiv 1 \pmod 5$ also, so $4k\equiv -2\equiv 3 \pmod 5$. Since $4(4)\equiv 1 \pmod 5$, we get $k\equiv 4\cdot 3\equiv 12\equiv 2 \pmod 5$. Hence $x\equiv 3+4\cdot 2=11 \pmod {20}$. The numbers with $0\le x<100$ are therefore $11,31,51,71,91$. $\proofend$

3) Prove that if $n > 2$ then $\phi(n)$ is even.

By Theorem 7.9, $\phi$ is multiplicative on relatively prime factors, and by Proposition 7.10, if $p$ is prime then $\phi(p^r)=p^r-p^{r-1}=p^{r-1}(p-1)$. Write $n=\prod p_i^{r_i}$. If some odd prime $p_i$ divides $n$, then $p_i-1$ is even, so $\phi(p_i^{r_i})=p_i^{r_i-1}(p_i-1)$ is even, and therefore $\phi(n)$ is even. If no odd prime divides $n$, then $n=2^r$ with $r>1$, since $n>2$. Then $\phi(n)=\phi(2^r)=2^r-2^{r-1}=2^{r-1}$, which is even. Hence $\phi(n)$ is even for every $n>2$. $\proofend$

4) Use the Chinese remainder theorem to find all of the solutions to $x^2 + 1 = 0$, modulo $1313$.

Factor $1313=13\cdot 101$. By Proposition 7.5, the solutions to $x^2+1\equiv 0 \pmod {1313}$ correspond to simultaneous solutions modulo $13$ and modulo $101$, and by Theorem 7.2 these can be assembled uniquely modulo $1313$. Modulo $13$, $5^2=25\equiv -1 \pmod {13}$, so $x\equiv \pm 5 \pmod {13}$. Modulo $101$, $10^2=100\equiv -1 \pmod {101}$, so $x\equiv \pm 10 \pmod {101}$. Assembling the four combinations gives $x\equiv 616 \pmod {1313}$ from $x\equiv 5 \pmod {13}$ and $x\equiv 10 \pmod {101}$, $x\equiv 798 \pmod {1313}$ from $x\equiv 5 \pmod {13}$ and $x\equiv -10 \pmod {101}$, $x\equiv 515 \pmod {1313}$ from $x\equiv -5 \pmod {13}$ and $x\equiv 10 \pmod {101}$, and $x\equiv 697 \pmod {1313}$ from $x\equiv -5 \pmod {13}$ and $x\equiv -10 \pmod {101}$. Therefore the solutions modulo $1313$ are $515,616,697,798$. $\proofend$

5) What are the last two digits of $3^{1000}$?

The last two digits are determined modulo $100=4\cdot 25$. By Theorem 7.2, it is enough to compute modulo $4$ and modulo $25$. Modulo $4$, $3^{1000}\equiv (-1)^{1000}\equiv 1 \pmod 4$. By Proposition 7.10, $\phi(25)=25-5=20$, so Euler's theorem gives $3^{20}\equiv 1 \pmod {25}$. Since $20\mid 1000$, we get $3^{1000}\equiv 1 \pmod {25}$. Therefore $3^{1000}\equiv 1 \pmod 4$ and $3^{1000}\equiv 1 \pmod {25}$, so by Theorem 7.2, $3^{1000}\equiv 1 \pmod {100}$. Thus the last two digits are $01$. $\proofend$

6) Find a positive integer x such that the last three digits of $7^{7^x}$ are $007$.

Take $x=4$. Then $7^{7^x}=7^{7^4}$. By Theorem 7.2, it is enough to check modulo $8$ and modulo $125$. Modulo $8$, since $7\equiv -1 \pmod 8$ and $7^4$ is odd, we have $7^{7^4}\equiv (-1)^{7^4}\equiv -1\equiv 7 \pmod 8$. Modulo $125$, since $7^{10}\equiv -1 \pmod {125}$, we have $7^{20}\equiv 1 \pmod {125}$. Also $7^4\equiv 1 \pmod {20}$, so $7^4-1\equiv 0 \pmod {20}$, and therefore $7^{7^4-1}\equiv 1 \pmod {125}$. Hence $7^{7^4}\equiv 7 \pmod {125}$. Thus $7^{7^4}\equiv 7 \pmod 8$ and $7^{7^4}\equiv 7 \pmod {125}$, so by Theorem 7.2, $7^{7^4}\equiv 7 \pmod {1000}$. Hence the last three digits of $7^{7^4}$ are $007$, so $x=4$ works. $\proofend$

7) Find the multiplicative inverse of 3 modulo $5^8$.

Use Lemma 7.16, lifting multiplicative inverses. Start with $3\cdot 2\equiv 1 \pmod 5$. Since $3\cdot 2=1+1\cdot 5$, Lemma 7.16 gives $2-2\cdot 1\cdot 5=-8\equiv 17 \pmod {25}$. Since $3\cdot 17=1+2\cdot 25$, Lemma 7.16 gives $17-17\cdot 2\cdot 25=-833\equiv 417 \pmod {625}$. Since $3\cdot 417=1+2\cdot 625$, Lemma 7.16 gives $417-417\cdot 2\cdot 625=-520833\equiv 260417 \pmod {390625}$. Therefore $3\cdot 260417\equiv 1 \pmod {5^8}$. $\proofend$

8) What are the square roots of 3, modulo $11^4$?

Modulo $11$, $5^2=25\equiv 3 \pmod {11}$, so $x\equiv \pm 5 \pmod {11}$. By Theorem 7.20, each square root lifts because $11$ is odd and $\gcd(5,11)=1$. Lifting $5$ first gives $27 \pmod {11^2}$. Since $27^2=3+6\cdot 11^2$ and $(2\cdot 27)^{-1}\equiv 65 \pmod {11^2}$, Theorem 7.20 gives $27-65\cdot 6\cdot 11^2\equiv 11401 \pmod {11^4}$. Since $11^4=14641$, the other root is $-11401\equiv 3240 \pmod {14641}$. Therefore the square roots of $3$ modulo $11^4$ are $3240,11401$. $\proofend$

9) Is 17 a square modulo 104? (Use the Chinese remainder theorem)

Factor $104=8\cdot 13$. By Corollary 7.6, $17$ is a square modulo $104$ if and only if it is a square modulo $8$ and modulo $13$. Modulo $8$, $17\equiv 1 \pmod 8$, and $1$ is a square modulo $8$. Modulo $13$, $17\equiv 4 \pmod {13}$, and $4=2^2$. Therefore $17$ is a square modulo both $8$ and $13$, so it is a square modulo $104$. For example, by Theorem 7.2, solving $x\equiv 1 \pmod 8$ and $x\equiv 2 \pmod {13}$ gives $x=41$, and $41^2\equiv 17 \pmod {104}$. Thus, $17$ is a square modulo $104$. $\proofend$

10) Fix a prime number p in what follows. The p-adic norm of an integer x, denoted $|x|_p$ is defined to be $p^{-e}$, if $p^e$ is the power of p appearing in the prime decomposition of x. For example, $|50|_2 = \frac{1}{2}$ and $|50|_5 = \frac{1}{25}$. The p-adic norm of zero is defined to be zero. The p-adic distance between two integers x and y is defined to be $|x - y|_p$. a) Prove that $|x|_p \le 1$ for all integers x. b) Prove the ultrametric triangle inequality, $|x+y|_p \le max\{|x|_p, |y|_p \}$. c) Let a be an integer. Describe the set of integers x such that $|x-a|_p < p^{-e}$, using the languages of congruences.

a)

By definition, if $x=0$, then $|0|_p=0\le 1$. If $x\neq 0$, then the exponent $v_p(x)$ of $p$ in the prime decomposition of $x$ is nonnegative, so $|x|_p=p^{-v_p(x)}\le 1$. Therefore $|x|_p\le 1$ for all integers $x$. $\proofend$

b)

By definition, if $x=0$, $y=0$, or $x+y=0$, the inequality is immediate. Otherwise, write $v_p(x)=r$ and $v_p(y)=s$, so $x=p^r u$ and $y=p^s v$, where $p\nmid u$ and $p\nmid v$. Assume without loss of generality that $r\le s$. Then $x+y=p^r u+p^s v=p^r(u+p^{s-r}v)$, so $p^r\mid x+y$, which implies $v_p(x+y)\ge r=\min\{r,s\}$. Therefore $|x+y|_p=p^{-v_p(x+y)}\le p^{-\min\{r,s\}}=\max\{p^{-r},p^{-s}\}=\max\{|x|_p,|y|_p\}$. Hence $|x+y|_p\le \max\{|x|_p,|y|_p\}$. $\proofend$

c)

By definition, if $x=a$, then $|x-a|_p=0<p^{-e}$, and also $x\equiv a \pmod {p^{e+1}}$. If $x\ne a$, then $|x-a|_p<p^{-e}$ means $p^{-v_p(x-a)}<p^{-e}$, which is equivalent to $v_p(x-a)>e$. Since $v_p(x-a)$ is an integer, this is equivalent to $v_p(x-a)\ge e+1$, which means $p^{e+1}\mid x-a$. This is exactly $x\equiv a \pmod {p^{e+1}}$. Therefore $\{x\in \mathbb Z: |x-a|_p<p^{-e}\}=\{x\in \mathbb Z: x\equiv a \pmod {p^{e+1}}\}$. $\proofend$