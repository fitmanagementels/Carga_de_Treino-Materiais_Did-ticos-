# Fluxo de producao no NotebookLM

Status: Diretriz operacional atualizada para corpus amplo.

## Decisao de fluxo

Neste projeto, o NotebookLM sera usado primeiro como motor de leitura e sintese do corpus amplo. Depois, sera usado para apoiar a producao dos materiais finais.

Ele deve receber:

- `fluxo padrão/04_roteiro-mestre-rascunho.md`;
- `fluxo padrão/07_fontes-e-evidencias.md` como mapa de contexto e hierarquia;
- auditorias das rodadas;
- outputs brutos do OpenEvidence;
- diretrizes especificas de slides e ebook, quando forem criadas.

O NotebookLM pode construir uma fonte mestre, mas essa fonte deve voltar ao Codex para auditoria antes de orientar slides e ebook.

## Ordem recomendada

1. Subir roteiro, `07`, auditorias e outputs brutos no NotebookLM.
2. Configurar o chat do NotebookLM com o prompt de hierarquia.
3. Pedir sinteses por blocos/topicos, uma de cada vez.
4. Pedir a montagem de uma fonte mestre preliminar.
5. Trazer a fonte mestre preliminar ao Codex para auditoria.
6. Corrigir a fonte mestre no NotebookLM, se necessario.
7. Criar diretriz editorial do material.
8. Criar diretriz da apresentacao em slides.
9. Criar diretriz do ebook mobile-first.
10. Gerar slides e ebook por etapas.

## Regra central

Nao pedir produto final completo em um unico comando.

Usar comandos curtos por etapa, sempre com:

- objetivo do produto;
- publico: trainees de Educacao Fisica;
- foco: ajuste agudo da intensidade durante a sessao;
- exclusoes: registro de treino, performance esportiva, reabilitacao clinica e periodizacao complexa;
- linguagem: operacional, clara, profissional e pouco densa;
- exigencia de mini checklists quando for ebook.

## Cuidados com o NotebookLM

- Se o output ficar tecnico demais, pedir reducao de densidade e mais linguagem operacional.
- Se o output ficar generico demais, pedir mais decisao pratica do tipo "se observar X, ajuste Y".
- Se aparecer registro de treino como etapa central, corrigir imediatamente.
- Se o material virar aula de hipertrofia, performance ou periodizacao, reenquadrar para atendimento de publico geral.
- Se o NotebookLM criar nomes de metodo demais, pedir remocao de nomenclaturas extras.

## Prompts relacionados

Os prompts usados para criar a fonte mestre ja foram concluidos e agora ficam apenas como historico em:

- `prompts/historico/notebooklm-sistema-e-fonte-mestre.md`

Novos prompts de producao devem ser criados diretamente em `prompts/`, um arquivo por funcao real do fluxo, atualizando o proprio arquivo quando houver ajustes.

Prompts ativos para a etapa de produtos:

- `prompts/notebooklm-slides-producao.md`: configuracao do chat, mapa da apresentacao, roteiro por lotes, apresentacao final em partes e revisao final.
- `prompts/notebooklm-ebook-estrutura-e-capitulos.md`: estrutura geral do ebook, capitulos separados, revisao/correcao por capitulo e revisao consolidada.
