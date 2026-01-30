# Chapter 0: Basic Notions
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 0.0 Vector Spaces
---
### Definitions
- **Vector Space**
  - A collection of vectors along with the operations addition of vectors and scalar multiplication.
  - (1) Additive Commutative.
  - (2) Additive Associative.
  - (3) Zero vector: $\forall v \in V (v + 0 = v)$.
  - (4) Additive Inverse.
  - (5) Multiplicative identity.
  - (6) Multiplicative Associativity.
  - (7) $\forall \alpha \in F \forall u, v \in V (\alpha (u + v) = \alpha u + \alpha v)$.
  - (8) $\forall \alpha , \beta \in F \forall v \in V ((\alpha + \beta)v = \alpha v + \beta v)$.
  - If $F = \mathbb{R}$, V is the real vector space.
  - If $F = \mathbb{C}$, V is the complex vector space.
  - V can be a vector space over arbitrary $\mathbb{F}$.
- **Matrix Notation**
  - $A = (a_{j, k})^{m, n}_{j = 1, k = 1} = \begin{pmatrix} a_{1,1} & a_{1,2} & ... & a_{1, n} \\ ... & ... & ... & ... \\ a_{m, 1} & a_{m, 2} & ... & a_{m, n} \end{pmatrix}$.
- **Matrix Transpose**
  - $\forall j, k \in \mathbb{Z} (1 \le j \le m \land 1 \le k \le n \implies (A^T)_{j,k} = (A)_{k, j})$.

### Examples
**Example Title**
**Problem 1.1:**
Let $x = (1, 2, 3)^T$ , $y = (y_1, y_2, y_3)^T$ , $z = (4, 2, 1)^T$ . Compute $2x, 3y, x + 2y - 3z$.
**Solution:**
$$
2x = (2, 4, 6)^T, 3y = (3y_1, 3y_2, 3y_3)^T, x + 2y - 3z = (2y_1 - 11, 2y_2 - 4, 2y_3)^T
$$

**Problem 1.2:**
Which of the following sets (with natural addition and multiplication by a scalar) are vector spaces. Justify your answer.
a) The set of all continuous functions on the interval $[0, 1]$;
b) The set of all non-negative functions on the interval $[0, 1]$;
c) The set of all polynomials of degree exactly n;
d) The set of all symmetric $n \times n$ matrices, i.e. the set of matrices $A = \{a_{j,k}\}^n_{j,k=1}$ such that $A^T = A$.
**Solution:**
Too trivial and tedious.


**Problem 1.3:**
True or false:
a) Every vector space contains a zero vector;
b) A vector space can have more than one zero vector;
c) An $m \times n$ matrix has m rows and n columns;
d) If f and g are polynomials of degree n, then $f + g$ is also a polynomial of degree n;
e) If f and g are polynomials of degree at most n, then $f + g$ is also a polynomial of degree at most n
**Solution:**
a)
True by axiom 3.

b)
False by problem 1.4.

c)
True by standard notation.

d)
False.
$$
f + g = f_0 + f_1x + ... + f_nx^n + g_0 + g_1x + ... + g_nx^n = (f_0 + g_0) + (f_1 + g_1)x + ... + (f_n + g_n)x^n
$$
which has degree n - 1 when $f_n + g_n = 0$. 

e)
True.
Suppose f and g are polynomials of degree at most n. Then suppose $f + g$ is a polynomial of degree more than n, namely $n + m$ for some $m \in \mathbb{N}$ where $m > 0$.
Then,
$$
f + g = (f_0 + g_0) + ... (f_{n + m} + g_{n + m})x^{n + m}
$$
$$
= f_0 + f_1x + ... + f_{n + m}x^{n + m} + g_0 + g_1x + ... + g_{n + m}x^{n + m}
$$
which suggests f has degree $m + n$ and g has degree $m + n$. However, this is a contradiction because f and g have degree at most n which is less than $m + n$. Therefore, if f and g are polynomials of degree at most n, then $f + g$ is also a polynomial of degree at most n.

**Problem 1.4:**
Prove that a zero vector 0 of a vector space V is unique.
**Solution:**
Define arbitrary $v \in V$.
Existence - By axiom 3 of vector spaces, we can pick some $v_0 \in V$ where $v + v_0 = v$.
Uniqueness - Define arbitrary $v_p \in V$ and suppose $v + v_p = v$. Apply $v_0$ to $v + v_p = v$ such that $v_0 + v_p = v_0$. But we also have $v_p + v_0 = v_p$ from applying $v_p$ to $v + v_0 = v$. By axiom 1, $v_0 + v_p = v_p + v_0$ and so $v_p = v_0$.
Therefore, a zero vector 0 of a vector space V is unique.

**Problem 1.5:**
What matrix is the zero vector of the space $M_{2\times3}$?
**Solution:**
Define $M_0 = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}$.
Let v be arbitrary and suppose $v \in V$. Notice,
$$
v + M_0 = \begin{pmatrix} v_{1,1} + 0 & v_{1, 2} + 0 & v_{1, 3} + 0 \\ v_{2, 1} + 0 & v_{2, 2} + 0 & v_{2, 3} + 0 \end{pmatrix} = v
$$
and so $M_0$ is a zero vector and unique by problem 1.4.

**Problem 1.6:**
Prove that the additive inverse, defined in Axiom 4 of a vector space is unique.
**Solution:**
Define arbitrary $v \in V$.
Existence - By axiom 4 we can pick some $w \in V$ such that $v + w = 0$.
Uniqueness - Define arbitrary $t \in V$ and suppose $v + t = 0$. Since, $v + w = 0$, we get $v + t = v + w$ because the zero vector is unique by problem 1.4. Notice $v + t \in V$ and $v + w \in V$ since addition is closed. Also, we can add vectors giving $w + (v + t) = w + (v + w)$ such that $(w + v) + t = w$ by axiom 2. Finally, $t = w$.
Therefore, the additive inverse, defined in Axiom 4 of a vector space is unique.

**Problem 1.7:**
Prove that $0v = 0$ for any vector $v \in V$.
**Solution:**
Define arbitrary $v \in V$.
$$
0v = (0 + 0)v
$$
since $0 = 0 + 0$.
$$
= (0v + 0v)
$$
by axiom 8.
$$
0v + w = (0v + 0v) + w
$$
by axiom 4 where $w$ is the additive inverse of $0v$.
$$
0 = 0v + (0v + w)
$$
by axiom 2.
$$
= 0v
$$
Therefore, $0v = 0$.

