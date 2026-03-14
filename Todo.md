# To-Do: Swift DS&A (with Explanations)

Status uses ⬜️ (Todo), 🚧 (In Progress), ✅ (Done). Difficulty is a rough guide.
Each item links to an anchor with a short explanation of scope and acceptance criteria.

## Data Structures

| Status | Problem | Difficulty |
|---|---|---|
| ⬜️ | [Design Dynamic Array (Resizable Array)](#design-dynamic-array-resizable-array) | Easy |
| ⬜️ | [Design Singly Linked List](#design-singly-linked-list) | Easy |
| ⬜️ | [Design Double-ended Queue](#design-double-ended-queue) | Medium |
| ⬜️ | [Design Binary Search Tree](#design-binary-search-tree) | Medium |
| ⬜️ | [Design Hash Table](#design-hash-table) | Medium/Hard |
| ⬜️ | [Design Heap](#design-heap) | Medium |
| ⬜️ | [Design Graph](#design-graph) | Medium |
| ⬜️ | [Design Disjoint Set (Union-Find)](#design-disjoint-set-union-find) | Medium |
| ⬜️ | [Design Segment Tree](#design-segment-tree) | Medium/Hard |

### Design Dynamic Array (Resizable Array)
- Implement a generic `DynamicArray<Element>` backed by contiguous storage.
- Operations: `append`, `insert(at:)`, `remove(at:)`, random access, iteration, capacity doubling.
- Acceptance: amortized O(1) appends, value semantics, copy-on-write where appropriate, XCTest covering growth and edge cases.

### Design Singly Linked List
- `SinglyLinkedList<Element>` with `push`, `append`, `insert(after:)`, `pop`, `removeLast`, `remove(after:)`.
- Acceptance: correct pointer updates, sequence conformance/iterator, tests for empty/singleton/multi-node scenarios.

### Design Double-ended Queue
- `Deque<Element>` with O(1) amortized `pushFront`, `pushBack`, `popFront`, `popBack` (ring buffer or two-stack approach).
- Acceptance: capacity growth strategy, correctness under wrap-around, thorough tests.

### Design Binary Search Tree
- `BinarySearchTree<Element: Comparable>` with insert/search/remove (Hibbard deletion), traversal, min/max.
- Acceptance: BST invariants maintained; tests cover duplicates policy and rebalancing note (no balancing initially).

### Design Hash Table
- `HashTable<Key: Hashable, Value>` using separate chaining or open addressing.
- Acceptance: load factor growth, collision handling, deletion semantics; tests simulate worst-case hashing.

### Design Heap
- Binary heap (min/max) over array with `insert`, `peek`, `extract`, `heapify`, `buildHeap`.
- Acceptance: heap property preserved; tests cover random permutations and edge cases.

### Design Graph
- Adjacency list graph (directed/undirected) with weighted/unweighted edges.
- Acceptance: add/remove vertices/edges, traversal hooks; tests for both directed and undirected modes.

### Design Disjoint Set (Union-Find)
- `DisjointSet` with path compression and union by rank/size.
- Acceptance: near-constant operations; tests validate parent/rank invariants.

### Design Segment Tree
- Segment tree over array for range queries (sum/min/max) with point updates.
- Acceptance: O(log n) update/query; randomized tests vs. naive verification.

## Sorting

| Status | Problem | Difficulty |
|---|---|---|
| ⬜️ | [Insertion Sort](#insertion-sort) | Easy |
| ⬜️ | [Merge Sort](#merge-sort) | Medium |
| ⬜️ | [Quick Sort](#quick-sort) | Medium |

### Insertion Sort
- Stable in-place sort; best-case O(n) on nearly sorted input.
- Acceptance: generic over `Comparable`; tests include empty, singleton, duplicates, reversed, nearly-sorted.

### Merge Sort
- Stable O(n log n); either top-down or bottom-up with auxiliary buffer.
- Acceptance: no extra allocations per recursion frame beyond buffer; tests for stability and large arrays.

### Quick Sort
- In-place partition; choose pivot strategy (median-of-three or random).
- Acceptance: worst-case guard (cutover to insertion sort or randomization); thorough tests including duplicates.

## Graphs

| Status | Problem | Difficulty |
|---|---|---|
| ⬜️ | [Matrix Depth-First Search](#matrix-depth-first-search) | Easy |
| ⬜️ | [Matrix Breadth-First Search](#matrix-breadth-first-search) | Easy |
| ⬜️ | [Dijkstra's Algorithm](#dijkstras-algorithm) | Medium/Hard |
| ⬜️ | [Prim's Algorithm](#prims-algorithm) | Medium/Hard |
| ⬜️ | [Kruskal's Algorithm](#kruskals-algorithm) | Medium/Hard |
| ⬜️ | [Topological Sort](#topological-sort) | Medium |

### Matrix Depth-First Search
- DFS over 2D grid with visited tracking and 4/8-directional movement.
- Acceptance: handles obstacles/bounds; tests small grids and components count.

### Matrix Breadth-First Search
- BFS over 2D grid with queue for shortest steps in unweighted grids.
- Acceptance: returns distances/parents; tests for shortest paths and unreachable cells.

### Dijkstra's Algorithm
- Single-source shortest paths on non-negative weighted graphs with priority queue.
- Acceptance: returns distances and predecessors; tests compare against known results and small graphs.

### Prim's Algorithm
- Minimum spanning tree for connected weighted graphs using priority queue.
- Acceptance: verifies total weight and tree properties; tests on small graphs.

### Kruskal's Algorithm
- MST using sorting edges and Union-Find.
- Acceptance: leverages Disjoint Set; tests confirm acyclicity and minimality.

### Topological Sort
- Ordering of DAG nodes using Kahn's algorithm or DFS postorder.
- Acceptance: detects cycles; tests with multiple valid orders.

## Dynamic Programming

| Status | Problem | Difficulty |
|---|---|---|
| ⬜️ | [0 / 1 Knapsack](#0--1-knapsack) | Medium |
| ⬜️ | [Unbounded Knapsack](#unbounded-knapsack) | Medium |

### 0 / 1 Knapsack
- DP over items and capacity with boolean/int table or 1D optimization.
- Acceptance: returns optimal value and optional reconstruction of chosen items; tests with small known cases.

### Unbounded Knapsack
- Unbounded item counts; 1D DP iterating capacities ascending.
- Acceptance: correct transitions; tests cover edge inputs and reconstruction where applicable.

---
When implementing, create module-appropriate files under `Sources/` and tests under `Tests/`. Keep PRs focused and update `Log.md` with status and date.

