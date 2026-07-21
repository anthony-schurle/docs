**Problem 1.**
(a) Find all the squares modulo $7,11,13,17,19,$ and $23$. (b) For which of the above primes is $5$ a square? Can you guess whether $5$ is a square modulo $97$?
**Solution.**
For (a), including $0$, the squares modulo each prime are as follows:
$$
\begin{array}{c|l}
p & \text{Squares modulo }p\\
\hline
7 & \{0,1,2,4\}\\
11 & \{0,1,3,4,5,9\}\\
13 & \{0,1,3,4,9,10,12\}\\
17 & \{0,1,2,4,8,9,13,15,16\}\\
19 & \{0,1,4,5,6,7,9,11,16,17\}\\
23 & \{0,1,2,3,4,6,8,9,12,13,16,18\}
\end{array}
$$
For (b), from the table, $5$ is a square modulo $11$ and $19$, and is not a square modulo $7,13,17,$ or $23$. Using theorem 8.22, Quadratic Reciprocity, since $5 \equiv 1 \pmod 4$, we have $\left(\frac{5}{p}\right)=\left(\frac{p}{5}\right)$, so $5$ is a square modulo $p$ exactly when $p \equiv \pm 1 \pmod 5$. Since $97 \equiv 2 \pmod 5$, we guess that $5$ is not a square modulo $97$. This guess is correct. $\proofend$

**Problem 2.**
Chapter 8, Exercise 1: Compute the following Legendre symbols, and interpret them in terms of squareness: $\left(\frac{3}{7}\right)$, $\left(\frac{2}{37}\right)$, $\left(\frac{-5}{29}\right)$, $\left(\frac{105}{101}\right)$, $\left(\frac{23}{37}\right)$, and $\left(\frac{62}{71}\right)$.
**Solution.**
The values and interpretations are:
$$
\begin{array}{c|c|l}
\text{Symbol} & \text{Value} & \text{Interpretation}\\
\hline
\left(\frac{3}{7}\right) & -1 & x^2 \equiv 3 \pmod 7 \text{ has no solutions}\\
\left(\frac{2}{37}\right) & -1 & x^2 \equiv 2 \pmod {37} \text{ has no solutions}\\
\left(\frac{-5}{29}\right) & 1 & x^2 \equiv -5 \pmod {29} \text{ has two solutions}\\
\left(\frac{105}{101}\right) & 1 & x^2 \equiv 105 \pmod {101} \text{ has two solutions}\\
\left(\frac{23}{37}\right) & -1 & x^2 \equiv 23 \pmod {37} \text{ has no solutions}\\
\left(\frac{62}{71}\right) & -1 & x^2 \equiv 62 \pmod {71} \text{ has no solutions}
\end{array}
$$
We have $\left(\frac{3}{7}\right)=-1$ since the nonzero squares modulo $7$ are $1,2,4$. Also, $\left(\frac{2}{37}\right)=-1$ since $37 \equiv 5 \pmod 8$, using theorem 8.10, the reciprocity law for $2$. Next, $\left(\frac{-5}{29}\right)=\left(\frac{-1}{29}\right)\left(\frac{5}{29}\right)=1\cdot \left(\frac{29}{5}\right)=\left(\frac{4}{5}\right)=1$, using corollary 8.6 and theorem 8.22. Thus $x^2 \equiv -5 \pmod {29}$ has two solutions, in fact $x \equiv 13,16 \pmod {29}$. Next, $105 \equiv 4 \pmod {101}$, so $\left(\frac{105}{101}\right)=\left(\frac{4}{101}\right)=1$, and the solutions are $x \equiv \pm 2 \pmod {101}$. For $\left(\frac{23}{37}\right)$, Quadratic Reciprocity gives $\left(\frac{23}{37}\right)=\left(\frac{37}{23}\right)=\left(\frac{14}{23}\right)=\left(\frac{2}{23}\right)\left(\frac{7}{23}\right)$; since $23 \equiv 7 \pmod 8$, theorem 8.10 gives $\left(\frac{2}{23}\right)=1$, while theorem 8.22 gives $\left(\frac{7}{23}\right)=-\left(\frac{23}{7}\right)=-\left(\frac{2}{7}\right)=-1$, so $\left(\frac{23}{37}\right)=-1$. Finally, $\left(\frac{62}{71}\right)=\left(\frac{2}{71}\right)\left(\frac{31}{71}\right)$; since $71 \equiv 7 \pmod 8$, theorem 8.10 gives $\left(\frac{2}{71}\right)=1$, and theorem 8.22 gives $\left(\frac{31}{71}\right)=-\left(\frac{71}{31}\right)=-\left(\frac{9}{31}\right)=-1$, so $\left(\frac{62}{71}\right)=-1$. $\proofend$

