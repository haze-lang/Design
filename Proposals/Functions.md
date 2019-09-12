# Functions

## Goal
- Provide purely functional programming features for access to functional paradigm in an 
imperative environment.
- Enable declarative code.

## Benefits
- Can be optimized to skip the call if return value is unused since there are no side effects.
- Possible [Lazy evaluation](LazyEvaluation.md).
- Can be cached for a set of arguments.
- Can always run concurrenctly.
- Possible compile-time invocation.
- Possible optimization of recursive calls.

## Design Details
Procedures with additional constraints.

### Constraints
- Must not use any imperative code constructs (e.g. Loops).
- Must return a value.
- Must not have any side effects (I/O, File handles, Sockets, etc).
- Can only call other pure functions.

### Properties
- Every Function always returns same result for a given set of arguments.

## Relevant Links
- [Counting Immutable Beans: Reference Counting Optimized for Purely Functional Programming](https://arxiv.org/abs/1908.05647)