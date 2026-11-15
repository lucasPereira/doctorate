# Portuguese academic writing style examples

Representative passages that define this style, with annotations to guide new writing. The `e.g.` and `i.e.` abbreviations reflect the convention for new text. **Output prose stays in Portuguese**; annotations are in English.

## Abstract (Resumo)

```text
A manutenibilidade do código de teste é crucial durante a atividade de teste.
Isso porque uma baixa capacidade de manutenção do código de teste dificulta tanto
a adição de novos testes quanto o ajuste dos testes já existentes quando ocorrem
mudanças no código de aplicação. Mesmo que o código de teste já possua boa
manutenibilidade, ela tende a se degradar com o tempo sem um processo contínuo
de refatoração. Assim, é preciso que os testes sejam continuamente refatorados.

Palavras-chave: teste de software; refatoração; reuso de código; métrica de
similaridade; algoritmo de agrupamento; configuração implícita.
```

**Patterns:** thematic opening; `Isso porque` for causality; `Assim,` for intermediate conclusion; keywords separated by semicolons.

## Context with citations

```text
Teste de software é uma das atividades presentes no processo de
desenvolvimento e manutenção de software. A percepção sobre sua utilidade tem
evoluído nos últimos anos. Teste de software não é mais visto como uma atividade a
ser realizada apenas ao final da etapa de codificação para detectar falhas. A
atividade de teste passou a estar presente durante todo o processo de
desenvolvimento e manutenção de software (Bourque e Fairley, 2014).
```

**Patterns:** general claim; progressive refinement; citation at the end of the sentence; no em dash.

## Scope restriction

```text
Este trabalho se enquadra no contexto de testes automatizados codificados
manualmente. Nesse contexto, a qualidade do código de teste tem especial
importância, uma vez que, assim como o código da aplicação, o código de teste
também precisará ser mantido, compreendido e ajustado durante todo o projeto
(Greiler et al., 2013).
```

## Illustrative example (e.g.)

Original artifact:

```text
Por exemplo, considerando o teste apresentado na Figura 1 seria possível
utilizar métricas de similaridade que permitam identificar que as linhas 4 a 6 também
aparecem no teste apresentado na Figura 2.
```

Aligned with the `e.g.` convention:

```text
e.g., considerando o teste apresentado na Figura 1, seria possível utilizar
métricas de similaridade que permitam identificar que as linhas 4 a 6 também
aparecem no teste apresentado na Figura 2.
```

## Clarification (i.e.)

Original artifact:

```text
Isto é, evitar a identificação de dois trechos de código como duplicados
quando eles não são semanticamente equivalentes.
```

Aligned with the `i.e.` convention:

```text
i.e., evitar a identificação de dois trechos de código como duplicados quando
eles não são semanticamente equivalentes.
```

## Numbered steps

```text
Para isso, é necessário que o desenvolvedor realize as seguintes etapas:
(1) identifique testes com código comum; (2) agrupe os testes com código em comum
em classes de teste; e (3) extraia o código comum para um método compartilhado
entre os testes da classe.
```

**Patterns:** introduction with colon; items with `(n)`; semicolons between items; `e` before the last item.

## Research problem

```text
No contexto da implementação manual de código de teste, técnicas de reuso
de código são utilizadas durante a criação e manutenção dos testes para melhorar a
manutenibilidade (Fowler, 1999; Meszaros 2007). A aplicação manual de técnicas de
reuso de código é suscetível a erros de refatoração e demanda um esforço de
desenvolvimento que, por vezes, supera o ganho obtido com a melhoria na
manutenibilidade (Landhäußer e Tichy, 2012; Meszaros 2007), principalmente
quando o número de testes aumenta (Berner, Weber e Keller, 2005). O problema
está em aplicar técnicas de reuso de código de teste reduzindo o esforço de
desenvolvimento sem que erros ou inconsistências de refatoração possam ocorrer
durante o processo.
```

## Hypothesis

```text
Considerando o problema apresentado, a hipótese de pesquisa deste
trabalho é enunciada da seguinte forma: através de um método de refatoração
automatizado de classes de teste que (1) utiliza métricas de similaridade para
identificação de testes com código em comum e (2) algoritmos de agrupamento para
a criação de grupos de testes similares entre si, é possível reduzir a duplicação de
código de teste e, ao mesmo tempo, reduzir o esforço total de desenvolvimento dos
testes sem que o processo esteja suscetível a erros ou inconsistências.
```

## Objectives

```text
O objetivo geral deste trabalho consiste em reduzir a duplicação de código
de teste e reduzir o esforço total de desenvolvimento dos testes sem alterar o
resultado esperado dos testes. Para alcançar o objetivo geral, os seguintes objetivos
específicos deverão ser alcançados: (1) identificar métricas de similaridade
adequadas para identificar testes com código em comum; (2) identificar algoritmos
de agrupamento adequados para criar grupos de testes com código em comum
entre si; (3) definir um modelo para refatoração automática de classes de teste a
partir da utilização das métricas de similaridade e algoritmos de agrupamento; e (4)
definir um framework para o modelo com base na seleção das métricas de
similaridade e algoritmos de agrupamento mais adequados.
```

## Technical definition

```text
Um teste é um procedimento, manual ou automático, que pode ser usado
para verificar se um dado SUT funciona de acordo com o comportamento esperado.
O SUT representa a parte do sistema que está sendo testada. Cada teste deve
realizar, inicialmente, uma série de passos para colocar o SUT no estado desejado
para que o teste possa ser executado.
```

**Patterns:** definition with `é`; technical term introduced before the acronym; medium to long sentences.

## English acronym with en-dash

```text
...interações manuais com o sistema em teste (System Under Test – SUT) e a
geração baseada em modelos...
```

**Pattern:** en-dash only between English term and acronym; no em dash in Portuguese prose.

## Work organization

```text
Os demais capítulos deste trabalho são organizados da seguinte forma: no
Capítulo 2 é apresentada a fundamentação teórica; no Capítulo 3 é apresentado o
estado da arte e os trabalhos relacionados; no Capítulo 4 é apresentada a proposta
deste trabalho; e no Capítulo 5 é apresentada a conclusão e os próximos passos
para elaboração deste trabalho.
```

## Contrast and addition connectors

```text
Entretanto, a aplicação manual de técnicas de reuso de código de teste e o
agrupamento manual dos testes em classes são tarefas suscetíveis a erros e que
demandam esforço de desenvolvimento.

Além disso, essa estratégia pode dificultar a compreensão do teste nos
casos em que os acessórios forem muito complexos.
```
