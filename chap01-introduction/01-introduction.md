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

