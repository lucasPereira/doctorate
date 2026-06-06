# Write from references reference

Corpus search, citation resolution, and terminology. Workflow: [SKILL.md](SKILL.md). Examples: [examples.md](examples.md). PDF inventory: [Artifacts](../../AGENTS.md#artifacts).

## Corpus search

Follow [Reference corpus](SKILL.md#reference-corpus) in [SKILL.md](SKILL.md) for which paths to include. Then:

1. Glob all `*.tex` under `qualification/` and `an-architecture-for-automatic-test-setup-code-refactoring-ieee-access/`.
2. Glob all `*.pdf` under `artifacts/`.
3. Grep for section titles, keywords, and `\cite{...}` keys related to the topic.
4. Read matching regions in every hit file, not only the first match.

Partial reads are fine; do not skip a file without checking relevance.

### Paired bibliographies

| Directory | Paired `.bib` |
| --- | --- |
| `qualification/` | `qualification/qualification.bib` |
| `an-architecture-for-automatic-test-setup-code-refactoring-ieee-access/` | `bibliography.bib` |

## Artifacts

All PDFs under `artifacts/` are read-only reference sources. Corpus `.tex` outside the target workspace is read-only too.

## Reading PDF artifacts

Try the Read tool first. If extraction is poor or empty, use `pdftotext` when available:

```bash
pdftotext -layout artifacts/progress-seminar-2025.pdf -
```

When a PDF cites literature without bibliographic metadata, record a reference gap; do not guess BibTeX.

## Citation resolution

Every factual claim that had a citation in a source should keep a citation in the draft.

Resolve each work in this order:

1. Search the target project's `.bib` by key, author surname, or normalized title.
2. Search other workspace `.bib` files the same way.
3. If found only in step 2, import into the target `.bib` via [import-bib-tex](../import-bib-tex/SKILL.md).
4. If a source `.tex` cites a key, grep workspace `.bib` files for that key or title+year.
5. If still missing and the only source is a PDF, report a reference gap.

**Reuse source keys.** When a claim comes from a source `.tex`, prefer the same `\cite{...}` keys.

**PDF without BibTeX.** Do not invent a key. Keep the prose if requested, add `% TODO: cite — ...`, and report the gap.

**Duplicate work.** If import-bib-tex reports an existing key, use it; do not add a second entry.

**After import.** Use the key returned by import-bib-tex, not the source `.bib` key when they differ.

### Citation commands by target

For `qualification/`, use `abntex2cite`: `\citeonline{key}` for narrative mentions, `\cite{key}` for parenthetical references. For the IEEE Access submodule, follow `\cite{}` usage in that manuscript.

## Terminology

When the target language is pt-BR, follow [portuguese-academic-writing-style](../portuguese-academic-writing-style/SKILL.md). Keep established English technical terms where the target manuscript already does.

## Reference gap report format

List each unresolved citation once:

```text
- Source: artifacts/progress-seminar-2025.pdf (p. N approx.)
  Claim: ...
  Visible reference: Author (Year) — Title (partial)
  Action: provide BibTeX or ask user to confirm DOI
```
