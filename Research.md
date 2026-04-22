# Support Logic: A Working Paper

## Abstract

This paper develops a propositional framework in which formulas receive values in the interval `[0,1]`, interpreted as **degrees of support** rather than degrees of truth. The intended reading is:

- `1` = full support
- `0.5` = neutrality
- `0` = full support against

The framework is designed so that its support-`1` fragment reproduces ordinary classical propositional logic, while its interior support region models graded reasoning. The central structural idea is to separate:

1. **semantic support**, determined compositionally by the connectives, from  
2. **inferentially licensed support**, determined by rules that yield lower bounds rather than exact values.

This permits a hybrid picture: deductive reasoning is recovered at the endpoints, while graded support propagation below certainty is governed by explicitly inferential principles. The paper proves classical collapse at support `1`, shows that the current desiderata do not uniquely determine support-sensitive modus ponens, proves a semantic separation theorem establishing that the inferential layer is not reducible to the truth-functional support semantics, and proves that the current modus ponens rule cannot be represented by any standard t-norm.

---

## 1. Introduction

We introduce a propositional framework in which formulas are assigned values in the interval `[0,1]`, interpreted not as degrees of truth but as degrees of support.

The intended reading is:

- `1` = full support
- `0.5` = neutrality
- `0` = full support against

Thus values above `0.5` favor a formula, values below `0.5` count against it, and `0.5` represents a balanced state. The system is designed so that its support-`1` fragment reproduces ordinary classical propositional logic.

The central idea is to separate:

1. the **semantic support** of formulas, determined compositionally by the connectives, and  
2. the **inferentially licensed support** of conclusions, determined by rules that provide lower bounds rather than exact values.

This allows the framework to preserve classical certainty while also modeling graded support below the classical threshold.

A guiding philosophical reading is that the framework is meant to capture both **deductive** and **inductive** reasoning. Deductive reasoning is represented by endpoint support values `0` and `1`, while graded support in the interior of `[0,1]` models non-deductive transmission of support.

---

## 2. Language and Support Scale

We work in the ordinary language of propositional logic with:

- atomic formulas `P, Q, R, ...`
- negation `¬`
- conjunction `∧`
- disjunction `∨`
- implication `→`

### Definition 2.1 (Support Scale)

Support is measured on the interval `[0,1]`, with:

- `1` = full support
- `0.5` = neutrality
- `0` = full support against

Support values are **not** interpreted as degrees of truth.  
A formula with support `0.8` is strongly supported, but may still turn out false.

---

## 3. Semantic Clauses for the Connectives

### Definition 3.1 (Negation)

Negation reflects support across the neutral midpoint:

```text
supp(¬P) = 1 - supp(P)
```

So:

- if `supp(P) = 1`, then `supp(¬P) = 0`
- if `supp(P) = 0`, then `supp(¬P) = 1`
- if `supp(P) = 0.5`, then `supp(¬P) = 0.5`

Negation is therefore perfectly symmetric around `0.5`.

### Definition 3.2 (Conjunction)

Conjunction is minimal:

```text
supp(A ∧ B) = min(supp(A), supp(B))
```

This reflects the idea that a conjunction can be no more supported than its weaker conjunct.

### Definition 3.3 (Disjunction)

Disjunction is maximal:

```text
supp(A ∨ B) = max(supp(A), supp(B))
```

This reflects the idea that a disjunction inherits the strongest support available from its disjuncts, but does not gain extra support merely by combining two non-maximal claims.

### Definition 3.4 (Implication)

Implication is defined classically via disjunction:

```text
P → Q ≡ ¬P ∨ Q
```

Hence:

```text
supp(P → Q) = max(1 - supp(P), supp(Q))
```

This agrees with the classical truth table at support values `0` and `1`.

---

## 4. Basic Structural Consequences

### Proposition 4.1 (Double Negation)

For every formula `P`,

```text
supp(¬¬P) = supp(P)
```

#### Proof

By Definition 3.1,

```text
supp(¬¬P) = 1 - supp(¬P) = 1 - (1 - supp(P)) = supp(P).
```

∎

### Proposition 4.2 (Contradiction Bound)

For every formula `P`,

