---
type: reference
title: Auditorias Produtos NotebookLM
created: 2026-06-30
tags:
  - revisoes
  - auditoria
  - notebooklm
  - slides
  - ebook
  - controle-carga
related:
  - '[[Intake Outputs NotebookLM Slides]]'
  - '[[Intake Outputs NotebookLM Ebook]]'
  - '[[Diretriz Apresentacao Slides]]'
  - '[[Diretriz Ebook Mobile First]]'
  - '[[Fontes para o NotebookLM - produtos finais]]'
  - '[[Fluxo de producao no NotebookLM]]'
  - '[[Roteiro Mestre]]'
  - '[[Fonte Mestre Validada]]'
---

# Revisoes de produtos NotebookLM

Use esta pasta para auditorias, diagnosticos, comparacoes entre versoes e prompts de correcao dos outputs de slides e ebook gerados no NotebookLM.

Os outputs brutos devem ficar em:

- `outputs/produtos-slides/`
- `outputs/produtos-ebook/`

Wiki-links de referencia: [[Intake Outputs NotebookLM Slides]], [[Intake Outputs NotebookLM Ebook]], [[Diretriz Apresentacao Slides]], [[Diretriz Ebook Mobile First]], [[Fonte Mestre Validada]], [[Roteiro Mestre]].

## Quando criar uma revisao

Criar um arquivo de revisao quando houver:

- mapa geral de slides a auditar;
- roteiro de slides por lote;
- parte final da apresentacao;
- estrutura geral do ebook;
- capitulo de ebook;
- revisao consolidada do NotebookLM;
- diferenca relevante entre duas versoes;
- necessidade de prompt de correcao.

## Nomes recomendados

Slides:

- `auditoria-slides-00-mapa-geral.md`
- `auditoria-slides-01-roteiro-lote-1.md`
- `auditoria-slides-02-roteiro-lote-2.md`
- `auditoria-slides-03-roteiro-lote-3.md`
- `auditoria-slides-05-apresentacao-parte-1.md`
- `auditoria-slides-06-apresentacao-parte-2.md`
- `auditoria-slides-07-apresentacao-parte-3.md`
- `auditoria-slides-08-revisao-final.md`

Ebook:

- `auditoria-ebook-00-estrutura-geral.md`
- `auditoria-ebook-01-capitulo-1.md`
- `auditoria-ebook-02-capitulo-2.md`
- `auditoria-ebook-03-capitulo-3.md`
- `auditoria-ebook-04-capitulo-4.md`
- `auditoria-ebook-05-capitulo-5.md`
- `auditoria-ebook-06-capitulo-6.md`
- `auditoria-ebook-07-capitulo-7.md`
- `auditoria-ebook-08-capitulo-8.md`
- `auditoria-ebook-09-revisao-consolidada.md`

## Checklist de auditoria

Para qualquer produto, verificar:

- aderencia ao publico: trainees de Educacao Fisica em formacao para personal trainer com publico geral;
- foco central: ajuste agudo da intensidade durante a sessao;
- ausencia de registro de treino como etapa central da decisao aguda;
- respeito a [[Fonte Mestre Validada]] e ao [[Roteiro Mestre]];
- respeito a `diretrizes/fontes-notebooklm-produtos.md`;
- linguagem operacional, profissional e pouco academica;
- cautelas contra automatizar decisoes do tipo "se X, sempre faca Y";
- preservacao da hierarquia de fontes quando houver conflito.

Para slides, verificar tambem:

- cada slide tem titulo, texto visivel, elemento visual, layout, nota de fala, cautela e ancora de fonte;
- a apresentacao esta dividida em partes controladas, nao em produto unico longo;
- o texto em tela nao virou apostila;
- o elemento visual tem funcao didatica.

Para ebook, verificar tambem:

- capitulos estao separados e auditaveis;
- cada capitulo tem objetivo, secoes curtas, exemplos operacionais, mini checklist, frases de comunicacao quando relevantes e recapitulo;
- o formato mobile-first evita tabelas largas e paragrafos extensos;
- comparacoes e matrizes aparecem como cards, listas empilhadas ou blocos legiveis no celular.

## Modelo de arquivo de revisao

~~~markdown
---
type: analysis
title: Auditoria [produto e rodada]
created: YYYY-MM-DD
tags:
  - revisoes
  - notebooklm
  - slides-ou-ebook
related:
  - '[[Intake Outputs NotebookLM Slides]]'
  - '[[Intake Outputs NotebookLM Ebook]]'
  - '[[Fonte Mestre Validada]]'
  - '[[Roteiro Mestre]]'
---

# Auditoria [produto e rodada]

## Produto avaliado

- Arquivo bruto:
- Prompt usado:
- Data do output:

## Base de comparacao

- `fluxo padrão/08_fonte-mestre-validada.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `diretrizes/fontes-notebooklm-produtos.md`
- Diretriz especifica do produto:

## Diagnostico

[Aprovado, aprovado com ajustes pequenos, regerar uma parte, regerar tudo ou mudar diretriz antes de tentar de novo.]

## Problemas por prioridade

1. 
2. 
3. 

## Correcoes necessarias

- 

## Prompt de correcao, se necessario

```text
[Prompt pronto para colar no NotebookLM.]
```

## Decisao

- Status:
- Proxima acao:
~~~

## Regra de preservacao

Nao substituir um output bruto por uma versao corrigida. Se o NotebookLM gerar nova versao, salvar a nova resposta em `outputs/produtos-slides/` ou `outputs/produtos-ebook/` com novo numero ou sufixo `v2`, e registrar aqui o que mudou.
