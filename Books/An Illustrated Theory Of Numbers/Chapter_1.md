# Chapter 1: The Euclidean Algorithm
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## 1.0 The Euclidean Algorithm
---
### Definitions
- **Greatest Common Divisor**
  - Natural number g is the gcd of a and b if:
  - $g | a$ and $g | b$.
  - If $d | a$ and $d | b$, then $d | g$.
  - $GCD(a,b)$.
- **Least Common Multiple**
  - L is the least common multiple of integer a and b if:
  - $a | L$ and $b | L$.
  - $a | m \land b |m \implies L | m$.
  - $LCM(a,b)$.
### Algorithms
**Euclidean Algorithm**
Input: $a, b \in \mathbb{N}$ with $b \ne 0$.
Output: $gcd(a, b)$.
```pseudo
1. Let r_0 := a, r_1 := b
2. For i = 1,2,3,... do:
	1. Divide r_{i-1} by r_i:
	   r_{i-1} = q_ir_i + r_{i+1}
	If r_{i+1} = 0, stop
Return gcd(a, b) = r_i
```

### Theorems & Proofs
**Proposition 1.2**
Suppose one can hop a units and skip b units, and $a > b$. Then if r is a remainder after dividing a by b, then one can jump r units.

$r = a - q(b)$. **Q.E.D**

**Proposition 1.6**
Let a and b be positive integers with $a > b$. Let $bits(b)$ be the number of bits in the binary expansion of b. Then the euclidean algorithm on a and b, performed with minimal remainders, stops after at most $bits(b)$ steps.

The first remainder is bounded by $0.5b$, and so the first remainder has at most $bits(b) - 1$ bits (if nonzero).The second remainder is bounded by half the first remainder, and so the second remainder has at most $bits(b) - 2$ bits. etc - in step s, the remainder has at most $bits(b) - s$ bits. Therefore, the algorithm must terminate in no more than $bits(b)$ steps.

**Theorem 1.7**
Let a and b be natural numbers, not both zero. The Euclidean algorithm on a and b leads to the gcd of a and b by the final nonzero remainder.

Carry out the algorithm on a and b. In the last line, we find an expression of the form $a_{final} = q_{final}(r_{final}) + 0$, where $r_{final}$ is the final nonzero remainder. Lemma 1.9 states that $GCD(r_{final}, 0) = r_{final}$. Applying Lemma 1.10 to each line of the algorithm, from the bottom up, we find that $GCD(a, b) = r_{final}$. **Q.E.D**

**Lemma 1.9**
If a is a natural number, then $GCD(a, 0) = a$.

Since $a | a$ and $a | 0$, we find that a is a common divisor of a and 0. If $d | a$ and $d | 0$, then in particular $d | a$. Every common divisor of a and 0 is a divisor of a. **Q.E.D**

**Lemma 1.10**
Suppose that a, b, q, r are integers and $a = q(b) + r$. Let g be a natural number. Then $g = GCD(a, b)$ iff $g = GCD(b, r)$.

If $g = GCD(a, b)$, then $g | a$ and $g | b$, and thus $g | r$ by the two-out-of-three principle. Hence g is a common divisor of b and r. If $d | b$ and $d | r$, then $d | a$ by the two-out-of-three principle, hence $d | g$. Thus $g = GCD(b, r)$ as well. Since $r = -q(b) + a$, the same argument demonstrates that if $g = GCD(b, r)$, then $g = GCD(a, b)$. **Q.E.D**

**Theorem 1.14 (Solubility Of Linear Diophantine Equations)**
Let a, b, and c be integers. The equation  $ax + by = c$ has an integer solution (x, y) iff c is a multiple of $GCD(a, b)$.

If x and y are integers, then $ax + by$ is a multiple of $GCD(a, b)$. Hence for $ax + by = c$ to have an integer solution, it is necessary that c be a multiple of $GCD(a, b)$. Suppose c is a multiple of $GCD(a, b)$. Apply the algorithm to the natural numbers $|a|$ and $|b|$. Considering hops of $|a|$ and skips of $|b|$, the remainders provide a sequence of compound moves, culminating in a move by $GCD(a, b)$ - let us call this move a step. By steps, one can travel to every multiple of $GCD(a, b)$. Hence by steps, one can travel to c. So, one can hop and skip to c. Therefore, for $ax + by = c$ to have an integer solution, it suffices that c be a multiple of $GCD(a, b)$. **Q.E.D**

**Lemma 1.18**
Let a and b be integers. If m is a common multiple of a and b, and n is a common multiple of a and b, then $GCD(m, n)$ is a common multiple of a and b.

Since $a | m$ and $a | n$, we find that $a | GCD(m, n)$. Similarly, since $b | m$ and $b | n$, we find that $b | GCD(m, n)$. Hence $GCD(m, n)$ is a common multiple of a and b. **Q.E.D**

**Proposition 1.19**
Let a and b be nonzero integers. Let l be the smallest positive integer which is a common multiple of a and b. The l divides every common multiple of a and b and so $l = LCM(a, b)$.

