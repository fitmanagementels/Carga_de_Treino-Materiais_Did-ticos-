# Fontes para o NotebookLM - produtos finais

Status: diretriz operacional para montagem do notebook de producao dos produtos finais.

## Principio

Nem todo arquivo produzido no projeto deve virar fonte do NotebookLM para slides e ebook. Alguns arquivos sao historico operacional, auditoria ou etapa intermediaria. Se forem misturados com as fontes validadas, podem confundir a hierarquia, reintroduzir formulacoes antigas ou dar peso demais a correcoes que ja foram resolvidas.

## Fontes obrigatorias para o notebook de producao

Subir estes arquivos como fontes principais:

- `diretrizes/fontes-notebooklm-produtos.md`
- `fluxo padrão/01_briefing-inicial.md`
- `fluxo padrão/03_arquitetura-logica-rascunho.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `fluxo padrão/08_fonte-mestre-validada.md`
- `diretrizes/criterios-linguagem-densidade-operacional.md`
- `diretrizes/tema-visual-xsteam.md`
- `diretrizes/diretriz-apresentacao-slides.md`
- `diretrizes/diretriz-ebook-mobile-first.md`

Quando forem criadas, tambem subir:

- `diretrizes/roteiro-apresentacao.md`, quando for produzir a apresentacao em slides.
- `diretrizes/roteiro-ebook-mobile-first.md`, quando for produzir o ebook mobile-first.
- `prompts/notebooklm-slides-producao.md`, quando for produzir a apresentacao em slides.
- `prompts/notebooklm-ebook-estrutura-e-capitulos.md`, quando for produzir o ebook mobile-first.

## Fontes secundarias recomendadas

Subir como fontes secundarias, se o objetivo for preservar rastreabilidade e permitir consulta teorica:

- `fluxo padrão/07_fontes-e-evidencias.md`
- `outputs/dotflow-01-fadiga-execucao-coletar-base.md`
- `outputs/dotflow-02-rpe-rir-tecnica.md`
- `outputs/dotflow-03-falha-proximidade-fadiga.md`
- `outputs/dotflow-04-ajustes-agudos.md`
- `outputs/dotflow-05-lacunas-fadiga.md`

Essas fontes nao devem mandar na estrutura, no tom ou no escopo. Elas servem para sustentar conceitos, referencias e cautelas quando a fonte mestre pedir apoio.

## Fontes que nao devem entrar no notebook de producao

Nao subir como fontes para criar slides ou ebook:

- `outputs/notebooklm-00-checagem-hierarquia.md`
- `outputs/notebooklm-01-fonte-blocos-1-2.md`
- `outputs/notebooklm-02-fonte-blocos-3-4.md`
- `outputs/notebooklm-03-fonte-bloco-5.md`
- `outputs/notebooklm-04-fonte-bloco-6.md`
- `outputs/notebooklm-05-fonte-blocos-7-8.md`
- `outputs/notebooklm-06-revisao-transversal.md`
- `outputs/notebooklm-07-fonte-mestre-preliminar.md`
- `outputs/notebooklm-08-autocritica-fonte-mestre.md`
- `outputs/notebooklm-09-fonte-mestre-revisada.md`
- arquivos da pasta `revisoes/`

Motivo: esses arquivos foram etapas de construcao, revisao ou auditoria. A funcao deles ja foi incorporada em `fluxo padrão/08_fonte-mestre-validada.md` e nas diretrizes atuais.

## Hierarquia para informar ao NotebookLM

Ao pedir qualquer produto, usar esta hierarquia:

1. `fluxo padrão/01_briefing-inicial.md`, `fluxo padrão/03_arquitetura-logica-rascunho.md`, `fluxo padrão/04_roteiro-mestre-rascunho.md` e `fluxo padrão/08_fonte-mestre-validada.md` definem objetivo, publico, escopo, progressao e conteudo validado.
2. `diretrizes/roteiro-apresentacao.md`, para slides, e `diretrizes/roteiro-ebook-mobile-first.md`, para ebook, definem a estrutura especifica do produto em producao.
3. As demais diretrizes em `diretrizes/` definem linguagem, densidade, visual, formato e criterios de qualidade.
4. `fluxo padrão/07_fontes-e-evidencias.md` e os `dotflows` sao fontes secundarias de apoio teorico e rastreabilidade.
5. Se houver conflito, seguir os arquivos validados e as diretrizes, nao os outputs brutos.

## Regra de higiene

Nao usar outputs intermediarios do NotebookLM como fonte para novos produtos, exceto em um notebook separado de auditoria ou comparacao.
