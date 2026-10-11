# Chapter 3: Numerical Sequences And Series

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 3.1 Numerical Sequences And Series

---

### Key Concepts

- **Sequence Summation**: Given $\{a_n\}$, we denote $\sum_{n=p}^q a_n (p \le q) = a_p + a_{p+1} + ... + a_q$. We associate $\{s_n\}$ with $s_n = \sum_{k=1}^n a_k$, or also denoted by $a_1 + a_2 + ...$ or $\sum_{n=1}^\infty a_n$.

### Definitions

- **Converge**: Sequences $\{p_n\}$ of metric space $X$ converges if $\exists p \in X \forall \epsilon > 0\exists N \in \mathbb{Z}$ such that $n \ge N \implies d(p_n, p) < \epsilon$, denoted $p_n \to p$ or $\lim_{n \to \infty} p_n = p$.
- **Diverge**: Does not converge.
- **Bounded**: Sequence with bounded range.
- **Subsequence**: Given $\{p_n\}$, consider $\{n_k\}$ of positive integers, such that $n_1 < n_2 < n_3 < ...$. Then the sequence $\{p_{n_i}\}$ is a subsequence of $\{p_n\}$. 
- **Subsequential Limit**: The limit of a subsequence if it converges.
- **Cauchy Sequence**: Sequence $\{p_n\}$ such that $\forall \epsilon > 0 \exists N$ where $d(p_n, p_m) < \epsilon$ if $n, m \ge N$.
- **Diameter**: Let $\emptyset \ne E \subseteq X$ for metric space $X$ and $S = \{d(p, q) \in R | p, q \in E\}$. The diameter of $E$ is $\sup S$.
- **Complete**: Metric Space in which every Cauchy sequence converges.
- **Monotonically Increasing**: Sequence $\{s_n\}$ of reals such that $s_n \le s_{n+1}$.
- **Monotonically Decreasing**: Sequence $\{s_n\}$ of reals such that $s_n \ge s_{n+1}$.
- **$s_n \to + \infty$**: Let $\{s_n\}$ be a sequence. $s_n \to + \infty$ means that for every real $M$, $\exists N$ such that $n \ge N$ implies $s_n \ge M$. 
- **$s_n \to - \infty$**: Let $\{s_n\}$ be a sequence. $s_n \to - \infty$ means that for every real $M$, $\exists N$ such that $n \ge N$ implies $s_n \le M$. 
- **Upper Limit**: Let $E = \{x | \exists \{s_{n_k}\} (s_{n_k} \to x)\}$ for $x$ in the extended real number system. Then the upper limit is $s^* = \sup E$ and we denote $\lim_{n \to \infty} \sup s_n = s^*$.
- **Lower Limit**: Let $E = \{x | \exists \{s_{n_k}\} (s_{n_k} \to x)\}$ for $x$ in the extended real number system. Then the lower limit is $s_* = \inf E$ and we denote $\lim_{n \to \infty} \inf s_n = s_*$.
- **(Infinite) Series**: $\sum_{n=1}^\infty a_n$ for sequence $\{a_n\}$. Each $s_n$ is called a partial sum. If $\{s_n\} \to s$ we denote $\sum_{n=1}^\infty a_n = s$.

### Examples

**Basic Example**
Present a simple case that demonstrates the preceding definitions or concepts.
> Presented example...

### Axioms

- **Example Axiom**: A foundational assumption used within the subject area.

### Results & Proofs

**Theorem: Properties Of Convergent Points**
Let $\{p_n\}$ be a sequence in a metric space $X$.
a) $\{p_n\}$ converges to $p \in X$ iff every neighborhood of $p$ contains $p_n$ for all but finitely many $n$.
b) If $p \in X$, $p' \in X$, and if $\{p_n\}$ converges to $p$ and to $p'$, then $p = p'$.
c) If $\{p_n\}$ converges, then $\{p_n\}$ is bounded.
d) If $E \subseteq X$and if $p$ is a limit point of $E$, then there is a sequence $\{p_n\}$ in $E$ such that $p = \lim_{n \to \infty}p_n$.

**Theorem: Convergence Related To Algebraic Operations**
Suppose $\{s_n\}$, $\{t_n\}$ are complex sequences, and $\lim_{n \to \infty}s_n = s$, $\lim_{n \to \infty} t_n = t$. Then,
a) $\lim_{n \to \infty} (s_n + t_n) = s + t$;
b) $\lim_{n \to \infty}cs_n = cs$, $\lim_{n \to \infty} (c + s_n) = c + s$ for any number $c$;
c) $\lim_{n \to \infty} s_n t_n = st$;
d) $\lim_{n \to \infty} \frac{1}{s_n} = \frac{1}{s}$, provided $s_n \ne 0$ and $s \ne 0$.

