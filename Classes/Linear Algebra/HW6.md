**Problem 1.6:**
If A is nilpotent, then $\sigma(A) = \{0\}$.
**Solution:**
Consider arbitrary eigenvalue $\lambda$ such that $Av = \lambda v$ for some non-zero vector v. By definition of nilpotent, $A^k v = \lambda^k v = 0$ which is true iff $\lambda = 0$. Thus, 0 is the unique eigenvalue for A. $\blacksquare$

**Problem 1.7:**
Show that the characteristic polynomial of a block triangular matrix:
$$
\begin{pmatrix} A & * \\ 0 & B \end{pmatrix}
$$

where A and B are square matrices, coincides with det($A - \lambda I$)det($B - \lambda I$). 
**Solution:**
$$
det(\begin{pmatrix} A & * \\ 0 & B \end{pmatrix} - \lambda I) = det(\begin{pmatrix} A - \lambda I & * \\ 0 & B - \lambda I \end{pmatrix})
$$
which by problem 3.11 is,
$$
= det(A - \lambda I)det(B - \lambda I)
$$
$\blacksquare$

**Problem 1.8:**
Let $v_1, v_2, ..., v_n$ be a basis in a vector space V. Assume also that the first k vectors $v_1, v_2, ..., v_k$ of the basis are eigenvectors of an operator A, corresponding to an eigenvalue $\lambda$. Show that in this basis the matrix of the operator A has block triangular form,
$$
\begin{pmatrix} \lambda I_k & * \\ 0 & B \end{pmatrix}
$$

where $I_k$ is the $k \times k$ identity matrix and B is some $(n-k) \times (n-k)$ matrix.
**Solution:**
By assumption, $Av_i = \lambda v_i$ for all $1 \le i \le k$ so that the i-th column of A corresponds to $\lambda v_i$ (where $v_i$ is a basis element and so has $\lambda$ in its i-th row and 0 elsewhere). Meaning A must look like,
$$
\begin{pmatrix} \lambda & 0 & 0 & ... & * & * & ... & * \\ 0 & \lambda & 0 & ... & * & * & ... & * \\ 0 & 0 & \lambda & ... & * & * & ... & * \\ ... & ... & ... & ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & b & b & b & b \\ 0 & 0 & 0 & ... & b & b & b & b \\ ... & ... & ... & ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & b & b & b & b \end{pmatrix}
$$
for some entries * and b which is precisely,
$$
\begin{pmatrix} \lambda I_k & * \\ 0 & B \end{pmatrix}
$$
$\blacksquare$

**Problem 1.9:**
Show that geometric multiplicity of an eigenvalue cannot exceed its algebraic multiplicity.
**Solution:**
Consider arbitrary eigenvalue $\lambda$ for operator A. Let k be its geometric multiplicity, so that there exist k linearly independent eigenvectors. Choose these as the first k vectors of a basis for A. By problem 1.8, the matrix of A takes form,
$$
\begin{pmatrix} \lambda I_k & * \\ 0 & B \end{pmatrix}
$$
for some matrix B and some matrix \*. By problem 1.7, the characteristic polynomial for such a matrix is $det(\lambda I_k - x I) det(B - x I) = (\lambda - x)^k det(B - x I)$. Clearly, $\lambda$ has algebraic multiplicity at least k. Thus, the geometric multiplicity of an eigenvalue cannot exceed its algebraic multiplicity. $\blacksquare$

**Problem 1.10:**
Prove that the determinant of a matrix A is the product of its eigenvalues.
**Solution:**
By definition, the characteristic polynomial $det(A - \lambda I)$ roots are precisely all the eigenvalues for A. Such a polynomial is composed of its complex roots such that $det(A - \lambda I) = (\lambda_1 - \lambda)(\lambda_2 - \lambda)...(\lambda_n - \lambda)$. Setting $\lambda = 0$ shows that $det(A) = \lambda_1 \lambda_2 ... \lambda_n$, where $\lambda_i$ for all $1 \le i \le n$ are the roots of the characteristic polynomial - the eigenvalues for A. $\blacksquare$

