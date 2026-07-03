---
type: prompt-pack
title: Prompts NotebookLM Slides Producao
created: 2026-06-29
updated: 2026-06-30
tags:
  - notebooklm
  - slides
  - prompts
  - controle-carga
related:
  - '[[Diretriz Apresentacao Slides]]'
  - '[[Fonte Mestre Validada]]'
  - '[[Tema Visual XSTEAM]]'
---

# Prompts NotebookLM - slides

Status: prompt pack ativo para criar a apresentacao usando **Conversa** e **Studio** do NotebookLM sem misturar as funcoes.

## Entendimento correto do NotebookLM

O NotebookLM tem dois usos diferentes neste fluxo:

1. **Conversa:** campo de chat. Tem memoria dentro da conversa, permite pedir revisoes, ajustes, auditorias e continuidade. Use para pensar, estruturar, revisar e corrigir.
2. **Studio:** campo de criacao de artefato, como "Apresentacao". E um comando unico para gerar um produto. Nao conte com interacao posterior dentro daquele artefato. O prompt precisa sair completo.

Portanto:

- prompts da **Conversa** podem ser sequenciais e usar memoria do chat;
- prompts do **Studio** precisam ser autocontidos;
- quando a apresentacao for gerada em 3 partes no Studio, cada prompt deve especificar exatamente quais slides do roteiro deve produzir;
- as instrucoes de continuidade visual devem orientar o Studio, mas nao devem aparecer como conteudo de slide;
- a consistencia visual nao deve depender da memoria do NotebookLM.

## Fontes que devem estar no notebook

Fontes principais:

- `diretrizes/fontes-notebooklm-produtos.md`
- `fluxo padrão/01_briefing-inicial.md`
- `fluxo padrão/03_arquitetura-logica-rascunho.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `fluxo padrão/08_fonte-mestre-validada.md`
- `diretrizes/criterios-linguagem-densidade-operacional.md`
- `diretrizes/tema-visual-xsteam.md`
- `diretrizes/diretriz-apresentacao-slides.md`
- `diretrizes/roteiro-apresentacao.md`

Fontes secundarias, se estiverem no notebook:

- `fluxo padrão/07_fontes-e-evidencias.md`
- `outputs/dotflow-01-fadiga-execucao-coletar-base.md`
- `outputs/dotflow-02-rpe-rir-tecnica.md`
- `outputs/dotflow-03-falha-proximidade-fadiga.md`
- `outputs/dotflow-04-ajustes-agudos.md`
- `outputs/dotflow-05-lacunas-fadiga.md`

Nao usar outputs intermediarios antigos do NotebookLM como fonte para a apresentacao.

## Hierarquia obrigatoria para gerar slides

Use esta hierarquia dentro de qualquer prompt de Conversa ou Studio:

1. `diretrizes/roteiro-apresentacao.md` define a quantidade de slides, a numeracao, a ordem, a funcao didatica de cada slide, o titulo, o conteudo em tela, o elemento visual principal e a organizacao visual.
2. `fluxo padrão/01_briefing-inicial.md`, `fluxo padrão/03_arquitetura-logica-rascunho.md`, `fluxo padrão/04_roteiro-mestre-rascunho.md` e `fluxo padrão/08_fonte-mestre-validada.md` definem publico, escopo, progressao didatica e conteudo tecnico validado.
3. `diretrizes/criterios-linguagem-densidade-operacional.md`, `diretrizes/tema-visual-xsteam.md` e `diretrizes/diretriz-apresentacao-slides.md` definem linguagem, densidade, identidade visual, formato e criterios de qualidade dos slides.
4. `diretrizes/fontes-notebooklm-produtos.md` define quais fontes podem ou nao orientar o produto.
5. `fluxo padrão/07_fontes-e-evidencias.md` e os arquivos `outputs/dotflow-*` sao fontes secundarias de apoio teorico e rastreabilidade. Eles nao devem mudar roteiro, escopo, ordem, tom ou design.

Se houver conflito entre fontes, seguir primeiro `diretrizes/roteiro-apresentacao.md`; depois os arquivos validados do fluxo padrao; depois as diretrizes; por ultimo as fontes secundarias.

## Configuracao recomendada no Studio

Ao criar o artefato no Studio:

- Tipo: **Apresentacao**.
- Formato: **Slides do apresentador**.
- Idioma: **Portuguese / Portugues**, se disponivel.
- Duracao: **Padrao**.

Motivo: queremos slides limpos, visuais e com notas para apoiar a fala, nao uma apostila detalhada em formato de slide.

## Design lock XSTEAM

Cole este bloco dentro de **todo prompt de Studio**. Ele e a trava principal para evitar que a Parte 2 ou Parte 3 mudem o tema visual.

```text
DESIGN LOCK XSTEAM

