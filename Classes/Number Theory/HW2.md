1)
($GCD(300, 111)$)
300 = 2(111) + 78
111 = 1(78) + 33
78 = 2(33) + 12
33 = 2(12) + 9
12 = 1(9) + 3
9 = 3(3) + 0
and so we get 3.
($GCD(289, 323)$)
289 = 0(323) + 289
323 = 1(289) + 34
289 = 8(34) + 17
34 = 2(17) + 0
and so we get 17.
($GCD(3939, 10403)$)
3939 = 0(10403) + 3939
10403 = 2(3939) + 2525
3939 = 1(2525) + 1414
2525 = 1(1414) + 1111
1414 = 1(1111) + 303
1111 = 3(303) + 202
303 = 1(202) + 101
202 = 2(101) = 0
and so we get 101.

2)
One obvious solution is $(x, y) = (-50, 50)$. By Corollary 1.25, we see that the general solution is:
$$
x = -50 + n\frac{19}{GCD(19,17)}, y = 50 - n\frac{17}{GCD(19,17)}
$$
(GCD(19, 17)) = 1 by
19 = 1(17) + 2
17 = 8(2) + 1
2 = 2(1)

and so our solution becomes
$$
x = -50 + 19n, y = 50 - 17n
$$
$\blacksquare$

3)
(GCD(10403, 3939)) = 101 by problem 1. One obvious solution is $(x, y) = (24, -9)$. By corollary 1.25 we see that:
$$
x = 24 + 103n, y = -9 - 39n
$$
$\blacksquare$

4)
Suppose a and b are positive integers and $GCD(a, b) = LCM(a, b)$. We see that $GCD(a, b) | a | LCM(a, b)$ and $GCD(a, b) | b | LCM(a, b)$ by definition. It follows, by squeezing, that $a = GCD(a, b) = LCM(a, b) = b$. $\blacksquare$

5)
We can describe all solutions to the Diophantine equation $15x + 35y + 21z = 1$ using methods of this chapter. Notice $15x + 35y = 1$ can never happen because $1$ is not a multiple of $\gcd(15, 35) = 5$. Therefore, we really aim to show $5u + 21z = 1$ where $u = 3x + 7y$. Corollary 1.25 shows us - where $(u, z) = (-4, 1)$ is a solution - that $u = -4 + n\frac{21}{\gcd(5, 21)}$, $z = 1 - n\frac{5}{\gcd(5, 21)}$. It is easy to see that $\gcd(5, 21) = 1$ and so we get $u = -4 + 21n$, $z = 1 - 5n$. Now substituting back $u = 3x + 7y$, we have $3x + 7y = -4 + 21n$, which means $n = \frac{3x + 7y + 4}{21}$. For this to yield integer values of $n$, we need $3x + 7y \equiv -4 \pmod{21}$. The complete solution is therefore: $(x, y, z)$ is a solution to $15x + 35y + 21z = 1$ if and only if $3x + 7y \equiv -4 \pmod{21}$ and $z = 1 - 5n$ where $n = \frac{3x + 7y + 4}{21}$. In other words, we can choose any integers $x, y$ satisfying $3x + 7y \equiv -4 \pmod{21}$, compute $n = \frac{3x + 7y + 4}{21}$, and then set $z = 1 - 5n$. $\blacksquare$

6)
(GCD(, 221, 85)) = 17 because
221 = 2(85) + 51
85 = 1(51) + 34
51 = 1(34) + 17
34 = 2(17)

![[Hasse.png]]