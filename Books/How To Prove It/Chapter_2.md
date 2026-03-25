# Chapter 2: Proofs
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 2.0 Proof Strategies
---
### Definitions
- **Counterexample**
  - Instance of a theorem that is invalid.

### Formulas
**Prove Conditional**
Assume P and show Q for $P \implies Q$.
Assume $\neg Q$ and show $\neg P$.

### Examples
**Example Title**
**Problem 1:**
Consider,
Theorem. Suppose n is an integer larger than 1 and n is not prime. Then $2^n - 1$ is not prime.
a) Identify the hypotheses and conclusion of the theorem. Are the hypotheses true when $n= 6$? What does the theorem tell you in this instance? Is it right?
b) What can you conclude from the theorem in the case $n = 15$? Check directly that this conclusion is correct.
c) What can you conclude from the theorem in the case $n = 11$?
**Solution:**
a)
The hypothesis are that n is an integer, n is larger than 1, and n is not prime. The conclusion of the theorem is that $2^n - 1$ is not prime. When $n = 6$, n is an integer larger than 1 with factorization $2^1 \times 3^1$, and so not prime. Therefore, the hypothesis are true when $n = 6$. The theorem states $2^6 - 1 = 63$ is not prime. 63 has factorization $3^2 \times 7^1$ and so is not prime, meaning the theorem is right.

b)
15 is an integer larger than 1 that is not prime, meaning the theorem suggests $2^{15} - 1 = 32767$ is not prime. $32767$ is divisible by 7 and so is not prime, meaning the theorem is correct.

c)
11 is prime so the theorem's hypothesis are not met. Therefore, we can not conclude anything from the theorem.

**Problem 2:**
Consider,
Theorem. Suppose that $b^2 > 4ac$. Then the quadratic equation $ax^2 + bx + c = 0$ has exactly two real solutions.
a) Identify the hypotheses and conclusion of the theorem.
b) To give an instance of the theorem, you must specify values for a, b, and c, but not x. Why?
c) What can you conclude from the theorem in the case $a = 2, b = -5, c = 3$? Check directly that this conclusion is correct.
d) What can you conclude from the theorem in the case $a = 2, b = 4, c = 3$?
**Solution:**
a)
The hypothesis are that $b^2 > 4ac$ and the conclusion is $ax^2 + bx + c = 0$ has exactly two real solutions.

b)
x is a bound variable that is the solution determined by choice of a, b, and c. x expresses the theorem and is not of the theorem itself.

c)
$(-5)^2 = 25 > 4(2)(3) = 24$ and so the hypothesis of the theorem is met. Therefore, the theorem concludes that $2x^2 -5x + 3 = 0$ has exactly two real solutions. It is easy to verify that $x = 1, 1.5$ are the only two solutions to the polynomial and so the theorem is correct.

d)
$4^2 = 16 < 4(2)(3) = 24$ and so the hypothesis of the theorem is not met. Therefore, we can not conclude anything from the theorem.

**Problem 3:**
Consider,
Theorem. Suppose n is a natural number larger than 2, and n is not a prime number. Then $2n + 13$ is not a prime number.
What are the hypotheses and conclusion of this theorem? Show that the theorem is incorrect by finding a counterexample.
**Solution:**
The hypotheses are that n is a natural number, n is larger than 2, and n is not a prime number. The conclusion of the theorem is that $2n + 13$ is not a prime number. Let $n = 8$,  which is a natural number larger than 2 that is not prime. The theorem suggests $2(8) + 13 = 29$ is not prime, which is clearly false. Therefore, the theorem is incorrect.

**Problem 4:**
Complete the proof,
Suppose $0 < a < b$. Then $b - a > 0$. \[Fill in proof of $b^2 - a^2 > 0$\]. Since $b^2 - a^2 > 0$, it follows that $a^2 < b^2$. Therefore if $0 < a < b$ then $a^2 < b^2$ $\blacksquare$
**Solution:**
Fill in:
It also follows that since $0 < a < b$, we get $b + a > 0$. But $b - a > 0$ and so $(b - a)(b + a) = b^2 - a^2 > 0$.

**Problem 5:**
Suppose a and b are real numbers. Prove that if $a < b < 0$ then $a^2 > b^2$.
**Solution:**
Suppose $a < b < 0$. Then $a < b$ multiplied by a on both sides is $a^2 > ba$ because a is negative. Similarly, multiplying $a < b$ by b gives the expression $ba > b^2$. It follows that  $a^2 > ba > b^2$ and so $a^2 > b^2$. $\blacksquare$