**Problem 3.**
Chapter 8, Exercise 2: Is $41$ a square modulo $1000007$?
**Solution.**
First factor $1000007 = 29 \cdot 34483$. If $41$ were a square modulo $1000007$, then it would be a square modulo $29$. But $41 \equiv 12 \pmod {29}$, so we compute $\left(\frac{12}{29}\right)=\left(\frac{3}{29}\right)\left(\frac{4}{29}\right)=\left(\frac{3}{29}\right)$. By theorem 8.22, Quadratic Reciprocity, $\left(\frac{3}{29}\right)=\left(\frac{29}{3}\right)=\left(\frac{2}{3}\right)=-1$. Therefore $12$ is not a square modulo $29$, so $41$ is not a square modulo $1000007$. $\proofend$

**Problem 4.**
Chapter 8, Exercise 7: Let $p$ be an odd prime. Recall that a primitive root modulo $p$ is an integer $g$ such that $g^{p-1} \equiv 1 \pmod p$, and no smaller positive power of $g$ is congruent to $1 \pmod p$. Some results in this chapter can be proved by using the existence of a primitive root. (a) Use a primitive root $g$ to demonstrate that $-1$ is a square modulo $p$ iff $p \equiv 1 \pmod 4$. (b) Use a primitive root to prove Wilson's Theorem. Hint: show that $(p-1)! \equiv g^{(p-1)(p-2)/2} \pmod p$. (c) Given a primitive root $g$, and an integer $a$ such that $a \not\equiv 0 \pmod p$, prove that $a$ is a square modulo $p$ iff $a \equiv g^n \pmod p$ for an even number $n$. Use this to prove Euler's Criterion: $a$ is a square modulo $p$ iff $a^{(p-1)/2} \equiv 1 \pmod p$.
**Solution.**
For (a), let $g$ be a primitive root modulo $p$. Since $g$ has order $p-1$, we have $g^{p-1} \equiv 1 \pmod p$. Then $g^{(p-1)/2}$ has square $1$, but $g^{(p-1)/2} \not\equiv 1 \pmod p$, since $g$ has no smaller positive exponent giving $1$. Therefore $g^{(p-1)/2} \equiv -1 \pmod p$. Now $-1$ is a square iff $g^{(p-1)/2}$ is an even power of $g$, which is equivalent to the existence of $k$ such that $g^{2k} \equiv g^{(p-1)/2} \pmod p$. Since powers of $g$ are unique modulo $p-1$, this is equivalent to $2k \equiv \frac{p-1}{2} \pmod {p-1}$. This congruence is solvable iff $2$ divides $\frac{p-1}{2}$, so $-1$ is a square modulo $p$ iff $\frac{p-1}{2}$ is even, which is equivalent to $p \equiv 1 \pmod 4$. This agrees with corollary 8.6, the reciprocity law for $-1$. $\proofend$ For (b), since $g$ is primitive modulo $p$, the nonzero classes modulo $p$ are $1,g,g^2,\dots,g^{p-2}$. Therefore $(p-1)! \equiv 1\cdot g\cdot g^2\cdots g^{p-2} \equiv g^{1+2+\cdots+(p-2)} \equiv g^{(p-2)(p-1)/2} \pmod p$. Also, $g^{(p-2)(p-1)/2}=\left(g^{(p-1)/2}\right)^{p-2}$. From part (a), $g^{(p-1)/2} \equiv -1 \pmod p$, and since $p$ is odd, $p-2$ is odd. Hence $(p-1)! \equiv (-1)^{p-2} \equiv -1 \pmod p$. Therefore $(p-1)! \equiv -1 \pmod p$, which proves theorem 8.2, Wilson's Theorem. $\proofend$ For (c), let $a \not\equiv 0 \pmod p$. Since $g$ is primitive, there is some integer $n$ such that $a \equiv g^n \pmod p$. If $a$ is a square modulo $p$, then for some $k$, $a \equiv (g^k)^2 \equiv g^{2k} \pmod p$, so $a$ is an even power of $g$. Conversely, if $a \equiv g^{2k} \pmod p$, then $a \equiv (g^k)^2 \pmod p$, so $a$ is a square. Therefore $a$ is a square modulo $p$ iff $a \equiv g^n \pmod p$ with $n$ even. Now $a^{(p-1)/2} \equiv (g^n)^{(p-1)/2}=\left(g^{(p-1)/2}\right)^n \equiv (-1)^n \pmod p$. Thus $a^{(p-1)/2} \equiv 1 \pmod p$ iff $n$ is even, iff $a$ is a square modulo $p$. This proves theorem 8.5, Euler's Criterion. $\proofend$

