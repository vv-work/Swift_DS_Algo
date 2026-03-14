# Swift Data Structures & Algorithms (TDD)

Learn and practice Swift by building a reusable algorithms and data structures library, driven by Test-Driven Development (TDD) and modern Swift tooling.

## Goals
- Develop idiomatic, performant implementations of core data structures and algorithms.
- Use TDD to guide design, ensure correctness, and enable refactors.
- Practice modern Swift (generics, protocol-oriented design, value semantics).
- Keep setup lightweight via Swift Package Manager (SPM) and XCTest.

## Why TDD
- Captures intent and edge cases before implementation (red → green → refactor).
- Encourages small, composable APIs and confidence to iterate.
- Produces a living specification of behavior through tests.

## Tooling
- Swift 5.9+ (SPM + XCTest)
- Xcode (optional) or any editor with Swift support
- Optional: `swift-format`, `swiftlint` (add when configured)

## Getting Started
1. Ensure Swift is installed: `swift --version`.
2. If the package is not yet initialized, scaffold it:
   - `swift package init --type library`
3. Run tests:
   - `swift test`
4. Build the library:
   - `swift build`

## Project Structure (SPM)
- `Package.swift` – package manifest
- `Sources/AlgoDS/` – library source (module name may vary)
- `Tests/AlgoDSTests/` – unit tests using XCTest

## Working Style
- Start every feature by writing a failing test.
- Implement the simplest code to pass the test.
- Refactor while keeping tests green.
- Prefer value types, clear invariants, and strong pre/postconditions.

## Roadmap (examples)
- Arrays, Stacks, Queues, Linked Lists
- Hash Tables, Heaps, Trees (BST/AVL), Graphs
- Searching/Sorting (Binary Search, Quick/Merge/Heap Sort)
- Graph algorithms (BFS/DFS, Dijkstra, Topological Sort)
- String algorithms (KMP, Trie, Rabin–Karp)
- Misc: Union-Find, Interval, Sweep-line, DP patterns

## Contributing
- Use TDD and keep PRs focused.
- Document public APIs and invariants.
- Add tests for edge cases and performance where relevant.

---
This repository is intentionally simple to make iteration fast. We’ll introduce additional tooling (formatters/linters/CI) as the library matures.