**Problem 1.11:**
Prove that the trace of a matrix equals the sum of eigenvalues in three steps.
**Solution:**
By problem 1.10, $det(A - \lambda I) = (\lambda_1 - \lambda) (\lambda_2 - \lambda)...(\lambda_n - \lambda)$. This implies the coefficient of $\lambda^{n-1}$ is $(-1)^{n-1}(\lambda_1 + \lambda_2 + ... + \lambda_n)$. By definition of $D(v_1, v_2, ..., v_n) = \sum_{\sigma \in Perm(n)}a_{\sigma(1),1}a_{\sigma(2),2}...a_{\sigma(n),n} sign(\sigma)$, we see that $det(A - \lambda I) = \sum_{\sigma \in Perm(n)} \prod_{i = 1}^n (A - \lambda I)_{\sigma(i), i} = (a_{1,1} - \lambda)(a_{2,2} - \lambda)...(a_{n,n} - \lambda) + q(\lambda)$ for some polynomial q with at most degree $n-2$ since only the identity permutation carries $\lambda$ in every term and it is impossible to have a permutation with $\lambda$ in only $n-1$ terms. By this equation, we see that the coefficient of $\lambda^{n-1}$ is $(-1)^{n-1}(a_{1,1} + a_{2,2} + ... + a_{n,n})$. But then this means $(-1)^{n-1}(a_{1,1} + a_{2,2} + ... + a_{n,n}) = (-1)^{n-1}(\lambda_1 + \lambda_2 + ... + \lambda_n)$ and so $trace(A) = (\lambda_1 + \lambda_2 + ... + \lambda_n)$. $\blacksquare$


**Problem 2.3:**
Let $A = \begin{pmatrix} 4 & 3 \\ 1 & 2 \end{pmatrix}$. Find $A^{2004}$ by diagonalizing A.
**Solution:**
$det(A - \lambda I) = (4 - \lambda)(2 - \lambda) - 3 = \lambda^2 -6\lambda + 5$. The characteristic polynomial clearly has roots at $\lambda = 1, 5$. Now we check the eigenspaces. First, $\lambda = 1$, $A - I = \begin{pmatrix} 3 & 3 \\ 1 & 1 \end{pmatrix} \to \begin{pmatrix} 1 & 1 \\ 0 & 0 \end{pmatrix}$ and so $Ker(A - I) = span\{\begin{pmatrix} 1 \\ -1 \end{pmatrix}\}$. Next, $\lambda = 5$ so that $A - 5I = \begin{pmatrix} -1 & 3 \\ 1 & -3 \end{pmatrix} \to \begin{pmatrix} -1 & 3 \\ 0 & 0 \end{pmatrix}$ and so $Ker(A - 5I) = span\{\begin{pmatrix} 3 \\ 1 \end{pmatrix}\}$. By Theorem 2.8, A is diagonalizable and so we let, $A = SDS^{-1}$ where $D = \begin{pmatrix} 1 & 0 \\ 0 & 5 \end{pmatrix}$ and $S = \begin{pmatrix} 1 & 3 \\ -1 & 1 \end{pmatrix}$ giving $S^{-1} = \begin{pmatrix} 1 & 3 & 1 & 0 \\ -1 & 1 & 0 & 1 \end{pmatrix} \to \begin{pmatrix} 0 & 4 & 1 & 1 \\ 1 & -1 & 0 & -1 \end{pmatrix} \to \begin{pmatrix} 1 & -1 & 0 & -1 \\ 0 & 1 & 0.25 & 0.25 \end{pmatrix} \to \begin{pmatrix} 1 & 0 & 0.25 & -0.75 \\ 0 & 1 & 0.25 & 0.25 \end{pmatrix}$. Therefore, $A^{2004} = SD^{2004}S^{-1}$ and $D^{2004} = \begin{pmatrix} 1 & 0 \\ 0 & 5^{2004} \end{pmatrix}$ giving 
$$A^{2004} = \begin{pmatrix} 1 & 3 \\ -1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 5^{2004} \end{pmatrix} \begin{pmatrix} 0.25 & -0.75 \\ 0.25 & 0.25 \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ -1 & 1 \end{pmatrix} \begin{pmatrix} 0.25 & -0.75 \\ 0.25(5^{2004}) & (0.25)5^{2004} \end{pmatrix}
$$
$$
= \begin{pmatrix} 0.25 + 0.75(5^{2004}) & -0.75 + 0.75(5^{2004}) \\ -0.25 + 0.25(5^{2004}) & 0.75 + (0.25)5^{2004} \end{pmatrix}
$$
$\blacksquare$

