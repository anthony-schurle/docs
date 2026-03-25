**Problem 1:**
Translate to congruences:
a) $3u - 5v$ is a multiple of 7
b) 10 divides $x^2 - 1$
c) If x is an even number, then $x^2$ is a multiple of 4.
d) x belongs to the sequence $..., -7, -3, 1, 5, 9, 13, 17, ...$.
e) x belongs to the sequence $-18, -8, 2, 12, 22, 32, ...$.
f) When e is even, $10^e$ leaves a remainder 1 when divided by 11.
g) The linear Diophantine equation $11x + 13y = 1$ has a solution.
h) If x is a multiple of 2 and of 3, then x is a multiple of 6.
**Solution:**
a) $3u \equiv 5v \pmod{7}$ 
b) $x^2 \equiv 1 \pmod{10}$ 
c) $x \equiv 0 \pmod{2} \implies x^2 \equiv 0 \pmod{4}$ 
d) $x \equiv 1 \pmod{4}$ 
e) $x \equiv 2 \pmod{10}$ 
f) $e \equiv 0 \pmod{2} \implies 10^e \equiv 1 \pmod{11}$ 
g) $11x \equiv 1 \pmod{13}$ 
h) $x \equiv 0 \pmod{2} \land x \equiv 0 \pmod{3} \implies x \equiv 0 \pmod{6}$
$\blacksquare$

**Problem 2:**
Simplify with natural representatives:
a) $10 \times 9 \times 8 \times ... \times 1$ mod 7
b) $37^5$ mod 5
c) $1 + 2 + 3 + ... + 23 + 24 + 25$ mod 13
d) $1^2 + 2^2 + 3^2 + ... + 101^2$ mod 3.
**Solution:**
a) Since $7$ is a factor in the product, $7 \equiv 0 \pmod{7}$. Thus, the entire product is $\equiv 0 \pmod{7}$.

b) Since $37 \equiv 2 \pmod{5}$, then $37^5 \equiv 2^5 \pmod{5}$. $2^5 = 32$. $32 \equiv 2 \pmod{5}$.

c) Using the summation formula $\frac{n(n+1)}{2}$: $\frac{25(26)}{2} = 25 \times 13$. Since $13 \equiv 0 \pmod{13}$, the sum is $\equiv 25 \times 0 \equiv 0 \pmod{13}$.

d) Note that $n^2 \equiv 1 \pmod{3}$ if $n$ is not a multiple of 3, and $n^2 \equiv 0 \pmod{3}$ if $n$ is a multiple of 3. In the sequence $1, \dots, 101$, there are $33$ multiples of $3$ ($3, 6, \dots, 99$) and $101 - 33 = 68$ non-multiples. The sum becomes $68(1) + 33(0) \equiv 68 \pmod{3}$. Since $68 = 3(22) + 2$, the natural representative is $2 \pmod{3}$.

**Problem 3:**
Let N be a positive integer with units digits u, tens digits t, hundreds digit h, thousands digit s, etc. Let $A = u - t + h - s ...$. Demonstrate that $N \equiv A$ mod 11. Is 123456789 divisible by 11?
**Solution:**
First, consider $10^k$ modulo 11, which is $(-1)^k$ under minimal representatives. Clearly, this is 1 when k is even and -1 when k is odd. Notice $N = 1(u) + 10(t) + 100(h) + ...$ so that N mod 11 in minimal representatives is $1(u) - 1(t) + 1(h) - 1(s) + ... = A$. It follows that $N \equiv A$ mod 11.

We now apply this to the number 123456789. $A = 5$ and so $123456789 \equiv 5$ modulo 11, meaning 123456789 is not divisible by 11. $\blacksquare$

**Problem 4**
Using the result from Problem 3, prove that a palindromic number with an even number of digits is divisible by 11.
**Solution:**
Represent the length of the palindrome number by the letter $p$, where $p = 2k$ for some positive integer $k$. Let the digits of the number $N$ be denoted by $d_{2k-1}, d_{2k-2}, \dots, d_1, d_0$. By the definition of a palindrome, the digits are symmetric such that $d_i = d_{2k-1-i}$ for all $0 \le i < 2k$. From the result in Problem 3, we know that $N \equiv A \pmod{11}$, where $A$ is the alternating sum of the digits $A = \sum_{i=0}^{2k-1} (-1)^i d_i$. Because there are an even number of terms ($2k$), we can group them into $k$ pairs that represent the symmetric positions of the palindrome. We rewrite the sum as $A = (d_0 - d_{2k-1}) + (d_2 - d_{2k-3}) + \dots + (d_{2k-2} - d_1)$. Since the property of a palindrome dictates that $d_i = d_{2k-1-i}$, each difference in the parentheses is exactly $0$. Consequently, the total sum $A$ must equal $0$. Since $N \equiv A \equiv 0 \pmod{11}$, it follows that $N$ is divisible by 11. $\blacksquare$

