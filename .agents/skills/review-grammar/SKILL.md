---
name: review-grammar
description: Review and correct grammar, spelling, punctuation, agreement, clarity, captions, tables, figures, and code-snippet prose in academic writing in English or Brazilian Portuguese. Use when the user asks for a grammar review, proofreading, language polish, ortografia, or corrections to LaTeX manuscript text.
disable-model-invocation: false
---

# Review grammar

Corrects grammar, clarity, and readability in LaTeX manuscripts without changing technical meaning. Grammar-only review: do not alter claims, terminology, citations, or structure unless the user asks.

## Language

Choose rules from [English](#english) or [Brazilian Portuguese](#brazilian-portuguese) after the target language is known.

**Detect language.** Infer from the file content, document class, abstract language, or user request.

**Ask when unclear.** Confirm language before editing mixed or bilingual passages.

## Scope

This skill covers language polish in manuscript text and labels, not technical rewrites.

- Spelling, accent, and cedilla errors.
- Punctuation and spacing.
- Agreement and regência errors.
- Unclear, awkward, or repetitive wording.
- Capitalization in headings, captions, tables, and figures.
- Caption, table, figure, and diagram label text.
- Comments and messages in code snippets.
- Editable figure sources (`.dot`, `.mmd`, `.tex`, `.svg`).

## Workflow

Read context first, edit language only, then validate when practical.

**Read context.** Understand the paragraph, section, figure, table, or listing before changing wording.

**Separate language from technical edits.** Apply fixes that preserve meaning. Ask before changing claims, terminology, citations, or structure.

**Preserve LaTeX.** Keep commands, labels, `\ref{}`, `\cite{}`, math, bibliography keys, paths, and advisor macros intact unless the user asks otherwise.

**Limit code edits to prose.** Change comments, messages, and labels only unless the user asks for code changes.

**Edit figures at the source.** Prefer `.dot`, `.mmd`, `.tex`, or `.svg` over rendered images.

**Validate.** Run a LaTeX build or diagram render when the change type allows it.

**Report briefly.** Summarize edits; note only unresolved ambiguity or risky wording.

## Shared rules

These rules apply in English and pt-BR.

**Concise sentences.** Prefer a simpler sentence when meaning stays the same.

**Consistent terminology.** Match terms already used in the document.

**Stable voice and tense.** Change only when grammar or local clarity requires it.

**Formal tone.** Avoid informal phrasing.

**No new technical content.** Do not add claims, citations, or simplified substitutes for technical terms.

**Latin abbreviations.** Use `e.g.` for example and `i.e.` for that is.

**No em dashes in prose.** Replace `—` and `–` used as pauses with comma, semicolon, colon, or period.

**Capitalization.** Match the manuscript pattern in headings and captions.

## English

Apply [shared rules](#shared-rules) plus these checks.

**Agreement.** Fix subject-verb and noun-pronoun agreement.

**Apostrophes.** Correct possessives; expand contractions in formal prose.

## Brazilian Portuguese

Apply [shared rules](#shared-rules) plus these checks.

**Grammar.** Fix verbal and nominal agreement, regência, crase, and accentuation.

## Response

Keep replies short. Templates and the no-edit review format: [reference.md](reference.md).
