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

### Examples
**Example Title**
**Problem 2.1:**
Write the systems of equations below in matrix form and as vector equations:
a)
$$
\begin{cases} x_1 + 2x_2 - x_3 = -1 \\ 2x_1 + 2x_2 + x_3 = 1 \\ 3x_1 + 5x_2 - 2x_3 = -1 \end{cases}
$$

b)
$$
\begin{cases} x_1 - 2x_2 - x_3 = 1 \\ 2x_1 - 3x_2 + x_3 = 6 \\ 3x_1 - 5x_2 = 7 \\ x_1 + 5x_3 = 9 \end{cases}
$$

c)
$$
\begin{cases} x_1 + 2x_2 + 2x_4 = 6 \\ 3x_1 + 5x_2 - x_3 + 6x_4 = 17 \\ 2x_1 + 4x_2 + x_3 + 2x_4 = 12 \\ 2x_1 - 7x_3 + 11x_4 = 7 \end{cases}
$$

d)
$$
\begin{cases} x_1 - 4x_2 - x_3 + x_4 = 3 \\ 2x_1 - 8x_2 + x_3 - 4x_4 = 9 \\ -x_1 + 4x_2 - 2x_3 + 5x_4 = -6 \end{cases}
$$

e)
$$
\begin{cases} x_1 + 2x_2 - x_3 + 3x_4 = 2 \\ 2x_1 + 4x_2 - x_3 + 6x_4 = 5 \\ x_2 + 2x_4 = 3 \end{cases}
$$

f)
$$
\begin{cases} 2x_1 - 2x_2 - x_3 + 6x_4 - 2x_5 = 1 \\ x_1 - x_2 + x_3 + 2x_4 - x_5 = 2 \\ 4x_1 - 4x_2 + 5x_3 + 7x_4 - x_5 = 6 \end{cases}
$$

g)
$$
\begin{cases} 3x_1 - x_2 + x_3 - x_4 + 2x_5 = 5 \\ x_1 - x_2 - x_3 - 2x_4 - x_5 = 2 \\ 5x_1 - 2x_2 + x_3 - 3x_4 + 3x_5 = 10 \\ 2x_1 - x_2 - 2x_4 + x_5 = 5 \end{cases}
$$


Solve the systems in vector form.
**Solution:**
a)  
$$
\begin{pmatrix} 
1 & 2 & -1 \\ 
2 & 2 & 1 \\ 
3 & 5 & -2 
\end{pmatrix} 
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} 
= 
\begin{pmatrix} -1 \\ 1 \\ -1 \end{pmatrix}
$$

$$
x_1 \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix} + 
x_2 \begin{pmatrix} 2 \\ 2 \\ 5 \end{pmatrix} + 
x_3 \begin{pmatrix} -1 \\ 1 \\ -2 \end{pmatrix} 
= 
\begin{pmatrix} -1 \\ 1 \\ -1 \end{pmatrix}
$$

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix}
=
\begin{pmatrix} 4 \\ -3 \\ -1 \end{pmatrix}
$$

b)  
$$
\begin{pmatrix} 
1 & -2 & -1 \\ 
2 & -3 & 1 \\ 
3 & -5 & 0 \\ 
1 & 0 & 5 
\end{pmatrix} 
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} 
= 
\begin{pmatrix} 1 \\ 6 \\ 7 \\ 9 \end{pmatrix}
$$

$$
x_1 \begin{pmatrix} 1 \\ 2 \\ 3 \\ 1 \end{pmatrix} + 
x_2 \begin{pmatrix} -2 \\ -3 \\ -5 \\ 0 \end{pmatrix} + 
x_3 \begin{pmatrix} -1 \\ 1 \\ 0 \\ 5 \end{pmatrix} 
= 
\begin{pmatrix} 1 \\ 6 \\ 7 \\ 9 \end{pmatrix}
$$

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix}
=
\begin{pmatrix} 9 - 5x_3 \\ 4 - 3x_3 \\ x_3 \end{pmatrix}, \forall x_3 \in \mathbb{R}
$$

