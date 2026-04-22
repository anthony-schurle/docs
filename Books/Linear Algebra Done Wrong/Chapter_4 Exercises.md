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
\sum_{j,k=1}^2 |A_{j,k}|^2 = 1 + 4 + 4 - 1 = 8
$$
and
$$
\sum_{j,k = 1}^2|B_{j,k}|^2 = -1 + 16 + 1 + 1 = 17
$$
so by contrapositive of b), A and B are not unitarily equivalent.
$\proofend$

**Problem 7.1**
Give an example of a rigid motion T in $\mathbb{C}^n$, $T(0) = 0$, which is not a linear transformation.
**Solution**
Define $T(z) = \overline{z}$. Notice then that $T(0) = \overline{0} = 0$. More importantly, for $x,y \in \mathbb{C}^n$ we have,
$$
||T(x) - T(y)|| = ||\overline{x} - \overline{y}|| = ||\overline{x-y}|| = ||x-y||
$$

and so T is a rigid motion. Lastly, $T(2i) = -2i \ne 2i = iT(2)$ and so T is not a linear transformation.
$\proofend$

**Problem 8.3**
Let U be an orthogonal transformation (in a real inner product space X) satisfying $U^2 = -I$. Prove that for all $x \in X$ we have $Ux \perp x$.
**Solution**
Let $x \in X$ be arbitrary. Since U is unitary, $(Ux, U^2x) = (x, Ux)$ and because $U^2 = -I$ we see that $(Ux, U^2x) = (Ux, -x)$. Then $(x, Ux) = -(Ux, x)$ and because X is real, $(Ux, x) = -(Ux, x)$. This gives $2(Ux, x) = 0$ and so $(Ux, x) = 0$. By definition, $Ux \perp x$.
$\proofend$

**Problem 8.4**
Show that if U is an orthogonal transformation satisfying $U^2 = -I$, then $U* = -U$.
**Solution**
We see that because $U^2 = -I$, we have $U*U^2 = -U*$. But $U*U^ = I$ by definition of orthogonal, and so $U = -U*$. Hence $U* = -U$.
$\proofend$

**Problem 8.5**
Let U be an orthogonal transformation in a real inner product space, satisfying $U^2 = -I$. Show that in this case $dim X = 2n$, and that there exists a subspace $E \subset X$, $dim E = n$, and an orthogonal transformation $U_0 : E \to E^\perp$ such that U in the decomposition $X = E \oplus E^\perp$ is given by the block matrix $U = \begin{pmatrix} 0 & -U_0^* \\ U_0 & 0 \end{pmatrix}$. This statement can be easily obtained from Theorem 5.1 of Chapter 6, if one notes the only rotation $R_\alpha$ in $\mathbb{R}^2$ satisfying $R^2_\alpha = -I$ are rotations through $\alpha = \pm 0.5\pi$. However, one can find an elementary proof here, not using this theorem. For example, the statement is trivial if $dim X = 2$: in this case we can take for E any 1-D subspace. Then it is not hard to show, that such operator U does not exist in $\mathbb{R}^2$, and one can use induction in $dim X$ to complete the proof.
**Solution**
We prove the statement by induction on $\dim X$. Assume $\dim X\ge 2$, and choose $0\ne x\in X$. Since $U^2=-I$, we have $Ux\ne 0$. Also, from the previous problem, $U^*=-U$. Hence
$$
(Ux,x)=(x,U^*x)=(x,-Ux)=-(x,Ux),
$$
so $(Ux,x)=0$. Thus $Ux\perp x$. Let $L=\operatorname{span}\{x,Ux\}$. Since $x$ and $Ux$ are nonzero and orthogonal, they are linearly independent, so $\dim L=2$. Also $L$ is $U$-invariant, because
$$
U(x)=Ux\in L,\qquad U(Ux)=U^2x=-x\in L.
$$

We claim that $L^\perp$ is also $U$-invariant. Let $y\in L^\perp$ and $z\in L$. Then
$$
(Uy,z)=(y,U^*z)=(y,-Uz).
$$
Since $L$ is $U$-invariant, $Uz\in L$, and since $y\in L^\perp$, it follows that $(y,-Uz)=0$. Hence $(Uy,z)=0$ for all $z\in L$, so $Uy\in L^\perp$.

Therefore,
$$
X=L\oplus L^\perp
$$
is an orthogonal decomposition into $U$-invariant subspaces. On $L^\perp$, the restriction $U|_{L^\perp}$ is again orthogonal and satisfies
$$
(U|_{L^\perp})^2=-I.
$$
So the induction hypothesis applies to $L^\perp$.

Now let
$$
E_1=\operatorname{span}\{x\}\subset L.
$$
Then $E_1^\perp\cap L=\operatorname{span}\{Ux\}$, so
$$
L=E_1\oplus (E_1^\perp\cap L).
$$
Define
$$
U_1:E_1\to E_1^\perp\cap L,\qquad U_1(ax)=a\,Ux.
$$
Since $U$ is orthogonal, $U_1$ is an orthogonal transformation. In the decomposition
$$
L=E_1\oplus (E_1^\perp\cap L),
$$
the operator $U|_L$ has block form
$$
\begin{pmatrix}
0 & -U_1^*\\
U_1 & 0
\end{pmatrix}.
$$
Indeed, $U$ sends $E_1$ to $E_1^\perp\cap L$, and if $f=U_1e$, then
$$
Uf=U(U_1e)=U^2e=-e=-U_1^*f.
$$

By induction, there exists a subspace $E_2\subset L^\perp$, with
$$
\dim E_2=\frac{\dim L^\perp}{2},
$$
and an orthogonal transformation
$$
U_2:E_2\to E_2^\perp\cap L^\perp
$$
such that in the decomposition
$$
L^\perp=E_2\oplus E_2^\perp,
$$
the operator $U|_{L^\perp}$ has block form
$$
\begin{pmatrix}
0 & -U_2^*\\
U_2 & 0
\end{pmatrix}.
$$

Now set
$$
E=E_1\oplus E_2.
$$
Then
$$
E^\perp=(E_1^\perp\cap L)\oplus E_2^\perp,
$$
and
$$
\dim E=1+\dim E_2=1+\frac{\dim X-2}{2}=\frac{\dim X}{2}.
$$
So $\dim X$ is even, say $\dim X=2n$, and $\dim E=n$.

Finally define
$$
U_0=U_1\oplus U_2:E\to E^\perp.
$$
Then $U_0$ is orthogonal, and in the decomposition
$$
X=E\oplus E^\perp
$$
the operator $U$ has block matrix
$$
U=\begin{pmatrix}
0 & -U_0^*\\
U_0 & 0
\end{pmatrix}.
$$
$\proofend$
