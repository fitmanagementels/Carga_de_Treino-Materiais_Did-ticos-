---
type: reference
title: Intake Outputs NotebookLM Slides
created: 2026-06-30
tags:
  - notebooklm
  - outputs
  - slides
  - controle-carga
related:
  - '[[Intake Outputs NotebookLM Ebook]]'
  - '[[Auditorias Produtos NotebookLM]]'
  - '[[Diretriz Apresentacao Slides]]'
  - '[[Fontes para o NotebookLM - produtos finais]]'
  - '[[Fluxo de producao no NotebookLM]]'
  - '[[Roteiro Mestre]]'
  - '[[Fonte Mestre Validada]]'
---

# Outputs NotebookLM - slides

Use esta pasta para salvar as respostas brutas do NotebookLM relacionadas a apresentacao em slides. Estes arquivos preservam o que a ferramenta retornou para auditoria posterior; nao devem ser editados para "melhorar" a resposta.

## Contexto de producao

Antes de gerar ou salvar outputs aqui, confira:

- `prompts/notebooklm-slides-producao.md`
- `diretrizes/fontes-notebooklm-produtos.md`
- `diretrizes/notebooklm-fluxo-producao.md`
- `diretrizes/diretriz-apresentacao-slides.md`
- `diretrizes/criterios-linguagem-densidade-operacional.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `fluxo padrão/08_fonte-mestre-validada.md`

Wiki-links de referencia: [[Diretriz Apresentacao Slides]], [[Fontes para o NotebookLM - produtos finais]], [[Fluxo de producao no NotebookLM]], [[Roteiro Mestre]], [[Fonte Mestre Validada]].

## Sequencia recomendada

Salvar cada rodada como arquivo separado, mantendo a diferenca entre Conversa e Studio.

### Conversa

- `notebooklm-chat-00-confirmacao-hierarquia.md`
- `notebooklm-chat-01-mapa-geral.md`
- `notebooklm-chat-02-roteiro-lote-1.md`
- `notebooklm-chat-03-roteiro-lote-2.md`
- `notebooklm-chat-04-roteiro-lote-3.md`
- `notebooklm-chat-05-revisao-roteiro.md`
- `notebooklm-chat-06-auditoria-studio.md`

### Studio

- `notebooklm-studio-a-apresentacao-unica.md`
- `notebooklm-studio-b1-parte-1.md`
- `notebooklm-studio-b2-parte-2.md`
- `notebooklm-studio-b3-parte-3.md`
- `notebooklm-studio-c-correcao.md`

Se o NotebookLM dividir a apresentacao em mais partes, continuar a sequencia sem sobrescrever arquivos anteriores.

## Padrao de cabecalho por output

Ao colar um output bruto, iniciar o arquivo com este bloco:

```markdown
# NotebookLM slides - [rodada]

Origem: NotebookLM
Data: YYYY-MM-DD
Prompt usado: `prompts/notebooklm-slides-producao.md` - [nome do prompt]
Fontes principais no notebook:
- `fluxo padrão/01_briefing-inicial.md`
- `fluxo padrão/03_arquitetura-logica-rascunho.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `fluxo padrão/08_fonte-mestre-validada.md`
- `diretrizes/diretriz-apresentacao-slides.md`

Status: bruto, ainda nao auditado.
```

## Regras de uso

- Nao corrigir o texto dentro do output bruto.
- Nao misturar no mesmo arquivo mapa, roteiro, partes finais e revisao.
- Nao usar outputs intermediarios do NotebookLM como fonte para novos produtos, exceto em notebook separado de auditoria ou comparacao.
- Registrar problemas, decisoes e correcoes em `revisoes/produtos/`.
- Consolidar versoes finais apenas depois da auditoria contra [[Fonte Mestre Validada]], [[Roteiro Mestre]] e [[Diretriz Apresentacao Slides]].

## Onde auditar

Auditorias, comparacoes entre partes, diagnosticos e prompts de correcao devem entrar em `revisoes/produtos/README.md` e nos arquivos de revisao criados dentro de `revisoes/produtos/`.