c)  
$$
\begin{pmatrix} 
1 & 2 & 0 & 2 \\ 
3 & 5 & -1 & 6 \\ 
2 & 4 & 1 & 2 \\ 
2 & 0 & -7 & 11 
\end{pmatrix} 
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} 
= 
\begin{pmatrix} 6 \\ 17 \\ 12 \\ 7 \end{pmatrix}
$$

$$
x_1 \begin{pmatrix} 1 \\ 3 \\ 2 \\ 2 \end{pmatrix} + 
x_2 \begin{pmatrix} 2 \\ 5 \\ 4 \\ 0 \end{pmatrix} + 
x_3 \begin{pmatrix} 0 \\ -1 \\ 1 \\ -7 \end{pmatrix} + 
x_4 \begin{pmatrix} 2 \\ 6 \\ 2 \\ 11 \end{pmatrix} 
= 
\begin{pmatrix} 6 \\ 17 \\ 12 \\ 7 \end{pmatrix}
$$

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix}
=
\begin{pmatrix} 2 \\ 3 \\ -2 \\ -1 \end{pmatrix}
$$

d)  
$$
\begin{pmatrix} 
1 & -4 & -1 & 1 \\ 
2 & -8 & 1 & -4 \\ 
-1 & 4 & -2 & 5 
\end{pmatrix} 
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} 
= 
\begin{pmatrix} 3 \\ 9 \\ -6 \end{pmatrix}
$$

$$
x_1 \begin{pmatrix} 1 \\ 2 \\ -1 \end{pmatrix} + 
x_2 \begin{pmatrix} -4 \\ -8 \\ 4 \end{pmatrix} + 
x_3 \begin{pmatrix} -1 \\ 1 \\ -2 \end{pmatrix} + 
x_4 \begin{pmatrix} 1 \\ -4 \\ 5 \end{pmatrix} 
= 
\begin{pmatrix} 3 \\ 9 \\ -6 \end{pmatrix}
$$

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix}
=
\begin{pmatrix} 4x_2 + x_4 + 4 \\ x_2 \\ 2x_4 + 1 \\ x_4 \end{pmatrix}, \forall x_2, x_4 \in \mathbb{R}
$$


e)  
$$
\begin{pmatrix} 
1 & 2 & -1 & 3 \\ 
2 & 4 & -1 & 6 \\ 
0 & 1 & 0 & 2 
\end{pmatrix} 
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} 
= 
\begin{pmatrix} 2 \\ 5 \\ 3 \end{pmatrix}
$$

$$
x_1 \begin{pmatrix} 1 \\ 2 \\ 0 \end{pmatrix} + 
x_2 \begin{pmatrix} 2 \\ 4 \\ 1 \end{pmatrix} + 
x_3 \begin{pmatrix} -1 \\ -1 \\ 0 \end{pmatrix} + 
x_4 \begin{pmatrix} 3 \\ 6 \\ 2 \end{pmatrix} 
= 
\begin{pmatrix} 2 \\ 5 \\ 3 \end{pmatrix}
$$

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} 
= 
\begin{pmatrix} x_4 - 3 \\ 3 - 2x_4 \\ 1 \\ x_4 \end{pmatrix}, \forall x_4 \in \mathbb{R}
$$

f)  
$$
\begin{pmatrix} 
2 & -2 & -1 & 6 & -2 \\ 
1 & -1 & 1 & 2 & -1 \\ 
4 & -4 & 5 & 7 & -1 
\end{pmatrix} 
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \\ x_5 \end{pmatrix} 
= 
\begin{pmatrix} 1 \\ 2 \\ 6 \end{pmatrix}
$$

$$
x_1 \begin{pmatrix} 2 \\ 1 \\ 4 \end{pmatrix} + 
x_2 \begin{pmatrix} -2 \\ -1 \\ -4 \end{pmatrix} + 
x_3 \begin{pmatrix} -1 \\ 1 \\ 5 \end{pmatrix} + 
x_4 \begin{pmatrix} 6 \\ 2 \\ 7 \end{pmatrix} + 
x_5 \begin{pmatrix} -2 \\ -1 \\ -1 \end{pmatrix} 
= 
\begin{pmatrix} 1 \\ 2 \\ 6 \end{pmatrix}
$$

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \\ x_5 \end{pmatrix}
=
\begin{pmatrix} x_2 - 23(x_5 + 1) \\ x_2 \\ 6x_5 + 7 \\ 9(x_5 + 1) \\ x_5 \end{pmatrix}, \forall x_2, x_5 \in \mathbb{R}
$$

