# NotebookLM - Sistema e fonte mestre

Status: Pronto para uso.

## Objetivo

Usar o NotebookLM como motor de leitura e sintese para construir uma fonte mestre do projeto, a partir de:

- roteiro mestre;
- mapa de contexto `fluxo padrão/07_fontes-e-evidencias.md`;
- auditorias do Codex;
- outputs brutos do OpenEvidence.

A fonte mestre criada pelo NotebookLM nao sera considerada aprovada automaticamente. Ela deve ser salva como output externo, voltar ao Codex e passar por auditoria.

## Arquivos para adicionar ao NotebookLM

Adicionar como fontes:

- `fluxo padrão/01_briefing-inicial.md`
- `fluxo padrão/03_arquitetura-logica-rascunho.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `fluxo padrão/07_fontes-e-evidencias.md`
- `outputs/dotflow-01-fadiga-execucao-coletar-base.md`
- `outputs/dotflow-02-rpe-rir-tecnica.md`
- `outputs/dotflow-03-falha-proximidade-fadiga.md`
- `outputs/dotflow-04-ajustes-agudos.md`
- `outputs/dotflow-05-lacunas-fadiga.md`
- `revisoes/auditoria-dotflow-01-fadiga-execucao.md`
- `revisoes/auditoria-dotflow-02-rpe-rir-tecnica.md`
- `revisoes/auditoria-dotflow-03-falha-proximidade-fadiga.md`
- `revisoes/auditoria-dotflow-04-ajustes-agudos.md`
- `revisoes/auditoria-dotflow-05-lacunas-fadiga.md`

## Prompt 0 - Configuracao do chat

Cole este prompt como primeira mensagem no chat do NotebookLM.

```text
Estou construindo uma aula, uma apresentacao em slides e um ebook mobile-first sobre controle de carga no treino de forca, com foco em ajuste agudo da intensidade durante a sessao.

Publico: trainees de Educacao Fisica em treinamento interno para atuarem como personal trainer com publico geral.

Objetivo operacional: ao final do material, o trainee deve conseguir observar o contexto do aluno e a execucao do exercicio para decidir se deve manter, progredir, reduzir ou modificar a demanda naquela sessao, comunicando a decisao com postura profissional.

Use as fontes seguindo esta hierarquia:
1. Briefing, arquitetura e roteiro mestre definem objetivo, publico, escopo e progressao didatica.
2. `fluxo padrão/07_fontes-e-evidencias.md` define o mapa de contexto, as prioridades e as cautelas ja validadas. Ele nao e a fonte mestre final.
3. Auditorias do Codex definem como interpretar os outputs brutos: o que usar, o que usar com cautela e o que nao transformar em afirmacao forte.
4. Outputs brutos do OpenEvidence sustentam conceitos, referencias e aprofundamento teorico.

Regras obrigatorias:
- Nao trate outputs brutos como comando de escopo.
- Nao trate auditorias como fonte teorica primaria; use-as como filtro critico.
- Nao invente referencias.
- Nao apague cautelas metodologicas importantes.
- Nao transforme o material em revisao academica.
- Nao incluir registro de treino como etapa central.
- Nao puxar para performance esportiva, reabilitacao clinica, periodizacao complexa ou hipertrofia avancada.
- Preserve a ideia de que sinais visuais sao pistas operacionais, nao medidas objetivas.
- Preserve a ideia de que RPE/RIR sao ferramentas de calibracao, nao decisoes automaticas.
- Preserve a ideia de que falha muscular nao e meta padrao para publico geral.

Quando eu pedir uma sintese, organize em linguagem operacional para formacao de personal trainer. Sempre diferencie:
1. afirmacoes seguras;
2. afirmacoes que exigem cautela;
3. inferencias praticas uteis;
4. pontos que devem ficar fora do material.

