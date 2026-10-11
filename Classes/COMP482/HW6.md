# Ch 13 (13.9)

**Problem 1(a, d, k, n, u)**
For each of the following languages $L$, state whether $L$ is regular, context-free but not regular, or not context-free and prove your answer.
a) $\{xy : x, y \in \{a, b\}^* \text{ and } |x| = |y|\}$.
d) $\{a^ib^n : i, n > 0 \text{ and } (i = n \text{ or } i = 2n)\}$.
k) $\{a^i : i \ge 0\}\{b^i : i \ge 0\}\{a^i : i \ge 0\}$.
n) $\{a^nb^{2n}c^m\} \cap \{a^nb^mc^{2m}\}$.
u) $\neg A^nB^n$.
**Solution**
a)
$L$ is regular. If $w = xy$ with $|x| = |y|$, then $|w| = 2|x|$, so $w$ has even length. Conversely, every even-length string over $\{a, b\}$ can be split into two equal-length halves. Thus, $L$ is exactly the language described by the regular expression $((a \cup b)(a \cup b))^*$. $\proofend$

d)
$L$ is context free but not regular. Define $L_1 = \{a^nb^n : n > 0\}$ and $L_2 = \{a^{2n}b^n : n > 0\}$. The grammars $S_1 \to aS_1b \mid ab$ and $S_2 \to aaS_2b \mid aab$ generate $L_1$ and $L_2$, respectively. Since context-free languages are closed under union, $L = L_1 \cup L_2$ is context-free. Suppose $L$ were regular, and let $k$ be its pumping length. Choose $w = a^kb^k \in L$ which has length greater than $k$. For any decomposition $w = xyz$ with $|xy| \le k$ and $y \ne \epsilon$, we have $y = a^t$ for some $1 \le t \le k$. Pumping down gives $xz = a^{k-t}b^k$. Since $k-t$ is neither $k$ nor $2k$, this string is not in $L$, contradicting the Pumping Theorem. Hence, $L$ is not regular. $\proofend$

k)
$L$ is regular. Define $L_A = \{a^i \mid i \ge 0\}$ and $L_B = \{b^i \mid i \ge 0\}$. Since regular languages are closed under concatenation, it suffices to show that $L_A, L_B$ are regular so that $L = L_AL_BL_A$. But $L_A = a^*$ and $L_B = b^*$ ($p^* = \{p\}^* = L_p$), so they are regular. $\proofend$

n)
$L$ is not context-free. Membership in the first language requires twice as many $b$’s as $a$’s, and membership in the second requires twice as many $c$’s as $b$’s. Thus, $L = \{a^nb^{2n}c^{4n} : n \ge 0\}$. Suppose $L$ were context-free, and let $k$ be its pumping length. Choose $w = a^kb^{2k}c^{4k}$. For any decomposition $w = uvxyz$ satisfying $|vxy| \le k$ and $vy \ne \epsilon$, the substring $vxy$ cannot contain both an $a$ and a $c$, because the intervening $b$-block has length $2k$. Consequently, pumping down to $uxz$ leaves at least one of the three symbol counts unchanged and decreases at least one other count. The unchanged count forces the parameter $n$ to remain $k$, but the decreased count then contradicts the required ratio $1:2:4$. Hence, $uxz \notin L$, contradicting the Pumping Theorem. Therefore, $L$ is not context-free. $\proofend$

u)
$L$ is context-free but not regular. Since $A^nB^n = \{a^nb^n : n \ge 0\}$ is deterministic context-free (by the book) and deterministic context-free languages are closed under complement, $L = \neg A^nB^n$ is context-free. If $L$ were regular, then its complement $A^nB^n$ would also be regular, since regular languages are closed under complement. But $A^nB^n$ is not regular (by the book). Therefore, $L$ is not regular. $\proofend$

<div class="page-break"></div>

**Problem 17**
Show that the following languages are deterministic context-free:
a) $\{w : w \in \{a, b\}^* \text{ and each prefix of } w \text{ has at least as many } a\text{’s as } b\text{’s}\}$.
b) $\{a^nb^n : n \ge 0\} \cup \{a^nc^n : n \ge 0\}$.
**Solution**
a)
Let $\$$ be an end-of-string marker. Define $M = (\{s, f\}, \{a, b, \$\}, \{a\}, \Delta, s, \{f\})$, where $\Delta = \{((s, a, \epsilon), (s, a)), ((s, b, a), (s, \epsilon)), ((s, \$, \epsilon), (f, \epsilon)), ((f, \epsilon, a), (f, \epsilon))\}$. While reading $w$, the stack contains one $a$ for each unmatched $a$ in the prefix read so far. If a prefix has more $b$’s than $a$’s, $M$ cannot read the $b$ that causes the excess, so it rejects. Otherwise, $M$ reads all of $w$, consumes $\$$, and enters $f$, where it empties the remaining stack and accepts. $M$ is deterministic because its transitions do not compete, and it has no available transition from an accepting configuration with empty input and empty stack. Thus, $M$ accepts exactly $L\$$, so $L$ is deterministic context-free. $\proofend$

