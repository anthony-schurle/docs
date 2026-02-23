Problem 6
Prove that if $a, b,$ and $n$ are positive integers and $a^n | b^n$, then $a | b$.
**Solution:**
Suppose $a, b,$ and $n$ are positive integers such that $a^n | b^n$. Let $a = p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k}$ and $b = p_1^{b_1} p_2^{b_2} \cdots p_k^{b_k}$ be the prime factorizations of $a$ and $b$. Then $a^n = p_1^{na_1} p_2^{na_2} \cdots p_k^{na_k}$ and $b^n = p_1^{nb_1} p_2^{nb_2} \cdots p_k^{nb_k}$. Since $a^n | b^n$, for each prime $p_i$, we must have $na_i \leq nb_i$. Dividing both sides by $n$ (which is non-zero), we get $a_i \leq b_i$ for all $i$. Therefore, $a | b$. $\blacksquare$

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
Let $n$ be the smallest positive integer with precisely 60 positive divisors. Let its prime factorization be $n = p_1^{e_1}p_2^{e_2}\cdots p_k^{e_k}$. Then $\sigma_0(n) = (e_1+1)(e_2+1)\cdots(e_k+1) = 60$. Since $60 = 2^2 \cdot 3 \cdot 5$, we consider various factorizations. To minimize $n$, we assign larger exponents to smaller primes. The candidates are -
$60 = 5 \cdot 3 \cdot 2 \cdot 2$: $n = 2^4 \cdot 3^2 \cdot 5 \cdot 7 = 16 \cdot 9 \cdot 5 \cdot 7 = 5,040$
$60 = 5 \cdot 4 \cdot 3$: $n = 2^4 \cdot 3^3 \cdot 5^2 = 16 \cdot 27 \cdot 25 = 10,800$
$60 = 6 \cdot 5 \cdot 2$: $n = 2^5 \cdot 3^4 \cdot 5 = 32 \cdot 81 \cdot 5 = 12,960$
$60 = 15 \cdot 2 \cdot 2$: $n = 2^{14} \cdot 3^1 \cdot 5^1 = 245,760$
etc.
Therefore, the smallest such integer is $5040$. $\blacksquare$

Problem 11
If $n$ is a positive integer, and $\sigma_0(n)$ is a prime, then $n$ is a power of a prime number.
**Solution:**
Let $n$ be a positive integer with prime factorization $n = p_1^{e_1} p_2^{e_2} \cdots p_k^{e_k}$ and suppose $\sigma_0(n)$ is prime. Then
$$\sigma_0(n) = (e_1+1)(e_2+1)\cdots(e_k+1)$$
Since each factor $(e_i+1) \geq 2$, the only way this product can be prime is if there is exactly one factor. Therefore, $n = p_1^{e_1}$, which is a power of a prime. $\blacksquare$

Problem 14
If $n$ is a square number, then $n$ is not a perfect number.
**Solution:**
Let $n$ be a perfect square, so $n = m^2$ for some positive integer $m$ with prime factorization $m = p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k}$. Then $n = p_1^{2a_1} p_2^{2a_2} \cdots p_k^{2a_k}$. For any odd prime $p$,
$$\sigma_1(p^{2a}) = 1 + p + p^2 + \cdots + p^{2a}$$
This is a sum of $2a+1$ odd terms, so it is odd. For $p = 2$,
$$\sigma_1(2^{2a}) = 2^{2a+1} - 1$$
which is odd. Therefore, $\sigma_1(n) = \sigma_1(p_1^{2a_1})\sigma_1(p_2^{2a_2})\cdots\sigma_1(p_k^{2a_k})$ is a product of odd numbers, hence odd. However, $2n$ is even. It follows that $\sigma_1(n) \neq 2n$. Therefore, $n$ is not a perfect number. $\blacksquare$

Problem 16
Describe all circumstances under which $\sigma_1(n)$ is odd.
**Solution:**
For a prime power $p^k$, we have $\sigma_1(p^k) = 1 + p + p^2 + \cdots + p^k$. If $p$ is odd and $k$ is even, we have a sum of $k+1$ odd terms, so it is odd. If $p$ is odd and $k$ is odd, we have a sum of $k+1$ odd terms, so it is even. If $p = 2$: $\sigma_1(2^k) = 2^{k+1} - 1$, which is always odd. Therefore, $\sigma_1(n)$ is odd if and only if every odd prime in the factorization of $n$ has an even exponent. $\blacksquare$