g)  
$$
\begin{pmatrix} 
3 & -1 & 1 & -1 & 2 \\ 
1 & -1 & -1 & -2 & -1 \\ 
5 & -2 & 1 & -3 & 3 \\ 
2 & -1 & 0 & -2 & 1 
\end{pmatrix} 
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \\ x_5 \end{pmatrix} 
= 
\begin{pmatrix} 5 \\ 2 \\ 10 \\ 5 \end{pmatrix}
$$

$$
x_1 \begin{pmatrix} 3 \\ 1 \\ 5 \\ 2 \end{pmatrix} + 
x_2 \begin{pmatrix} -1 \\ -1 \\ -2 \\ -1 \end{pmatrix} + 
x_3 \begin{pmatrix} 1 \\ -1 \\ 1 \\ 0 \end{pmatrix} + 
x_4 \begin{pmatrix} -1 \\ -2 \\ -3 \\ -2 \end{pmatrix} + 
x_5 \begin{pmatrix} 2 \\ -1 \\ 3 \\ 1 \end{pmatrix} 
= 
\begin{pmatrix} 5 \\ 2 \\ 10 \\ 5 \end{pmatrix}
$$

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \\ x_5 \end{pmatrix}
=
\begin{pmatrix} 3 - x_3 - 2x_5 \\ 7 - 2x_3 - 5x_5 \\ x_3 \\ x_5 - 3 \\ x_5 \end{pmatrix}, \forall x_3, x_5 \in \mathbb{R}
$$

**Problem 2.2:**
Find all solutions of the vector equation $x_1v_1 + x_2v_2 + x_3v_3 = 0$ where $v_1 = (1, 1, 0)^T$, $v_2 = (0, 1, 1)^T$, and $v_3 = (1, 0, 1)^T$. What conclusion can you make about linear independence of the system of vectors $v_1, v_2, v_3$?
**Solution:**
$$
\begin{pmatrix} 1 & 0 & 1 \\ 1 & 1 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}
$$
and by row reduction,
$$
\equiv \begin{pmatrix} 1 & 0 & 1 \\ 0 & 1 & -1 \\ 0 & 0 & 2 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}
$$
We see that $x_3 = 0$ and so $x_2 = 0, x_1 = 0$. Therefore, the system is linearly independent by definition since all coefficients must be 0. $\blacksquare$

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

### Examples
**Example Title**
**Problem 3.1:**
For what value of b the system,
$$
\begin{pmatrix} 1 & 2 & 2 \\ 2 & 4 & 6 \\ 1 & 2 & 3 \end{pmatrix}x = \begin{pmatrix} 1 \\ 4 \\ b \end{pmatrix}
$$
has a solution. Find the general solution of the system for this value of b.
**Solution:**
First we get to reduced echelon form,
$$
\begin{pmatrix} 1 & 2 & 2 & 1 \\ 2 & 4 & 6 & 4 \\ 1 & 2 & 3 & b \end{pmatrix} = \begin{pmatrix} 1 & 2 & 2 & 1 \\ 0 & 0 & 2 & 2 \\ 0 & 0 & 1 & b - 1 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 2 & 1 \\ 0 & 0 & 1 & 1 \\ 0 & 0 & 0 & b - 2 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 0 & -1 \\ 0 & 0 & 1 & 1 \\ 0 & 0 & 0 & b - 2 \end{pmatrix}
$$
Clearly, $b - 2 = 0$ for the equation to be consistent because a system is inconsistent iff there is a pivot in the last column of an echelon form of the augmented matrix. It follows that $b = 2$. We see immediately that $x_3 = 1$ and $x_1 + 2x_2 = -1$. Thus, our general solution becomes:
$$
\begin{pmatrix} -(2x_2 + 1) \\ x_2 \\ 1 \end{pmatrix}, \forall x_2 \in \mathbb{F}
$$
$\blacksquare$

