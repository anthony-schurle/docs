# Computation as Mathematical Structure

### On computation and proof as two descriptions of the same mathematical phenomenon

_Working essay — draft in progress_

---

## I. The standard picture and its assumption

The standard introduction to theoretical computer science proceeds as follows: define a machine, specify what it can do in bounded time or space, and call the resulting collection of problems a complexity class. Complexity, on this view, is a property of machines. It is defined relative to a computational model, and the mathematical content is downstream of an engineering artifact.

This picture carries a quiet assumption — that computation is something we built, and complexity is something we measured about what we built. Mathematics enters to describe the construction, not to constitute it.

The position developed here is different. Computation is not an artifact that mathematics is applied to. It is a mathematical phenomenon as foundational as proof itself — intrinsic to the structure of formal reasoning, not imported from engineering. To see why, it helps to start not with machines or complexity classes, but with what a proof actually is.

---

## II. Proofs are constructions

A proof is not merely a certificate that something is true. It is a construction — a finite sequence of steps that builds a conclusion out of prior steps, where each step depends on what came before and the sequence as a whole constitutes the mathematical object. The building is the proof. The sequence is not incidental scaffolding that can be discarded once the result is secured. Remove the steps and there is no proof, only an assertion.

This is true regardless of whether the proof is constructive in the technical sense. A classical proof by contradiction is still a construction — you construct a sequence of steps that derives absurdity from the negation. An existence proof via the probabilistic method constructs a sequence of inequalities and expectations that forces the conclusion. The algorithm is always present. Constructive proofs make the computational content explicit and extractable, but classical proofs do not escape the algorithmic character. They simply do not advertise it.

The consequence is immediate: a proof is an algorithm. Not analogous to one, not translatable into one — it is one. A finite sequence of steps, each dependent on prior steps, building toward a conclusion. This is precisely what computation is. The parallel between proof theory and computation is not a surprising theorem about two independently defined objects. It is a consequence of what both things fundamentally are, prior to any formalism.

---

## III. The correspondence made exact — Curry-Howard

The Curry-Howard correspondence makes the identification precise in a specific formal setting: proofs in intuitionistic logic correspond directly to programs in typed lambda calculus, and proof normalization — simplifying a proof to its normal form — corresponds exactly to computation. A program of type A → B is literally a proof that given A you can construct B. The proposition is baked into the type.

One might object that computation lacks propositional content — that a program just transforms inputs to outputs without proving anything. But this does not hold up. Every computation that halts establishes a relationship between its input and output, and that relationship is a proposition. Showing that 1 + 2 + 3 = 6 is a proposition. A sorting algorithm witnesses that a certain permutation relationship holds between input and output. The proposition is implicit, not absent. What matters is that the sequence of steps depends on the logical structure at each stage, whether or not that structure is explicitly stated. The steps are constructed, and constructions carry propositional content by their nature.

Curry-Howard is sometimes presented as a surprising discovery — a hidden connection between two separate fields. The framing here makes it feel inevitable. Of course proofs and programs correspond. They were always the same kind of thing.

---

## IV. The distinction between proof and computation is one of emphasis

If proof and computation are the same phenomenon, why do proof theory and the theory of computation feel like different subjects? The answer is that they foreground different aspects of the same underlying object.

Proof theory foregrounds the logical structure — what propositions are used, how they relate, what the derivation establishes. Resource cost is present but secondary. Computation foregrounds the process and its cost — how many steps, in what order, at what resource expenditure. The logical content is present but implicit.

Both are aspects of structured sequential process. Both involve steps that are ordered, each dependent on prior steps, building toward a conclusion. Both have resource cost in the length or number of steps required. Neither aspect is absent in either case — the emphasis simply differs.

This is why the distinction is methodological and historical rather than ontological. Proof theory and computation theory developed as separate disciplines with different motivations and different notations. But they study the same mathematical object. Logic asks what is true. Proof theory and computation both ask how truth is reached and at what cost — which is why their deep theory converges, and why the Curry-Howard correspondence is an identification rather than a mere analogy.

---

## V. Descriptive complexity — the reversal

With this foundation in place, descriptive complexity takes on its full significance. Rather than asking what a machine computes, it asks: what logic is required to express a complexity class? The answer, in the fundamental cases, is exact.

