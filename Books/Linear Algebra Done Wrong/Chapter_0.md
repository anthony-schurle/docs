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
  - (3) Zero vector: $\exists 0 \in V \forall v \in V (v + 0 = v)$.
  - (4) Additive Inverse: $\forall v \in V \exists w \in V (v + w = 0)$.
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
  - $A: V \to W$ is right invertible if $\exists B: W \to V (AB = I)$.
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
Let $A : X \to Y$ a linear transformation. Then A is invertible iff for any right side $b \in Y$, the equation $Ax = b$ has a unique solution $x \in X$.

Suppose A is invertible. Then $x = A^{-1}b$ solves the equation $Ax = b$. Suppose for some other vector $v_1 \in X$, $Ax_1 = b$. Multiplying by $A^{-1}$ from the left gives $A^{-1}Ax_1 = A^{-1}b$. Therefore, $x_1 = x$. Now suppose the equation $Ax = b$ has unique solution $x$ for any $b \in Y$. Call the solution $B(b)$ and define a transformation $B : Y \to X$. It is easy to show that B is a linear transformation if we define $x_k := B(y_k)$. Take $x \in X$ and let $y = Ax$, so by definition of B we have $x = By$. Then for all $x \in X$, $BAx = By = x$. So $BA = I$. For arbitrary $y \in Y$, let $x = By$, so $y = Ax$. Then for all y, $ABy = Ax = y$ and so $AB = I$.
**Q.E.D**

**Corollary 6.9**
An $m \times n$ matrix is invertible iff its columns form a basis in $\mathbb{F}^m$.

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

### References
- *Book Title* — Chapter X, Pages Y–31


## 0.7 Application To Computer Graphics
---
### Key Concepts
- **Graphics**:
  - Monitor can be represented as a grid of discrete pixels.
### Definitions
- **Bitmap**
  - Every pixel of an object is described.
- **Vector Object**
  - Only critical points of an object are described.

### Visual Aids
![[Screenshot from 2026-02-02 14-30-08.png]]


### References
- *Book Title* — Chapter X, Pages Y–37
