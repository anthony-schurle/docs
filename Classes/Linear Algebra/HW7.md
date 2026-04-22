**Problem 1.6:**
Prove that $|(x, y)| = ||x|| \cdot ||y||$ iff one of the vectors is a multiple of the other.
**Solution:**
The property trivially holds for $y = 0$ so suppose $y \ne 0$.
($\implies$) Suppose $|(x, y)| = ||x|| \cdot ||y||$. Then 
$$
0 = ||x||^2 - \frac{|(x, y)|^2}{||y||^2} = ||x||^2 - \frac{(x,y)}{||y||^2}(y,x) - \overline{\frac{(x,y)}{||y||^2}}(x,y) + |\frac{(x,y)}{||y||^2}|^2||y||^2$$
$$
= (x, x - \frac{(x,y)}{||y||^2}y) - \frac{(x,y)}{||y||^2}(y, x - \frac{(x,y)}{||y||^2}y) = (x - \frac{(x,y)}{||y||^2}y, x - \frac{(x,y)}{||y||^2}y)
$$

and so $(x - \frac{(x,y)}{||y||^2}y, x - \frac{(x,y)}{||y||^2}y) = 0$. Therefore, $x - \frac{(x, y)}{||y||^2}y = 0$ and so $x = \frac{(x, y)}{||y||^2}y$. Thus, x is a multiple of y.
($\Longleftarrow$) Suppose one of the vectors is a multiple of the other, WLOG $x = ky$ for some scalar $k$. Then $|(x, y)| = |(ky, y)| = |k(y,y)| = |k| ||y||^2 = |k| ||y|| \cdot ||y||$. Since $x = ky$, it must be that $||x|| = ||ky|| = |k|||y||$. Therefore, $|(x, y)| = ||x|| \cdot ||y||$. $\blacksquare$

**Problem 2.4:**
Let V be a vector space and let $v_1, v_2, ..., v_n$ be a basis in V. For $x = \sum_{k=1}^n \alpha_k v_k, y = \sum_{k=1}^n \beta_k v_k$ define $<x,y> := \sum_{k=1}^n \alpha_k \overline{\beta_k}$. Prove that $<x, y>$ defines an inner product in V.
**Solution:**
We will show that $<x, y>$ satisfies all properties of an inner product space. Let $x = \sum_{k=1}^n \alpha_k v_k, y = \sum_{k=1}^n \beta_k v_k, z = \sum_{k=1}^n \pi_k v_k$.
Conjugate symmetry -
$<x, y> = \sum_{k=1}^n \alpha_k \overline{\beta_k} = \overline{\sum_{k=1}^n \overline{\alpha_k} \beta_k} = \overline{<y, x>}$.
Linearity -
$$
<wx + vy, z> = <\sum_{k=1}^n (w \alpha_k + v \beta_k)v_k, z> = \sum_{k=1}^n (w \alpha_k + v \beta_k) \overline{\pi_k} = \sum_{k=1}^n w \alpha_k \overline{\pi_k} + \sum_{k=1}^n v \beta_k \overline{\pi_k}
$$
$$
= w \sum_{k=1}^n \alpha_k \overline{\pi_k} + v \sum_{k=1}^n \beta_k \overline{\pi_k} = w <x, z> + v <y, z>
$$

Non-negativity -
$<x, x> = \sum_{k=1}^n \alpha_k \overline{\alpha_k} = \sum_{k=1}^n |\alpha_k|^2$. Since $|\alpha_k|^2 \ge 0$ for all k, $<x, x> \ge 0$.

Non-degeneracy -
Suppose $<x, x> = \sum_{k=1}^n |\alpha_k|^2 = 0$. Since $|\alpha_k|^2 \ge 0$ for all k, it must be that $|\alpha_k|^2 = 0$. But this is true precisely when $\alpha_k = 0$ and so $x = 0$. Suppose $x = 0$. Because $v_1, v_2, ..., v_n$ is a basis, and so linearly independent, $x = 0$ only when $\alpha_k = 0$ for all k. Therefore, $<x, x> = \sum_{k=1}^n \alpha_k \overline{\alpha_k} = 0$. $\blacksquare$

