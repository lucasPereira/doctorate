# AGENTS.md

## Project Purpose

This repository is a workspace that groups the projects related to Lucas Pereira's doctorate. Treat it as a submodule-based research workspace, not as a single application monorepo with one global build.

The goal is to let AI agents work with the dissertation, papers, framework code, and examples in one context while preserving each subproject as an independent Git repository.

## Workspace Layout

- `a-reuse-oriented-framework-for-automated-test-code-refactoring/` is the IEEE Access manuscript project for the paper "A Reuse-Oriented Framework for Automated Test Code Refactoring". It has its own `AGENTS.md`; read and follow it before editing anything inside that submodule.
- `roza/` is the Roza framework being developed for the thesis. It is a Java 11 Gradle project for automated reuse-oriented test code refactoring.
- `doctorate-examples/` contains small example programs and tests used in papers and the thesis. It is a Gradle Kotlin/JVM 17 project with Kotlin and Java examples.
- `thesis/` is expected to become a future submodule for the dissertation, but it does not exist yet.

## Workflow

- Each top-level project directory is a Git submodule. Check the relevant submodule status before making changes that span repositories.
- Prefer working inside the specific submodule requested by the user. Do not assume a root-level build, test, format, or release command exists.
- Before editing a submodule, look for and follow its local `AGENTS.md`, `.cursor/rules/`, README, or build files. Local guidance overrides this root workspace guidance for files inside that submodule.
- Commit only when the user explicitly asks. If committing, commit from the repository that owns the changed files; root workspace changes and submodule changes may require separate commits.
- Do not rewrite submodule history, change submodule remotes, or force-push unless the user explicitly asks.

## Agent Behavior

- Respond in the language used by the user unless they request otherwise.
- Keep this root workspace guidance high level. Put project-specific instructions in the relevant submodule's own `AGENTS.md` when that submodule needs them.
- When a task touches research claims, experimental results, statistics, or academic interpretation, flag uncertainty and ask for confirmation before changing the claim.
- Prefer focused validation in the affected submodule: compile LaTeX for manuscript edits, run Gradle tests for code changes, and report clearly when validation was not run.
