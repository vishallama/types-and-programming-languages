# 1. Introduction

## Types in Computer Science

### Formal Methods

#### Powerful Frameworks
Hoare logic, algebraic specification languages, modal logics, and denotational
semantics. These can express some very general correctness properties, but are
cumbersome to use and require a high level of sophistication on the part of the
programmers.

#### Lightweight Formal Methods
Automatic checkers built into compilers, linkers, and program analyzers. Another
example is that of model checkers which are tools that search for errors in
finite-state systems such as chip designs or communication protocols. Another
is that of *run-time monitoring*, a collection of techniques that allow a system
to detect dynamically when one of its components is not behaving according to
specification.

However, the most popular and best established lightweight formal methods are
*type systems*.

##### Definition
> A type system is a tractable syntactic method for proving the absence of
> certain program behaviors by classifying phrases according to the kinds of
> values they compute.


## What Type Systems Are Good For

### Detecting Errors
Allows early detection of some programming errors. It is always less costly
to fix errors early. Errors can also be pinpointed more accurately during
typechecking. Deeper conceptual errors will often manifest as inconsistencies
at the level of types.

A typechecker can also be an invaluable *maintenance tool*. For example, in
order to change the definition of a complex data structure, one need not
search by hand all the places in a large program where code involving this
structure needs to be fixed.

### Abstraction
Enforces disciplined programming. Types show up in the interfaces of modules
(and classes). In SML and OCaml, the interface itself is the "type" for the
module that implements it. Modules implementing clear interfaces leads to a
more abstract style of design, which facilitates better code maintenance.

### Documentation
Types provide useful documentation that always remains current and never gets
outdated, since it gets checked during every run of the compiler.

### Language Safety
*A safe language is one that protects its own abstractions*. Language safety
is not the same thing as type safety. Language safety can be achieved by
static checking and also by run-time checks that trap nonsensical operations
just at the moment when the are attempted and stop the program or raise an
exception. For instance, Scheme is a safe language, even though it has no
static type system.

|              | Statically checked       | Dynamically checked         |
| ------------ | ------------------------ | --------------------------- |
| **Safe**     | ML, Haskell, Java, etc.  | Lisp, Scheme, Perl, etc.    |
| **Unsafe**   | C, C++, etc.             |                             |

### Efficiency
Type systems allow the compiler to distinguish between different kinds of
data, and thus permits the generation of appropriate machine instructions.
The ML Kit Compiler uses a powerful *region inference* algorithm to replace
most (in some programs, all) of the need for garbage collection by
stack-based memory management.

### Further Applications
 - Computer and Network Security.
 - Type checking and inference algorithms can be applied in conversion
   utilities and alias analysis.
 - Type systems (based on dependent types) are used in proof assistants, such
   as Nuprl, Coq, and Alf.
 - Use in web metadata.
 - In computational linguistics, where typed lambda-calculi form the basis for
   formalisms such as *categorial grammar*.

## Type Systems and Language Design
Ideally, language design should go hand-in-hand with type system design. In
typed languages, the type system itself is often taken as the foundation of
the design. It is true that the concrete syntax of typed languages tends to
be more complicated than that of untyped languages, because type annotations
must be taken into account. However, a well-designed statically typed
language will never require huge amounts of type annotations. For instance,
languages in the ML family require very minimal type annotations from the
programmer, letting the type inference methods recover the necessary
information.

## Capsule History
The earliest type systems were used to make very simple distinctions between
integer and floating point representations of numbers (e.g. in Fortran.) In
the 50s and 60s, his was extended to  structured data and higher-order
functions. In the 70s, even richer concepts, such as parametric polymorphism,
abstract data types, module systems, and subtyping, were introduced. At time
same time, connections between the type systems found in programming
languages and those studied in mathematical logic were found.

## Related Reading
A short list of related reading:

  - *Lambda-Calculus and Combinators, An Introduction*, Hindley and Seldin
  - *A Theory of Objects*, Abadi and Cardelli
  - *Foundations of Object-Oriented Languages: Types and Semantics*, Bruce
  - *Basic Category Theory for Computer Scientists*, Pierce
  - *Proofs and Types*, Girard, Lafont, and Taylor
  - *Type Theory and Functional Programming*, Thompson