**Problem 1.8:**
Prove that for any vector v its additive inverse −v is given by (−1)v.
**Solution:**
Define arbitrary $v \in V$.
By problem 1.7, $0v = 0$ and
$$
0v = (1 - 1)v = 1v + (-1)v
$$
by axiom 8.
$$
= v + (-1)v
$$
by axiom 5.
So, $v + (-1)v = 0$. By axiom 4 and problem 1.6, $(-1)v$ is then the unique additive inverse to v. 

### References
- *Linear Algebra Done Wrong* — Chapter 1, Pages 1-5


## 0.1 Linear Combinations, Bases.
---
### Definitions
- **Linear Combination**
  - For $v_1, v_2, ..., v_n \in V$, $\sum^n_{k = 1}\alpha_k v_k$.
- **Basis**
  - $v_1, v_2, ..., v_n \in V$ is a basis for vector space V if $\forall v \in V \exists ! \alpha_1, \alpha_2, ..., \alpha_n \in \mathbb{F} (v = \sum^n_{k = 1}\alpha_k v_k)$.
  - $\alpha_1, \alpha_2, ..., \alpha_n$ are called the coordinates.
  - Standard basis is the system $e_1, e_2, ..., e_n \in \mathbb{F}^n$ where $e_k$ has all entries 0 except number k.
  - Standard basis is the system $e_0, e_1, ..., e_n \in \mathbb{P}^n$ where $e_k = t^k$.
- **Generating\Spanning System**
  - A system of vectors $v_1, ..., v_p \in V$ where for any $v \in V$ we get $v = \alpha_1 v_1 + \alpha_2 v_2 + ... + \alpha_p v_p = \sum^p_{k = 1} \alpha_k v_k$.
- **Trivial Linear Combination**
  - $\forall k (\alpha_k = 0)$ in a linear combination.
- **Linearly Independent**
  - A system of vectors such that only the trivial linear combination equals the 0 vector.
### Theorems & Proofs
**Proposition 2.6**
A system of vectors $v_1, ..., v_p \in V$ is linearly dependent iff one of the vectors $v_k$ can be represented as a linear combination of the other vectors.
$$
v_k = \sum^p_{j = 1, j \ne k}\beta_jv_j
$$

Proof:
($\implies$) Suppose the system $v_1, ..., v_p$ is linearly dependent. Then there exists scalars $\alpha_k$ where $\sum^p_{k = 1}|\alpha_k| \ne 0$ such that $\alpha_1 v_1 + ... + \alpha_p v_p = 0$. Let k be the index such that $\alpha_k \ne 0$. Then we get $\alpha_k v_k = - \sum^p_{j = 1, j \ne k}\alpha_j v_j$. Dividing both sides produces $v_k = \sum^p_{j = 1, j \ne k}\frac{- \alpha_j}{\alpha_k} v_j$ which is a linear combination.
($\Longleftarrow$) Suppose one of the vectors $v_k$ can be represented as a linear combination of the other vectors. Then $v_k - \sum^p_{j = 1, j \ne k}\beta_j v_j = 0$. But then we can express the 0 vector non-trivially and so the system is linearly dependent.

**Proposition 2.7**
A system of vectors $v_1, ..., v_p \in V$ is a basis iff it is linearly independent and generating.

Proof:
($\implies$) Suppose a system of vectors $v_1, ..., v_p \in V$ is a basis. By definition then, it is linearly independent and generating.
($\Longleftarrow$) Suppose a system of vectors $v_1, ..., v_p \in V$ is linearly independent and generating. Pick arbitrary $v \in V$. 
Existence - Since the system is generating, we get $v = \sum_{k = 1}^n \alpha_k v_k$. 
Uniqueness - Suppose we also had $v = \sum^n_{k = 1} \beta_k v_k$ for arbitrary $\beta_k$. Then,
$$
\sum^n_{k = 1}(\alpha_k - \beta_k)v_k = \sum_{k = 1}^n \alpha_k v_k - \sum^n_{k = 1} \beta_k v_k = v - v = 0
$$
and so $\forall k (\alpha_k - \beta_k = 0)$ because the system is linearly independent. Therefore, the coordinates are unique.
Thus, a system of vectors $v_1, ..., v_p \in V$ is a basis iff it is linearly independent and generating.

**Proposition 2.8**
Any (finite) generating system contains a basis.

Proof:
Suppose $v_1, v_2, ..., v_p \in V$ is a generating set. Two cases exist, either the system is linearly independent or linearly dependent. Case 1: linearly independent. Then we are done because the system is also generating and so a basis. Case 2: linearly dependent. Then there exists a vector $v_k$ that can be represented as a linear combination of the other vectors by Prop 2.6. Then any linear combination of $v_1, v_2, ..., v_p$ can be represented as a linear combination of the same vectors without $v_k$. If we remove $v_k$, the new system is still generating. If linearly independent, we are done. If not, we continue this procedure. We eventually arrive at a linearly independent and generating system, because otherwise we reach the empty set. Thus, Any (finite) generating system contains a basis.
### Examples
**Example Title**
**Problem 2.1:**
Find a basis in the space of $3 \times 2$ matrices $M_{3 \times 2}$.
**Solution:**
Define ($e_{1}, e_{2}, ..., e_{6}$ in order),
$$
\begin{pmatrix} 1 & 0 \\ 0 & 0 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 1 \\ 0 & 0 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 1 & 0 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 0 & 1 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 0 & 0 \\ 1 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 0 & 0 \\ 0 & 1 \end{pmatrix}
$$
Pick arbitrary $v \in M_{3 \times 2}$. Then set $\alpha_1 = v_{11}, \alpha_2 = v_{12}, ..., \alpha_6 = v_{32}$ and notice,
$$
\alpha_1 e_{1} + \alpha_2 e_{2} + ... + \alpha_6 e_{6} = \begin{pmatrix} v_{11} & v_{12} \\ v_{21} & v_{22} \\ v_{31} & v_{32} \end{pmatrix} = v
$$
and so the system $e_{1}, e_{2}, ..., e_{6}$ is generating. Now we show linear independence.
Define arbitrary $(\alpha_1, \alpha_2, ..., \alpha_6) \in \mathbb{F}^6$. Suppose $\sum_{k = 1}^6 \alpha_k e_k = 0$. Then,
$$
\sum_{k = 1}^6 \alpha_k e_k = \begin{pmatrix} \alpha_1 & \alpha_2 \\ \alpha_3 & \alpha_4 \\ \alpha_5 & \alpha_6 \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \\ 0 & 0 \end{pmatrix}
$$
which is only true when $\forall \alpha \in \{\alpha_1, ..., \alpha_6\} (\alpha = 0)$. Because $(\alpha_1, \alpha_2, ..., \alpha_6) \in \mathbb{F}^6$ was arbitrary, the system is $e_{1}, e_{2}, ..., e_{6}$ linearly independent.
Thus, the system is a basis by Proposition 2.7.

