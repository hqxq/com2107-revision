
# 📚 Bridging Propositional and Predicate Logic: A Complete Glossary

This glossary provides a structured, side-by-side comparison of propositional and predicate logic, building your understanding layer by layer.

---

## 🧱 Layer 1: Basic Elements — What Are We Even Talking About?

| Concept | **Propositional Logic** | **Predicate Logic** |
|--------|--------------------------|----------------------|
| **Atomic formula** | Just a single variable like `p`, `q`, `r`. It stands for a whole proposition ("It is raining"). | A predicate applied to terms, like `P(a)`, `Loves(x, y)`, `TallerThan(John, x)` — expresses something about objects. |
| **Language** | Built from propositional variables + connectives (`∧`, `∨`, `→`, `¬`) | Built from **predicates**, **functions**, **constants**, and **quantifiers** (`∀`, `∃`) as well as the same connectives |
| **Formula** | Propositional combinations like `p ∧ ¬q → r` | Quantified formulas like `∀x (Man(x) → Mortal(x))`, or open ones like `P(x)` |

---

## 🧠 Layer 2: Interpretation and Meaning

| Concept | **Propositional Logic** | **Predicate Logic** |
|--------|--------------------------|----------------------|
| **Valuation (v)** | A function assigning `true` or `false` to each propositional variable. E.g. `v(p) = true`, `v(q) = false`. | An **assignment** of objects to variables (`v(x) = 7`), and a **structure `𝔄`** that tells us what predicates, functions, and constants mean. |
| **Model** | A valuation `v` that makes a formula (or set of formulas) true. | A **pair** `(𝔄, v)` — the structure and the variable assignment — that makes the formula true. |
| **Truth** | `v ⊨ φ` means φ is true under valuation `v`. | `𝔄 ⊨ᵥ φ` means φ is true in structure `𝔄` under assignment `v`. If φ has no free variables, just write `𝔄 ⊨ φ`. |

---

## 📐 Layer 3: Satisfiability, Validity, and Entailment

| Concept | **Propositional Logic** | **Predicate Logic** |
|--------|--------------------------|----------------------|
| **Satisfiable** | `φ` is satisfiable if **some valuation** makes it true. | `φ` is satisfiable if **some structure and assignment** makes it true. |
| **Valid (tautology)** | `φ` is valid if it’s true under **every valuation**: `⊨ φ` | `φ` is valid if it’s true in **every structure and assignment**: `⊨ φ` |
| **Unsatisfiable** | No valuation makes φ true. | No structure/assignment makes φ true. |
| **Semantic entailment** | `Γ ⊨ φ`: every valuation that makes all of Γ true also makes φ true. | `Γ ⊨ φ`: every structure where all of Γ are true also makes φ true. |
| **Syntactic entailment** | `Γ ⊢ φ`: φ is derivable from Γ using inference rules (e.g. natural deduction). | Same. But proof rules now include quantifier rules (like ∀-intro, ∃-elim). |
| **Soundness** | If `Γ ⊢ φ`, then `Γ ⊨ φ` (everything provable is true). | Same. |
| **Completeness** | If `Γ ⊨ φ`, then `Γ ⊢ φ` (everything true is provable). | Same — but completeness is **deeper and trickier** in predicate logic. |

---

## 🔧 Layer 4: Connectives — Truth and Interpretation Rules

| Connective | **Meaning (Propositional)** | **Meaning (Predicate)** |
|------------|------------------------------|--------------------------|
| `¬φ` | True iff φ is false | True iff φ is false in the model/structure |
| `φ ∧ ψ` | True iff both are true | True iff both formulas are true in the structure |
| `φ ∨ ψ` | True iff at least one is true | True iff at least one is true in the structure |
| `φ → ψ` | False only if φ is true and ψ is false | True if whenever φ is true in the model, so is ψ |
| `φ ↔ ψ` | True iff both are true or both are false | True iff φ and ψ have the same truth value in the model |

---

## ∀ Layer 5: Quantifiers (Unique to Predicate Logic)

| Quantifier | **Informal Meaning** | **Formal Satisfaction Condition** |
|------------|-----------------------|-----------------------------------|
| `∀x. φ(x)` | "For all x, φ(x) is true" | `𝔄 ⊨ ∀x. φ` iff `𝔄 ⊨ φ[c/x]` for **all** objects `c` in the domain |
| `∃x. φ(x)` | "There exists an x such that φ(x)" | `𝔄 ⊨ ∃x. φ` iff `𝔄 ⊨ φ[c/x]` for **some** object `c` in the domain |

---

## 🧩 Layer 6: Other Key Terms in Both Logics

| Term | **Propositional Logic** | **Predicate Logic** |
|------|--------------------------|----------------------|
| **Assignment** | v: assigns truth values to vars | v: assigns objects to variables |
| **Structure `𝔄`** | Not used (you only need v) | Gives meaning to all non-logical symbols |
| **Free variable** | Not applicable | A variable not bound by a quantifier (needs assignment to evaluate) |
| **Sentence** | All formulas are closed (no free vars) | A formula with no free variables — only these have definite truth values |
| **Model class of Γ** | Set of valuations making all formulas in Γ true | Set of structures `𝔄` where `𝔄 ⊨ φ` for all `φ ∈ Γ` |
| **Theory** | A set of propositional formulas | A set of sentences (usually axioms) that define a model class |
| **Axiomatisation** | Set of formulas from which other formulas follow | Same — defines the properties of a class of structures |
| **Contradiction** | Formula false under every valuation | Formula false in every structure |
| **Consistency** | Γ is consistent if not all of Γ ⊢ ⊥ | Same — there’s **some model** of Γ (i.e. Γ is satisfiable) |
