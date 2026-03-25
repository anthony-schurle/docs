**Problem 3.5:**
A square matrix is called nilpotent if $A^k = 0$ for some positive integer k. Show that for a nilpotent matrix A $det A = 0$.
**Solution:**
Suppose A is nilpotent for some positive integer k. It suffices to show that the columns of A are linearly dependent, and so A is not invertible, because of proposition 3.3. For the sake of contradiction, suppose A was linearly independent in its columns. We see that $A^k x = 0$ for all x and so $A(A^{k-1}x) = 0$. This implies $A^{k-1}x = 0$ since A is linearly independent in its columns. This then implies $A(A^{k-2}x) = 0$ so that $A^{k-2}x = 0$. Continuing this process gets $Ax = 0$ for all x. This is a contradiction of A being linearly independent. Thus, A is linearly dependent in its columns. $\blacksquare$

**Problem 3.6**
Prove that if the matrices A and B are similar, then $det A = det B$.
**Solution:**
By definition of similar matrices, $A = Q^{-1}BQ$ for some matrix Q. By theorem 3.5, $det(A) = det(Q^{-1}BQ) = det(Q^{-1})det(BQ) = det(BQ)det(Q^{-1}) = det(BQQ^{-1}) = det(BI) = det(B)$. $\blacksquare$

**Problem 3.8**
Show that $\begin{vmatrix} 1 & x & x^2 \\ 1 & y & y^2 \\ 1 & z & z^2 \end{vmatrix} = (z - x)(z - y)(y - x)$. This is a particular case of the Vandermonde determinant.
**Solution:**
By theorem 3.5 and because,
$$
\begin{pmatrix} 1 & x & x^2 \\ 0 & 1 & y + x \\ 0 & 0 & z - y \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & -1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & \frac{1}{z - x} \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 \\ 0 & \frac{1}{y - x} & 0 \\ 0 & 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -1 & 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 \\ -1 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & x & x^2 \\ 1 & y & y^2 \\ 1 & z & z^2 \end{pmatrix}
$$
we see that:
$$
\begin{vmatrix} 1 & x & x^2 \\ 0 & 1 & y + x \\ 0 & 0 & z - y \end{vmatrix} = \begin{vmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & -1 & 1 \end{vmatrix} \begin{vmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & \frac{1}{z - x} \end{vmatrix} \begin{vmatrix} 1 & 0 & 0 \\ 0 & \frac{1}{y - x} & 0 \\ 0 & 0 & 1 \end{vmatrix} \begin{vmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -1 & 0 & 1 \end{vmatrix} \begin{vmatrix} 1 & 0 & 0 \\ -1 & 1 & 0 \\ 0 & 0 & 1 \end{vmatrix} \begin{vmatrix} 1 & x & x^2 \\ 1 & y & y^2 \\ 1 & z & z^2 \end{vmatrix}
$$
$$
\implies z - y = (1)(\frac{1}{z - x})(\frac{1}{y - x})(1)(1)\begin{vmatrix} 1 & x & x^2 \\ 1 & y & y^2 \\ 1 & z & z^2 \end{vmatrix}
$$
$$
\implies (z - y)(z - x)(y - x) = \begin{vmatrix} 1 & x & x^2 \\ 1 & y & y^2 \\ 1 & z & z^2 \end{vmatrix}
$$
If $z - y$, $z - x$, or $y - x$ are 0 then the matrix is not invertible and so both sides are 0. $\blacksquare$

**Problem 3.12**
Let A be $m \times n$ and B be $n \times m$ matrices. Prove that $\begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} = det(AB)$.
**Solution:**
By theorem 3.5,
$$
\begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} \begin{vmatrix} I & 0 \\ B & I \end{vmatrix} = \begin{vmatrix} AB & A \\ 0 & I \end{vmatrix}
$$
By problem 3.11 and theorem 3.4 this implies,
$$
\begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} \begin{vmatrix} I & B \\ 0 & I \end{vmatrix} = det(AB)det(I)
$$
and so,
$$
\begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} det(I)^2 = det(AB) \implies \begin{vmatrix} 0 & A \\ -B & I \end{vmatrix} = det(AB)
$$
$\blacksquare$

