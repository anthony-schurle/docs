**Problem 8.2:**
Show that a rotation through $\gamma$ can be represented as a composition of two shear-and-scale transformations,
$$
T_1 = \begin{pmatrix} 1 & 0 \\ sin(\gamma) & cos(\gamma) \end{pmatrix}, T_2 = \begin{pmatrix} sec(\gamma) & -tan(\gamma) \\ 0 & 1 \end{pmatrix}
$$
In what order the transformations should be taken?
**Solution:**
$$
T_2T_1 = \begin{pmatrix} sec(\gamma) & -tan(\gamma) \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 0 \\ sin(\gamma) & cos(\gamma) \end{pmatrix} = \begin{pmatrix} sec(\gamma) - tan(\gamma)sin(\gamma) & -tan(\gamma)cos(\gamma) \\ sin(\gamma) & cos(\gamma) \end{pmatrix}
$$
$$
= \begin{pmatrix} \frac{1 - sin^2(\gamma)}{cos(\gamma)} & -sin(\gamma) \\ sin(\gamma) & cos(\gamma) \end{pmatrix} = \begin{pmatrix} cos(\gamma) & -sin(\gamma) \\ sin(\gamma) & cos(\gamma) \end{pmatrix}
$$
But this is just the rotation through $\gamma$. Therefore, a rotation through $\gamma$ can be represented as a composition of two shear-and-scale transformations $T_2T_1$. $\blacksquare$

**Problem 8.4:**
Write $4 \times 4$ matrix performing perspective projection to $x-y$ plane with center $(d_1, d_2, d_3)^T$.
**Solution:**
This can be represented by the linear transformation to move the center and then applying the projection to the x-y plane before moving it back.
$$
T_f := \begin{pmatrix} 1 & 0 & 0 & -d_1 \\ 0 & 1 & 0 & -d_2 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}, T_b := \begin{pmatrix} 1 & 0 & 0 & d_1 \\ 0 & 1 & 0 & d_2 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}, T_p := \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & \frac{-1}{d_3} & 1 \end{pmatrix}
$$
which gives us the matrix,
$$
T_bT_pT_f = \begin{pmatrix} 1 & 0 & 0 & d_1 \\ 0 & 1 & 0 & d_2 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & \frac{-1}{d_3} & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 & -d_1 \\ 0 & 1 & 0 & -d_2 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}
$$
$$
 = \begin{pmatrix} 1 & 0 & 0 & d_1 \\ 0 & 1 & 0 & d_2 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 & -d_1 \\ 0 & 1 & 0 & -d_2 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & \frac{-1}{d_3} & 1 \end{pmatrix} = \begin{pmatrix} 1 & 0 & \frac{-d_1}{d_3} & 0 \\ 0 & 1 & \frac{-d_2}{d_3} & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & \frac{-1}{d_3} & 1 \end{pmatrix}
$$
$\blacksquare$

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

**Problem 5.3:**
A linearly independent system of vectors $v_1, v_2, ..., v_n$ in a vector space V is a basis iff $n = dim V$.
**Solution:**
Suppose such a system is a basis. By Proposition 3.4 then every basis must be size n. It follows by definition that $n = dim V$. Now suppose $n = dim V$. By proposition 5.4, the system can be completed to a basis. However, the system is already size $n = dim V$ so it must be a basis already. $\blacksquare$

**Problem 5.5**
Let vectors $u, v, w$ be a basis in V. Show that $u + v + w, v + w, w$ is also a basis in V.
**Solution:**
Since $u, v, w$ is a basis in V, by Proposition 3.4, it must be that $dim V = 3$. For $a, b, c \in \mathbb{F}$, notice the linear combination of $u + v + w, v + w, w$ is $a(u + v + w) + b(v + w) + cw = au + (a + b)v + (a + b + c)w$. This is 0 only when $a = (a + b) = (a + b + c) = 0$ by definition of linear independence of $u, v, w$. Therefore, $u + v + w, v + w, w$ are linearly independent. By Proposition 5.4, any such linearly independent system can be completed to a basis. But the size of the system is already $dim V$ and so no new vectors can be added. Thus, $u + v + w, v + w, w$ is a basis already. $\blacksquare$
