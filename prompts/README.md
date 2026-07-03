# Prompts externos

Esta pasta guarda apenas prompts e orientacoes operacionais que ainda serao usados no projeto.

## Regra de atualizacao

Quando um prompt ativo precisar de ajuste, atualizar o proprio arquivo em vez de criar uma nova versao paralela.

Crie um novo prompt apenas quando houver uma nova funcao real no fluxo, por exemplo: uma rodada de producao de slides, uma rodada de producao do ebook, uma auditoria especifica ou uma correcao externa com objetivo diferente.

## Prompts de geracao de produtos

Use estes prompt packs para produzir os materiais finais no NotebookLM em etapas auditaveis. Eles nao substituem a fonte mestre validada nem os documentos de diretriz; apenas orientam a geracao externa dos produtos.

- `notebooklm-slides-producao.md`: prompt pack ativo para criar mapa, roteiro slide a slide, apresentacao em partes e revisao final dos slides.
- `notebooklm-ebook-estrutura-e-capitulos.md`: prompt pack ativo para criar a estrutura do ebook mobile-first, escrever capitulos separadamente e revisar/corrigir os outputs.

## Arquivo ativo

- `notebooklm-slides-producao.md`: prompts separados para Conversa e Studio do NotebookLM; a Conversa planeja/audita com memoria, o Studio recebe comandos unicos para gerar artefatos.
- `notebooklm-ebook-estrutura-e-capitulos.md`: prompts em etapas para criar a estrutura do ebook mobile-first, escrever capitulos por vez e revisar/corrigir outputs do NotebookLM.

## Historico

Prompts substituidos, concluidos ou abandonados ficam em `prompts/historico/` apenas para rastreabilidade. Eles nao devem orientar novas producoes sem revisao.
