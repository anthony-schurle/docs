# Chapter 2: Prime Factorization
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## 2.0 Prime Factorization
---
### Key Concepts
- **Sieve Of Eratosthenes**:
  - Remove multiples of primes sequentially.
- **Prime Count Estimate**:
  - $\pi(x) \approx Li(x) = \int_{2}^x\frac{1}{log(t)}dt$.
### Definitions
- **Prime Number**
  - Positive integer not equal to one, whose only positive factors are 1 and itself.
- **Composite Number**
  - Positive integers, not equal to one, which are not prime.
- **One**
  - Unit that is neither composite nor prime.
- **Factoring**
  - Expressing number as product of 1+ primes.
  - Decomposition is unique.
  - Prime decomposition groups all primes.
- **Mersenne Primes**
  - sequence of powers of two minus 1.
- **Divisor Count Function**
  - Denoted $\sigma_0$.
- **Divisor Sum Function**
  - Denoted $\sigma_k$ for the sum of the kth powers of the positive divisors.
  - Generalizes divisor count.
- **Coprime**
  - $GCD(a, b) = 1$ for integers a and b.
- **Multiplicative Functions**
  - $f(ab) = f(a) \cdot f(b)$ when a and b are coprime.
- **Perfect Number**
  - Positive integer n which satisfies $\sigma_1(n) = 2n$.

### Theorems & Proofs
**Proposition 2.2**
Let N be a positive integer. If N is composite then N has a prime factor between 2 and $\lfloor \sqrt{N} \rfloor$. Thus, if $N > 1$ and N has no prime factors between 2 and $\lfloor \sqrt{N} \rfloor$ then N must be prime.

**Theorem 2.3**
There are infinitely many prime numbers.

Suppose you have a finite list of prime numbers. Multiply all the prime numbers and call the result N. So N is a positive integer. As $N + 1$ is again a positive integer, bigger than 1, $N + 1$ has a prime factor p. If p were in our list, then $p | N$ and $p | N + 1$. By the two-out-of-three principle $p | 1$. But this is a contradiction. Therefore, since no finite list contains all prime numbers, there are infinite $\blacksquare$

**Theorem 2.4**
If a,b are positive integers and $GCD(a, b) = 1$, then there are infinitely many prime numbers in the progression $a,a + b,a + 2b,a + 3b,...$.

**Theorem 2.5**
The set of prime numbers contains infinitely many arithmetic progressions of length k, for all positive k.

**Conjecture 2.8**
For all $x \ge 2657$, $|\pi(x) - li(x)| \le \frac{\sqrt{x} \cdot log(x)}{8\pi}$.

**Conjecture 2.9**
There are infinitely many twin primes.

**Conjecture 2.10**
Let k be a positive even number. Then there are infinitely many prime numbers p such that the next prime number is $p + k$.

**Theorem 2.11**
There exist infinitely many pairs of consecutive prime numbers (p, q) such that $0 < q - p \le 246$.

