## 1.1

**Problem 1**
Give three sentences in English together with translations into our formal language. The sentences should be chosen so as to have an interesting structure, and the translations should each contain 15 or more symbols.
**Solution**
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

**Problem 2**
Show that there are no wffs of length 2, 3, or 6, but that any other positive length is possible.
**Solution**
Let S be the set of all wffs of positive length not equal to $2, 3, 6$. Consider arbitrary nth sentence $A_n$, which is a wff by definition. Its construction is simply $<A_n>$, length 1. It follows that since $A_n$ is a wff of length 1, $A_n \in S$. But $A_n$ was arbitrary and so S contains all sentence symbols. We show that S is closed under all five formula-building operations. Consider $\alpha, \beta \in S$, by definition wffs with positive length not equal to $2, 3, \lor 6$. Denote $L(\alpha)$ to be the length of $\alpha$ and $L(\beta)$ to be the length of $\beta$. We see that $\xi_\neg(\alpha) = (\neg \alpha)$, which has length $3 + L(\alpha)$ and is a wff. Since $L(\alpha) \ge 1$, $3 + L(\alpha) \ge 4$ and so can not be 2 or 3. If $3 + L(\alpha) = 6$, then in particular $L(\alpha) = 3$ contradicting $\alpha \in S$. Therefore, $\xi_\neg(\alpha) \in S$. Let $\blacksquare$ be a binary logical connective. We see that $\xi_\blacksquare(\alpha, \beta) = (\alpha \blacksquare \beta)$ which has length $3 + L(\alpha) + L(\beta)$ and is a wff. Since $L(\alpha), L(\beta) \ge 1$, $3 + L(\alpha) + L(\beta) \ge 5$ and so can not be 2 or 3. If $3 + L(\alpha) + L(\beta) = 6$, then $L(\alpha) + L(\beta) = 3$. By pigeonhole principle, $L(\alpha)$ or $L(\beta)$ must be at least 2. WLOG, suppose $L(\alpha) \ge 2$. It follows that $1 \ge L(\beta) = 3 - L(\alpha)$ and since $L(\beta) \ge 1$, $L(\beta) = 1$ precisely. But then $L(\alpha) = 3 - L(\beta) = 2$ which is a contradiction. Therefore, $3 + L(\alpha) + L(\beta) \ne 6$ and so $\xi_\blacksquare(\alpha, \beta) \in S$.  We have shown that S is a set of wffs containing all the sentence symbols and closed under all five formula-building operations. Thus, by the induction principle, S is a set of all wffs and so no wff is of length 2, 3, or 6.

Clearly, every sentence symbol is a wff of length 1, and so wffs of length 1 exist. Let $A_n$ be a sentence symbol. Notice $\xi_\neg(A_n) = (\neg A_n)$, and so length 4 wffs exist. We also see that $\xi_\land(A_n) = (A_n \land A_n)$ and so wffs of length 5 are possible. We now induct to show lengths $\ge 7$ are possible. First we construct $7, 8, 9$. Let $A_n$ be a sentence symbol. Then $\xi_\neg^2(A_n) = (\neg(\neg A_n))$ which has length 7. Also, $\xi_\neg(\xi_\land(A_n, A_n)) = (\neg(A_n \land A_n))$ which has length 8. Finally, $\xi_\land(A_n, \xi_\land(A_n, A_n)) = (A_n \land (A_n \land A_n))$ which has length 9. Now let $n \ge 9$ be arbitrary and suppose there exists wffs of length k for all integers $7 \le k \le n$. Define $\alpha_{n-2}$ to be a wff of length $n-2$, which exists since $n - 2 \ge 7$. Notice $\xi_\neg(\alpha_{n-2}) = (\neg \alpha_{n-2})$ which is of length $3 + (n-2) = n + 1$. Therefore, a wff of length $n + 1$ exists. By strong induction then, for every integer $n \ge 7$ there exists a wff of length n. Thus, wffs of positive length other than $2,3,6$ are possible.
$\proofend$