Problem 18
a) Find the prime decomposition of $20!$.
b) How many zeros would you find at the end of $100!$, if you expanded it out in base ten?
**Solution:**
a) 
We count how many of the numbers $1, 2, 3, \ldots, 20$ are divisible by prime $p$, by $p^2$, by $p^3$, etc. There are $\left\lfloor \frac{20}{p} \right\rfloor$ multiples of $p$. There are $\left\lfloor \frac{20}{p^2} \right\rfloor$ multiples of $p^2$. There are $\left\lfloor \frac{20}{p^3} \right\rfloor$ multiples of $p^3$. And so on... Therefore, the exponent of $p$ in $20!$ is:
$$e_p = \left\lfloor \frac{20}{p} \right\rfloor + \left\lfloor \frac{20}{p^2} \right\rfloor + \left\lfloor \frac{20}{p^3} \right\rfloor + \cdots$$
For $20!$, the primes up to 20 are: 2, 3, 5, 7, 11, 13, 17, 19.
For $p = 2$:
$$e_2 = \left\lfloor \frac{20}{2} \right\rfloor + \left\lfloor \frac{20}{4} \right\rfloor + \left\lfloor \frac{20}{8} \right\rfloor + \left\lfloor \frac{20}{16} \right\rfloor = 10 + 5 + 2 + 1 = 18$$
For $p = 3$:
$$e_3 = \left\lfloor \frac{20}{3} \right\rfloor + \left\lfloor \frac{20}{9} \right\rfloor = 6 + 2 = 8$$
For $p = 5$:
$$e_5 = \left\lfloor \frac{20}{5} \right\rfloor + \left\lfloor \frac{20}{25} \right\rfloor = 4 + 0 = 4$$
For $p = 7$:
$$e_7 = \left\lfloor \frac{20}{7} \right\rfloor + \left\lfloor \frac{20}{49} \right\rfloor = 2 + 0 = 2$$
For $p = 11, 13, 17, 19$:
$$e_{11} = e_{13} = e_{17} = e_{19} = \left\lfloor \frac{20}{11} \right\rfloor = 1$$
Therefore:
$$20! = 2^{18} \cdot 3^8 \cdot 5^4 \cdot 7^2 \cdot 11 \cdot 13 \cdot 17 \cdot 19$$

b) A trailing zero in base 10 is produced by a factor of $10 = 2 \cdot 5$. The number of trailing zeros equals the number of times 10 divides $100!$, which is $\min(e_2, e_5)$ where $e_2$ and $e_5$ are the exponents of 2 and 5 in the prime factorization of $100!$. Since there are more multiples of 2 than multiples of 5 (hinted at by part a and easily checked for 100!), we have $e_2 > e_5$. Therefore, the number of trailing zeros equals $e_5$. For $p = 5$ in $100!$:
$$e_5 = \left\lfloor \frac{100}{5} \right\rfloor + \left\lfloor \frac{100}{25} \right\rfloor + \left\lfloor \frac{100}{125} \right\rfloor = 20 + 4 + 0 = 24$$
Therefore, $100!$ has 24 trailing zeros. $\blacksquare$

Problem 9
If $a$ and $b$ are relatively prime integers and $ab$ is a perfect square, then both $a$ and $b$ are perfect squares.
**Solution:**
Let $a$ and $b$ be coprime integers such that $ab = n^2$ for some integer $n$. Let $a = p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k}$ and $b = q_1^{b_1} q_2^{b_2} \cdots q_m^{b_m}$ be the prime factorizations of $a$ and $b$. Since $\gcd(a,b) = 1$, the sets $\{p_1, p_2, \ldots, p_k\}$ and $\{q_1, q_2, \ldots, q_m\}$ are disjoint. Therefore,
$$ab = p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k} q_1^{b_1} q_2^{b_2} \cdots q_m^{b_m}$$
Since $ab$ is a perfect square, every prime in its factorization must have an even exponent. Thus, $a_i$ is even for all $i = 1, 2, \ldots, k$ and $b_j$ is even for all $j = 1, 2, \ldots, m$. This means:
$$a = \left(p_1^{a_1/2} p_2^{a_2/2} \cdots p_k^{a_k/2}\right)^2 \quad \land \quad b = \left(q_1^{b_1/2} q_2^{b_2/2} \cdots q_m^{b_m/2}\right)^2$$
which are natural numbers to the power of two. Therefore, both $a$ and $b$ are perfect squares. $\blacksquare$
