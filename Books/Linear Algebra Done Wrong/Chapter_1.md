# Chapter 1: Systems Of Linear Equations
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.


## 1.0 Different Faces Of Linear Systems
---
### Key Concepts
- **Linear System**:
  - Contains several representations including matrices.
### Definitions
- **Augmented Matrix**
  - Coefficient matrix with solution(desired vector) column appended.

### References
- *Book Title* — Chapter X, Pages 39–40


## 1.1 Solutions Of A Linear System. Echelon And Reduced Echelon Forms
---
### Key Concepts
- **Row Operations (Gauss-Jordan Elimination)**:
  - 1. Row exchange
  - 2. Multiply a row by a non-zero scalar a.
  - 3. Replace a row by its sum with a constant multiple of another row.
  - $Ax = b$ equivalent to $EAx = Eb$.
- **Row Reduction**:
  - 1. Find the leftmost non-zero column of the matrix.
  - 2. Ensure the first upper entry of this column is non-zero (pivot).
  - 3. Kill all non-zero entries below the pivot.
  - 4. Continue for each row downwards.
  - Runs at most the number of rows times.
### Definitions
- **Echelon Form**
  - Leading entry (pivot) is the leftmost non-zero entry for a row.
  - 1. All zero-rows are below all non-zero entries.
  - 2. For any non-zero row, its leading entry is strictly to the right of the leading entry in the previous row.
  - Triangular form has coefficient $n \times n$ matrix, entries on the main diagonal are non-zero, and all entries below the diagonal are zero.
  - Reduced echelon form has pivots equal to 1 and entries above the pivots set to 0.

### Visual Aids
Interchange rows.
![[Screenshot from 2026-02-02 15-19-36.png]]

Multiply row k by a.
![[Screenshot from 2026-02-02 15-22-49.png]]

Add row k to row j.
![[Screenshot from 2026-02-02 15-23-37.png]]

### References
- *Book Title* — Chapter X, Pages Y–46


## 1.2 Analyzing The Pivots
---
### Definitions
- **Consistent**
  - $Ax = b$ has a solution for some vector b.

### Theorems & Proofs
**Statement 1**
A system is inconsistent iff there is a pivot in the last column of an echelon form of the augmented matrix.

**Statement 2**
A solution (if exists) is unique iff there is a pivot in every column of the coefficient matrix.

**Statement 3**
Equation $Ax = b$ is consistent for all right sides b iff the echelon form of the coefficient matrix has a pivot in every row.

**Statement 4**
Equation $Ax = b$ has a unique solution for any right side b iff both statement 2 and 3 are true.

**Statement 5**
In echelon form, any row and any column has no more than 1 pivot in it.

**Proposition 3.1**
Let us have a system $v_1, v_2, ..., v_m \in \mathbb{F}^n$, and let $A = [v_1, v_2, ..., v_m]$ be an $n \times m$ matrix with columns $v_1, v_2, ..., v_m$. Then,
1) The system is linearly independent iff echelon form of A has a pivot in every column.
2) The system is complete in $\mathbb{F}^n$ iff echelon form of A has a pivot in every row.
3) The system is a basis in $\mathbb{F}^n$ iff echelon form of A has a pivot in every column and every row.

**Proposition 3.2**
Any linearly independent system of vectors in $\mathbb{F}^n$ cannot have more than n vectors in it.

**Proposition 3.3**
Any two bases in a vector space V have the same number of vectors in them.

Let $v_1, v_2, ..., v_n$ and $w_1, w_2, ..., w_m$ be two different bases in V. WLOG assume $n \le m$. Consider an isomorphism $A: \mathbb{F}^n \to V$ defined by $Ae_k = v_k$. Since $A^{-1}$ is also an isomorphism, the system $A^{-1}w_1, A^{-1}w_2, ..., A^{-1}w_m$ is a basis. So it is linearly independent and by Proposition 3.2, $m \le n$. Therefore, $m = n$. $\blacksquare$

**Proposition 3.4**
Any basis in $\mathbb{F}^n$ must have exactly n vectors in it.

By proposition 3.3 or analyzing the matrix of a basis. $\blacksquare$