**Problem 3.7:**
True or false: if E is a subspace of V, then $dimE + dim(E^\perp) = dim V$? Justify.
**Solution:**
True. Suppose E is a subspace of V. Let $dim E = n$ and $dim(E^\perp) = m$. Since $V = E \oplus E^\perp$, by Theorem 2.6 a basis in V is precisely the union of the basis elements in both $E$ and $E^\perp$. Therefore, $dim V = dim E + dim(E^\perp)$ since $E \cap E^\perp = \{0\}$. $\blacksquare$

**Problem 3.8**
Let P be the orthogonal projection onto a subspace E of an inner product space V, $dim V = n$, $dim E = r$. Find the eigenvalues and the eigenvectors (eigenspaces). Find the algebraic and geometric multiplicities of each eigenvalue.
**Solution:**
Take any non-zero vector $v \in E$. By definition, $Pv = v = 1v$. This means $\lambda = 1$ is an eigenvalue, and the entire subspace $E$ is contained within its eigenspace. Therefore, the geometric multiplicity of $\lambda = 1$ is at least $r$. Take any non-zero vector $w \in E^\perp$. By definition, $Pw = 0 = 0w$. This means $\lambda = 0$ is an eigenvalue, and the entire subspace $E^\perp$ is contained within its eigenspace. Therefore, the geometric multiplicity of $\lambda = 0$ is at least $n - r$. Since the characteristic polynomial has degree n, it must be that the sum of the algebraic multiplicity of $\lambda = 0$ and $\lambda = 1$ is less than or equal to n. So, the algebraic and geometric multiplicity for $\lambda = 1$ must be exactly $r$ and the algebraic and geometric multiplicity for $\lambda = 0$ must be exactly $n - r$. Therefore, no other eigenvalues can exist, because there is no room left in the degree-$n$ characteristic polynomial. The eigenspaces are exactly $E$ and $E^\perp$. $\blacksquare$

**Problem 3.10**
Let an inner product on the space of polynomials be defined by $(f, g) = \int_{-1}^1 f(t) \overline{g(t)}dt$. Apply Gram-Schmidt to the system $1, t, t^2, t^3$.
**Solution:**
First we set $v_1 = 1$. Then $v_2 = t - \frac{(t, 1)}{||1||^2}(1) = t$ since $(t, 1) = \int_{-1}^1 tdt = 0$. Next, $v_3 = t^2 - (\frac{(t^2, 1)}{||1||^2}(1) + \frac{(t^2, t)}{||t||^2}t)$. We see that $(t^2, 1) = \int_{-1}^1 t^2 dt = \frac{2}{3}$ and $(1, 1) = \int_{-1}^1 dt = 2$ so $||1||^2 = 2$. We also see that $(t^2, t) = \int_{-1}^1 t^3 dt = 0$. It follows that $v_3 = t^2 - \frac{1}{3}$. Next, $v_4 = t^3 - \left(\frac{(t^3, v_1)}{\|v_1\|^2}v_1 + \frac{(t^3, v_2)}{\|v_2\|^2}v_2 + \frac{(t^3, v_3)}{\|v_3\|^2}v_3\right)$. We compute the necessary inner products: $(t^3, v_1) = (t^3, 1) = \int_{-1}^1 t^3 dt = 0$, $(t^3, v_2) = (t^3, t) = \int_{-1}^1 t^4 dt = \frac{2}{5}$, $\|v_2\|^2 = (t, t) = \int_{-1}^1 t^2 dt = \frac{2}{3}$, $(t^3, v_3) = (t^3, t^2 - \frac{1}{3}) = \int_{-1}^1 (t^5 - \frac{1}{3}t^3) dt = 0$. Substituting these values into the formula $v_4 = t^3 - \left(0 + \frac{2/5}{2/3}t + 0\right) = t^3 - \frac{3}{5}t$. Thus, the Gram-Schmidt algorithm provides $1, t, t^2 - \frac{1}{3}, t^3 - \frac{3}{5}t$. $\blacksquare$