**Lemma 2.12 (Euclid's Lemma)**
Let a, b, and c be integers. If $a | bc$, and $GCD(a, b) = 1$, then $a | c$.

Since $GCD(a, b) = 1$, theorem 1.14 implies that there exist integers x and y such that $ax + by = 1$. Multiplying both sides by c, $axc + byc = c$. Observe that $a | axc$ and $a | byc$ since $a | bc$. Therefore, $a | c$. $\blacksquare$

**Corollary 2.13**
Let p, b, and c be integers, and suppose p is a prime number. If $p | bc$ then $p | b$ or $p | c$.

Consider $GCD(p, b)$. It is a positive divisor of p, and since p is prime, we find $GCD(p, b) = 1$ or $GCD(p, b) = p$. If $GCD(p, b) = p$, then $p = GCD(p, b) | b$ so $p | b$. If $GCD(p, b) = 1$, then Lemma 2.12 implies that $p | c$. $\blacksquare$

**Corollary 2.14**
If a prime number divides a product of integers , then p divides at least one term in the product.

**Theorem 2.15**
Suppose that $e_2, e_3, e_5, ...$ and $f_2, f_3, f_5, ...$ are natural numbers, and only finitely many of them are nonzero. If $2^{e_2}3^{e_3}5^{e_5}7^{e_7} = 2^{f_2}3^{f_3}5^{f_5}7^{f_7}...p^{f_p}...$ then the exponents are equal.

Suppose that N is a positive integer, and $N = 2^{e_2}3^{e_3}... = 2^{f_2}3^{f_3}...$. Let p be a prime. We wish to show that $e_p = f_p$. It suffices to show the case with $e_p \le f_p$. In this case we may define a natural number $d_p = f_p - e_p$, and consider the positive integer $\frac{N}{p^{e_p}}$ with prime decompositions. $\frac{N}{p^{e_p}} = 2^{e_2}3^{e_3}...p^0 = 2^{f_2}3^{f_3}...p^{d_p}$. If $d_p$ were positive, then p would divide the right side, and hence would divide the left side. By Corollary 2.14, p would divide a prime on the left side which is a contradiction. Hence $d_p = 0$. Therefore, $e_p = f_p$. $\blacksquare$

**Conjecture 2.17**
Every even number starting with 4 can be expressed as the sum of two prime numbers.

**Theorem 2.18**
There exists a positive number N such that if $n > N$ and n is even, then n can be expressed as a sum $n = p + s$ in which p is prime and s is a prime or a product of two primes.

**Theorem 2.19**
Every odd number starting at can be expressed as the sum of three primes.

**Proposition 2.20**
Let a and b be positive integers with prime decompositions: $a = 2^{e_2}3^{e_3}..., b = 2^{f_2}3^{f_3}...$. Then $a | b$ iff $e_p \le f_p$ for every prime number p.

By definition, $a | b$ iff there is a positive integer c satisfying $b = ac$. Such a positive integer c has a prime decomposition also: $2^{g_2}3^{g_3}...$. We find that $a | b$ iff there are natural numbers $g_2, g_3, ...$ such that $(2^{e_2}3^{e_3}...) \cdot (2^{g_2}3^{g_3}...) = 2^{f_2}3^{f_3}...$. But by theorem 2.15, this occurs iff $e_k + g_k = f_k$. Finding c is equivalent to finding natural numbers $g_2, g_3, ...$. This is possible iff $e_2 \le f_2, e_3 \le f_3, ...$. Hence $a | b$ iff $e_p \le f_p$ for every prime number p.

**Corollary 2.22**
Let N be a positive integer. For each prime number p, let $e_p$ denote the exponent of p in the prime decomposition of N. Then $\sigma_0(N) = (e_2 + 1) \cdot (e_3 + 1) \cdot (e_5 + 1) ...$.

To choose a divisor of N, it is equivalent to choose a power of 2 between 0 and $e_2$, to choose a power of 3 between 0 and $e_3$, etc. The number of choices equals the product as defined. $\blacksquare$

**Corollary 2.24**
$GCD(a, b)$ has prime decomposition $2^{min(e_2,f_2)}3^{min(e_3, f_3)}...$. Similarly, $LCM(a, b)$ has prime decomposition $2^{max(e_2,f_2)}3^{max(e_3,f_3)}...$.

The greatest common divisor of a and b is characterized by $GCD(a, b) | a$ and $GCD(a, b) | b$. If d is a positive integer and $d | a$ and $d | b$, then $d | GCD(a, b)$. Let $g_p$ denote the exponents in the prime decomposition of $GCD(a,b)$. Let $v_p$ denote the exponents in the prime decomposition of a positive integer d. Then we see that $g_p \le e_p$ and $g_p \le f_p$ for every prime number p. Also, if $v_p \le e_p$ and $v_p \le f_p$, then $v_p \le g_p$ for every prime number p. But then it follows that $g_p$ is the minimum of $e_p$ and $f_p$. Hence $g_p = min(e_p, f_p)$ for all p. LCM follows similarly. $\blacksquare$

**Corollary 2.25**
If $GCD(a, b) = 1$ then $GCD(a^m, b^n) = 1$ for all positive integers m and n.

Since $GCD(a, b) = 1$, we have $min(e_p, f_p) = 0$ for all primes p. Hence $min(m \cdot e_p, n \cdot f_p) = 0$ for all primes p. But $m \cdot e_p$ and $n \cdot f_p$ are the exponents of p in $a^m$ and $b^n$, respectively; therefore $GCD(a^m, b^n) = 1$. $\blacksquare$

**Theorem 2.27**
Let N be a positive integer, and let $C(N)$ be the probability that two integers a and b, chosen independently and at random from $\{1, ..., N\}$ are coprime. Then $lim_{N \to \infty}C(N) = \frac{6}{\pi^2} \approx 0.6079$.

**Theorem 2.28**
Let a and b be coprime positive integers. If $u | a$ and $v | b$, then $uv | ab$. This gives a one-to-one correspondence between divisors of ab and ordered pairs (u, v) consisting of a divisor of and a divisor of b.

For the first assertion, note $a = um$ and $b = vn$ then $ab = mnuv$. To see the correspondence, consider the prime decompositions of a and b. Since $GCD(a, b) = 1$, they have no primes in common. Thus we can write $a = p_1^{e_1}...p_s^{e_s}$ and $b = q_1^{f_1}...q_t^{f_t}$ for disjoint lists of prime numbers $\{p_1, ..., p_s\}$ and $\{q_1, ..., q_t\}$. The prime decomposition of ab is then $ab = p_1^{e_1}...p_s^{e_s} \cdot q_1^{f_1}...q_t^{f_t}$. Giving a divisor $w | ab$ is the same as giving exponents $e_i' \le e_i$ and $f_i' \le f_i$ for all $1 \le i \le s$ and all $1 \le j \le t$, so that $w | ab$. This is the same as giving a pair of divisors $u = p_1^{e_1'}...p_s^{e_s'} | a$ and $v = q_1^{f_1'}...q_t^{f_t'} | b$. $\blacksquare$

**Corollary 2.29**
If a and b are coprime positive integers, then $\sigma_0(a, b) = \sigma_0(a) \times \sigma_0(b)$.

**Proposition 2.30**
Let f be a multiplicative function. If N is a positive integer with prime decomposition $N = 2^{e_2}3^{e_3}...$, then $f(N) = f(2^{e_2}) \cdot f(3^{e_3})...$.

Since $GCD(2^{e_2}, 3^{e_3}5^{e_5}...) = 1$, we have $f(N) = f(2^{e_2})\cdot f(3^{e_3}5^{e_5}...)$. Carrying on in this manner leads to the result. $\blacksquare$

**Theorem 2.31**
If a and b are positive and coprime, then $\sigma_k(ab) = \sigma_k(a) \cdot \sigma_k(b)$.

**Proposition 2.33**
Let x be any number except 1. Let e be a natural number. Then $1 + x + x^2 + ... + x^e = \frac{x^{e + 1} - 1}{x - 1}$.

$$
(x - 1) \cdot (1 + x + x^2 + ... + x^e) = x \cdot (1 + x + x^2 + ... + x^e) - (1 + x + x^2 + ... + x^e) = -1 + x^{e+1}
$$
$\blacksquare$

**Corollary 2.34**
If p is a prime number, and k is a positive integer, and e is a positive integer, then $\sigma_k(p^e) = \frac{p^{ke + k} - 1}{p^k - 1}$.

When p is a prime number, the divisors of $p^e$ are 1, p, $p^2$, $p^3$, ..., $p^e$.
$$
\sigma_k(p^e) = 1^k + p^k + (p^2)^k + (p^3)^k + ... + (p^e)^k = 1 + p^k + (p^k)^2 + (p^k)^3 + ... + (p^k)^e
$$
$$
= \frac{(p^k)^{e+1} - 1}{(p^k) - 1}
$$
$\blacksquare$

**Proposition 2.36**
If n is a positive integer, and $2^n - 1$ is a prime number, then n is a prime number.

If $n = 1$, then $2^n - 1 = 1$, which is not prime. If n is composite, then $n = de$ for two integers d,e with $d > 1$ and $e > 1$. It follows that $2^n - 1 = 2^{de} - 1 = (2^d - 1)(1 + 2^d + ... + 2^{d(e - 1)})$. Since $d > 1$, $2^d - 1 > 1$ and $1 + 2^d + ... + 2^{d(e - 1)} > 1$. Hence the above equality demonstrates that $2^n - 1$ is composite. $\blacksquare$

**Theorem 2.37**
If the quantity $q = 1 + 2 + 2^2 + ... + 2^{n - 1} = 2^n - 1$ is prime, then $2^{n - 1}q$ is a perfect number.

Let $q = 1 + 2 + 2^2 +... + 2^{n-1} = 2^n - 1$, a prime number. Let $N = 2^{n-1}(2^n-1) = 2^{n-1}q$.
$$
\sigma_1(N) = \sigma_1(2^{n-1})\sigma_1(q) = (2^n-1)(q+1) = q(2^n - 1 + 1) = q \cdot 2 \cdot 2^{n-1} = 2(2^{n-1})q = 2N
$$
Hence N is a perfect number. $\blacksquare$

**Theorem 2.38**
Suppose N is an even perfect number. Then there exist prime numbers p and q, for which $q = 2^p - 1$ and $N = 2^{p-1} \cdot q$.

Begin with the prime decomposition of $N = 2^{e_2}3^{e_3}...$. Define $p = e_2 + 1$ and define $q = 3^{e_3}5^{e_5}...$. Then, $N = 2^{p-1} \cdot q$. Since N is even, $e_2 \ge 1$, so $p \ge 2$. Observe that $GCD(2^{p-1}, q) = 1$ since q is odd. With the fact that $\sigma_1$ is multiplicative we see that $\sigma_1(N) = \sigma_1(2^{p-1})\sigma_1(q) = (2^p-1)\sigma_1(q)$. Since N is perfect, $\sigma_1(N) = 2N = 2^pq$. Hence $(2^p-1)\sigma_1(q) = 2^pq$. Hence $\sigma_1(q) = (\frac{2^p}{2^p-1})q = (\frac{2^p-1}{2^p-1})q + (\frac{1}{2^p-1})q = q + \frac{q}{2^p-1}$. $\frac{q}{2^p-1} = \sigma_1(q) - q$ and so is positive. It is a proper divisor of q, since $p \ge 2$ implies $2^p - 1 > 1$. Notice that $\sigma_1(q)$ equals q plus one other divisor of q. Thus, the sum of all divisors of $\sigma_1(q)$ equals the sum of only two divisors of q, so q must have only two divisors. Hence q is prime, and the two divisors are q and 1. Hence $\frac{q}{2^p-1} = 1$, and so $q = 2^p-1$ is a prime number. By proposition 2.36, p is prime too. $\blacksquare$

### Examples
**Example Title**
**Problem 6:**
Prove that if a, b, and n  are positive integers and $a^n | b^n$, then $a | b$.
**Solution:**
Suppose a, b, and n are positive integers such that $a^n | b^n$. 

**Problem 7:**
Compute $\sigma_0(1000), \sigma_0(750), \sigma_0(1024)$.
**Solution:**
a)
$$
\sigma_0(1000) = \sigma_0(2^35^3) = (3+1)(3+1) = 16
$$
b)
$$
\sigma_0(750) = \sigma_0(2^13^15^3) = (1 + 1)(1 + 1)(3 + 1) = 16
$$
c)
$$
\sigma_0(1024) = \sigma(2^{10}) = 11
$$

