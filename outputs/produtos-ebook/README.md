---
type: reference
title: Intake Outputs NotebookLM Ebook
created: 2026-06-30
tags:
  - notebooklm
  - outputs
  - ebook
  - mobile-first
  - controle-carga
related:
  - '[[Intake Outputs NotebookLM Slides]]'
  - '[[Auditorias Produtos NotebookLM]]'
  - '[[Diretriz Ebook Mobile First]]'
  - '[[Fontes para o NotebookLM - produtos finais]]'
  - '[[Fluxo de producao no NotebookLM]]'
  - '[[Roteiro Mestre]]'
  - '[[Fonte Mestre Validada]]'
---

# Outputs NotebookLM - ebook

Use esta pasta para salvar as respostas brutas do NotebookLM relacionadas ao ebook mobile-first. Cada capitulo ou rodada estrutural deve ficar em arquivo separado para facilitar auditoria, correcao e consolidacao posterior.

## Contexto de producao

Antes de gerar ou salvar outputs aqui, confira:

- `prompts/notebooklm-ebook-estrutura-e-capitulos.md`
- `diretrizes/fontes-notebooklm-produtos.md`
- `diretrizes/notebooklm-fluxo-producao.md`
- `diretrizes/diretriz-ebook-mobile-first.md`
- `diretrizes/criterios-linguagem-densidade-operacional.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `fluxo padrão/08_fonte-mestre-validada.md`

Wiki-links de referencia: [[Diretriz Ebook Mobile First]], [[Fontes para o NotebookLM - produtos finais]], [[Fluxo de producao no NotebookLM]], [[Roteiro Mestre]], [[Fonte Mestre Validada]].

## Sequencia recomendada

Salvar cada rodada como arquivo separado, mantendo a numeracao do fluxo:

- `notebooklm-ebook-00-estrutura-geral.md`
- `notebooklm-ebook-00-revisao-estrutura.md`
- `notebooklm-ebook-01-capitulo-1.md`
- `notebooklm-ebook-02-capitulo-2.md`
- `notebooklm-ebook-03-capitulo-3.md`
- `notebooklm-ebook-04-capitulo-4.md`
- `notebooklm-ebook-05-capitulo-5.md`
- `notebooklm-ebook-06-capitulo-6.md`
- `notebooklm-ebook-07-capitulo-7.md`
- `notebooklm-ebook-08-capitulo-8.md`
- `notebooklm-ebook-09-revisao-consolidada.md`

Quando um capitulo for revisado pelo NotebookLM, salvar a resposta bruta da revisao com o mesmo prefixo do capitulo e sufixo `-revisao`, por exemplo:

- `notebooklm-ebook-01-capitulo-1-revisao.md`
- `notebooklm-ebook-05-capitulo-5-revisao.md`

Se o capitulo 5 for dividido em decisao de ajuste e botoes de ajuste, usar:

- `notebooklm-ebook-05a-capitulo-5-decisao.md`
- `notebooklm-ebook-05b-capitulo-5-botoes-ajuste.md`

## Padrao de cabecalho por output

Ao colar um output bruto, iniciar o arquivo com este bloco:

```markdown
# NotebookLM ebook - [estrutura ou capitulo]

Origem: NotebookLM
Data: YYYY-MM-DD
Prompt usado: `prompts/notebooklm-ebook-estrutura-e-capitulos.md` - [nome do prompt]
Fontes principais no notebook:
- `fluxo padrão/01_briefing-inicial.md`
- `fluxo padrão/03_arquitetura-logica-rascunho.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `fluxo padrão/08_fonte-mestre-validada.md`
- `diretrizes/diretriz-ebook-mobile-first.md`

Status: bruto, ainda nao auditado.
```

## Regras de uso

- Nao corrigir o texto dentro do output bruto.
- Nao colar o ebook inteiro em um unico arquivo se ele foi gerado por capitulos; usar `notebooklm-ebook-09-revisao-consolidada.md` apenas para a revisao final do conjunto.
- Nao aceitar tabelas largas, paragrafos longos ou densidade de apostila sem auditoria.
- Registrar problemas, decisoes e correcoes em `revisoes/produtos/`.
- Consolidar versoes finais apenas depois da auditoria contra [[Fonte Mestre Validada]], [[Roteiro Mestre]] e [[Diretriz Ebook Mobile First]].

## Onde auditar

Auditorias de estrutura, capitulos, densidade mobile-first, continuidade entre capitulos e prompts de correcao devem entrar em `revisoes/produtos/README.md` e nos arquivos de revisao criados dentro de `revisoes/produtos/`.
