# Chapter 4: Gaussian And Eisenstein Integers
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## #.# Subsection Title
---
### Definitions
- **Complex Numbers**
  - On a plane, not a line.
  - Has a real part and imaginary part sometimes represented as a pair.
  - Absolute value is distance from 0.
  - Complex conjugate defined by $\overline{x + yi} = x - yi$ or $\overline{r \cdot e(\theta)} = r \cdot e(-\theta)$.
  - $|z|^2 = z \cdot \overline{z}$ (trivial to check).
- **Gaussian Integers**
  - Complex numbers $x + yi$ where x and y are integers.
  - Closed under addition, subtraction, products, and conjugates.
  - Gaussian units are 1, -1, i, and -i.
  - $|G(r) - \pi r^2 | \le \pi \sqrt{2} \cdot r + \frac{\pi}{2}$.
  - Euclidean algorithm works.
  - Integer q is prime if not a unit and if z and w are integers with $zw = q$, then z or w is a unit.
- **Eisenstein Integers**
  - Complex numbers $x + y\omega$ in which x and y are integers and $\omega = e(\frac{2\pi}{3})$.
  - $\omega^2 = -1 - \omega$ and $\omega^3 = 1$.
  - Closed under addition, subtraction, products, and conjugates.
  - Eisenstein units are 1, -1, $\omega$, $-\omega$, $\omega^2$, and $-\omega^2$.
  - $|E(r) - \frac{2\pi}{\sqrt{3}}r^2 | \le \frac{4\pi}{3}r + \frac{2\pi}{3\sqrt{3}}$.
- Integer q is prime if not a unit and if z and w are integers with $zw = q$, then z or w is a unit.
- **Prime Integer**
  - Integer p that is not a unit (1 or -1).
  - If x and y are integers, and $xy = p$, then x or y is a unit.
- **Inert**
  - Prime p lies below type I Gaussian prime q.
- **Ramified**
  - Prime p lies below type R Gaussian prime q.
- **Split**
  - Prime p lies below type S Gaussian prime q.

### Theorems & Proofs
**Proposition 4.3**
Let $r \cdot e(\theta)$ and $s \cdot e(\phi)$ be two complex numbers in polar form. Then $(r \cdot e(\theta)) \cdot (s \cdot e(\phi)) = rs \cdot e(\theta + \phi)$.

Consider eulers formula $e(\theta) = e^{i\theta}$. $\blacksquare$ 

**Proposition 4.5**
For all complex number z and w, $\overline{z} + \overline{w} = \overline{z + w}$, $\overline{z} - \overline{w} = \overline{z - w}$, and $\overline{z} \cdot \overline{w} = \overline{zw}$.

**Proposition 4.6**
If $z | w$ and $w \ne 0$, then $|z| \le |w|$.

**Conjecture 4.9**
For every positive real number $\epsilon$, there exists a positive constant $K_\epsilon$ such that $|G(r) - \pi r^2 | \le K_\epsilon r^{\frac{1}{2} + \epsilon}$ for all positive r.

**Conjecture 4.10**
For every positive real number $\epsilon$, there exists a positive constant $K_\epsilon$ such that $|E(r) - \frac{2\pi}{\sqrt{3}}r^2 | \le K_\epsilon r^{\frac{1}{2} + \epsilon}$ for all positive r.

**Theorem 4.11**
Let both and b be Gaussian integers or both be Eisenstein integers with $b \ne 0$. Then there exist Gaussian or Eisenstein integers q and r, such that $a = q(b) + r$ and $|r| \le |b| \frac{\sqrt{2}}{2}$ or $|r| \le |b| \frac{\sqrt{3}}{3}$ in the Gaussian or Eisenstein cases respectively.

**Theorem 4.13**
If z is a nonzero Gaussian or Eisenstein integer, then z can be expressed as a product of primes. This prime decomposition is unique, in the sense that any two such decompositions differ only by rearrangement and units.

**Proposition 4.15**
If q is a Gaussian or Eisenstein prime, and u is a unit, then uq is a Gaussian or Eisenstein prime.

**Proposition 4.16**
If q is a Gaussian or Eisenstein prime then $\overline{q}$ is a Gaussian or Eisenstein prime.

**Proposition 4.17**
Suppose that z, w, are integers. Then $z | w$ as Gaussian or Eisenstein integers iff $z | w$ as integers.

**Theorem 4.18**
Let p be a prime number. Then exactly one of the following two statements is true:
1) p lies below a prime q ($q | p$) of type R or S (in visual aids), and $p = q\overline{q}$. Moreover, p lies below the primagons of q and $\overline{q}$ and no others.
2) p itself is a Gaussian or Eisenstein prime of type I. p lies below its own primagon and no others.

**Corollary 4.19**
If p lies below a Gaussian or Eisenstein prime q, then p is a factor of $q\overline{q}$.

**Theorem 4.20**
Let q be a Gaussian or Eisenstein prime. Then q lies above ($p | q\overline{q}$) exactly one prime number p. Exactly one of the following statements is true about p and q:
1) q is a prime of type R or S, and $q\overline{q} = P$.
2) q is a Gaussian or Eisenstein prime of type I, $q\overline{q} = p^2$, and p lies in the primagon of q.

**Corollary 4.21**
If p is a factor of $q\overline{q}$, then q is a Gaussian or Eisenstein prime factor of p.

**Proposition 4.22**
The only prime number which ramifies is 2. (Gaussian)

**Proposition 4.23**
Let p be an odd prime number. Then p splits iff p can be expressed as the sum of two squares. (Gaussian)

**Theorem 4.24**
Let p be an odd prime number. Then  p can be expressed as the sum of two squares iff $p - 1$ is a multiple of 4. (Gaussian)

**Proposition 4.25**
The only prime number which ramifies is 3.

**Proposition 4.26**
Let p be a prime number with $p \ne 3$. Then p splits iff there exist integers x and y such that $p = x^2 - xy + y^2$.

**Theorem 4.27**
Let p be a prime number with $p \ne 3$. Then p can be expressed as $x^2 - xy + y^2$ iff $p - 1$ is a multiple of 3.

### Visual Aids
![[Screenshot from 2026-02-21 13-39-03.png]]

### Examples
**Example Title**
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
$(1 + i)^{10} = (1 + i)^{2^3 + 2^1} = (((i + 1)^2)^2)^2 \cdot (i + 1)^2 = 16 + 2i$.

d)
$$
1 + 2i + 3 + 4i + ... + 99 + 100i = 2i( 1+ 2 + 3... + 50) + (1 + 99 + 3 + 97 + ... + 47 + 53)
$$
$$
= 2i(25)(51) + 100(50) = 5000 + 2550i
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
= \omega (1 + 4 + 7 + ... + 100) + (-1 - \omega)(2 + 5 + 8 + ... + 98) + (-1)(3 + 6 + 9 + ... + 99)
$$
$$
= \omega(101)(17) + (-1 - \omega)(101(16) + 50) + (-1)(101(16) + 51)
$$
$$
= 1717\omega - 1666 - 1666\omega -16667   = -3333 + 51\omega
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
e(\theta + \phi) = e^{i(\theta + \phi)} = e^{i\theta}e^{i\phi} = e(\theta)e(\phi)
$$

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
Two potential roots are $S = 1$ and $1 + S + S^2 + ... + S^{n-1} = 0$. However, $S = 1$ is true precisely when $n = 1$ which the sum converges trivially to 1. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–123
