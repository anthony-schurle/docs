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

### Examples
**Example Title**
**Problem 7.2:**
A $54 \times 37$ matrix has rank 31. What are dimensions of all 4 fundamental subspaces?
**Solution:**
This is simply application of theorem 72.
$\text{dim Ran} A = 31$.
$\text{dim Ker} A = 37 - 31 = 6$.
$\text{dim Ran} A^T = 31$.
$\text{dim Ker} A^T = 54 - 31 = 23$.

**Problem 7.3**
Compute rank and find bases of all four fundamental subspaces for the matrices,
$$
\begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 1 & 0 \end{pmatrix},\begin{pmatrix} 1 & 2 & 3 & 1 & 1 \\ 1 & 4 & 0 & 1 & 2 \\ 0 & 2 & -3 & 0 & 1 \\ 1 & 0 & 0 & 0 & 0 \end{pmatrix}
$$
**Solution:**
a)
Reduced echelon form,
$$
\begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 1 & 0 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & -1 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{pmatrix}
$$
We see that $\text{dim Ran}A^T = 2$ given by the basis:
$$
\begin{pmatrix} 1 \\ 0 \\ -1 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix}
$$
We also see that $\text{dim Ran} A = 2$ given by the basis:
$$
\begin{pmatrix} 1 \\ 0 \\ 1 \end{pmatrix}, \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}
$$
Solving the matrix for 0 gives the solution basis:
$$
\begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}
$$
which means $\text{dim Ker} A = 1$ (This is ok because the resulting matrix is 0 which is not effected by row operations). Consider the transpose,
$$
\begin{pmatrix} 1 & 0 & 1 \\ 1 & 1 & 1 \\ 0 & 1 & 0 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 0 & 1 & 0 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{pmatrix}
$$
and solving for solutions of 0 gives the kernel basis of the transpose,
$$
\begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix}
$$
and so $\text{dim Ker} A^T = 1$.

b)
Reduced echelon form,
$$
\begin{pmatrix} 1 & 2 & 3 & 1 & 1 \\ 1 & 4 & 0 & 1 & 2 \\ 0 & 2 & -3 & 0 & 1 \\ 1 & 0 & 0 & 0 & 0 \end{pmatrix} \to \begin{pmatrix} 1 & 2 & 3 & 1 & 1 \\ 0 & 2 & -3 & 0 & 1 \\ 0 & 2 & -3 & 0 & 1 \\ 0 & -2 & -3 & -1 & -1 \end{pmatrix} \to \begin{pmatrix} 1 & 2 & 3 & 1 & 1 \\ 0 & 2 & -3 & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & -6 & -1 & 0 \end{pmatrix}
$$
$$
\to \begin{pmatrix} 1 & 2 & 3 & 1 & 1 \\ 0 & 1 & -1.5 & 0 & 0.5 \\ 0 & 0 & 1 & \frac{1}{6} & 0 \\ 0 & 0 & 0 & 0 & 0 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & 6 & 1 & 0 \\ 0 & 1 & -1.5 & 0 & 0.5 \\ 0 & 0 & 1 & \frac{1}{6} & 0 \\ 0 & 0 & 0 & 0 & 0 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0.25 & 0.5 \\ 0 & 0 & 1 & \frac{1}{6} & 0 \\ 0 & 0 & 0 & 0 & 0 \end{pmatrix}
$$
We see that $\text{dim Ran} A^T = 3$ given by the basis:
$$
\begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ 0 \\ 0.25 \\ 0.5 \end{pmatrix}, \begin{pmatrix} 0 \\ 0 \\ 1 \\ \frac{1}{6} \\ 0 \end{pmatrix}
$$
We also see that $\text{dim Ran} A = 3$ given by the basis:
$$
\begin{pmatrix} 1 \\ 1 \\ 0 \\ 1 \end{pmatrix}, \begin{pmatrix} 2 \\ 4 \\ 2 \\ 0 \end{pmatrix}, \begin{pmatrix} 3 \\ 0 \\ -3 \\ 0 \end{pmatrix}
$$
Solving the matrix for 0 gives the solution basis:
$$
\begin{pmatrix} 0 \\ -0.25 \\ \frac{-1}{6} \\ 1 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ -0.5 \\ 0 \\ 0 \\ 1 \end{pmatrix}
$$
which means $\text{dim Ker} A = 2$. Consider the transpose,
$$
\begin{pmatrix} 1 & 1 & 0 & 1 \\ 2 & 4 & 2 & 0 \\ 3 & 0 & -3 & 0 \\ 1 & 1 & 0 & 0 \\ 1 & 2 & 1 & 0 \end{pmatrix} \to \begin{pmatrix} 1 & 1 & 0 & 1 \\ 0 & 2 & 2 & -2 \\ 0 & -3 & -3 & -3 \\ 0 & 0 & 0 & -1 \\ 0 & 1 & 1 & -1 \end{pmatrix} \to \begin{pmatrix} 1 & 1 & 0 & 1 \\ 0 & 1 & 1 & -1 \\ 0 & 1 & 1 & 1 \\ 0 & 0 & 0 & 1 \\ 0 & 1 & 1 & -1 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & -1 & 2 \\ 0 & 1 & 1 & -1 \\ 0 & 0 & 0 & 2 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \end{pmatrix} 
$$
$$
\to \begin{pmatrix} 1 & 0 & -1 & 2 \\ 0 & 1 & 1 & -1 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & -1 & 0 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix} 
$$
and solving for solutions of 0 gives the transpose kernel basis:
$$
\begin{pmatrix} 1 \\ -1 \\ 1 \\ 0 \end{pmatrix}
$$
and so $\text{dim Ker} A^T = 1$.

