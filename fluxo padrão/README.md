# Fluxo padrão

Esta pasta guarda os documentos estruturantes do projeto didatico.

Use esta pasta para arquivos que definem briefing, arquitetura, roteiro, estrategia de fontes, mapa de evidencias e fonte mestre validada.

## Arquivos

- `00_estado-projeto.md`: estado atual, decisoes assumidas e proximo checkpoint.
- `01_briefing-inicial.md`: briefing do material.
- `02_lacunas-para-validacao.md`: lacunas e respostas de validacao.
- `03_arquitetura-logica-rascunho.md`: arquitetura logica da aula.
- `04_roteiro-mestre-rascunho.md`: roteiro mestre validado.
- `05_estrategia-fontes-e-evidencias.md`: estrategia de fontes.
- `06_dotflows-open-evidence.md`: organizacao das rodadas de OpenEvidence.
- `07_fontes-e-evidencias.md`: mapa de contexto e evidencias.
- `08_fonte-mestre-validada.md`: fonte mestre validada para orientar produtos finais.

## Regra

Documentos de producao visual, editorial e operacional ficam em `diretrizes/`.

Prompts colaveis em ferramentas externas ficam em `prompts/`.

Outputs externos ficam em `outputs/`.

Auditorias e revisoes ficam em `revisoes/`.

## Regra de manutencao

Atualize os documentos ativos em vez de criar um novo arquivo para cada ajuste.

Exemplos:

- se o roteiro mudar, atualizar `04_roteiro-mestre-rascunho.md`;
- se a fonte mestre precisar de ajuste editorial validado, atualizar `08_fonte-mestre-validada.md`;
- se a regra de fontes do NotebookLM mudar, atualizar `diretrizes/fontes-notebooklm-produtos.md`;
- se a formatacao de slides mudar, atualizar `diretrizes/diretriz-apresentacao-slides.md`.

Crie novos arquivos apenas para novas categorias de artefato ou para preservar outputs externos e auditorias. Outputs do NotebookLM, outputs do OpenEvidence e auditorias podem permanecer como historico/rastreabilidade, mas nao devem virar uma cascata de documentos de producao paralelos.
