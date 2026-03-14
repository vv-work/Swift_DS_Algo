# Agents Guide

Guidelines for contributors and automations collaborating on this Swift algorithms and data structures library using Test-Driven Development (TDD).

## Principles
- TDD-first: write a failing test before implementation (red → green → refactor).
- Small steps: prefer minimal, composable changes that keep tests passing.
- Idiomatic Swift: value semantics, clear naming, protocol-oriented design, safe APIs.
- Quality over scope: resist adding features without tests and documentation.
- Focus: do not modify unrelated code or tooling in the same change.

## Workflow
1. Plan: outline the change and identify edge cases.
2. Red: add/adjust tests in `Tests/<Module>Tests/` that fail for the right reason.
3. Green: implement the simplest solution in `Sources/<Module>/` to satisfy tests.
4. Refactor: improve design and performance without changing behavior.
5. Document: update README or inline docs for public APIs when needed.
6. Verify: run `swift test` locally; keep the test suite fast and deterministic.

## Coding Standards
- Naming: prefer clarity; avoid abbreviations unless conventional.
- Immutability: use `let` by default; keep state localized and explicit.
- Errors: use `throws` for recoverable errors and precondition assertions for programmer errors.
- Generics: constrain with protocols where appropriate; avoid over-generalizing prematurely.
- Complexity: state big-O where non-obvious; keep algorithms efficient and measured.
- Performance: add micro-benchmarks or `XCTestCase.measure` when optimizing hot paths.

## Tests
- Cover typical, edge, and pathological inputs; include empty/singleton cases.
- Verify invariants thoroughly (e.g., heap property, BST ordering).
- Prefer black-box tests; add white-box tests if it clarifies tricky invariants.
- Use fixtures/builders sparingly; keep tests readable.

## Repository Conventions
- Layout: Swift Package Manager defaults (`Sources/`, `Tests/`, `Package.swift`).
- Commits: single-purpose, descriptive messages; reference the component touched.
- Branches/PRs: keep focused; include rationale and examples.
- Tooling: add new tools (formatters/linters/CI) only with consensus and configuration.

## Commands
- Build: `swift build`
- Test: `swift test`
- Generate Xcode project (optional): `swift package generate-xcodeproj` (deprecated for recent Xcode; prefer opening the Package directly).

## Definition of Done
- Tests added and passing.
- Public API documented.
- No warnings introduced; code formatted per repo conventions (when configured).
- README or module docs updated if behavior is user-facing.

---
These guidelines aim to keep the codebase approachable and educational while maintaining rigor through TDD.

