## 7.0 Equinumerous Sets

**Problem 1**
Show that the following sets are denumerable.
a) $\mathbb{N}$.
b) The set of all even integers.
**Solution**
a)
Define the function $f : \mathbb{Z}^+ \to \mathbb{N}$ by $f(x) = x - 1$. Let $n \in \mathbb{N}$ be arbitrary. Notice $n + 1 \in \mathbb{Z}$ since $n \ge 0$. Then $f(n+1) = (n+1) - 1 = n$. Hence $f$ is surjective. Now let $f(a) = f(b)$ for $a, b \in \mathbb{Z}^+$. It follows that $f(a) = a - 1 = b - 1 = f(b)$. So, $a = b$, meaning $f$ is injective. Therefore, $\mathbb{N}$ is denumerable.

b)
Let such a set be called $C$. Define the function $f : \mathbb{Z}^+ \to C$ by $f(x) = \begin{cases} 2x & \text{if, x odd} \\ -x & \text{if, x even} \end{cases}$. Let $c \in C$ be arbitrary. Clearly, $c$ is either positive or negative. Case 1: $c$ positive. Notice $\frac{c}{2} \in \mathbb{Z}^+$ since $c$ is positive and even. Then $f(\frac{c}{2}) = 2(\frac{c}{2}) = c$. Case 2: $c$ negative. Notice $-c \in \mathbb{Z}+$ since $c$ is negative and an integer. Then $f(-c) = -(-c) = c$. Hence $f$ is surjective. Now let $f(a) = f(b)$ for $a, b \in \mathbb{Z}^+$. Four cases exist, depending on whether $a, b$ are even or odd. Case 1: $a$ and $b$ both even. Then $f(a) = -a = -b = f(b)$ so that $a = b$. Case 2: $a$ and $b$ are both odd. Then $f(a) = 2a = 2b = f(b)$ so that $a = b$. Case 3: $a$ even and $b$ odd. Then $f(a) = -a = 2b = f(b)$. A contradiction since $-a$ and $2b$ are both non-zero but opposite sign. Case 4: $a$ odd and $b$ even. Then $f(a) = 2a = -b = f(b)$. A contradiction since $2a$ and $-b$ are both non-zero but opposite sign. Hence $f$ is injective. Therefore, $C$ is denumerable. $\proofend$
