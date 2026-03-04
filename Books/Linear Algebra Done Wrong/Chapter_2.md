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
  - Deducible from column replacement $D(v_1, ..., v_j, ..., v_j, ..., v_n) = -D(v_1, ..., v_k, ..., v_j, ..., v_n)$.
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

### Examples
**Example Title**
**Problem 3.5:**
A square matrix is called nilpotent if $A^k = 0$ for some positive integer k. Show that for a nilpotent matrix A $det A = 0$.
**Solution:**
Suppose A is nilpotent for some positive integer k. It suffices to show that the columns of A are linearly dependent, and so A is not invertible, because of proposition 3.3. For the sake of contradiction, suppose A was linearly independent. We see that $A^k x = 0$ for all x and so $A(A^{k-1}x) = 0$. This implies $A^{k-1}x = 0$ since A is linearly independent. This then implies $A(A^{k-2}x) = 0$ so that $A^{k-2}x = 0$. Continuing this process gets $Ax = 0$ for all x. This is a contradiction of A being linearly independent. Thus, A is linearly dependent in its columns. $\blacksquare$

**Problem 3.6**
Prove that if the matrices A and B are similar, then $det A = det B$.
**Solution:**
By definition of similar matrices, $A = Q^{-1}BQ$ for some matrix Q. By theorem 3.5, $det(A) = det(Q^{-1}BQ) = det(Q^{-1})det(BQ) = det(BQ)det(Q^{-1}) = det(BQQ^{-1}) = det(BI) = det(B)$. $\blacksquare$

**Problem 3.8**
Show that $\begin{vmatrix} 1 & x & x^2 \\ 1 & y & y^2 \\ 1 & z & z^2 \end{vmatrix} = (z - x)(z - y)(y - x)$. This is a particular case of the Vandermonde determinant.
**Solution:**
$$
\begin{vmatrix} 1 & x & x^2 \\ 0 & 1 & y + x \\ 0 & 0 & z - y \end{vmatrix} = \begin{vmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & -1 & 1 \end{vmatrix} \begin{vmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & \frac{1}{z - x} \end{vmatrix} \begin{vmatrix} 1 & 0 & 0 \\ 0 & \frac{1}{y - x} & 0 \\ 0 & 0 & 1 \end{vmatrix} \begin{vmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -1 & 0 & 1 \end{vmatrix} \begin{vmatrix} 1 & 0 & 0 \\ -1 & 1 & 0 \\ 0 & 0 & 1 \end{vmatrix} \begin{vmatrix} 1 & x & x^2 \\ 1 & y & y^2 \\ 1 & z & z^2 \end{vmatrix}
$$
$$
\implies z - y = (1)(\frac{1}{z - x})(\frac{1}{y - x})(1)(1)\begin{vmatrix} 1 & x & x^2 \\ 1 & y & y^2 \\ 1 & z & z^2 \end{vmatrix}
$$
$$
\implies (z - y)(z - x)(y - x) = \begin{vmatrix} 1 & x & x^2 \\ 1 & y & y^2 \\ 1 & z & z^2 \end{vmatrix}
$$
If $z - y$, $z - x$, or $y - x$ are 0 then the matrix is not invertible and so both sides are 0. $\blacksquare$

**Problem 3.12**
Let A be $m \times n$ and B be $n \times m$ matrices. Prove that $\begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} = det(AB)$.
**Solution:**
By theorem 3.5,
$$
\begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} \begin{vmatrix} I & 0 \\ B & I \end{vmatrix} = \begin{vmatrix} AB & A \\ 0 & I \end{vmatrix}
$$
By problem 3.11 and theorem 3.4 this implies,
$$
\begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} \begin{vmatrix} I & B \\ 0 & I \end{vmatrix} = det(AB)det(I)
$$
and so,
$$
\begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} det(I)^2 = det(AB) \implies \begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} = det(AB)
$$
$\blacksquare$

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
### Examples
**Example Title**
**Problem 4.3:**
Why is there an even number of permutations of (1, 2, . . . , 9) and why are
exactly half of them odd permutations? Hint: This problem can be hard to solve
in terms of permutations, but there is a very simple solution using determinants.
**Solution:**
There are $9! = 9 * 8 * 7 * 6 * 5 * 4 * 3 * 2 * 1 = 362880$ permutations. Notice this is even because 2 is a factor. Now consider the $9 \times 9$ matrix where every entry is 1 and its corresponding determinant 0 (two columns\vectors are identitical). We see that $0 = \sum_{\sigma \in Perm(9)}a_{\sigma(1),1}a_{\sigma(2),2}...a_{\sigma(9),9} sign(\sigma)$. But every entry is 1 so this simplifies to $0 = \sum_{\sigma \in Perm(9)} sign(\sigma)$. Because odd permutations have negative sign this becomes $0 = \text{\# even permutations} - \text{\# odd permutations}$ which indicates there are equal even permutations to odd permutations. In other words, odd permutations make up half the permutation count of (1, 2, ..., 9). $\blacksquare$

**Problem 4.4:**
If $\sigma$ is an odd permutation, explain why $\sigma^2$ is even but $\sigma^{-1}$ is odd.
**Solution:**
Suppose $\sigma$ is an odd permutation. Then $sign(\sigma^2) = 
### References
- *Book Title* — Chapter X, Pages Y–89


## 2.4 Cofactor Expansion
---
### Key Concepts
- **Concept Name**:
  - Subpoint or clarification.
### Definitions
- **Term 1**
  - Concise explanation of the term.
### Algorithms
**Algorithm Name**
Description.
```pseudo
1. Step 1
2. Step 2
3. Step 3
```

### Theorems & Proofs
**Theorem 5.1**
Let A be an $n \times n$ matrix and let $A_{j,k}$ denote the $(n - 1) \times (n - 1)$ matrix obtained from A by crossing out row number j and column number k. For each j, $1 \le j \le n$, determinant of A can be expanded in the row number j as $det(A) = \sum_{k=1}^n a_{j,k}(-1)^{j+k}det(A_{j,k})$. Similarly, for each k, $1 \le k \le n$, the determinant can be expanded in the column number k, $det(A) = \sum_{j=1}^n a_{j,k}(-1)^{j + k}det(A_{j,k})$.

Just need to show this works for rows (j) because of theorem 3.4. When $a_{1,k}$ is the only non-zero term in the first row we easily see that $det A = (-1)^{1 + k}a_{1,k}det(A_{1,k})$.

### Formulas
**Formula Name**
Description.
$$
Equation
$$
### Visual Aids
| Header | Header |
| - | - |
| Content | Content |
![Diagram]()
### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.
### Notable Quotes
> “Notable quote."
### Common Pitfalls
- Pitfall 1.
### Related Links
- [Link]()
### References
- *Book Title* — Chapter X, Pages Y–Z

- [Author(s), "Paper or Article Title," Journal or Conference Name, Year]() 

- [Related Chapter in This Wiki]()  

- [Official Specification or Standard Document (PDF/URL)]()  

- Class Lecture ([Link]())