**Problem 7.4**
Prove that if $A: X \to Y$ and V is a subspace of X then dim AV $\le$ rank A. ($AV := \{Av : v \in V\}$) Deduce that rank(AB) $\le$ rank A.
**Solution:**
Suppose $A: X \to Y$ and that V is a subspace of X. For the sake of contradiction, suppose $\text{dim} AV > \text{rank} A$. Since $\text{dim} AX \ge \text{dim} AV$ because $V \subseteq X$ and the basis of V is linearly independent in X and so can be extended to form a basis for X, we see that $\text{dim} AX > \text{rank}A$ which is a contradiction by definition of the transformation. Therefore,  if $A: X \to Y$ and V is a subspace of X then dim AV $\le$ rank A. Now consider AB. Because the matrix product is defined, the image of B must be X itself or a subspace. If a subspace, we immediately see that $rank(AB) \le rank A$ by the previous reasoning. If X itself, then it immediately follows that $rank(AB) = rank A$. Therefore, $rank(AB) \le rank(A)$. $\blacksquare$

**Problem 7.5**
Prove that if $A: X \to Y$ and V is a subspace of X, then dim AV $\le$ dim V. Deduce that rank(AB) $\le$ rank B.
**Solution:**
Suppose $A: X \to Y$ and V is a subspace of X. For the sake of contradiction, suppose $\text{dim} AV > \text{dim} V$.

**Problem 7.6**
Prove that if the product $AB$ of two $n \times n$ matrices is invertible, then both A and B are invertible.
**Solution:**
Suppose AB is invertible. By corollary 6.9, AB's columns form a basis in $\mathbb{F}^n$. It follows that $\text{dim Ran} AB = n$. By problems 7.4 and 7.5, we see that $\text{rank} B \ge n$ and $\text{rank} A \ge n$. But A and B have n columns and so $\text{rank} A \le n$ and $\text{rank} B \le n$. Then $\text{rank} A = \text{rank} B = n$ and so both have columns that form a basis in $\mathbb{F}^n$. Thus, by Corollary 6.9, both A and B are invertible. $\blacksquare$