Mantenha a identidade visual da XSTEAM durante todo o artefato.

Paleta fixa:
- preto/grafite dominante: #000000, #0B0B0B, #151515;
- branco para texto principal: #FFFFFF;
- cinza claro/cinza medio para texto secundario;
- verde-limao XSTEAM para acentos: #DFFF2F ou #E3FF28;
- superficies claras pontuais: #F2F3F6.

Estilo:
- visual de capacitacao interna profissional de academia;
- alto contraste;
- energia, precisao e movimento;
- formas angulares, diagonais, cortes, faixas e marcadores inspirados na marca;
- fotos reais ou realistas de treino, academia, personal em atendimento e interacao professor-aluno;
- nada de tema academico generico, corporativo azul, minimalista branco, esportivo de performance ou estetica clinica.

Tipografia e composicao:
- titulos curtos, fortes e com peso visual;
- etiquetas curtas em caixa alta quando fizer sentido;
- pouco texto em tela;
- notas de fala separadas do texto visivel;
- nada de paragrafos longos nos slides;
- todo slide precisa ter elemento visual relevante ocupando cerca de 50% da area percebida.

Componentes recorrentes:
- slide escuro com foto ou geometria forte;
- matriz operacional de 2 colunas;
- fluxo de decisao com poucos blocos;
- cards de decisao sem card dentro de card;
- imagem anotada para sinais observaveis de fadiga;
- checklist curto de consolidacao;
- faixa ou marcador verde-limao para enfase.

Regra de consistencia:
- nao mudar paleta entre partes;
- nao mudar estilo de titulo entre partes;
- nao mudar estilo de cards, fluxos e matrizes entre partes;
- se a apresentacao for gerada em partes, cada parte deve parecer continuacao direta da anterior.
```

## Contrato de conteudo dos slides

Use este bloco nos prompts da Conversa e do Studio.

```text
CONTRATO DE CONTEUDO DOS SLIDES

Tema: controle de carga no treino de forca.
Publico: trainees/estagiarios de Educacao Fisica em formacao para atuarem como personal trainer com publico geral.
Foco: ajuste agudo da carga/intensidade durante a sessao.
Duracao da aula: 60 a 90 minutos.

Cada slide deve ter:
- funcao didatica clara;
- titulo curto;
- texto visivel enxuto;
- elemento visual principal;
- organizacao visual coerente;
- notas de fala ou apoio ao apresentador;
- cautela quando houver risco de desvio;
- conexao com as fontes do notebook.

Evitar:
- registro de treino como etapa central;
- performance esportiva;
- reabilitacao clinica;
- periodizacao complexa;
- prescricao por percentual de 1RM;
- sinais visuais tratados como medidas objetivas;
- RPE/RIR como comandos automaticos;
- falha muscular como meta padrao;
- slides puramente textuais;
- excesso de fisiologia ou linguagem academica.
```

## Fluxo recomendado

1. Use a **Conversa** para gerar o mapa/roteiro e auditar o conteudo.
2. Traga o output da Conversa para o Codex, se quiser auditoria antes de gerar artefato.
3. Use o **Studio** para gerar a apresentacao.
4. Se o Studio nao conseguir entregar tudo bem em uma geracao, use os prompts de Studio por partes.
5. Exporte o artefato ou copie o resultado para `outputs/produtos-slides/`.
6. Traga a apresentacao ao Codex para auditoria de alinhamento e continuidade visual.

# Prompts para a Conversa

Use estes prompts no campo **Conversa** do NotebookLM.

Estes prompts correspondem a versao usada para construir o roteiro que agora foi consolidado em `diretrizes/roteiro-apresentacao.md`.

## Chat 0 - Confirmacao de hierarquia

Onde usar: Conversa do NotebookLM.

Objetivo: alinhar o comportamento do NotebookLM antes de pedir o roteiro.

Prompt pronto:

```text
Voce sera meu assistente de producao da apresentacao em slides da aula "controle de carga no treino de forca".

Antes de produzir qualquer slide, confirme que entendeu esta hierarquia:

1. `diretrizes/roteiro-apresentacao.md` define quantidade, numeracao, ordem, funcao didatica, titulo, conteudo em tela, elemento visual principal e organizacao visual de cada slide.
2. Briefing, arquitetura, roteiro mestre e fonte mestre validada definem publico, escopo, progressao e conteudo tecnico.
3. As diretrizes de linguagem, tema visual XSTEAM e diretriz de apresentacao definem formato, densidade, visual e padrao de organizacao.
4. Fontes secundarias servem apenas para apoio teorico e rastreabilidade.

