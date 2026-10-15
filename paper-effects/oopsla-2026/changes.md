# Changes

We have corrected the typos and minor errors pointed out by the reviewers
throughout the paper and made various small edits; below we describe the more
significant changes.

## New Material

We have updated the paper with relevant new material since our last submission.
This has led to a slight reframing of our contribution beyond the framework for
effect-generic gradual typing from the prior submission; we now include novel
results about the relationship between gradual typing and effects independent of
any semantic model. These results show that not all effects are compatible with
gradual typing, which strengthens the utility of our framework as identifying a
subset of effects that are compatible.

## Changes to Introduction

We have rewritten much of the introduction in light of the new framing for the
paper. The new version begins by illustrating a serious issue that arises in
combining gradual typing with Malcev theories. We use this result as a
stepping-stone to motivate our framework, in that we have identified sufficient
conditions on algebraic theories that allow for graduality to be proved without
hitting obstructions like the one we described for Malcev theories.

Most of the material in the "Overview of Approach" subsection is unchanged.

## Changes to Section 2 (Background)

No major changes.

## Changes to Section 3 (Syntax)

Added missing precision contexts \Delta to the rules.

## Changes to Section 4 (Operational Semantics)

In 4.2: Replaced contexts \Gamma with the empty context in the small-step rules.

In 4.2: Added prose explaining that the recording of a true step when downcasting the
dynamic type to a function type corresponds to the denotational semantics.

In 4.3: Added clarification of the rules characterizing the multi-step
semantics.

## Changes to Section 5 (Denotational Semantics)

5.1.2: Added prose explaining the concept of lifting of free models

In 5.2: Added further explanation of the technical devices we import from prior work
(specifically, the concept of perturbations).

## Changes to Section 6 (Adequacy)

No major changes.

## Changes to Section 7 (Globalization)

We removed a paragraph at the end of the section that is now out of date given
the new material. The paragraph had said that while our framework doesn't
support non-determinism and probability, it does support their free variants and
our graduality result will translate to any ordering on the free algebras that
is a congruence with respect to the operations. Since then, we have discovered
that the situation is more complicated, and those effects are now left to future
work.

## Changes to Section 8 (Describing the Framework)

No major changes.

## Changes to Discussion

We added a subsection discussing how handlers could be incorporated into our
framework, as well as the relationship to existing work on gradual typing and
effects, e.g., GrEff.

We added material on semilattice-like theories to the future work section. These
theories don't fit the requirements of our framework, but we expect them to be
compatible with gradual typing. We also added the theory of convex spaces (for
probabilistic choice) as an area for future work.





















## Changes to Introduction

We have rewritten much of the introduction to better motivate the issues that
arise in the construction of our model. Specific changes include:

* Shortening the exposition on gradual typing at the beginning of the introduction.
* Removing the dependence on knowledge of presheaves.
* Adding a section describing the challenges in adapting the New-Licata model to the guarded setting.
* Giving an overview of the notion of adequacy for our semantics.

We additionally emphasized that while our goal for future work is to scale our
approach to handle language features that the New-Licata approach is incapable
of handling, supporting even a simple semantics already presents nontrivial
issues. Thus, in this paper we take the first steps towards that goal. This
addresses a question of Reviewer B about the benefit of our approach over that
of New-Licata.

## Changes in Section 2

* Removed the rules corresponding to functoriality of casts from the
  syntax of our gradually-typed lambda calculus in Figure 2 of
  Section 2. These were left in from a previous version of the
  semantics, but are not necessary for modeling graduality, and are
  only true up to weak bisimilarity in our model. For example, the
  compositionality of downcasts is not generally the same as the
  downcast for the composite (dn c ∘ dn c') M = dn (cc') M because dn
  cc' can incur an additional perturbation over the composition of dn
  c and dn c'.

* Added a paragraph addressing Reviewer A's question about an alternative
  formulation of the axioms for type precision.

## Changes in Section 3

* Improved the exposition in the section on the big-step term semantics.

## Changes in Section 4

* Improved the exposition in the section explaining why transitivity is needed
  in the construction of our model.
* Added a brief sketch of the proof of the no-go theorem, referring to the
  appendix for more details.
* Explained the meaning of downward closed and upward closed for relations.
* Added the simpler squares corresponding to the UpR, DnL, and DnR rules.
* Added a brief description of the "heterogeneous" version of the lock-step
  error ordering differs from the homogeneous version defined in Figure 5.

## Changes in Section 5

* Added the definitions of the three embedding morphisms involving dyn (e_Nat,
  e_\times, e_\to).
* Explained why the set of perturbations has to have a monoid structure.
* Explained why the definition of value/computation morphisms does not have any
  condition involving the monoids of perturbations.
* Moved the definition of the free composition of error domain relations from
  the Appendix into this section.
* Added the definition of squares between predomain morphisms (squares between
  error domain morphisms are defined identically).
* Moved the details of the constructions on value types and computation types
  (i.e., defining the perturbations and interpretation as endomorphisms) from
  the Appendix into this section.
* Explained why the perturbations for the dynamic type need to be
  defined as an inductive type as opposed to using guarded recursion.
* Added the interpretation of the type precision equivalence rules as
  quasi-equivalence of the denoted relations.
* Added a description of the notation x[k] in the expression ∀𝑘.𝑥[𝑘] ⊑ 𝑦[𝑘].

## Changes to Discussion

* Reorganized the related work section to improve the flow.
* Added Section 6.2 which discusses the benefits of the denotational approach to
  gradual typing research over operational methods, addressing a question from
  Reviewer B.
* Discussed the implications of our work on gradual typing research, e.g.,
  applying it to model alternative cast semantics, and leveraging the
  intensional nature of our model to reason about the quantitative properties of
  cast optimizations. This addresses a question from Reviewer B.
