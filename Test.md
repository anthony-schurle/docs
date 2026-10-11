# Ch 2.

Problem 15:
For each of the following pairs of numbers 𝑎 and 𝑏, calculate gcd⁡(𝑎,𝑏) and find integers 𝑟 and 𝑠 such that gcd⁡(𝑎,𝑏) =𝑟⁢𝑎 +𝑠⁢𝑏.

1. 14 and 39
    
2. 234 and 165
    
3. 1739 and 9923
    
4. 471 and 562
    
5. 23771 and 19945
    
6. −4357 and 3754
Solution:
1)
39 = 2(14) + 11
14 = 1(11) + 3
11 = 3(3) + 2
3 = 1(2) + 1
2 = 2(1)
hence gcd = 1.
Now 1 = 3 - 2, 1 = 3 - (11 - 3(3)) = 4(3) - 11, 1 = 4(14 - 11) - 11 = 4(14) - 5(11), 1 = 4(14) - 5(39 - 2(14)) = 14(14) - 5(39).
The rest follow a similar process.

Problem 16:
Let 𝑎 and 𝑏 be nonzero integers. If there exist integers 𝑟 and 𝑠 such that 𝑎⁢𝑟 +𝑏⁢𝑠 =1, show that 𝑎 and 𝑏 are relatively prime.
Solution:
gcd(a, b) = min{|ar + bs| : |ar + bs| > 0}. But no smaller integer than 1 exists thats positive, so gcd(a, b) = ar + bs = 1.

Problem 27:
Let 𝑎,𝑏,𝑐 ∈ℤ. Prove that if gcd⁡(𝑎,𝑏) =1 and 𝑎 ∣𝑏⁢𝑐, then 𝑎 ∣𝑐.
Solution:
Since gcd(a, b) = 1, we have 1 = na + mb for integers n and m. Hence c = cna + cmb. But a | cna and a | cmb (since a | bc) and so a |c.

# Ch 3.

Problem 7:
Let 𝑆 =ℝ ∖{−1} and define a binary operation on 𝑆 by 𝑎 ∗𝑏 =𝑎 +𝑏 +𝑎⁢𝑏. Prove that (𝑆, ∗) is an abelian group.
Solution:
Let e = 0 and a^{-1} = \frac{a}{1+a}. Clearly we satisfy the group axioms (only thing not trivial is closure but notice we require b = -1 which is not possible). Abelian follows trivially also by commutivity of addition.







Define a context-free grammar by $G = (\{S, P, C, A, N, ', \neg, \land, \lor, \implies, \iff, (, )\}, \{S, P, C, A, N, ', \neg, \land, \lor, \implies, \iff, (, )\}, R, S)$ where,
$$
\begin{aligned}
R = &\{(S, P), (S, C), \\
&(P, (AN)), (N, 'N), (N, ') \\
&(C, (\neg P)), (C, (P \land P)), (C, (P \lor P)), \\ 
&(C, (P \implies P)), (C, (P \iff P))\}
\end{aligned}
$$

 We claim that this defines the language of wffs in propositional logic (Denote $L_G$). First, we show that $L_G \subseteq L(G)$ by induction on string length. Take $w \in L_G$ with $|w| = 1$. This is only possible 
 Let $w \in L_G$ with $|w| = 7$. 

