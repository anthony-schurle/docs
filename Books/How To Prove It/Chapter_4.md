# Chapter 4: Functions
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 4.0 Functions
---
### Definitions
- **Function**
  - Suppose F is a relation from A to B. Then F is a function from A to B if $\forall a \in A \exists !b \in B ((a, b) \in F)$. Denoted $F : A \to B$.
  - $b = f(a) \iff (a, b) \in f$.
  - $Ran(f) = \{f(a) | a \in A\}$.
  - Identity function given by identity relation.

### Theorems & Proofs
**Theorem 5.1.4**
Suppose f and g are functions from A to B. If $\forall a \in A(f(a) = g(a))$ then $f = g$.

**Theorem 5.1.5**
Suppose $f : A \to B$ and $g : B \to C$, then $g \circ f : A \to C$, and for any $a \in A$, the value of $g \circ f$ at a is given by $(g \circ f)(a) = g(f(a))$.

### References
- *Book Title* — Chapter X, Pages Y–239


## 4.1 One-To-One And Onto
---
### Definitions
- **One-To-One (Injection)**
  - Suppose $f : A \to B$. f is one-to-one if $\neg \exists a_1 \in A \exists a_2 \in A (f(a_1) = f(a_2) \land a_1 \ne a_2)$.
- **Onto (Surjection)**
  - Suppose $f : A \to B$. f is onto if $\forall b \in B \exists a \in A (f(a) = b)$.
- **Bijection**
  - Function that is a injection and surjection.

### Theorems & Proofs
**Theorem 5.2.3**
Suppose $f : A \to B$.
1. f is injective iff $\forall a_1 \in A \forall a_2 \in A (f(a_1) = f(a_2) \implies a_1 = a_2)$.
2. f is surjective iff $Ran(f) = B$.

**Theorem 5.2.5**
Suppose $f : A \to B$ and $g : B \to C$. As we saw in Theorem 5.1.5, it follows that $g \circ f : A \to C$.
1. If f and g are both one-to-one, then so is $g \circ f$.
2. If f and g are both onto, then so is $g \circ f$.

### References
- *Book Title* — Chapter X, Pages Y–249


## 4.2 Inverses Of Functions
---
### Theorems & Proofs
**Theorem 5.3.1**
Suppose $f : A \to B$. If f is bijective, then $f^{-1} : B \to A$.

**Theorem 5.3.2**
Suppose f is a function from A to B, and suppose that $f^{-1}$ is a function from B to A. Then $f^{-1} \circ f = i_A$ and $f \circ f^{-1} = i_B$.

**Theorem 5.3.3**
Suppose $f : A \to B$.
1. If there is a function $g : B \to A$ such that $g \circ f = i_A$, then f is injective.
2. If there is a function $g : B \to A$ such that $f \circ g = i_B$ then f is surjective.

**Theorem 5.3.4**
Suppose $f : A \to B$. Then the following statements are equivalent.
1. f is bijective.
2. $f^{-1} : B \to A$.
3. There is a function $g : B \to A$ such that $g \circ f = i_A$ and $f \circ g = i_B$.

**Theorem 5.3.5**
Suppose $f : A \to B$, $g : B \to A$, $g \circ f = i_A$, and $f \circ g = i_B$. Then $g = f^{-1}$.

### References
- *Book Title* — Chapter X, Pages Y–259


## 4.3 Closures
---
### Definitions
- **Closed**
  - Suppose $f : A \to A$ and $C \subseteq A$. C is closed under f if $\forall x \in C (f(x) \in C)$.
  - Extends to multiple variable functions.
- **Closure**
  - Suppose $f : A \to A$ and $B \subseteq A$. Then the closure of B under f is  $C \subseteq A$ such that:
  - $B \subseteq C$.
  - C is closed under f.
  - C is the smallest set satisfying the above two properties.
- **Binary Operation**
  - Function from $A \times A$ to $A$ written with symbol, such as addition.

### Theorems & Proofs
**Theorem 5.4.5**
Suppose that $f : A \to A$ and $B \subseteq A$. Then $B$ has a closure under f.

**Theorem 5.4.9**
Suppose that $f : A \times A \to A$ and $B \subseteq A$. Then $B$ has a closure under f.

### References
- *Book Title* — Chapter X, Pages Y–268


## 4.4 Images And Inverse Images: A Research Project
---
### Definitions
- **Image**
  - Suppose $f : A \to B$ and $X \subseteq A$. The image of X under f is $f(X) = \{f(x) | x \in X\}$.
- **Inverse Image**
  - Suppose $f : A \to B$ and $X \subseteq B$. The inverse image of X under f is $f^{-1}(X) = \{a \in A | f(a) \in X\}$.
  - Note: Not treated as a function.

### Theorems & Proofs
**Theorem 5.5.2**
Suppose $f : A \to B$, and W and X are subsets of A. Then $f(W \cap X) \subseteq f(W) \cap f(X)$. Furthermore, if f is one-to-one, then $f(W \cap X) = f(W) \cap f(X)$.

### Common Pitfalls
- Notational ambiguity between inverse function and inverse image is harmless.

### References
- *Book Title* — Chapter X, Pages Y–272