**Problem 6**
Solve the congruences $5x \equiv 11 \pmod{37}$ and $11y \equiv 5 \pmod{37}$. If both are satisfied, simplify $xy \pmod{37}$.
**Solution:**
To solve the first congruence $5x \equiv 11 \pmod{37}$, we look for the modular inverse of $5$ modulo $37$. We observe that $5 \times 15 = 75$. Since $75 = 2 \times 37 + 1$, it follows that $75 \equiv 1 \pmod{37}$, so $15$ is the modular inverse of $5$. Multiplying both sides of the congruence by $15$, we get $x \equiv 11 \times 15 \pmod{37}$, which simplifies to $x \equiv 165 \pmod{37}$. Since $165 = 4 \times 37 + 17$, we find the unique solution $x \equiv 17 \pmod{37}$.

To solve the second congruence $11y \equiv 5 \pmod{37}$, we find the modular inverse of $11$ modulo $37$. We note that $11 \times 10 = 110$ and $37 \times 3 = 111$. This means $110 \equiv -1 \pmod{37}$. To get a remainder of $1$, we multiply by $-1$, yielding $11 \times (-10) \equiv 1 \pmod{37}$. The inverse is $-10$, which is equivalent to $27 \pmod{37}$. Multiplying the original congruence by $27$, we get $y \equiv 5 \times 27 \pmod{37}$, which simplifies to $y \equiv 135 \pmod{37}$. Since $135 = 3 \times 37 + 24$, we find $y \equiv 24 \pmod{37}$.

Finally, to simplify $xy \pmod{37}$, we substitute the values found: $17 \times 24 = 408$. We reduce this modulo $37$ by dividing $408$ by $37$. We find that $37 \times 11 = 407$. Therefore, $408 = 407 + 1$, which means $xy \equiv 1 \pmod{37}$. $\blacksquare$

**Problem 7**
Find the multiplicative inverse of 4, or prove that one does not exist, modulo 30, 31, 32, 33, 34, and 35.
**Solution:**
Notice $\text{GCD}(30, 4) = 2$, and so by Theorem 5.20, 4 does not have a multiplicative inverse modulo 30 because the greatest common divisor is not 1. Notice $4 \times 8 = 32$, which is $1 \pmod{31}$, and so 8 is the multiplicative inverse of 4 modulo 31. Notice $\text{GCD}(32, 4) = 4$, and so 4 does not have a multiplicative inverse modulo 32. Notice that $4 \times 25 \equiv 1 \pmod{33}$. Thus, 25 is the multiplicative inverse of 4 modulo 33. For modulo 34, we observe that $\text{GCD}(34, 4) = 2$. Since the greatest common divisor is not 1, 4 does not have a multiplicative inverse modulo 34. Notice that $4 \times 9 \equiv 1 \pmod{35}$. Thus, 9 is the multiplicative inverse of 4 modulo 35. $\blacksquare$

**Problem 9**
Prove that there are infinitely many primes in the sequence $5, 11, 17, 23, 29, 35, 41, ...$.
**Solution:**
This problem is equivalent to finding primes which satisfy $p \equiv 5 \pmod 6$. For the sake of contradiction, suppose there were finitely many primes in such a sequence, labeled $p_1, p_2, \dots, p_n$. Consider the quantity $Q = 6(p_1 p_2 \dots p_n) - 1$. Note that $Q \equiv -1 \equiv 5 \pmod 6$. Since $Q > 1$, it must have a prime factorization. Furthermore, because $Q$ is odd, $2$ does not divide $Q$, and because $Q = 6(p_1 \dots p_n) - 1$, $3$ does not divide $Q$. Thus, all prime factors of $Q$ must be of the form $6k+1$ or $6k+5$. If all prime factors of $Q$ were of the form $6k+1$, their product would also be of the form $6k+1$. However, we know $Q \equiv 5 \pmod 6$. Therefore, $Q$ must have at least one prime factor $q$ of the form $6k+5$. This prime $q$ must be one of the primes in our finite list $\{p_1, p_2, \dots, p_n\}$. But if $q$ divides $Q$ and $q$ also divides $6(p_1 p_2 \dots p_n)$, then $q$ must divide the difference, which is $1$. Since no prime divides $1$, we have reached a contradiction. Thus, there are infinitely many primes in the sequence. $\blacksquare$

**PSET Problem 8**
Give a complete set of representatives mod 17 where each representive is
divisible by 3. If this is not possible, explain why.
**Solution**
Such a set is $\{3k : k = 0, 1, 2, \dots, 16\}$. Each element is divisible by 3, and because $\text{GCD}(3, 17)=1$, no two elements are congruent modulo 17. In addition, each term is congruent to a natural representative modulo 17 and so the set is complete. $\blacksquare$