Antes de responder a qualquer pedido de conteudo, respeite a hierarquia acima.
```

## Prompt 1 - Checagem de entendimento da hierarquia

Use este prompt antes de pedir conteudo. Ele testa se o NotebookLM entendeu o papel dos arquivos.

```text
Antes de produzir conteudo, confirme como voce entendeu a hierarquia das fontes deste projeto.

Responda em quatro partes:
1. quais arquivos definem objetivo, escopo e estrutura da aula;
2. qual papel do arquivo `fluxo padrão/07_fontes-e-evidencias.md`;
3. qual papel das auditorias do Codex;
4. qual papel dos outputs brutos do OpenEvidence.

Depois liste 8 riscos de desvio que voce deve evitar ao construir a fonte mestre.
```

Salvar a resposta em:

`outputs/notebooklm-00-checagem-hierarquia.md`

## Prompt 2 - Blocos 1 e 2

```text
Construa uma sintese para a futura fonte mestre cobrindo apenas:
- Bloco 1: Por que controle de carga aparece dentro da sessao;
- Bloco 2: Vocabulario minimo: carga, intensidade e resposta.

Use a hierarquia definida no inicio do chat.

Formato:
1. ideias centrais;
2. conceitos essenciais;
3. afirmacoes seguras com fonte de origem;
4. cautelas;
5. linguagem operacional para trainees;
6. exemplos ou analogias que o professor pode usar oralmente;
7. o que nao deve entrar nesses blocos.

Nao escreva slides ainda. Nao escreva ebook ainda.
```

Salvar a resposta em:

`outputs/notebooklm-01-fonte-blocos-1-2.md`

## Prompt 3 - Blocos 3 e 4

```text
Construa uma sintese para a futura fonte mestre cobrindo apenas:
- Bloco 3: Leitura inicial da sessao;
- Bloco 4: Intensidade na pratica: RPE/RIR e qualidade tecnica.

Use a hierarquia definida no inicio do chat.

Deve ficar claro que RPE/RIR sao ferramentas de calibracao e que iniciantes podem estimar mal esforco e repeticoes em reserva.

Formato:
1. ideias centrais;
2. conceitos essenciais;
3. afirmacoes seguras com fonte de origem;
4. cautelas;
5. como cruzar relato do aluno e qualidade tecnica;
6. linguagem operacional para trainees;
7. o que nao deve entrar nesses blocos.

Nao escreva slides ainda. Nao escreva ebook ainda.
```

Salvar a resposta em:

`outputs/notebooklm-02-fonte-blocos-3-4.md`

## Prompt 4 - Bloco 5

```text
Construa uma sintese para a futura fonte mestre cobrindo apenas:
- Bloco 5: Da leitura ao ajuste: manter, progredir, reduzir ou modificar.

Use a hierarquia definida no inicio do chat.

Foco: transformar leitura do aluno em decisao aguda durante a sessao. A ideia central deve ser a menor mudanca suficiente.

Formato:
1. ideias centrais;
2. variaveis manipulaveis na sessao;
3. matriz "leitura dominante -> ajuste possivel";
4. afirmacoes seguras com fonte de origem;
5. cautelas;
6. frases operacionais para trainees;
7. o que nao deve entrar nesse bloco.

Nao escreva slides ainda. Nao escreva ebook ainda.
```

Salvar a resposta em:

`outputs/notebooklm-03-fonte-bloco-5.md`

## Prompt 5 - Bloco 6

```text
Construa uma sintese para a futura fonte mestre cobrindo apenas:
- Bloco 6: Sinais de fadiga durante a execucao.

Use a hierarquia definida no inicio do chat.

Este bloco exige cautela metodologica. Diferencie claramente:
1. sinais com evidencia direta ou instrumental;
2. sinais com evidencia indireta plausivel;
3. sinais uteis pedagogicamente, mas sem validacao direta;
4. sinais que nao devem virar afirmacao forte.

