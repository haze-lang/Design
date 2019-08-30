# Design
This repository contains documentation for the design of the language.

## Aim
The goal is to combine features which have been either proposed in 

- research but are not part of the mainstream languages, or 
- used in niche *academic* languages such as Lisp and family, 

in an imperative paradigm to enable everyday developers to understand them and use them without 
needing to learn the excessive theory behind them.

## Research
Collection of features and literature for the design.

### Pure Functional Programming
Pure functional programming features from Lisp and family, notably Haskell.

- Continuations
- Algebraic Effects
- Pure Functions & Higher-order functions
- Full Lazy Evaluation (Haskell)
- [Icon's Goal-directed Execution](https://en.wikipedia.org/wiki/Icon_(programming_language)#Goal-directed_execution)

### Type System
- Robust Type System such as Dependent Types in [Idris](https://www.idris-lang.org/)
- [Multiple Dispatch](https://en.wikipedia.org/wiki/Multiple_dispatch) (Lisp, Julia, C#)


### Memory Management

- Choice of different memory management strategies such as GC, Reference Count, Smart Pointers, etc.

### Metaprogramming
- Lisp's [Homoiconicity](https://en.wikipedia.org/wiki/Homoiconicity)


## Initial Design
I have selected some features to be part of the initial design. They can be found at 
[Initial Proposal](/Proposals/Initial.md).