**Problem 8:**
Compute $\sigma_1(100), \sigma_2(750), \sigma_3(1024)$.
**Solution:**
a)
$$
\sigma_1(100) = \sigma_1(2^2)\sigma_1(5^2) = \frac{2^3 - 1}{2 - 1}\frac{5^3 - 1}{5 - 1} = 217
$$

b)
$$
\sigma_2(750) = \sigma_2(2^1)\sigma_2(3^1)\sigma_2(5^3) = \frac{2^4 - 1}{4 - 1}\frac{3^4 - 1}{9 - 1}\frac{5^8 - 1}{25 - 1} = 16,276
$$

c)
$$
\sigma_3(1024) = \sigma_3(2^{10}) = \frac{2^{33} - 1}{8 - 1} = 1,227,133,513
$$

**Problem 10:**
What is the smallest positive integer with precisely 60 positive divisors?
**Solution:**
Let n be the smallest positive integer with precisely 60 positive divisors. Let its prime decomposition be defined by $n = 2^{e_2}3^{e_3}...$. 

**Problem 11:**
If n is a positive integer, and $\sigma_0(n)$ is a prime then n is a power of a prime number.
**Solution:**
Let n be a positive integer and suppose $\sigma_0(n)$ is prime. Then $\sigma_0(n)$ is a product of 1 and a prime number itself. By corollary 2.22, we see that $\sigma_0(n) = 1 \times (e_k + 1)$ for some $e_k$ that is the exponent of the prime decomposition of n. It follows that n is composed of only one prime p. And $\sigma_0(n) = 1 \times (e_k + 1) = \sigma_0(p^{e_k})$. Therefore, $n = p^{e_k}$, and so n is the product of a prime number. $\blacksquare$

