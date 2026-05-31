# Doctorate workspace guidance

This file gives agents the workspace-level context needed to choose the right subproject and use the work terminology consistently.

## Project purpose

This repository groups Lucas Pereira's doctorate work in a submodule-based workspace: each top-level directory is its own Git repository, with no single global build at the root.

## Workspace layout

The top-level directories are independent projects. Work inside the submodule named by the user whenever possible.

- `an-architecture-for-automatic-test-setup-code-refactoring-ieee-access/` — IEEE Access manuscript.
- `roza/` — Róża framework for automatic test code refactoring.
- `doctorate-examples/` — small Kotlin/Java examples and tests for papers and the thesis.

## Workflow

Project-local instructions override this file. Before editing, read the named submodule's local `AGENTS.md`, `.cursor/rules/`, `README.md`, or build files when they are relevant.

## Definitions

**Treatment.** Test placement is treated as a global refactoring task: redistribute existing tests into classes that increase shared setup code without changing observed test behavior.

**Architecture.** A pipeline architecture for refactoring test code.

**Róża.** An extensible framework that instantiates the pipeline architecture by refactoring test classes through the implicit setup strategy.

**Proposal.** _"We propose (1) a pipeline architecture for refactoring test code, and (2) the Róża framework, an extensible framework that instantiates this architecture by refactoring test classes through the implicit setup strategy."_
