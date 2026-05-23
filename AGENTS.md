# AGENTS.md

## Project purpose

This repository groups Lucas Pereira's doctorate work in a submodule-based workspace: each top-level directory is its own Git repository, with no single global build at the root.

## Workspace layout

- `a-reuse-oriented-framework-for-automated-test-code-refactoring/` — IEEE Access manuscript for "A Reuse-Oriented Framework for Automated Test Code Refactoring".
- `roza/` — Róża framework (Java 11, Gradle) for automated reuse-oriented test code refactoring.
- `doctorate-examples/` — small Kotlin/Java examples and tests for papers and the thesis (Gradle, JVM 17).

## Workflow

- Prefer the submodule the user named. Before editing, follow that project's local `AGENTS.md`, `.cursor/rules/`, `README.md`, or build files; they override this file.

## Definitions

These definitions must be used consistently throughout the workspace.

- Camus architecture: a pipeline architecture for refactoring test code.
- Róża framework: an extensible framework that instantiates the Camus architecture by refactoring test classes through implicit setup.

Preferred sentence:

> We propose (1) the Camus architecture, a pipeline architecture for refactoring test code, and (2) the Róża framework, an extensible framework that instantiates this architecture by refactoring test classes through implicit setup.