b)
Let $\$$ be an end-of-string marker. Define $M = (\{s, B, C, f\}, \{a, b, c, \$\}, \{a\}, \Delta, s, \{f\})$, where
$$
\begin{align}
\Delta = \{&
((s, a, \epsilon), (s, a)),\\
&((s, b, a), (B, \epsilon)),
((s, c, a), (C, \epsilon)),\\
&((B, b, a), (B, \epsilon)),
((C, c, a), (C, \epsilon)),\\
&((s, \$, \epsilon), (f, \epsilon)),
((B, \$, \epsilon), (f, \epsilon)),
((C, \$, \epsilon), (f, \epsilon))
\}.
\end{align}
$$
In state $s$, $M$ pushes one $a$ onto the stack for each $a$ read. Reading the first $b$ moves $M$ to $B$, where it pops one $a$ for each $b$ read; similarly, reading the first $c$ moves $M$ to $C$, where it pops one $a$ for each $c$ read. Neither $B$ nor $C$ permits any further $a$’s, and neither permits switching between $b$’s and $c$’s. On reading $\$$, $M$ enters $f$ without changing its stack. Since acceptance requires both an accepting state and an empty stack, $M$ accepts exactly when the number of $b$’s or $c$’s equals the number of preceding $a$’s. Too many $b$’s or $c$’s cause $M$ to get stuck when it attempts to pop an empty stack, while too few leave a nonempty stack in $f$. The input $\$$ is also accepted by moving directly from $s$ to $f$ with an empty stack, accounting for $n=0$. Therefore, $M$ accepts exactly $L\$$. Finally, $M$ is deterministic because every transition consumes an input symbol, no two transitions from the same state read the same symbol, and $f$ has no outgoing transitions. Thus, $L$ is deterministic context-free. $\proofend$

<div class="page-break"></div>

**Problem 18**
Show that $L = \{a^nb^n : n \ge 0\} \cup \{a^nb^{2n} : n \ge 0\}$ is not deterministic context-free.
**Solution**
Suppose $L$ were deterministic context-free, and let $M$ be a deterministic PDA accepting $L\$$. Construct $N$ using the following algorithm.
$\operatorname{buildN}(M)$:
1. Set $P = \operatorname{convertPDAtodetnormalform}(M)$, with state set $K$ and accepting set $A$.
2. For a stack string $\gamma$, define $E_\gamma = \{(q,u) \in K \times \{\epsilon,\$\} : (q,u,\gamma) \vdash_P^* (f,\epsilon,\epsilon) \text{ for some } f \in A\}$. Although there are infinitely many stack strings, there are at most $2^{2|K|}$ different sets $E_\gamma$.
3. Augment $P$’s states to record (have) $(q,E_\gamma)$. For each stack symbol $X$, the value of $E_{X\gamma}$ is determined by $X$ and $E_\gamma$: record which state and remaining input can result when $X$ and everything pushed above it have been removed, then check whether that pair belongs to $E_\gamma$. On pushing $X$, save $E_\gamma$ with $X$ and replace the recorded set by $E_{X\gamma}$; on popping $X$, restore the saved set. This requires only finitely many additional states and stack symbols.
4. Create $N_0$ with two copies of the augmented machine’s states and transitions, sharing one stack. Its start state is the first copy’s start state.
5. In the first copy, retain only transitions reading $a$, $b$, or $\epsilon$, and make every state nonaccepting.
6. In the second copy, retain the $\epsilon$- and $\$$-transitions, change every transition reading $b$ to read $c$, and remove every transition reading $a$. Retain this copy’s accepting states.
7. From each first-copy state recording $(q,E_\gamma)$, add an $\epsilon$-transition to the corresponding second-copy state exactly when $(q,\$) \in E_\gamma$. This transition leaves the stack unchanged.
8. Construct a DFSM $D$ accepting $a^+b^+c^+\$$. Return $\operatorname{intersectPDAandFSM}(N_0,D)$.

The restriction from $D$ forces the switch between copies to occur after the last $b$ and before the first $c$. Step 7 allows this switch exactly when the prefix $a^ib^j$ belongs to $L$. The second copy then continues the same computation, treating each $c$ as a $b$, and accepts exactly when $a^ib^{j+k} \in L$. Since $P$ is deterministic, these checks concern the same computation up to the switch. Thus, $N$ accepts $a^ib^jc^k\$$ exactly when $j \in \{i,2i\}$ and $j+k \in \{i,2i\}$, where $i,j,k>0$. Since $k>0$, these conditions force $j=k=i$. Consequently, $\operatorname{without\$}(N)$ accepts exactly $\{a^nb^nc^n : n>0\}$, contradicting the fact that this language is not context-free. Therefore, $L$ is not deterministic context-free. $\proofend$

<div class="page-break"></div>

