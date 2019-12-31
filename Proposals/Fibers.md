# Structured Concurrency with Fibers

## Goal
- Concurrency using imperative style.
- Structured flow control to preserve abstractions.
- Unified scoping rules for opening/closing mechanisms.

## Benefits
- Abstraction over concurrent constructs such as OS threads.
- Structured control flow.
- Elimination of unstructured control flow.

## Design Details
- Dependency on [Delimited Continuations](Continuations.md).

## Complications
- Handling of CPU Bound Tasks

## Relevant Links
- [Research: Concurrency](/Research/README.md#Concurrency)