**Problem 2.2:**
True or false:
a) Any set containing a zero vector is linearly dependent
b) A basis must contain 0;
c) subsets of linearly dependent sets are linearly dependent;
d) subsets of linearly independent sets are linearly independent;
e) If $\alpha_1v_1 + \alpha_2v_2 + ... + \alpha_nv_n = 0$ then all scalars $\alpha_k$ are zero;
**Solution:**
a)
True.
Suppose arbitrary system $v_0, v_1, v_2, ..., v_n \in V$ where $v_0$ is a zero vector. If we set $\forall k \in \{1, ..., n\} (\alpha_k = 0)$ and $\alpha_0 = 1$ then we get $\sum_{k = 0}^n \alpha_k v_k = 0$. Because $\alpha_0 \ne 0$, the system is linearly dependent.

b)
False.
Suppose we had a basis. Then it is linearly independent by definition. But by part a, the system must not contain a zero vector.

c)
False.
Suppose we had a linearly dependent set that was generating. Then by Proposition 2.8, there exists a subset of the linearly dependent set that is a basis which is then linearly independent by definition. Therefore, not all subsets of linearly dependent sets are also linearly dependent.

d)
True.
Suppose we had an arbitrary linearly independent set $v$ and arbitrary set $j \subseteq v$ where $j = \{j_1, ..., j_p\}$. Suppose j was linearly dependent. Then there is some $k \in \{1, 2, ..., p\}$ such that $j_k = \sum^p_{i = 1, i \ne k}\beta_ij_i$ by proposition 2.6. But $j \subseteq v$, so $j_1, ..., j_p \in v$. Then we still have $j_k = \sum^p_{i = 1, i \ne k}\beta_ij_i$ for the system v. Therefore, v would be linearly dependent, but this is a contradiction. Thus, j is linearly independent.

e)
False.
Let $v_1 = v_2 = ... = v_n = 0$ and $\alpha_1 = \alpha_2 = ... = \alpha_n = 1$. Then, $\alpha_1v_1 + \alpha_2v_2 + ... + \alpha_nv_n = 0$ but all scalars $\alpha_k$ are not zero.

**Problem 2.3:**
Recall, that a matrix is called symmetric if $A^T = A$. Write down a basis in the
space of symmetric $2 \times 2$ matrices (there are many possible answers). How many
elements are in the basis?
**Solution:**
Let the basis of ($e_{1}, e_{2}, e_{3}$) be defined as,
$$
\begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}, \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}
$$
which contains 3 elements. Pick arbitrary v in the space of symmetric $2 \times 2$ matrices. Then set $\alpha_1 = v_{11}, \alpha_2 = v_{22}, \alpha_3 = v_{12}$ and notice because $v_{12} = v_{21}$ by definition of symmetric matrices,
$$
\alpha_1 e_{1} + \alpha_2 e_{2} + \alpha_3e_{3} = \begin{pmatrix} v_{11} & v_{12} \\ v_{12} & v_{22} \end{pmatrix} = \begin{pmatrix} v_{11} & v_{12} \\ v_{21} & v_{22} \end{pmatrix} = v
$$
and so the system is generating. Now we show linear independence. Define arbitrary $(\alpha_1, \alpha_2, \alpha_3) \in \mathbb{F}^3$ and suppose $\sum_{k = 1}^3 \alpha_k e_k = 0$. It follows that,
$$
\sum_{k = 1}^3 \alpha_k e_k = \begin{pmatrix} \alpha_1 & \alpha_3 \\ \alpha_3 & \alpha_2 \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}
$$
which is only true when $\alpha_1 = \alpha_2 = \alpha_3 = 0$. Therefore, the system is linearly independent because $(\alpha_1, \alpha_2, \alpha_3) \in \mathbb{F}^3$ was arbitrary. Thus, the system is a basis by Proposition 2.7.

**Problem 2.4:**
Write down a basis for the space of
a) $3 \times 3$ symmetric matrices;
b) $n \times n$ symmetric matrices;
c) $n \times n$ anti-symmetric ($A^T = - A$) matrices;
**Solution:**
a)
Let the basis of ($e_{1}, e_{2}, e_{3}, ..., e_{6}$) be defined as,
$$
\begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 1 \\ 0 & 0 & 0 \\ 1 & 0 & 0 \end{pmatrix},
\begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix},
\begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 1 & 0 \end{pmatrix}
$$
Pick arbitrary v in the space of symmetric $3 \times 3$ matrices. Then set $\alpha_1 = v_{11}, \alpha_2 = v_{22}, \alpha_3 = v_{33}, \alpha_4 = v_{13}, \alpha_5 = v_{12}, \alpha_6 = v_{23}$ and notice because $v_{13} = v_{31}, v_{12} = v_{21}, v_{23} = v_{32}$ by definition of symmetric matrices,
$$
\alpha_1 e_{1} + \alpha_2 e_{2} + ... + \alpha_6e_6 = \begin{pmatrix} v_{11} & v_{12} & v_{13} \\ v_{12} & v_{22} & v_{23} \\ v_{13} & v_{23} & v_{33} \end{pmatrix} = \begin{pmatrix} v_{11} & v_{12} & v_{13} \\ v_{21} & v_{22} & v_{23} \\ v_{31} & v_{32} & v_{33} \end{pmatrix} = v
$$
and so the system is generating. Now we show linear independence. Define arbitrary $(\alpha_1, ..., \alpha_6) \in \mathbb{F}^6$ and suppose $\sum_{k = 1}^6 \alpha_k v_k = 0$. It follows that,
$$
\sum_{k = 1}^6 \alpha_k v_k = \begin{pmatrix} \alpha_1 & \alpha_5 & \alpha_4 \\ \alpha_5 & \alpha_2 & \alpha_6 \\ \alpha_4 & \alpha_6 & \alpha_3 \end{pmatrix} = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}
$$
which is only true when $\alpha_1 = ... = \alpha_6 = 0$. Therefore, because $(\alpha_1, ..., \alpha_6) \in \mathbb{F}^6$ was arbitrary, the system is linearly independent. Thus, the system $e_{1}, e_{2}, e_{3}, ..., e_{6}$ is a basis by Proposition 2.7.

