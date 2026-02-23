1) *
Let V , W, and U be vector spaces of dimension m, n and k respectively. Let A and B be linear transformations with B : V −→ W, and A : W −→ U Show that rank(B) − rank(AB) = nullity(AB) − nullity(B). Here the nullity of a linear transformation is the dimension of its kernel.

Theorem 7.2 is shows,
$$
\text{rank} B = m - \text{null} B \land -\text{rank} AB = \text{null} AB - m
$$
so that $\text{rank} B - \text{rank} AB = \text{null} AB - \text{null} B$. $\blacksquare$

2)
Exhibit all 3 × 3 matrices which rotates the xz plane by 45 degrees and which does not change the y coordinate. Hint: You could rotate the xZ plane clockwise or counterclockwise.

$$
\begin{pmatrix} \cos{45} & 0 & -\sin{45} \\ 0 & 1 & 0 \\ \sin{45} & 0 & \cos{45} \end{pmatrix} = \begin{pmatrix} \frac{\sqrt{2}}{2} & 0 & \frac{-\sqrt{2}}{2} \\ 0 & 1 & 0 \\ \frac{\sqrt{2}}{2} & 0 & \frac{\sqrt{2}}{2} \end{pmatrix}, \begin{pmatrix} \cos{45} & 0 & \sin{45} \\ 0 & 1 & 0 \\ -\sin{45} & 0 & \cos{45} \end{pmatrix} = \begin{pmatrix} \frac{\sqrt{2}}{2} & 0 & \frac{\sqrt{2}}{2} \\ 0 & 1 & 0 \\ \frac{-\sqrt{2}}{2} & 0 & \frac{\sqrt{2}}{2} \end{pmatrix}
$$
$\blacksquare$

3) *
Suppose that A and B are matrices with the product AB defined. Suppose that AB is invertible. Show that A is right invertible and that B is left invertible.

$AB(AB)^{-1} = I \implies A(B(AB)^{-1}) = I$ and so A is right invertible. $(AB)^{-1}AB = ((AB)^{-1}A)B = I$ and so B is left invertible. $\blacksquare$

4)
Let A be an invertible matrix which is symmetric, meaning that $A = A^T$ . Prove that $A^{-1}$ is symmetric.

$A^{-1} = (A^T)^{-1} = (A^{-1})^T$ by theorem 6.5 and so $A^{-1}$ is symmetric. $\blacksquare$

5)
What is the smallest subspace of the vector space of 4 × 4 matrices over the real numbers which contains all of the symmetric matrices and all of the upper triangular matrices. We say that a matrix is upper triangular if aj,k = 0 whenever j > k.

Represented by the span of,
$$
\{ \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}, \begin{pmatrix} 0 & 1 & 0 & 0 \\ 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}
$$
$$
\begin{pmatrix} 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \\ 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 1 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix}
$$
$$
\begin{pmatrix} 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix},
$$

$$
\begin{pmatrix} 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \end{pmatrix} \}
$$
which is exactly the vector space of all $4 \times 4$ matrices.
$\blacksquare$

6) *
Prove or disprove: If the columns of a square matrix A are linearly independent so are the rows of the matrix $A^3 = AAA$.

Pick arbitrary vector x and consider $A^3(x) = 0$. Let $y = A(A(x))$. Because A is linearly independent, we see $y = 0$ and so $A(A(x)) = 0$. Similarly, $A(x) = 0$ and so finally $x = 0$ which means $A^3$ is linearly independent. But A is square so then full pivots in all columns implies full pivots in every row and so the rows of $A^3$ are linearly independent. $\blacksquare$

7)
Let ~u, ~v, ~w be a basis for a vector space V . Show that ~u, ~u + ~v, and ~u + ~v + ~w are also a basis for V .

Consider the linear combination,
$$
au + b(u + v) + c(u + v + w) = 0 \implies (a + b + c)u + (b + c)v + cw = 0
$$
which is only true when $(a + b + c) = (b + c) = c = 0$ because u, v, and w are a basis of V. it follows that this forces $a = b = c = 0$ and so u, u + v, u + v + w are linearly independent vectors of V. But u, v, and w are a basis so any basis of V must have dimension 3 making u, u + v, u + v + w also a basis because they are linearly independent vectors. $\blacksquare$

8)
What is the dimension of the largest subspace of 4 × 4 real matrices so that the trace of the 3 × 3 matrix of the first three rows of the first three columns is zero and the trace of the 3 × 3 matrix of the last 3 rows of the the last 3 columns is zero.

The off-diagonal entries are unconstrained giving 12 free parameters, and the two independent trace constraints on the 4 diagonal entries reduce their contribution from 4 to 2, giving 14 total. $\blacksquare$

9) *
Is ir possible for a real matrix A that the range of A is the kernel of AT ? Is it possible for a complex matrix.

For reals, it is not possible. If the range of A is the kernel of $A^T$, then $A^TA = 0$. But this implies $A = 0$ because the diagonal entries of $A^TA$ are sums of squares of real entries of A. Since $A = 0$, we see that range(A) $= \{0\}$ and ker ($A^T$) $= \mathbb{R}^m$ which have different dimensions unless m = 0. Therefore, we have a contradiction.

For complex yes, define $A := \begin{pmatrix} 1 & i \\ i & -1 \end{pmatrix}\begin{pmatrix} a + bi \\ c + di \end{pmatrix} = \begin{pmatrix} (a -d) + (b + c)i \\ -(b + c) + (a - d)i \end{pmatrix}$ so that $A \begin{pmatrix} a + bi \\ c + di \end{pmatrix} = \begin{pmatrix} (a -d) + (b + c)i \\ -(b + c) + (a - d)i \end{pmatrix}$ and $A^T\begin{pmatrix} (a -d) + (b + c)i \\ -(b + c) + (a - d)i \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$ which shows the range of A and kernel of $A^T$ are the same because range of A is contained in the kernel of $A^T$ and both of their dimensions are 1 by theorem 7.2. $\blacksquare$

10)
Prove that if A and B are similar matrices then the trace of A is equal to the trace of B.

By definition, $A = Q^{-1}BQ$. It follows that $trace(A) = trace(Q^{-1}BQ) = trace(QQ^{-1}B) = trace(B)$.  $\blacksquare$