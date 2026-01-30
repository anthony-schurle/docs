**Problem 5.3:**
Multiply two rotation matrices $T_\alpha$ and $T_\beta$ (it is a rare case when the multiplication is commutative, so the order is not essential). Deduce formulas for $sin(\alpha + \beta)$ and $cos(\alpha + \beta)$ from here.
**Solution:**
$$
T_{\alpha + \beta} := T_\alpha \circ T_\beta
$$
But $T_{\alpha + \beta}$ is just the transformation that rotates by $\alpha + \beta$. Therefore,
$$
[T_{\alpha + \beta}] = \begin{pmatrix} cos(\alpha + \beta) & -sin(\alpha + \beta) \\ sin(\alpha + \beta) & cos(\alpha + \beta) \end{pmatrix} = [T_\alpha] [T_\beta] = \begin{pmatrix} cos(\alpha) & -sin(\alpha) \\ sin(\alpha) & cos(\alpha) \end{pmatrix} \begin{pmatrix} cos(\beta) & -sin(\beta) \\ sin(\beta) & cos(\beta) \end{pmatrix}
$$
$$
= \begin{pmatrix} cos(\alpha)cos(\beta) -sin(\alpha)sin(\beta) & -cos(\alpha)sin(\beta) + cos(\beta)sin(\alpha) \\ sin(\alpha)cos(\beta) + cos(\alpha)sin(\beta) & -sin(\alpha)sin(\beta) + cos(\alpha)cos(\beta) \end{pmatrix}
$$
and so we see that $sin(\alpha + \beta) = sin(\alpha)cos(\beta) + cos(\alpha)sin(\beta)$ and $cos(\alpha + \beta) = cos(\alpha)cos(\beta) -sin(\alpha)sin(\beta)$. **Q.E.D**

**Problem 5.4:**
Find the matrix of the orthogonal projection in $\mathbb{R}^2$ onto the line $x_1 = -2x_2$. Hint: What is the matrix of the projection onto the coordinate axis $x_1$?
**Solution:**
$$
T_{r} := \begin{pmatrix} cos(tan^{-1}(-0.5)) & -sin(tan^{-1}(-0.5)) \\ sin(tan^{-1}(-0.5)) & cos(tan^{-1}(-0.5)) \end{pmatrix}, T_{x_1} := \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}
$$

Notice $T_{x_1}$ is the projection onto the $x_1$ axis and $T_{r}$ is the rotation of the line. Therefore, the matrix of the orthogonal projection in $\mathbb{R}^2$ onto the line $x_1 = -2x_2$ must be $T_{r}^TT_{x_1}T_r$,
$$
\begin{pmatrix} cos(tan^{-1}(-0.5))^2 & -sin(tan^{-1}(-0.5))cos(tan^{-1}(-0.5)) \\ -sin(tan^{-1}(-0.5))cos(tan^{-1}(-0.5)) & sin(tan^{-1}(-0.5))^2 \end{pmatrix}
$$

**Q.E.D**

**Problem 5.6:**
Prove Theorem 5.1, i.e. prove that $trace(AB) = trace(BA)$.
**Solution:**
By definition of AB and BA both being defined, A and B are square matrices of dimension $m \times m$ for some $m \in \mathbb{N}$. It follows that,
$$
trace(AB) = \sum_{k=1}^m(AB)_{k, k} = \sum_{k=1}^m\sum_{j=1}^m a_{k, j}b_{j, k} = \sum_{j=1}^m\sum_{k=1}^m b_{j, k}a_{k, j} = \sum_{j=1}^m(BA)_{j,j} = trace(BA)
$$

and so $trace(AB) = trace(BA)$. **Q.E.D**

**Problem 5.7:**
Construct a non-zero matrix A such that $A^2 = 0$.
**Solution:**
$$
A := \begin{pmatrix} 1 & -1 \\ 1 & -1 \end{pmatrix}
$$
$$
A^2 = \begin{pmatrix} 1 & -1 \\ 1 & -1 \end{pmatrix}\begin{pmatrix} 1 & -1 \\ 1 & -1 \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = 0
$$
**Q.E.D**

**Problem 6.2:**
Find all right inverses to the $1 \times 2$ matrix (row) $A = (1, 1)$. Conclude from here that the row A is not left invertible.
**Solution:**
All right inverses are defined as $\begin{pmatrix} a \\ b \end{pmatrix}$ where $a + b = 1$ because $A\begin{pmatrix} a \\ b \end{pmatrix} = (a + b) = (1)$. We can see there are infinitely many such solutions. But then by theorem 6.1, because the right inverse is not unique, we see that A is not invertible. We know A is right invertible so it must not be left invertible. **Q.E.D**

