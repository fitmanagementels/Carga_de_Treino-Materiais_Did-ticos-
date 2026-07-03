# Dotflows do OpenEvidence

Status: Diretriz operacional.

## Papel dos Dotflows neste projeto

Os Dotflows serao usados como modos padronizados de resposta dentro do OpenEvidence. Eles nao substituem o roteiro mestre nem produzem os produtos finais. A funcao deles e melhorar a coleta, triagem, comparacao e critica de evidencias antes da etapa de NotebookLM.

## Decisao de uso

O OpenEvidence tende a funcionar melhor com perguntas curtas, especificas e orientadas por evidencia do que com prompts longos tentando fazer muitas tarefas de uma vez.

Por isso:

- as rodadas reais serao feitas com Dotflows;
- cada rodada tera uma pergunta curta;
- cada output sera salvo bruto;
- o Codex fara auditoria antes de consolidar.

## Dotflows disponiveis

### `.COLETAR_BASE`

Funcao: abrir um tema e organizar o mapa conceitual amplo.

Quando usar:

- quando o tema ainda precisa de definicoes, fundamentos e panorama;
- antes de pedir analise de qualidade de evidencia;
- quando queremos linguagem teorica reaproveitavel.

### `.COLETAR_EVIDENCIA`

Funcao: identificar a melhor evidencia disponivel e a forca das afirmacoes.

Quando usar:

- uso pontual, nao como fluxo principal neste projeto;
- quando uma afirmacao cientifica sensivel precisar de blindagem;
- quando houver risco de exagero, controversia ou necessidade de revisar estudos/revisoes;
- evitar como primeira rodada para temas operacionais, porque tende a gerar output tecnico demais para o material dos trainees.

### `.COMPARAR_CONCEITOS`

Funcao: comparar duas ou mais ideias de forma estruturada.

Quando usar:

- RPE versus RIR;
- treinar ate a falha versus treinar proximo da falha;
- carga externa versus carga interna;
- sinais subjetivos versus sinais observaveis de fadiga;
- ajuste de peso versus ajuste de variacao/execucao.

### `.MAPEAR_LACUNAS`

Funcao: identificar o que a literatura ainda nao responde bem.

Quando usar:

- quando uma resposta parecer forte demais;
- quando o OpenEvidence generalizar;
- antes de transformar um ponto em afirmacao central da aula;
- para separar incerteza real de lacuna secundaria.

### `.RESUMIR_PARA_FONTE`

Funcao: consolidar outputs anteriores em uma fonte-base limpa, rastreavel e reutilizavel.

Quando usar:

- em projetos futuros, quando as rodadas estiverem no mesmo chat ou quando todos os outputs anteriores puderem ser fornecidos integralmente ao Dotflow;
- antes de enviar material ao NotebookLM, se o OpenEvidence tiver contexto suficiente;
- quando for preciso reduzir redundancia e preservar nuances.

Decisao neste projeto:

- nao usar `.RESUMIR_PARA_FONTE`;
- motivo: as rodadas foram executadas em chats separados, sem contexto compartilhado;
- substituto: consolidacao local no Codex em `07_fontes-e-evidencias.md`.

## Ordem recomendada para este projeto

1. `.COLETAR_BASE` para abrir temas e gerar material-fonte com linguagem mais aproveitavel.
2. `.MAPEAR_LACUNAS` para checar excesso de certeza e separar evidencia direta de inferencia pratica.
3. `.COMPARAR_CONCEITOS` apenas quando houver tensao conceitual importante.
4. `.COLETAR_EVIDENCIA` apenas de forma pontual, quando uma afirmacao sensivel exigir blindagem tecnica.
5. Auditoria no Codex.
6. Consolidacao em `07_fontes-e-evidencias.md`.
7. Uso do NotebookLM para produzir slides e ebook a partir da fonte refinada.

## Regras de salvamento

Cada output bruto deve ser salvo em `outputs/` com nome descritivo.

Nao editar o output bruto diretamente. Correcoes, auditorias e consolidacoes devem entrar em `revisoes/` ou no futuro arquivo consolidado de fontes.

## Criterios de auditoria no Codex

Cada output sera avaliado por:

- pertinencia ao roteiro;
- rastreabilidade das referencias;
- separacao entre evidencia direta e inferencia pratica;
- utilidade didatica;
- risco de exagero;
- lacunas restantes;
- destino no material: fonte, roteiro, checklist, diretriz ou descarte.
