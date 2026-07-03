# Auditoria - Dotflow 01 - Sinais de fadiga durante a execucao

Status: Auditoria inicial, reorganizada apos remocao do output `.COLETAR_EVIDENCIA`.

## Produto avaliado

Output bruto da Rodada 1 no OpenEvidence:

- `outputs/dotflow-01-fadiga-execucao-coletar-base.md`

Dotflows usados:

- `.COLETAR_BASE`

## Base de comparacao

- Briefing: aula para trainees de Educacao Fisica em treinamento interno para atuacao como personal trainer.
- Roteiro mestre: foco em ajuste agudo da intensidade durante a sessao.
- Bloco prioritario: `Bloco 6 - Sinais de fadiga durante a execucao`.
- Restricoes: nao focar em performance esportiva, reabilitacao clinica, periodizacao complexa ou registro de treino.

## Diagnostico

O output `.COLETAR_BASE` e mais adequado para esta etapa do projeto do que o `.COLETAR_EVIDENCIA`, porque entrega panorama, fundamentos e traducao pratica com menor risco de puxar o material para excesso de tecnicismo.

Mesmo assim, a consolidacao deve preservar uma cautela importante: a evidencia forte sustenta principalmente perda de velocidade, desempenho e marcadores instrumentais de fadiga. Ja sinais visuais como compensacoes, encurtamento de amplitude, instabilidade, hesitacao e alteracao respiratoria devem entrar como inferencias praticas plausiveis, nao como afirmacoes diretamente validadas por estudos de observacao olho-nu em contexto de personal training.

## Achados aproveitaveis

### Seguro para usar

- A reducao de velocidade de movimento e o indicador observavel/instrumental mais sustentado de fadiga durante series de treino de forca.
- A perda de velocidade se relaciona com fadiga neuromuscular, perda de desempenho e proximidade da falha.
- RPE/RIR e percepcao do aluno ajudam, mas nao devem substituir a observacao da execucao.
- Ha variabilidade individual importante; a leitura da fadiga precisa ser contextualizada por exercicio, aluno, nivel de experiencia e objetivo da serie.
- Treinar ate a falha tende a aumentar fadiga periferica, dano muscular e tempo de recuperacao em comparacao com parar antes da falha, embora isso dependa do protocolo e objetivo.

### Usar com cautela

- Percentuais de perda de velocidade, como 20% ou 40%, nao devem virar regra operacional rigida para trainees sem equipamento.
- Conclusoes oriundas de velocity-based training podem orientar o olhar do personal, mas nao equivalem automaticamente a avaliacao visual precisa.
- Sinais como compensacoes, encurtamento de amplitude, instabilidade, perda de fluidez, respiracao desorganizada e hesitacao sao uteis didaticamente, mas a evidencia direta para cada sinal isolado e limitada.
- Parte da literatura vem de homens treinados, power athletes, strength athletes, supino e agachamento; a transferencia para publico geral deve ser feita com ressalva.

### Descartar ou nao centralizar

- Detalhes de EMG, marcadores bioquimicos, CK, AST, lactato e amonia nao devem entrar nos slides principais.
- Discussao sobre recuperacao 48-72h pode aparecer apenas como contexto, nao como foco do bloco.
- Configuracoes cluster e periodizacao por velocity loss nao devem ser centrais neste material.

## Avaliacao do `.COLETAR_BASE`

Melhor para:

- construir panorama teorico;
- explicar mecanismos de fadiga;
- extrair linguagem para fonte tecnica;
- obter lista ampla de termos-chave.

Risco:

- fica tecnico demais;
- mistura conceitos laboratoriais com aplicacao pratica;
- tende a sugerir implicacoes operacionais que precisam de filtragem.

## Implicacao para o Bloco 6

O Bloco 6 deve ensinar o trainee a olhar para:

- velocidade: a repeticao ficou claramente mais lenta?
- fluidez: o movimento ficou quebrado ou travado?
- amplitude: a amplitude encurtou sem decisao tecnica?
- posicao: o aluno perdeu alinhamento ou estabilidade?
- compensacao: outro segmento passou a "resolver" o movimento?
- ritmo: pausas, acelerações e controle mudaram de forma relevante?
- expressao/comportamento: ha hesitacao, perda de confianca ou tolerancia reduzida?
- conflito relato-execucao: o aluno diz que esta bem, mas a execucao denuncia queda de qualidade?

Esses sinais devem ser apresentados como `pistas de julgamento`, nao como diagnosticos isolados de fadiga.

## Decisao

Aprovado com ajustes pequenos.

O output pode ser usado como fonte tecnica parcial para o pacote de evidencias, desde que a consolidacao:

- separe evidencia direta de inferencia pratica;
- reduza densidade tecnica para o publico trainee;
- nao transforme percentuais laboratoriais em regras rigidas;
- nao prometa precisao visual que a literatura nao validou diretamente.

## Proxima acao recomendada

Fazer uma rodada curta com `.MAPEAR_LACUNAS` antes de consolidar, usando uma pergunta muito especifica sobre sinais visuais sem equipamento.

Objetivo: confirmar quais lacunas impedem afirmacoes fortes e quais lacunas sao aceitaveis para uso pedagogico.

Prompt recomendado:

```text
Quais lacunas, incertezas ou limitacoes existem na literatura sobre usar sinais visuais observaveis sem equipamento durante series de treino de forca para orientar ajuste agudo de carga?

Considere reducao aparente de velocidade, perda de fluidez, compensacoes, encurtamento de amplitude, instabilidade, perda de posicao, mudanca de ritmo, respiracao desorganizada, hesitacao e conflito entre relato do aluno e qualidade da execucao.

Quero separar:
1. sinais com evidencia direta;
2. sinais com evidencia indireta plausivel;
3. sinais uteis pedagogicamente, mas sem validacao direta;
4. sinais que nao devem virar afirmacao forte em material didatico.
```

Salvar em:

`outputs/dotflow-05-lacunas-fadiga.md`

## Arquivo futuro a consolidar

Depois da rodada de lacunas, consolidar em:

`07_fontes-e-evidencias.md`