**Problem 3:**
Let $\alpha$ be a wff; let c be the number of places at which binary connective symbols occur in $\alpha$; let s be the number of places at which sentence symbols occur in $\alpha$. Show by using the induction principle that $s = c + 1$.
**Solution:**
Let the set S be the collection of all wffs holding the property that $s = c + 1$. Consider sentence symbol $A_n$, which has values $s = 1$ and $c = 0$. Clearly, it holds that $s = c + 1$ and so $A_n \in S$. It follows that S contains all sentence symbols. Consider $\alpha, \beta \in S$. Let $s(x)$ denote the number of places at which sentence symbols occur in x and let $c(x)$ denote the number of places at which binary connective symbols occur in x. We see that $\xi_\neg(\alpha) = (\neg \alpha)$ has $s((\neg \alpha)) = s(\alpha)$ and $c((\neg \alpha)) = c(\alpha)$. By assumption, $s(\alpha) = c(\alpha) + 1$ and so $s((\neg \alpha)) = c((\neg \alpha)) + 1$. Hence $\xi_\neg$ is closed under S. It also follows that $\xi_\blacksquare (\alpha, \beta) = (\alpha \blacksquare \beta)$, for binary connective symbol $\blacksquare$, where $s(\alpha \blacksquare \beta) = s(\alpha) + s(\beta)$ and $c(\alpha \blacksquare \beta) = c(\alpha) + c(\beta) + 1$. By assumption, $s(\alpha) = c(\alpha) + 1$ and $s(\beta) = c(\beta) + 1$ so that $s(\alpha \blacksquare \beta) = c(\alpha) + c(\beta) + 2$. But  $s(\alpha \blacksquare \beta) = c(\alpha) + c(\beta) + 2$ and $c(\alpha \blacksquare \beta) = c(\alpha) + c(\beta) + 1$ so that $s(\alpha \blacksquare \beta) = c(\alpha \blacksquare \beta) + 1$. Therefore, the four binary formula-building operations are closed under S. Thus, because S contains all the sentence symbols and is closed under all five formula-building operations, every wff must hold the property that $s = c + 1$. $\proofend$

**Problem 4**
Assume that we have a construction sequence ending in $\phi$, where $\phi$ does not contain the symbol $A_4$. Suppose we delete all the expressions in the construction sequence that contain $A_4$. Show that the result is still a legal construction sequence.
**Solution**
Let $s := <s_0, s_1, ..., s_m>$ be the original construction sequence and $p := <p_0, p_1, ..., p_n>$ the modified sequence where $s_m = p_n = \phi$. Suppose, for contradiction, $p$ is not a valid construction sequence so that for some $0 \le i \le n$ - $p_i$ is not a sentence symbol, $p_i \ne \xi_\neg (p_j)$ for some $j < i$, and $p_i = \xi_{\blacksquare}(p_j, p_k)$ for some $j, k < i$ and $\blacksquare = \land, \lor, \implies, \iff$. We induct 

**Problem 5**
Suppose that $\alpha$ is a wff not containing the negation symbol $\neg$.
a) Show that the length of $\alpha$ is odd.
b) Show that more than a quarter of the symbols are sentence symbols.
**Solution**
a)
Denote $p$ as the number of $($ and $)$, $s$ as the number of sentence symbols, and c as the number of binary connective symbols in $\alpha$. We know $p$ must be even since a wff can not contain more left parentheses than right parenthesis or left parentheses than right parentheses. By problem 3, $s = c + 1$. Since $\alpha$ only does not contain $\neg$, it must be that $p$, $s$, and $c$ compose the entire string of $\alpha$. Now $s$ must either be even or odd. Case 1: $s$ is even. Because s is even and $s - c = 1$, c must be odd. But then $\alpha$ is odd length since $s + p$ is even making $(s+p) + c$ odd. Case 2: $s$ is odd. Then since $s - c = 1$ and s is odd, $c$ must be even. Hence $c + p$ is even making $(c + p) + s$ odd. Therefore, $\alpha$ has odd length. $\proofend$

b)

## 1.2

**Problem 1**
Show that neither of the following two formulas tautologically implies the other.
$$
\begin{aligned} & \text{a) }(A \iff (B \iff C)) \\
& \text{b) }((A \land (B \land C)) \lor ((\neg A) \land ((\neg B) \land (\neg C)))) \end{aligned}
$$
**Solution**

| A   | B   | C   | $(A \iff (B \iff C))$ | $((A \land (B \land C)) \lor ((\neg A) \land ((\neg B) \land (\neg C))))$ |
| --- | --- | --- | --------------------- | ------------------------------------------------------------------------- |
| T   | F   | F   | T                     | F                                                                         |
| F   | F   | F   | F                     | T                                                                         |

Clearly, neither of the two formulas tautologically implies the other. $\proofend$

**Problem 2**
a) Is $(((P \implies Q) \implies P) \implies P)$ a tautology?
b) Define $\sigma_k$ recursively as follows: $\sigma_0 = (P \implies Q)$ and $\sigma_{k+1} = (\sigma_k \implies P)$. For which values of k is $\sigma_k$ a tautology?
**Solution**
a)