Regras obrigatorias:
- O foco e ajuste agudo da carga/intensidade dentro da sessao.
- O publico e trainee/estagiario de Educacao Fisica em formacao para atuar como personal trainer com publico geral.
- Nao puxe para performance esportiva, reabilitacao clinica, periodizacao complexa ou registro de treino.
- Nao crie a apresentacao inteira em uma unica resposta.
- Nao defina conteudo por fora das fontes.
- Cada slide futuro deve conter: numero, bloco, funcao, objetivo didatico, titulo, frase-guia, texto em tela, elemento visual principal, organizacao visual, nota de fala, cautela e ancora de fonte.
- Todo slide precisa ter elemento visual relevante ocupando cerca de 50% da area percebida.
- Mantenha identidade XSTEAM: preto/grafite, verde-limao como acento, alto contraste, formas angulares, fotos reais/realistas de treino e linguagem profissional.

Responda apenas:
1. confirmacao da hierarquia;
2. 8 riscos de desvio que voce vai evitar;
3. padrao visual e estrutural que voce vai manter em todas as proximas respostas.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-chat-00-confirmacao-hierarquia.md`.

## Chat 1 - Mapa geral da apresentacao

Onde usar: Conversa do NotebookLM.

Objetivo: criar a arquitetura da apresentacao, sem escrever todos os slides ainda.

Prompt pronto:

```text
Crie o mapa geral da apresentacao em slides, sem escrever o conteudo final dos slides ainda.

Use as fontes principais e a diretriz de apresentacao. Voce deve decidir a melhor distribuicao de slides, respeitando:
- aula de 60 a 90 minutos;
- roteiro ativo de 27 slides;
- 8 blocos do roteiro mestre;
- baixa densidade textual;
- pelo menos um elemento visual relevante por slide;
- producao futura em 3 partes: slides 1-9, 10-18 e 19-27.

Nao quero que voce escreva a apresentacao final agora.

Entregue:
1. quantidade total sugerida de slides;
2. divisao por blocos da aula;
3. objetivo didatico de cada bloco;
4. tipos de slide recomendados por bloco, sem fechar o conteudo exato;
5. regras de continuidade visual para as proximas rodadas;
6. proposta de divisao em 3 lotes de producao: Parte 1 slides 1-9, Parte 2 slides 10-18 e Parte 3 slides 19-27.

Formato:
- Use tabela.
- Nao coloque paragrafos longos.
- Nao invente exemplos especificos.
- Preserve espaco para exemplos orais do professor.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-chat-01-mapa-geral.md`.

## Chat 2 - Roteiro slide a slide do Lote 1

Onde usar: Conversa do NotebookLM.

Objetivo: produzir o roteiro slide a slide do primeiro lote, nao a apresentacao final.

Prompt pronto:

```text
Agora crie o roteiro slide a slide do Lote 1 da apresentacao.

Use o mapa geral aprovado nesta conversa. O Lote 1 deve cobrir os primeiros slides da apresentacao, normalmente abertura e blocos iniciais, mantendo a numeracao absoluta.

Importante:
- Voce decide o conteudo especifico de cada slide com base nas fontes.
- Nao copie textos longos da fonte mestre.
- Nao gere ainda a apresentacao final.
- Mantenha a estrutura visual e editorial combinada no mapa geral.
- Cada slide deve ter um elemento visual relevante, ocupando cerca de 50% da area percebida.

Para cada slide, preencha exatamente estes campos:

Slide:
Bloco:
Funcao:
Objetivo didatico:
Titulo:
Frase-guia:
Texto em tela:
Elemento visual principal:
Organizacao visual:
Nota de fala:
Cautela:
Ancora de fonte:

Regras:
- Texto em tela curto.
- Nota de fala pode ser um pouco mais explicativa.
- A cautela deve aparecer quando houver risco de tecnicismo, automatizacao, performance, saude clinica ou registro de treino.
- Use linguagem de capacitacao profissional para trainees.
- Nao crie slides puramente textuais.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-chat-02-roteiro-lote-1.md`.

## Chat 3 - Roteiro slide a slide do Lote 2

Onde usar: Conversa do NotebookLM.

Objetivo: produzir o roteiro do segundo lote sem mudar o estilo do primeiro.

Prompt pronto:

```text
Agora crie o roteiro slide a slide do Lote 2 da apresentacao.

Antes de escrever os slides, releia o Lote 1 produzido nesta conversa e preserve:
- numeracao absoluta;
- estilo dos titulos;
- densidade textual;
- tipo de notas de fala;
- padrao de elementos visuais;
- identidade XSTEAM;
- ritmo entre conceito, comparacao, fluxo, matriz e consolidacao.

O Lote 2 deve continuar a apresentacao sem repetir o que ja foi tratado no Lote 1. Use o mapa geral aprovado para decidir quais blocos entram neste lote.

Para cada slide, preencha exatamente estes campos:

Slide:
Bloco:
Funcao:
Objetivo didatico:
Titulo:
Frase-guia:
Texto em tela:
Elemento visual principal:
Organizacao visual:
Nota de fala:
Cautela:
Ancora de fonte:

Inclua no inicio da resposta:
1. slides cobertos neste lote;
2. blocos cobertos neste lote;
3. padrao visual que esta sendo preservado do Lote 1;
4. ideias que nao devem ser repetidas.

Regras:
- Nao mude a identidade visual.
- Nao aumente a densidade textual.
- Nao invente exemplos especificos.
- Nao transforme matriz em algoritmo automatico.
- Nao trate sinais visuais como medidas objetivas.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-chat-03-roteiro-lote-2.md`.

## Chat 4 - Roteiro slide a slide do Lote 3

Onde usar: Conversa do NotebookLM.

Objetivo: produzir o roteiro do terceiro lote e fechar a apresentacao.

Prompt pronto:

```text
Agora crie o roteiro slide a slide do Lote 3 da apresentacao.

Antes de escrever os slides, releia os Lotes 1 e 2 produzidos nesta conversa e preserve:
- numeracao absoluta;
- estilo dos titulos;
- densidade textual;
- tipo de notas de fala;
- padrao de elementos visuais;
- identidade XSTEAM;
- continuidade da progressao didatica.

O Lote 3 deve completar os blocos restantes e encerrar a apresentacao com consolidacao operacional.

Para cada slide, preencha exatamente estes campos:

Slide:
Bloco:
Funcao:
Objetivo didatico:
Titulo:
Frase-guia:
Texto em tela:
Elemento visual principal:
Organizacao visual:
Nota de fala:
Cautela:
Ancora de fonte:

Inclua no inicio da resposta:
1. slides cobertos neste lote;
2. blocos cobertos neste lote;
3. padrao visual preservado dos lotes anteriores;
4. como este lote fecha a pergunta-guia da aula.

Regras:
- Feche a apresentacao sem criar uma nova tese.
- Reforce a pergunta-guia e a menor mudanca suficiente.
- Mantenha postura profissional e foco operacional.
- Nao inserir registro de treino como etapa.
- Nao puxar para periodizacao, performance ou reabilitacao.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-chat-04-roteiro-lote-3.md`.

## Chat 5 - Revisao transversal do roteiro

Onde usar: Conversa do NotebookLM.

Objetivo: revisar os tres lotes de roteiro antes de gerar o artefato no Studio.

Prompt pronto:

```text
Revise transversalmente os tres lotes de roteiro slide a slide que voce produziu nesta conversa.

Compare contra as fontes principais e as diretrizes.

Avalie:
1. ha progressao clara entre os 8 blocos?
2. ha repeticoes desnecessarias?
3. algum bloco ficou raso demais?
4. algum bloco ficou denso demais?
5. todos os slides tem elemento visual relevante?
6. a identidade XSTEAM esta consistente?
7. a linguagem esta operacional para trainees?
8. houve desvio para performance, saude clinica, periodizacao, registro de treino ou revisao academica?
9. sinais visuais foram tratados como pistas, nao como medidas?
10. RPE/RIR foram tratados como ferramentas, nao comandos automaticos?

Entregue:
- diagnostico geral;
- ajustes obrigatorios por slide;
- slides que devem ser removidos, unidos ou divididos;
- slides que precisam de visual mais claro;
- versao corrigida apenas dos slides que precisam de correcao.

Nao reescreva toda a apresentacao se apenas alguns slides precisarem de ajuste.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-chat-05-revisao-roteiro.md`.

## Chat 6 - Auditoria depois do Studio

Onde usar: Conversa do NotebookLM.

Objetivo: avaliar a apresentacao gerada no Studio.

Prompt pronto:

```text
Vou colar abaixo a apresentacao gerada pelo Studio. Audite contra as fontes e diretrizes do notebook.

APRESENTACAO GERADA:
[COLE AQUI O TEXTO EXPORTADO/COPIADO DA APRESENTACAO]

Avalie:
1. continuidade de conteudo;
2. continuidade visual;
3. alinhamento com a fonte mestre;
4. densidade textual;
5. qualidade dos elementos visuais;
6. utilidade das notas de fala;
7. desvios de escopo;
8. slides que precisam ser reescritos;
9. se a apresentacao parece XSTEAM ou generica.

Entregue:
- aprovado / aprovado com ajustes / precisa refazer;
- problemas por slide;
- correcoes pontuais;
- prompt de correcao para Studio, se necessario.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-chat-06-auditoria-studio.md`.

# Prompts para o Studio

Use estes prompts no campo **Descreva a apresentacao de slides que voce quer criar** dentro do Studio.

## Studio A - Apresentacao unica

Use quando quiser tentar gerar toda a apresentacao em um unico artefato.

Configuracao recomendada:

- Formato: **Slides do apresentador**.
- Idioma: **Portuguese / Portugues**.
- Duracao: **Padrao**.

Prompt pronto:

```text
Crie uma apresentacao de slides em portugues sobre "Controle de carga no treino de forca: ajuste agudo da intensidade na sessao".

