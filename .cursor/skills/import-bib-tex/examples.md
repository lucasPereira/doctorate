# Import BibTeX examples

Run commands from the LaTeX project root. Replace `<bib>` and `<tex>` with the resolved file paths. Rules and workflow: [SKILL.md](SKILL.md).

## Resolving target files

**User names files**

```bash
python3 .cursor/skills/import-bib-tex/scripts/import-bibtex.py \
  --bib thesis/references.bib \
  --tex thesis/thesis.tex \
  --entry '@article{...}'
```

**Infer from `\bibliography{...}`**

Main file `qualification/qualification.tex` contains `\bibliography{qualification}` → use `qualification/qualification.bib` and `qualification/qualification.tex`.

## New single-author book

**Input**

```bibtex
@book{Meszaros07,
  author = {Meszaros, Gerard},
  title = {xUnit Test Patterns: Refactoring Test Code},
  publisher = {Pearson Education},
  year = {2007}
}
```

**Result key:** `meszaros:2007`

**Output fragment**

```bibtex
@book{meszaros:2007,
	title={xUnit Test Patterns: Refactoring Test Code},
	author={Meszaros, Gerard},
	year={2007},
	publisher={Pearson Education}
}
```

## Strip abstract from incoming entry

**Input**

```bibtex
@article{a5ca128a-76cb-3df0-bd72-44b50e076e59,
  author = {Yang Yang and Colin Onita and Xihui Zhang and Jasbir Dhaliwal},
  title = {TESTQUAL: Conceptualizing Software Testing as a Service},
  journal = {e-Service Journal},
  volume = {7},
  number = {2},
  pages = {46--65},
  year = {2011},
  abstract = {ABSTRACT Software testing has emerged as a distinct and critical component...}
}
```

**Output fragment** (no `abstract` field)

```bibtex
@article{yang:etal:2011,
	title={TESTQUAL: Conceptualizing Software Testing as a Service},
	author={Yang Yang and Colin Onita and Xihui Zhang and Jasbir Dhaliwal},
	year={2011},
	journal={e-Service Journal},
	volume={7},
	number={2},
	pages={46--65}
}
```

## New multi-author inproceedings

**Input**

```bibtex
@inproceedings{greiler_test_2013,
  author = {Greiler, M. and van Deursen, A. and Storey, M. A.},
  title = {Test Code Quality and Its Relation to Issue Handling Efficiency},
  booktitle = {Proceedings of the 2013 International Workshop on Principles of Software Evolution},
  pages = {1--4},
  year = {2013},
  publisher = {ACM}
}
```

**Result key:** `greiler:etal:2013`

## Collision with letter suffixes

`<bib>` already has `smith:2020` (article A). User imports another `smith:2020` (article B).

**After import**

- Article A → `smith:2020:a`
- Article B → `smith:2020:b`

**`<tex>` before**

```latex
\cite{smith:2020}
```

**`<tex>` after** (cite referred to article A)

```latex
\cite{smith:2020:a}
```

## Normalize existing file

```bash
python3 .cursor/skills/import-bib-tex/scripts/import-bibtex.py \
  --bib <bib> \
  --tex <tex> \
  --normalize-only
```

## Script invocation

```bash
python3 .cursor/skills/import-bib-tex/scripts/import-bibtex.py \
  --bib <bib> \
  --tex <tex> \
  --entry '@article{...}'
```