**Problem 7.7**
Prove that if $Ax = 0$ has unique solution, then the equation $A^Tx = b$ has a solution for every right side b.
**Solution:**
Suppose $Ax = 0$ has unique solution and let A be a $m \times n$ matrix. It follows that $\text{dim Ker} A = 0$ because the column vectors are linearly independent. It must also be that $n \ge m$, or there would be less pivots than columns - only one pivot per row - which would contradict $\text{dim Ker} A = 0$. By theorem 7.1 and theorem 7.2, we see that $\text{rank} A^T = \text{rank} A = n$. But $A^T$ only has m columns so $n \le m$, giving $n = m$. Then $A^T$ has a pivot in every row too and so the column vectors are also generating - by proposition 3.1. Therefore, the equation $A^Tx = b$ has a solution for every right side b. $\blacksquare$

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

### Examples
**Example Title**
**Problem 8.3:**
Find the change of coordinates matrix that changes the coordinates in the basis $1, 1 + t$ in $\mathbb{P}_1$ to the coordinates in the basis $1-t, 2t$.
**Solution:**
Let the first basis be called A and the second called B. Notice,
$$
[I]_{SA} = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, [I]_{SB} = \begin{pmatrix} 1 & 0 \\ -1 & 2 \end{pmatrix}, ([I]_{SB})^{-1} = [I]_{BS} = \begin{pmatrix} 1 & 0 \\ 0.5 & 0.5 \end{pmatrix}
$$
and so we see that,
$$
[I]_{BA} = [I]_{BS}[I]_{SA} = \begin{pmatrix} 1 & 0 \\ 0.5 & 0.5 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 0.5 & 1 \end{pmatrix}
$$
$\blacksquare$

**Problem 8.4**:
Let T be the linear operator in $\mathbb{F}^2$ defined by $T\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 3x + y \\ x - 2y \end{pmatrix}$. Find the matrix of T in the standard basis and in the basis: $(1, 1)^T, (1,2)^T$.
**Solution:**
Standard basis -
$$
T(e_1) = \begin{pmatrix} 3 \\ 1 \end{pmatrix}, T(e_2) = \begin{pmatrix} 1 \\ -2 \end{pmatrix}, [T]_{SS} = \begin{pmatrix} 3 & 1 \\ 1 & -2 \end{pmatrix}
$$
New basis (N) -
$$
[I]_{SN} = \begin{pmatrix} 1 & 1 \\ 1 & 2 \end{pmatrix}, [I]_{NS} = \begin{pmatrix} 2 & -1 \\ -1 & 1 \end{pmatrix}
$$
$$
[T]_{NN} = [I]_{NS}[T]_{SS}[I]_{SN} = \begin{pmatrix} 2 & -1 \\ -1 & 1 \end{pmatrix} \begin{pmatrix} 3 & 1 \\ 1 & -2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 2 \end{pmatrix} = \begin{pmatrix} 9 & 13 \\ -5 & -8 \end{pmatrix}
$$
$\blacksquare$

**Problem 8.5**
If A and B are similar matrices then trace A = trace B.
**Solution:**
Suppose A and B are similar matrices. It follows that for some matrix Q,
$$
A = Q^{-1}BQ, B = QAQ^{-1}
$$
We see then that $\text{trace} A = \text{trace} (Q^{-1}B)Q, \text{trace} B = \text{trace} Q(AQ^{-1})$. But notice $AQ^{-1} = Q^{-1}BQQ^{-1} = Q^{-1}B$. It follows that because $\text{trace} (XY) = \text{trace}(YX)$ for any matrices X and Y, trace A = trace B. $\blacksquare$

**Problem 8.6**
Are the matrices $\begin{pmatrix} 1 & 3 \\ 2 & 2 \end{pmatrix} \land \begin{pmatrix} 0 & 2 \\ 4 & 2 \end{pmatrix}$ similar?
**Solution:**
No, follows directly from problem 8.5. $\blacksquare$

### References
- *Book Title* — Chapter X, Pages Y–73
