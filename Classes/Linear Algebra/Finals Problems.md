1) Let $A_n$ be the given $n \times n$ matrix, and let $D_n = \det(A_n)$. Show that $D_n = D_{n-1} + D_{n-2}$ for $n \geq 3$, and conclude that $D_1,D_2,\dots$ is the Fibonacci sequence $1,2,3,5,\dots$.

Expand $D_n$ along the first row. The first row has only two nonzero entries, $a_{11}=1$ and $a_{12}=-1$. The $a_{11}$ cofactor gives $D_{n-1}$, since deleting the first row and first column leaves $A_{n-1}$. For the $a_{12}$ cofactor, the sign is negative, and since $a_{12}=-1$, the signs cancel. The corresponding minor has first column $(1,0,\dots,0)^T$, and expanding along that column leaves exactly $A_{n-2}$. Thus this term gives $D_{n-2}$. Hence $D_n=D_{n-1}+D_{n-2}$. Also $D_1=1$ and $D_2=\det \begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix}=2$. Therefore $D_1,D_2,D_3,\dots=1,2,3,5,8,\dots$. $\blacksquare$

Visual: $A_4=\begin{pmatrix} 1 & -1 & 0 & 0 \\ 1 & 1 & -1 & 0 \\ 0 & 1 & 1 & -1 \\ 0 & 0 & 1 & 1 \end{pmatrix}$

2) Let $A$ be an $n \times n$ skew-symmetric matrix over the complex numbers with $n$ odd. Show that $\det(A)=0$.

Since $A^T=-A$ and $det(A) = det(A^T)$ (A is a square), we have $\det(A)=\det(A^T)=\det(-A)=(-1)^n\det(A)$. Since $n$ is odd, $\det(A)=-\det(A)$, so $\det(A)=0$. $\blacksquare$

3) Let $A$ be an $n \times n$ matrix over the complex numbers. Show that $A$ is diagonalizable if and only if there is a polynomial $p$ with distinct roots so that $p(A)=0$.

If $A$ is diagonalizable, then $A=SDS^{-1}$, where $D$ is diagonal and its diagonal entries are the eigenvalues of $A$. Let $\lambda_1,\dots,\lambda_k$ be the distinct eigenvalues of $A$, and define $p(x)=(x-\lambda_1)\cdots(x-\lambda_k)$. Since every diagonal entry of $D$ is one of the $\lambda_i$, we have $p(D)=0$. Therefore $p(A)=Sp(D)S^{-1}=0$.

Conversely, suppose $p(A)=0$ for some polynomial $p$ with distinct roots. Put $A$ in Jordan form, so $A=SJS^{-1}$. Then $p(A)=Sp(J)S^{-1}$, so $p(J)=0$. For a Jordan block $J_\lambda=\lambda I+N$, we have $p(J_\lambda)=p(\lambda)I+p'(\lambda)N+\cdots$. Since $p(J_\lambda)=0$, its diagonal entries give $p(\lambda)=0$. Since $p$ has distinct roots, $p'(\lambda)\neq 0$. If the block had size greater than $1$, then $N\neq 0$, and the first superdiagonal of $p(J_\lambda)$ would be nonzero. This is impossible. Therefore every Jordan block has size $1$, so $J$ is diagonal. Hence $A$ is diagonalizable. $\blacksquare$

4) Let $V$ be a finite dimensional vector space over the complex numbers and let $A:V \to V$ be diagonalizable. Let $W$ be any subspace of $V$ invariant under $A$. Show that $A$ restricted to $W$ is diagonalizable.

Since $A$ is diagonalizable, by problem 3 there is a polynomial $p$ with distinct roots such that $p(A)=0$. Since $W$ is invariant under $A$, $A|_W$ is well-defined and $(A|_W)^j=A^j|_W$ for every $j$, so $p(A|_W)=p(A)|_W=0$. Therefore, again by problem 3, $A|_W$ is diagonalizable. $\blacksquare$

5) Let $A$ be an $n \times n$ matrix of real numbers which is symmetric. Show there is a real symmetric $n \times n$ matrix $B$ so that $A=B^3$.

By the spectral theorem, since $A$ is real symmetric, $A=QDQ^T$, where $Q$ is orthogonal and $D$ is real diagonal. Let $D'$ be the real diagonal matrix obtained by taking the real cube root of each diagonal entry of $D$. Then $(D')^3=D$. Define $B=QD'Q^T$. Then $B$ is real symmetric, and $B^3=Q(D')^3Q^T=QDQ^T=A$. $\blacksquare$

