# Chapter 3: Rational And Constructible Numbers
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## #.# Subsection Title
---
### Definitions
- **Rational Number**
  - Expressed as $\frac{a}{b}$ for some integers a and b(non-zero).
  - $\frac{a}{b} = \frac{c}{d}$ if $ad = bc$.
  - Reduced fraction if $GCD(a, b) = 1$ and $b > 0$.
- **Constructible Number**
  - Obtained beginning with a unit line segment and carrying out straight edge compass drawings.
- **Commensurable**
  - There exists a length z and integers m and n such that $x = mz$ and $y = nz$ for lengths x and y.
  - Essentially those with rational quotient.
  - leg and hypotenuse incommensurable.
- **Mediant**
  - $\frac{a}{b} \lor \frac{c}{d} = \frac{a + c}{b + d}$.
- **Kissing Fractions**
  - $\frac{a}{b} \heartsuit \frac{c}{d}$ if $ad -bc = \pm 1$.
- **Ford Circle**
  - Circle of diameter $\frac{1}{b^2}$ above $\frac{a}{b}$ on the number line.
- **Price**
  - Size of fraction denominator.

### Theorems & Proofs
**Theorem 3.1**
If $\frac{a}{b}$ is a fraction with $b \ne 0$, then there exists a unique reduced fraction $\frac{c}{d}$ such that $\frac{a}{b} = \frac{c}{d}$. Moreover, there exists a nonzero integer n such that $a = nc$ and $b = nd$.

Basic divisibility constructions. $\blacksquare$

**Proposition 3.2**
If x is a non-zero rational number, then there exist unique integers $e_2, e_3, e_5, e_7, ...$ such that all but finitely many are zero and $x = \pm 2^{e_2}3^{e_3}5^{e_5}...$.

What does it mean to divide by an integer, how can it be represented? $\blacksquare$

**Theorem 3.3**
Addition, subtraction, multiplication, division, and square roots suffice to describe every constructible number.

How can constructible points be made? How do we find distances? $\blacksquare$

**Theorem 3.4**
There are infinitely man primitive Pythagorean triples. In other words, there are infinitely man triples (a, b, c) of integers for which $GCD(a, b, c) = 1$ and $a^2 + b^2 = c^2$.

Consider the unit circle and a line through (0, 1). $\blacksquare$

**Proposition 3.5**
Let $\frac{a}{b}$ be a reduced fraction with $b > 0$. Then $\sqrt[n]{\frac{a}{b}}$ is a rational number iff a and b are nth powers of integers.

Trivial to prove. $\blacksquare$

**Theorem 3.8**
Let $\frac{a}{b}$ be a reduced fraction, representing a rational number x. Let $c_0, ..., c_d$ be positive integers. Then $c_0 + c_1x + ... + c_{d-1}x^{d-1} + c_dx^d = 0$ implies $a | c_0$ and $b | c_d$.

Fill in x into the equation. $\blacksquare$

**Proposition 3.10**
If n is an integer, $n \ge 3$ and $\cos{\frac{\pi}{n}}$ is a constructible number, then one can inscribe a regular n-gon in a unit circle with only straightedge and compass.

**Proposition 3.11**
Let $\frac{a}{b}$ and $\frac{c}{d}$ be fractions with $b > 0$ and $d > 0$. Then the mediant represents a rational number that lies between $\frac{a}{b}$ and $\frac{c}{d}$.

**Theorem 3.15**
$\frac{a}{b} \heartsuit \frac{c}{d}$ iff the Ford circle atop $\frac{a}{b}$ is tangent to the Ford circle atop $\frac{c}{d}$ and $c, d > 0$.

**Proposition 3.16**
Let $\frac{a}{b}$ and $\frac{c}{d}$ be two kissing fractions. Then the mediant kisses both $\frac{a}{b}$ and $\frac{c}{d}$.

**Proposition 3.17**
If $GCD(a, b) \ne 1$ then $\frac{a}{b}$ kisses no further fractions.

**Proposition 3.18**
Let $\frac{a}{b}$ be a reduced fraction. Then $\frac{a}{b}$ kisses infinitely many fractions. If $b > 1$ then among the reduced fractions kissing $\frac{a}{b}$, there are exactly two with denominator smaller than b. These two fractions kiss each other and have mediant $\frac{a}{b}$.

**Corollary 3.19**
Let $\frac{a}{b}$ be a reduced fraction. Then the Ford circle atop $\frac{a}{b}$ is tangent to infinitely many other Ford circles; if $b > 1$, then two of these have larger diameters and kiss each other.

**Theorem 3.21**
Begin with integer fractions $\frac{n}{1}$ for every integer n. Whenever fractions kiss, take their mediants, and continue this process indefinitely. Only reduced fractions will occur, and all reduced fractions will eventually occur. 

**Proposition 3.22**
Let x be a real number and be be a positive integer. Then there exists a rational number $\frac{a}{b}$ such that $|x - \frac{a}{b} | \le \frac{1}{2b}$.

Imagine circles. $\blacksquare$

**Theorem 3.23**
Let x be an irrational real number. Then there exist infinitely many reduced fractions $\frac{a}{b}$ such that $| x - \frac{a}{b} | < \frac{1}{2b^2}$.

### Examples
**Example Title**
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
Notice $n! \cdot x = \sum_{k = 0}^n \frac{n!}{k}$. Each term is an integer, because k is a product of integers contained in the terms of $n!$. The summation of integers is itself an integer so $n! \cdot x$ is an integer. By definition, $n! \cdot e = n! \cdot \frac{a}{n} = (n-1)! \cdot a$ which is a product of integers and so is an integer itself. e is an infinite summation of positive rational numbers, so y must be non-zero and we see that $n! \cdot y = \sum_{k = n + 1}^\infty \frac{n!}{(k)!}$. Consider geometric series $\sum_{k = 0}^\infty 0.5(0.5)^k$ which converges to 1. Notice $n + 1 \ge 2$ and each sequential term of $n! \cdot y$ gets smaller faster than the geometric series, so $n! \cdot y < 1$. Therefore, $0 < n! \cdot y < 1$. Since $e = x + y$ by definition, we see that $n! e = n! x + n! y$. But $n! y$ is not an integer added to integer $n! x$ which sums to something that is not an integer. However, $n! e$ was determined to be an integer which is a contradiction. Thus, e must not be rational. $\blacksquare$

**Problem 12:**
Prove that if Fermat's Last Theorem is true for a prime exponents p, and for the exponent 4, then Fermat's Last Theorem is true for all exponents $n \ge 3$.
**Solution:**
Suppose Fermat's Last Theorem is true for a prime exponents p, and for the exponent 4. Consider arbitrary $n \ge 3$. If n is prime, then Fermat's Last Theorem is true trivially. If n is not prime, then it is the product of primes $p_1p_2p_3...$. If one prime $p_k$ in the decomposition is not 2, we can set $(x^{p_1p_2p_3...})^{p_k} + (y^{p_1p_2p_3...})^{p_k} = (z^{p_1p_2p_3...})^{p_k}$ which satisfies Fermat's Last Theorem by our assumption. Else, the decomposition of n is just $2^x$ for some x. However, since $n \ge 3$, we see that x must be at least 2. Therefore, by our assumption again, we see that $(x^{2^{x - 2}})^{4} + (y^{2^{x - 2}})^{4} = (z^{2^{x - 2}})^{4}$ satisfies Fermat's Last Theorem. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages 75-98
