
# Chapter 4: Inner Product Spaces
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 4.0 Inner Product in $\mathbb{R}^n$ and $\mathbb{C}^n$. Inner Product Spaces.
---
### Key Concepts
- **Inner Product Spaces**:
  - Conjugate Symmetry - $(x, y) = \overline{(y, x)}$.
  - Linearity - $(\alpha x + \beta y, z) = \alpha(x, z) + \beta(y, z)$ for all vectors $x, y, z$ and scalars $\alpha, \beta$.
  - Non-negativity - $(x, x) \ge 0$ for all x.
  - Non-degeneracy - $(x, x) = 0$ iff $x = 0$.
  - Inner product is a function, $f : \{(x, y) | \text{x and y are vectors}\} \to \mathbb{F}$, satisfying these properties.
  - Inner product space is a function along with a vector space (inherits norm space).

### Definitions
- **Norm**
  - A norm of $x \in \mathbb{R}^n$ is $||x|| = \sqrt{x_1^2 + x_2^2 + ... + x_n^2}$.
  - A norm of $z \in \mathbb{C}^n$ is $||z||^2 = \sum_{k = 1}^n |z_k|^2$.
  - Norm is a function $v \to ||v||$ that must satisfy:
  - Homogeneity - $||\alpha v|| = |\alpha | \cdot ||v||$.
  - Triangle Inequality - $|| u + v|| \le ||u|| + ||v||$.
  - Non-negativity - $||v|| \ge 0$.
  - Non-degeneracy - $||v|| = 0 \iff v = 0$.
  - Norm space is a vector space with a norm.
  - Norm alternative - $||x||_p = (|x_1|^p + |x_2|^p + ... + |x_n|^p)^{\frac{1}{p}}$.
  - $||x||_\infty = max\{|x_k| : k = 1, 2, ..., n\}$.
- **Inner Product**
  - The inner product of $x, y \in \mathbb{R}^n$ is $(x, y) := x_1y_1 + x_2y_2 + ... + x_ny_n = y^T x = x^Ty$.
  - The standard inner product of $z, w \in \mathbb{C}^n$ is $(z, w) := \sum_{k=1}^n z_k \overline{w_k} = w*z$. (motivated by the reals)
  - $||x|| = \sqrt{(x, x)}$.
- **Hermitian Adjoint**
  - Adjoint of matrix A denoted by $A* = \overline{A}^T$.

### Theorems & Proofs
**Statement 1**
$(x, \alpha y + \beta z) = \overline{a} (x, y) + \overline{\beta} (x, z)$.

**Statement 2**
$(0, x) = (x, 0) = x$.

*All below assume norm in an inner product space:*

**Lemma 1.4**
Let x be a vector in an inner product V. Then $x = 0$ iff $\forall y \in V (x, y) = 0$.

**Corollary 1.5**
Let $x, y$ be vectors in an inner product space V. The equality $x = y$ holds iff $(x, z) = (y, z)$ for all $z \in V$.

**Corollary 1.6**
Suppose two operators $A, B : X \to Y$ satisfy $(Ax, y) = (Bx, y)$ $\forall x \in X, \forall y \in Y$. Then $A = B$.

**Theorem 1.7**
$|(x, y)| \le ||x|| \cdot ||y||$.

**Lemma 1.8**
For any vectors $x, y$ in an inner product space $||x + y|| \le ||x|| + ||y||$.

**Lemma 1.9**
For $x, y \in V$ we have $(x, y) = 0.25(||x + y||^2 - ||x - y||^2)$ if V is a real inner product space, and $(x, y) = 0.25 \sum _{\alpha = \pm 1, \pm i} \alpha ||x + \alpha y ||^2$ if V is a complex inner product space.

**Lemma 1.10**
For any vectors u, v $||u + v||^2 + ||u - v||^2 = 2(||u||^2 + ||v||^2)$.

**Theorem 1.11**
A norm in a normed space is obtained from some inner product iff it satisfies Lemma 1.10.

### References
- *Book Title* — Chapter X, Pages Y–125


## 4.1 Orthogonality. Orthogonal and orthonormal bases.
---
### Definitions
- **Orthogonal**
  - Two vectors $u, v$ are orthogonal if $(u, v) = 0$, denoted $u \perp v$.
  - $||u + v||^2 = ||u||^2 + ||v||^2$.
  - Vector v is orthogonal to a subspace E if v is orthogonal to all vectors w in E.
  - Subspaces E and F are orthogonal if all vectors in E are orthogonal to F.
  - A system of vectors is orthogonal if any two vectors are orthogonal to each other.
  - Any system that is orthogonal and a basis is called an orthogonal basis.
  - In an orthogonal basis, coordinates determined by $\alpha_k = \frac{(x, v_k)}{||v_k||^2}$ for vector x.
