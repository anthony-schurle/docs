$$
\require{unicode}
\newcommand{\proofend}{\Large\unicode{x263B}}
$$

**Problem 6.3**
Prove the Polarization identities, $(Ax, y) = 0.25[(A(x+y), x+y) - (A(x-y), x-y)]$ in the reals ($A = A*$) and $(Ax, y) = 0.25\sum_{\alpha = \pm 1, \pm i} \alpha(A(x + \alpha y), x + \alpha y)$ in the complex case (A is arbitrary).
**Solution**
$$
0.25[(A(x+y), x+y) - (A(x-y), x-y)]
$$
$$
= 0.25[(Ax, x+y) + (Ay, x+y) - (Ax, x-y) - (-Ay, x-y)]
$$
$$
= 0.25[(Ax, x) + (Ax, y) + (Ay, x) + (Ay, y) - (Ax, x) + (Ax, y) - (-Ay, x) + (-Ay, y)]
$$
$$
= 0.25[2(Ax, y) + 2(Ay, x)] = 0.5[(Ax, y) + (y, Ax)] = 0.5[2(Ax, y)] = (Ax, y)
$$
and so we verified the identity for the reals when $A = A*$. Now the complex case,
$$
0.25\sum_{\alpha = \pm 1, \pm i} \alpha(A(x + \alpha y), x + \alpha y) = 0.25\sum_{\alpha = \pm 1, \pm i}\alpha[(Ax, x + \alpha y) + \alpha(Ay, x + \alpha y)]
$$
$$
= 0.25 \sum_{\alpha = \pm 1, \pm i} \alpha[(Ax, x) + \overline{\alpha}(Ax, y) + \alpha(Ay, x) + \alpha\overline{\alpha}(Ay, y)]
$$
$$
= 0.25 \sum_{\alpha = \pm 1, \pm i} \alpha(Ax, x) + |\alpha|^2(Ax, y) + \alpha^2(Ay, x) + \alpha|\alpha|^2(Ay, y)
$$
$$
= 0.25[4(Ax, y)] = (Ax, y)
$$
$\proofend$

**Problem 6.4**
Show that a product of orthogonal matrices is orthogonal.
**Solution**
Let A and B be orthogonal matrices. By definition, $I = B*B = BB*$ and $I = A*A = AA*$ and so $AB(AB)* = ABB*A* = AA* = I$, $(AB)*AB = B*A*AB = B*B = I$. Therefore, AB is orthogonal by Lemma 6.2 and invertibility. But A and B were arbitrary and so a product of orthogonal matrices is orthogonal.
$\proofend$

**Problem 6.6**
Let A and B be unitarily equivalent $n \times n$ matrices.
a) Prove that $trace(A*A) = trace(B*B)$.
b) Use a) to prove that $\sum_{j,k = 1}^n |A_{j,k}|^2 = \sum_{j,k=1}^n |B_{j,k}|^2$.
c) Use b) to prove that the matrices $A := \begin{pmatrix} 1 & 2 \\ 2 & i \end{pmatrix}$ and $B := \begin{pmatrix} i & 4 \\ 1 & 1 \end{pmatrix}$ are not unitarily equivalent.
**Solution**
a)
By definition, $A = UBU*$ for some operator U. So,
$$
trace(A*A) = trace((U(BU*))*UBU*) = trace((BU*)*U*UBU*) = trace(UB*BU*)
$$
and since $trace(XY) = trace(YX)$ for any matrices X and Y with defined products,
$$
trace((UB*B)U*) = trace(U*UB*B) = trace(B*B)
$$
as desired.

b)
$$
trace(A*A) = \sum_{k=1}^n (A*A)_{k,k} = \sum_{k=1}^n \sum_{j=1}^n A*_{k,j}A_{j,k} = \sum_{k=1}^n \sum_{j=1}^n \overline{A_{j,k}}A_{j,k} = \sum_{k=1}^n \sum_{j=1}^n |A_{j,k}|^2
$$
and similarly $trace(B*B) = \sum_{k=1}^n \sum_{j=1}^n |B_{j,k}|^2$. By a) then, $\sum_{j,k = 1}^n |A_{j,k}|^2 = \sum_{j,k=1}^n |B_{j,k}|^2$ as desired.

c)
$$
\sum_{j,k=1}^2 |A_{j,k}|^2 = 1 + 4 + 4 + 1 = 10
$$
and
$$
\sum_{j,k = 1}^2|B_{j,k}|^2 = 1 + 16 + 1 + 1 = 19
$$
so by contrapositive of b), A and B are not unitarily equivalent.
$\proofend$