**Problem 2.9:**
Define $\phi$ to be the fibonacci sequence.
a) Find a $2 \times 2$ matrix A such that $\begin{pmatrix} \phi_{n+2} \\ \phi_{n+1} \end{pmatrix} = A\begin{pmatrix} \phi_{n+1} \\ \phi_{n} \end{pmatrix}$.
b) Diagonalize A and find a formula for $A^n$.
c) Noticing that $\begin{pmatrix} \phi_{n+1} \\ \phi_n \end{pmatrix} = A^n \begin{pmatrix} \phi_{1} \\ \phi_0 \end{pmatrix} = A^n \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ find a formula for $\phi_n$.
d) Show that the vector $\begin{pmatrix} \frac{\phi_{n+1}}{\phi_n} \\ 1 \end{pmatrix}$ converges to an eigenvector of A. What do you think, is it a coincidence?
**Solution:**
a)
$A := \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$ so that $A\begin{pmatrix} \phi_{n+1} \\ \phi_{n} \end{pmatrix} = \begin{pmatrix} \phi_{n+1} + \phi_n \\ \phi_{n + 1} \end{pmatrix} = \begin{pmatrix} \phi_{n+2} \\ \phi_{n+1} \end{pmatrix}$.

b)
$det(A - \lambda I) = (1 - \lambda)(-\lambda) - 1 = \lambda^2 - \lambda - 1$ which has roots at $\lambda = \frac{1 \pm \sqrt{5}}{2}$. Now we check eigenspaces. Let $\lambda = 0.5(1 + \sqrt{5})$, so that $A - \lambda I = \begin{pmatrix} 1 - \frac{1 + \sqrt{5}}{2} & 1 \\ 1 & -\frac{1 + \sqrt{5}}{2} \end{pmatrix} \to \begin{pmatrix} \frac{1 - \sqrt{5}}{2} & 1 \\ 0 & 0 \end{pmatrix}$. Therefore, $Ker(A - \lambda I) = span\{\begin{pmatrix} 1 \\ \frac{\sqrt{5} - 1}{2}\end{pmatrix}\}$. Now we let $\lambda = \frac{1 - \sqrt{5}}{2}$. $A - \lambda I = \begin{pmatrix} \frac{1 + \sqrt{5}}{2} & 1 \\ 1 & 1 - \frac{1 + \sqrt{5}}{2} \end{pmatrix} \to \begin{pmatrix} \frac{1 + \sqrt{5}}{2} & 1 \\ 0 & 0 \end{pmatrix}$ so that $Ker(A - \lambda I) = span\{\begin{pmatrix} \frac{1 - \sqrt{5}}{2} \\ 1 \end{pmatrix}\}$. It follows that $A = SDS^{-1}$ by Theorem 2.8 where:
$$
D = \begin{pmatrix} \frac{1 + \sqrt{5}}{2} & 0 \\ 0 & \frac{1 - \sqrt{5}}{2} \end{pmatrix}, S = \begin{pmatrix} \frac{1 + \sqrt{5}}{2} & \frac{1 - \sqrt{5}}{2} \\ 1 & 1 \end{pmatrix}
$$
and so,
$$
S^{-1} = \frac{1}{\sqrt{5}}\begin{pmatrix} 1 & \frac{\sqrt{5} - 1}{2} \\ -1 & \frac{1 + \sqrt{5}}{2} \end{pmatrix}
$$
Thus,
$$
A^n = \begin{pmatrix} \frac{1 + \sqrt{5}}{2} & \frac{1 - \sqrt{5}}{2} \\ 1 & 1 \end{pmatrix} \begin{pmatrix} \frac{1 + \sqrt{5}}{2}^n & 0 \\ 0 & \frac{1 - \sqrt{5}}{2}^n \end{pmatrix} \frac{1}{\sqrt{5}}\begin{pmatrix} 1 & \frac{\sqrt{5} - 1}{2} \\ -1 & \frac{1 + \sqrt{5}}{2} \end{pmatrix}
$$

c)
$\begin{pmatrix} \phi_{n+1} \\ \phi_n \end{pmatrix} = \frac{1}{\sqrt{5}} \begin{pmatrix} \frac{1 + \sqrt{5}}{2} & \frac{1 - \sqrt{5}}{2} \\ 1 & 1 \end{pmatrix} \begin{pmatrix} \frac{1 + \sqrt{5}}{2}^n \\ -(\frac{1 - \sqrt{5}}{2})^n \end{pmatrix}$ and reading the second row shows, $\phi_n = \frac{1}{\sqrt{5}}((\frac{1 + \sqrt{5}}{2}^n) - \frac{1 - \sqrt{5}}{2}^n)$.

