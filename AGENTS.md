# Doctorate workspace guidance

This file gives agents the workspace-level context needed to choose the right subproject, understand the doctorate timeline, and use the work terminology consistently.

## Project purpose

This repository is the umbrella workspace for Lucas Pereira's PhD thesis at Universidade Federal de Santa Catarina. The research topic is automatic refactoring of test code through a pipeline architecture and the Róża framework.

The workspace is submodule-based: most top-level directories are independent Git repositories. There is no single global build at the root. Work inside the directory named by the user whenever possible.

## Doctorate timeline

Lucas started the doctorate in an earlier cycle, reached the progress seminar (_seminário de andamento_) and the qualification exam (_qualificação_), then interrupted the program without completing the degree. He has since returned to the doctorate.

**Earlier cycle (circa 2016).** Qualification materials and related thesis draft live under [Artifacts](#artifacts). They are historical reference, not the active source of truth.

**Return (circa 2024).** A new progress seminar marks the restart. Its slides, document, and committee notes are also under [Artifacts](#artifacts).

**Current work.** Active writing and implementation happen in the subprojects below, especially `qualifying-exam/` for the qualifying exam document and `roza/` for the framework.

## Workspace layout

The top-level directories are independent projects unless noted otherwise.

| Directory                                                                | Role                                                                 |
| ------------------------------------------------------------------------ | -------------------------------------------------------------------- |
| `roza/`                                                                  | Róża framework for automatic test code refactoring.                  |
| `an-architecture-for-automatic-test-setup-code-refactoring-ieee-access/` | IEEE Access manuscript on the pipeline architecture.                 |
| `doctorate-examples/`                                                    | Small Kotlin/Java examples and tests used in papers and thesis text. |
| `qualifying-exam/`                                                       | Active LaTeX project for the qualifying exam document.               |
| `artifacts/`                                                             | Read-only PDFs from past doctorate events.                           |

**Submodule registration.** `roza/`, `doctorate-examples/`, `an-architecture-for-automatic-test-setup-code-refactoring-ieee-access/`, and `qualifying-exam/` are registered in `.gitmodules`. `artifacts/` is a plain directory at the umbrella root.

## Artifacts

The `artifacts/` directory stores PDF outputs from doctorate milestones. These files are the reference base for the next qualifying exam, papers, and the thesis: use them to recover earlier wording, structure, and committee feedback. Do not edit them in place; regenerate or revise content in the corresponding active project (`qualifying-exam/`, paper repos, etc.).

| File                                         | Origin                                                                      |
| -------------------------------------------- | --------------------------------------------------------------------------- |
| `qualification-exam-2019.pdf`                | Qualification document from the earlier cycle.                              |
| `qualification-exam-2019-presentation.pdf`   | Qualification presentation slides from the earlier cycle.                   |
| `qualification-exam-2019-notes-adenilso.pdf` | Committee notes from the qualification exam in the earlier cycle.           |
| `thesis-2019.pdf`                            | Thesis-related draft from the earlier cycle.                                |
| `progress-seminar-2025.pdf`                  | Progress seminar document after returning to the doctorate.                 |
| `progress-seminar-2025-presentation.pdf`     | Progress seminar slides after returning to the doctorate.                   |
| `progress-seminar-2025-notes-carina.pdf`     | Committee notes from the progress seminar after returning to the doctorate. |
| `lccss-a-similarity-metric-for-identifying-similar-test-code.pdf` | SBCARS 2020 paper proposing the LCCSS similarity metric. |
| `automating-test-class-refactoring-for-setup-reuse-a-clustering-based-approach.pdf` | Paper on clustering-based test class refactoring for setup reuse (implicit setup, LCCSS, experiment with 16 student programs). |

## Workflow

Project-local instructions override this file. Before editing, read the named project's local `AGENTS.md`, `.cursor/skills/`, `README.md`, or build files when they are relevant.

When the user names a milestone (qualifying exam, qualification, progress seminar, article, framework), default to the matching directory above rather than `artifacts/`.

## Definitions

**Treatment.** Test placement is treated as a global refactoring task: redistribute existing tests into classes that increase shared setup code without changing observed test behavior.

**Architecture.** A pipeline architecture for refactoring test code.

**Róża.** An extensible framework that instantiates the pipeline architecture by refactoring test classes through the implicit setup strategy.

**Proposal.** _"We propose (1) a pipeline architecture for refactoring test code, and (2) the Róża framework, an extensible framework that instantiates this architecture by refactoring test classes through the implicit setup strategy."_