Use as fontes deste notebook. Siga esta hierarquia:
1. `diretrizes/roteiro-apresentacao.md` define exatamente os 27 slides, sua numeracao, ordem, funcao didatica, titulo, conteudo em tela, elemento visual principal e organizacao visual;
2. briefing, arquitetura, roteiro mestre e fonte mestre validada definem publico, escopo, progressao e conteudo tecnico;
3. criterios de linguagem, tema visual XSTEAM e diretriz de apresentacao definem formato, densidade, visual e estilo;
4. fontes secundarias servem apenas como apoio teorico e nao podem alterar roteiro, ordem, tom ou design.

Publico:
Trainees/estagiarios de Educacao Fisica em formacao interna para atuarem como personal trainer com publico geral.

Objetivo:
Ajudar o trainee a observar o aluno durante a sessao, interpretar esforço/execucao/contexto e decidir ajustes agudos de carga, repeticoes, amplitude, ritmo, intervalo ou variacao do exercicio com postura profissional.

Duracao:
Aula de 60 a 90 minutos. Gere exatamente os 27 slides previstos no roteiro ativo `diretrizes/roteiro-apresentacao.md`.

CONTRATO DE CONTEUDO DOS SLIDES
- foco em ajuste agudo dentro da sessao;
- manter os 8 blocos do roteiro mestre;
- seguir `diretrizes/roteiro-apresentacao.md` como roteiro slide a slide;
- nao criar slides extras alem dos 27 slides do roteiro;
- baixo texto em tela;
- notas de fala para apoiar o apresentador;
- todo slide precisa ter elemento visual relevante;
- exemplos especificos podem ficar para a fala oral do professor;
- nao inserir registro de treino como etapa central;
- nao puxar para performance esportiva, reabilitacao clinica ou periodizacao complexa.

DESIGN LOCK XSTEAM
- fundo preto/grafite dominante;
- verde-limao XSTEAM como acento;
- branco/cinza para texto;
- alto contraste;
- formas angulares, diagonais, faixas e marcadores;
- fotos reais ou realistas de treino, academia e personal em atendimento;
- titulos curtos, fortes e profissionais;
- matrizes, fluxos, cards e checklists com estilo consistente;
- nao usar tema azul corporativo, minimalista branco, academico generico, clinico ou de performance esportiva.

Estrutura visual:
- cada slide deve ter aproximadamente 50% de area visual;
- alternar fotos, matrizes, fluxos, imagens anotadas, cards e checklists;
- evitar slides puramente textuais;
- evitar paragrafos longos;
- nao usar card dentro de card.

Slides obrigatorios por funcao, sem engessar titulos:
- abertura com promessa operacional;
- problema da sessao real vs ficha planejada;
- conceitos essenciais de carga externa, carga interna e intensidade relativa;
- leitura inicial do aluno;
- uso operacional de RPE/RIR;
- tecnica observada como criterio;
- matriz de leitura para ajuste;
- sinais observaveis de fadiga;
- comunicacao profissional do ajuste;
- consolidacao final com pergunta-guia e checklist mental.

Pergunta-guia da apresentacao:
"O que esta acontecendo agora e qual e a menor mudanca suficiente para adequar a intensidade?"

Gere slides de apresentador: limpos, visuais, com pontos principais e notas de fala.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-studio-a-apresentacao-unica.md`.

## Studio B1 - Apresentacao em partes: Parte 1

Use quando o Studio estiver gerando melhor em blocos menores.

Configuracao recomendada:

- Formato: **Slides do apresentador**.
- Idioma: **Portuguese / Portugues**.
- Duracao: **Padrao**.

Prompt pronto:

```text
Crie a PARTE 1 de uma apresentacao de slides em portugues sobre "Controle de carga no treino de forca: ajuste agudo da intensidade na sessao".

Esta e a Parte 1 de 3. Gere apenas os slides 1 a 9 do roteiro ativo `diretrizes/roteiro-apresentacao.md`.

IMPORTANTE:
- Esta parte sera unida manualmente com as Partes 2 e 3 depois.
- Nao crie slide extra de continuidade, abertura secundaria, encerramento parcial ou resumo para a proxima parte.
- As instrucoes de continuidade visual abaixo sao apenas orientacoes de producao, nao conteudo de slide.
- Mantenha numeracao absoluta dos slides: 1/27 ate 9/27.