**Problem 6:**
Suppose a and b are real numbers. Prove that if $0 < a < b$ then $\frac{1}{b} < \frac{1}{a}$.
**Solution:**
Suppose $0 < a < b$. Dividing $a < b$ by b gets $\frac{a}{b} < 1$, because $0 < b$. Similarly, dividing $\frac{a}{b} < 1$ by a gets $\frac{1}{b} < \frac{1}{a}$. $\blacksquare$

**Problem 7:**
Suppose that a is a real number. Prove that if $a^3 > a$ then $a^5 > a$.
**Solution:**
Suppose $a^3 > a$. Notice $a^2 \ge 0 > -1$ and so $a^2 > -1$, where adding 1 shows $a^2 + 1 > 0$. Since $a^3 > a$, subtracting a shows that $a^3 - a > 0$. It follows that $(a^2 + 1)(a^3 - a) = a^5 - a > 0$. Because $a^5 - a > 0$, adding a reveals $a^5 > a$. $\blacksquare$

**Problem 8:**
Suppose $A \backslash B \subseteq C \cap D$ and $x \in A$. Prove that if $x \not \in D$ then $x \in B$.
**Solution:**
We prove by contrapositive. Suppose $x \not \in B$. Since $x \in A$ and $x \not \in B$, it follows that $x \in A \backslash B$. But $A \backslash B \subseteq C \cap D$ and so $x \in C \cap D$. Because $x \in C \cap D$, we get $x \in D$. $\blacksquare$

**Problem 9:**
Suppose $A \cap B \subseteq C \backslash D$. Prove that if $x \in A$, then if $x \in D$ then $x \not \in B$.
**Solution:**
Suppose $x \in A$. We prove if $x \in D$ then $x \not \in B$ by contrapositive. Suppose $x \in B$. Since $x \in A$ and $x \in B$, it follows that $x \in A \cap B$. But $A \cap B \subseteq C \backslash D$, and so $x \in C \backslash D$. By definition then, $x \not \in D$. $\blacksquare$

**Problem 10:**
Suppose a and b are real numbers. Prove that if $a < b$ then $\frac{a + b}{2} < b$.
**Solution:**
Suppose $a < b$. Then adding b to the inequality gives $a + b < 2b$. Dividing by 2 shows that $\frac{a + b}{2} < b$. $\blacksquare$

**Problem 11:**
Suppose x is a real number and $x \ne 0$. Prove that if $\frac{\sqrt[3]{x} + 5}{x^2 + 6} = \frac{1}{x}$ then $x \ne 8$.
**Solution:**
We prove this by contrapositive. Suppose $x = 8$. Then,
$$
\frac{\sqrt[3]{8} + 5}{8^2 + 6} = \frac{7}{70} = \frac{1}{10} \ne \frac{1}{8}
$$
$\blacksquare$

**Problem 12:**
Suppose a, b, c, and d are real numbers, $0 < a < b$, and $d > 0$. Prove that if $ac \ge bd$ then $c > d$.
**Solution:**
Suppose $ac \ge bd$. By problem 6, it must be that $\frac{1}{b} < \frac{1}{a}$ since $0 < a < b$. Because $ac \ge bd$ and $a > 0$, it must be that $c \ge bd \times \frac{1}{a}$. But $0 < \frac{1}{b} < \frac{1}{a}$ and $bd > 0$ so $c \ge bd \times \frac{1}{a} > bd \times \frac{1}{b} = d$. Thus, in particular, $c > d$. $\blacksquare$

**Problem 13:**
Suppose x and y are real numbers, and $3x + 2y \le 5$. Prove that if $x > 1$ then $y < 1$.
**Solution:**
Suppose $x > 1$. Then multiplying by 3 gives $3x > 3$ so that $5 - 3x < 2$. We also see that since $3x + 2y \le 5$, subtracting 3x gives $2y \le 5 - 3x$. Because $5 - 3x < 2$ and $2y \le 5 - 3x$, it follows that $2y < 2$. Dividing $2y < 2$ by 2 reveals that $y < 1$ as desired. $\blacksquare$

**Problem 14:**
Suppose that x and y are real numbers. Prove that if $x^2 + y = -3$ and $2x - y = 2$ then $x = -1$.
**Solution:**
Suppose $x^2 + y = -3$ and $2x - y = 2$. Because $2x - y = 2$, we see that $-y = 2 - 2x$ and multiplying by $-1$ gives $y = 2x - 2$.  Substituting $y = 2x - 2$ into $x^2 + y = -3$ gives $x^2 + 2x - 2 = -3$. Adding 3 reveals $x^2 + 2x + 1 = 0$, which by the quadratic formula has solutions $\frac{-2 \pm \sqrt{2^2 - 4(1)(1)}}{2(1)} = \frac{-2 \pm 0}{2} = -1$. Since $-1$ is the only solution to $x^2 + 2x + 1 = 0$, it must be that $x = -1$. $\blacksquare$

