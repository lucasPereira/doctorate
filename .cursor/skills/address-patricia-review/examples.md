## Inline wording

Only the replacement token belongs inside `\lucas{...}` when the surrounding sentence is unchanged.

```latex
% Before
In this setting \patricia{(não seria melhor "context" ao invés de "setting"?)}, maintainability is critical.

% After
In this \lucas{context}, maintainability is critical.
```

## Replacement in the middle of a sentence

When grammar requires small surrounding adjustments, mark only the adjusted tokens.

```latex
% Before
The framework \patricia{(Roza framework ou Roza UI???)} during the clustering stage.

% After
The \lucas{UI} during the clustering stage.
```

## Structural change

If the resolved comment only moves or removes content, delete the note at the old location without adding `\lucas{...}` there.

```latex
% Before
\subsection{Illustrative use case}
...
\patricia{(tirar da seção Evaluation?)}

% After moving content
\subsection{Illustrative use case}
...
```

## Overbroad markup

Do not wrap a whole sentence when only one word changed.

```latex
% Do not use
\lucas{In this context, maintainability is critical and tests evolve together with production code.}
```