- **Orthonormal**
  - If $||v_k|| = 1$ for all k in a system of vectors.
  - Any system that is orthonormal and a basis is called an orthonormal basis.

### Theorems & Proofs
**Lemma 2.3**
Let E be spanned by vectors $v_1, v_2, ..., v_r$. Then $v \perp E$ iff $v \perp v_k$ for all $k = 1,2,...,r$.

**Lemma 2.5**
Let $v_1, v_2, ..., v_n$ be an orthogonal system. Then $||\sum_{k=1}^n\alpha_k v_k ||^2 = \sum_{k=1}^n |\alpha_k |^2 ||v_k ||^2$.

**Corollary 2.6**
Any orthogonal system $v_1, v_2, ..., v_n$ of non-zero vectors is linearly independent.

### References
- *Book Title* — Chapter X, Pages Y–129


## 4.2 Orthogonal Projection And Gram-Schmidt Orthogonalization
---
### Definitions
- **Orthogonal Projection**
  - Orthogonal projection of v from inner product space V to subspace E, $P_Ev$, is a vector w such that:
  - 1) $w \in E$.
  - 2) $v - w \perp E$.
  - Scalar multiplication does not change the orthogonality.
- **Orthogonal Complement**
  - For a subspace E, its orthogonal complement is notated $E^{\perp} := \{x | x \perp E\}$.
  - Also a subspace.

### Algorithms
**Gram-Schmidt Orthogonalization Algorithm**
Constructs orthogonal system $v_1, v_2, ..., v_n$ from linearly independent system $x_1, x_2, ..., x_n$ such that $span\{x_1, x_2, ..., x_n\} = span\{v_1, v_2, ..., v_n\}$. Moreover, for every $r \le n$, $span\{x_1, x_2, ..., x_r\} = span\{v_1, v_2, ..., v_r\}$.

1. Put $v_1 := x_1$. Denote $E_1 := span\{x_1\} = span\{v_1\}$.
2. Define $v_2$ by $v_2 = x_2 - P_{E_1}x_2 = x_2 - \frac{(x_2, v_1)}{||v_1||^2}v_1$. Define $E_2 = span\{v_1, v_2\} = span\{x_1, x_2\}$.
3. (r+1) Suppose we have $E_r := span\{v_1, v_2, ..., v_r\} = span\{x_1, x_2, ..., x_r\}$. Define $v_{r+1} := x_{r+1} - P_{E_r}x_{r+1} = x_{r+1} - \sum_{k=1}^r \frac{(x_{r+1}, v_k)}{||v_k||^2}v_k$. Note that $x_{r+1} \not \in E_r$ so $v_{r+1} \not = 0$.

### Theorems & Proofs
**Theorem 3.2**
The orthogonal projection $w = P_Ev$ satisfies $||v - w|| \le ||v - x||$ for all $x \in E$. Moreover, if for some $x \in E$, $||v - w|| = ||v - x||$, then $x = w$.

**Proposition 3.3**
Let $v_1, v_2, ..., v_r$ be an orthogonal basis in E. Then the orthogonal projection $P_Ev$ of a vector v is given by the formula $P_Ev = \sum_{k = 1}^r \alpha_k v_k$ where $\alpha_k = \frac{(v, v_k)}{||v_k||^2}$.

**Statement 1**
$v = v_1 + v_2$ where $v_1 \in E$ and $v_2 \in E^\perp$ for any vector v in a inner product space V. Denoted $V = E \oplus E^\perp$.

**Proposition 3.6**
For a subspace E $(E^{\perp})^\perp = E$.

### References
- *Book Title* — Chapter X, Pages Y–135


## 4.3 Least Square solution. Formula For The Orthogonal Projection
---
### Key Concepts
- **Least Square Solution**:
  - Find minimal error solution for $||Ax - b||$ such that $Ax$ close to b.
  - Clearly, $Ax = P_{Ran A}b$ solves this since we can not get any closer distance wise.
  - $Ax = P_{Ran A}b$ iff $b - Ax \perp Ran A$ iff $b - Ax \perp a_k$ for all $k = 1, 2, ..., n$ where $a_k$ is a column of A.
  - Then $0 = (b - Ax, a_k) = a_k* (b - Ax) = A*(b - Ax)$.
  - We get the normal equation $A*Ax = A*b$.
  - If $A*A$ is invertible then x is unique and $P_{Ran A} = A(A*A)^{-1}A*$.

### Theorems & Proofs
**Theorem 4.1**
For an $m \times n$ matrix A $Ker A = Ker(A*A)$.

### References
- *Book Title* — Chapter X, Pages Y–142