b)
repetitive...

c)
repetitive...

**Problem 2.5:**
Let a system of vectors $v_1, v_2, ..., v_r$ be linearly independent but not generating. Show that it is possible to find a vector $v_{r+1}$ such that the system
$v_1, v_2, ..., v_r , v_{r+1}$ is linearly independent. Hint: Take for $v_{r+1}$ any vector that
cannot be represented as a linear combination $\sum^r_{k=1} \alpha_kv_k$ and show that the system $v_1, v_2, ..., v_r , v_{r+1}$ is linearly independent.
**Solution:**
Because $v_1, v_2, ..., v_r$ is not generating, we know there is some vector $v_{r + 1}$ such that $\forall (\alpha_1, ..., \alpha_r) \in \mathbb{F}^r (v_{r + 1} \ne \sum^r_{k = 1} \alpha_k v_k)$. Define arbitrary $(\alpha_1, ..., \alpha_{r + 1}) \in \mathbb{F}^{r + 1}$ and suppose $\sum_{k = 1}^{r + 1} \alpha_k v_k = 0$. We consider two cases. Case 1: $\alpha_{r + 1} \ne 0$. Then we have,
$$
\sum_{k = 1}^{r + 1} \alpha_k v_k = 0 \iff v_{r+1} = \frac{-1}{\alpha_{r+1}} \sum_{k = 1}^r \alpha_k v_k \iff v_{r + 1} = \sum_{k = 1}^r \beta_k v_k
$$
which is a contradiction and so this case is not possible. Case 2: $\alpha_{r + 1} = 0$. Then because the system $v_1, v_2, ..., v_r$ is linearly independent, $\sum_{k = 1}^{r} \alpha_k v_k = 0$ is true only when $\alpha_1 = ... = \alpha_r = 0$.  But $(\alpha_1, ..., \alpha_{r + 1}) \in \mathbb{F}^{r + 1}$ was arbitrary so the system $v_1, v_2, ..., v_r , v_{r+1}$ is linearly independent. Thus, it is possible to find a vector $v_{r+1}$ such that the system $v_1, v_2, ..., v_r , v_{r+1}$ is linearly independent.

**Problem 2.6:**
Is it possible that vectors $v_1, v_2, v_3$ are linearly dependent, but the vectors $w_1 = v_1 + v_2, w_2 = v_2 + v_3$ and $w_3 = v_3 + v_1$ are linearly independent?
**Solution:**
No.
Suppose the vectors $v_1, v_2, v_3$ are linearly dependent. Then there exists some $(a_1, a_2, a_3) \in \mathbb{F}^3$ such that $\sum_{k = 1}^3 a_k v_k = 0$ and $a_1 \ne 0 \lor a_2 \ne 0 \lor a_3 \ne 0$. Let $b_1 = \frac{a_1 + a_2 - a_3}{2}, b_2 = \frac{a_2 + a_3 - a_1}{2}, b_3 = \frac{a_1 + a_3 - a_2}{2}$. Notice,
$$
b_1 w_1 + b_2 w_2 + b_3 w_3 = (b_1 + b_3)v_1 + (b_1 + b_2)v_2 + (b_2 + b_3)v_3
$$
$$
= a_1v_1 + a_2v_2 + a_3v_3 = 0
$$
Since $(a_1, a_2, a_3) \ne (0, 0, 0)$, it follows that $(b_1, b_2, b_3) \ne (0, 0, 0)$ because $a_1 = b_1 + b_3, a_2 = b_1 + b_2, a_3 = b_2 + b_3$. Thus, the vectors $w_1 = v_1 + v_2, w_2 = v_2 + v_3$ and $w_3 = v_3 + v_1$ are linearly dependent.

### References
- *Linear Algebra Done Wrong* — Chapter 1, Pages 6–11


## 0.2 Linear Transformations. Matrix-Vector Multiplication
---
### Key Concepts
- **Linear Transformation Basis**:
  - A linear transformation is completely defined by its values on a generating set (in particular by its values on a basis).
### Definitions
- **Transformation**
  - $\forall x \in X (T(x) \in Y)$ notated as $T: X \to Y$.
  - The set X is the domain of T.
  - The set Y the the codomain of T.
  - Matrix represented as $[T]$.
- **Linear Transformation**
  - For transformation $T: V \to W$ where V and W are vector spaces over field $\mathbb{F}$
  - (1) $\forall u,v \in V T(u + v) = T(u) + T(v)$.
  - (2) $\forall v \in V \forall \alpha \in \mathbb{F} T(\alpha v) = \alpha T(v)$.
  - (1 & 2) $\forall u,v \in V \forall \alpha, \beta \in \mathbb{F} (T(\alpha u + \beta v) = \alpha T(u) + \beta T(v))$.
  - $T: \mathbb{R} \to \mathbb{R}$, $T(x) = T(1x) = xT(1) = xa = ax$.
  - $T: \mathbb{F}^n \to \mathbb{F}^m$, $T(x) = T(\sum_{k = 1}^n x_k e_k) = \sum_{k = 1}^nT(x_k e_k) = \sum_{k = 1}^n x_k T(e_k) = \sum_{k = 1}^n x_k a_k = Ax$.
- **Column By Coordinate Rule**
  - Multiply each column of the matrix by the corresponding coordinate of the vector.
- **Row By Column Rule**
  - If $Ax = y$, then $y_k = \sum^n_{j = 1}a_{k, j}x_j, k = 1, 2, ..., m$.

### Examples
**Example Title**
**Problem 3.1:**
Multiply:
a)
$$
\begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix} \begin{pmatrix} 1 \\ 3 \\ 2 \end{pmatrix}
$$

b)
$$
\begin{pmatrix} 1 & 2 \\ 0 & 1 \\ 2 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 3 \end{pmatrix}
$$

c)
$$
\begin{pmatrix} 1 & 2 & 0 & 0 \\ 0 & 1 & 2 & 0 \\ 0 & 0 & 1 & 2 \\ 0 & 0 & 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \\ 3 \\ 4 \end{pmatrix}
$$