Inclua linguagem operacional para ensinar o trainee a olhar a execucao, mas sem afirmar que observacao visual sem equipamento mede fadiga.

Formato:
1. ideias centrais;
2. classificacao dos sinais por nivel de confianca;
3. perguntas para guiar o olhar do trainee;
4. afirmacoes seguras com fonte de origem;
5. cautelas;
6. frases recomendadas;
7. frases a evitar;
8. o que nao deve entrar nesse bloco.

Nao escreva slides ainda. Nao escreva ebook ainda.
```

Salvar a resposta em:

`outputs/notebooklm-04-fonte-bloco-6.md`

## Prompt 6 - Blocos 7 e 8

```text
Construa uma sintese para a futura fonte mestre cobrindo apenas:
- Bloco 7: Postura profissional: comunicar o ajuste sem parecer perdido;
- Bloco 8: Consolidacao final.

Use a hierarquia definida no inicio do chat.

O foco aqui e transformar decisao tecnica em comunicacao profissional simples. Nao invente base cientifica onde houver apenas diretriz didatica.

Formato:
1. ideias centrais;
2. estrutura de comunicacao do ajuste;
3. frases modelo;
4. frases a evitar;
5. checklist final da logica da aula;
6. cautelas;
7. o que nao deve entrar nesses blocos.

Nao escreva slides ainda. Nao escreva ebook ainda.
```

Salvar a resposta em:

`outputs/notebooklm-05-fonte-blocos-7-8.md`

## Prompt 7 - Revisao transversal

Use depois dos prompts por bloco.

```text
Agora revise transversalmente as sinteses produzidas para os blocos 1 a 8.

Procure:
1. redundancias;
2. contradicoes;
3. excesso de tecnicismo;
4. afirmacoes fortes demais;
5. trechos que puxam para performance, hipertrofia avancada, reabilitacao, periodizacao ou registro de treino;
6. cautelas que precisam aparecer na fonte mestre;
7. lacunas que devem ser mantidas como lacunas, nao resolvidas artificialmente.

Entregue uma lista de correcoes antes de montar a fonte mestre.
```

Salvar a resposta em:

`outputs/notebooklm-06-revisao-transversal.md`

## Prompt 8 - Fonte mestre preliminar

Use apenas depois de gerar e revisar as sinteses por bloco.

```text
Com base nas sinteses por bloco e na revisao transversal, monte uma fonte mestre preliminar para este projeto.

Essa fonte mestre deve orientar a criacao futura de slides e ebook, mas ainda nao deve ser escrita como slides nem como ebook.

Estrutura obrigatoria:
1. objetivo do material;
2. publico e escopo;
3. principios centrais;
4. conceitos essenciais;
5. sintese por bloco da aula;
6. matriz de decisao para ajuste agudo;
7. sinais de fadiga por nivel de confianca;
8. frases operacionais;
9. checklists potenciais;
10. cautelas metodologicas;
11. o que deve ficar fora do material;
12. referencias rastreaveis por tema.

Regras:
- linguagem clara, operacional e intermediaria;
- sem excesso academico;
- sem criar nomes de metodo novos;
- sem registro de treino como etapa central;
- sem transformar sinais visuais em medida objetiva;
- sem tratar falha muscular como meta padrao;
- preserve fontes/rastreabilidade sempre que possivel.
```

Salvar a resposta em:

`outputs/notebooklm-07-fonte-mestre-preliminar.md`

## Prompt 9 - Autocritica da fonte mestre

Use depois que o NotebookLM gerar a fonte mestre preliminar.

```text
Faça uma autocritica da fonte mestre preliminar que voce acabou de criar.

Avalie:
1. ela respeita o roteiro mestre?
2. ela respeita as auditorias do Codex?
3. ela usa os outputs brutos sem deixar que eles dominem o escopo?
4. ela ficou tecnica demais para trainees?
5. ela deixou de fora alguma cautela importante?
6. ela incluiu algo fora do escopo?
7. ela tem afirmacoes que precisam ser rebaixadas para cautela?
8. ela tem trechos redundantes ou longos demais?