```text
supp(P ∧ ¬P) ≤ 0.5
```

#### Proof

By Definitions 3.1 and 3.2,

```text
supp(P ∧ ¬P) = min(supp(P), 1 - supp(P)).
```

For any `x ∈ [0,1]`, one has `min(x, 1-x) ≤ 0.5`. Hence the result follows. ∎

### Proposition 4.3 (Excluded Middle Bound)

For every formula `P`,

```text
supp(P ∨ ¬P) ≥ 0.5
```

#### Proof

By Definitions 3.1 and 3.3,

```text
supp(P ∨ ¬P) = max(supp(P), 1 - supp(P)).
```

For any `x ∈ [0,1]`, one has `max(x, 1-x) ≥ 0.5`. Hence the result follows. ∎

These propositions show:

- contradiction is never more than neutral
- excluded middle is never less than neutral

Thus the midpoint `0.5` acquires a natural structural significance.

---

## 5. Consequence Relation

A consequence relation specifies when a conclusion follows from a set of premises.

In classical logic, consequence is given either semantically (truth preservation across all interpretations) or syntactically (derivability via proof rules). In support logic, the consequence relation instead expresses what level of support a set of premises licenses for a conclusion.

### Definition 5.1 (Support-1 Consequence)

```text
Γ ⊨₁ φ
```

means: if every formula in `Γ` has support `1`, then `φ` has support `1`.

### Definition 5.2 (Graded Consequence)

```text
Γ ⊨_{≥r} φ
```

means: the premises in `Γ` license support at least `r` for `φ`.

The first notion captures classical collapse; the second captures genuinely graded inference.

---

## 6. Inferential Support as Lower-Bound Licensing

The semantic support of a formula does not by itself determine how arguments transmit support. Instead, inference rules license lower bounds on conclusions.

### Principle 6.1 (Lower-Bound Licensing)

If an argument yields support level `r` for a conclusion `Q`, the correct reading is:

```text
supp(Q) ≥ r
```

rather than

```text
supp(Q) = r.
```

This prevents repeated use of the same argument from artificially inflating support.

### Principle 6.2 (Aggregation by Maximum)

If multiple arguments license support for the same formula `Q`, then the resulting inferential support is the maximum of the licensed lower bounds.

So if:

- one argument licenses `supp(Q) ≥ r`
- another licenses `supp(Q) ≥ s`

then inferentially:

```text
supp(Q) ≥ max(r, s)
```

This ensures that certainty is never manufactured merely by repetition or accumulation of non-certain arguments.

---

## 7. Support-Sensitive Modus Ponens

Classically:

- `P`
- `P → Q`
- therefore `Q`

In support logic, modus ponens yields a lower bound.

### Definition 7.1 (Support-Sensitive Modus Ponens)

Given support for `P` and `P → Q`, define:

```text
MP(P, P → Q) = max(0.5, min(supp(P), supp(P → Q)))
```

and license:

```text
supp(Q) ≥ MP(P, P → Q).
```

Equivalently, in variable form:

```text
MP(a,b) = max(0.5, min(a,b)).
```

### Proposition 7.2 (Basic Behavior of MP)

The rule satisfies:

1. `MP(1,1) = 1`
2. `MP(0.5,0.5) = 0.5`
3. if either input is `0`, then the licensed support for `Q` is `0.5`

#### Proof

Immediate from the definition of `MP`. ∎

### Proposition 7.3 (No Certainty from Uncertainty)

```text
MP(P, P → Q) = 1
```

if and only if `supp(P) = 1` and `supp(P → Q) = 1`.

#### Proof

By definition,

```text
MP(P, P → Q) = max(0.5, min(supp(P), supp(P → Q))).
```

This equals `1` exactly when `min(supp(P), supp(P → Q)) = 1`, which occurs exactly when both arguments are `1`. ∎

Thus certainty is propagated, but never manufactured from uncertainty.

---

## 8. Generalized Classical Rules

### 8.1 Conjunction Elimination

Classically:

- from `P ∧ Q`, infer `P`
- from `P ∧ Q`, infer `Q`

Support version:

```text
supp(P) ≥ supp(P ∧ Q)
supp(Q) ≥ supp(P ∧ Q)
```