**Problem 22(d, e, f, g)**
For each of the following claims, state whether it is True or False. Prove your answer.
d) If $L_1$ and $L_2$ are context-free languages and $L_1 \subseteq L \subseteq L_2$, then $L$ must be context-free.
e) If $L_1$ is a context-free language and $L_2 \subseteq L_1$, then $L_2$ must be context-free.
f) If $L_1$ is a context-free language and $L_2 \subseteq L_1$, it is possible that $L_2$ is regular.
g) A context-free grammar in Chomsky normal form is always unambiguous.
**Solution**
d)
False. As noted in part (e) and (f), both $\emptyset$ and $\{a, b, c\}^*$ are context-free. However, $\emptyset \subset A^nB^nC^n \subset \{a, b, c\}^*$ where $A^nB^nC^n$ is not context-free as discovered in the book. $\proofend$

e)
False. Take $L_1 = \{a^nb^nc^m \in \{a, b, c\}^* \mid n,m \ge 0\}$ and $L_2 = A^nB^nC^n$. Notice $L_2 \subset L_1$ but, again, $L_2$ is not context-free. However, $L_1 = (A^nB^n)c^*$ where $A^nB^n$ was shown to be context-free in the book and $c^*$ is regular, making it also context-free. Since context-free languages are closed under concatenation, $L_1$ is context-free. $\proofend$

f)
True. Take any context-free language $L_1$ and set $L_2 = \emptyset$. Then $L_2 \subseteq L_1$. Also, the regular expression $\emptyset = L_2$ meaning $L_2$ is a regular language as desired. $\proofend$

g)
False. Define $G = (\{S, a\}, \{a\}, \{(S, SS), (S, a)\}, S)$ and consider $w = aaa$. We see that $c_1 := S \Rightarrow_G SS \Rightarrow_G SSS \Rightarrow_G aSS \Rightarrow_G aaS \Rightarrow_G aaa$ and $c_2 := S \Rightarrow_G SS \Rightarrow_G aS \Rightarrow_G aSS \Rightarrow_G aaS \Rightarrow_G aaa$ both derive $w$. These are distinct leftmost derivations and therefore represent distinct parse trees for $w$. Hence, $G$ is ambiguous. But every production has the form $X \to YZ$ or $X \to a$, so $G$ is in Chomsky normal form. $\proofend$

<div class="page-break"></div>

# Ch 14 (14.4)

**Problem 1(a, b, c, d, e)**
Give a decision procedure to answer each of the following questions:
a) Given a regular expression $\alpha$ and a PDA $M$, is the language accepted by $M$ a subset of the language generated by $\alpha$?
b) Given a context-free grammar $G$ and two strings $s_1$ and $s_2$, does $G$ generate $s_1s_2$?
c) Given a context-free grammar $G$, does $G$ generate at least three strings?
d) Given a context-free grammar $G$, does $G$ generate any even length strings?
e) Given a regular grammar $G$, is $L(G)$ context-free?
**Solution**
a)
Convert $\alpha$ to a DFSM $D$ over the combined input alphabet of $\alpha$ and $M$. Complement $D$ by swapping accepting and nonaccepting states. Construct a PDA (closure of context-free languages with regular languages in intersection and `intersectPDAandFSM`) for $L(M) \cap \neg L(D)$, convert it to a context-free grammar, and apply the context-free language emptiness decision procedure. Answer Yes exactly when this language is empty, since $L(M) \subseteq L(D)$ iff $L(M) \cap \neg L(D) = \emptyset$. Each construction and the emptiness test terminate, so this is a decision procedure. $\proofend$

b)
Return `decideCFLusingGrammar(G, `$s_1s_2$`)` as defined in the book which terminates. $\proofend$

c)
Initialize $F = \emptyset$. Repeat the following at most three times: construct a grammar for $L(G) \setminus F$ and test it for emptiness. This construction is possible because $F$ is finite and therefore regular, and context-free languages are closed under difference with regular languages. If the remaining language is empty, answer No. Otherwise, enumerate finite derivations in its grammar until a terminal string $w$ is found, and add $w$ to $F$. If three distinct strings have been found, answer Yes. Each search for a string terminates because the preceding emptiness test guarantees that one exists. Removing $F$ ensures that the strings found are distinct. Hence, the procedure terminates and answers Yes exactly when $G$ generates at least three strings. $\proofend$

d)
Let $\Sigma$ be the terminal alphabet of $G$. Construct a DFSM for the regular language $E = \{w \in \Sigma^* : |w| \text{ is even}\}$ by using two states that track length parity, with the even state initial and accepting (reference 1a from chapter 13 as well). Construct a grammar for $L(G) \cap E$ and apply the context-free language emptiness decision procedure. Answer Yes exactly when the intersection is nonempty. This includes $\epsilon$, whose length is even. All steps terminate. $\proofend$

e)
Always answer Yes. Every regular grammar generates a regular language, and every regular language is context-free. This procedure immediately terminates and is correct for every input. $\proofend$

