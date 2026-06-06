---
name: portuguese-academic-writing-style
description: Generates and revises Brazilian Portuguese academic prose in a formal thesis-and-article style. Use when writing or editing pt-BR text for thesis, dissertation, qualification, seminar report, abstract, introduction, and other academic sections in LaTeX or plain text.
---

# Portuguese academic writing style

Use this skill when producing or revising Brazilian Portuguese text for academic documents, including LaTeX manuscripts and `\input{}` chapter files. Tone, punctuation, and vocabulary follow the conventions below and the model passages in [examples.md](examples.md).

## Objective

Produce formal, continuous, argumentative academic prose: developed paragraphs, explicit logical chaining, and stable terminology from the work. Preserve technical content; adjust only form, tone, and conventions.

## Variant and register

**Use pt-BR.** Prefer Brazilian Portuguese over European Portuguese (e.g. `aplicação`, `linguagem`, `programa`, not pt-PT variants such as `ecrã` or `ficheiro`).

**Formal academic register.** Third person or impersonal constructions (`este trabalho`, `a proposta`, `o objetivo`). Avoid colloquialisms, contractions, and blog-like tone.

**Connected prose.** Prefer full chained sentences over telegraphic phrases or loose lists in body text. Numbered lists are acceptable in objectives, method steps, and explicit criteria.

## Punctuation

**Do not use em dashes** (`—` or `–`) for pauses, explanations, or enumerations in prose. Replace with comma, semicolon, colon, or period.

**Use semicolons** to separate parallel items in inline enumerations, multiple citations in one reference, and `Palavras-chave`.

**En-dash allowed only** when expanding English acronyms: `System Under Test – SUT`, `Java Virtual Machine – JVM`.

**Latin abbreviations.** Use `e.g.` for example and `i.e.` for that is, instead of `por exemplo` and `isto é`/`ou seja`, unless the user asks otherwise.

## Connectors and flow

Link paragraphs and sentences with markers common in this style:

- causal: `Isso porque`, `Diante disso,`, `Com isso,`
- sequence: `Assim,`, `Para isso,`, `Nesse sentido,`
- contrast: `Entretanto,`, `No entanto,`, `Embora`
- evidence: `Segundo`, `De acordo com`, `Conforme`, `Conforme definido por`

Definitions and framing use `consiste em`, `é enunciada da seguinte forma`, `tem como objetivo`, `visa`/`com o objetivo de`.

## Lists and enumerations

**Numbered objectives, steps, and criteria** follow this pattern:

```text
(1) primeiro item; (2) segundo item; e (3) terceiro item.
```

**Palavras-chave** in the abstract, separated by semicolons:

```text
Palavras-chave: teste de software; refatoração; reuso de código; métrica de similaridade; algoritmo de agrupamento.
```

**Organização do trabalho** may use semicolons between chapters and `e` before the last item.

## Work terminology

Keep terminology consistent within the document. For this research topic, prefer:

| Prefer | Avoid |
| ------ | ----- |
| código de teste | código de testes (except for occasional grammatical agreement) |
| reuso | reutilização |
| duplicação | duplicidade |
| refatoração | generic reformulation |
| classe de teste/classes de teste | classe de testes |
| configuração de acessórios | setup de fixtures (without translation on first occurrence) |
| configuração implícita | implicit setup (after defining the Portuguese term) |
| manutenibilidade | capacidade de manutenção (unless the distinction is needed) |
| métricas de similaridade | medidas de similaridade |
| algoritmos de agrupamento | clustering (alone, untranslated) |
| framework | quadro, estrutura |

**English terms** (`framework`, `setup`, `fixture`, `tear down`) may stay in English when they are established technical terms; on the first relevant occurrence, give the Portuguese equivalent in parentheses or in the immediate definition.

**Work acronyms:** `SUT`, `JVM`, `API`. Expand on first mention when the document does so.

## Academic section structure

**Resumo.** Open with the central theme and motivation; chain problem, approach, and contribution in one dense block; close with `Palavras-chave:`.

**Introdução.** Contextualize the domain; cite literature for general facts; narrow scope (`Este trabalho se enquadra em...`); present problem, hypothesis, objectives, and organization.

**Problema de pesquisa.** Describe the context, the limitation of the manual process, and the gap the work addresses.

**Hipótese.** Use `é enunciada da seguinte forma:` followed by a testable proposition, with numbered steps `(1)` and `(2)` when appropriate.

**Objetivos.** General objective with `consiste em`; specific objectives in a numbered list with semicolons.

**Fundamentação teórica.** Define before classifying (`X consiste em...`, `Y é dividido em...`). Explain figures in the flow (`A Figura N apresenta...`, `É possível observar que...`).

## LaTeX and formatting

When writing for LaTeX sources:

- preserve commands, labels, `\cite{}`, and existing structure;
- do not change section titles or template metadata unless explicitly asked;
- keep correct accents and cedilla in UTF-8;
- in running text, avoid unnecessary capitals beyond proper names and acronyms.

## Avoid

- em dashes in any syntactic role in prose;
- promotional tone or first person (`nós propomos`), unless the user asks;
- sequences of very short single-sentence paragraphs;
- avoidable anglicisms when a fixed Portuguese term already exists in the work;
- switching established terminology across sections (`reuso` vs `reutilização`).

## Workflow

1. Read the existing passage and neighboring section for coherence.
2. Draft or revise applying the rules above.
3. Check connectors, semicolons in lists, absence of em dashes, and stable terminology.
4. If the user asks for revision only, return the corrected text without long commentary, unless substantial changes require a brief note.

## Example reference

For model passages, read [examples.md](examples.md).
