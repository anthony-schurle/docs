1) Prove that the equation $x^2 + y^2 + z^2 = 8007$ has no solutions. Demonstrate that there are infinitely many positive integers which cannot be expressed as the sum of three squares.
Suppose $x^2 + y^2 + z^2 = 8007$ did have an integer solution. Then by proposition 5.14, $x^2 + y^2 + z^2 = 8007$ has a solution for every mod m. Let $m = 8$, so that $x^2 + y^2 + z^2 = 8007 \equiv x^2 + y^2 + z^2 = 7$ mod 8. We show that this is not the case, and the equation has no solutions. It suffices to only check when $x^2$, $y^2$, $z^2$ in $\{0, 1, 4\}$ since squares mod 8 only take on these values. Also, order of assignment does not matter (i.e. $(x^2, y^2, z^2) = (1,4, 1) = (4, 1, 1) = ...$) and so we restrict to $x \le y \le z$ WLOG.

| $x^2$ | $y^2$ | $z^2$ | $x^2+y^2+z^2 \pmod{8}$ |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 0 | 4 | 4 |
| 0 | 1 | 1 | 2 |
| 0 | 1 | 4 | 5 |
| 0 | 4 | 4 | 0 |
| 1 | 1 | 1 | 3 |
| 1 | 1 | 4 | 6 |
| 1 | 4 | 4 | 1 |
| 4 | 4 | 4 | 4 |

Therefore, we have reached a contradiction - since 7 is never a result - and so it must be that the equation $x^2 + y^2 + z^2 = 8007$ has no solutions.

It also follows that $x^2 + y^2 + z^2 \not \equiv 7$ mod 8 for any x, y, or z (since $8007 \equiv 7$ mod 8). Therefore, $k \equiv 7$ mod 8 for some k implies it cannot be expressed as the sum of three squares. By showing there are infinite such k, we demonstrate that there are infinitely many positive integers which cannot be expressed as the sum of three squares. By definition of $k \equiv 7$ mod 8, $k - 7 = 8y$  for some y which is equivalent to $k = 7 + 8y$. Since y can be any natural number, there are infinite such k congruent to 7 modulo 8. $\blacksquare$

2) List all irreducible polynomials mod 3, of degree 2.
Such a polynomial can be represented by $a + bT + cT^2$ for integers a, b, and c. Since the polynomial resides in mod 3 and the degree must be 2 (nonzero c), it suffices to check only $a \in \{0, 1, 2\}$, $b \in \{0, 1, 2\}$, and $c \in \{1, 2\}$ - 18 unique polynomials.

| Factorization | Product         | Irreducible? |
| ------------- | --------------- | ------------ |
| $T \cdot T$   | $T^2$           | ✗            |
| $T(T+1)$      | $T^2 + T$       | ✗            |
| $T(T+2)$      | $T^2 + 2T$      | ✗            |
| $(T+1)^2$     | $T^2 + 2T + 1$  | ✗            |
| $(T+1)(T+2)$  | $T^2 + 2$       | ✗            |
| $(T+2)^2$     | $T^2 + T + 1$   | ✗            |
| $2T \cdot T$  | $2T^2$          | ✗            |
| $2T(T+1)$     | $2T^2 + 2T$     | ✗            |
| $2T(T+2)$     | $2T^2 + T$      | ✗            |
| $2(T+1)^2$    | $2T^2 + T + 2$  | ✗            |
| $2(T+1)(T+2)$ | $2T^2 + 1$      | ✗            |
| $2(T+2)^2$    | $2T^2 + 2T + 2$ | ✗            |
| —             | $T^2 + 1$       | ?            |
| —             | $T^2 + T + 2$   | ?            |
| —             | $T^2 + 2T + 2$  | ?            |
| —             | $2T^2 + 2$      | ?            |
| —             | $2T^2 + 2T + 1$ | ?            |
| —             | $2T^2 + T + 1$  | ?            |

