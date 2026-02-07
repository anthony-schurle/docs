1)
Computer Science $\land$ Math

2)
I hope to utilize number theory in other mathematical domains and strengthen my mathematical maturity overall.

3)
The Twin Prime Conjecture was a particularly interesting concept discussed during week 1. The conjecture was very straightforward, yet is still open. In addition, it shows how accessible the frontier of modern mathematics is, at least in terms of conceptual understanding of the problem.

4)
Let $n = 2$. Notice, $n \in \mathbb{N}$ and $n^5 - 1 = 31$. But 31 is a prime number. Therefore, there is a natural number n such that $n^5 - 1$ is a prime number.

5)
Define arbitrary $m, n \in \mathbb{N}$. Notice,
$$
m^4 + 4n^4 = (m^2 - 2mn + 2n^2)(m^2 + 2mn + 2n^2)
$$
Therefore, the result is a factorization of two numbers. But then for the result to be prime, one factor must be 1 and the other the prime number itself by definition. Then there are two cases. Case 1: $(m^2 + 2mn + 2n^2) = 1$. It follows that, $m^2 \ge 1, 2mn \ge 2, 2n^2 \ge 2$ since $m, n \in \mathbb{N}$.  Then $m^2 + 2mn + 2n^2 \ge 5$ which contradicts our assumption and so this case is not possible. Case 2: $(m^2 - 2mn + 2n^2) = 1$. Then we have,
$$
(m^2 - 2mn + 2n^2) = (m - n)^2 + n^2 = 1
$$
where $n^2 \ge 1$ and $(m - n)^2 \ge 0$ because $m, n \in \mathbb{N}$. Since $(m - n)^2 + n^2 = 1$, $(m - n)^2 = 0$ and $n^2 = 1$ is the only possibility. It follows that $n = 1$ and therefore, $m = 1$ because $m \in \mathbb{N}$. Thus, from both cases, we see the only possible solution is $m = n = 1$ such that for natural numbers m and n, the result of $m^4 + 4n^2$ is prime.