**Problem 7.1**
Give an example of a rigid motion T in $\mathbb{C}^n$, $T(0) = 0$, which is not a linear transformation.
**Solution**
Define $T(z_1, z_2, ...,  z_n) = (\overline{z_1}, \overline{z_2}, ..., \overline{z_n})$. Notice then that $T(0) = \overline{0} = 0$. More importantly, for $x,y \in \mathbb{C}^n$ we have,
$$
||T(x) - T(y)|| = ||\overline{x} - \overline{y}|| = ||\overline{x-y}|| = ||x-y||
$$

and so T is a rigid motion. Lastly, $T(2i, 0, ..., 0) = (-2i, 0, ..., 0) \ne (2i, 0, ..., 0) = iT(2, 0, ..., 0)$ and so T is not a linear transformation.
$\proofend$

**Problem 8.3**
Let U be an orthogonal transformation (in a real inner product space X) satisfying $U^2 = -I$. Prove that for all $x \in X$ we have $Ux \perp x$.
**Solution**
Let $x \in X$ be arbitrary. Since U is unitary, $(Ux, U^2x) = (x, Ux)$ and because $U^2 = -I$ we see that $(Ux, U^2x) = (Ux, -x)$. Then $(x, Ux) = -(Ux, x)$ and because X is real, $(Ux, x) = -(Ux, x)$. This gives $2(Ux, x) = 0$ and so $(Ux, x) = 0$. By definition, $Ux \perp x$.
$\proofend$

**Problem 8.4**
Show that if U is an orthogonal transformation satisfying $U^2 = -I$, then $U* = -U$.
**Solution**
We see that because $U^2 = -I$, we have $U*U^2 = -U*$. But $U*U = I$ by definition of orthogonal, and so $U = -U*$ because $U*U^2 = -U*$. Hence $U* = -U$.
$\proofend$

**Problem 8.5**
Let U be an orthogonal transformation in a real inner product space, satisfying $U^2 = -I$. Show that in this case $dim X = 2n$, and that there exists a subspace $E \subset X$, $dim E = n$, and an orthogonal transformation $U_0 : E \to E^\perp$ such that U in the decomposition $X = E \oplus E^\perp$ is given by the block matrix $U = \begin{pmatrix} 0 & -U_0^* \\ U_0 & 0 \end{pmatrix}$. This statement can be easily obtained from Theorem 5.1 of Chapter 6, if one notes the only rotation $R_\alpha$ in $\mathbb{R}^2$ satisfying $R^2_\alpha = -I$ are rotations through $\alpha = \pm 0.5\pi$. However, one can find an elementary proof here, not using this theorem. For example, the statement is trivial if $dim X = 2$: in this case we can take for E any 1-D subspace. Then it is not hard to show, that such operator U does not exist in $\mathbb{R}^2$, and one can use induction in $dim X$ to complete the proof.
**Solution**
We prove the statement by induction on $\dim X$. If $\dim X=0$, there is nothing to prove. Now assume $\dim X\ge 2$, and choose $0\ne x\in X$. By Problem 8.3, $Ux\perp x$. Also $Ux\ne 0$, since otherwise $U^2x=0$, contradicting $U^2=-I$. Hence $x$ and $Ux$ are nonzero orthogonal vectors, so they are linearly independent. Let $L=\operatorname{span}\{x,Ux\}$. Then $\dim L=2$, and $L$ is $U$-invariant because $U(x)=Ux\in L$ and $U(Ux)=U^2x=-x\in L$. We claim that $L^\perp$ is also $U$-invariant. If $y\in L^\perp$ and $z\in L$, then using Problem 8.4, $(Uy,z)=(y,U^*z)=(y,-Uz)$. Since $L$ is $U$-invariant, $Uz\in L$, so $(y,-Uz)=0$. Thus $(Uy,z)=0$ for all $z\in L$, and therefore $Uy\in L^\perp$. Hence $X=L\oplus L^\perp$, where both $L$ and $L^\perp$ are $U$-invariant. The restriction $U|_{L^\perp}$ is again orthogonal and satisfies $(U|_{L^\perp})^2=-I$. By induction, $\dim L^\perp$ is even, say $\dim L^\perp=2m$, and there exists a subspace $E_2\subset L^\perp$ with $\dim E_2=m$ and an orthogonal map  
$U_2:E_2\to(E_2^\perp\cap L^\perp)$ such that, relative to $L^\perp=E_2\oplus(E_2^\perp\cap L^\perp)$, the operator $U|_{L^\perp}$ has matrix $\begin{pmatrix}0&-U_2^*\\ U_2&0\end{pmatrix}$. Now let $E_1=\operatorname{span}\{x\}$. Then $L=E_1\oplus\operatorname{span}\{Ux\}$. Define  
$U_1:E_1\to\operatorname{span}\{Ux\}$ by $U_1(ax)=a\,Ux$. This is an orthogonal transformation, and relative to the decomposition $L=E_1\oplus\operatorname{span}\{Ux\}$, the operator $U|_L$ has matrix  $\begin{pmatrix}0&-U_1^*\\ U_1&0\end{pmatrix}$. Finally set $E=E_1\oplus E_2$ and $U_0=U_1\oplus U_2$. Then $E^\perp=\operatorname{span}\{Ux\}\oplus(E_2^\perp\cap L^\perp)$, so  
$$  
\dim E = 1+\dim E_2 = 1+\frac{\dim X-2}{2}=\frac{\dim X}{2}.  
$$  
Therefore $\dim X$ is even, say $\dim X=2n$, and $\dim E=n$. In the decomposition $X=E\oplus E^\perp$, the operator $U$ has block form  
$$  
U=\begin{pmatrix}0&-U_0^*\\ U_0&0\end{pmatrix}.  
$$  
$\proofend$