**Fagin's theorem (1974).** A property of finite structures is in NP if and only if it is expressible in existential second-order logic.

**Immerman–Vardi theorem (1982–87).** On ordered finite structures, a property is in PTIME if and only if it is expressible in first-order logic with a least fixed point operator.

These are exact correspondences between logical expressibility and computational tractability. The machine has been eliminated from the definition. What remains is pure structure — a complexity class characterized entirely by the expressive power of a formal language over finite mathematical objects. Machines do not define the classes; logic reveals them.

The Immerman–Vardi theorem carries a qualification that is not incidental: it requires ordered structures. Without a linear order on the domain, first-order logic with least fixed point does not capture PTIME. Whether any logic captures PTIME on unordered structures remains one of the central open problems in finite model theory.

This is philosophically significant. It shows that computation is not simply reducible to logical expressibility — computation brings something logic does not inherently contain. That something is order: a canonical notion of sequence, of first step and next step, of process unfolding. Logic over unordered structures is indifferent to permutation. Computation is not. But this is exactly what section II established — order is constitutive of proof too. A proof without a sequence of steps is not a proof. The order requirement in descriptive complexity does not separate computation from mathematics. It locates computation precisely alongside proof theory, as one of the foundational notions about structured sequential process that logic alone cannot capture.

---

## VI. Objections

**Resource constraints are not physical contamination.** A natural objection holds that complexity theory imports something non-mathematical — time, physical steps, resource bounds — that pure mathematics does not contain. This misreads where resource constraints come from. Mathematics already contains hard limits on formal reasoning with no physical content. Gödel's incompleteness theorems establish that no sufficiently powerful formal system can prove all truths about itself. Turing's undecidability results establish that certain questions cannot be resolved by any formal procedure. These are mathematical facts about the limits of formal reasoning, with no reference to hardware.

Time complexity is continuous with this tradition. The question of whether a property is decidable in polynomial time is a question about how many formal steps are required to reach a conclusion — not about how fast a physical device runs. It is a question about construction length, and construction length is a mathematical object. Proof complexity studies exactly this: the relationship between logical provability and the lengths of the constructions required.

**Model dependence is parallel to definition dependence.** A more serious objection holds that complexity classes are defined relative to a computational model — Turing machines, Boolean circuits, RAM machines — and different models yield different constants or classes. Pure mathematical objects do not have this dependence.

But model dependence is already present throughout mathematics under a different name: dependence on definitions and axioms. There are multiple inequivalent definitions of dimension. There are multiple foundations for mathematics — ZFC, constructive type theory, categorical foundations — that yield different theorems. Choosing a computational model is choosing a definition. The mathematical content lives above the choice, just as algebraic theorems live above the choice of representation for a group.

Moreover, descriptive complexity largely dissolves model dependence by design. A logical characterization of a complexity class is model-independent by its nature. The statement that NP equals existential second-order logic does not mention Turing machines. The logical view is precisely the level of abstraction at which computation becomes model-independent — the same move abstract algebra makes when it stops caring about how a group is represented.

---

## VII. The emerging picture

What emerges is a precise and strong position. Computation is foundational to mathematics not because complexity theory is a branch of pure mathematics, or because complexity classes happen to have logical characterizations, but because proof — the most basic activity of mathematics — has always been computation. A proof is a construction. A construction is an algorithm. The identification is prior to any theorem, prior to Curry-Howard, prior to descriptive complexity. Those results make it precise and visible. They do not create it.

Logic, proof, and computation are three aspects of formal reasoning, each foregrounding something different. Logic foregrounds structure and truth. Proof theory foregrounds derivation — the sequential construction of truth from prior steps. Computation foregrounds process and resource cost — the ordered steps required and their number. None fully reduces to the others. The order requirement in descriptive complexity shows that computation is not simply logic. But all three are aspects of the same underlying mathematical reality, and the project of understanding their relationships precisely is itself a central part of the foundations of mathematics.

This is not a project of applying mathematics to computers. It is mathematics understanding itself. Mathematics has traditionally treated the 'proof' as a ladder to be kicked away once the theorem is reached. The computational view reverses this: the ladder _is_ the mathematical object of interest. The theorem is merely the height at which the ladder ends.

---

_This essay is a working document. Arguments should be refined as technical foundations develop — particularly after serious engagement with finite model theory, proof complexity, and the Curry-Howard correspondence in detail._