Since

```text
supp(P ∧ Q) = min(supp(P), supp(Q)),
```

this is exactly the support licensed by conjunction.

### 8.2 Disjunction Elimination

Classically:

- `P ∨ Q`
- `P → R`
- `Q → R`
- therefore `R`

Support version:

```text
supp(R) ≥ min(supp(P ∨ Q), max(supp(P → R), supp(Q → R)))
```

So the support for `R` is limited by:

- the support for the disjunction itself, and
- the strongest available route from either disjunct to `R`.

### 8.3 Negation Elimination

Classically:

- `P`
- `¬P`
- therefore contradiction

Support version:

```text
supp(P ∧ ¬P) = min(supp(P), 1 - supp(P))
```

So the contradiction generated from `P` is exactly the minimum of the support for `P` and the support against it.

### 8.4 Negation Introduction

Negation is already built into the semantics:

```text
supp(¬P) = 1 - supp(P)
```

So negation introduction is not taken as a separate primitive inference rule.

### 8.5 Conjunction Introduction

Classically:

- `P`
- `Q`
- therefore `P ∧ Q`

Support version:

```text
supp(P ∧ Q) ≥ min(supp(P), supp(Q))
```

Since conjunction is already semantically defined by this minimum, conjunction introduction is built directly into the connective semantics.

### 8.6 Disjunction Introduction

Classically:

- `P`
- therefore `P ∨ Q`

and symmetrically from `Q`.

Support version:

```text
supp(P ∨ Q) ≥ supp(P)
supp(P ∨ Q) ≥ supp(Q)
```

Since disjunction is already semantically defined by the maximum, disjunction introduction is likewise built directly into the connective semantics.

### 8.7 Modus Tollens

Classically:

- `P → Q`
- `¬Q`
- therefore `¬P`

Support version:

```text
supp(¬P) ≥ MT(P → Q, ¬Q) = max(0.5, min(supp(P → Q), supp(¬Q)))
```

Equivalently, since `supp(¬Q) = 1 - supp(Q)`,

```text
supp(¬P) ≥ max(0.5, min(supp(P → Q), 1 - supp(Q)))
```

### 8.8 Hypothetical Syllogism

Classically:

- `P → Q`
- `Q → R`
- therefore `P → R`

Support version:

```text
supp(P → R) ≥ max(0.5, min(supp(P → Q), supp(Q → R)))
```

So the composed implication is limited by the weaker of the two implications, but never falls below neutrality by inference alone.

### 8.9 Explosion

Classically:

- from contradiction, infer any formula

Support version:

- rejected in unrestricted form

Contradiction may contribute support, but it never yields absolute truth unless it already has support `1`.

Since contradiction is always at most `0.5` in the present framework, explosion does not occur.

---

## 9. Classical Collapse

### Theorem 9.1 (Classical Collapse at Support 1)

If all premises in a classical propositional argument have support `1`, then every conclusion classically derivable from them also has support `1`.

#### Proof Sketch

This follows from the support behavior of the connectives and rules at the endpoints:

- `supp(¬P) = 1 - supp(P)`, so negation matches classical endpoint behavior
- `supp(P ∧ Q) = min(supp(P), supp(Q))`, so conjunction is `1` exactly when both conjuncts are `1`
- `supp(P ∨ Q) = max(supp(P), supp(Q))`, so disjunction is `1` exactly when at least one disjunct is `1`
- `supp(P → Q) = max(1 - supp(P), supp(Q))`, so implication matches the classical truth table at support `0` and `1`
- support-sensitive modus ponens yields support `1` for `Q` exactly when both `P` and `P → Q` have support `1`
- support-sensitive modus tollens behaves analogously
- the introduction and elimination rules above align with their classical forms at support `1`

Therefore, the support-`1` fragment reproduces ordinary classical propositional logic. ∎

### Corollary 9.2 (Deductive Endpoint Fragment)

The restriction of the system to the support endpoints `{0,1}` forms a deductive fragment equivalent to classical propositional logic.

---

## 10. Non-Uniqueness of Support-Sensitive Modus Ponens

A natural question is whether the current desiderata uniquely determine the support-sensitive modus ponens rule.