**Problem 1.1**
Use the upper triangular representation of an operator to give an alternative proof of the fact that determinant is the product and the trace is the sum of eigenvalues counting multiplicities.
**Solution**
By the upper triangular representation theorem, for some unitary matrix $U$, $A = UTU*$
where $T$ is upper triangular. Since $A$ and $T$ are similar, they have the same determinant and the same trace by previous homeworks. Let the diagonal entries of $T$ be $\lambda_1, \lambda_2, \dots, \lambda_n$. Then
$$
T =
\begin{pmatrix}
\lambda_1 & * & \cdots & * \\
0 & \lambda_2 & \cdots & * \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & \lambda_n
\end{pmatrix}.
$$

Because $T$ is upper triangular, its eigenvalues are exactly its diagonal entries, counted with multiplicities. Hence the eigenvalues of $A$ are $\lambda_1, \lambda_2, \dots, \lambda_n$, counting multiplicities. Also, for an upper triangular matrix, the determinant is the product of the diagonal entries, so
$$
\det(T) = \lambda_1 \lambda_2 \cdots \lambda_n.
$$
Therefore,
$$
\det(A) = \det(T) = \prod_{k=1}^n \lambda_k.
$$

Similarly, for an upper triangular matrix, the trace is the sum of the diagonal entries, so
$$
trace(T) = \lambda_1 + \lambda_2 + \cdots + \lambda_n.
$$
Therefore,
$$
\operatorname{tr}(A) = \operatorname{tr}(T) = \sum_{k=1}^n \lambda_k.
$$

Thus determinant is the product and trace is the sum of the eigenvalues of $A$, counting multiplicities.
$\proofend$

**Problem 2.2**
True or false: the sum of normal operators is normal?
**Solution**
False. Define $A := \begin{pmatrix} 1 & 0 \\ 0 & i \end{pmatrix}, B := \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$. Notice,
$$
A + B = \begin{pmatrix} 1 & 1 \\ 1 & i \end{pmatrix}, (A+B)* = \begin{pmatrix} 1 & 1 \\ 1 & -i \end{pmatrix}
$$
and so,
$$
(A+B)*(A+B) = \begin{pmatrix} 2 & 1 + i \\ 1 - i & 2 \end{pmatrix}, (A+B)(A+B)* = \begin{pmatrix} 2 & 1 - i \\ 1 + i & 2 \end{pmatrix}
$$
Therefore, $(A+B)$ is not normal. We verify A and B are normal, however.
$$
A* = \begin{pmatrix} 1 & 0 \\ 0 & -i \end{pmatrix}, A*A = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = AA*
$$
$$
B* = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, B*B = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = BB*
$$

and so A and B are both normal.
$\proofend$

**Problem 2.3**
Show that an operator unitarily equivalent to a diagonal one is normal.
**Solution**
Let O be an operator unitarily equivalent to the diagonal operator D. By definition, $O = UDU^{-1}$ for unitary operator U. We see that $O* = (UDU^{-1})* = (DU^{-1})*U* = U^{-1}*D*U*$. Since U unitary with $U^{-1} = U*$, $O* = UD*U^{-1}$. Notice,
$$
OO* = UDU^{-1}UD*U^{-1} = UDD*U^{-1}
$$
$$
O*O = UD*U^{-1}UDU^{-1} = UD*DU^{-1}
$$
$D*D = DD*$ since D is a diagonal and so $OO* = O*O$ meaning O is normal.
$\proofend$