d)
$$
\begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 2 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \\ 3 \\ 4 \end{pmatrix}
$$
**Solution:**
a)
$$
\begin{pmatrix} 13 \\ 31 \end{pmatrix}
$$

b)
$$
\begin{pmatrix} 7 \\ 3 \\ 2 \end{pmatrix}
$$

c)
$$
\begin{pmatrix} 5 \\ 8 \\ 11 \\ 4 \end{pmatrix}
$$

d)
Not possible to multiply $M_{4 \times 3}$ and $\mathbb{R}^4$.


**Problem 3.2:**
Let a linear transformation in $\mathbb{R}^2$ be the reflection in the line $x_1 = x_2$. Find
its matrix.
**Solution:**
Notice the basis of $\mathbb{R}^2$ is the system $e_1$ and $e_2$.
$$
T(e_1) = e_2, T(e_2) = e_1
$$
and so $[T] = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$.

**Problem 3.3:**
For each linear transformation below find it matrix
a) $T : \mathbb{R^2} \to \mathbb{R}^3$ defined by $T(x, y)^T = (x + 2y, 2x - 5y, 7y)^T$ ;
b) $T : \mathbb{R}^4 \to \mathbb{R}^3$ defined by $T(x_1, x_2, x_3, x_4)^T = (x_1 +x_2 +x_3 +x_4, x_2 - x_4, x_1 + 3x_2 + 6x_4)^T$ ;
c) $T : \mathbb{P}_n \to \mathbb{P}_n$, $Tf(t) = f'(t)$ (find the matrix with respect to the standard basis $1, t, t^2, ..., t^n$);
d) $T : \mathbb{P}_n \to \mathbb{P}_n$, $Tf(t) = 2f(t) + 3f'(t) - 4f''(t)$ (again with respect to the standard basis $1, t, t^2, ..., t^n$).
**Solution:**
a)
$\mathbb{R}^2$ basis is $e_1$ and $e_2$.
$$
T(e_1) = (1, 2, 0)^T, T(e_2) = (2, -5, 7)^T
$$
and so $[T] = \begin{pmatrix} 1 & 2 \\ 2 & -5 \\ 0 & 7 \end{pmatrix}$.

b)
$\mathbb{R}^4$ basis is $e_1, e_2, e_3, e_4$.
$$
T(e_1) = (1, 0, 1)^T, T(e_2) = (1, 1, 3)^T, T(e_3) = (1, 0, 0)^T, T(e_4) = (1, -1, 6)^T
$$
and so $[T] = \begin{pmatrix} 1 & 1 & 1 & 1 \\ 0 & 1 & 0 & -1 \\ 1 & 3 & 0 & 6 \end{pmatrix}$.

c)
$$
\forall k \in \{0, 1, 2, ..., n\} (T(t^k) = k t^{k - 1})
$$
and so,
$$
[T] = \begin{pmatrix} 0 & 1 & 0 & 0 & ... & 0 \\ 0 & 0 & 2 & 0 & ... & 0 \\ 0 & 0 & 0 & 3 & ... & 0 \\ ... & ... & ... & ... & ... & ... \\ 0 & 0 & 0 & 0 & ... & n \end{pmatrix}
$$

d)
$$
\forall k \in \{0, 1, 2, ..., n\} (T(t^k) = 2t^k + 3kt^{k - 1} - 4(k^2 - k)t^{k - 2})
$$
and so,
$$
[T] = \begin{pmatrix} 2 & 3 & -8 & ... & 0 \\ 0 & 2 & 6 & ... & 0 \\ 0 & 0 & 2 & ... & 0 \\ ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & 2 \end{pmatrix}
$$


**Problem 3.4:**
Find $3 \times 3$ matrices representing the transformations of $\mathbb{R}^3$ which:
a) project every vector onto x-y plane;
b) reflect every vector through x-y plane;
c) rotate the x-y plane through $30^{\circ}$, leaving z-axis alone.
**Solution:**
Notice the basis of $\mathbb{R}^3$ is the system $e_1, e_2, e_3$.
a)
$$
T(e_1) = e_1, T(e_2) = e_2, T(e_3) = 0
$$
and so $[T] = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{pmatrix}$.

b)
$$
T(e_1) = e_1, T(e_2) = e_2, T(e_3) = -1e_3
$$
and so $[T] = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & -1 \end{pmatrix}$.

c)
$$
T(e_1) = \begin{pmatrix} cos(30) \\ sin(30) \\ 0 \end{pmatrix}, T(e_2) = \begin{pmatrix} -sin(30) \\ cos(30) \\ 0 \end{pmatrix}, T(e_3) = e_3
$$
and so $[T] = \begin{pmatrix} cos(30) & -sin(30) & 0 \\ sin(30) & cos(30) & 0 \\ 0 & 0 & 1 \end{pmatrix}$.

**Problem 3.5:**
Let A be a linear transformation. If z is the center of the straight interval $[x, y]$, show that $Az$ is the center of the interval $[Ax, Ay]$. Hint: What does it mean that z is the center of the interval $[x, y]$?
**Solution:**
Suppose z is the center of the straight interval $[x, y]$. It follows that $z = \frac{x + y}{2}$. Then we get $A(z) = A(\frac{x + y}{2}) = 0.5A(x + y) = 0.5(A(x) + A(y))$. But then $A(z) = \frac{A(x) + A(y)}{2}$ and so $Az$ is the center of the interval $[Ax, Ay]$. Thus, if z is the center of the straight interval $[x, y]$, show that $Az$ is the center of the interval $[Ax, Ay]$.

**Problem 3.6:**
The set $\mathbb{C}$ of complex numbers can be canonically identified with the space $\mathbb{R}^2$ by treating each $z = x + iy \in \mathbb{C}$ as a column $(x, y)^T \in \mathbb{R}^2$.
a) Treating $\mathbb{C}$ as a complex vector space, show that the multiplication by $\alpha = a + ib \in \mathbb{C}$ is a linear transformation in $\mathbb{C}$. What is its matrix?
b) Treating $\mathbb{C}$ as the real vector space $\mathbb{R}^2$ show that the multiplication by $\alpha = a + ib$ defines a linear transformation there. What is its matrix?
c) Define $T(x + iy) = 2x - y + i(x - 3y)$. Show that this transformation is not a linear transformation in the complex vectors space $\mathbb{C}$, but if we treat $\mathbb{C}$ as the real vector space $\mathbb{R}^2$ then it is a linear transformation there (i.e. that $T$ is a real linear but not a complex linear transformation). Find the matrix of the real liner transformation $T$.
**Solution:**
a)
Define arbitrary $u, v \in \mathbb{C}$ and $\beta, \lambda \in \mathbb{C}$. Then $T(\beta u + \lambda v) = \alpha(\beta u + \lambda v) = \alpha \beta u + \alpha \lambda v = \beta \alpha u + \lambda \alpha v = \beta T(u) + \lambda T(v)$ and so the transformation is linear. With basis $1$, we see that $T(1) = \alpha = a + bi$ and so the matrix is $a + bi$.

