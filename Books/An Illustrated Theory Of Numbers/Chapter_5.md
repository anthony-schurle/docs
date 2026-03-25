# Chapter 5: The Modular Worlds
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## #.# The Modular Worlds
---
### Definitions
- **Congruence**
  - Let m be a positive integers (the modulus). $x \equiv y$ modulo m if their difference is a multiple of m.
- **System Of Representatives**
  - Every number n mod m is congruent to an element of the system.
  - No two elements of the system are congruent to each other.
  - Natural representatives are typically natural numbers
  - Minimal representatives include negative numbers to have lowest absolute value members.
- **Polynomials**
  - Degree determined by modulus on coefficients.
  - Roots determined by congruence to 0, and so are all equivalent.
  - Polynomial A divides B if there exists C such that $B \equiv AC$ mod p.
  - The absolute value of polynomial A for prime modulus p is $|A| = p^{deg(A)}$, and $|0| = 0$.
  - Units are constant polynomials.
- **Irreducible Polynomials**
  - Polynomial P such that $deg(P) \ne 0$ and if A and B are polynomials with $AB \equiv P$ mod p, then A or B is a constant.

### Theorems & Proofs
**Proposition 5.3**
If $x \equiv x'$ and $y \equiv y'$ mod m, then $x \pm y \equiv x' \pm y'$ and $x \cdot y \equiv x' \cdot y'$ mod m.

**Proposition 5.9**
Let N be a positive integer. Let S be the sum of the base-ten digits of N. Then $N \equiv S$ mod 3 and $N \equiv S$ mod 9.

**Corollary 5.10**
Let N be a positive integer. Then N is divisible by 3 or 9 iff the sum of the digits of N is divisible by 3 or 9.

**Proposition 5.14**
Let (E ) be an equation, involving only integers, variables, addition, multiplication, and equality. If (E) has an integer solution, then the congruence (E mod m) has a solution for every modulus m.

**Theorem 5.15**
Every natural number can be expressed as the sum of four squares.

**Proposition 5.18**
The congruence $ax \equiv b$ mod m has a solution iff $GCD(a, m)$ divides b.

**Theorem 5.20**
Let m be a positive integer. Let a be an integer. Then a has a multiplicative inverse, mod m, iff $GCD(a, m) = 1$. Moreover, any two multiplicative inverses of a, mod m, are congruent mod m.

**Corollary 5.21**
Let p be a prime number and a an integer. Then a has a multiplicative inverse, mod p, iff $a \not \equiv 0$ mod p.

**Corollary 5.23**
Let m be a positive integer and a an integer satisfying $GCD(a, m) = 1$. Then for all integers x and y, $ax \equiv ay$ mod m implies $x \equiv y$ mod m.

**Corollary 5.24**
Let p be a prime number. If $a \not \equiv 0$ mod p then for all integers x and y, $ax \equiv ay$ mod p implies $x \equiv y$ mod p.

**Proposition 5.26**
Let $F = a + bT$ be a polynomial, and p be a prime number. If $b \not \equiv 0$ mod p, then there exists a unique root of F, mod p. If $b \equiv 0$ mod p, and $a \not \equiv 0$ mod p, then F has no roots, mod p.

**Theorem 5.28**
If A and B are nonzero polynomials mod p, then $deg(AB) = deg(A) + deg(B)$.

**Corollary 5.29**
If A and B are polynomials mod p, then $|AB| = |A| \cdot |B|$.

**Corollary 5.30**
If A and B are polynomials and $B \ne 0$, then $|A| \le |AB|$. Equivalently, $deg(A) \le deg(AB)$.

**Proposition 5.31**
$|A| = 1$ iff there exists a polynomial B such that $A \cdot B \equiv 1$ mod p.

**Ultrametric Triangle Inequality**
If A and B are polynomials mod p, then $|A + B | \le max(|A|, |B|)$.

**Lemma 5.33**
Let B be a nonzero polynomial mod p. Suppose that $Q_1, Q_2$ and $R_1, R_2$ are polynomials, with $|R|_1 < |B|$ and $|R|_2 < |B|$. If $Q_1B + R_1 \equiv Q_2B + R_2$ mod p, then $Q_1 \equiv Q_2$ mod p and $R_1 \equiv R_2$ mod p.

**Lemma 5.34**
If A is a polynomial, then the number of polynomials P mod p satisfying $|P| < |A|$ is equal to $|A|$.