**Problem 6.5:**
Find two matrices A and B that AB is invertible, but A and B are not. Hint:
square matrices A and B would not work. Remark: It is easy to construct such
A and B in the case when AB is a $1 \times 1$ matrix (a scalar). But can you get $2 \times 2$
matrix AB? $3 \times 3$? $n \times n$?
**Solution:**
Define the $n \times m$ matrix A and the $m \times n$ matrix B where $m > n$:
$$
A := \begin{pmatrix} 1 & 0 & 0 & ... & 0 & 0 & ... \\ 0 & 1 & 0 & ... & 0 & 0 & ... \\ 0 & 0 & 1 & ... & 0 & 0 & ... \\ ... & ... & ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & 1 & 0 & ... \end{pmatrix}, B := \begin{pmatrix} 1 & 0 & 0 & ... & 0 \\ 0 & 1 & 0 & ... & 0 \\ 0 & 0 & 1 & ... & 0 \\ ... & ... & ... & ... & 1 \\ 0 & 0 & 0 & ... & 0 \\ ... & ... & ... & ... & ... \end{pmatrix}
$$
Clearly, A and B are not invertible by Corollary 6.9 because A's columns are not linearly independent (0 vectors) in $\mathbb{F}^n$ and B is not generating (0 rows for all vectors) for $\mathbb{F}^m$. However, $AB = I$ which is invertible by definition (inverse is I). **Q.E.D**


**Problem 6.7:**
Let A and AB be invertible (assuming that the product AB is well defined). Prove that B is invertible.
**Solution:**
$$
AB(AB)^{-1} = I \implies A^{-1}AB(AB)^{-1} = A^{-1} \implies B(AB)^{-1} = A^{-1} \implies B(AB)^{-1}A = I
$$
and so B is right invertible.
$$
AB = AB \implies (AB)^{-1}AB = (AB)^{-1}AB \implies (AB)^{-1}AB = I
$$
and so B is left invertible. Therefore, B is invertible. **Q.E.D**

**Problem 6.8:**
Let A be $n \times n$ matrix. Prove that if $A^2 = 0$ then A is not invertible.
**Solution:**
Suppose $A^2 = 0$. Suppose A were invertible. Then there is $n \times n$ matrix B such that $AB = I$ and $BA = I$ by theorem 6.1. However, multiply the left sides both by A gives $AAB = AI$ which is equivalent to $0 = A$. But then $AB = 0$ always which is a contradiction, therefore A is not invertible. **Q.E.D**

**Problem 7.2:**
Let V be a vector space. For $X, Y \subset V$ the sum $X + Y$ is the collection of all vectors v which can be represented as $v = x + y, x \in X, y \in Y$. If X and Y are subspaces of V, then $X + Y$ is also a subspace.
**Solution:**
Suppose X and Y are subspaces of V. Pick arbitrary $z_1, z_2 \in X+Y$ such that $z_1 := x_1 + y_1$ and $z_2 := x_2 + y_2$ for $x_1,x_2 \in X$ and $y_1,y_2 \in Y$. But $z_1 + z_2 = (x_1 + y_1) + (x_2 + y_2) = (x_1 + x_2) + (y_1 + y_2)$ by additive commutivity and associativity. Because X is a subspace of V, we have $x_1 + x_2 \in X$. Similar reasoning follows for $y_1 + y_2 \in Y$. Therefore, $z_1 + z_2 \in X + Y$. Consider $\alpha z_1 = \alpha(x_1 + y_1)$ for $\alpha \in \mathbb{F}$. It follows from vector space properties that $\alpha(x_1 + y_1) = \alpha x_1 +\alpha y_1$ where $\alpha x_1 \in X$ and $\alpha y_1 \in Y$ by definition. Take arbitrary $x \in X$ and $y \in Y$. By definition, $x, y \in V$ and so $x + y \in V$. But x and y were arbitrary and so $X + Y \subseteq V$. Thus, $X + Y$ is a subspace. **Q.E.D**

**Problem 7.3:**
Let X be a subspace of a vector space V, and let $v \in V$, $v \not \in X$. If $x \in X$ then $x + v \not \in X$.
**Solution:**
Suppose arbitrary $x \in X$. Then consider $x + v \in X$. It follows by definition of closure that $v \in X$ which is a contradiction ($x + v + (-x) \in X$). Thus, $x + v \not \in X$. **Q.E.D**
