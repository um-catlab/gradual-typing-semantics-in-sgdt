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