**Problem 4.3:**
Why is there an even number of permutations of (1, 2, . . . , 9) and why are
exactly half of them odd permutations? Hint: This problem can be hard to solve
in terms of permutations, but there is a very simple solution using determinants.
**Solution:**
There are $9! = 9 * 8 * 7 * 6 * 5 * 4 * 3 * 2 * 1 = 362880$ permutations. Notice this is even because 2 is a factor. Now consider the $9 \times 9$ matrix where every entry is 1 and its corresponding determinant 0 (two columns are identitical). We see that $0 = \sum_{\sigma \in Perm(9)}a_{\sigma(1),1}a_{\sigma(2),2}...a_{\sigma(9),9} sign(\sigma)$. But every entry is 1 so this simplifies to $0 = \sum_{\sigma \in Perm(9)} sign(\sigma)$. Because odd permutations have negative sign this becomes $0 = \text{\# even permutations} - \text{\# odd permutations}$ which indicates there are equal even permutations to odd permutations. In other words, odd permutations make up half the permutation count of (1, 2, ..., 9). $\blacksquare$

**Problem 4.4:**
If $\sigma$ is an odd permutation, explain why $\sigma^2$ is even but $\sigma^{-1}$ is odd.
**Solution:**
Suppose $\sigma$ is an odd permutation. Then it takes $2k + 1$ elementary transposes to get to permutation $\sigma$ for some k. It follows that it takes an additional $2k + 1$ elementary transposes to get from $\sigma$ to permutation $\sigma^2$. So, to get to permutation $\sigma^2$ is requires $2(2k + 1)$ elementary transposes which is even. Thus, $\sigma^2$ has the same sign as the original tuple - trivially even because requires 0 transposes - and so is an even permutation. Notice $\sigma^2(\sigma^{-1}) = \sigma$ and so it takes an even number of elementary transposes to reach $\sigma$ from $\sigma^{-1}$ which means both have the same sign. Therefore, since $\sigma$ is odd, $\sigma^{-1}$ is an odd permutation. $\blacksquare$

**Problem 5.4:**
Using cofactor formula compute inverses of the matrices,
$$
A := \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}, B := \begin{pmatrix} 19 & -17 \\ 3 & -2 \end{pmatrix}, D := \begin{pmatrix} 1 & 0 \\ 3 & 5 \end{pmatrix}, E := \begin{pmatrix} 1 & 1 & 0 \\ 2 & 1 & 2 \\ 0 & 1 & 1 \end{pmatrix}
$$
**Solution:**
A)
$$
C_{1,1} = (1)(4) = 4, C_{1,2} = (-1)(3) = -3, C_{2,1} = (-1)(2) = -2, C_{2,2} = (1)(1) = 1
$$
so that,
$$
C = \begin{pmatrix} 4 & -3 \\ -2 & 1 \end{pmatrix} \implies C^T = \begin{pmatrix} 4 & -2 \\ -3 & 1 \end{pmatrix}
$$
It follows that,
$$
det(A) = \sum_{k = 1}^2 a_{1, k}C_{1, k} = 4 - 6 = -2
$$
Finally,
$$
A^{-1} = \frac{1}{det(A)}C^T = \begin{pmatrix} -2 & 1 \\ 1.5 & -0.5 \end{pmatrix}
$$

B)
$$
C_{1,1} = (1)(-2) = -2, C_{1,2} = (-1)(3) = -3, C_{2,1} = (-1)(-17) = 17, C_{2,2} = (1)(19) = 19
$$
so that,
$$
C = \begin{pmatrix} -2 & -3 \\ 17 & 19 \end{pmatrix} \implies C^T = \begin{pmatrix} -2 & 17 \\ -3 & 19 \end{pmatrix}
$$
It follows that,
$$
det(B) = \sum_{k = 1}^2 b_{1, k}C_{1, k} = -38 + 51 = 13
$$
Finally,
$$
B^{-1} = \frac{1}{det(B)}C^T = \begin{pmatrix} \frac{-2}{13} & \frac{17}{13} \\ \frac{-3}{13} & \frac{19}{13} \end{pmatrix}
$$

D)
$$
C_{1,1} = (1)(5) = 5, C_{1,2} = (-1)(3) = -3, C_{2,1} = (-1)(0) = 0, C_{2,2} = (1)(1) = 1
$$
so that,
$$
C = \begin{pmatrix} 5 & -3 \\ 0 & 1 \end{pmatrix} \implies C^T = \begin{pmatrix} 5 & 0 \\ -3 & 1 \end{pmatrix}
$$
It follows that,
$$
det(D) = \sum_{k = 1}^2 d_{1, k}C_{1, k} = 5
$$
Finally,
$$
D^{-1} = \frac{1}{det(D)}C^T = \begin{pmatrix} 1 & 0 \\ \frac{-3}{5} & \frac{1}{5} \end{pmatrix}
$$

