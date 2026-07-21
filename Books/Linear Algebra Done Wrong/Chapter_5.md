# Chapter #: Structure Of Operators In Inner Product Spaces.
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 5.0 Upper Triangular (Schur) Representation Of An Operator
---
### Theorems & Proofs
**Theorem 1.1**
Let $A: X\to X$ be an operator acting in a complex inner product space. A can be represented by $A = UTU*$ where T is an upper triangular matrix and U is a unitary.

**Theorem 1.2**
Let $A : X \to X$ be an operator in a real inner product space. Suppose that all eigenvalues of A are real. Then $A = UTU* = UTU^T$ where U is an orthogonal and T is a real upper triangular matrix.

### References
- *Book Title* — Chapter X, Pages Y–165


## 5.1 Spectral Theorem For Self-Adjoint And Normal Operators
---
### Definitions
- **Hermitian Matrix**
  - Self-adjoint operator in some orthonormal basis.
- **Normal**
  - Operator N is normal if $N*N = NN*$.

### Theorems & Proofs
**Theorem 2.1**
Let A be self-adjoint operator in an inner product space X. Then all eigenvalues of A are real, and there exists and orthonormal basis of eigenvectors of A in X.

**Theorem 2.2**
Let A be self-adjoint matrix. Then A can be represented as $A = UDU*$ where U is a unitary matrix and D is a diagonal matrix with real entries. Moreover, if the matrix is real, matrix U can be chosen to be real.

**Proposition 2.3**
Let A be a self-adjoint operator, and let $u, v$ be its eigenvectors, $Au = \lambda u, Av = \mu v$. Then, if $\lambda \ne \mu$, the eigenvectors u and v are orthogonal.

**Theorem 2.4**
Any normal operator N in a complex vector space can be represented as $N = UDU*$ where U is a unitary matrix and D is a diagonal one.

**Proposition 2.5**
An operator $N : X \to X$ is normal iff $||Nx|| = ||N*x||$ for all $x \in X$.

### References
- *Book Title* — Chapter X, Pages Y–171


## 5.2 Polar And Singular Value Decompositions
---
### Key Concepts
- **Concept Name**:
  - Subpoint or clarification.
### Definitions
- **Positive Definite**
  - Self-adjoint operator $A : X \to X$ is positive definite if $(Ax, x) > 0$ for all $x \ne 0$.
  - Notated $A > 0$.
- **Positive Semidefinite**
  - Self-adjoint operator $A : X \to X$ is positive definite if $(Ax, x) \ge 0$ for all $x \in X$.
  - Notated $A \ge 0$.
- **Hermitian Square**
  - For an operator A, its hermitian square is $A*A$.
  - Always positive semidefinite.
- **Modulus**
  - Denoted $|A|$ for operator A, is the square root of the hermitian square.
- **Singular Values**
  - Eigenvalues of $|A|$.
- **Schmidt Decomposition**
  - Derived from Proposition 3.6.
  - $A = \sum_{k=1}^r \sigma_k w_k v_k*$.
  - Not unique.
  - Matrix can be represented by $A = W'\sum ' V'*$, where $W', V'$ are the matrices with columns $w_1, w_2, ..., w_r$ and $v_1, v_2, ..., v_r$ respectively and $\sum ' = diag\{\sigma_1, \sigma_2, ..., \sigma_r\}$ - called reduced SVD after the next part.
  - Notice $W'$ and $V'$ can be completed to unitary matrices with Gram-Schmidt orthogonalization and filling $\sum '$ with 0s.
  - The representation is then $A = W\sum V*$ and is called the singular value decomposition (SVD).
  - SVD derives polar decomposition since $W\sum V* = (WV*)(V\sum V*) = U|A|$.

### Theorems & Proofs
**Theorem 3.1**
Let $A = A*$. Then $A > 0$ iff all eigenvalues of A are positive. $A \ge 0$ iff all eigenvalues of A are non-negative.

**Corollary 3.2**
Let $A = A* \ge 0$. There exists a unique positive semidefinite operator B such that $B^2 = A$.

**Proposition 3.3**
For a linear operator $A : X \to Y$, $|| |A | x || = ||Ax||$ for all $x \in X$.

**Corollary 3.4**
$Ker A = Ker |A| = (Ran|A|)^\perp$.

**Theorem 3.5**
Let $A : X \to X$ be an operator. Then A can be represented as $A = U|A|$ where U is a unitary operator. U is unique iff A is invertible.

**Proposition 3.6**
Let $A : X \to Y$ be an operator with singular values $\sigma_1, \sigma_2, ..., \sigma_n$ and $\sigma_1, \sigma_2, ..., \sigma_r$ non-zero singular values. Also, let $v_1, v_2, ..., v_n$ be an orthonormal basis of eigenvectors of $A*A$ such that $A*Av_k = \sigma_k^2 v_k$. The system $w_k := \frac{1}{\sigma_k}Av_k, k = 1, 2, ..., r$ is an orthonormal system.

**Lemma 3.7**
Let A be represented as $A = \sum_{k=1}^r \sigma_k w_k v_k*$ where $\sigma_k > 0$ and $v_1, v_2, ..., v_r, w_1, w_2, ..., w_r$ are some orthonormal systems. Then this representation gives a Schmidt decomposition of A.

**Corollary 3.8**
Let $A = \sum_{k=1}^r \sigma_k w_k v_k*$ be a Schmidt decomposition of A. Then $A* = \sum_{k=1}^r \sigma_k v_k w_k*$ is a Schmidt decomposition of $A*$.

### References
- *Book Title* — Chapter X, Pages Y–179


## 5.3 Applications Of The Singular Value Decomposition
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
**Theorem Name**
Proof.

### Notable Quotes
> “Notable quote."
### Common Pitfalls
- Pitfall 1.
### Related Links
- [Link]()
### References
- *Book Title* — Chapter X, Pages Y–
