# Chapter 2: Determinants
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## 2.0 Introduction
---
### Key Concepts
- **Notation**:
  - Determinant of system $v_1, v_2, ..., v_n$ denoted $D(v_1, v_2, ..., v_n)$.
  - Determinant of matrix A made of a system is $det A = D(v_1, v_2, ..., v_n)$.
  - $det A = \begin{vmatrix} a_{1,1} & a_{1, 2} & ... & a_{1, n} \\ a_{2, 1} & a_{2, 2} & ... & a_{2, n} \\ ... & ... & ... & ... \\ a_{n, 1} & a_{n, 2} & ... & a_{n, n} \end{vmatrix}$.

### References
- *Book Title* — Chapter 3, Pages Y–76


## 2.1 What Properties Determinant Should Have
---
### Key Concepts
- **Linearity**:
  - We desire $D(v_1, v_2, ..., \alpha v_k, ..., v_n) = \alpha D(v_1, v_2, ..., v_k, ..., v_n)$.
  - We also desire $D(v_1, ..., u_k + v_k, ..., v_n) = D(v_1, ..., u_k, ..., v_n) + D(v_1, ..., v_k, ..., v_n)$.
- **Column Replacement**:
  - We want $D(v_1, ..., v_j + \alpha v_k, ..., v_k, ..., v_n) = D(v_1, ..., v_j, ..., v_k, ..., v_n)$.
- **Antisymmetry**:
  - Deducible from column replacement $D(v_1, ..., v_k, ..., v_j, ..., v_n) = -D(v_1, ..., v_j, ..., v_k, ..., v_n)$.
- **Normalization**:
  - $det(I) = D(e_1, e_2, ..., e_n) = 1$.

### References
- *Book Title* — Chapter X, Pages Y–78


## 2.2 Constructing The Determinant
---
### Definitions
- **Determinant**
  - Linearity.
  - Antisymmetry.
  - Normalization.

### Theorems & Proofs
**Properties 3.1**
For a square matrix A the following statements holds:
1)If A has a zero column, then $det A = 0$.
2)If A has two equal columns, then $det A = 0$.
3)If one column of A is a multiple of another, then $det A = 0$.
4)If columns of A are linearly dependent, then $det A = 0$.

**Proposition 3.2**
The determinant does not change if we add to a column a linear combination of the other columns.

**Statement 1**
$det(diag\{a_1, a_2, ..., a_ n\}) = a_1 a_2 ... a_n$.

**Statement 2**
If A is triangular, $det A = a_{1,1}a_{2, 2}...a_{n,n}$.

**Proposition 3.3**
$det A = 0$ iff A is not invertible. $det A \ne 0$ iff A is invertible.

**Theorem 3.4**
$det A = det (A^T)$ for square matrix A.

**Theorem 3.5**
$det(AB) = det(A)det(B)$ for square matrices of same size A and B.

**Lemma 3.6**
$det(AE) = det(A)det(E)$ for square matrix A and elementary matrix E of same size.

**Corollary 3.7**
For any matrix A and any sequence of elementary matrices $E_1, E_2, ..., E_N$ (all $n \times n$),
$$
det(AE_1E_2...E_N) = det(A)det(E_1)det(E_2)...det(E_N)
$$

**Lemma 3.8**
Any invertible matrix is a product of elementary matrices.

**Statement 3**
If A is a $n \times n$ matrix, then $det(aA) = a^ndet(A)$.

### References
- *Book Title* — Chapter X, Pages Y–86


## 2.3 Formal definition. Existence and uniqueness of the determinant.
---
### Key Concepts
- **Determinant**:
  - $D(v_1, v_2, ..., v_n) = \sum_{j = 1}^n a_{j,1} D(e_j, v_2, ..., v_n)$.
  - $D(v_1, v_2, ..., v_n) = \sum_{j_1 = 1}^n\sum_{j_2 = 1}^n...\sum_{j_n = 1}^n a_{j_1,1}a_{j_2,2}...a_{j_n,n} D(e_{j_1}, e_{j_2}, ..., e_{j_n})$.
  - $D(v_1, v_2, ..., v_n) = \sum_{\sigma \in Perm(n)}a_{\sigma(1),1}a_{\sigma(2),2}...a_{\sigma(n),n}D(e_{\sigma(1)}, e_{\sigma(2)}, ..., e_{\sigma(n)})$.
  - $D(v_1, v_2, ..., v_n) = \sum_{\sigma \in Perm(n)}a_{\sigma(1),1}a_{\sigma(2),2}...a_{\sigma(n),n} sign(\sigma)$

### References
- *Book Title* — Chapter X, Pages Y–89


## 2.4 Cofactor Expansion
---
### Definitions
- **Cofactors**
  - The numbers $C_{j, k} = (-1)^{j+k}det(A_{j,k})$ in theorem 5.1.
- **Cofactor Matrix**
  - $C = \{C_{j,k}\}_{j,k=1}^n$ whose entries are cofactors of given matrix.

### Theorems & Proofs
**Theorem 5.1**
Let A be an $n \times n$ matrix and let $A_{j,k}$ denote the $(n - 1) \times (n - 1)$ matrix obtained from A by crossing out row number j and column number k. For each j, $1 \le j \le n$, determinant of A can be expanded in the row number j as $det(A) = \sum_{k=1}^n a_{j,k}(-1)^{j+k}det(A_{j,k})$. Similarly, for each k, $1 \le k \le n$, the determinant can be expanded in the column number k, $det(A) = \sum_{j=1}^n a_{j,k}(-1)^{j + k}det(A_{j,k})$.

Just need to show this works for rows (j) because of theorem 3.4. When $a_{1,k}$ is the only non-zero term in the first row we easily see that $det A = (-1)^{1 + k}a_{1,k}det(A_{1,k})$. But by theorem 3.4, we can just make the first row a sum so that there is only one non-zero row entry per. Then we can just interchange rows to get the first getting us our general formula. $\blacksquare$
Cool fact: requires $\sum_{k=2}^n \frac{n!}{k!}$ multiplications for $n \times n$ matrix.

**Theorem 5.2**
Let A be an invertible matrix and let C be its cofactor matrix. Then $A^{-1} = \frac{1}{det(A)}C^T$.

Notice $AC^T = det(A)I$. $\blacksquare$

**Corollary 5.3**
For an invertible matrix A, the entry number k of the solution of the equation $Ax = b$ is given by the formula $x_k = \frac{det(B_k)}{det(A)}$ where the matrix $B_x$ is obtained from A by replacing column number k of A by vector b.

### Notable Quotes
> “Very often the cofactor expansion formula is used as the definition of determinant."

### References
- *Book Title* — Chapter X, Pages Y–95


## 2.5 Minors And Rank
---
### Definitions
- **Minor**
  - Minor of order k of matrix A is the determinant of its $k \times k$ submatrix.
  - Matrix A has $\begin{pmatrix} m \\ k \end{pmatrix} \cdot \begin{pmatrix} n \\ k \end{pmatrix}$ different $k \times k$ submatrices.

### Theorems & Proofs
**Theorem 6.1**
For a non-zero matrix A its rank equals to the maximal integer k such that there exists a non-zero minor of order k.

**Corollary 6.2**
Let $A = A(x)$ be an $m \times n$ polynomial matrix. Then rank $A(x)$ is a constant everywhere, except maybe finitely many points, where the rank is smaller.

Consider maximum rank of A(x) and some particular minor of order - its a polynomial matrix. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–97
