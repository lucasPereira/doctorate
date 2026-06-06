---
name: write-from-references
description: Drafts academic LaTeX prose by searching all .tex files in qualification/ and the IEEE Access submodule, all PDFs in artifacts/, and resolving citations through import-bib-tex. Use when the user asks to write or draft a section from prior doctorate materials and wants citations included.
disable-model-invocation: true
---

# Write from references

Drafts academic LaTeX from the user's brief and prior doctorate manuscripts. Searches the [reference corpus](#reference-corpus), resolves citations into the target `.bib` via [import-bib-tex](../import-bib-tex/SKILL.md), and returns a source-and-citation report. Invoke when the user asks to write or draft a section from those materials with citations included.

## Reference corpus

Read-only sources for wording, structure, claims, and citation keys. Corpus search steps live in [reference.md](reference.md); PDF inventory in [Artifacts](../../AGENTS.md#artifacts).

| Location                                                                 | Include              |
| ------------------------------------------------------------------------ | -------------------- |
| `qualification/`                                                         | Every `*.tex` file   |
| `an-architecture-for-automatic-test-setup-code-refactoring-ieee-access/` | Every `*.tex` file   |
| `artifacts/`                                                             | Every `*.pdf` file   |

Also read paired `.bib` files in the LaTeX subprojects.

**Read-only references.** Do not edit files used only as sources: all of `artifacts/`, and corpus `*.tex` outside the target workspace.

**Write target.** Edit only the workspace being worked on (the named target file and its paired `.bib`). If a corpus file is that target, reading and editing it is allowed.

**Prefer newer `.tex`.** When sources disagree, prefer active LaTeX over older PDFs in `artifacts/`.

**Search the full corpus.** Glob every file group and grep for the topic; do not stop at `paper.tex` or one chapter.

## Inputs

Collect before drafting. Ask only for what is missing.

- **Topic or section.** e.g. contextualização, problema de pesquisa, objetivos.
- **Target file.** e.g. `qualification/introduction.tex`. Infer from context when omitted.
- **Language.** Infer from target, corpus, or user; ask when unclear.
- **Scope.** Length, subsections, claims to keep or omit, other constraints.

The target may sit inside the corpus; still search every corpus file.

## Workflow

1. Read [reference.md](reference.md).
2. Glob and grep the [reference corpus](#reference-corpus); read all hits.
3. Resolve target `.bib` and `.tex` ([Resolving target files](../import-bib-tex/SKILL.md#resolving-target-files)).
4. Draft LaTeX for the user's brief from recovered material.
5. Resolve citations ([Citation resolution](reference.md#citation-resolution)).
6. Apply [portuguese-academic-writing-style](../portuguese-academic-writing-style/SKILL.md) when target language is pt-BR.
7. Return [output](#output).

Read each subproject `AGENTS.md` before editing the target workspace. When the user asks for a repo edit, change only files in that workspace (typically the named target file and target `.bib` via import-bib-tex).

## Output

Return two blocks unless the user asked for a direct file edit.

**Draft.** LaTeX ready to paste or apply in the target workspace; preserve `\chapter{}`, labels, and structure.

**Source and citation report.** Sources consulted, adapted passages, keys added to the target `.bib`, and reference gaps ([format](reference.md#reference-gap-report-format)).

## Supporting files

- [reference.md](reference.md) — corpus search, citations, terminology.
- [examples.md](examples.md) — worked invocations.