**Problem 15:**
Prove,
Theorem. Suppose $x > 3$ and $y < 2$. Then $x^2 - 2y > 5$.
**Solution:**
Because $x > 3 > 0$,  problem 4 states that $x^2 > 9$. Because $y < 2$, multiplying by $-2$ gives $-2y > -4$ . Since $x^2 > 9$ and $-2y > -4$, we see that $x^2 + (-2y) > 9 - 4 = 5$. $\blacksquare$

**Problem 16:**
Consider,
Theorem. Suppose x is a real number and $x \ne 4$. If $\frac{2x - 5}{x - 4} = 3$ then $x = 7$.
a)
Whats wrong with the following proof of the theorem?
Proof: Suppose $x = 7$. Then $\frac{2x - 5}{x - 4} = \frac{2(7) - 5}{7 - 4} = \frac{9}{3} = 3$. Therefore if $\frac{2x - 5}{x - 4} = 3$ then $x = 7$. $\blacksquare$
b)
Give a correct proof of the theorem.
**Solution:**
a)
The proof shows the converse which is not equivalent.
b)
Suppose $\frac{2x - 5}{x - 4} = 3$, which is well-defined because $x \ne 4$. Multiplying $\frac{2x - 5}{x - 4} = 3$ by $(x - 4) \ne 0$ gives $2x - 5 = 3(x - 4)$ and then adding 5 shows $2x = 3x - 12 + 5$. Subtracting $3x$ and multiplying by -1 gives $x = 7$. $\blacksquare$

**Problem 17:**
Consider,
Suppose that x and y are real numbers and $x \ne 3$. If $x^2y = 9y$, then $y = 0$.
a)
What is wrong with the following proof of the theorem?
Proof: Suppose that $x^2y = 9y$. Then $(x^2 - 9)y = 0$. Since $x \ne 3$, $x^2 \ne 9$, so $x^2 - 9 \ne 0$. Therefore, we can divide both sides of the equation $(x^2 - 9)y = 0$ by $x^2 - 9$, which leads to the conclusion that $y = 0$. Thus, if $x^2y = 9y$, then $y = 0$. $\blacksquare$
b)
Show that the theorem is incorrect by finding a counterexample.
**Solution:**
a)
It does not follow that $x^2 \ne 9$ because $x \ne 3$. If $x = -3$, then $x^2 = 9$.

b)
Let $x = -3$ and $y = 1$. Both x and y are real numbers where $x \ne 3$. Since $x^2y = (-3)^2(1) = 9(1) = 9y$, the theorem states it must be that $y = 0$ but this is clearly not true.

### References
- *Book Title* — Chapter X, Pages Y–100


## 2.1 Proofs Involving Negations And Conditionals
---
### Key Concepts
- **Proof By Contradiction**:
  - Assume the negated goal is true and show this leads to a contradiction.
- **Rules Of Inference**:
  - Draw inferences from givens.

### Formulas
**Prove Negation**
Turn into equivalent positive expression.
Proof by contradiction.

**Use Negation**
Re-express as positive statement.
Use negated given as goal for proof by contradiction.

**Modus Ponens**
$P \implies Q$ and $P$, $\therefore Q$.

**Modus Tollens**
$P \implies Q$ and $\neg Q$, $\therefore \neg P$.

### Examples
**Example Title**
**Problem 1:**
Use the methods for writing proofs discussed so far in this chapter.
a)
Suppose $P \implies Q$ and $Q \implies R$ are both true. Prove that $P \implies R$ is true.
b)
Suppose $\neg R \implies (P \implies \neg Q)$ is true. Prove that $P \implies (Q \implies R)$ is true.
**Solution:**
a)
Suppose P. Because P and $P \implies Q$, we have Q. Then Q and $Q \implies R$, so R. Therefore, $P \implies R$. $\blacksquare$

b)
Suppose P. We show that then $\neg R \implies \neg Q$ must be true. Suppose $\neg R$. Since $\neg R \implies (P \implies \neg Q)$ and $\neg R$, it must be that $P \implies \neg Q$. But P, and so $\neg Q$. Therefore, $\neg R \implies \neg Q$ if P. $\blacksquare$

**Problem 2:**
Use proof techniques of the chapter.
a)
Suppose $P \implies Q$ and $R \implies \neg Q$ are both true. Prove that $P \implies \neg R$ is true.
b)
Suppose that P is true. Prove that $Q \implies \neg(Q \implies \neg P)$ is true.
**Solution:**
a)
Suppose P. Then, because $P \implies Q$, we have Q. But $R \implies \neg Q$ and Q, so it must be that $\neg R$. Therefore, $P \implies \neg R$. $\blacksquare$

b)
Suppose Q. Then we have P and Q, so that $\neg(Q \implies \neg P)$. $\blacksquare$

