$$
\require{unicode}
\newcommand{\proofend}{\Large\unicode{x263B}}
$$

**Problem 1:**
Give three sentences in English together with translations into our formal language. The sentences should be chosen so as to have an interesting structure, and the translations should each contain 15 or more symbols.
**Solution:**
a)
If Anthony is fast and not smart, then he is confused and not smart.
$$
((F \land (\neg S)) \implies (C \land (\neg S)))
$$

b)
You are wealthy and not smart iff you have two feet or four feet.
$$
((W \land (\neg S)) \iff (2 \lor 4))
$$

c)
If you read logic and finite model theory, then you can study descriptive complexity or automated reasoning iff you have not graduated.
$$
((L \land F) \implies ((D \lor A) \iff (\neg G)))
$$

$\proofend$

**Problem 2:**
Show that there are no wffs of length 2, 3, or 6, but that any other positive length is possible.
**Solution:**
Let S be the set of all wffs of positive length not equal to $2, 3, 6$. Consider arbitrary nth sentence $A_n$, which is a wff by definition. Its construction is simply $<A_n>$, length 1. It follows that since $A_n$ is a wff of length 1, $A_n \in S$. But $A_n$ was arbitrary and so S contains all sentence symbols. We show that S is closed under all five formula-building operations. Consider $\alpha, \beta \in S$, by definition wffs with positive length not equal to $2, 3, \lor 6$. Denote $L(\alpha)$ to be the length of $\alpha$ and $L(\beta)$ to be the length of $\beta$. We see that $\xi_\neg(\alpha) = (\neg \alpha)$, which has length $3 + L(\alpha)$ and is a wff. Since $L(\alpha) \ge 1$, $3 + L(\alpha) \ge 4$ and so can not be 2 or 3. If $3 + L(\alpha) = 6$, then in particular $L(\alpha) = 3$ contradicting $\alpha \in S$. Therefore, $\xi_\neg(\alpha) \in S$. Let $\blacksquare$ be a binary logical connective. We see that $\xi_\blacksquare(\alpha, \beta) = (\alpha \blacksquare \beta)$ which has length $3 + L(\alpha) + L(\beta)$ and is a wff. Since $L(\alpha), L(\beta) \ge 1$, $3 + L(\alpha) + L(\beta) \ge 5$ and so can not be 2 or 3. If $3 + L(\alpha) + L(\beta) = 6$, then $L(\alpha) + L(\beta) = 3$. By pigeonhole principle, $L(\alpha)$ or $L(\beta)$ must be at least 2. WLOG, suppose $L(\alpha) \ge 2$. It follows that $1 \ge L(\beta) = 3 - L(\alpha)$ and since $L(\beta) \ge 1$, $L(\beta) = 1$ precisely. But then $L(\alpha) = 3 - L(\beta) = 2$ which is a contradiction. Therefore, $3 + L(\alpha) + L(\beta) \ne 6$ and so $\xi_\blacksquare(\alpha, \beta) \in S$.  We have shown that S is a set of wffs containing all the sentence symbols and closed under all five formula-building operations. Thus, by the induction principle, S is a set of all wffs and so no wff is of length 2, 3, or 6.

Clearly, every sentence symbol is a wff of length 1, and so wffs of length 1 exist. Let $A_n$ be a sentence symbol. Notice $\xi_\neg(A_n) = (\neg A_n)$, and so length 4 wffs exist. We also see that $\xi_\land(A_n) = (A_n \land A_n)$ and so wffs of length 5 are possible. We now induct to show lengths $\ge 7$ are possible. First we construct $7, 8, 9$. Let $A_n$ be a sentence symbol. Then $\xi_\neg^2(A_n) = (\neg(\neg A_n))$ which has length 7. Also, $\xi_\neg(\xi_\land(A_n, A_n)) = (\neg(A_n \land A_n))$ which has length 8. Finally, $\xi_\land(A_n, \xi_\land(A_n, A_n)) = (A_n \land (A_n \land A_n))$ which has length 9. Now let $n \ge 9$ be arbitrary and suppose there exists wffs of length k for all integers $7 \le k \le n$. Define $\alpha_{n-2}$ to be a wff of length $n-2$, which exists since $n - 2 \ge 7$. Notice $\xi_\neg(\alpha_{n-2}) = (\neg \alpha_{n-2})$ which is of length $3 + (n-2) = n + 1$. Therefore, a wff of length $n + 1$ exists. By strong induction then, for every integer $n \ge 7$ there exists a wff of length n. Thus, wffs of positive length other than $2,3,6$ are possible.
$\proofend$

**Problem 3:**
Let $\alpha$ be a wff; let c be the number of places at which binary connective symbols occur in $\alpha$; let s be the number of places at which sentence symbols occur in $\alpha$. Show by using the induction principle that $s = c + 1$.
**Solution:**
Let the set S be the collection of all wffs holding the property that $s = c + 1$. Consider sentence symbol $A_n$, which has values $s = 1$ and $c = 0$. Clearly, it holds that $s = c + 1$ and so $A_n \in S$. It follows that S contains all sentence symbols. Consider $\alpha, \beta \in S$. Let $s(x)$ denote the number of places at which sentence symbols occur in x and let $c(x)$ denote the number of places at which binary connective symbols occur in x. We see that $\xi_\neg(\alpha) = (\neg \alpha)$ has $s((\neg \alpha)) = 1 + s(\alpha)$ and $c((\neg \alpha)) = c(\alpha)$. By assumption, $s(\alpha) = c(\alpha) + 1$ and so 