Therefore, there are 6 candidate polynomials that are potentially irreducible. By Theorem 5.28, any factorization of the candidates without constant polynomials requires two degree 1 polynomials. Notice any 1 degree polynomial $a + bT$ where $b \ne 0$ is equivalent to $b(T - x)$ where $x = \frac{a}{b}$, and so 1 degree polynomials of the form $T - x$ cover all 1 degree polynomials. By Lemma 5.38, the polynomial $(T - x)$ is a factor iff x is a root of the candidate. Then it suffices to check that the candidates have no root to show that they are irreducible.

| $P(T)$ | $P(0)$ | $P(1)$ | $P(2)$ | Irreducible? |
|---|---|---|---|---|
| $T^2 + 1$ | $1$ | $2$ | $2$ | ✓ |
| $T^2 + T + 2$ | $2$ | $1$ | $2$ | ✓ |
| $T^2 + 2T + 2$ | $2$ | $2$ | $1$ | ✓ |
| $2T^2 + 2$ | $2$ | $1$ | $1$ | ✓ |
| $2T^2 + 2T + 1$ | $1$ | $2$ | $1$ | ✓ |
| $2T^2 + T + 1$ | $1$ | $1$ | $2$ | ✓ |

$\blacksquare$

3) What is the greatest common divisor of $T^6 + 1$ and $T^{15} + 1$, modulo 2? Use the Euclidean algorithm.
$$
T^{15} + 1 \equiv (T^{9} + T^3)(T^6 + 1) + (T^3 + 1)
$$
$$
T^6 + 1 = (T^3 + 1)(T^3 + 1) + 0
$$
and so the GCD is $T^3 + 1$. $\blacksquare$

4) Write a single congruence that is equivalent (same solutions) as the pair of congruence $x \equiv 1$ mod 4 and $x \equiv 2$ mod 3.
$x \equiv 5$ mod 12 is equivalent to the pair. Suppose $x \equiv 5$ mod 12. By definition then, $12 | x - 5$. Since $4 | 12$, it follows that $4 | x - 5$. So $x \equiv 5 \equiv 1$ mod 4 by definition. Since $3 | 12$, it follows that $3 | x - 5$. So $x \equiv 5 \equiv 2$ mod 3 by definition. Therefore, $x \equiv 5$ mod 12 implies the pair of congruence $x \equiv 1$ mod 4 and $x \equiv 2$ mod 3. Now suppose the pair of congruence $x \equiv 1$ mod 4 and $x \equiv 2$ mod 3. Then, by definition, $4 | x - 1$ and $3 | x - 2$. Because $4 | x - 1$ and $4 | 4$, we have $4 | x - 5$. Because $3 | x - 2$ and $3 | 3$, we have $3 | x - 5$. Since $4 | x-5$, for some k we get $x - 5 = 4k$. Now $3 | 4k$, because $3 | x- 5$, and $GCD(4, 3) = 1$ so by Euclid's Lemma - $3 | k$. Hence $k = 3j$ for some j and $x - 5 = 4(3j) = 12j$. By definition then, $12 | x - 5$. Therefore, the pair of congruence $x \equiv 1$ mod 4 and $x \equiv 2$ mod 3 implies $x \equiv 5$ mod 12. Thus, $x \equiv 5$ mod 12 is equivalent to the pair of congruence $x \equiv 1$ mod 4 and $x \equiv 2$ mod 3. $\blacksquare$

5) Let $f(T)$ be a polynomial with integer coefficients and m as modulus. Show that if $x \equiv y$ mod m then $f(x) \equiv f(y)$ mod m.
Suppose $x \equiv y$ mod m and let $f(T) := f_1 + f_2T + f_3T^2 + ... + f_nT^n$ mod m. We see that,
$$
f(x) = f_1 + f_2(x) + f_3(x^2) + ... + f_n(x^n)
$$
and by proposition 5.3 ($x^k \equiv y^k$ for all k),
$$
f_1 + f_2(x) + f_3(x^2) + ... + f_n(x^n) \equiv f_1 + f_2(y) + f_3(y^2) + ... + f_n(y^n) = f(y)
$$
$\blacksquare$

