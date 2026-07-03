---
type: analysis
title: Auditoria Slides Rascunho 01
created: 2026-06-30
tags:
  - slides
  - auditoria
  - controle-carga
related:
  - '[[Roteiro Apresentacao Controle de Carga]]'
  - '[[Fonte Mestre Validada]]'
---

# Auditoria Slides Rascunho 01

Status: primeira auditoria do rascunho de slides.

Arquivos auditados:

- `slides/roteiro-apresentacao.md`
- `slides/controle-carga-slides.html`
- `fluxo padrão/08_fonte-mestre-validada.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `diretrizes/diretriz-apresentacao-slides.md`
- `diretrizes/criterios-linguagem-densidade-operacional.md`

Modo de fonte: roteiro e deck locais, com status de rascunho local aguardando revisao humana/NotebookLM. A pasta `outputs/produtos-slides/` ainda nao contem produto de slides consolidado alem de `README.md`.

## Decisao da auditoria

**Aprovado com ajustes pequenos.**

O material ja sustenta uma aula interna de 60 a 90 minutos sobre controle de carga com foco em ajuste agudo durante a sessao. A progressao didatica esta preservada, o escopo esta majoritariamente protegido e o deck explicita os principios centrais da fonte validada.

Antes de considerar a fase finalizada, o proximo ajuste deve reconciliar a diferenca entre o roteiro ativo e o HTML: o roteiro atual esta consolidado em **33 slides**, enquanto o deck HTML esta estruturado em **32 slides**. Isso nao invalida o rascunho, mas exige decisao de consolidacao para evitar divergencia entre roteiro e produto apresentado.

## Alinhamento com publico

O material esta adequado a trainees e estagiarios de Educacao Fisica em treinamento interno para atuacao como personal trainer com publico geral.

Pontos fortes:

- Usa linguagem operacional, centrada em observacao, decisao e comunicacao.
- Evita transformar o trainee em pesquisador, clinico ou treinador de elite.
- Mantem exemplos e situacoes no nivel do chao da academia: sono, prontidao, aquecimento, qualidade tecnica, fala profissional e ajuste proporcional.
- Trata RPE/RIR como ferramentas pedagogicas e de calibragem, nao como medidas absolutas.

Risco residual:

- Alguns termos de interface do HTML permanecem em ingles nos kickers, como `Fatigue signs`, `Communication phrases` e `Final synthesis`. Isso nao compromete o conteudo, mas reduz a consistencia editorial em portugues.

## Alinhamento com escopo

O rascunho permanece dentro do recorte definido pela fonte mestre:

- foco em ajuste agudo de intensidade dentro da sessao;
- publico geral em academia;
- leitura combinada de contexto, execucao, RPE/RIR e sinais de fadiga;
- comunicacao profissional do ajuste.

Exclusoes preservadas:

- nao ensina performance esportiva de elite;
- nao conduz para prescricao clinica ou diagnostico de dor/patologia;
- nao usa 1RM, percentuais fixos ou periodizacao complexa como eixo decisorio;
- nao transforma registro de treino em etapa central da logica aguda.

Ponto de atencao:

- O deck inclui um slide de escopo com `Nao e registro cronico`, o que ajuda a proteger a fronteira. Na proxima revisao, manter esse enquadramento como exclusao e nao expandir o tema para controle historico.

## Progressao dos 8 blocos

A progressao geral esta preservada nos dois arquivos:

1. Problema real da sessao.
2. Vocabulario minimo de carga, intensidade e resposta.
3. Leitura inicial antes de ajustar.
4. RPE/RIR e qualidade tecnica como leitura combinada.
5. Manter, progredir, reduzir, recuperar, simplificar ou modificar.
6. Sinais de fadiga como pistas operacionais.
7. Comunicacao profissional do ajuste.
8. Sintese do raciocinio e pergunta-guia final.

O deck HTML comprime e redistribui algumas ideias do roteiro, mas cobre todos os blocos. A divergencia principal nao e de progressao; e de numeracao/estrutura: `slides/roteiro-apresentacao.md` declara 33 slides e o HTML declara 32.

## Densidade de linguagem

O HTML esta, em geral, adequado para apresentacao ao vivo:

- titulos curtos;
- bullets enxutos;
- notas do professor separadas do texto em tela;
- uso frequente de matrizes, cards, fluxos e marcadores visuais;
- baixa tendencia a transformar slide em apostila.

Pontos a ajustar:

- Conferir se os slides com matrizes e listas continuam legiveis em projetor, especialmente os blocos 5 e 7.
- Converter os kickers em ingles para portugues.
- Ao reconciliar 32 vs 33 slides, evitar resolver a diferenca colocando texto adicional em slides ja densos.

## Fidelidade a fonte

O rascunho esta fiel aos principios da `fluxo padrão/08_fonte-mestre-validada.md`:

- `A ficha orienta, a sessao calibra` aparece como eixo de abertura.
- Carga externa e carga interna/resposta aparecem como diferenca operacional.
- RPE/RIR sao apresentados como conversa e calibragem.
- Tecnica e sinais de fadiga podem reabrir a decisao quando entram em conflito com o autorrelato.
- A matriz de decisao cobre manter, progredir, reduzir, recuperar, simplificar e modificar.
- O principio da menor mudanca suficiente aparece explicitamente.

Risco residual:

- O roteiro consolidado menciona revisoes NotebookLM e um roteiro ativo de 33 slides, enquanto o HTML ainda se apresenta como deck de 32 slides. Isso cria uma pequena perda de rastreabilidade entre fonte de roteiro e produto final.

## Excluidos e cautelas

As cautelas principais estao bem protegidas:

- sinais visuais sao tratados como pistas, nao diagnosticos;
- velocidade/perda de fluidez nao e apresentada como medida precisa a olho nu;
- desconforto incomum nao vira diagnostico clinico;
- reducao de carga nao e tratada como fracasso do aluno;
- fluxos e checklists nao sao descritos como algoritmos rigidos.

Ponto de atencao:

- A expressao `Na duvida, o seu olho decide`, presente no roteiro do slide 27, pode soar absoluta se for usada sem a cautela associada. A nota de cautela mitiga isso, mas a proxima revisao pode preferir uma formulacao menos soberana, como `A tecnica reabre a decisao`.

## Utilidade operacional

O material e operacionalmente util para a aula:

- oferece uma pergunta-guia clara;
- organiza leitura antes, durante e apos a serie;
- mostra variaveis concretas de ajuste;
- inclui frases profissionais;
- preserva o principio de mudar uma variavel por vez;
- ajuda o professor a inserir exemplos orais sem depender de texto longo no slide.

O deck ainda nao deve ser tratado como versao final de design visual, porque usa elementos graficos locais/abstratos e nao imagens reais de treino. Para esta fase, isso e aceitavel como deck de trabalho sem dependencia externa.

## Correcoes concretas ja feitas durante a fase

- Roteiro consolidado em `slides/roteiro-apresentacao.md` a partir de uma versao NotebookLM de 33 slides.
- Refinamentos incorporados nos slides 15, 24, 27 e 32 do roteiro para reduzir redundancia, reforcar cautelas sobre sinais visuais e diferenciar calibragem pedagogica de decisao de seguranca.
- HTML atualizado com chamadas explicitas para os cinco pontos centrais: controle de carga alem de kg, carga externa vs resposta interna, RPE/RIR como calibragem, tecnica/fadiga reabrindo o autorrelato e menor mudanca suficiente.
- Escopo protegido com exclusao explicita de periodizacao, clinica, performance elite e registro cronico como foco central.

## Correcoes recomendadas para a proxima tarefa

1. Reconciliar `slides/roteiro-apresentacao.md` e `slides/controle-carga-slides.html`: decidir se o deck final tera 32 ou 33 slides e ajustar numeracao, fontes e estrutura.
2. Traduzir kickers residuais em ingles no HTML para portugues.
3. Revisar a formulacao de tecnica como criterio prioritario para evitar tom absoluto sem perder a ideia de que a tecnica pode sobrepor ou reabrir o autorrelato.
4. Conferir slides dos blocos 5 e 7 para manter baixa densidade textual apos qualquer ajuste de reconciliacao.
5. Manter registro de treino apenas como exclusao/contexto, sem reinseri-lo na logica central de decisao aguda.

## Itens restantes para verificar apos revisao humana ou NotebookLM

- Se o professor prefere manter o fechamento em 32 slides ou restaurar a estrutura de 33 slides do roteiro consolidado.
- Se os exemplos orais planejados cobrem alunos cansados, inseguros, tecnicamente instaveis e alunos com resposta melhor que a esperada.
- Se a linguagem visual XSTEAM deve receber imagens reais/realistas de treino na versao final ou permanecer com graficos locais no rascunho HTML.
- Se a matriz de decisao esta clara para trainees sem transformar decisao contextual em protocolo automatico.
- Se as frases profissionais soam naturais para a cultura de atendimento da equipe.