| P   | Q   | $(((P \implies Q) \implies P) \implies P)$ |
| --- | --- | ------------------------------------------ |
| F   | F   | T, F, T                                    |
| F   | T   | T, F, T                                    |
| T   | F   | F, T, T                                    |
| T   | T   | T, T, T                                    |

Yes. $\proofend$

b)
$\sigma_k$ is a tautology when $k = 2n$ for $n \in \mathbb{N} \backslash \{0\}$. As shown, $\sigma_k$ is a tautology when $n = 1$. Suppose $\sigma_k$ is a tautology where $k = 2m$ for some $m \in \mathbb{N} \backslash \{0\}$. Consider $\sigma_{k+1} = (\sigma_k \implies P) \implies P$. We know $v(\sigma_k) = T$ and clearly $v(\sigma_{k+1})$ does not depend on $v(Q)$, so we only consider $v(P)$. If $v(P) = T$, then $v(\sigma_k \implies P) = T$ so that $v(\sigma_{k+1}) = T$. If $v(P) = F$, then $v(\sigma_k \implies P) = F$ so that $v(\sigma_{k+1}) = T$. In either case, $v(\sigma_{k+1}) = T$. Hence we have shown that $\sigma_k$ is a tautology precisely when $k = 2n$ for $n \in \mathbb{N} \backslash \{0\}$. For contradiction, suppose $k \ne 2n$ for $n \in \mathbb{N} \backslash \{0\}$, but $\sigma_k$ is a tautology, This is only possible when $k = 2n + 1$ for some $n \in \mathbb{N} \backslash \{0\}$. We have shown already that $\sigma_{2n}$ is a tautology. But $\sigma_k = (\sigma_{2n} \implies P)$, and when $v(P) = F$ we see that $v(\sigma_k) = F$. A contradiction. Therefore, $\sigma_k$ is a tautology only when $k = 2n$ for $n \in \mathbb{N} \backslash \{0\}$. $\proofend$

**Problem 3**
(a) Determine whether or not $((P \implies Q) \lor (Q \implies P))$ is a tautology.
(b) Determine whether or not $((P \land Q) \implies R)$ tautologically implies $((P \implies R) \lor (Q \implies R))$.
**Solution**
a)

| P   | Q   | $((P \implies Q) \lor (Q \implies P))$ |
| --- | --- | -------------------------------------- |
| F   | F   | T                                      |
| F   | T   | T                                      |
| T   | F   | T                                      |
| T   | T   | T                                      |

Yes. $\proofend$

b)

| P   | Q   | R   | $((P \land Q) \implies R)$ | $((P \implies R) \lor (Q \implies R))$ |
| --- | --- | --- | -------------------------- | -------------------------------------- |
| F   | F   | F   | T                          | T                                      |
| F   | F   | T   | T                          | T                                      |
| F   | T   | F   | T                          | T                                      |
| F   | T   | T   | T                          | T                                      |
| T   | F   | F   | T                          | T                                      |
| T   | F   | T   | T                          | T                                      |
| T   | T   | F   | F                          |                                        |
| T   | T   | T   | T                          | T                                      |

Yes. $\proofend$

**Problem 4**
Show that the following hold:
(a) $\sum \cup \alpha \vDash \beta$ iff $\sum \vDash (\alpha \implies \beta)$.
(b) $\alpha \tauteq \beta$ iff $\vDash (\alpha \iff \beta)$.
**Solution**
a)
Suppose $\sum \cup \alpha \vDash \beta$. Give an arbitrary truth assignment $v$ with $\overline{v}$ being its extension and suppose $v$ satisfies every member of $\sum$. We show that $v$ then must satisfy $\alpha \implies \beta$. Either $v(\alpha) = T$ or $v(\alpha) = F$. Case 1: $v(\alpha) = T$. Since $\sum \cup \alpha \vDash \beta$, we must also have $v(\beta) = T$. Hence $\overline{v}(\alpha \implies \beta) = T$. Case 2: $v(\alpha) = F$. It is immediate that $\overline{v}(\alpha \implies \beta) = T$. Therefore, in either case, $\alpha \implies \beta$ is satisfied by $v$. We conclude that $\sum \cup \alpha \vDash \beta \implies \sum \vDash (\alpha \implies \beta)$. Now suppose that $\sum \vDash (\alpha \implies \beta)$. Give truth assignment $v$ with extension $\overline{v}$ such that $v$ satisfies every member of $\sum \cup \alpha$. We show that $v$ must also satisfy $\beta$, and thus conclude that $\sum \vDash (\alpha \implies \beta) \implies \sum \cup \alpha \vDash \beta$. Since $v$ satisfies every member of $\sum \cup \alpha$, in particular it must satisfy every member of $\sum$. And from $\sum \vDash (\alpha \implies \beta)$, it must be that $\overline{v}(\alpha \implies \beta) = T$. Again, since $v$ satisfies every member of $\sum \cup \alpha$, in particular it must satisfy  $\alpha$. Hence $\overline{v}(\alpha) = T$ and $\overline{v}(\alpha \implies \beta) = T$, which is only possible when $v$ satisfies $\beta$ as desired. $\proofend$