**Problem 3:**
Suppose $A \subseteq C$, and B and C are disjoint. Prove that if $x \in A$ then $x \not \in B$.
**Solution:**
Suppose $x \in A$. For contradiction, suppose $x \in B$. Since $x \in A$ and $A \subseteq C$, it must be that $x \in C$. But $x \in C$ and $x \in B$ so that $x \in B \cap C$. Since B and C are disjoint, this is a contradiction. Therefore, it must be that $x \not \in B$. $\blacksquare$

**Problem 4:**
Suppose that $A \backslash B$ is disjoint from C and $x \in A$. Prove that if $x \in C$ then $x \in B$.
**Solution:**
Suppose $x \in C$. For contradiction, suppose $x \not \in B$. Since $x \in A$ and $x \not \in B$, it follows that $x \in A \backslash B$. But then $x \in C$ and $x \in A \backslash B$ which is a contradiction, since C is disjoint from $A \backslash B$. Therefore, $x \in B$ if $x \in C$. $\blacksquare$

**Problem 5:**
Prove that it cannot be the case that $x \in A \backslash B$ and $x \in B \backslash C$.
**Solution:**
Suppose $x \in A \backslash B$. By definition then, $x \in A$ and $x \not \in B$. Since $x \not \in B$, it must be that $x \not \in B \backslash C$. Therefore, $x \in A \backslash B$ implies $x \not \in B \backslash C$. Thus, the conclusion follows. $\blacksquare$

**Problem 6:**
Use contradiction to prove,
Suppose $A \cap C \subseteq B$ and $a \in C$. Prove that $a \not \in A \backslash B$.
**Solution:**
For contradiction, suppose $a \in A \backslash B$. Then by definition, $a \in A$ and $a \not \in B$. Since $a \in A$ and $a \in C$, it follows that $a \in A \cap C$. But $A \cap C \subseteq B$ and so it must be that $a \in B$. However, $a \not \in B$ which is a contradiction. Therefore, $a \not \in A \backslash B$. $\blacksquare$

**Problem 7:**
Use contradiction to prove,
Suppose that $A \subseteq B$, $a \in A$, and $a \not \in B \backslash C$. Prove that $a \in C$.
**Solution:**
For contradiction, suppose $a \not \in C$. Since $a \in A$ and $A \subseteq B$, it follows that $a \in B$. Because $a \in B$ and $a \not \in C$, by definition $a \in B \backslash C$. However, this is a contradiction since $a \not \in B \backslash C$. Therefore, $a \in C$. $\blacksquare$

**Problem 8:**
Suppose that $y + x = 2y - x$, and x and y are not both zero. Prove that $y \ne 0$.
**Solution:**
For contradiction, suppose $y = 0$. It follows that since x and y are not both zero, $x \ne 0$. Then adding x and subtracting y to $y + x = 2y - x$ gives $2x = y$. But $y = 0$, so it must be that $2x = 0$ which means $x = 0$. However, x can not be zero so this is a contradiction. Therefore, $y \ne 0$. $\blacksquare$

**Problem 9:**
Suppose that a and b are nonzero real numbers. Prove that if $a < \frac{1}{a} < b < \frac{1}{b}$, then $a < -1$.
**Solution:**
Suppose $a < \frac{1}{a} < b < \frac{1}{b}$. Since $\frac{1}{a} < \frac{1}{b}$, we can infer by modus tollens (if $0 < a < b$ then $\frac{1}{b} < \frac{1}{a}$) that $a < b \implies a \le 0$. It is given that $a < b$, so $a \le 0$. But a is nonzero and $a \le 0$, giving $a < 0$. Since $a < \frac{1}{a}$ and $a < 0$, multiplying by a gives $a^2 > 1$ which is equivalent to $a^2 - 1 = (a+1)(a-1) > 0$. Because $a < 0 < 1$, $a - 1 < 0$ and so it must be that $a + 1 < 0$. This forces $a < -1$ as desired. $\blacksquare$

**Problem 10:**
Suppose that x and y are real numbers. Prove that if $x^2y = 2x + y$, then if $y \ne 0$ then $x \ne 0$.
**Solution:**
Suppose $x^2y = 2x + y$ and $y \ne 0$. For contradiction, suppose $x = 0$. Then substituting x into $x^2y = 2x + y$ gives $0y = 2(0) + y$ which is equivalent to $0 = y$. However, $y \ne 0$ which is a contradiction. Therefore, *f $x^2y = 2x + y$, then if $y \ne 0$ then $x \ne 0$. $\blacksquare$