**Problem 14:**
If n is a square number, then n is not a perfect number.
**Solution:**
Let n be a square number. Define its prime decomposition as $(2^{e_2}3^{e_3}...)^2$, which is possible since $\sqrt{n}$ is a natural number by definition. We see that,
$$
\sigma_1(n) = \sigma_1(2^{2e_2})\sigma_1(3^{2e_3})... = \frac{2^{2e_2 + 1} - 1}{2 - 1}\frac{3^{2e_3 + 1} - 1}{3 - 1}... \ne 2n
$$
Therefore, n is not a perfect number. $\blacksquare$

**Problem 16:**
Describe all circumstances under which $\sigma_1(n)$ is odd.
**Solution:**
$\sigma_1(n)$ is odd when




Problem 6
Prove that if $a, b,$ and $n$ are positive integers and $a^n | b^n$, then $a | b$.
**Solution:**
Suppose $a, b,$ and $n$ are positive integers such that $a^n | b^n$. Let $a = p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k}$ and $b = p_1^{b_1} p_2^{b_2} \cdots p_k^{b_k}$ be the prime factorizations of $a$ and $b$. Then $a^n = p_1^{na_1} p_2^{na_2} \cdots p_k^{na_k}$ and $b^n = p_1^{nb_1} p_2^{nb_2} \cdots p_k^{nb_k}$. Since $a^n | b^n$, for each prime $p_i$, we must have $na_i \leq nb_i$. Dividing both sides by $n > 0$, we get $a_i \leq b_i$ for all $i$. Therefore, $a | b$. $\blacksquare$

