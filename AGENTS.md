# Doctorate workspace guidance

This repository brings together the projects developed as part of Lucas Pereira
da Silva's PhD at Universidade Federal de Santa Catarina. The research
investigates how test code can be refactored automatically and proposes two
connected contributions: a pipeline architecture for organizing the refactoring
process and the Róża framework for putting that architecture into practice.

Most top-level projects are independent Git submodules, so each may define its
own structure and working rules. When a task concerns one of these submodules
and it contains an `AGENTS.md`, the agent must always read that file before
making changes.

## Structure

- `roza/` contains the Róża framework.
- `roza-edge/` contains the new Róża Edge framework.
- `qualifying-exam/` contains the qualifying exam document and presentation.
- `paper-2026-ieee/` contains the IEEE Access manuscript.
- `paper-2026-sncs/` contains the SN Computer Science manuscript.
- `artifacts/` contains historical and reference PDFs.
- `doctorate-examples/` contains the Java and Kotlin examples.