**Problem 3.11**
Let $P = P_E$ be the matrix of an orthogonal projection onto a subspace E. Show that,
a) The matrix P is self-adjoint, $P* = P$.
b) $P^2 = P$.
**Solution:**
a)
To show $P^* = P$, it suffices to show $(Px, y) = (x, Py)$ for all $x, y \in V$. Since $V = E \oplus E^\perp$, we can write $x = x_1 + x_2$ and $y = y_1 + y_2$ where $x_1, y_1 \in E$ and $x_2, y_2 \in E^\perp$. By the definition of an orthogonal projection, $Px = x_1$ and $Py = y_1$. We see that $(Px, y) = (x_1, y_1 + y_2) = (x_1, y_1) + (x_1, y_2)$. Since $x_1 \in E$ and $y_2 \in E^\perp$, they are orthogonal, so $(x_1, y_2) = 0$. Thus, $(Px, y) = (x_1, y_1)$. Notice $(x, Py) = (x_1 + x_2, y_1) = (x_1, y_1) + (x_2, y_1)$. Similarly, $(x_2, y_1) = 0$. Thus, $(x, Py) = (x_1, y_1)$. Since $(Px, y) = (x, Py)$, it follows that $P^* = P$. 

b)
Let v be arbitrary. We see that $P^2v = P(Pv) = Pw$ for $w \in E$ and $v - w \perp E$. Notice $w \in E$ and $w - w = 0 \perp E$ and so w is a orthogonal projection of w. But the orthogonal projection is unique so it must be that $Pw = w = Pv$. Thus, $P^2 = P$. $\blacksquare$

**Problem 4.5:**
Let an equation $Ax = b$ have a solution, and let A have non-trivial kernel. Prove that
a) There exist a unique solution $x_0$ of $Ax = b$ minimizing the norm $||x||$.
b) $x_0 = P_{(Ker A)^\perp}x$ for any x satisfying $Ax = b$.
**Solution:**
Let $x$ be any arbitrary solution to the equation, so $Ax = b$. We know that $V = \ker A \oplus (\ker A)^\perp$ and so we can uniquely write our solution $x$ as $x = u + x_0$ where $u \in \ker A$ and $x_0 \in (\ker A)^\perp$. By the definition of orthogonal projection, $x_0 = P_{(\ker A)^\perp}x$. Apply the operator $A$ to $x$, $A(x) = A(u + x_0) = Au + Ax_0$. Because $u \in \ker A$, we know $Au = 0$. We also know $Ax = b$. Substituting these in gives $b = 0 + Ax_0 \implies Ax_0 = b$. So, $x_0$ is a solution. Let $y$ be any other solution to the system, so $Ay = b$. We can rewrite $y$ relative to $x_0$ $y = x_0 + (y - x_0)$. Notice that $A(y - x_0) = Ay - Ax_0 = b - b = 0$. This means the vector $(y - x_0)$ belongs to $\ker A$. Since $x_0 \in (\ker A)^\perp$ and $(y - x_0) \in \ker A$, the two vectors are completely orthogonal. Therefore, we can apply the Pythagorean property for orthogonal vectors $||y||^2 = ||x_0 + (y - x_0)||^2 = ||x_0||^2 + ||y - x_0||^2$. By the non-negativity of norms, $||y - x_0||^2 \ge 0$. This immediately forces $||y||^2 \ge ||x_0||^2 \implies ||y|| \ge ||x_0||$. Thus, $x_0$ minimizes the norm. For the norm of $y$ to equal the minimum norm of $x_0$, the equation above dictates that $||y - x_0||^2 = 0$. By the non-degeneracy property of inner product spaces, $||y - x_0||^2 = 0$ if and only if $y - x_0 = 0$, which means $y = x_0$. Therefore, no other solution can have this minimum norm. $x_0$ is unique. $\blacksquare$