Slides obrigatorios da Parte 1:
- Slide 1: Controle de carga acontece no atendimento.
- Slide 2: O aluno planejado nem sempre chega igual.
- Slide 3: Ajuste nao e improviso.
- Slide 4: Carga nao e so peso.
- Slide 5: O corpo responde a proposta.
- Slide 6: Prescrito x acontecendo.
- Slide 7: A decisao comeca antes da serie efetiva.
- Slide 8: Pergunte sem virar interrogatorio.
- Slide 9: Aquecimento como validacao.

Quantidade:
Gere exatamente 9 slides.

Use as fontes deste notebook seguindo a hierarquia:
1. `diretrizes/roteiro-apresentacao.md` define exatamente os slides 1 a 9 desta parte, sua numeracao, ordem, funcao didatica, titulo, conteudo em tela, elemento visual principal e organizacao visual;
2. briefing, arquitetura, roteiro mestre e fonte mestre validada definem publico, escopo, progressao e conteudo tecnico;
3. criterios de linguagem, tema visual XSTEAM e diretriz de apresentacao definem formato, densidade, visual e estilo;
4. fontes secundarias servem apenas como apoio teorico e nao podem alterar roteiro, ordem, tom ou design.

Publico:
Trainees/estagiarios de Educacao Fisica em formacao interna para atuarem como personal trainer com publico geral.

Objetivo desta parte:
Fazer o trainee entender por que o ajuste de carga acontece dentro da sessao e criar vocabulário minimo para pensar carga/intensidade como resposta do aluno, nao apenas peso usado.

DESIGN LOCK XSTEAM
- fundo preto/grafite dominante;
- verde-limao XSTEAM como acento;
- branco/cinza para texto;
- alto contraste;
- formas angulares, diagonais, faixas e marcadores;
- fotos reais ou realistas de treino, academia e personal em atendimento;
- titulos curtos, fortes e profissionais;
- matrizes, fluxos, cards e checklists com estilo consistente;
- nada de tema azul corporativo, minimalista branco, academico generico, clinico ou de performance esportiva.

Regras de slide:
- formato de slides do apresentador;
- pouco texto em tela;
- notas de fala separadas;
- todo slide com elemento visual relevante ocupando cerca de 50% da area;
- nao usar paragrafos longos;
- nao transformar em apostila;
- nao inventar casos especificos.
- nao incluir slide de continuidade visual;
- nao incluir instrucoes de design como conteudo dos slides.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-studio-b1-parte-1.md`.

## Studio B2 - Apresentacao em partes: Parte 2

Use depois de gerar a Parte 1. Este prompt ja contem a continuidade necessaria; nao depende de memoria do Studio.

Configuracao recomendada:

- Formato: **Slides do apresentador**.
- Idioma: **Portuguese / Portugues**.
- Duracao: **Padrao**.

Prompt pronto:

```text
Crie a PARTE 2 de uma apresentacao de slides em portugues sobre "Controle de carga no treino de forca: ajuste agudo da intensidade na sessao".

Esta e a Parte 2 de 3. Gere apenas os slides 10 a 18 do roteiro ativo `diretrizes/roteiro-apresentacao.md`.

IMPORTANTE:
- Esta parte sera unida manualmente com as Partes 1 e 3 depois.
- Nao crie slide extra de abertura, recapitulacao, continuidade, transicao ou encerramento parcial.
- As instrucoes de continuidade visual abaixo sao apenas orientacoes de producao, nao conteudo de slide.
- Mantenha numeracao absoluta dos slides: 10/27 ate 18/27.

Continuidade obrigatoria da Parte 1:
- A Parte 1 terminou no aquecimento como validacao.
- A Parte 2 deve continuar com a ideia de que contexto e prontidao mudam a intensidade.
- Preserve o mesmo tema visual: XSTEAM, preto/grafite, verde-limao, alto contraste, formas angulares, fotos/anotacoes de treino, cards e matrizes consistentes.

Slides obrigatorios da Parte 2:
- Slide 10: Contexto muda a intensidade.
- Slide 11: RPE abre conversa.
- Slide 12: RIR aproxima da qualidade restante.
- Slide 13: Tecnica pode mudar a leitura.
- Slide 14: Leia por triangulacao.
- Slide 15: Da leitura para a acao.
- Slide 16: Quando manter.
- Slide 17: Quando progredir.
- Slide 18: Quando reduzir ou recuperar.

Quantidade:
Gere exatamente 9 slides.

Use as fontes deste notebook seguindo a hierarquia:
1. `diretrizes/roteiro-apresentacao.md` define exatamente os slides 10 a 18 desta parte, sua numeracao, ordem, funcao didatica, titulo, conteudo em tela, elemento visual principal e organizacao visual;
2. briefing, arquitetura, roteiro mestre e fonte mestre validada definem publico, escopo, progressao e conteudo tecnico;
3. criterios de linguagem, tema visual XSTEAM e diretriz de apresentacao definem formato, densidade, visual e estilo;
4. fontes secundarias servem apenas como apoio teorico e nao podem alterar roteiro, ordem, tom ou design.