**Proposition 3.5**
Any spanning set in $\mathbb{F}^n$ must have at least n vectors.

Let $v_1, v_2, ..., v_m$ be a complete system in $\mathbb{F}^n$, and let A be $n \times m$ matrix with columns of this system. Statement 2 of Proposition 3.1 implies that echelon form of A has a pivot in every row. Since number of pivots cannot exceed the number of columns, $n \le m$.

**Proposition 3.6**
A matrix A is invertible iff its echelon form has pivot in every column and every row.

Statement 4 and theorem 6.8 show this.

**Corollary 3.7**
An invertible matrix must be square $n \times n$.

**Proposition 3.8**
If a square ($n \times n$) matrix is left invertible, or it is right invertible, then it is invertible.

If a matrix A is left invertible, the equation $Ax = 0$ has unique solution $x = 0$. Indeed, if B is a left inverse of A, and x satisfies $Ax = 0$, then multiplying this identity by B from the left gets $x = 0$., so the solution is unique. Therefore, the echelon form of A has pivots in every column. If the matrix A is a square ($n \times n$), the echelon form also have pivots in every row, so the matrix is invertible. If a matrix A is right invertible, and C is its right inverse, then for $x = Cb$ for $b \in \mathbb{F}^n$ we get $Ax = ACb = Ib = b$. Therefore, for any right side b the equation $Ax = b$ has a solution $x = Cb$. Thus, echelon form of A has a pivot in every row. If A is square, it also has a pivot in every column, so A is invertible. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–52


## 1.3 Finding $A^{-1}$ by row reduction.
---
### Algorithms
**Inverse Matrix**
Find $A^{-1}$ if existent. If confused, think of the matrix E defined by the row operations.
```pseudo
1. Form an augmented n by 2n matrix (A | I).
2. Row reduce A to I.
3. I will transform to the inverse of A
```

### Theorems & Proofs
**Statement 1**
Any invertible matrix is row equivalent to the identity matrix.

**Theorem 4.1**
Any invertible matrix can be represented as a product of elementary matrices.

$A = (A^{-1})^{-1} = E_1^{-1}E_2^{-1}...E_N^{-1}$. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–54


## 1.4 Dimension. Finite-dimensional spaces.
---
### Definitions
- **Dimension**
  - Number of vectors in a basis.
  - If only the zero vectors, $dim V = 0$.
  - If no finite basis, $dim V = \infty$.

### Theorems & Proofs
**Proposition 5.1**
A vector space V is finite-dimensional iff it has a finite spanning system.

Implied by Proposition 2.8 and Proposition 3.3.

**Proposition 5.2**
Any linearly independent system in a finite-dimensional vector space V cannot have more than dim V vectors in it.

Let $v_1, v_2, ..., v_m \in V$ be linearly independent system, and let $A : V \to \mathbb{R}^n$ be an isomorphism. Then $Av_1, Av_2, ..., Av_m$ is linearly independent system in $\mathbb{R}^n$, and by proposition 3.2 $m \le n$. $\blacksquare$

**Proposition 5.3**
Any generating system in a finite-dimensional vector space V must have at least dim V vectors in it.

Let $v_1, v_2, ..., v_m \in V$ be a complete system, and let $A : V \to \mathbb{R}^n$ be an isomorphism. Then $Av_1, Av_2, ..., Av_m$ is a complete system in $\mathbb{R}^n$, and by Proposition 3.5 $m \ge n$. $\blacksquare$

**Proposition 5.4**
A linearly independent system of vectors in a finite-dimensional space can be completed to a basis.

Let $n = dim V$ and let $r < n$ ($r = n$ is already a basis and $r > n$ is impossible). Take any vector not belonging to $span\{v_1, v_2, ..., v_r\}$ and call it $v_{r + 1}$. This new system is linearly independent. Repeat this process. This stops eventually because vectors can not be more than n. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–56


## 1.5 General Solution Of A Linear System
---
### Definitions
- **Homogeneous System**
  - Has form $Ax = 0$.