**Problem 4.6:**
Applying the preivous problem to $Ax = P_{Ran A}b$ show that
a) There exists a unique least square solution $x_0$ of $Ax = b$ minimizing the norm $||x||$.
b) $x_0 = P_{(Ker A)^\perp}x$ for any least square solution x of $Ax = b$.
**Solution:**
a) 
Applying the result of 4.5(a) to the system $Ax = P_{Ran A}b$, there exists a unique solution $x_0$ that minimizes the norm $||x||$ among all solutions to $Ax = P_{Ran A}b$. Because the solutions to $Ax = P_{Ran A}b$ are exactly the least squares solutions to $Ax = b$, $x_0$ uniquely minimizes the norm among all least squares solutions.

b)
Applying the result of 4.5(b) to the system $Ax = P_{Ran A}b$, this unique minimum norm solution $x_0$ is given by $x_0 = P_{(\ker A)^\perp}x$, where $x$ is _any_ solution to $Ax = P_{Ran A}b$. Thus, $x_0 = P_{(\ker A)^\perp}x$ for any least square solution $x$ of $Ax = b$. $\blacksquare$

**Problem 5.3:**
Let A be an $m \times n$ matrix. Show that $Ker A = Ker(A*A)$.
**Solution:**
Suppose $x \in Ker A$. By definition, $Ax = 0$ then. We see that $A*Ax = A*(0) = 0$ and so $x \in Ker(A*A)$. Therefore, $Ker A \subseteq Ker(A*A)$. Suppose $y \in Ker(A*A)$. By definition, $A*Ay = 0$. Notice $||Ay||^2 = (Ay, Ay) = (A*Ay, y) = (0, y) = 0$ and so $||Ay||^2 = 0$. It follows that since $||Ay|| \ge 0$ and $||Ay||^2 = 0$, it must be that $||Ay|| = 0$. This is true precisely when $Ay = 0$ and so $y \in Ker A$. Therefore, $Ker(A*A) \subseteq Ker A$. Because $Ker A \subseteq Ker(A*A)$ and $Ker(A*A) \subseteq Ker A$, we have $Ker A = Ker(A*A)$. $\blacksquare$

**Problem 5.6**
Let a matrix P be self-adjoint ($P* = P$) and let $P^2 = P$. Show that P is the matrix of an orthogonal projection. 
**Solution:**
For any $v \in V$, $v = v_1 + v_2$ where $v_1 \in Ran P$ and $v_2 \in Ran P^\perp$ since $V = Ran P \oplus Ran P^\perp$. Because $v_1 \in Ran P$, there must some x such that $Px = v_1$. We see that $Pv_1 = P^2x$ and because $P^2 = P$, we get $P^2x = Px = v_1$. Therefore, we see that $Pv_1 = v_1$. Notice $||Pv_2||^2 = (Pv_2, Pv_2) = (P*Pv_2, v_2)$ and since $P = P*$ we have $(P*Px_2, x_2) = (P^2v_2, v_2)$ and from $P^2 = P$ we get $(P^2v_2, v_2) = (Pv_2, v_2)$. Since $v_2 \in Ran P^\perp$, it must be that for any $y \in Ran P$ we have $(y, v_2) = 0$. Therefore, in particular, it must be that $(Pv_2, v_2) = 0$. It follows that $||Pv_2||^2 = (Pv_2, v_2) = 0$, meaning $||Pv_2|| = 0$. Then $Pv_2 = 0$. So, $Pv = P(v_1 + v_2) = Pv_1 + Pv_2 = v_1 + 0 = v_1$. Thus, P is an orthogonal projection. $\blacksquare$