Problem 7
Compute $\sigma_0(1000), \sigma_0(750), \sigma_0(1024)$.
**Solution:**
a) $1000 = 2^3 \cdot 5^3$
$$\sigma_0(1000) = \sigma_0(2^3 \cdot 5^3) = (3+1)(3+1) = 16$$

b) $750 = 2 \cdot 3 \cdot 5^3$
$$\sigma_0(750) = \sigma_0(2 \cdot 3 \cdot 5^3) = (1 + 1)(1 + 1)(3 + 1) = 16$$

c) $1024 = 2^{10}$
$$\sigma_0(1024) = \sigma_0(2^{10}) = 10 + 1 = 11$$

Problem 8
Compute $\sigma_1(100), \sigma_2(750), \sigma_3(1024)$.
**Solution:**
a) $100 = 2^2 \cdot 5^2$
$$\sigma_1(100) = \sigma_1(2^2)\sigma_1(5^2) = \frac{2^3 - 1}{2 - 1}\frac{5^3 - 1}{5 - 1} = 7 \cdot 31 = 217$$

b) $750 = 2 \cdot 3 \cdot 5^3$
$$\sigma_2(750) = \sigma_2(2)\sigma_2(3)\sigma_2(5^3) = \frac{2^4 - 1}{2^2 - 1}\frac{3^4 - 1}{3^2 - 1}\frac{5^8 - 1}{5^2 - 1} = \frac{15}{3} \cdot \frac{80}{8} \cdot \frac{390624}{24} = 5 \cdot 10 \cdot 16276 = 813,800$$

