# 2. Mathematical Preliminaries

## Sets, Relations, and Functions
Definitions to know:
  - Set: set comprehension, empty set, set difference, set cardinality, and
    powerset of a set.
  - The set of naturals and countability of a set.
  - An *n-*th place *relation*.
  - *Predicate* on a set S is a one-place relation.
  - *Binary relation*.
  - *Domain, range*, and *codomain* of a relation R.
  - *Partial* and *total* function.
  - A predicate P is *preserved* by a binary relation R on a set S, if whenever
    we have s R s' and P(s), we also have P(s').

## Ordered Sets
Definitions to know:
  - Reflexive, symmetric, transitive, and anti-symmetric binary relations.
  - A reflexive and transitive relation R on a set S is called *preorder* on S.
  - A preorder that is also anti-symmetric is called a *partial order*.
  - Total order.
  - Join (least upper bound), and meet (greatest lower bound).
  - Equivalence relation.
  - *Reflexive closure* of R is the smallest reflexive relation R' that
    contains R. Similarly, the *transitive closure* of R is the smallest
    transitive relation R' that contains R. Similar definition for *reflexive
    and transitive closure*.
  - *Decreasing chain* defined on a preorder defined on a set S. Chains can
    be either finite or infinite.
  - A preorder on a set S is *well-founded* if it contains no infinite
    decreasing chains. For example, the usual order on the natural numbers is
    well-founded. We sometimes omit mentioning the preorder explicitly and
    simply speak of S as a *well-founded set*.

## Sequences
A *sequence* is written by listing its elements, separated by commas. A comma
is used as both the "cons" operation for adding an element to either end of a
sequence and as the "append" operation on sequences. So if *a* is the sequence
*3, 2, 1* and *b* is the sequence *5, 6*, then *0, a* denotes the sequence
*0, 3, 2, 1*, while *a, 0* denotes *3, 2, 1, 0*, and *b, a* denotes the
sequence *5, 6, 3, 2, 1*. The sequence of numbers from *1* to *n* is
abbreviated *1..n*. We write *|a|* for the length of the sequence *a*. The
empty sequence is written either as • or as a blank.

One sequence is said to be a *permutation* of another if it contains exactly
the same elements, possibly in a different order.

## Induction
Proofs are ubiquitous in the theory of programming languages, and many of
these are based on one of the following principles.

#### AXIOM (Principle of Ordinary Induction on Natural Numbers)
Suppose that *P* is a predicate on the natural numbers. Then:

> If *P(0)*, and for all *i*, *P(i)* implies *P(i+1)*,
> then *P(n)* holds for all *n*.

#### AXIOM (Principle of Complete Induction on Natural Numbers)

#### AXIOM (Principle of Lexicographic Induction)

#### AXIOM (Principle of Structural Induction)

