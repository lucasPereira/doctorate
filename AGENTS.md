# AGENTS.md

## Project purpose

This repository groups Lucas Pereira's doctorate work in a submodule-based workspace: each top-level directory is its own Git repository, with no single global build at the root.

## Workspace layout

- `a-reuse-oriented-framework-for-automated-test-code-refactoring/` — IEEE Access manuscript for "A Reuse-Oriented Framework for Automated Test Code Refactoring".
- `roza/` — Róża framework (Java 11, Gradle) for automated reuse-oriented test code refactoring.
- `doctorate-examples/` — small Kotlin/Java examples and tests for papers and the thesis (Gradle, JVM 17).
- `thesis/` — planned dissertation submodule (not present yet).

## Workflow

- Prefer the submodule the user named. Before editing, follow that project's local `AGENTS.md`, `.cursor/rules/`, `README.md`, or build files; they override this file.
