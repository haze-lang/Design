# Initial Design Proposal

## Type System

### Fundamental Types
- Byte

[Main Proposal](TypeSystem.md)

## Built-in Data Structures

## Memory Management Strategies
1. [Restrained](RestrainedMemoryManagement.md)
1. Automatic Scope-based Deallocation (Smart Pointers, C++'s `unique_ptr`)
1. Reference Count
1. Deletion on Unreachable Decision (Dylan)
1. Garbage Collection
    - Tracing GC

## Language Specifics
### First Class Citizens
- Variables
- Subroutines

### Copy Semantics
- Copy on write

### Move Semantics

### Expressions

### Operators

### Short-Circuit Operators

## Evaluation
1. Eager
1. [Lazy](LazyEvaluation.md)

## Subroutines
There are two types of subroutines.

### Procedures
C-like subroutine.

### Functions
A function is a purely functional piece of code.
[Main Proposal](Functions.md)

## Function Dispatch

- Single
- Double
- Multiple

## Object-Orientation

### Prototypes

### Classes
#### Inheritance Breakdown
- Composition
- Implicit Composition/Delegation (Mixin Classes)
- Polymorphism

## Concurrency:
- Mutable & Immutable Variables

## Standard Library:
### Types
- Array
- Table
- Dynamic Array