Let m be a common multiple of a and b. Since l is a common multiple of a and b, we find that $GCD(l, m)$ is a common multiple of a and b. Since $GCD(l, m) | l$ and l is a positive integer, we find that $GCD(l, m) \le l$. But since l was the smallest positive common multiple of a and b, we find that $GCD(l ,m) = l$. Therefore, $l | m$. $\blacksquare$

**Proposition 1.20**
Let a and b be integers. Then for every n, there is an integer solution $(u, v)$ of the equation $au + bv = 0$ given by $u = n\frac{LCM(a, b)}{a}, v = -n\frac{LCM(a,b)}{b}$. All solutions are obtained this way.

If $au + bv = 0$, then $au = -bv$. The left side is evidently a multiple of a and the right side is evidently a multiple of b; since they are equal, they equal a common multiple of a and b. Every common multiple of a and b is a multiple of $LCM(a, b)$. Therefore, for some integer n, $nLCM(a, b) = au = -bv$. Dividing through by a or by -b yields the equations desired. $\blacksquare$

**Theorem 1.21 (General Solution Of Linear Diophantine Equations)**
Let a, b, and c be integers. Suppose that $a \ne 0$ or $b \ne 0$. If c is not a multiple of $GCD(a, b)$ then the equation $ax + by = c$ has no integer solutions. On the other hand, if c is a multiple of $GCD(a, b)$ then the equation $ax + by = c$ has infinitely many solutions. Given one solution $(x_0, y_0)$, all solutions have the form:
$$
x = x_0 + n \frac{LCM(a, b)}{a}, y = y_0 - n\frac{LCM(a,b)}{b}
$$

Theorem 1.14 shows that the equation has a solution iff c is a multiple of $GCD(a, b)$. Suppose $(x_0, y_0)$ is one solution to the equation. Given integers $(x, y)$, we find that $ax + by = c$ iff $a(x - x_0) + b(y - y_0) = 0$. Therefore, $ax + by = c$ iff $u = (x - x_0)$ and $v = (y - y_0)$ are solutions to the homogeneous equation $au + bv = 0$. By proposition 1.20, we see that we get the equations desired through simple algebra. $\blacksquare$

**Theorem 1.23 (GCD-LCM product formula)**
Let a and b be positive integers. Then $GCD(a, b) \times LCM(a, b) = a \times b$.

We will use the reference image 1.15 in the proof. Notice $b = mg$ and $a = ng$. Hence g is a common divisor of a and b. It follows that $g | GCD(a, b)$. Second, observe that $l = av$ and $l = bu$. Hence l is a common multiple of a and b. It follows that $LCM(a, b) | l$. We therefore find $ab = g \cdot LCM(a, b) | GCD(a, b) \cdot LCM(a, b) | GCD(a, b) \cdot l = ab$. It follows that by a squeeze that all intermediate terms are equal:
$$
ab = g \cdot LCM = GCD(a, b) \cdot LCM(a, b) | GCD(a, b) \cdot l = ab
$$
$\blacksquare$

**Corollary 1.25**
Suppose that $(x_0, y_0)$ is a solution to the linear Diophantine equation $ax + by = c$. Then the general solution to this equation is:
$$
x = x_0 + n\frac{b}{GCD(a, b)}, y = y_0 - n\frac{a}{GCD(a, b)}
$$

**Proposition 1.27**
If g, a, and b are integers, and $g > 0$, then $GCD(ga, gb) = gGCD(a, b)$ and $LCM(ga, gb) = gLCM(a, b)$.

When a or b is zero, one may check the result directly. Since $GCD(a, b) = GCD(|a|, |b|)$, we may assume a and b are positive in what follows. Consider the euclidean algorithm applied to a,b alongside ga, gb. $a = qb + r, ga = qgb + gr$. If r is the natural remainder after dividing a by b, then gr is the remainder after dividing ga by gb. If $0 \le r < b$ then $0 \le gr < gb$. Thus $GCD(ga, gb) = GCD(gb, gr)$. In this way, every step of the Euclidean algorithm for ga, gb is obtained by scaling a step of the euclidean algorithm for a, b. Scaling the last nonzero remainders, we find that $gGCD(a, b) = GCD(ga, gb)$. Foe the LCM, we apply Theorem 1.23 to find $LCM(ga, gb) = \frac{gagb}{GCD(ga, gb)} = \frac{g^2ab}{gGCD(a, b)} = gLCM(a, b)$. $\blacksquare$

**Corollary 1.29**
If a and b are integers, not both zero, and $g = GCD(a, b)$, then $GCD(\frac{a}{g}, \frac{b}{g}) = 1$.

We have,
$$
gGCD(\frac{a}{g}, \frac{b}{g}) = GCD(g\frac{a}{g}, g\frac{b}{g}) = GCD(a, b) = g
$$
and so we get $GCD(\frac{a}{g}, \frac{b}{g}) = 1$. $\blacksquare$

### Visual Aids

![[Screenshot from 2026-02-01 14-46-13.png]]

### References
- *Book Title* — Chapter X, Pages Y–43
