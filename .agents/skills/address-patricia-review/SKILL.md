---
name: address-patricia-review
description: Resolve Patricia advisor review notes marked with \patricia{...} in LaTeX manuscripts. Apply approved text changes, wrap only modified spans in \lucas{...}, and remove the resolved \patricia{...}. Use when the user asks to address, fix, apply, or modify text for a Patricia comment, Patricia review, or \patricia markup.
disable-model-invocation: true
---

# Address Patricia review

Resolves advisor comments written as `\patricia{...}` in LaTeX manuscripts. Patricia's notes are red; accepted author changes are marked with `\lucas{...}` in blue.

## Resolving target files

Identify the manuscript and its root `.tex` before editing.

**User names a file.** Edit that file and any related sources the note points to.

**User does not name a file.** Search for `\patricia{` in `.tex` files. If one file contains the note, use it. If several files match, ask which note to address.

**Find the manuscript root.** The root is the `.tex` with `\documentclass` that `\input{}` or `\include{}` the edited file, directly or through other chapters. If the note is already in the root file, that file is the root.

**Find related sources.** From the root `.tex`, resolve the paired `.bib` through `\bibliography{...}` or `\addbibresource{...}` (without extension). Follow `\input{}`, `\include{}`, and literal file paths in the note to reach snippet or figure sources.

## Decision rules

These rules decide whether the agent should edit immediately, discuss a note, or leave the text unchanged.

**Treat comments as feedback, not commands.** Evaluate Patricia's note against the surrounding text, terminology, claims, and document structure. If the note is wrong, based on a misunderstanding, or would weaken the manuscript, say so and explain briefly.

**Ask or propose an alternative when the note is risky.** Do not change experimental numbers, statistics, claims, citations, labels, or section structure unless the user confirms the change or the requested edit clearly preserves the manuscript's meaning.

**Ask the user when intent is unclear.** If you are not sure whether Patricia wants a change, say what you understood, what is ambiguous, and practical options; ask before editing. Do not treat reviewer confusion or missing background as an automatic rewrite request.

**Use enough context before editing.** Read the relevant sentence, paragraph, section heading, citations, figures, or tables before deciding how to address the note.

## Markup rules

These rules define how resolved comments must appear in the LaTeX source and in the review PDF.

**Remove resolved Patricia notes.** Delete the full `\patricia{...}` command once the note has been addressed.

**Mark only modified text.** Wrap only the changed word, phrase, sentence, or clause in `\lucas{...}`. Do not wrap unchanged surrounding text, and never leave `\patricia{...}` inside `\lucas{...}`.

**Avoid fake markup for structural edits.** If the fix only moves or removes content, delete the old `\patricia{...}` note without adding `\lucas{...}` at that location. Add `\lucas{...}` only where wording actually changed.

## Editing rules

These rules apply when the user asks to apply a Patricia review comment.

**Preserve document structure.** Keep labels, references, citations, template structure, and existing macros stable unless the comment requires changing them.

**Edit source files, not rendered output.** Change the target `.tex` for manuscript text, paired `.bib` files for references, and included snippet or figure sources when the note points there.

**Check remaining comments in scope.** Before finishing a scoped fix, search for `\patricia{` in the edited manuscript and report whether the addressed note is gone and whether unrelated notes remain.

## Response rules

These rules keep responses short while giving the user enough information to continue reviewing.

**Use an analysis format when not editing.** If the user asks to discuss a note before applying it, respond with `Understanding`, `Does it make sense?`, and `Proposed change`.

**Confirm applied markup after editing.** After editing, state what was wrapped in `\lucas{...}`, confirm that the relevant `\patricia{...}` note was removed, and mention validation.

**Consult examples only when needed.** Use [examples.md](examples.md) when the markup boundary is ambiguous.

## Validation

Compile after substantive manuscript edits when possible. From the directory that contains the manuscript root, run `latexmk -pdf -interaction=nonstopmode -halt-on-error <root>.tex`.

Report compile failures and unresolved review notes in the edited scope.
