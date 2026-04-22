$$
\require{unicode}
\newcommand{\proofend}{\Large\unicode{x263B}}
$$

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
