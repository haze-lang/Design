# Design
## Type System
Byte Type
    
## Language Provided Data Structures
Byte
    
## Memory Management Strategies:
1. Manual (Restrained)
1. Automatic Scope Deallocation (Smart Pointers, C++'s `unique_ptr`)
1. Reference Count?
1. Deletion on Unreachable Decision (Dylan)
1. Garbage Collection
    - Tracing GC

## Language Specifics
### First Class Citizens
???

### Copy Semantics
- Copy on write
### Move Semantics
## Evaluation
1. Eager
2. Lazy

## Procedural
### Pure Functions
#### Constraints
- Always returns same value for same set of arguments.
- Must return a value.
- Must not have any variables.?
- Must not have any side effects.
- Can only call other pure functions.
#### Benefits
- Can be optimized to skip the call if return value is unused since the function has No side effects (lazy evaluation).
- Can be cached for a set of arguments.
- Can always run concurrenctly.
- Possible compile-time evaluation.
### Procedures

## Function Dispatch
??

## Object-Orientation
### Prototype
### Class
#### Inheritance Breakdown
- Composition
- Implicit Composition/Delegation (Mixin Classes)
- Polymorphism

## Concurrency:
- Mutable & Immutable Variables
## Restrained Manual Memory Management:
- Compile-time checking of deallocations for every allocation.
- Deallocation only allowed in scope in which the allocation took place.

## Standard Library:
### Types
- Array
- Table