b)
Suppose $\alpha \tauteq \beta$ and let $v$ be a truth assignment with extension $\overline{v}$. We show that $v$ must satisfy $\alpha \iff \beta$ to conclude that $\alpha \tauteq \beta \implies \vDash (\alpha \iff \beta)$. Either $v(\alpha) = T$ or $v(\alpha) = F$. Case 1: $v(\alpha) = T$. Then, because $\alpha \tauteq \beta$, $v(\beta) = T$. Hence $\overline{v}(\alpha \iff \beta) = T$. Case 2: $v(\alpha) = F$. If $v(\beta) = T$, we contradict $\alpha \tauteq \beta$. So it must be that $v(\beta) = F$. It follows that $\overline{v}(\alpha \iff \beta) = T$. Therefore, in either case, $v$ satisfies $\alpha \iff \beta$. Now suppose that $\alpha \iff \beta$ is a tautology. We show first that $\alpha \vDash \beta$. Let $v$ be a truth assignment with extension $\overline{v}$ and suppose it satisfies $\alpha$. Since $\alpha \iff \beta$ is a tautology and $v(\alpha) = T$, we have $v(\beta) = T$. Hence $\alpha \vDash \beta$. Now we show that $\beta \vDash \alpha$. Let $v$ be a truth assignment with extension $\overline{v}$ and suppose it satisfies $\beta$. Since $\alpha \iff \beta$ is a tautology and $v(\beta) = T$, we have $v(\alpha) = T$. Hence $\beta \vDash \alpha$. Thus, $\alpha \tauteq \beta$. $\proofend$

**Problem 5**
Prove or refute each of the following assertions:
(a) If either $\sum \vDash \alpha$ or $\sum \vDash \beta$, then $\sum \vDash (\alpha \lor \beta)$.
(b) If $\sum \vDash (\alpha \lor \beta)$, then either $\sum \vDash \alpha$ or $\sum \vDash \beta$.
**Solution**
a)
Case 1: $\sum \vDash \alpha$. Let $v$ be a truth assignment with extension $\overline{v}$ that satisfies every member of $\sum$. Then $v$ must satisfy $\alpha$. Hence $\overline{v}(\alpha \lor \beta) = T$. Case 2 with $\sum \vDash \beta$ follows similarly. $\proofend$

b)
This statement is false. Consider $\sum = \{\alpha \lor \beta\}$. Clearly, $\sum \vDash (\alpha \lor \beta)$. We first show that $\sum \not \vDash \alpha$. Let $v$ be the truth assignment with $v(\alpha) = F$ and $v(\beta) = T$ and $\overline{v}$ its extension. Then $v$ satisfies every member of $\sum$, but $\overline{v}(\alpha) = F$. Hence $\sum \not \vDash \alpha$. $\sum \not \vDash \beta$ follows similarly by assigning $v(\alpha) = T$ and $v(\beta) = F$. $\proofend$

