# Chapter 3

**Problem 2:**
Prove that there are infinitely many positive integer triples (x, y, z) such that $x^2 + 2y^2 = 3z^2$. Hint: Similar to pythagorean triples. 
**Solution:**
Notice, (1, 1, 1) and notice $1^2 + 2(1)^2 = 3(1)^2$ is a solution. Now consider arbitrary natural number k and the solution set $(k, k, k)$. We see that $k^2(1)^2 + 2k^2(1)^2 = 3k^2(1)^2 \implies  1^2 + 2(1)^2 = 3(1)^2$ which was shown to be a solution and so all $(k, k, k)$ are solutions. Thus, because there are infinite natural numbers, there are infinitely many positive integer triples (x, y, z) such that $x^2 + 2y^2 = 3z^2$. $\blacksquare$

**Problem 3:**
Demonstrate that $\sqrt{\frac{5}{7}}$, $\sqrt{3} + \sqrt{5}$, and $\sqrt{8 - \sqrt{7}}$ are irrational.
**Solution:**
It is trivial to see that $\frac{5}{7}$ is a reduced fraction ($GCD(5, 7) = 1$) and since 5 is not the result of an integer to the second power, by proposition 3.5 $\sqrt{\frac{5}{7}}$ is irrational. 
Suppose $x = \sqrt{3} + \sqrt{5}$ is rational. Then we see that $x^4 - 16x^2 +4 = 0$. All reduced fractions that are roots for the equation are $\frac{a}{b}$ where $a | 4$ and $b | 1$. This implies $x = 1, x = -1, x = 2, x = -2, x = 4, x = -4$. None of these are roots to the equation. But this contradicts that x is rational and so x can not be a rational number.
Suppose $x = \sqrt{8 - \sqrt{7}}$ is rational. Then we see that $x^4 - 16x^2 + 57 = 0$. All reduced fractions that are roots for the equation are $\frac{a}{b}$ where $a | 57$ and $b | 1$. This implies $x = 1, x = -1, x= 3, x = -3, x = 19, x = -19, x = 57, x = -57$. None of these are roots to the equation. But this contradicts that x is rational and so x can not be a rational number. $\blacksquare$

**Problem 5:**
The number e is defined as the sum of reciprocals of the factorials. If e were rational, let n be its denominator when represented as a fraction, let x be the sum of the terms up to $\frac{1}{n!}$, and let y be the sum of the rest of the terms. Demonstrate in this case that $n! \cdot x$ is an integer and $n! \cdot e$ is an integer, and that $0 < n! \cdot y < 1$. Use this to achieve a contradiction, and fill in the steps to prove that e is irrational.
**Solution:**
Notice $n! \cdot x = \sum_{k = 0}^n \frac{n!}{k!}$. Each term is an integer, because k is a product of integers contained in the terms of $n!$. The summation of integers is itself an integer so $n! \cdot x$ is an integer. By definition, $n! \cdot e = n! \cdot \frac{a}{n} = (n-1)! \cdot a$ which is a product of integers and so is an integer itself. e is an infinite summation of positive rational numbers, so y must be non-zero and we see that $n! \cdot y = \sum_{k = n + 1}^\infty \frac{n!}{(k)!}$. Consider geometric series $\sum_{k = 0}^\infty 0.5(0.5)^k$ which converges to 1. Notice $n + 1 \ge 2$ and each sequential term of $n! \cdot y$ gets smaller faster than the geometric series, so $n! \cdot y < 1$. Therefore, $0 < n! \cdot y < 1$. Since $e = x + y$ by definition, we see that $n! e = n! x + n! y$. But $n! y$ is not an integer added to integer $n! x$ which sums to something that is not an integer. However, $n! e$ was determined to be an integer which is a contradiction. Thus, e must not be rational. $\blacksquare$

**Problem 12:**
Prove that if Fermat's Last Theorem is true for a prime exponents p, and for the exponent 4, then Fermat's Last Theorem is true for all exponents $n \ge 3$.
**Solution:**
Suppose Fermat's Last Theorem is true for a prime exponents p, and for the exponent 4. Consider arbitrary $n \ge 3$. If n is prime, then Fermat's Last Theorem is true trivially. If n is not prime, then it is the product of primes $p_1p_2p_3...$. If one prime $p_k$ in the decomposition is not 2, we can set $(x^{p_1p_2p_3...})^{p_k} + (y^{p_1p_2p_3...})^{p_k} = (z^{p_1p_2p_3...})^{p_k}$ which satisfies Fermat's Last Theorem by our assumption. Else, the decomposition of n is just $2^x$ for some x. However, since $n \ge 3$, we see that x must be at least 2. Therefore, by our assumption again, we see that $(x^{2^{x - 2}})^{4} + (y^{2^{x - 2}})^{4} = (z^{2^{x - 2}})^{4}$ satisfies Fermat's Last Theorem. $\blacksquare$

