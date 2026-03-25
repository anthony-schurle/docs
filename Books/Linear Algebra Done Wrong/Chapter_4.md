# Chapter 4: Inner Product Spaces
---
## Summary
---
> Briefly explain what the chapter is about (2–4 sentences). Focus on the goals, main topics, and why this chapter matters.

## 4.0 Inner Product in $\mathbb{R}^n$ and $\mathbb{C}^n$. Inner Product Spaces.
---
### Key Concepts
- **Inner Product Spaces**:
  - Conjugate Symmetry - $(x, y) = \overline{(y, x)}$.
  - Linearity - $(\alpha x + \beta y, z) = \alpha(x, z) + \beta(y, z)$ for all vectors $x, y, z$ and scalars $\alpha, \beta$.
  - Non-negativity - $(x, x) \ge 0$ for all x.
  - Non-degeneracy - $(x, x) = 0$ iff $x = 0$.
  - Inner product is a function, $f : \{(x, y) | \text{x and y are vectors}\} \to \mathbb{F}$, satisfying these properties.
  - Inner product space is a function along with a vector space.

### Definitions
- **Norm**
  - The norm of $x \in \mathbb{R}^n$ is $||x|| = \sqrt{x_1^2 + x_2^2 + ... + x_n^2} = \sqrt{(x, x)}$.
  - The norm of $z \in \mathbb{C}^n$ is $||z||^2 = \sum_{k = 1}^n |z_k|^2$.
- **Inner Product**
  - The inner product of $x, y \in \mathbb{R}^n$ is $(x, y) := x_1y_1 + x_2y_2 + ... + x_ny_n = y^T x = x^Ty$.
  - The standard inner product of $z, w \in \mathbb{C}^n$ is $(z, w) := \sum_{k=1}^n z_k \overline{w_k} = w*z$. (motivated by the reals)
- **Hermitian Adjoint**
  - Adjoint of matrix A denoted by $A* = \overline{A}^T$.

### Algorithms
**Algorithm Name**
Description.
```pseudo
1. Step 1
2. Step 2
3. Step 3
```
### Code Snippets
**Snippet Name**
Description.
```program
// code
```
### Theorems & Proofs
**Theorem Name**
Proof.
### Formulas
**Formula Name**
Description.
$$
Equation
$$
### Visual Aids
| Header | Header |
| - | - |
| Content | Content |
![Diagram]()
### Examples
**Example Title**
**Problem:**
Problem Statement.
**Solution:**
Solution Statement.
### Notable Quotes
> “Notable quote."
### Common Pitfalls
- Pitfall 1.
### Related Links
- [Link]()
### References
- *Book Title* — Chapter X, Pages Y–Z

- [Author(s), "Paper or Article Title," Journal or Conference Name, Year]() 

- [Related Chapter in This Wiki]()  

- [Official Specification or Standard Document (PDF/URL)]()  

- Class Lecture ([Link]())