Publico:
Trainees/estagiarios de Educacao Fisica em formacao interna para atuarem como personal trainer com publico geral.

Objetivo desta parte:
Ensinar o trainee a cruzar prontidao, relato de esforco e tecnica observada para decidir se a intensidade esta adequada ou precisa de ajuste.

DESIGN LOCK XSTEAM
Repita exatamente a identidade da Parte 1:
- fundo preto/grafite dominante;
- verde-limao XSTEAM como acento;
- branco/cinza para texto;
- alto contraste;
- formas angulares, diagonais, faixas e marcadores;
- fotos reais ou realistas de treino, academia e personal em atendimento;
- titulos curtos, fortes e profissionais;
- matrizes, fluxos, cards e checklists com o mesmo estilo da Parte 1;
- a Parte 2 deve parecer continuacao direta da Parte 1, nao uma nova apresentacao.

Regras de slide:
- formato de slides do apresentador;
- pouco texto em tela;
- notas de fala separadas;
- todo slide com elemento visual relevante ocupando cerca de 50% da area;
- nao repetir conteudo da Parte 1;
- nao mudar tema visual;
- nao tratar RPE/RIR como comando automatico;
- nao inserir registro de treino como etapa central;
- nao puxar para performance, reabilitacao ou periodizacao.
- nao incluir slide de continuidade visual;
- nao incluir instrucoes de design como conteudo dos slides.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-studio-b2-parte-2.md`.

## Studio B3 - Apresentacao em partes: Parte 3

Use depois de gerar a Parte 2. Este prompt ja contem a continuidade necessaria; nao depende de memoria do Studio.

Configuracao recomendada:

- Formato: **Slides do apresentador**.
- Idioma: **Portuguese / Portugues**.
- Duracao: **Padrao**.

Prompt pronto:

```text
Crie a PARTE 3 de uma apresentacao de slides em portugues sobre "Controle de carga no treino de forca: ajuste agudo da intensidade na sessao".

Esta e a Parte 3 de 3. Gere apenas os slides 19 a 27 do roteiro ativo `diretrizes/roteiro-apresentacao.md`.

IMPORTANTE:
- Esta parte sera unida manualmente com as Partes 1 e 2 depois.
- Nao crie slide extra de abertura, recapitulacao, continuidade, transicao ou encerramento alem do slide 27 previsto no roteiro.
- As instrucoes de continuidade visual abaixo sao apenas orientacoes de producao, nao conteudo de slide.
- Mantenha numeracao absoluta dos slides: 19/27 ate 27/27.

Continuidade obrigatoria da Parte 2:
- A Parte 2 terminou com decisoes de manter, progredir, reduzir ou recuperar.
- A Parte 3 deve continuar com modificar/simplificar, menor mudanca suficiente, sinais de fadiga, comunicacao profissional e fechamento.
- Preserve o mesmo tema visual: XSTEAM, preto/grafite, verde-limao, alto contraste, formas angulares, fotos/anotacoes de treino, cards, fluxos e matrizes consistentes.

Slides obrigatorios da Parte 3:
- Slide 19: Quando simplificar ou modificar.
- Slide 20: Menor mudanca suficiente.
- Slide 21: Sinais sao pistas.
- Slide 22: Pistas de execucao e contexto.
- Slide 23: Ajuste precisa de fala profissional.
- Slide 24: Frases que sustentam criterio.
- Slide 25: Frases que passam inseguranca.
- Slide 26: O raciocinio completo.
- Slide 27: Pergunta-guia final.

Quantidade:
Gere exatamente 9 slides.

Use as fontes deste notebook seguindo a hierarquia:
1. `diretrizes/roteiro-apresentacao.md` define exatamente os slides 19 a 27 desta parte, sua numeracao, ordem, funcao didatica, titulo, conteudo em tela, elemento visual principal e organizacao visual;
2. briefing, arquitetura, roteiro mestre e fonte mestre validada definem publico, escopo, progressao e conteudo tecnico;
3. criterios de linguagem, tema visual XSTEAM e diretriz de apresentacao definem formato, densidade, visual e estilo;
4. fontes secundarias servem apenas como apoio teorico e nao podem alterar roteiro, ordem, tom ou design.

Publico:
Trainees/estagiarios de Educacao Fisica em formacao interna para atuarem como personal trainer com publico geral.

Objetivo desta parte:
Ensinar o trainee a reconhecer sinais de fadiga como pistas operacionais, escolher a menor mudanca suficiente e comunicar o ajuste com seguranca profissional.