**Problem 11:**
Suppose that x and y are real numbers. Prove that if $x \ne 0$, then if $y = \frac{3x^2 + 2y}{x^2 + 2}$ then $y = 3$.
**Solution:**
Suppose $x \ne 0$ and $y = \frac{3x^2 + 2y}{x^2 + 2}$. Since $y = \frac{3x^2 + 2y}{x^2 + 2}$, multiplying by $(x^2 + 2)$ gives $yx^2 + 2y = 3x^2 + 2y$. Then subtracting by $2y$ and dividing by $x^2 \ne 0$ (since $x \ne 0$) reveals $y = 3$. $\blacksquare$

**Problem 12:**
Consider,
Theorem. Suppose x and y are real numbers and $x + y = 10$. Then $x \ne 3$ and $y \ne 8$.
a)
Whats wrong with the following proof?
Proof: Suppose the conclusion of the theorem is false. Then $x = 3$ and $y = 8$. But then $x + y = 11$, which contradicts the given information that $x + y = 10$. Therefore the conclusion must be true. $\blacksquare$
b)
Show that the theorem is incorrect by finding a counterexample.
**Solution:**
a)
The false conclusion of the theorem is that $x = 3$ OR $y = 8$, not that $x = 3$ AND $y = 8$.

b)
Let $x = 3$ and $y = 7$ so that $x + y = 10$.

**Problem 13:**
Consider,
Theorem. Suppose that $A \subseteq C$, $B \subseteq C$, and $x \in A$. Then $x \in B$.
a)
What is wrong with the following proof?
Proof: Suppose that $x \not \in B$. Since $x \in A$ and $A \subseteq C$, $x \in C$. Since $x \not \in B$ and $B \subseteq C$, $x \not \in C$. But now we have proven both $x \in C$ and $x \not \in C$, so we have reached a contradiction. Therefore $x \in B$. $\blacksquare$
b)
Show that the theorem is incorrect by finding a counterexample.
**Solution:**
a)
It does not follow that $x \not \in C$ if $x \not \in B$ and $B \subseteq C$. 

b)
$$
A := \{2\}, B := \emptyset, C := \{2\}, x := 2
$$
Clearly $A \subseteq C$, $B \subseteq C$, and $x \in A$ but $x \not \in B$.

**Problem 14:**
Use truth tables to show that modus tollens is a valid rule of inference.
**Solution:**

| P   | Q   | $P \implies Q$ | $\neg Q$ | $\neg P$ |
| --- | --- | -------------- | -------- | -------- |
| F   | F   | T              | T        | T        |
| F   | T   | T              |          |          |
| T   | F   | F              |          |          |
| T   | T   | T              |          |          |

**Problem 15:**
Use truth tables to check the correctness of,
Theorem. Suppose $P \implies (Q \implies R)$. Prove that $\neg R \implies (P \implies \neg Q)$.
**Solution:**

| P   | Q   | R   | $P \implies (Q \implies R)$ | $\neg R \implies (P \implies \neg Q)$ |
| --- | --- | --- | --------------------------- | ------------------------------------- |
| F   | F   | F   | T                           | T                                     |
| F   | F   | T   | T                           | T                                     |
| F   | T   | F   | T                           | T                                     |
| F   | T   | T   | T                           | T                                     |
| T   | F   | F   | T                           | T                                     |
| T   | F   | T   | T                           | T                                     |
| T   | T   | F   | F                           | F                                     |
| T   | T   | T   | T                           | T                                     |

**Problem 16:**
Use truth tables to check the correctness of problem 1.
**Solution:**
a)

| P   | Q   | R   | $P \implies Q$ | $Q \implies R$ | $P \implies R$ |
| --- | --- | --- | -------------- | -------------- | -------------- |
| F   | F   | F   | T              | T              | T              |
| F   | F   | T   | T              | T              | T              |
| F   | T   | F   | T              | F              |                |
| F   | T   | T   | T              | T              | T              |
| T   | F   | F   | F              |                |                |
| T   | F   | T   | F              |                |                |
| T   | T   | F   | T              | F              |                |
| T   | T   | T   | T              | T              | T              |

b)

| P   | Q   | R   | $\neg R \implies (P \implies \neg Q)$ | $P \implies (Q \implies R)$ |
| --- | --- | --- | ------------------------------------- | --------------------------- |
| F   | F   | F   | T                                     | T                           |
| F   | F   | T   | T                                     | T                           |
| F   | T   | F   | T                                     | T                           |
| F   | T   | T   | T                                     | T                           |
| T   | F   | F   | T                                     | T                           |
| T   | F   | T   | T                                     | T                           |
| T   | T   | F   | F                                     |                             |
| T   | T   | T   | T                                     | T                           |

**Problem 17:**
Use truth tables to check the correctness of problem 2.
a)
Suppose $P \implies Q$ and $R \implies \neg Q$ are both true. Prove that $P \implies \neg R$ is true.
b)
Suppose that P is true. Prove that $Q \implies \neg(Q \implies \neg P)$ is true.
**Solution:**
a)