6) Let $T$ be a linear transformation from a complex inner product space $X$ to itself. Suppose that $T$ is normal. Show that any linear transformation $U:X \to X$ satisfying $UT=TU$ must also satisfy $UT^*=T^*U$.

Since $T$ is normal, $X$ has an orthonormal basis of eigenvectors of $T$. In this basis, $T$ is diagonal, so $T^*$ is also diagonal with the same eigenvectors and conjugated eigenvalues. Let $v$ be in the $\lambda$-eigenspace of $T$. Since $UT=TU$, we have $T(Uv)=U(Tv)=\lambda Uv$, so $U$ preserves each eigenspace of $T$. Since $T^*$ acts as multiplication by $\overline{\lambda}$ on the $\lambda$-eigenspace, we have $UT^*v=\overline{\lambda}Uv=T^*Uv$ for every eigenvector $v$. Since the eigenvectors form a basis, $UT^*=T^*U$. $\blacksquare$

7) Let $A=\begin{pmatrix} A_{n-1} & \vec b \\ \vec b^T & c \end{pmatrix}$, where $A_{n-1}$ is invertible. Show that $\det(A)=\det(A_{n-1})(c-(A_{n-1}^{-1}\vec b \cdot \vec b))$.

Let $P=\begin{pmatrix} I & 0 \\ -\vec b^T A_{n-1}^{-1} & 1 \end{pmatrix}$. Then $\det(P)=1$, and $PA=\begin{pmatrix} A_{n-1} & \vec b \\ 0 & c-\vec b^T A_{n-1}^{-1}\vec b \end{pmatrix}$. Therefore $\det(A)=\det(PA)=\det(A_{n-1})(c-\vec b^T A_{n-1}^{-1}\vec b)$. $\blacksquare$

Let $P=\begin{pmatrix} I & 0 \\ -\vec b^T A_{n-1}^{-1} & 1 \end{pmatrix}$. Then $\det(P)=1$, and $PA=\begin{pmatrix} A_{n-1} & \vec b \\ 0 & c-\vec b^T A_{n-1}^{-1}\vec b \end{pmatrix}$. Therefore $\det(A)=\det(PA)=\det(A_{n-1})(c-\vec b^T A_{n-1}^{-1}\vec b)$. Since $A_{n-1}$ is symmetric, $A_{n-1}^{-1}$ is symmetric, so $\vec b^T A_{n-1}^{-1}\vec b=A_{n-1}^{-1}\vec b\cdot \vec b$. $\blacksquare$

8) Use problem 7 to give a proof of Sylvester’s criterion for positive definiteness of quadratic forms.

We prove by induction that $A$ is positive definite if and only if $\det(A_k)>0$ for every $1\leq k\leq n$. The case $n=1$ is immediate. Write $A=\begin{pmatrix} A_{n-1} & \vec b \\ \vec b^T & c \end{pmatrix}$.

First suppose $A$ is positive definite. Then $A_{n-1}$ is positive definite, so by induction $\det(A_k)>0$ for every $1\leq k\leq n-1$. Also $A_{n-1}$ is invertible, and $c-\vec b^T A_{n-1}^{-1}\vec b$ is the value of the quadratic form of $A$ on $\begin{pmatrix} -A_{n-1}^{-1}\vec b \\ 1 \end{pmatrix}$, so it is positive. By problem 7, $\det(A)=\det(A_{n-1})(c-\vec b^T A_{n-1}^{-1}\vec b)>0$. Therefore $\det(A_k)>0$ for every $1\leq k\leq n$.

Conversely, suppose $\det(A_k)>0$ for every $1\leq k\leq n$. By induction, $A_{n-1}$ is positive definite. By problem 7, $\det(A)=\det(A_{n-1})(c-\vec b^T A_{n-1}^{-1}\vec b)$, so $c-\vec b^T A_{n-1}^{-1}\vec b=\frac{\det(A)}{\det(A_{n-1})}>0$. For any vector $\begin{pmatrix} x \\ t \end{pmatrix}$, the quadratic form equals $(x+tA_{n-1}^{-1}\vec b)^T A_{n-1}(x+tA_{n-1}^{-1}\vec b)+t^2(c-\vec b^T A_{n-1}^{-1}\vec b)$, which is positive for every nonzero vector. Therefore $A$ is positive definite. $\blacksquare$

