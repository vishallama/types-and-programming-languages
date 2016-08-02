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

### Efficiency