## 4.4 Adjoint Of A Linear Transformation. Fundamental Subspaces Revisited.
---
### Key Concepts
- **Linear Transformation Essentials**:
  - Let $A' : Ran A* \to Ran A$ where $A'x = Ax$. Then $Ax = AP_{RanA*x} = A'P_{RanA*}$ for all $x \in X$. So $A = A' P_{Ran A*}$.
  - $A'$ is the essential part of A and is invertible.

### Theorems & Proofs
**Statement 1**
$\forall x \in \mathbb{C^n}, \forall y \in \mathbb{C^m} (Ax, y) = (x, A*y)$ obtained from adjoint property.

**Statement 2**
The adjoint property is unique.

**Statement 3**
a) $(A + B)* = A* + B*$.
b) $(\alpha A)* = \overline{\alpha}A*$.
c) $(AB)* = B*A*$.
d) $(A*)* = A$.
e) $(y, Ax) = (A*y, x)$.

**Theorem 5.1**
Let $A : V \to W$ be an operator acting from one inner product space to another. Then
a) $Ker A* = (Ran A)^\perp$.
b) $Ker A = (Ran A*)^\perp$.
c) $Ran A = (Ker A*)^\perp$.
d) $Ran A* = (Ker A)^\perp$.

### References
- *Book Title* — Chapter X, Pages Y–146


## 4.5 Isometries And Unitary Operators. Unitary And Orthogonal Matrices.
---
### Definitions
- **Isometry**
  - Operator $U : X \to Y$ that preserves the norm $||Ux|| = ||x||$ for all $x \in X$.
- **Unitary**
  - Isometry that is invertible.
  - Unitary square matrix U such that $U*U = I$.
  - Real unitary matrix is called an orthogonal matrix.
- **Unitarily Equivalent**
  - Operators A and B such that there exists a unitary operator U where $A = UBU*$.

### Theorems & Proofs
**Theorem 6.1**
An operator $U : X \to Y$ is an isometry iff it preserves the inner product $(x, y) = (Ux, Uy)$ for all $x,y \in Xx$. (linear U)

**Lemma 6.2**
An operator $U : X \to Y$ is an isometry iff $U*U = I$.

**Proposition 6.3**
An isometry $U : X \to Y$ is a unitary operator iff $dim X = dim Y$.

**Statement 1**
a) For a unitary transformation U, $U^{-1} = U*$.
b) If U is unitary, $U* = U^{-1}$ is also unitary.
c) If U is a isometry, and $v_1, v_2, ..., v_n$ is an orthonormal basis, then $Uv_1, Uv_2, ..., Uv_n$ is an orthonormal system. Moreover, if U is unitary, $Uv_1$, $Uv_2$, ..., $Uv_n$ is an orthonormal basis.
d) A product of unitary operators is a unitary operator as well.

**Statement 2**
A matrix U is an isometry iff its columns form an orthonormal system.

**Proposition 6.4**
Let U be a unitary matrix. Then
a) $|det U| = 1$. In particular, for an orthogonal matrix $det U = \pm 1$.
b) If $\lambda$ is an eigenvalue of U, then $|\lambda| = 1$.

**Proposition 6.5**
A matrix A is unitarily equivalent to a diagonal one iff it has an orthogonal basis of eigenvectors.

### References
- *Book Title* — Chapter X, Pages Y–151


## 4.6 Rigid Motions in $\mathbb{R}^n$
---
### Definitions
- **Rigid Motion**
  - Rigid motion in an inner product space V is a transformation $f: V \to V$ where $||f(x) - f(y) || = ||x-y||$ for all $x, y \in V$.
  - Not necessarily linear.

### Theorems & Proofs
**Theorem 7.1**
Let f be a rigid motion in a real inner product space X, and let $T(x) := f(x) - f(0)$. Then T is an orthogonal transformation.

**Lemma 7.2**
Let T be as defined in Theorem 7.1. Then for all $x, y \in X$,
a) $||Tx|| = ||x||$;
b) $||T(x) - T(y)|| = ||x-y||$;
c) $(T(x), T(y)) = (x,y)$.

### References
- *Book Title* — Chapter X, Pages Y–153
  
  
## 4.7 Complexification And Decomplexification
---
### Key Concepts
- **Decomplexification**:
  - To decomplexify a complex inner product space, only allow real multiples.
  - $(x, y)_{\mathbb{R}} = Re(x, y)_{\mathbb{C}}$.
- **Complexification**:
  - To construct a complification of a real vector space X, pick a basis and then work with coordinates, allowing complex ones. No dependence on choice of basis in resulting space.
  - 

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

### Notable Quotes
> “Notable quote."
### Common Pitfalls
- Pitfall 1.
### Related Links
- [Link]()
### References
- *Book Title* — Chapter X, Pages Y–Z
