**Problem**
Let $A_0$ be the closed interval $[0, 1]$ in $\mathbb{R}$. Let $A_1$ be the set obtained from $A_0$ by deleting its middle third $(\frac{1}{3}, \frac{2}{3})$. Let $A_2$ be the set obtained from $A_1$ by deleting its middle thirds $(\frac{1}{9}, \frac{2}{9})$ and $(\frac{7}{9}, \frac{8}{9})$. In general, define $A_n$ by the equation $A_n = A_{n-1} - \bigcup_{k=0}^\infty (\frac{1+3k}{3^n}, \frac{2+3k}{3^n})$. The intersection $C = \bigcap_{n \in Z_{+}}A_n$ is called the Cantor set; it is a subspace of $[0, 1]$.
a) Show that C is totally disconnected.
b) Show that C is compact.
c) Show that each set $A_n$ is a union of finitely many disjoint closed intervals of length $\frac{1}{3^n}$; and show that the end points of these intervals lie in C.
d) Show that C has no isolated points.
e) Conclude that C is uncountable.
**Solution**
c)

We prove this by induction. For $n=0$, $A_0=[0,1]$, which is a single closed interval of length $1=3^0$. Assume $A_{n-1}$ is a union of $2^{n-1}$ pairwise disjoint closed intervals, each of length $3^{-(n-1)}$. Passing from $A_{n-1}$ to $A_n$ deletes the open middle third of each such interval. Thus an interval $[a,b]$ with $b-a=3^{-(n-1)}$ is replaced by $\left[a,a+\frac{b-a}{3}\right]\cup \left[b-\frac{b-a}{3},b\right]$, two closed intervals of length $\frac{1}{3}\cdot 3^{-(n-1)}=3^{-n}$. Therefore $A_n$ is a union of $2^n$ pairwise disjoint closed intervals, each of length $3^{-n}$. Now let $x$ be an endpoint of one of these intervals. At later stages, only open middle thirds are deleted, so endpoints are never removed. Hence $x\in A_m$ for every $m\ge n$, and also $x\in A_m$ for every $m<n$ since the sets are nested. Therefore $x\in \bigcap_{m\ge 0}A_m=C$. $\proofend$

a)

Let $Y\subset C$ be connected. Suppose, for contradiction, that $Y$ contains two distinct points $x<y$. Choose $n$ large enough that $3^{-n}<y-x$. By part c), $A_n$ is a finite union of pairwise disjoint closed intervals, each of length $3^{-n}$. Since $x,y\in C\subset A_n$, but no interval of $A_n$ has length as large as $y-x$, the points $x$ and $y$ cannot lie in the same interval component of $A_n$. Hence some deleted open interval lies between them, so there exists $z\in(x,y)$ such that $z\notin A_n$, and therefore $z\notin C$ (by construction). Now $Y\cap(-\infty,z)$ and $Y\cap(z,\infty)$ are disjoint nonempty sets whose union is $Y$; they are open in $Y$ because $(-\infty,z)$ and $(z,\infty)$ are open in $\mathbb R$. Hence they form a separation of $Y$, contradicting the assumption that $Y$ is connected. Therefore no connected subspace of $C$ contains two distinct points, so $C$ is totally disconnected. $\proofend$

b)

Each $A_n$ is a finite union of closed intervals, so each $A_n$ is closed in $\mathbb R$ by Theorem 17.1. Therefore $C=\bigcap_{n\ge 0}A_n$ is closed in $\mathbb R$, again by Theorem 17.1. Since $C\subset[0,1]$, it follows that $C$ is closed as a subspace of $[0,1]$ by Theorem 17.2. By Theorem 27.1, closed intervals in $\mathbb R$ are compact, so $[0,1]$ is compact. By Theorem 26.2, every closed subspace of a compact space is compact. Therefore $C$ is compact. $\proofend$

d)

Let $x\in C$, and let $\varepsilon>0$. Choose $n$ such that $3^{-n}<\varepsilon$. Since $x\in C\subset A_n$, the point $x$ lies in one of the closed intervals $I_n$ making up $A_n$. By part c), both endpoints of $I_n$ lie in $C$. Since $I_n$ has positive length $3^{-n}$, at least one endpoint $y$ of $I_n$ is different from $x$. Then $y\in C$ and $|x-y|\le 3^{-n}<\varepsilon$. Therefore every $\varepsilon$-neighborhood of $x$ contains a point $y\in C$ with $y\neq x$. Hence $x$ is not isolated. Since $x\in C$ was arbitrary, $C$ has no isolated points. $\proofend$

e)

For each infinite sequence $(a_1,a_2,a_3,\dots)$ with $a_i\in\{0,2\}$, define $x=\sum_{i=1}^{\infty}\frac{a_i}{3^i}$. We first show that $x\in C$. Fix $n\in\mathbb Z_+$. Let $s_n=\sum_{i=1}^{n}\frac{a_i}{3^i}$. Then $x=s_n+\sum_{i=n+1}^{\infty}\frac{a_i}{3^i}$, and since each $a_i\in\{0,2\}$, we have $0\le \sum_{i=n+1}^{\infty}\frac{a_i}{3^i}\le \sum_{i=n+1}^{\infty}\frac{2}{3^i}=\frac{1}{3^n}$. Hence $x\in\left[s_n,s_n+\frac{1}{3^n}\right]$. By the description of the intervals in part c), this interval is one of the closed intervals making up $A_n$. Therefore $x\in A_n$. Since $n$ was arbitrary, $x\in \bigcap_{n\ge 0}A_n=C$. Now suppose two sequences first differ at index $m$. Then one has digit $0$ and the other has digit $2$ at the $m$-th place. The difference contributed at that digit is $\frac{2}{3^m}$, while the largest possible difference contributed by all later digits is $\sum_{i=m+1}^{\infty}\frac{2}{3^i}=\frac{1}{3^m}$. Since $\frac{2}{3^m}>\frac{1}{3^m}$, the two sums cannot be equal. Thus the map from $\{0,2\}^{\mathbb Z_+}$ into $C$ is injective. The set $\{0,2\}^{\mathbb Z_+}$ is uncountable. Therefore $C$ contains an uncountable subset, so $C$ is uncountable. $\proofend$
