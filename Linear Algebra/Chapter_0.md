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
a)
Define arbitrary $f: [0, 1] \to Y$ and $g: [0, 1] \to X$ for some X and Y.

b)
Define arbitrary $f: [0, 1] \to Y$ and $g: [0, 1] \to X$ for some X and Y.

c)
No. By Problem 1.3 part d, addition is not closed in $\mathbb{P}^n$.

d)


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
which suggests f has degree $m + n$ and g has degree $m + n$. However, this is a contradiction because f and g have degree at most n which is less than $m + n$. Therefore, If f and g are polynomials of degree at most n, then $f + g$ is also a polynomial of degree at most n.

**Problem 1.4:**
Prove that a zero vector 0 of a vector space V is unique.
**Solution:**
Existence - By axiom 3 of vector spaces, we can pick some $v_0 = 0$ where $v_0 \in V$.
Uniqueness - Define arbitrary $v_p \in V$ and suppose $v_p = 0$. But $v_0 = 0$ so $v_p = v_0$.
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
Uniqueness - Define arbitrary $t \in V$ and suppose $v + t = 0$. Since, $v + w = 0$, we get $v + t = v + w$. By subtracting v, we see that $t = w$.
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
Define ($e_{11}, e_{12}, ..., e_{32}$ in order),
$$
\begin{pmatrix} 1 & 0 \\ 0 & 0 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 1 \\ 0 & 0 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 1 & 0 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 0 & 1 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 0 & 0 \\ 1 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 0 & 0 \\ 0 & 1 \end{pmatrix}
$$
Pick arbitrary $v \in M_{3 \times 2}$. Then set $\alpha_1 = v_{11}, \alpha_2 = v_{12}, ..., \alpha_6 = v_{32}$ and notice,
$$
\alpha_1 e_{11} + \alpha_2 e_{12} + ... + \alpha_6 e_{32} = \begin{pmatrix} v_{11} & v_{12} \\ v_{21} & v_{22} \\ v_{31} & v_{32} \end{pmatrix} = v
$$
and so the system is generating. Now we show linear independence.
Existence - As before, we set $\alpha_1 = v_{11}, \alpha_2 = v_{12}, ..., \alpha_6 = v_{32}$ for $v = 0$ getting $\begin{pmatrix} 0 & 0 \\ 0 & 0 \\ 0 & 0 \end{pmatrix} = 0$.
Uniqueness - Suppose for arbitrary $\beta_1, \beta_2, ..., \beta_6$ we had $\beta_1 e_{11} + \beta_2 e_{12} + ... + \beta_6 e_{32} = 0$. But then we have $\beta_1 e_{11} + \beta_2 e_{12} + ... + \beta_6 e_{32} = \alpha_1 e_{11} + \alpha_2 e_{12} + ... + \alpha_6 e_{32}$ which can be represented as $(\beta_1 - \alpha_1)e_{11} + (\beta_2 - \alpha_2)e_{12} + ... + (\beta_6 - \alpha_6)e_{32} = 0$. Then,
$$
\begin{pmatrix} \beta_1 - \alpha_1 & \beta_2 - \alpha_2 \\ \beta_3 - \alpha_3 & \beta_4 - \alpha_4 \\ \beta_5 - \alpha_5 & \beta_6 - \alpha_6 \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \\ 0 & 0 \end{pmatrix}
$$
which is only true when $\forall k \in \{1, 2, 3, 4, 5, 6\} (\beta_k = \alpha_k)$. Therefore, the system is linearly independent.
Thus, the system is a basis by Proposition 2.7.

**Problem 2.2:**
rue or false:
a) Any set containing a zero vector is linearly dependent
b) A basis must contain 0;
c) subsets of linearly dependent sets are linearly dependent;
d) subsets of linearly independent sets are linearly independent;
e) If $\alpha_1v_1 + \alpha_2v_2 + ... + \alpha_nv_n = 0$ then all scalars $\alpha_k$ are zero;
**Solution:**
a)
True.
Suppose we an arbitrary system $0, v_1, v_2, ..., v_n \in V$. If we set $\forall k \in \{2, ..., n + 1\} (\alpha_k = 0)$ and $\alpha_1 = 1$ then we get $\alpha_1 0 + \alpha_2 v_1 + ... + \alpha_{n + 1} v_n = (1) 0 + (0) v_1 + ... + (0) v_n = 0$ and so the system is linearly dependent.

b)
False.
Suppose we had a basis. Then it is linearly independent by definition. But by part a, the system must not contain a zero vector.

c)
False.
Suppose we had a linearly dependent set that was generating. Then by Proposition 2.8, a subset is a basis which is then linearly independent by definition. Therefore, not all subsets of linearly dependent sets are also linearly dependent.

d)
True.


### References
- *Book Title* — Chapter X, Pages Y–Z