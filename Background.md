# Background
Described here is some context and reasons why I decided to work on a programming language for my senior project. This document needs to be updated since it was originally the outline of my proposal before the project was accepted.

## Motivation and Goal
The focus of this project is on features

- proposed in research but are not part of the mainstream languages, or
- used in niche *academic languages* (such as Lisp/ML and family)

The goal is to combine these features with the latest advancements in programming languages and make 
them available in an imperative paradigm to enable everyday developers to understand them and use them 
without needing the theoretical background in Programming Language Theory.

## Research
Collection of features and literature for the design. For details, see [Research](/Research/README.md).

### Pure Functional Programming
Pure functional programming features from Lisp/ML and family, notably Haskell.

- Algebraic Effects
- Pure & Higher-order functions
- Full Lazy Evaluation (Haskell)

### Flow Control
- Continuations (Scheme)
- [Icon's Goal-directed Execution](https://en.wikipedia.org/wiki/Icon_(programming_language)#Goal-directed_execution)

### Concurrency
- Goroutines (Go)

### Type System
- Robust Type System such as Dependent Types in [Idris](https://www.idris-lang.org/)
- [Multiple Dispatch](https://en.wikipedia.org/wiki/Multiple_dispatch) (Lisp, Julia, C#)

### Memory Management

Choice of different memory management strategies such as 
- Reference Count
- Smart Pointers
- Garbage Collection

### Metaprogramming
- Lisp's [Homoiconicity](https://en.wikipedia.org/wiki/Homoiconicity)

## Initial Design
I have selected some features to be part of the initial design. See 
[Initial Proposal](/Proposals/Initial.md).