### Theorems & Proofs
**Theorem 6.1**
Let a vector $x_1$ satisfy the equation $Ax = b$, and let H be the set of all solutions of the associated homogeneous system $Ax = 0$. Then the set $\{x = x_1 + x_h : x_h \in H\}$ is the set of all solutions of the equation $Ax = b$.

Fix a vector $x_1$ satisfying $Ax_1 = b$. Let a vector $x_h$ satisfy $Ax_h = 0$. Then for $x = x_1 + x_h$, we have $Ax = A(x_1 + x_h) = Ax_1 + Ax_h = b + 0 = b$. So any x of the form $x = x_1 + x_h$ for $x_h \in H$ is a solution of $Ax = b$. Now let x satisfy $Ax = b$. Then for $x_h := x - x_1$, we get $Ax_h = A(x - x_1) = Ax - Ax_1 = b - b = 0.$ So $x_h \in H$. Therefore, any solution x of $Ax = b$ can be represented as $x = x_1 + x_h$ with some $x_h \in H$. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–59


## 1.6 Fundamental Subspaces Of A Matrix. Rank.
---
### Key Concepts
- **Computing Fundamental Subspaces**:
  - The pivot columns of the original matrix gives us a basis in the Ran - notice reduced echelon form has a basis of such columns but row reductions do not influence linear independence and this basis can represent Ev where E is the row reduction matrix which is invertible.
  - Pivot rows of echelon form give us a basis in the row space - notice these rows are linearly independent because each has a unique non-zero entry by definition of reduced echelon form and $\text{Ran} A_e^T = \text{Ran}(A^TE^T) = A^T(\text{Ran}E^T) = A^T(\mathbb{R}^m) = \text{Ran}A^T$.
  - Ker A is found by solving the homogeneous equation - notice the solution of free variables is linearly independent and spanning.
- **Completing A Basis**:
  - Add rows to an echelon form matrix that add pivots to columns.
  - Assumes the original vectors are already linearly independent.
### Definitions
- **Row Space**
  - For matrix A we have Ran $A^T$.
- **Left Null Space**
  - For matrix A we have Ker $A^T$.
- **Fundamental Subspaces**
  - Row Space, Column Space, Null Space, Left Null Space.
- **Rank**
  - rank $A := \text{dim Ran} A$.

### Theorems & Proofs
**Theorem 7.1**
rank A = rank $A^T$ for a matrix A.

**Theorem 7.2**
Let A be an $m \times n$ matrix. Then
1) $\text{dim Ker} A + \text{dim Ran} A = \text{dim Ker} A + \text{rank} A = n$.
2) $\text{dim Ker} A^T + \text{dim Ran} A^T = \text{dim Ker} A^T + \text{rank} A^T = \text{dim Ker} A^T + \text{rank} A = m$.

**Theorem 7.3**
Let A be an $m \times n$ matrix. Then the equation $Ax = b$ has a solution for every $b \in \mathbb{R}^m$ iff the dual equation $A^Tx = 0$ has a unique solution.

### References
- *Book Title* — Chapter X, Pages X-68


## 1.8 Representation Of A Linear Transformation In Arbitrary Bases. Change Of Coordinates Formula.
---
### Key Concepts
- **Coordinate Linear Transformation**:
  - $[Tv]_B = [T]_{BA}[v]_A$.
  - $[v]_B = [I]_{BA}[v]_A$.
  - $[I]_{AB} = ([I]_{BA})^{-1}$.
  - $[T]_{BB} = [I]_{BA}[T]_{AA}[I]_{AB}$.
### Definitions
- **Coordinate Vector**
  - Coordinate vector relative to specified basis.
  - Mapping of vectors to coordinate vectors is isomorphic between V and $\mathbb{F}^n$.
  - Transforms basis to standard basis (why?).
- **Similar**
  - Matrix A similar to B if there exists an invertible matrix Q such that $A = Q^{-1}BQ$.
  - Follows that A and B must be square of same size.

### Theorems & Proofs
**Statement 1**
To get $[T]_{B'A'}$, surround $[T]_{BA}$ by change of coordinates matrices.
$$
[T]_{B'A'} = [I]_{B'B}[T]_{BA}[I]_{AA'}
$$

### References
- *Book Title* — Chapter X, Pages Y–73
