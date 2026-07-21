# Chapter 3: Introduction To Spectral Theory
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 3.0 Main Definitions
---
### Key Concepts
- **Finding Characteristic Polynomial Of Abstract Operator**:
  - Take arbitrary basis, and compute eigenvalues of the matrix of the operator in this basis.
  - Statement 2 supports arbitrary basis.

### Definitions
- **Eigenvalue + Eigenvector + Eigenspace**
  - Scalar $\lambda$ is an eigenvalue of $A : V \to V$ if there exists a non-zero eigenvector (corresponding to $\lambda$) $v \in V$ such that $Av = \lambda v \implies (A - \lambda I)v = 0$.
  - Eigenspace is Ker($A - \lambda I$).
- **Spectrum**
  - Set of all eigenvalues of operator A denoted $\sigma(A)$.
- **Characteristic Polynomial**
  - $det(A - \lambda I)$ is a polynomial that describes the eigenvalues of A by its roots, including multiplicity.
- **Complexification**
  - Interpreting an abstract real vector space as a complex space.
  - Crucial for solutions to the characteristic polynomial.
- **Geometric Multiplicity**
  - Dimension of eigenspace.

### Theorems & Proofs
**Statement 1**
$\lambda \in \sigma(A) \iff det(A - \lambda I) = 0$.

**Statement 2**
Characteristic polynomials of similar matrices coincide.

**Proposition 1.1**
Geometric multiplicity of an eigenvalue cannot exceed its algebraic multiplicity.

**Theorem 1.2**
Let A be an $n \times n$ matrix, and let $\lambda_1, \lambda_2, ..., \lambda_n$ be its eigenvalues. Then:
1)trace(A) $= \lambda_1 + \lambda_2 + ... + \lambda_n$.
2)det(A) $= \lambda_1 \lambda_2 ... \lambda_n$.

**Statement 3**
Eigenvalues of a triangular matrix are exactly the diagonal entries.

Implied by Theorem 1.2. $\blacksquare$

### Notable Quotes
> “The fundamental theorem of algebra asserts that any polynomial (of degree at least 1) has a complex root. That implies that an operator in a finite-dimensional complex vector space has at least one eigenvalue, so its spectrum is non-empty."

### References
- *Book Title* — Chapter X, Pages Y–105


## 3.1 Diagonalization
---
### Definitions
- **Matrix Exponent**
  - $e^{tA} = \sum_{k=0}^\infty \frac{t^kA^k}{k!}$.
- **Subspace Definitions**
  - $V_1, V_2, ..., V_p$ form a basis for V if $v = \sum_{k=1}^p v_k$ for all $v \in V$ where $v_k \in V_k$ (unique).
  - The systems of subspaces is generating if such a representation is not unique.
  - $V_1, V_2, ..., V_p$ linearly independent in V if $v_1 + v_2 + ... + v_p = 0$ only has the trivial solution.

### Theorems & Proofs
**Theorem 2.1**
A matrix A admits a representation $A = SDS^{-1}$ where D is a diagonal matrix and S is an invertible one iff there exists a basis in $\mathbb{F}^n$ of eigenvectors of A. Diagonal entries of D are the eigenvalues and the columns of S are the corresponding eigenvectors.

**Statement 1**
$$
A^N = SD^NS^{-1}
$$
and
$$
[e^{tA}]_{BB} = diag\{e^{\lambda_1 t}, e^{\lambda_2 t}, ...\}
$$

**Theorem 2.2**
Let $\lambda_1, \lambda_2, ..., \lambda_r$ be distinct eigenvalues of A, and let $v_1, v_2, ..., v_r$ be the corresponding eigenvectors. Then vectors $v_1, v_2, ..., v_r$ are linearly independent. (Eigenspaces system are linearly independent)

**Corollary 2.3**
If an operator $A : V \to V$ has exactly $n = dim V$ distinct eigenvalues, then it is diagonalizable.

**Theorem 2.6**
Let $V_1, V_2, ..., V_p$ be a basis of subspaces, and let us have in each subspace $V_k$ a basis $\beta_k$. Then the union $\cup_k \beta_k$ of these bases is a basis in V.

**Lemma 2.7**
Let $V_1, V_2, ..., V_p$ be linearly independent family of subspaces, and let us have in each subspace $V_k$ a linearly independent system $\beta_k$ of vectors. Then the union $\beta := \cup_k \beta_k$ is a linearly independent system.

**Theorem 2.8**
Let an operator $A : V \to V$ have exactly $n = dim V$ eigenvalues. Then A is diagonalizable iff for each eigenvalue $\lambda$ the dimension of the eigenspace $Ker(A - \lambda I)$ coincides with the algebraic multiplicity of $\lambda$.

**Theorem 2.9**
A real $n \times n$ matrix A admits a real factorization iff it admits complex factorization and all eigenvalues of A are real.

### References
- *Book Title* — Chapter X, Pages Y–116