**Problem 3.2:**
Determine if the vectors,
$$
\begin{pmatrix} 1 \\ 1 \\ 0 \\ 0 \end{pmatrix}, \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ 0 \\ 1 \\ 1 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ 0 \\ 1 \end{pmatrix}
$$
are linearly independent or not. Do these four vectors span $\mathbb{R}^4$? What about $\mathbb{C}^4$?
**Solution:**
By using proposition 3.1, we see that since
$$
\begin {pmatrix} 1 & 1 & 0 & 0 \\ 1 & 0 & 0 & 1 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 1 & 1 \end{pmatrix} \to \begin {pmatrix} 1 & 1 & 0 & 0 \\ 0 & -1 & 0 & 1 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 1 & 1 \end{pmatrix} \to \begin {pmatrix} 1 & 1 & 0 & 0 \\ 0 & -1 & 0 & 1 \\ 0 & 0 & 1 & 1 \\ 0 & 0 & 1 & 1 \end{pmatrix} \to \begin {pmatrix} 1 & 1 & 0 & 0 \\ 0 & -1 & 0 & 1 \\ 0 & 0 & 1 & 1 \\ 0 & 0 & 0 & 0 \end{pmatrix}
$$
the echelon form of the system matrix has no pivot in the last column, it is linearly dependent. In addition, these vectors do not span $\mathbb{R}^4$ or $\mathbb{C}^4$ because the matrix does not have a pivot in every row. $\blacksquare$

**Problem 3.6:**
If the columns of a square $(n \times n)$ matrix A are linearly independent, so are the columns of $A^2$.
**Solution:**
True. Because the columns of A are linearly independent, we know by definition that $Ax = 0$ implies $x = 0$.  Now consider $A^2x = 0$. We can rewrite this as $A(Ax) = 0$. Let $y = Ax$. Then we have $Ay = 0$. But since the columns of A are linearly independent, this forces $y = 0$. Therefore $Ax = 0$. But again, since the columns of A are linearly independent, this forces $x = 0$.  Thus $A^2x = 0$ implies $x = 0$, which means the columns of $A^2$ are linearly independent by definition. $\blacksquare$

**Problem 3.7:**
If the columns of a square $(n \times n)$ matrix A are linearly independent, so are the rows of $A^3$.
**Solution:**
True. Because the columns of A are linearly independent, we know by definition that $Ax = 0$ implies $x = 0$.  By the same reasoning as Problem 3.6, we can show that $A^2x = 0$ implies $x = 0$, and then $A^3x = 0$ implies $x = 0$. Therefore the columns of $A^3$ are linearly independent. Now, $A^3$ is an $n \times n$ square matrix with n linearly independent columns. By proposition 3.1, this means the echelon form of $A^3$ has a pivot in every column, giving us exactly n pivots total. These n pivots must be distributed among the n rows of the echelon form. Since each row can contain at most one pivot (by the definition of echelon form), and we have exactly n pivots across n rows, every row must contain exactly one pivot. Therefore, by proposition 3.1, the rows of $A^3$ are linearly independent. $\blacksquare$

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

### Examples
**Example Title**
**Problem 5.3:**
A linearly independent system of vectors $v_1, v_2, ..., v_n$ in a vector space V is a basis iff $n = dim V$.
**Solution:**
Suppose such a system is a basis. By Proposition 3.4 then every basis must be size n. It follows by definition that $n = dim V$. Now suppose $n = dim V$. By proposition 5.4, the system can be completed to a basis. However, the system is already size $n = dim V$ so it must be a basis already. $\blacksquare$

**Problem 5.5**
Let vectors $u, v, w$ be a basis in V. Show that $u + v + w, v + w, w$ is also a basis in V.
**Solution:**
Since $u, v, w$ is a basis in V, by Proposition 3.4, it must be that $dim V = 3$. For $a, b, c \in \mathbb{F}$, notice the linear combination of $u + v + w, v + w, w$ is $a(u + v + w) + b(v + w) + cw = au + (a + b)v + (a + b + c)w$. This is 0 only when $a = (a + b) = (a + b + c) = 0$ by definition of linear independence of $u, v, w$. Therefore, $u + v + w, v + w, w$ are linearly independent. By Proposition 5.4, any such linearly independent system can be completed to a basis. But the size of the system is already $dim V$ and so no new vectors can be added. Thus, $u + v + w, v + w, w$ is a basis already. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–56