**Theorem: Euclidean Space Convergence**
a) Suppose $x_n \in R^k$ ($n = 1, 2, 3, ...$) and $x_n = (\alpha_{1, n}, ..., \alpha_{k, n})$. Then $\{x_n\}$ converges to $x = (\alpha_1, ..., \alpha_k)$ iff $\lim_{n \to \infty}\alpha_{j, n} = \alpha_j$ $(1 \le j \le k)$.
b) Suppose $\{x_n\}$, $\{y_n\}$ are sequences in $R^k$, $\{\beta_n\}$ is a sequence of real numbers, and $x_n \to x$, $y_n \to y$, $\beta_n \to \beta$. Then $\lim_{n \to \infty} (x_n + y_n) = x + y$, $\lim_{n \to \infty}x_n \cdot y_n = x \cdot y$, and $\lim_{n \to \infty}\beta_n x_n = \beta x$.

**Theorem: Convergent Subsequences**
a) If $\{p_n\}$ is a sequence in a compact metric space $X$, then some subsequence of $\{p_n\}$ converges to a point of $X$.
b) Every bounded sequence in $R^k$ contains a convergent subsequence.

**Theorem: Subsequential Limits Closed**
The subsequential limits of a sequence $\{p_n\}$ in a metric space $X$ form a closed subset of $X$.

**Theorem: Properties Of Diameter**
a) If $\overline{E}$ is the closure of $E$ in $X$, then $\text{diam} \overline{E} = \text{diam} E$.
b) If $K_n$ is a sequence of compact sets in $X$ such that $K_n \supseteq K_{n+1}$ and if $\lim_{n \to \infty} \text{diam} K_n = 0$, then $\bigcap_{n=1}^\infty K_n$ consists of exactly one point.

**Theorem: Cauchy Sequence Properties**
a) In metric space $X$, every convergent sequence is a Cauchy Sequence.
b) If $X$ is a compact metric space and if $\{p_n\}$ is a Cauchy Sequence in $X$, then $\{p_n\}$ converges to some point of $X$.
c) In $R^K$, every Cauchy Sequence converges.

**Theorem: Monotonic Sequences Converge**
Suppose $\{s_n\}$ is monotonic. Then $\{s_n\}$ converges iff it is bounded.

**Theorem: Upper Limit Properties**
Let $\{s_n\}$ be a sequence of real numbers. Let $E$ and $s^*$ have their upper limit meanings. Then $s^*$ has the following properties:
a) $s^* \in E$;
b) If $x> s^*$, then $\exists N$ such that $n \ge N$ implies $s_n < x$.
Moreover, $s^*$ is the only number with the properties (a) and (b).

**Theorem: Bounding Upper And Lower Limits**
If $s_n \le t_n$ for $n \ge N$, where $N$ is fixed, then $\lim_{n \to \infty}\text{inf} s_n \le \lim_{n \to \infty}\text{inf} t_n$ and $\lim_{n \to \infty}\text{sup} s_n \le \lim_{n \to \infty}\text{sup} t_n$.

**Theorem: Special Sequences**
a) If $p>0$, then $\lim_{n \to \infty} \frac{1}{n^p} = 0$;
b) If $p>0$, then $\lim_{n \to \infty} \sqrt[n]{p} = 1$.
c) $\lim_{n \to \infty} \sqrt[n]{n} = 1$.
d) If $p>0$ and $\alpha$ is real, then $\lim_{n \to \infty}\frac{n^\alpha}{(1+p)^n} = 0$.
e) If $|x| < 1$, then $\lim_{n \to \infty}x^n = 0$.

**Theorem: Cauchy Criterion As Series**
$\sum a_n$ converges iff for every $\epsilon > 0$ there is an integer $N$ such that $|\sum_{k = n}^m a_k| \le \epsilon$ if $m \ge n \ge N$.

**Theorem: Series Convergent Terms**
If $\sum a_n$ converges, then $\lim_{n \to \infty}a_n = 0$.

**Theorem: Nonnegative Term Sequence Convergence**
A series of nonnegative terms converges iff its partial sums form a bounded sequence.

**Theorem: Comparison Test**
a) If $|a_n| \le c_n$ for $n \ge N_0$, where $N_0$ is some fixed integer, and if $\sum c_n$ converges, then $\sum a_n$ converges.
b) If $a_n \ge d_n \ge 0$ for $n \ge N_0$, and if $\sum d_n$ diverges, then $\sum a_n$ diverges.

**Theorem: Geometric Series**
If $0 \le x < 1$, then $\sum_{n=0}^\infty x^n = \frac{1}{1-x}$. If $x \ge 1$, the series diverges.

### Visual Aids

**Example Comparison [Table]**

|Criterion|Example Case A|Example Case B|
|---|---|---|
|Property 1|Value or description|Value or description|
|Property 2|Value or description|Value or description|
|Property 3|Value or description|Value or description|

**Example Process or Structure [Diagram]**

> Insert a diagram illustrating the relevant process, structure, hierarchy, mapping, or relationship.

### Notable Quotes

- **Example Author**: “Insert a relevant quotation here.”

### Common Pitfalls

- **Example Pitfall**: Describe a common misconception, invalid assumption, implementation error, or misuse of a method.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
- **Supporting Result [Paper]**: [Example Author, “Example Paper Title,” Year](https://example.com/)
- **Prerequisites [Internal Link]**: [[prerequisite_chapter]]
- **Course Material [Lecture]**: [Example Lecture or Recording](https://example.com/)
- **Supplementary Resource [Website]**: [Example Resource](https://example.com/)