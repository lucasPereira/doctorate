# Write from references examples

Invocation patterns and expected deliverables. Rules: [SKILL.md](SKILL.md).

## Example 1 — Draft qualification introduction

**User request**

> Use write-from-references to draft the introduction for qualification. Cover context, problem, proposal, objectives, and organization. Portuguese.

**Agent actions**

1. Glob `qualification/**/*.tex`, `an-architecture-for-automatic-test-setup-code-refactoring-ieee-access/**/*.tex`, `artifacts/**/*.pdf`.
2. Grep the corpus for introduction, problema, objetivos, pipeline, Róża.
3. Read hits across all files (e.g. `introduction.tex`, `qualification.tex`, `paper.tex`, `progress-seminar-2025.pdf`, `qualification-exam-2019.pdf`).
4. Draft `\chapter{Introdução}` body in pt-BR with `\citeonline{}` / `\cite{}`.
5. Import missing entries from `bibliography.bib` via import-bib-tex into `qualification.bib`.
6. Return draft + report listing every source file consulted.

**Report fragment**

```text
Sources consulted:
- qualification/introduction.tex, qualification/qualification.tex
- an-architecture-for-automatic-test-setup-code-refactoring-ieee-access/paper.tex
- artifacts/progress-seminar-2025.pdf, artifacts/qualification-exam-2019.pdf
Imported: greiler:2013, kumari:2018 (from bibliography.bib).
Reference gaps: none.
```

## Example 2 — Single paragraph from IEEE Access

**User request**

> Write one paragraph on implicit setup for introduction.tex, based on the IEEE Access paper.

**Agent actions**

1. Grep all `*.tex` in both LaTeX subprojects for implicit setup / fixture setup.
2. Read matching sections in every hit file.
3. Translate and adapt to pt-BR per portuguese-academic-writing-style.
4. Reuse `\cite{meszaros:2007}` if already in `qualification.bib`; otherwise import from `bibliography.bib`.
5. Return one LaTeX paragraph only.

## Example 3 — PDF-only citation gap

**User request**

> Add the hypothesis wording from progress-seminar-2025.pdf.

**Agent actions**

1. Read `artifacts/progress-seminar-2025.pdf` (and grep other PDFs if the topic appears elsewhere).
2. Draft the `\section{Hipótese}` paragraph.
3. If the PDF mentions a source not present in any workspace `.bib`, insert `% TODO: cite — ...` and report:

```text
Reference gaps:
- Source: artifacts/progress-seminar-2025.pdf
  Visible reference: Smith (2020) — partial title only
  Action: user to supply BibTeX or DOI
```

## Example 4 — Apply draft to target workspace

**User request**

> write-from-references: draft objetivos and put them in introduction.tex.

**Agent actions**

1. Search the full reference corpus for objetivos wording.
2. Replace or append the objetivos block in `qualification/introduction.tex` (the target workspace).
3. Do not edit `paper.tex`, `artifacts/`, or other read-only references.
4. Run import-bib-tex for any new keys in `qualification.bib` before finishing.
5. Summarize edits, sources consulted, and imported keys in the reply.