b)
Define arbitrary $u, v \in \mathbb{R^2}$ and $\beta, \lambda \in \mathbb{R}$. Then $T(\beta u + \lambda v) = \alpha(\beta u + \lambda v) = \alpha \beta u + \alpha \lambda v = \beta \alpha u + \lambda \alpha v = \beta T(u) + \lambda T(v)$ and so the transformation is linear. With basis $e_1$ and $e_2$, we see that $T(e_1) = \begin{pmatrix} a \\ b \end{pmatrix}$ and $T(e_2) = \begin{pmatrix} -b \\ a \end{pmatrix}$ and so the matrix is $\begin{pmatrix} a & -b \\ b & a \end{pmatrix}$.

c)
Define $1 + 2i \in \mathbb{C}$. Notice, $(1+ 2i) T(1 + 2i) = (1 + 2i)(-5i) = (10 - 5i)$ but $T((1 + 2i)(1 + 2i)) = T(-3 + 4i) = -10 -15i$ and so this is not a linear transformation.
Now define arbitrary $u, v \in \mathbb{R^2}$ and arbitrary $a \in \mathbb{R}$. Then $T(au) = \begin{pmatrix} 2au_1 - au_2 \\ au_1 - 3au_2 \end{pmatrix} = a T(u)$ and $T(u + v) = \begin{pmatrix} 2(u_1 + v_1) - (u_2 + v_2) \\ (u_1 + v_1) - 3(u_2 + v_2) \end{pmatrix} = \begin{pmatrix} 2(u_1) - (u_2) \\ (u_1) - 3(u_2) \end{pmatrix} + \begin{pmatrix} 2(v_1) - (v_2) \\ (v_1) - 3(v_2) \end{pmatrix} = T(u) + T(v)$ meaning this is a linear transformation. The matrix is then given by the basis $e_1$ and $e_2$ such that,
$$
T(e_1) = \begin{pmatrix} 2 \\ 1 \end{pmatrix}, T(e_2) = \begin{pmatrix} -1 \\ -3 \end{pmatrix}
$$
and so $[T] = \begin{pmatrix} 2 & -1 \\ 1 & -3 \end{pmatrix}$.

**Problem 3.7:**
Show that any linear transformation in $\mathbb{C}$ (treated as a complex vector space) is a multiplication by $\alpha \in C$.
**Solution:**
Let x be arbitrary vector in $\mathbb{C}$. It follows that, $T(x) = T(x \times 1) = xT(1)$. Notice $T(1) \in \mathbb{C}$ and so any linear transformation in $\mathbb{C}$ (treated as a complex vector space) is a multiplication by $\alpha \in C$.

### References
- *Book Title* — Chapter X, Pages 12–17


## 0.3 Linear Transformations As A Vector Space
---
### Key Concepts
- **Linear Transformation Vector Space**:
  - $L(V, W)$ is a vector space of linear transformations mapping V to W.
  - Addition defined as: $(T_1 + T_2)v = T_1v + T_2v$.
  - Scalar Multiplication: $(\alpha T)v = \alpha (Tv)$.
  - Satisfies Vector Space properties.

### References
- *Book Title* — Chapter 1, Pages Y–19


## 0.4 Composition Of Linear Transformations And Matrix Multiplication
---
### Key Concepts
- **Matrix Multiplication Properties**:
  - Associativity.
  - Distributivity.
  - Scalar multiple commutativity, not for matrices though.
### Definitions
- **Column By Vector Rule**
  - Multiply each column of the matrix by the corresponding vector of the other matrix.
- **Row By Column Rule**
  - $(AB)_{j, k} = \sum_l a_{j, l}b_{l, k}$.
  - Defined iff A is $m \times n$ and B is $n \times r$.
- **Linear Transformation Composition**
  - $T_1 : \mathbb{F}^n \to \mathbb{F}^m, T_2 : \mathbb{F}^r \to \mathbb{F}^n$. Define $T = T_1 \circ T_2$ as $\forall x \in \mathbb{F}^r T(x) = T_1(T_2(x))$.
- **Transpose**
  - $(A^T)_{j, k} = (A)_{k, j}$.
  - $(AB)^T = B^TA^T$.
- **Trace**
  - $\text{trace}(A) = \sum_{k =1}^n a_{k,k}$.

### Theorems & Proofs
**Theorem 5.1**
Let A and B be matrices of size $m \times n$ and $n \times m$. Then $\text{trace}(AB) = \text{trace}(BA)$.

### Examples
**Example Title**
**Problem 5.3:**
Multiply two rotation matrices $T_\alpha$ and $T_\beta$ (it is a rare case when the multiplication is commutative, so the order is not essential). Deduce formulas for $sin(\alpha + \beta)$ and $cos(\alpha + \beta)$ from here.
**Solution:**
$$
T_{\alpha + \beta} := T_\alpha \circ T_\beta
$$
But $T_{\alpha + \beta}$ is just the transformation that rotates by $\alpha + \beta$. Therefore,
$$
[T_{\alpha + \beta}] = \begin{pmatrix} cos(\alpha + \beta) & -sin(\alpha + \beta) \\ sin(\alpha + \beta) & cos(\alpha + \beta) \end{pmatrix} = [T_\alpha] [T_\beta] = \begin{pmatrix} cos(\alpha) & -sin(\alpha) \\ sin(\alpha) & cos(\alpha) \end{pmatrix} \begin{pmatrix} cos(\beta) & -sin(\beta) \\ sin(\beta) & cos(\beta) \end{pmatrix}
$$
$$
= \begin{pmatrix} cos(\alpha)cos(\beta) -sin(\alpha)sin(\beta) & -cos(\alpha)sin(\beta) + cos(\beta)sin(\alpha) \\ sin(\alpha)cos(\beta) + cos(\alpha)sin(\beta) & -sin(\alpha)sin(\beta) + cos(\alpha)cos(\beta) \end{pmatrix}
$$
and so we see that $sin(\alpha + \beta) = sin(\alpha)cos(\beta) + cos(\alpha)sin(\beta)$ and $cos(\alpha + \beta) = cos(\alpha)cos(\beta) -sin(\alpha)sin(\beta)$. **Q.E.D**