E)
$$
C_{1,1} = (1)(1 - 2) = -1, C_{1,2} = (-1)(2 - 0) = -2, C_{1, 3} = (1)(2 - 0) = 2
$$
$$
C_{2,1} = (-1)(1 - 0) = -1, C_{2,2} = (1)(1 - 0) = 1, C_{2, 3} = (-1)(1 - 0) = -1
$$
$$
C_{3, 1} = (1)(2 - 0) = 2, C_{3, 2} = (-1)(2 - 0) = -2, C_{3, 3} = (1)(1 - 2) = -1
$$
so that,
$$
C = \begin{pmatrix} -1 & -2 & 2 \\ -1 & 1 & -1 \\ 2 & -2 & -1 \end{pmatrix} \implies C^T = \begin{pmatrix} -1 & -1 & 2 \\ -2 & 1 & -2 \\ 2 & -1 & -1 \end{pmatrix}
$$
It follows that,
$$
det(E) = \sum_{k = 1}^3 e_{1, k}C_{1, k} = -1 - 2 = -3
$$
Finally,
$$
E^{-1} = \frac{1}{det(E)}C^T = \begin{pmatrix} \frac{1}{3} & \frac{1}{3} & \frac{-2}{3} \\ \frac{2}{3} & \frac{-1}{3} & \frac{2}{3} \\ \frac{-2}{3} & \frac{1}{3} & \frac{1}{3} \end{pmatrix}
$$
$\blacksquare$

**Problem 5.6:**
Vandermonde determinant revisited. Our goal is to prove the formula,
$$
\begin{vmatrix} 1 & c_0 & c_0^2 & ... & c_0^n \\ 1 & c_1 & c_1^2 & ... & c_1^n \\ ... & ... & ... & ... & ... \\ 1 & c_n & c_n^2 & ... & c_n^n \end{vmatrix} = \prod_{0 \le j < k \le n} (c_k - c_j)
$$
for the $(n + 1) \times (n + 1)$ Vandermonde determinant.
**Solution**
We will apply induction. We see that $\begin{vmatrix} 1 & c_0 \\ 1 & c_1 \end{vmatrix} = (1)(1)(c_1) + (c_0)(-1)(1) = c_1 - c_0$ and $\prod_{0 \le j < k \le 1} (c_k - c_j) = c_1 - c_0$ and so the formula holds for $n = 1$. We also see that $\begin{vmatrix} 1 & c_0 & c_0^2 \\ 1 & c_1 & c_1^2 \\ 1 & c_2 & c_2^2 \end{vmatrix} = (1)(1)(\begin{vmatrix} c_1 & c_1^2 \\ c_2 & c_2^2 \end{vmatrix} + (c_0)(-1)(\begin{vmatrix} 1 & c_1^2 \\ 1 & c_2^2 \end{vmatrix} + (c_0^2)(1)(\begin{vmatrix} 1 & c_1 \\ 1 & c_2 \end{vmatrix} = c_0c_1^2 - c_0c_2^2 - c_0^2c_1 + c_0^2c_2 + c_1c_2^2 - c_1^2c_2$ and $\prod_{0 \le j < k \le 2} (c_k - c_j) = (c_2 - c_1)(c_2 - c_0)(c_1 - c_0) = c_0c_1^2 - c_0c_2^2 - c_0^2c_1 + c_0^2c_2 + c_1c_2^2 - c_1^2c_2$ and so the formula holds for $n = 2$. Call $c_n = x$. Expanding the determinant along the last row, each entry $x^k$ has a cofactor depending only on $c_0, c_1, \ldots, c_{n-1}$. The highest power appearing is $x^n$, and so the determinant is a polynomial $A_0 + A_1x + A_2x^2 + \ldots + A_nx^n$ with coefficients $A_k$ depending on $c_0, c_1, \ldots, c_{n-1}$. For $x = c_j$ where $j \in \{0, 1, \ldots, n-1\}$, the last row becomes identical to row $j+1$, and so the determinant is 0. Thus $c_0, c_1, \ldots, c_{n-1}$ are $n$ roots of a degree $n$ polynomial, and so it can be written as,
$$A_0 + A_1x + \ldots + A_nx^n = A_n(x - c_0)(x - c_1)\cdots(x - c_{n-1})$$

$A_n$ is the cofactor of $x^n$, which is precisely the $n \times n$ Vandermonde determinant in $c_0, c_1, \ldots, c_{n-1}$. By the inductive hypothesis,
$$A_n = \prod_{0 \le j < k \le n-1}(c_k - c_j)$$
Substituting $x = c_n$ into the expression from part (c),
$$\det(V) = \prod_{0 \le j < k \le n-1}(c_k - c_j) \cdot \prod_{0 \le j \le n-1}(c_n - c_j) = \prod_{0 \le j < k \le n}(c_k - c_j)$$
where the last equality holds because $\prod_{0 \le j < k \le n}(c_k - c_j)$ consists exactly of the pairs from the $n \times n$ block together with all pairs involving $c_n$. $\blacksquare$