**Problem 6**
(a) Show that if $v_1$ and $v_2$ are truth assignments which agree on all the sentence symbols in the wff $\alpha$, then $\overline{v_1}(\alpha) = \overline{v_2}(\alpha)$. Use the induction principle.
(b) Let $S$ be the set of sentence symbols that include those in $\sum$ and $\tau$ (possibly more). Show that $\sum \vDash \tau$ iff every truth assignment for $S$ which satisfies every member of $\sum$ also satisfies $\tau$.
**Solution**
a)
Define the set $S := \{\alpha \in \text{wff } | v_1 \text{ and } v_2 \text{ agree on all sentence symbols in } \alpha \implies \overline{v_1}(\alpha) = \overline{v_2}(\alpha)\}$. Clearly, all sentence symbols belong to $S$. Let $\beta \in S$. Consider $\xi_\neg(\beta) = (\neg \beta) =: \zeta$. Clearly, $\zeta$ has the same sentence symbols $A_1, A_2, ..., A_n$. Let $v_1$ and $v_2$ be two truth assignments that agree on these sentence symbols. Since $\beta \in S$, we know that $\overline{v_1}(\beta) = \overline{v_2}(\beta)$. By definition of $\overline{v_1}$ and $\overline{v_2}$ then, it must be that $\overline{v_1}(\zeta) = \overline{v_2}(\zeta)$. Hence $\zeta \in S$ and so $S$ is closed under $\xi_\neg$. Now consider $\sigma := \xi_\blacksquare(\lambda_1, \lambda_2) = (\lambda_1 \blacksquare \lambda_2)$ for $\lambda_1, \lambda_2 \in S$ and $\blacksquare$ being one of $\land, \lor, \implies, \iff$. If $\lambda_1$ contains sentence symbols $X_1, X_2, ..., X_x$ and $\lambda_2$ contains sentence symbols $Y_1, Y_2, ..., Y_y$, then $\sigma$ contains precisely the sentence symbols $X_1, X_2, ..., X_x, Y_1, Y_2, ..., Y_y$. Let $v_1$ and $v_2$ be and two truth assignments that agree on the sentence symbols of $\sigma$. Since $\lambda_1, \lambda_2 \in S$, we have $\overline{v_1}(\lambda_1) = \overline{v_2}(\lambda_1)$ and $\overline{v_1}(\lambda_2) = \overline{v_2}(\lambda_2)$. But then by definition of $\overline{v_1}$ and $\overline{v_2}$, $\overline{v_1}(\sigma) = \overline{v_2}(\sigma)$. Thus, $\sigma \in S$ meaning that S is closed under these four formula building operations as well. We get the desired statement by the induction principle. $\proofend$

b)
Suppose $\sum \vDash \tau$ and let $v_1$ be a truth assignment for S which satisfies every member of $\sum$. Let $v_2$ be a truth assignment that satisfies every member of $\sum$ with sentence symbols of $\sum$ and $\tau$ being $B_1, B_2, ..., B_m$ so that $v_2$ agrees with $v_1$ on these sentence symbols (this exists as $v_1$ is one such instance). By part a, $\overline{v_1}(\tau) = \overline{v_2}(\tau)$. But $\sum \vDash \tau$, and so $v_2$ must satisfy $\tau$. Hence, $v_1$ must satisfy $\tau$. Now suppose every truth assignment for $S$ which satisfies every member of $\sum$ also satisfies $\tau$. Let $y_2$ be a truth assignment satisfying every member of $\sum$, with the extension $\overline{v}$. Let $y_1$ be the domain expanded truth assignment for $y_2$, with any sentence symbols in S but not the domain of $y_2$ being satisfied. Since $y_1$ and $y_2$ agree on the sentence symbols for any member of $\sum$, $y_1$ must also satisfy every member of $\sum$ by part a. Hence $y_1$ must satisfy $\tau$. Again, since $y_1$ and $y_2$ agree on the sentence symbols of $\tau$, $y_2$ must also satisfy $\tau$. $\proofend$

**Problem 7**
You are inhabited in a land by people who either always tell the truth or always tell falsehoods. You come to a fork in the road and you need to know which fork leads to the capital. There is a local resident there, but he has time only to reply to one yes-or-no question. What one question should you ask so as to learn which fork to take?
**Solution**