d)
$$
\frac{\phi_{n+1}}{\phi_n} = \frac{(\frac{1 + \sqrt{5}}{2})^{n+1} - (\frac{1 - \sqrt{5}}{2})^{n+1}}{(\frac{1 + \sqrt{5}}{2})^{n} - (\frac{1 - \sqrt{5}}{2})^{n}}
$$
and since $|\frac{1 - \sqrt{5}}{2}| < 1$, we have $\frac{1 - \sqrt{5}}{2}^n \to 0$ as $n \to \infty$. Then as $n \to \infty$, $\frac{\phi_{n+1}}{\phi_n} \to \frac{1 + \sqrt{5}}{2}$. Therefore, $\begin{pmatrix} \frac{\phi_{n+1}}{\phi_n} \\ 1 \end{pmatrix} \to \begin{pmatrix} \frac{1 + \sqrt{5}}{2} \\ 1 \end{pmatrix}$ which is precisely the eigenvector of A. This does not seem like a coincidence, repeated multiplication by A amplifies the larger eigenvalue. $\blacksquare$

**Problem 2.10:**
Let A be a $5 \times 5$ matrix with 3 distinct eigenvalues. Suppose we know that one eigenspace is 3D. Can you say if A is diagonalizable?
**Solution:**
By definition of eigenvalues, geometric and algebraic multiplicity is at least 1. Total algebraic multiplicity of all eigenvalues can not exceed 5 in a $5 \times 5$ matrix. By problem 1.9, since it is assumed some eigenvalue p has geometric multiplicity 3, it must also have algebraic multiplicity at least 3. But the other two eigenvalues have at least algebraic multiplicity 1, so it must be that p has exactly algebraic multiplicity 3. It follows that the other eigenvalues must have exactly algebraic multiplicity 1, and so geometric multiplicity 1 by problem 1.9. Thus, by theorem 2.8, A is diagonalizable. $\blacksquare$

**Problem 2.13:**
Eigenvalues of a transposition:
a)
Consider the transformation T in the space $M_{2\times 2}$ of $2 \times 2$ matrices, $T(A) = A^T$. Find all its eigenvalues and eigenvectors. Is it possible to diagonalize this transformation?
b)
Can you do the same problem but in the space of $n \times n$ matrices?
**Solution:**
a)
We need $A^T = \lambda A$ and so,
$$
A = \lambda A^T = \lambda^2 A
$$
giving $\lambda^2 = 1$ and so $\lambda = \pm 1$. Consider $\lambda = 1$, $A^T = A$. A basis for symmetric matrices is:
$$
\begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}, \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}, \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}
$$
so the corresponding eigenspace is 3D. Consider $\lambda = -1$, where $A^T = -A$. A basis for such an eigenspace is:
$$
\begin{pmatrix} 0 & 1 \\ -1 & 0 \end{pmatrix}
$$
so the corresponding eigenspace is 1D. By Theorem 2.2, the eigenspaces are linearly independent so that by Lemma 2.7 - their union of basis elements is linearly independent. This union has exactly dimension $4$ vectors, which is $dim(M_{2\times 2})$. Thus, by Theorem 2.1, A is diagonalizable. $\blacksquare$


b)
Eigenvalues remained unchanged by the same reasoning as part a. Consider $\lambda = 1$, where $A^T = A$. A basis for arbitrary symmetric n by n matrices are the diagonal matrices where only $a_{i,i} = 1$ for $1 \le i \le n$ and every other entry is 0, totaling n matrices, and the symmetric off-diagonal where $a_{i,j} = a_{j,i}$ for all i and j not equal. This totals $0.5n(n-1)$ matrices giving a total basis dimension of $\frac{n(n+1)}{2}$. Consider $\lambda = -1$, where $A^T = -A$. This consists of all matrices where $a_{i,j} = -a_{j,i}$ and so has basis dimension $\frac{n(n-1)}{2}$. By Theorem 2.2, the eigenspaces are linearly independent so that by Lemma 2.7 - their union of basis elements is linearly independent. This union has exactly dimension $\frac{n(n+1)}{2} + \frac{n(n-1)}{2} = n^2$ vectors, which is $dim(M_{n\times n})$. Thus, by Theorem 2.1, A is diagonalizable. $\blacksquare$