Na autocritica, considere tambem estes pontos obrigatorios:
1. Corrija a abertura: a fonte mestre ainda e preliminar, nao final.
2. Remova faixas fixas de RIR como regra geral. Use "acima do alvo planejado" e "proximo do alvo planejado".
3. Suavize frases absolutas sobre tecnica e resposta do aluno. A qualidade da execucao deve ter peso importante na decisao, especialmente em conflito com o relato, mas evite "sempre" e "criterio final".
4. Preserve sinais visuais como pistas operacionais, nunca como criterios diagnosticos ou medicoes.
5. Evite frases automaticas como "vamos parar aqui" para toda queda de velocidade.
6. Troque perguntas sobre dor por linguagem de desconforto incomum ou mudanca relevante no estado do aluno, sem puxar para triagem clinica.
7. Refaca a secao de referencias com nomes completos, ano, tema e origem, ou indique "ver output bruto correspondente" quando nao houver referencia completa.
8. Garanta que registro de treino, periodizacao, performance, reabilitacao e hipertrofia avancada continuem fora do escopo.

Entregue:
- diagnostico geral;
- lista de correcoes;
- versao revisada apenas dos trechos problematicos.
```

Salvar a resposta em:

`outputs/notebooklm-08-autocritica-fonte-mestre.md`

## Prompt 10 - Fonte mestre revisada completa

Use depois que a autocritica da fonte mestre for aprovada pelo Codex.

```text
Com base na fonte mestre preliminar e na autocritica aprovada, gere uma fonte mestre revisada completa para este projeto.

Voce deve aplicar as correcoes da autocritica diretamente no documento, nao entregar apenas trechos revisados.

Estrutura obrigatoria:
1. objetivo do material;
2. publico e escopo;
3. principios centrais;
4. conceitos essenciais;
5. sintese por bloco da aula;
6. matriz de decisao para ajuste agudo;
7. sinais de fadiga como pistas operacionais;
8. frases operacionais;
9. checklists potenciais;
10. cautelas metodologicas;
11. o que deve ficar fora do material;
12. referencias rastreaveis por tema.

Regras obrigatorias:
- trate esta versao como "fonte mestre revisada para auditoria", nao como versao final publicada;
- mantenha linguagem clara, operacional e intermediaria;
- nao crie nome formal de metodo;
- nao escreva slides nem ebook ainda;
- nao use faixas fixas de RIR como regra geral;
- use "acima do alvo planejado", "abaixo do alvo planejado" e "proximo do alvo planejado";
- sinais visuais devem ser apresentados como pistas operacionais, nunca como medicoes objetivas, provas de fadiga ou diagnosticos;
- nao transforme queda de velocidade em comando automatico de parar;
- preserve a matriz com possibilidades de manter, progredir, reduzir, recuperar, simplificar e modificar, mas sem parecer algoritmo rigido;
- evite linguagem clinica: use "desconforto incomum" ou "mudanca relevante no estado", sem transformar o personal em avaliador clinico;
- mantenha registro de treino, periodizacao, performance, reabilitacao e hipertrofia avancada fora do escopo;
- use referencias completas quando possivel; quando nao for possivel, indique o output bruto correspondente.

Entregue em formato de documento unico, pronto para ser auditado pelo Codex.
```

Salvar a resposta em:

`outputs/notebooklm-09-fonte-mestre-revisada.md`

## Depois do NotebookLM

Traga ao Codex:

- `outputs/notebooklm-07-fonte-mestre-preliminar.md`
- `outputs/notebooklm-08-autocritica-fonte-mestre.md`
- `outputs/notebooklm-09-fonte-mestre-revisada.md`

O Codex deve auditar os arquivos e decidir se a fonte mestre revisada pode virar arquivo validado do projeto.