**Problem 8**
Consider a sequence $\alpha_1, \alpha_2, ...,$ of wffs. For each wff $\phi$, let $\phi^*$ be the result of replacing the sentence symbol $A_n$ by $\alpha_n$, for each n.
(a) Let $v$ be a truth assignment for the set of all sentence symbols; define $u$ to be the truth assignment for which $u(A_n) = \overline{v}(\alpha_n)$. Show that $\overline{u}(\phi) = \overline{v}(\phi^*)$. Use the induction principle.
(b) Show that if $\phi$ is a tautology, then so is $\phi^*$,
**Solution**
a)
Define the set $S := \{\beta \in \text{wff } | \overline{u}(\beta) = \overline{v}(\beta^*)\}$. Consider arbitrary sentence symbol $A$. By definition, $u(A) = \overline{v}(\alpha_1)$. Hence $\overline{u}(A) = \overline{v}(A^*)$. Therefore, $S$ contains every sentence symbol. Let $\lambda_1 \in S$, and so $\overline{u}(\lambda_1) = \overline{v}(\lambda_1^*)$.  By definition of $\overline{u}$ and $\overline{v}$, $\overline{u}((\neg \lambda_1)) = \overline{v}((\neg \lambda_1^*))$.  Therefore, $S$ is closed under $\xi_\neg$. Finally, let $\lambda_2, \lambda_3 \in S$, so that $\overline{u}(\lambda_2) = \overline{v}(\lambda_2^*)$ and $\overline{u}(\lambda_3) = \overline{v}(\lambda_3^*)$. By construction of $\overline{u}$ and $\overline{v}$, we see that $\overline{u}(\lambda_2 \blacksquare \lambda_3) = \overline{v}(\lambda_2^* \blacksquare \lambda_3^*)$ where $\blacksquare$ is one of $\land, \lor, \implies, \iff$. It follows that $S$ is closed under all five formula building operations. Thus, by the induction principle, $\overline{u}(\phi) = \overline{v}(\phi^*)$ as desired. $\proofend$

b)
Suppose $\phi$ is a tautology. By problem 6, it suffices to consider arbitrary truth assignment $v$ with extension $\overline{v}$ over all sentence symbols. We are given that $u$ must satisfy $\phi$. By part a then, $v$ must satisfy $\phi^*$. But $v$ was arbitrary, so $\phi^*$ is a tautology. $\proofend$

**Problem 9**
Let $\alpha$ be a wff whose only connective symbols are $\land$, $\lor$, and $\neg$. Let $\alpha^*$ be the result of interchanging $\land$ and $\lor$ and replacing each sentence symbol by its negation. Show that $\alpha^*$ is a tautologically equivalent to $(\neg \alpha)$. Use the induction principle.
**Solution**
Temporarily call $\alpha$ special. Define $S := \{\alpha \in \text{wff } | \alpha \text{ is special } \implies \alpha^* \tauteq (\neg \alpha)\}$. Let $A$ be a sentence symbol. We see that $A* = (\neg A)$ and that $A$ is classified as special. Notice $A* = (\neg A) \tauteq (\neg A)$ clearly. Hence $S$ contains all the sentence symbols. Consider $\lambda_1 \in S$. If $\lambda_1$ is not special, then $\xi_\neg(\lambda_1) \in S$ by definition. If $\lambda_1$ is special, then we are given that $(\neg \lambda_1) \tauteq \lambda_1^*$. 

**Problem 10**
Say that a set $\sum_1$ of wffs is equivalent to a set $\sum_2$ of wffs iff for any wff $\alpha$, we have $\sum_1 \vDash \alpha$ iff $\sum_2 \vDash \alpha$. A set $\sum$ is independent iff no member of $\sum$ is tautologically implied by the remaining members in $\sum$. Show that the following hold.
(a) A finite set of wffs has an independent equivalent subset.
(b) An infinite set need not have an independent equivalent subset.
(c) Let $\sum = \{\sigma_0, \sigma_1, ...\}$; show that there is an independent equivalent set $\sum'$.
**Solution**
a)
Let $\sum$ be a finite set of wffs. If $\sum$ is independent, we are done. So suppose not, meaning there is a $\sigma \in \sum$ tautologically implied by the remaining members in $\sum$. Denote $\sum '$ to be the removal of all such members from $\sum$, which is possible since $\sum$ is finite. Then $\sum '$ must be independent. Let $\alpha$ be some wff. Suppose $\sum ' \vDash \alpha$. Then let $v_1$ be a truth assignment satisfying every member of $\sum$. Since $\sum ' \subseteq \sum$, $v_1$ must also satisfy every member of $\sum '$. Hence $v_1$ satisfies $\alpha$, meaning that $\sum \vDash \alpha$ if $\sum ' \vDash \alpha$. Now suppose that $\sum \vDash \alpha$. Let $v_2$ be a truth assignment satisfying every member of $\sum '$. For the sake of contradiction, suppose some member $\sigma \in \sum$ is not satisfied by $v_2$. Since $\sum '$ is satisfied, $\sigma \not \in \sum '$. By construction, $\sigma$ must have been tautologically implied by the members in $\sum '$. But all members of $\sum '$ are satisfied by $v_2$, so $\sigma$ must be satisfied by $v_2$. Our contradiction is reached. Therefore, every member of $\sum$ is satisfied by $v_2$. It follows that $\alpha$ is satisfied by $v_2$. Thus, $\sum '$ is equivalent to $\sum$. $\proofend$

b)