c) $1024 = 2^{10}$
$$\sigma_3(1024) = \sigma_3(2^{10}) = \frac{2^{33} - 1}{2^3 - 1} = \frac{8,589,934,591}{7} = 1,227,133,513$$

Problem 10
What is the smallest positive integer with precisely 60 positive divisors?
**Solution:**
Let $n$ be the smallest positive integer with precisely 60 positive divisors. Let its prime factorization be $n = p_1^{e_1}p_2^{e_2}\cdots p_k^{e_k}$. Then $\sigma_0(n) = (e_1+1)(e_2+1)\cdots(e_k+1) = 60$. Since $60 = 2^2 \cdot 3 \cdot 5$, we consider various factorizations. To minimize $n$, we assign larger exponents to smaller primes. The key candidates are:
- $60 = 5 \cdot 3 \cdot 2 \cdot 2$: $n = 2^4 \cdot 3^2 \cdot 5 \cdot 7 = 16 \cdot 9 \cdot 5 \cdot 7 = 5,040$
- $60 = 4 \cdot 3 \cdot 5$: $n = 2^4 \cdot 3^3 \cdot 5^2 = 16 \cdot 27 \cdot 25 = 10,800$
- $60 = 6 \cdot 5 \cdot 2$: $n = 2^5 \cdot 3^4 \cdot 5 = 32 \cdot 81 \cdot 5 = 12,960$

Therefore, the smallest such integer is $\boxed{5040}$. $\blacksquare$

Problem 11
If $n$ is a positive integer, and $\sigma_0(n)$ is a prime, then $n$ is a power of a prime number.
**Solution:**
Let $n$ be a positive integer with prime factorization $n = p_1^{e_1} p_2^{e_2} \cdots p_k^{e_k}$. Then 
$$\sigma_0(n) = (e_1+1)(e_2+1)\cdots(e_k+1)$$

Suppose $\sigma_0(n)$ is prime. Since each factor $(e_i+1) \geq 2$, the only way this product can be prime is if there is exactly one factor, i.e., $k = 1$. Therefore, $n = p_1^{e_1}$, which is a power of a prime. $\blacksquare$

Problem 14
If $n$ is a square number, then $n$ is not a perfect number.
**Solution:**
Let $n$ be a perfect square, so $n = m^2$ for some positive integer $m$ with prime factorization $m = p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k}$. Then $n = p_1^{2a_1} p_2^{2a_2} \cdots p_k^{2a_k}$. For any odd prime $p$ and even exponent $2a$:
$$\sigma_1(p^{2a}) = 1 + p + p^2 + \cdots + p^{2a}$$
This is a sum of $2a+1$ odd terms, so it is odd. For $p = 2$ and even exponent $2a$:
$$\sigma_1(2^{2a}) = 2^{2a+1} - 1$$
which is odd. Therefore, $\sigma_1(n) = \sigma_1(p_1^{2a_1})\sigma_1(p_2^{2a_2})\cdots\sigma_1(p_k^{2a_k})$ is a product of odd numbers, hence odd. However, $2n$ is even. Since $\sigma_1(n)$ is odd and $2n$ is even, we have $\sigma_1(n) \neq 2n$. Therefore, $n$ is not a perfect number. $\blacksquare$

Problem 16
Describe all circumstances under which $\sigma_1(n)$ is odd.
**Solution:**
For a prime power $p^k$, we have $\sigma_1(p^k) = 1 + p + p^2 + \cdots + p^k$.
- If $p$ is odd and $k$ is even: This is a sum of $k+1$ (odd number of) odd terms, so it is **odd**.
- If $p$ is odd and $k$ is odd: This is a sum of $k+1$ (even number of) odd terms, so it is **even**.
- If $p = 2$: $\sigma_1(2^k) = 2^{k+1} - 1$, which is always **odd**.

Therefore, $\sigma_1(n)$ is odd if and only if every odd prime in the factorization of $n$ appears to an even exponent. $\sigma_1(n)$ is odd if and only if $n$ divided by the largest power of 2 that divides it is a perfect square. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages 47–74
