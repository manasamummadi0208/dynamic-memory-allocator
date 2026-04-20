# Dynamic Memory Allocator in C

## Overview
This project implements a custom dynamic memory allocator in C, similar to `malloc` and `free`.
It is designed to efficiently manage heap memory using techniques such as segregated free lists and boundary tag coalescing.

The allocator supports dynamic memory allocation, deallocation, and reallocation while minimizing fragmentation and maintaining performance.

## Features
- Segregated free lists organized by size classes
- First-fit allocation strategy for fast allocation
- LIFO (Last-In-First-Out) free list management
- Boundary tag coalescing for merging adjacent free blocks
- Block splitting to optimize memory utilization
- Heap extension for handling large allocations

## Concepts Covered
- Heap memory management
- Pointer arithmetic
- Internal vs external fragmentation
- Free list management
- Coalescing and block splitting
- Low-level systems programming in C

## Project Structure
```text
dynamic-memory-allocator/
├── src/
│   └── allocator.c
├── include/
│   └── debug.h
├── examples/
│   └── demo.c
├── Makefile
└── README.md
```

## Build Instructions
```bash
make
```

## Run
```bash
./allocator
```

## Key Design Details

### Segregated Free Lists
Memory blocks are organized into multiple free lists based on size classes, allowing faster allocation and reduced search time.

### Allocation Strategy
A first-fit policy is used to quickly find suitable free blocks, improving performance for frequent allocations.

### Coalescing
Adjacent free blocks are merged using boundary tags to reduce external fragmentation and improve memory reuse.

### Block Splitting
Large blocks are split into smaller blocks when possible to maximize memory utilization.

## Key Learnings
- Trade-offs between allocation speed and memory utilization
- Efficient memory reuse through coalescing
- Handling fragmentation in dynamic memory systems
- Designing low-level systems with manual memory management

## Future Improvements
- Implement best-fit or next-fit allocation strategies
- Add thread-safety for concurrent environments
- Benchmark against standard `malloc` implementations
- Improve performance with caching techniques

## Author
Manasa Mummadi