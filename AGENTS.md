# Doctorate workspace guidance

This file gives agents the workspace-level context needed to choose the right subproject and use the paper terminology consistently.

## Project purpose

This repository groups Lucas Pereira's doctorate work in a submodule-based workspace: each top-level directory is its own Git repository, with no single global build at the root.

## Workspace layout

The top-level directories are independent projects. Work inside the submodule named by the user whenever possible.

- `an-architecture-for-automatic-test-code-refactoring/` — IEEE Access manuscript.
- `roza/` — Róża framework for automatic reuse-oriented test code refactoring.
- `doctorate-examples/` — small Kotlin/Java examples and tests for papers and the thesis.

## Workflow

Project-local instructions override this file. Before editing, read the named submodule's local `AGENTS.md`, `.cursor/rules/`, `README.md`, or build files when they are relevant.

## Definitions

Use these names consistently when discussing the manuscript, architecture, and framework.

**Define Camus architecture consistently.** Use _"a pipeline architecture for refactoring test code."_

**Define Róża framework consistently.** Use _"an extensible framework that instantiates the Camus architecture by refactoring test classes through the implicit setup strategy."_

**Use the preferred proposal sentence for compact definitions.** _"We propose (1) the Camus architecture, a pipeline architecture for refactoring test code, and (2) the Róża framework, an extensible framework that instantiates this architecture by refactoring test classes through the implicit setup strategy."_