**Problem 5.4:**
Find the matrix of the orthogonal projection in $\mathbb{R}^2$ onto the line $x_1 = -2x_2$. Hint: What is the matrix of the projection onto the coordinate axis $x_1$?
**Solution:**
$$
T_{r} := \begin{pmatrix} cos(tan^{-1}(-0.5)) & -sin(tan^{-1}(-0.5)) \\ sin(tan^{-1}(-0.5)) & cos(tan^{-1}(-0.5)) \end{pmatrix}, T_{x_1} := \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}
$$ Notice $T_{x_1}$ is the projection onto the $x_1$ axis and $T_{r}$ is the rotation of the line. Therefore, the matrix of the orthogonal projection in $\mathbb{R}^2$ onto the line $x_1 = -2x_2$ must be $T_{r}^TT_{x_1}T_r$,
$$
\begin{pmatrix} cos(tan^{-1}(-0.5))^2 & -sin(tan^{-1}(-0.5))cos(tan^{-1}(-0.5)) \\ -sin(tan^{-1}(-0.5))cos(tan^{-1}(-0.5)) & sin(tan^{-1}(-0.5))^2 \end{pmatrix}
$$
**Q.E.D**

**Problem 5.6:**
Prove Theorem 5.1, i.e. prove that $trace(AB) = trace(BA)$.
**Solution:**
By definition of AB and BA both being defined, A and B are square matrices of dimension $m \times m$ for some $m \in \mathbb{N}$. It follows that,
$$
trace(AB) = \sum_{k=1}^m(AB)_{k, k} = \sum_{k=1}^m\sum_{j=1}^m a_{k, j}b_{j, k} = \sum_{j=1}^m\sum_{k=1}^m b_{j, k}a_{k, j} = \sum_{j=1}^m(BA)_{j,j} = trace(BA)
$$
and so $trace(AB) = trace(BA)$. **Q.E.D**

**Problem 5.7:**
Construct a non-zero matrix A such that $A^2 = 0$.
**Solution:**
$$
A := \begin{pmatrix} 1 & -1 \\ 1 & -1 \end{pmatrix}
$$
$$
A^2 = \begin{pmatrix} 1 & -1 \\ 1 & -1 \end{pmatrix}\begin{pmatrix} 1 & -1 \\ 1 & -1 \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = 0
$$
**Q.E.D**

### References
- *Book Title* — Chapter X, Pages Y–Z


## 0.5 Invertible Transformations And Matrices. Isomorphisms
---
### Definitions
- **Identity Transformation**
  - $Ix = x, \forall x$.
  - Not unique.
  - $AI = A$ and $IA = A$ for any linear transformation A.
- **Left Invertible**
  - $A: V \to W$ is left invertible if $\exists B: W \to V (BA = I)$.
  - Matrix is left invertible if the transformation is.
- **Right Invertible**
  - $A: V \to W$ is left invertible if $\exists B: W \to V (AB = I)$.
  - Matrix is right invertible if the transformation is.
- **Invertible\Isomorphism**
  - Left and right invertible.
  - The domain and codomain are called isomorphic.
  - Matrix is invertible if the transformation is.
  - Must be a square matrix.
  - If A is invertible, then its inverse is invertible and is A.

### Theorems & Proofs
**Theorem 6.1**
If a linear transformation $A: V \to W$ is invertible, then its left and right inverses B and C are unique and coincide.

Let $BA = I$ and $AC = I$. Then $BAC = B(AC) = BI = B$. On the other hand, $BAC = (BA)C = IC = C$. Therefore, $B = C$. Suppose for some transformation $B_1$ we have $B_1A = I$. Repeating the reasoning above with $B_1$ instead of $B$ we get $B_1 = C$. Therefore, the left inverse B is unique. The uniqueness of C is proved similarly. **Q.E.D**

**Corollary**
A transformation $A: V \to W$ is invertible iff $\exists ! A^{-1}: W \to V (A^{-1}A = I_V \land AA^{-1} = I_W)$. $A^{-1}$ is called the inverse of A.

**Theorem 6.3**
If linear transformations A and B are invertible, then the product $AB$ is invertible if defined and $(AB)^{-1} = B^{-1}A^{-1}$.

$$
(AB)(B^{-1}A^{-1}) = I, (B^{-1}A^{-1})(AB) = I
$$
**Q.E.D**

**Theorem 6.5**
If a matrix A is invertible, then $A^T$ is also invertible and $(A^T)^{-1} = (A^{-1})^T$.

$$
(A^{-1})^TA^T = (AA^{-1})^T = I^T = I
$$
$$
A^T(A^{-1})^T = (A^{-1}A)^T = I^T = I
$$
**Q.E.D**

**Theorem 6.6**
Let $A : V \to W$ be an isomorphism, then let $v_1, v_2, ..., v_n$ be a basis in V. Then the system $Av_1, Av_2, ..., Av_n$ is a basis in W.

**Theorem 6.7**
Let $A : V \to W$ a linear map, and let $v_1, v_2, ..., v_n$ and $w_1, w_2, ..., w_n$ be bases in V and W. If $Av_k = w_k, k = 1, 2, ..., n$, then A is an isomorphism.

Define $A^{-1}$ by $A^{-1}w_k = v_k, k = 1, 2, ..., n$.

**Theorem 6.8**
Let $A : V \to W$ a linear transformation. and Then A is invertible iff for any right side $b \in Y$, the equation $Ax = b$ has a unique solution $x \in X$.

Suppose A is invertible. Then $x = A^{-1}b$ solves the equation $Ax = b$. Suppose for some other vector $v_1 \in X$, $Ax_1 = b$. Multiplying by $A^{-1}$ from the left gives $A^{-1}Ax_1 = A^{-1}b$. Therefore, $x_1 = x$. Now suppose the equation $Ax = b$ has unique solution $x$ for any $b \in Y$. Call the solution $B(b)$ and define a transformation $B : Y \to X$. It is easy to show that B is a linear transformation if we define $x_k := B(y_k)$. Take $x \in X$ and let $y = Ax$, so by definition of B we have $x = By$. Then for all $x \in X$, $BAx = By = x$. So $BA = I$. For arbitrary $y \in Y$, let $x = By$, so $y = Ax$. Then for all y, $ABy = Ax = y$ and so $AB = I$.
**Q.E.D**