**Problem 5.**
Which of the following congruences have solutions? If so, how many? (a) $x^2 \equiv 2 \pmod {61}$, (b) $x^2 \equiv 2 \pmod {59}$, (c) $x^2 \equiv -2 \pmod {61}$, (d) $x^2 \equiv -2 \pmod {59}$, (e) $x^2 \equiv 2 \pmod {122}$, (f) $x^2 \equiv 2 \pmod {118}$, (g) $x^2 \equiv -2 \pmod {122}$, and (h) $x^2 \equiv -2 \pmod {118}$.
**Solution.**
We use theorem 8.10, the reciprocity law for $2$, which says $\left(\frac{2}{p}\right)=1$ iff $p \equiv 1,7 \pmod 8$. Since $61 \equiv 5 \pmod 8$ and $59 \equiv 3 \pmod 8$, we get $\left(\frac{2}{61}\right)=-1$ and $\left(\frac{2}{59}\right)=-1$. By multiplicativity of the Legendre symbol, $\left(\frac{-2}{p}\right)=\left(\frac{-1}{p}\right)\left(\frac{2}{p}\right)$. Since $61 \equiv 1 \pmod 4$, corollary 8.6 gives $\left(\frac{-1}{61}\right)=1$, so $\left(\frac{-2}{61}\right)=1\cdot (-1)=-1$. Since $59 \equiv 3 \pmod 4$, corollary 8.6 gives $\left(\frac{-1}{59}\right)=-1$, so $\left(\frac{-2}{59}\right)=(-1)(-1)=1$. Therefore $x^2 \equiv 2 \pmod {61}$, $x^2 \equiv 2 \pmod {59}$, and $x^2 \equiv -2 \pmod {61}$ have no solutions, while $x^2 \equiv -2 \pmod {59}$ has two solutions. For the composite moduli, $122=2\cdot 61$ and $118=2\cdot 59$. Since $2$ and $-2$ are even, any solution modulo $2q$ must satisfy $x^2 \equiv 0 \pmod 2$, so $x \equiv 0 \pmod 2$. By the Chinese Remainder Theorem, solutions modulo $2q$ correspond to solutions modulo $q$ together with the parity condition $x \equiv 0 \pmod 2$, so the number of solutions modulo $2q$ is the same as the number of solutions modulo $q$. Thus the counts are:
$$
\begin{array}{c|l|c}
\text{Part} & \text{Congruence} & \text{Number of solutions}\\
\hline
(a) & x^2 \equiv 2 \pmod {61} & 0\\
(b) & x^2 \equiv 2 \pmod {59} & 0\\
(c) & x^2 \equiv -2 \pmod {61} & 0\\
(d) & x^2 \equiv -2 \pmod {59} & 2\\
(e) & x^2 \equiv 2 \pmod {122} & 0\\
(f) & x^2 \equiv 2 \pmod {118} & 0\\
(g) & x^2 \equiv -2 \pmod {122} & 0\\
(h) & x^2 \equiv -2 \pmod {118} & 2
\end{array}
$$
For part (h), the two solutions are $x \equiv 36,82 \pmod {118}$. $\proofend$