DESIGN LOCK XSTEAM
Repita exatamente a identidade das Partes 1 e 2:
- fundo preto/grafite dominante;
- verde-limao XSTEAM como acento;
- branco/cinza para texto;
- alto contraste;
- formas angulares, diagonais, faixas e marcadores;
- fotos reais ou realistas de treino, academia e personal em atendimento;
- titulos curtos, fortes e profissionais;
- matrizes, fluxos, cards e checklists com o mesmo estilo das partes anteriores;
- a Parte 3 deve parecer fechamento da mesma apresentacao, nao uma nova apresentacao.

Regras de slide:
- formato de slides do apresentador;
- pouco texto em tela;
- notas de fala separadas;
- todo slide com elemento visual relevante ocupando cerca de 50% da area;
- nao repetir conteudo das Partes 1 e 2;
- nao mudar tema visual;
- nao tratar sinais visuais como medidas objetivas;
- nao dizer que o olho mede percentual de perda de velocidade;
- nao inserir registro de treino como etapa central;
- nao puxar para performance, reabilitacao ou periodizacao.

Fechamento obrigatorio:
O slide 27 deve ser o slide final com a pergunta-guia:
"O que esta acontecendo agora e qual e a menor mudanca suficiente para adequar a intensidade?"

Inclua tambem um checklist mental final, curto e operacional no slide 26 ou nas notas do slide 27, sem criar slide extra.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-studio-b3-parte-3.md`.

## Observacao - ancoragem visual pela parte anterior oficial

Use esta observacao quando voce ja tiver uma parte anterior aprovada no NotebookLM, por exemplo `Parte_1_oficial` ou `Parte_2_oficial`, e quiser reforcar a continuidade estetica no final do prompt de Studio.

Importante:

- Este bloco deve ser colado **ao final** do prompt Studio da parte seguinte.
- Ele nao substitui o prompt B1, B2 ou B3.
- Ele nao deve virar conteudo de slide.
- Ele serve apenas como regra adicional de referencia visual, estrutural e narrativa.

### Complemento para a Parte 2

```text
REGRA INQUEBRAVEL DE REFERENCIA

- Use o arquivo "Parte_1_oficial" como referencia visual, estetica e estrutural para criar a Parte 2.
- Siga o modelo estetico e visual que foi iniciado nessa apresentacao.
- As apresentacoes serao juntadas posteriormente e nao pode parecer que existem dois temas na mesma apresentacao, como se cada parte tivesse sido feita por pessoas diferentes.
- Esta apresentacao que vamos criar sera a Parte 2 e sucede o documento de referencia "Parte_1_oficial".
- Garanta continuidade na logica visual, na logica de conteudo e na ordem do roteiro.
- Esta regra e instrucao de producao, nao conteudo de slide.
```

### Complemento para a Parte 3

```text
REGRA INQUEBRAVEL DE REFERENCIA

- Use os arquivos "Parte_1_oficial" e "Parte_2_oficial" como referencias visuais, esteticas e estruturais para criar a Parte 3.
- Siga o modelo estetico e visual que foi iniciado e mantido nas partes anteriores.
- As apresentacoes serao juntadas posteriormente e nao pode parecer que existem tres temas na mesma apresentacao, como se cada parte tivesse sido feita por pessoas diferentes.
- Esta apresentacao que vamos criar sera a Parte 3 e sucede os documentos de referencia "Parte_1_oficial" e "Parte_2_oficial".
- Garanta continuidade na logica visual, na logica de conteudo e na ordem do roteiro.
- Esta regra e instrucao de producao, nao conteudo de slide.
```

## Studio C - Correcao de uma parte gerada

Use quando uma parte saiu fora do padrao visual ou conceitual.

Prompt pronto:

```text
Corrija a apresentacao abaixo sem mudar seu escopo.

APRESENTACAO A CORRIGIR:
[COLE AQUI A PARTE GERADA]

Problema principal:
[DESCREVA O PROBLEMA: mudou tema visual, ficou densa, ficou academica, puxou para performance, faltou visual etc.]

DESIGN LOCK XSTEAM
- fundo preto/grafite dominante;
- verde-limao XSTEAM como acento;
- branco/cinza para texto;
- alto contraste;
- formas angulares, diagonais, faixas e marcadores;
- fotos reais ou realistas de treino, academia e personal em atendimento;
- titulos curtos, fortes e profissionais;
- matrizes, fluxos, cards e checklists com estilo consistente.

Corrija preservando:
- tema;
- publico;
- escopo;
- numeracao;
- progressao;
- conteudo validado nas fontes.

Corrija especialmente:
- continuidade visual;
- baixa densidade textual;
- elementos visuais por slide;
- notas de fala;
- cautelas contra performance, reabilitacao, periodizacao, registro de treino e sinais visuais como medidas.

Entregue a parte corrigida pronta para substituir a anterior.
```

Salvar resultado em: `outputs/produtos-slides/notebooklm-studio-c-correcao.md`.