**Corollary 6.9**
An $m \times n$ matrix is invertible iff its columns form a basis in $\mathbb{F}^m$.

### Examples
**Example Title**
**Problem 6.2:**
Find all right inverses to the $1 \times 2$ matrix (row) $A = (1, 1)$. Conclude from here that the row A is not left invertible.
**Solution:**
All right inverses are defined as $\begin{pmatrix} a \\ b \end{pmatrix}$ where $a + b = 1$ because $A\begin{pmatrix} a \\ b \end{pmatrix} = (a + b) = (1)$. We can see there are infinitely many such solutions. But then by theorem 6.1, because the right inverse is not unique, we see that A is not invertible. We know A is right invertible so it must not be left invertible. **Q.E.D**

**Problem 6.5:**
Find two matrices A and B that AB is invertible, but A and B are not. Hint:
square matrices A and B would not work. Remark: It is easy to construct such
A and B in the case when AB is a $1 \times 1$ matrix (a scalar). But can you get $2 \times 2$
matrix AB? $3 \times 3$? $n \times n$?
**Solution:**
Define the $n \times m$ matrix A and the $m \times n$ matrix B where $m > n$:
$$
A := \begin{pmatrix} 1 & 0 & 0 & ... & 0 & 0 & ... \\ 0 & 1 & 0 & ... & 0 & 0 & ... \\ 0 & 0 & 1 & ... & 0 & 0 & ... \\ ... & ... & ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & 1 & 0 & ... \end{pmatrix}, B := \begin{pmatrix} 1 & 0 & 0 & ... & 0 \\ 0 & 1 & 0 & ... & 0 \\ 0 & 0 & 1 & ... & 0 \\ ... & ... & ... & ... & 1 \\ 0 & 0 & 0 & ... & 0 \\ ... & ... & ... & ... & ... \end{pmatrix}
$$
Clearly, A and B are not invertible by Corollary 6.9 because A's columns are not linearly independent (0 vectors) in $\mathbb{F}^n$ and B is not generating (0 rows for all vectors) for $\mathbb{F}^m$. However, $AB = I$ which is invertible by definition (inverse is I). **Q.E.D**


**Problem 6.7:**
Let A and AB be invertible (assuming that the product AB is well defined). Prove that B is invertible.
**Solution:**
$$
AB(AB)^{-1} = I \implies A^{-1}AB(AB)^{-1} = A^{-1} \implies B(AB)^{-1} = A^{-1} \implies B(AB)^{-1}A = I
$$
and so B is right invertible.
$$
AB = AB \implies (AB)^{-1}AB = (AB)^{-1}AB \implies (AB)^{-1}AB = I
$$
and so B is left invertible. Therefore, B is invertible. **Q.E.D**

**Problem 6.8:**
Let A be $n \times n$ matrix. Prove that if $A^2 = 0$ then A is not invertible.
**Solution:**
Suppose $A^2 = 0$. Suppose A were invertible. Then there is $n \times n$ matrix B such that $AB = I$ and $BA = I$ by theorem 6.1. However, multiply the left sides both by A gives $AAB = AI$ which is equivalent to $0 = A$. But then $AB = 0$ always which is a contradiction, therefore A is not invertible. **Q.E.D**

### References
- *Book Title* — Chapter X, Pages Y–Z


## 0.6 Subspaces
---
### Definitions
- **Subspace**
  - Non-empty subset $V_0 \subset V$ where $\forall v \in V_0 \forall a \in \mathbb{F} av \in V_0$ and $\forall v, u \in V_0 (u + v \in V_0)$.
  - Inherits other vector space properties from V.
- **Null Space\Kernel**
  - Denoted Null A or Ker A for linear transformation $A : V \to W$ and consists of all vectors $v \in V$ such that $Av = 0$.
- **Range**
  - Denoted Ran A or Col A for linear transformation $A : V \to W$ for the set of all vectors $w \in W$ which can be represented as $w = Av$ for some $v \in V$.
- **Linear Span**
  - The span of system $v_1, v_2, ..., v_r \in V$ denoted $\{v_1, v_2, ..., v_r\}$ is the collection of all vectors $v \in V$ that can be represented as a linear combination of the system.

### Examples
**Example Title**
**Problem 7.2:**
Let V be a vector space. For $X, Y \subset V$ the sum $X + Y$ is the collection of all vectors v which can be represented as $v = x + y, x \in X, y \in Y$. If X and Y are subspaces of V, then $X + Y$ is also a subspace.
**Solution:**
Suppose X and Y are subspaces of V. Pick arbitrary $z_1, z_2 \in X+Y$ such that $z_1 := x_1 + y_1$ and $z_2 := x_2 + y_2$ for $x_1,x_2 \in X$ and $y_1,y_2 \in Y$. But $z_1 + z_2 = (x_1 + y_1) + (x_2 + y_2) = (x_1 + x_2) + (y_1 + y_2)$ by additive commutivity and associativity. Because X is a subspace of V, we have $x_1 + x_2 \in X$. Similar reasoning follows for $y_1 + y_2 \in Y$. Therefore, $z_1 + z_2 \in X + Y$. Consider $\alpha z_1 = \alpha(x_1 + y_1)$ for $\alpha \in \mathbb{F}$. It follows from vector space properties that $\alpha(x_1 + y_1) = \alpha x_1 +\alpha y_1$ where $\alpha x_1 \in X$ and $\alpha y_1 \in Y$ by definition. Take arbitrary $x \in X$ and $y \in Y$. By definition, $x, y \in V$ and so $x + y \in V$. But x and y were arbitrary and so $X + Y \subseteq V$. Thus, $X + Y$ is a subspace. **Q.E.D**

**Problem 7.3:**
Let X be a subspace of a vector space V, and let $v \in V$, $v \not \in X$. If $x \in X$ then $x + v \not \in X$.
**Solution:**
Suppose arbitrary $x \in X$. Then consider $x + v \in X$. It follows by definition of closure that $v \in X$ which is a contradiction ($x + v + (-x) \in X$). Thus, $x + v \not \in X$. **Q.E.D**

### References
- *Book Title* — Chapter X, Pages Y–31