Our current candidate is:

```text
MP(a,b) = max(0.5, min(a,b)).
```

This satisfies:

- `MP(1,1) = 1`
- `MP(0.5,0.5) = 0.5`
- if either input is at or below neutrality, the conclusion does not rise above neutrality
- certainty is never manufactured from uncertainty
- monotonicity in each argument

### Proposition 10.1

The current desiderata do **not** uniquely determine the support-sensitive modus ponens rule.

#### Proof

Let

```text
f(a,b) = max(0.5, min(a,b))
```

and define

```text
g(a,b) = 0.5                        if a ≤ 0.5 or b ≤ 0.5
g(a,b) = 0.5 + 2(a-0.5)(b-0.5)      if a > 0.5 and b > 0.5.
```

Then:

- `g(1,1) = 1`
- `g(0.5,0.5) = 0.5`
- if either input is at or below neutrality, `g(a,b) = 0.5`
- `g(a,b) = 1` only when `a = b = 1`
- `g` is monotone in each variable

So `g` satisfies the same basic desiderata as `f`.

But the two rules are different. For example,

```text
f(0.8,0.9) = 0.8
```

whereas

```text
g(0.8,0.9) = 0.5 + 2(0.3)(0.4) = 0.74.
```

So `f ≠ g`.

Therefore the current desiderata do not uniquely determine the support-sensitive modus ponens rule. ∎

### Consequence 10.2

To justify the rule

```text
MP(a,b) = max(0.5, min(a,b)),
```

one needs an additional principle.

A natural candidate is:

### Bottleneck Principle for Modus Ponens

When both the premise `P` and the implication `P → Q` are supported above neutrality, the support licensed for `Q` is exactly the weaker of the two support values.

Under this additional principle, the support-sensitive modus ponens rule is uniquely forced to be

```text
MP(a,b) = max(0.5, min(a,b)),
```

since:

- below neutrality, support does not propagate positively
- above neutrality, the weaker support value determines the licensed conclusion
- at full support, certainty propagates exactly

---

## 11. Semantic Separation Theorem

The inferential rule for modus ponens is not reducible to the truth-functional support semantics alone.

### Definition 11.1 (Purely Semantic Lower Bound)

Let the truth-functional support semantics be fixed by the clauses of Section 3. For real numbers `a,b ∈ [0,1]`, define the purely semantic lower bound for `Q` from the constraints

```text
supp(P) ≥ a
supp(P → Q) ≥ b
```

to be

```text
LB_sem(a,b) = inf { supp(Q) : supp(P) ≥ a and supp(P → Q) ≥ b }.
```

### Proposition 11.2 (Exact Semantic Lower Bound)

For the support semantics of this framework,

```text
LB_sem(a,b) =
  0    if a + b ≤ 1
  b    if a + b > 1.
```

#### Proof

Recall that

```text
supp(P → Q) = max(1 - supp(P), supp(Q)).
```

We compute the infimum in two cases.

**Case 1: `a + b ≤ 1`.**

Then `a ≤ 1-b`. Set `supp(P)=a` and `supp(Q)=0`. Then

```text
supp(P → Q) = max(1-a,0) = 1-a ≥ b.
```

So the premises can hold while `supp(Q)=0`. Hence

```text
LB_sem(a,b) = 0.
```

**Case 2: `a + b > 1`.**

Then `a > 1-b`. If `supp(P) ≥ a`, then

```text
1 - supp(P) ≤ 1-a < b.
```

So in order for

```text
supp(P → Q) = max(1 - supp(P), supp(Q))
```

to be at least `b`, it must be that

```text
supp(Q) ≥ b.
```

Thus every valuation satisfying the premises forces `supp(Q) ≥ b`.

This bound is sharp: set `supp(P)=a` and `supp(Q)=b`. Then

```text
supp(P → Q) = max(1-a,b) = b
```

because `b > 1-a`.

Hence

```text
LB_sem(a,b) = b.
```

This proves the proposition. ∎

### Theorem 11.3 (Deductive–Inductive Separation)

Let

```text
LB_inf(a,b) = MP(a,b) = max(0.5, min(a,b)).
```

Then

```text
LB_inf ≠ LB_sem.
```