# Chapter 4

**Problem 1:**
(Gaussian) Express your answers in the form $x + yi$.
a) $1 + 3i + 2 - 5i = ?$
b) $(1 + 3i) \cdot (2 - 5i) = ?$
c) $(1 + i)^{10} = ?$
d) $1 + 2i + 3 + 4i + ... + 99 + 100i = ?$
**Solution:**
a)
$3 - 2i$.

b)
$2 + 6i - 5i - 15i^2 = 17 + i$.

c)
$(1 + i)^{10} = (1 + i)^{2^3 + 2^1} = (((i + 1)^2)^2)^2 \cdot (i + 1)^2 = 32i$.

d)
$$
1 + 2i + 3 + 4i + ... + 99 + 100i = 2i( 1+ 2 + 3... + 50) + (1 + 99 + 3 + 97 + ... + 47 + 53)
$$
$$
= 2i(25)(51) + 100(25) = 2500 + 2550i
$$

**Problem 2:**
(Eisenstein) Express your answers in the form $x + y\omega$.
a) $2 + 5\omega - 1 - 7\omega = ?$
b) $(2 + 3\omega) \cdot (5 - \omega) = ?$
c) $(1 - \omega)^5  = ?$
d) $0 + 1\omega + 2\omega^2 + 3\omega^3 + ... + 99\omega^{99} = ?$
**Solution:**
a)
$1 - 2\omega$.

b)
$10 + 15\omega - 2\omega - 3\omega^2 = 13 + 16\omega$.

c)
$(1 - \omega)^5 = ((1 - \omega)^2)^2 \cdot (1 - \omega) = 9(-2 - \omega)$.

d)
$$
1(\omega) + 2(-1 - \omega) + 3(-1) + 4(\omega) + 5(-1 - \omega) + ...
$$
$$
= \omega (1 + 4 + 7 + ... + 97) + (-1 - \omega)(2 + 5 + 8 + ... + 98) + (1)(3 + 6 + 9 + ... + 99)
$$
$$
= \omega(98(16) + 49) + (-1 - \omega)(100(16) + 50) + (1)(102(16) + 51)
$$
$$
= 1617\omega - 1650 - 1650\omega + 1683   = 33 - 33\omega
$$

**Problem 3:**
Factor 85 into Gaussian primes.
**Solution:**
$$
85 = 17 \cdot 5 = (4 - i)(4 + i) \cdot (2 - i)(2 + i)
$$

**Problem 4:**
Plot the Gaussian multiples of $3 + i$ on graph paper. Divide 11 by $3 + i$ with remainder, as Gaussian integers.
**Solution:**
![[IMG_1416.png]]

$11 = (3 - i)(3 + i) + 1$.

**Problem 6:**
Use the identity $e(\theta) = \cos{\theta} + i\sin{\theta}$ to prove that $e(\theta + \phi) = e(\theta) \cdot e(\phi)$ for any angles $\theta$ and $\phi$. Hint: recall the formulae for $\cos{\theta + \phi}$ and $\sin{\theta + \phi}$.
**Solution:**
$$
e(\theta + \phi) = \cos{(\theta + \phi)} + i\sin{(\theta + \phi)} = \cos\theta \cos\phi - \sin\theta \sin\phi + (\sin\theta \cos\phi) i + (\cos\theta \sin\phi) i
$$
$$
= (\cos{\theta} + i\sin{\theta}) (\cos{\phi} + i\sin{\phi}) = e(\theta)e(\phi)
$$
$\blacksquare$

**Problem 8:**
Let n be a positive integer. Let $S = e(\frac{2\pi}{n})$. Prove that $1 + S + S^2 + ... + S^{n-1} = 0$. Hint: Show that the sum equals itself times S.
**Solution:**
$$
S(1 + S + S^2 + ... + S^{n-1}) = S + S^2 + ... + S^n
$$
$$
= S + S^2 + ... + (e^{\frac{i2\pi}{n}})^n = 1 + S + S^2 + ... + S^{n-1}
$$
and so,
$$
(1 + S + S^2 + ... + S^{n-1})(S - 1) = 0
$$
Since $S = e\left(\frac{2\pi}{n}\right) = e^{\frac{2\pi i}{n}} = 1$ only when $n = 1$, we have $S \neq 1$ for all $n > 1$. Therefore $(S-1) \neq 0$, and since $(1 + S + S^2 + \cdots + S^{n-1})(S-1) = 0$, we may divide both sides by $(S-1)$ to conclude $1 + S + S^2 + \cdots + S^{n-1} = 0$. We note the statement requires $n > 1$, as for $n = 1$ we have $S = 1$ and the sum equals 1, not 0. $\blacksquare$