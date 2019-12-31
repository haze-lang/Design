# Initial Design Proposal

## Concurrency

- Structured Concrrency with fibers.
- Default immutablity in functions.

[Main Proposal](Fibers.md)

## Type System

### Unit
Type with only one value, `()`. It represents a useless value, similar to `void` in C.

### Built-in Types
- Byte
- Character
- Number
- String

#### Built-in Data Structures
- See Standard Library section.

[Main Proposal](TypeSystem.md)

## Memory Management Strategies
1. [Restrained](RestrainedMemoryManagement.md)
<!-- 2. Reference Count -->
<!-- 3. Automatic Scope-based Deallocation (Smart Pointers, C++'s `unique_ptr`) -->

## Language Specifics
### First Class Citizens
- Variables
- Procedures
- Functions

### Expressions
- Procedure Invocations
- Pure Expressions
  - Function 
  - Switch Expressions (Pattern Matchhing)
  - Lambda Expressions
  - Literals (Number & String)

## Evaluation
1. Eager
1. [Lazy](LazyEvaluation.md)

## Subroutines
There are two types of subroutines.

### Procedures
List of statements.

### Functions
Single or composition of pure expressions.
[Main Proposal](Functions.md)

## Standard Library:
### Types
- Array
- List