Hence the graded inferential layer is not reducible to the truth-functional support semantics.

#### Proof

Take `a=0.8`, `b=0.2`. Then `a+b=1`, so by Proposition 11.2,

```text
LB_sem(0.8,0.2) = 0.
```

But the inferential rule gives

```text
LB_inf(0.8,0.2) = max(0.5, min(0.8,0.2)) = 0.5.
```

So the two lower bounds differ.

For a converse contrast, take `a=0.6`, `b=0.7`. Then `a+b>1`, so

```text
LB_sem(0.6,0.7) = 0.7,
```

while

```text
LB_inf(0.6,0.7) = max(0.5, min(0.6,0.7)) = 0.6.
```

Thus the inferential rule is not merely stronger or weaker than the semantic lower bound in general; it is a genuinely distinct inferential policy.

Therefore the graded inferential layer is not determined by the truth-functional support semantics alone. ∎

### Corollary 11.4

The framework has two formally distinct layers:

1. an **endpoint deductive layer**, equivalent to classical propositional logic; and  
2. an **interior graded layer**, governed by extra-semantic inferential licensing.

This supports the intended reading of the system as a hybrid of deductive and inductive reasoning.

---

## 12. Representation Failure for T-Norm Semantics

A natural question is whether support-sensitive modus ponens could still be represented by some standard fuzzy conjunction operator.

### Theorem 12.1 (No T-Norm Representation)

There is no t-norm `T : [0,1]^2 → [0,1]` such that

```text
T(a,b) = MP(a,b) = max(0.5, min(a,b))
```

for all `a,b ∈ [0,1]`.

#### Proof

Every t-norm `T` satisfies:

1. monotonicity in each variable  
2. identity at `1`, that is,
   ```text
   T(x,1) = x
   ```
3. hence the upper bound
   ```text
   T(x,y) ≤ min(x,y).
   ```

Now evaluate the present modus ponens rule at `a=0.8`, `b=0.2`:

```text
MP(0.8,0.2) = max(0.5, min(0.8,0.2)) = 0.5.
```

But any t-norm must satisfy

```text
T(0.8,0.2) ≤ min(0.8,0.2) = 0.2.
```

So no t-norm can equal `MP` on all inputs. ∎

### Short Proof Variant

Any t-norm satisfies

```text
T(0,1) = 0
```

because `1` is the identity.

But the present rule gives

```text
MP(0,1) = max(0.5, min(0,1)) = 0.5.
```

Contradiction. ∎

### Corollary 12.2

The support-sensitive modus ponens rule is not representable as standard fuzzy conjunction.

### Interpretive Consequence 12.3

Above neutrality, when `a,b ≥ 0.5`,

```text
MP(a,b) = min(a,b),
```

so the rule behaves like a bottleneck conjunction. But below neutrality, the rule imposes a **neutrality floor**, and this is exactly what blocks representation by a t-norm.

So the rule has a hybrid structure:

- **classical** at the endpoints,
- **bottleneck/min-like** above neutrality,
- **non-t-norm inductive floor behavior** below neutrality.

---

## 13. Philosophical Interpretation

The framework is philosophically motivated by the idea that support should not be identified with truth. A proposition may be strongly supported yet false, weakly supported yet true, or neutrally balanced between support and support-against.

Three interpretive features are central.

### 13.1 Midpoint Neutrality

The midpoint `0.5` is not merely a numerical convention. It is structurally marked by the logic itself:

- contradiction never exceeds `0.5`
- excluded middle never falls below `0.5`
- negation fixes `0.5`
- inference below certainty is constrained by `0.5`

Thus neutrality functions as a genuine logical boundary.

### 13.2 Lower-Bound Licensing

The framework does not identify inference with exact value production. Instead, inference licenses lower bounds. This reflects the idea that reasoning often tells us what level of support we are entitled to claim, not the precise total support a conclusion possesses.

### 13.3 Deductive and Inductive Roles

At supports `0` and `1`, the framework collapses to ordinary classical reasoning. In the interior, however, support propagation depends on additional inferential principles not fixed by truth-functionality alone. This provides a natural formal distinction between:

- **deductive consequence**, modeled by endpoint preservation, and
- **inductive or ampliative support transmission**, modeled by graded lower-bound licensing.

---

## 14. Assessment of the Current Framework

At its current stage, the framework has several clear strengths.

### Strengths

1. It gives a clean and intuitive support-based reading of values in `[0,1]`.
2. It identifies a mathematically meaningful neutrality point at `0.5`.
3. It recovers classical propositional logic at support `1`.
4. It sharply distinguishes compositional semantics from inferential licensing.
5. It yields nontrivial representation theorems showing that the inferential layer is not reducible to the truth-functional support semantics or to standard t-norm aggregation.

### Open Issues

1. The connective semantics themselves closely resemble familiar many-valued/fuzzy semantics.
2. The current generalized rules beyond modus ponens would benefit from a unified proof-theoretic presentation.
3. The intended interpretation of graded consequence should be developed further, especially for multi-premise arguments and competing bodies of evidence.
4. The framework would be strengthened by comparisons with existing support/evidence logics and paraconsistent annotated systems.
5. A completeness or representation theorem for the full inferential system would significantly deepen the project.

---

## 15. Future Directions

The following directions appear especially important.

### 15.1 Axiomatization and Proof Theory

State the system as a proof calculus with explicit rule schemas, derivability notion, and metatheorems.

### 15.2 Comparison Theorems

Compare the framework directly with:

- standard fuzzy systems using min/max and Kleene–Dienes implication,
- evidence-support systems,
- paraconsistent annotated logics,
- bilattice-style and uncertainty-oriented nonclassical logics.

### 15.3 Representation and Completeness

Investigate whether the inferential layer admits characterization by a special class of support-licensing operators, and whether a completeness theorem can be proved for the resulting consequence relation.

### 15.4 Applications

Because the framework distinguishes support, support-against, neutrality, and certainty, it may be promising for formal epistemology, argumentation, evidential reasoning, and AI systems that need graded but non-probabilistic support tracking.

---

## 16. Conclusion

The framework developed here has four central features:

1. a symmetric support scale on `[0,1]` with neutrality at `0.5`,  
2. min/max connective semantics together with midpoint negation,  
3. inferential lower-bound licensing aggregated by maximum, and  
4. a support-sensitive modus ponens with a neutrality floor.

This yields:

- contradiction never above neutrality,
- excluded middle never below neutrality,
- no certainty from uncertainty,
- recovery of classical logic at support `1`,
- non-uniqueness of the current modus ponens rule under the present desiderata,
- separation of graded inference from pure truth-functional semantics, and
- failure of representation by any t-norm.

Accordingly, the system is best understood not merely as a many-valued semantics, but as a hybrid support logic whose endpoint fragment is deductive and whose interior fragment is governed by extra-semantic graded support transmission.

The main remaining question is not whether the framework is coherent—it is—but how far its inferential layer is genuinely distinct from already existing many-valued, fuzzy, evidential, and paraconsistent systems. The present results give a strong start by proving two genuine separation results, and they suggest that the philosophically most distinctive feature of the framework lies not in the connective semantics alone, but in the explicit separation between semantic support and inferentially licensed support.

---

## Appendix A. Key Formulas

### Connective Semantics

```text
supp(¬P) = 1 - supp(P)
supp(P ∧ Q) = min(supp(P), supp(Q))
supp(P ∨ Q) = max(supp(P), supp(Q))
supp(P → Q) = max(1 - supp(P), supp(Q))
```

### Core Inferential Rules

```text
MP(a,b) = max(0.5, min(a,b))
MT(a,b) = max(0.5, min(a,b))
```

### Semantic Lower Bound from `supp(P) ≥ a` and `supp(P → Q) ≥ b`

```text
LB_sem(a,b) =
  0    if a + b ≤ 1
  b    if a + b > 1
```

### Separation Witnesses

```text
LB_sem(0.8,0.2) = 0
LB_inf(0.8,0.2) = 0.5

LB_sem(0.6,0.7) = 0.7
LB_inf(0.6,0.7) = 0.6
```

### T-Norm Failure Witness

```text
MP(0,1) = 0.5
```

but every t-norm `T` satisfies

```text
T(0,1) = 0.
```