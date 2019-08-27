# Restrained Memory Management

## Goal
- Compile-time enforcement of deallocations in procedures which have 
static allocations.
- Run-time tracking of allocations in owning procedure's stack frame.

## Benefits
- Minimal run-time (no run-time effect with compile-time safety).
- Prevention of memory leaks caused by programmer error.

## Design Details

### Compile-time
- Prevent allocation to variables not owned by a procedure.
- Compile-time checking of deallocations for every allocation in a procedure scope.
- Deallocation only allowed in scope in which the allocation took place.
- Special qualifier for procedures returning allocated data for use-cases involving 
multiple variables storing same address.

### Run-time (WIP)

#### Ownership
Procedure which declares the address variable owns it.