| P   | Q   | R   | $P \implies Q$ | $R \implies \neg Q$ | $P \implies \neg R$ |
| --- | --- | --- | -------------- | ------------------- | ------------------- |
| F   | F   | F   | T              | T                   | T                   |
| F   | F   | T   | T              | T                   | T                   |
| F   | T   | F   | T              | T                   | T                   |
| F   | T   | T   | T              | F                   |                     |
| T   | F   | F   | F              |                     |                     |
| T   | F   | T   | F              |                     |                     |
| T   | T   | F   | T              | T                   | T                   |
| T   | T   | T   | T              | F                   |                     |

b)

| P   | Q   | $Q \implies \neg(Q \implies \neg P)$ |
| --- | --- | ------------------------------------ |
| F   |     |                                      |
| F   |     |                                      |
| T   | F   | T                                    |
| T   | T   | T                                    |

**Problem 18:**
Can the proof be modified to prove that if $x^2 + y = 13$ and $x \ne 3$ then $y \ne 4$? Explain.
Proof: 
Suppose $x^2 + y = 13$ and $y \ne 4$. Suppose $x = 3$. Substituting this into the equation $x^2 + y = 13$, we get $9 + y = 13$, so $y = 4$. But this contradicts the fact that $y \ne 4$. Therefore $x \ne 3$. Thus, if $x^2 + y = 13$ and $y \ne 4$ then $x \ne 3$.
**Solution:**
Yes, the givens would be the same. The strategy would change to contradict $y = 4$ instead of $x = 3$ but can be reached the same way.

### References
- *Book Title* — Chapter X, Pages Y–113

## 2.2 Proofs Involving Quantifiers
---
### Formulas
**Prove Universal Quantifier**
Use arbitrary element.

**Prove Existential Quantifier**
Use particular element.

**Use Existential Quantifier**
Existential Instantiation.

**Use Universal Quantifier**
Universal instantiation.

### Examples
**Example Title**
**Problem 1:**
Prove that if $\exists x (P(x) \implies Q(x))$ then $\forall x P(x) \implies \exists x Q(x)$.
**Solution:**
Suppose $\exists x (P(x) \implies Q(x))$ and name such x, $x_0$, such that $P(x_0) \implies Q(x_0)$. Suppose $\forall x P(x)$. It follows that $P(x_0)$ must be true and since $P(x_0) \implies Q(x_0)$, $Q(x_0)$ must be true. But then we have shown $\forall x P(x) \implies \exists x Q(x)$. Thus, if $\exists x (P(x) \implies Q(x))$ then $\forall x P(x) \implies \exists x Q(x)$. $\blacksquare$

**Problem 2:**
Prove that if A and $B \backslash C$ are disjoint, then $A \cap B \subseteq C$.
**Solution:**
Suppose A and $B \backslash C$ are disjoint and that $x \in A \cap B$. By definition then, $x \in A$ and $x \in B$. Since A is disjoint from $B \backslash C$ and $x \in A$, it must be that $x \not \in B \backslash C$. But $x \in B$ which implies $x \in C$ if $x \not \in B \backslash C$. Since x was arbitrary $A \cap B \subseteq C$. $\blacksquare$

**Problem 3:**
Prove that if $A \subseteq B \backslash C$ then A and C are disjoint.
**Solution:**
Suppose $A \subseteq B \backslash C$. Let x be arbitrary and suppose $x \in A$. Since $A \subseteq B \backslash C$ and $x \in A$, it follows that $x \in B \backslash C$. By definition then, $x \not \in C$. But x was arbitrary, so A and C must be disjoint. $\blacksquare$

**Problem 4:**
Suppose $A \subseteq \mathcal{P}(A)$. Prove that $\mathcal{P}(A) \subseteq \mathcal{P}(\mathcal{P}(A))$.
**Solution:**
Let x be arbitrary and suppose $x \in \mathcal{P}(A)$. By definition, $x \subseteq A$. Let y be arbitrary and suppose $y \in x$. Let z be arbitrary and suppose $z \in y$. Since $x \subseteq A$ and $y \in x$, it must be that $y \in A$. Then $y \in A$ and $A \subseteq \mathcal{P}(A)$ so that $y \in \mathcal{P}(A)$. By definition, it follows that $y \subseteq A$. Because $z \in y$ and $y \subseteq A$, it must be that $z \in A$. Therefore, from arbitrary element z, $y \subseteq A$ which is equivalent to $y \in \mathcal{P}(A)$. But y was arbitrary so that $x \subseteq \mathcal{P}(A)$ which is equivalent to $x \in \mathcal{P}(\mathcal{P}(A))$. Thus, because x was arbitrary, $\mathcal{P}(A) \subseteq \mathcal{P}(\mathcal{P}(A))$. $\blacksquare$