6) Find all solutions to the congruences:
a) $20x \equiv 4$ mod 30
$GCD(30, 20):$
$$
30 = 1(20) + 10
$$
$$
20 = 2(10)
$$
and so $10$. By proposition 5.18, since $GCD(30, 20) = 10$ does not divide $4$, $20x \equiv 4$ mod 30 has no solutions.

b)$353x \equiv 254$ mod 400
$$
400 = 353 + 47 \to 353 = 7(47) + 24 \to 47 = 24 + 23 \to 24 = 23 + 1 \to 23 = 23(1)
$$
and so by theorem 5.20, 353 has multiplicative inverse mod 400. Through back-substitution (or that $17 \times 353 = 6001$), it is easy to see that the inverse is 17 so that $353(17) \equiv 1$ mod 400. So we see that, $x \equiv (353 \cdot 17) x \equiv 17 \cdot 254 \equiv 318$ mod 400.

c) $57x \equiv 87$ mod 105.
By definition of $57x \equiv 87$ mod 105, $57x - 105y = 87$ for some y. Dividing by 3 yields the equation $19x - 35y = 29$ which be definition is equivalent to $19x \equiv 29$ mod 35. Notice $(-11)(19) = -209 \equiv 1$ mod 35. So $-11 \equiv 24$ mod 35 is the multiplicative inverse for 19 in mod 35. Then $x \equiv 24(19)x \equiv 24(29) \equiv 12(58) \equiv 12(23) \equiv 6(46) \equiv 6(11) \equiv 66 \equiv 31$ mod 35. Therefore, $x = 31, 66, 101$ mod 105 are all solutions to $57x \equiv 87$ mod 105. $\blacksquare$

7) Find all the roots of the following polynomials modulo 11.
a) $T^2 - 5$.
Notice when $T = 4$, we get $4^2 - 5 = 11 \equiv 0$ mod 11 and so is a root. When $T = 7$, we have $7^2 - 5 = 44 \equiv 0$ mod 11 and so is a root. By theorem 5.39, $T^2 - 5$ has at most 2 roots and we found exactly two. Therefore, $4$ and $7$ compose all roots of $T^2 - 5$.
b) $T^2 + T - 3$.

| $T$  | $T^2 + T - 3 \pmod{11}$ |
| ---- | ----------------------- |
| $0$  | $-3 \equiv 8$           |
| $1$  | $-1 \equiv 10$          |
| $2$  | $3$                     |
| $3$  | $9$                     |
| $4$  | $17 \equiv 6$           |
| $5$  | $27 \equiv 5$           |
| $6$  | $39 \equiv 6$           |
| $7$  | $53 \equiv 9$           |
| $8$  | $69 \equiv 3$           |
| $9$  | $87 \equiv 10$          |
| $10$ | $107 \equiv 8$          |

Since no value yields $0 \pmod{11}$, the polynomial has no roots mod 11.
c) $T^3 - 5$.
Notice when $T = 3$, we get $3^3 - 5 = 22 \equiv 0$ mod 11 and so is a root. By Lemma 5.38 then, $T - 3$ is a factor of $T^3 - 5$, and so any remaining factors must reside in $\frac{(T^3 - 5)}{T - 3} = T^2 + 3T + 9$. 

| $T$ | $T^2 + 3T + 9 \pmod{11}$ |
|-----|--------------------------|
| $0$ | $9$ |
| $1$ | $13 \equiv 2$ |
| $2$ | $19 \equiv 8$ |
| $3$ | $27 \equiv 5$ |
| $4$ | $37 \equiv 4$ |
| $5$ | $49 \equiv 5$ |
| $6$ | $63 \equiv 8$ |
| $7$ | $79 \equiv 2$ |
| $8$ | $97 \equiv 9$ |
| $9$ | $117 \equiv 7$ |
| $10$ | $139 \equiv 7$ |

Therefore, $T^2 + 3T + 9$ has no roots mod 11, meaning $T = 3$ is the only root of $T^3 - 5$ mod 11. $\blacksquare$