**Theorem 5.35**
If A and B are polynomials, and $B \ne 0$, then there exist polynomials Q, R, such that $A \equiv QB + R$ mod p and $|R| < |B|$.

**Theorem 5.36**
If A is a nonzero polynomial, then A can be decomposed uniquely into irreducible polynomials.

**Proposition 5.37**
If $deg(P) = 1$, then P is irreducible.

**Lemma 5.38**
Suppose that x is a root of a polynomial P, mod p. Then the irreducible polynomial $(T - x)$ is a factor of P.

**Theorem 5.39**
Let P be a nonzero polynomial, mod p. The number of roots of P (mod p) is less than or equal to the degree of P.

**Theorem 5.40**
The number of irreducible polynomials mod p is infinite.

**Theorem 5.41**
Let d be a positive integer. The number of irreducible monic polynomials of degree d, mod p, satisfy the estimate: $|\pi(p;d) - \frac{p^d}{d} | \le 2 \frac{p^{0.5d}}{d}$.

### Examples
**Example Title**
**Problem 1:**
Problem Statement.
**Solution:**
a)
$3u \equiv 5v$ modulo 7.

b)
$x^2 - 1 \equiv 0$ modulo 10.

c)
$$
x \equiv 0 \text{ mod } 2 \implies x^2 \equiv 0 \text{ mod } 4
$$

d)
$$
x - 1 \equiv 0 \text{ mod } 4
$$

e)
$$
x - 2 \equiv 0 \text{ mod } 10
$$

f)
When $e \equiv 0 \text{ mod } 2$, we have $10^e \equiv 1 \text{ mod } 11$.

g)
$$
1 - 11x \equiv 0 \text{ mod } 13
$$

h)
$$
x \equiv 0 \text{ mod } 2 \land x \equiv 0 \text{ mod } 3 \implies x \equiv 0 \text{ mod } 6
$$
$\blacksquare$

**Problem 2:**
Problem Statement.
**Solution:**
a)
$$
= 3 \times 2 \times 1 \times 0 \times ... = 0
$$

b)
$$
37^5 \to 2^5 = 32 \to 2
$$

c)
$$
= \frac{25(26)}{2} = 25 \times 13 \to 12 \times 0 = 0
$$

d)
$$
= \frac{101(102)(203)}{6} = 101 \times 17 \times 203 \to 2 \times 2 \times 2 = 6 \to 0
$$

**Problem 3:**
Let N be a positive integer with units digits u, tens digits t, hundreds digit h, thousands digit s, etc. Let A = u - t + h - s .... Demonstrate that N \equiv A mod 11. Is 123456789 divisible by 11?
**Solution:**
First, consider $10^k$ modulo 11, which is $(-1)^k$ under minimal representatives. Clearly, this is 1 when k is even and -1 when k is odd. Notice $N = 1(u) + 10(t) + 100(h) + ...$ so that N mod 11 in minimal representatives is $1(u) - 1(t) + 1(h) - 1(s) + ... = A$. It follows that $N \equiv A$ mod 11.

We now apply this to the number 123456789. $A = 1 - 2 + 3 - ... = 5$ and so $123456789 \equiv 5$ modulo 11, meaning 123456789 is not divisible by 11. $\blacksquare$

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
This problem is equivalent to finding primes which satisfy $p \equiv 5 \pmod 6$. For the sake of contradiction, suppose there were finitely many primes in such a sequence, labeled $p_1, p_2, \dots, p_n$. Consider the quantity $Q = 6(p_1 p_2 \dots p_n) - 1$. Note that $Q \equiv -1 \equiv 5 \pmod 6$. Since $Q > 1$, it must have a prime factorization. Furthermore, because $Q$ is odd, $2$ does not divide $Q$, and because $Q = 6(p_1 \dots p_n) - 1$, $3$ does not divide $Q$. Thus, all prime factors of $Q$ must be of the form $6k+1$ or $6k+5$. If all prime factors of $Q$ were of the form $6k+1$, their product would also be of the form $6k+1$. However, we know $Q \equiv 5 \pmod 6$. Therefore, $Q$ must have at least one prime factor $q$ of the form $6k+5$. This prime $q$ must be one of the primes in our finite list $\{p_1, p_2, \dots, p_n\}$. But if $q$ divides $Q$ and $q$ also divides $6(p_1 p_2 \dots p_n)$, then $q$ must divide the difference, which is $1$. Since no prime divides $1$, we have reached a contradiction. Our assumption that there were finitely many such primes must be false. Thus, there are infinitely many primes in the sequence. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–152