**Problem 5:**
The hypothesis of the theorem in problem 4 is $A \subseteq \mathcal{P}(A)$.
a)
Can you think of a set A for which this hypothesis is true?
b)
Can you think of another?
**Solution:**
a)
The empty set is one obvious candidate.

b)
Another candidate is $\{\emptyset, \{\emptyset\}\}$.

**Problem 6:**
Suppose x is a real number.
a)
Prove that if $x \ne 1$ then there is a real number y such that $\frac{y + 1}{y - 2} = x$.
b)
Prove that if there is a real number y such that $\frac{y + 1}{y-2} = x$, then $x \ne 1$.
**Solution:**
a)
Suppose $x \ne 1$. Let $y = \frac{2x + 1}{x - 1}$ which is well defined since $x \ne 1$ and so $x - 1 \ne 0$. We see that $\frac{y + 1}{y - 2} = \frac{\frac{2x + 1}{x - 1} + 1}{\frac{2x + 1}{x - 1} - 2} = \frac{\frac{3x}{x-1}}{\frac{3}{x-1}} = \frac{3x}{3} = x$ as desired. $\blacksquare$

b)
Suppose there is a real number y such that $\frac{y + 1}{y-2} = x$. For contradiction, suppose $x = 1$. Multiplying by $y - 2$ gives $y + 1 = xy - 2x$. Substitute in x to get $y +1 = y - 2$. Subtracting y reveals $1 = -2$ which is a contradiction, therefore $x \ne 1$. $\blacksquare$

**Problem 7:**
Prove that for every real number x, if $x > 2$ then there is a real number y such that $\frac{y +1}{y} = x$.
**Solution:**
Let x be arbitrary and suppose $x > 2$. Let $y = \frac{1}{x-1}$, which is well defined since $x > 2$ and so $x - 1 > 1 > 0$. We see that $\frac{y +1}{y} = \frac{\frac{1}{x-1} + 1}{\frac{1}{x-1}} = \frac{\frac{x}{x-1}}{\frac{1}{x-1}} = \frac{x}{1} = x$ as desired. $\blacksquare$

**Problem 8:**
Prove that if F is a family of sets and $A \in F$, then $A \subseteq \bigcup F$.
**Solution:**
Suppose F is a family of sets and $A \in F$. Let $x \in A$ be arbitrary. Since $A \in F$ and $x \in A$, it follows that $x \in \bigcup F$. But x was arbitrary so that $A \subseteq \bigcup F$. $\blacksquare$

**Problem 9:**
Prove that if F is a family of sets and $A \in F$, then $\bigcap F \subseteq A$.
**Solution:**
Suppose F is a family of sets and $A \in F$. Let x be arbitrary and suppose $x \in \bigcap F$. Since $x \in \bigcap F$ and $A \in F$, it follows that $x \in A$. But x was arbitrary and so $\bigcap F \subseteq A$. $\blacksquare$

**Problem 10:**
Suppose that F is a nonempty family of sets, B is a set, and $\forall A \in F(B \subseteq A)$. Prove that $B \subseteq \bigcap F$.
**Solution:**
Let x be arbitrary and suppose $x \in B$. Then let Z be arbitrary and suppose $Z \in F$. Since $Z \in F$ and $\forall A \in F(B \subseteq A)$, it follows that $B \subseteq Z$. But $x \in B$ so it must be that $x \in Z$. Because Z was arbitrary element of F, $x \in \bigcap F$. Therefore, from arbitrary x, $B \subseteq \bigcap F$. $\blacksquare$

**Problem 11:**
Suppose that F is a family of sets. Prove that if $\emptyset \in F$ then $\bigcap F = \emptyset$.
**Solution:**
Suppose $\emptyset \in F$. Let x be arbitrary. Since $\emptyset \in F$, for $x \in \bigcap F$ it must be that $x \in \emptyset$ which is always false. Therefore $x \not \in \bigcap F$. But x was arbitrary, so no element is in $\bigcap F$. Thus, $\bigcap F = \emptyset$. $\blacksquare$

**Problem 12:**
Suppose F and G are families of sets. Prove that if $F \subseteq G$ then $\bigcup F \subseteq \bigcup G$.
**Solution:**
Suppose $F \subseteq G$. Let x be arbitrary and suppose $x \in \bigcup F$. By definition then, there is some $Z \in F$ such that $x \in Z$. Because $F \subseteq G$ and $Z \in F$, it must be that $Z \in G$. But then $Z \in G$ and $x \in Z$ so that $x \in \bigcup G$. Therefore, from arbitrary x, $\bigcup F \subseteq \bigcup G$. $\blacksquare$

