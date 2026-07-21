## 5.0 Proof By Mathematical Induction

**Problem 1**
Prove that for all $n \in \mathbb{N}$, $0 + 1 + 2 + ... + n = \frac{n(n+1)}{2}$.
**Solution**
Notice $0 = \frac{0(0 + 1)}{2}$ as desired. Let $n \in \mathbb{N}$ be arbitrary and suppose $0 + 1 + 2 + ... + n = \frac{n(n+1)}{2}$. Then $0 + 1 + 2 + ... + n + (n+1) = \frac{n(n+1)}{2} + (n+1)$. But $\frac{n(n+1)}{2} + (n+1) = \frac{2n + 2 + n(n+1)}{2} = \frac{(n+1)(n+2)}{2}$. Hence $0 + 1 + 2 + ... + n + (n+1) = \frac{(n+1)(n+2)}{2}$ as desired. $\proofend$


