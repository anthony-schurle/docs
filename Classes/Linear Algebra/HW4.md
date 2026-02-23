**Problem 7.2:**
A $54 \times 37$ matrix has rank 31. What are dimensions of all 4 fundamental subspaces?
**Solution:**
This is simply application of theorem 7.2.
$\text{dim Ran} A = 31$.
$\text{dim Ker} A = 37 - \text{dim Ran} A = 6$.
$\text{dim Ran} A^T = \text{dim Ran} A = 31$.
$\text{dim Ker} A^T = 54 - \text{dim Ran}A^T = 23$.

**Problem 7.3**
Compute rank and find bases of all four fundamental subspaces for the matrices,
$$
\begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 1 & 0 \end{pmatrix},\begin{pmatrix} 1 & 2 & 3 & 1 & 1 \\ 1 & 4 & 0 & 1 & 2 \\ 0 & 2 & -3 & 0 & 1 \\ 1 & 0 & 0 & 0 & 0 \end{pmatrix}
$$
**Solution:**
Most steps follow directly from chapter 2.
a)
Echelon form,
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
which means $\text{dim Ker} A = 1$. Consider the transpose,
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
Suppose $A: X \to Y$ and that V is a subspace of X. Since $V \subseteq X$, we have $AV \subseteq AX = \text{Ran} A$. Therefore, dim AV $\le$ dim (Ran A) = rank A. Now consider AB. Because the matrix product is defined, the image of B must be a subspace of X. We immediately see that $rank(AB) \le rank A$ by the previous reasoning where $\text{dim} A(Img(B)) = rank(AB) \le rank A$. Therefore, $rank(AB) \le rank(A)$. $\blacksquare$

**Problem 7.5**
Prove that if $A: X \to Y$ and V is a subspace of X, then dim AV $\le$ dim V. Deduce that rank(AB) $\le$ rank B.
**Solution:**
Suppose $A: X \to Y$ and V is a subspace of X and let $\{b_1, ..., b_k\}$ where $k = \text{dim} V$ be a basis for V. Consider arbitrary $v \in V$. We see that $v = a_1b_1 + ... + a_{k}b_{k}$ for some scalars $a_1, ..., a_k$. Therefore, $Av = a_1A(b_1) + ...$. Clearly, each vector in the image of V is a linear combination of $A(b_1), ..., A(b_{k})$. Therefore, because $A(b_1), ..., A(b_{k})$ may be linearly dependent, dim AV $\le$ dim V. Consider the product of matrices AB, which implies (because the product is defined) the image of matrix B is a subspace of X. We immediately see by previous reasoning that rank(AB) $\le$ rank B by letting $\text{dim} (A \text{Img}(B)) = \text{rank}(AB) \le \text{rank}(B)$. $\blacksquare$

**Problem 7.6**
Prove that if the product $AB$ of two $n \times n$ matrices is invertible, then both A and B are invertible.
**Solution:**
Suppose AB is invertible. By corollary 6.9, AB's columns form a basis in $\mathbb{F}^n$. It follows that $\text{dim Ran} AB = n$. By problems 7.4 and 7.5, we see that $\text{rank} B \ge n$ and $\text{rank} A \ge n$. But A and B have n columns and so $\text{rank} A \le n$ and $\text{rank} B \le n$. Then $\text{rank} A = \text{rank} B = n$ and so both have columns that form a basis in $\mathbb{F}^n$. Thus, by Corollary 6.9, both A and B are invertible. $\blacksquare$

**Problem 7.7**
Prove that if $Ax = 0$ has unique solution, then the equation $A^Tx = b$ has a solution for every right side b.
**Solution:**
Suppose $Ax = 0$ has unique solution and let A be a $m \times n$ matrix. It follows that $\text{rank} A = n$ because the column vectors are linearly independent and so have a pivot in every column by Proposition 3.1. By theorem 7.1, we see that $\text{rank} A^T = \text{rank} A = n$. Then $A^T$ has a pivot in every row (n rows and n pivots by its rank) and so the column vectors are generating - by proposition 3.1. Therefore, the equation $A^Tx = b$ has a solution for every right side b. $\blacksquare$

**Problem 8.3:**
Find the change of coordinates matrix that changes the coordinates in the basis $1, 1 + t$ in $\mathbb{P}_1$ to the coordinates in the basis $1-t, 2t$.
**Solution:**
Let the first basis be called A and the second called B. Notice,
$$
[I]_{SA} = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, [I]_{SB} = \begin{pmatrix} 1 & 0 \\ -1 & 2 \end{pmatrix}, ([I]_{SB})^{-1} = [I]_{BS} = \begin{pmatrix} 1 & 0 \\ 0.5 & 0.5 \end{pmatrix}
$$
Computations of the inverse:
$$
[I]_{BS} = \begin{pmatrix} 1 & 0 & 1 & 0 \\ -1 & 2 & 0 & 1 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & 1 & 0 \\ 0 & 2 & 1 & 1 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & 1 & 0 \\ 0 & 1 & 0.5 & 0.5 \end{pmatrix}
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
[T]_{NN} = [I]_{NS}[T]_{SS}[I]_{SN} = \begin{pmatrix} 2 & -1 \\ -1 & 1 \end{pmatrix} \begin{pmatrix} 3 & 1 \\ 1 & -2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 2 \end{pmatrix} = \begin{pmatrix} 2 & -1 \\ -1 & 1 \end{pmatrix} \begin{pmatrix} 4 & 5 \\ -1 & -3 \end{pmatrix}
$$
$$
= \begin{pmatrix} 9 & 13 \\ -5 & -8 \end{pmatrix}
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
No, follows directly from problem 8.5 by contrapositive.
$$
\text{trace}\begin{pmatrix} 1 & 3 \\ 2 & 2 \end{pmatrix} = 3 \ne \text{trace} \begin{pmatrix} 0 & 2 \\ 4 & 2 \end{pmatrix} = 2
$$
$\blacksquare$