**Problem 13:**
Suppose F and G are nonempty families of sets. Prove that if $F \subseteq G$ then $\bigcap G \subseteq \bigcap F$.
**Solution:**
Suppose $F \subseteq G$ and let $x \in \bigcap G$ be arbitrary. Let $Z \in F$ be arbitrary. Since $F \subseteq G$ and $Z \in F$, it follows that $Z \in G$. But $x \in \bigcap G$ and so it must be that $x \in Z$. Because Z was arbitrary, $x \in \bigcap F$. Thus, from arbitrary x, $\bigcap G \subseteq \bigcap F$. $\blacksquare$

**Problem 14:**
Suppose that $\{A_i | i \in I\}$ is an indexed family of sets. Prove that $U_{i \in I}\mathcal{P}(A_i) \subseteq \mathcal{P}(U_{i \in I}A_i)$.
**Solution:**
Let $x \in \bigcup_{i \in I}\mathcal{P}(A_i)$ be arbitrary and let $y \in x$ be arbitrary. By definition of $x \in \bigcup_{i \in I}\mathcal{P}(A_i)$, there is some $b \in I$ such that $x \in \mathcal{P}(A_b)$. It follows that $x \subseteq A_b$ and, since $y \in x$, we must have $y \in A_b$. Therefore, $y \in \bigcup_{i \in I} A_i$ and because y was arbitrary, $x \subseteq \bigcup_{i \in I}A_i$. This is equivalent to $x \in \mathcal{P}(\bigcup_{i \in I}A_i)$. But x was arbitrary and so $U_{i \in I}\mathcal{P}(A_i) \subseteq \mathcal{P}(U_{i \in I}A_i)$. $\blacksquare$

Finish these ...

### References
- *Book Title* — Chapter X, Pages Y–130


## 2.3 Proofs Involving Conjunctions And Biconditionals
---
### Formulas
**Prove Conjunction**
Prove both predicates.

**Use Conjunction**
Split into two givens.

**Prove BiConditional**
String of equivalences.
Same as conjunction.

### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.

### References
- *Book Title* — Chapter X, Pages Y–142


## 2.4 Proofs Involving Disjunctions
---
### Formulas
**Use Disjunction**
Split given into cases.
Disjunctive syllogism.

**Prove Disjunction**
Prove either predicate.

### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.

### References
- *Book Title* — Chapter X, Pages Y–153


## 2.5 Existence And Uniqueness Proofs
---
### Formulas
**Prove Uniqeness**
$\exists x (P(x) \land \forall y (P(y) \implies y = x))$.
$\exists x \forall y (P(y) \iff y = x)$.
$\exists x P(x) \land \forall y \forall z ((P(y) \land P(z)) \implies y = z)$.  

### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.

### References
- *Book Title* — Chapter X, Pages Y–162


## 2.6 More Examples Of Proofs
---
### Examples
**Example Title**
**Problem 1:**
Suppose F is a family of sets. Prove that there is a unique set A that has the following two properties:
a) $F \subseteq \mathcal{P}(A)$.
b)  $\forall B (F \subseteq \mathcal{P}(B) \implies A \subseteq B)$.
**Solution:**
Let $A = \bigcup F$. (a) Let x be arbitrary and suppose $x \in F$. Let y be arbitrary and suppose $y \in x$. Since $x \in F$ and $y \in x$, by definition then $y \in \bigcup F$. But $A = \bigcup F$ and so $y \in A$. Because y was arbitrary, we have $x \subseteq A$ which is equivalent to $x \in \mathcal{P}(A)$. Therefore, from arbitrary x, $F \subseteq \mathcal{P}(A)$. (b) Let B be arbitrary and suppose $F \subseteq \mathcal{P}(B)$. Let z be arbitrary and suppose $z \in A$. Since $A = \bigcup F$, we have $z \in \bigcup F$. By definition, there is some $Z \in F$ such that $z \in Z$. Because $F \subseteq \mathcal{P}(B)$, it follows that $Z \in \mathcal{P}(B)$ which is equivalent to $Z \subseteq B$. Then $z \in Z$ and $Z \subseteq B$ so that $z \in B$. However, z was arbitrary and so $A \subseteq B$. From arbitrary B, we can finally conclude that $\forall B (F \subseteq \mathcal{P}(B) \implies A \subseteq B)$. Now we show uniqueness, let C be arbitrary and suppose both properties hold for C. Since $F \subseteq \mathcal{P}(A)$, property b of set C implies that $C \subseteq A$. Similarly, $A \subseteq C$. But then $C \subseteq A$ and $A \subseteq C$ so that $A = C$. Therefore, A is both unique and exists. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–172