9) Let $X$ be a complex inner product space. Let $N:X \to X$ be both normal and nilpotent. Show that $N$ must be the zero linear transformation.

Since $N$ is normal, by the spectral theorem $N=UDU^*$, where $U$ is unitary and $D$ is diagonal. Since $N$ is nilpotent, $N^k=0$ for some $k$. Thus $0=N^k=(UDU^*)^k=UD^kU^*$, so $D^k=0$. But $D$ is diagonal, so $D^k$ is obtained by raising each diagonal entry of $D$ to the $k$th power. Hence every diagonal entry of $D$ is $0$, so $D=0$. Therefore $N=UDU^*=0$. $\blacksquare$

10) Let $N$ be an $n \times n$ matrix over the complex numbers with $N^n=0$ and $N^{n-1}\neq 0$. Show that there does not exist an $n \times n$ matrix $A$ with $A^2=N$.

Suppose $A^2=N$. Then $A^{2n}=N^n=0$, so $A$ is nilpotent. Thus all eigenvalues of $A$ are $0$, so its characteristic polynomial is $p(t)=\pm t^n$. By Cayley-Hamilton, $p(A)=0$, so $A^n=0$. Therefore $N^{n-1}=(A^2)^{n-1}=A^{2n-2}=0$, since $2n-2\geq n$. This contradicts $N^{n-1}\neq 0$. Therefore no such $A$ exists for $n\geq 2$. $\blacksquare$

11) What is the dimension of the largest subspace of $4 \times 4$ real matrices so that the trace of the $3 \times 3$ matrix of the first three rows and first three columns is zero, and the trace of the $3 \times 3$ matrix of the last three rows and last three columns is zero?

The two trace conditions are $a_{11}+a_{22}+a_{33}=0$ and $a_{22}+a_{33}+a_{44}=0$. Subtracting them gives $a_{11}=a_{44}$. The first equation then gives $a_{33}=-a_{11}-a_{22}$. Thus the diagonal entries have the form $(a_{11},a_{22},a_{33},a_{44})=(s,t,-s-t,s)$, so they form a $2$-dimensional subspace. The $12$ off-diagonal entries are unrestricted, so the total dimension is $12+2=14$. $\blacksquare$

12) Is it possible for a real matrix $A$ that the range of $A$ is the kernel of $A^T$? Is it possible for a complex matrix?

For real matrices, it is not possible. If $\operatorname{range}(A)=\ker(A^T)$, then every column of $A$ lies in $\ker(A^T)$, so $A^TA=0$. The diagonal entries of $A^TA$ are sums of squares of entries of $A$, so $A=0$. Then $\operatorname{range}(A)=\{0\}$ but $\ker(A^T)=\mathbb{R}^m$, a contradiction in the nontrivial case.

For complex matrices, it is possible. Let $A=\begin{pmatrix} 1 & i \\ i & -1 \end{pmatrix}$. Then $A^T=A$ and $A^2=0$, so $\operatorname{range}(A)\subseteq \ker(A^T)$. Since the columns of $A$ are nonzero multiples of each other, $\operatorname{rank}(A)=1$. Hence $\dim(\operatorname{range}(A))=1$ and $\dim(\ker(A^T))=2-\operatorname{rank}(A^T)=1$. Since one subspace is contained in the other and their dimensions are equal, $\operatorname{range}(A)=\ker(A^T)$ (any linearly independent system can be completed to a basis in a finite in a finite-dimensional space). $\blacksquare$

13) Prove that if $A$ and $B$ are similar matrices, then the trace of $A$ is equal to the trace of $B$.

Since $A$ and $B$ are similar, $A=Q^{-1}BQ$ for some invertible matrix $Q$. Therefore $\operatorname{tr}(A)=\operatorname{tr}(Q^{-1}BQ)=\operatorname{tr}((Q^{-1}B)Q)=\operatorname{tr}(Q(Q^{-1}B))=\operatorname{tr}(B)$, using $\operatorname{tr}(UV)=\operatorname{tr}(VU)$. $\blacksquare$


Known: 4, 6, 1, 10, 7, 5, 9, 2, 11, 12, 13