# Chapter 0: Seeing Arithmetic
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## 0.0 Seeing Arithmetic
---
### Key Concepts
- **Aggregation**:
  - Puts two "things" together, addition is the complement to this.
- **Partnering**:
  - Consider sequence of sums in pairs.
  - Triplication is a special case of duplication where instead three copies of the sum are used.
- **Hasse Diagrams**:
  - Display divisibility properties among numbers.
### Definitions
- **Triangle Number**
  - $\sum_{k = 1}^nk = \frac{n(n+1)}{2}$ for every $n \in \mathbb{N}$.
- **Ordered Pair**
  - $\forall a,b \in S (a, b)$, typically $|S|^2$ total.
- **Unordered Pair**
  - $\forall a,b \in S \{a, b\}$, typically $\frac{|S|(|S| - 1)}{2} = \begin{pmatrix} |S| \\ 2 \end{pmatrix}$ total.
- **Summation**
  - $\sum_{k = 1}^{N - 1} = \begin{pmatrix} N \\ 2 \end{pmatrix}$.
- **Floor**
  - $\lfloor{x}\rfloor = max\{n \in \mathbb{Z} : n \le x\}$.
- **Ceiling**
  - $\lceil{x}\rceil = min\{n \in \mathbb{Z} : n \ge x\}$.
- **Counting Multiples**
  - $\forall N, m \in \mathbb{Z}^+ (\lfloor \frac{N}{m} \rfloor = \text{ the number of multiples of m between 1 and N})$.
- **Counting Squares**
  - $\forall N \in \mathbb{Z}^+ (\lfloor \sqrt{N} \rfloor = \text{ the number of squares between 1 and N})$.
- **Counting Digits**
  - $\forall N \in \mathbb{Z}^+ (\text{decimal digits for representation of N} = \lfloor log_{10}(N)\rfloor + 1)$.
- **Counting Bits**
  - $\forall N \in \mathbb{Z}^+ (\text{binary digits for representation of N} = \lfloor log_{2}(N)\rfloor + 1)$.
- **Divides**
  - $x | y \iff \exists m \in \mathbb{N} y = mx$.
  - Reflexive: $x | x$ for all integer x.
  - Anti-symmetric: If $x | y$ and $y | x$, then $x = \pm y$ for any integers x and y.
  - Transitive: $x |y$ and $y | z$ suggests $x | z$ for all integers, x, y, and z.
  - If $d | x$, then $d | xy$ for all integers d, x, and y.
  - If $d | x$ and $d | y$, then $d | (x + y)$ and $d | (x - y)$ for all integers d, x, and y.

### Theorems & Proofs
**Traditional Division**
Let a and be be integers, with b positive. Then there exist integers q and r such that,
$$
a = q(b) + r \land 0 \le r < b
$$

$0 \le \frac{a}{b} - \lfloor\frac{a}{b}\rfloor < 1$ and so $0 \le a - b\lfloor\frac{a}{b}\rfloor < b$. Define $q = \lfloor\frac{a}{b}\rfloor$ and $r = a - q(b)$. **Q.E.D**

**Minimal Remainder Division**
Let a and be be integers, with b positive. Then there exist integers q and r such that,
$$
a = q(b) + r \land -0.5b \le r \le 0.5b
$$

Let q be an integer closest to $\frac{a}{b}$. Thus, $q = \lfloor\frac{a}{b}\rfloor$ or $q = \lceil\frac{a}{b}\rceil$. Therefore, $-0.5 \le \frac{a}{b} - q \le 0.5$ and so $-0.5b \le a - q(b) \le 0.5b$. Define $r = a - q(b)$. **Q.E.D**

**Two Out Of Three Principle**
Let a, b, and c be integers such that $a + b = c$. Let d be an integer. If two of $\{a, b, c\}$ are multiples of d, then the third number is a multiple of d.

### References
- *Book Title* — Chapter X, Pages Y–24
