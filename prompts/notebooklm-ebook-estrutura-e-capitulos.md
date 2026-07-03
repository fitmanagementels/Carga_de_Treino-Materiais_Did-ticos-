---
type: reference
title: Prompt NotebookLM Ebook Estrutura e Capitulos
created: 2026-06-30
updated: 2026-07-03
tags: [notebooklm, ebook, mobile-first, prompts]
related:
  - '[[Roteiro Ebook Mobile First Controle de Carga]]'
  - '[[Diretriz Ebook Mobile First]]'
  - '[[Fonte Mestre Validada]]'
---

# Prompts NotebookLM - ebook mobile-first

Status: prompt pack ativo para produzir o ebook mobile-first em etapas no NotebookLM.

Uso: este arquivo deve ser usado depois de subir as fontes corretas no NotebookLM. O ebook deve ser produzido em rodadas, seguindo o roteiro ativo `diretrizes/roteiro-ebook-mobile-first.md`. Nao pedir o ebook completo em uma unica resposta.

## Fontes que devem estar no notebook

Fontes principais:

- `diretrizes/fontes-notebooklm-produtos.md`
- `fluxo padrão/01_briefing-inicial.md`
- `fluxo padrão/03_arquitetura-logica-rascunho.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `fluxo padrão/08_fonte-mestre-validada.md`
- `diretrizes/criterios-linguagem-densidade-operacional.md`
- `diretrizes/tema-visual-xsteam.md`
- `diretrizes/diretriz-ebook-mobile-first.md`
- `diretrizes/roteiro-ebook-mobile-first.md`

Fontes secundarias, se estiverem no notebook:

- `fluxo padrão/07_fontes-e-evidencias.md`
- `outputs/dotflow-01-fadiga-execucao-coletar-base.md`
- `outputs/dotflow-02-rpe-rir-tecnica.md`
- `outputs/dotflow-03-falha-proximidade-fadiga.md`
- `outputs/dotflow-04-ajustes-agudos.md`
- `outputs/dotflow-05-lacunas-fadiga.md`

Nao usar outputs intermediarios antigos do NotebookLM como fonte para criar o ebook.

## Hierarquia obrigatoria

Use esta hierarquia em todos os prompts:

1. `fluxo padrão/01_briefing-inicial.md`, `fluxo padrão/03_arquitetura-logica-rascunho.md`, `fluxo padrão/04_roteiro-mestre-rascunho.md` e `fluxo padrão/08_fonte-mestre-validada.md` definem publico, escopo, progressao didatica e conteudo tecnico validado.
2. `diretrizes/roteiro-ebook-mobile-first.md` define os 8 capitulos, a ordem, a funcao de cada capitulo, o conteudo essencial, os componentes mobile-first, os exemplos, checklists, cautelas, relacao com slides e ancoras de fonte.
3. `diretrizes/diretriz-ebook-mobile-first.md` define formato, estrutura interna dos capitulos, densidade textual, componentes obrigatorios e leitura em celular.
4. `diretrizes/criterios-linguagem-densidade-operacional.md` define linguagem, tom, nivel operacional e limites de tecnicismo.
5. `diretrizes/tema-visual-xsteam.md` define identidade visual e criterios de estilo para futura diagramacao.
6. `diretrizes/fontes-notebooklm-produtos.md` define quais fontes podem ou nao orientar o produto.
7. `fluxo padrão/07_fontes-e-evidencias.md` e os arquivos `outputs/dotflow-*` sao fontes secundarias de apoio teorico e rastreabilidade. Eles nao devem mudar escopo, tom, estrutura, densidade, ordem dos capitulos ou formato mobile-first.

Se houver conflito entre fontes, seguir primeiro os arquivos validados do fluxo padrao; depois o roteiro do ebook; depois a diretriz do ebook; depois os criterios de linguagem e tema visual; por ultimo as fontes secundarias.

## Prompt de configuracao do sistema

Onde usar: NotebookLM > Configuracoes do notebook > instrucao/configuracao personalizada do notebook.

Funcao: definir o comportamento permanente do NotebookLM enquanto este notebook estiver sendo usado para produzir o ebook mobile-first.

Prompt pronto:

```text
Voce e meu assistente editorial para produzir um ebook mobile-first de capacitacao interna sobre controle de carga no treino de forca.

O publico do material sao trainees e estagiarios de Educacao Fisica em formacao para atuar como personal trainer com publico geral. O objetivo do ebook e ajudar esse trainee a estudar, fixar e revisar a habilidade de ler a resposta do aluno durante a sessao e ajustar a demanda do exercicio de forma aguda, com postura profissional.

Prioridade das fontes:
1. Briefing, arquitetura, roteiro mestre e fonte mestre validada definem publico, escopo, progressao didatica e conteudo tecnico validado.
2. O roteiro do ebook mobile-first define os 8 capitulos, a ordem, a funcao de cada capitulo, o conteudo essencial, os componentes mobile-first, os exemplos, checklists, cautelas, relacao com slides e ancoras de fonte.
3. A diretriz do ebook mobile-first define formato, estrutura interna dos capitulos, densidade textual, componentes obrigatorios e leitura em celular.
4. Os criterios de linguagem e o tema visual XSTEAM definem tom, nivel operacional, limites de tecnicismo e identidade visual futura.
5. A diretriz de fontes para NotebookLM define quais fontes podem ou nao orientar o produto.
6. Fontes secundarias e dotflows servem apenas para apoio teorico e rastreabilidade. Elas nao podem mudar escopo, tom, estrutura, densidade, ordem dos capitulos ou formato mobile-first.

Se houver conflito entre fontes, siga os arquivos validados do fluxo padrao e o roteiro do ebook. Nao deixe outputs brutos, dotflows, auditorias ou respostas intermediarias antigas do NotebookLM comandarem a estrutura do produto.

Estilo obrigatorio:
- Escreva em portugues do Brasil.
- Use tom de lider e mentor de equipe com funcao professoral.
- Seja tecnico sem academicismo.
- Priorize aplicacao operacional no contexto de personal trainer com publico geral.
- Explique termos de treino de forca quando aparecerem.
- Evite fisiologia profunda, linguagem clinica, jargoes desnecessarios e discussao academica longa.
- Use paragrafos curtos, secoes escaneaveis, listas, cards, boxes, checklists e matrizes simples.
- Evite tabelas largas, porque o ebook sera mobile-first.
- Mais de duas telas seguidas apenas de texto e excesso de densidade.

Escopo obrigatorio:
- O foco e ajuste agudo durante a sessao.
- O trainee deve aprender a ler contexto, aquecimento, execucao, RPE/RIR, tecnica e sinais de fadiga para decidir se deve manter, progredir, reduzir, recuperar, simplificar ou modificar.
- Registro de treino, periodizacao complexa, performance esportiva, reabilitacao clinica, calculos de 1RM como regra e fisiologia profunda ficam fora do eixo deste ebook.

Cautelas obrigatorias:
- Nao trate RPE/RIR como dado matematico perfeito ou comando automatico.
- Nao trate o relato de iniciantes como perfeitamente preciso.
- Nao trate sinais visuais de fadiga como medidas objetivas.
- Nao afirme que o personal mede percentuais de perda de velocidade a olho nu.
- Use termos como pistas, alertas, sugere, merece revisar e ajuda a decidir.
- Nao transforme checklists e matrizes em algoritmos rigidos.
- Nao invente autores, referencias, percentuais, protocolos ou evidencias que nao estejam nas fontes.

Quando eu pedir producao de conteudo, siga o roteiro do ebook mobile-first como estrutura principal. Quando eu pedir revisao, avalie alinhamento com a fonte mestre validada, o roteiro do ebook, a diretriz mobile-first, os criterios de linguagem e as cautelas metodologicas.

Quando produzir capitulos, use esta estrutura como padrao:
1. Abertura.
2. Ideia central.
3. O que voce precisa entender.
4. Definicao rapida.
5. Observe antes de ajustar.
6. Exemplo operacional.
7. Checklist de estudo.
8. Frases profissionais.
9. Cautela.
10. Recapitulo.
11. Nota de producao.

A Nota de producao deve indicar componentes visuais/mobile recomendados e ancoras de fonte, mas nao precisa entrar no ebook final do aluno.
```

## Regras fixas para todos os prompts

- Publico: trainees e estagiarios de Educacao Fisica em treinamento interno para atuar como personal trainer com publico geral.
- Objetivo: ensinar leitura da resposta do aluno e ajuste agudo da demanda do exercicio durante a sessao.
- Foco: ajuste dentro da sessao, com decisao profissional sobre manter, progredir, reduzir, recuperar, simplificar ou modificar.
- Tom: lider e mentor de equipe com funcao professoral; tecnico sem academicismo; operacional; claro; profissional.
- Produto: ebook mobile-first para estudo, fixacao e revisao posterior, nao material para consultar durante o atendimento.
- Densidade: paragrafos curtos, secoes escaneaveis, boxes, cards e checklists. Mais de duas telas seguidas apenas de texto e excesso.
- Fora de escopo: performance esportiva, reabilitacao clinica, periodizacao complexa, calculos de 1RM como regra, fisiologia profunda e registro de treino como etapa central do ajuste agudo.
- Cautelas: RPE/RIR, sinais visuais e qualidade tecnica sao ferramentas de julgamento, nao comandos automaticos.
- Sinais visuais de fadiga devem ser tratados como pistas operacionais, nao medidas objetivas.
- Nao transformar checklists em algoritmo rigido.
- Nao inventar fontes, autores, percentuais ou protocolos que nao estejam nas fontes.

## Estrutura obrigatoria de cada capitulo

Cada capitulo produzido deve seguir esta estrutura:

```text
# Capitulo [NUMERO] - [TITULO]

## Abertura
[Problema pratico do capitulo, em texto curto.]

## Ideia central
[Uma frase forte e operacional.]

## O que voce precisa entender
[Explicacao aplicada em secoes curtas.]

## Definicao rapida
[Termos tecnicos relevantes do capitulo. Se nao houver termo novo, diga que nao ha definicao nova.]

## Observe antes de ajustar
[Pergunta ou comando curto para impedir decisao automatica.]

## Exemplo operacional
[Situacao de academia com publico geral, sem depender da fala ao vivo do professor.]

## Checklist de estudo
[3 a 6 itens, em formato mobile-friendly.]

## Frases profissionais
[2 a 4 frases quando o tema envolver conversa, comando ou ajuste. Se nao for relevante, manter curto.]

## Cautela
[Principal exagero ou desvio a evitar.]

## Recapitulo
[Resumo final para fixacao, em lista curta ou cards.]

## Nota de producao
[Indicar componentes visuais/mobile recomendados e ancoras de fonte. Esta nota e para producao, nao precisa entrar no ebook final do aluno.]
```

## Fluxo recomendado

1. Colocar o prompt de configuracao do sistema nas configuracoes do notebook.
2. Rodar o Prompt 0 para confirmar hierarquia e riscos.
3. Rodar o Prompt 1 para criar o mapa consolidado do ebook.
4. Auditar no Codex o mapa consolidado.
5. Rodar os prompts de capitulos em lotes:
   - Prompt 2: capitulos 1 e 2.
   - Prompt 3: capitulos 3 e 4.
   - Prompt 4: capitulo 5.
   - Prompt 5: capitulo 6.
   - Prompt 6: capitulos 7 e 8.
6. Trazer cada lote ao Codex se houver duvida de densidade, escopo ou fidelidade.
7. Rodar o Prompt 7 para revisao final do ebook consolidado.

## Prompt 0 - Checagem de hierarquia e alinhamento

Onde usar: NotebookLM, na conversa.

Objetivo desta rodada: confirmar que o NotebookLM entendeu a hierarquia das fontes e os limites do ebook antes de produzir conteudo.

Prompt pronto:

```text
Antes de produzir o ebook, confirme a hierarquia de fontes e os limites do produto.

Use esta hierarquia:
1. Briefing, arquitetura, roteiro mestre e fonte mestre validada definem publico, escopo, progressao didatica e conteudo tecnico validado.
2. O roteiro do ebook mobile-first define os 8 capitulos, a ordem, a funcao de cada capitulo, o conteudo essencial, os componentes mobile-first, os exemplos, checklists, cautelas, relacao com slides e ancoras de fonte.
3. A diretriz do ebook mobile-first define formato, estrutura interna dos capitulos, densidade textual, componentes obrigatorios e leitura em celular.
4. Os criterios de linguagem e o tema visual XSTEAM definem tom, nivel operacional, limites de tecnicismo e identidade visual futura.
5. A diretriz de fontes para NotebookLM define quais fontes podem ou nao orientar o produto.
6. Fontes secundarias servem apenas para apoio teorico e rastreabilidade. Elas nao podem mudar escopo, tom, estrutura, densidade ou ordem dos capitulos.

Contexto obrigatorio:
- Publico: trainees e estagiarios de Educacao Fisica em treinamento interno para atuar como personal trainer com publico geral.
- Produto: ebook mobile-first para estudo, fixacao e revisao posterior.
- Objetivo: ensinar leitura da resposta do aluno e ajuste agudo da demanda do exercicio durante a sessao.
- Foco: decisao profissional sobre manter, progredir, reduzir, recuperar, simplificar ou modificar.
- Fora de escopo: performance esportiva, reabilitacao clinica, periodizacao complexa, calculos de 1RM como regra, fisiologia profunda e registro de treino como etapa central do ajuste agudo.

Entregue:
1. confirmacao da hierarquia em ate 8 bullets;
2. os 8 capitulos que devem ser preservados, na ordem do roteiro do ebook;
3. 10 riscos de desvio que voce deve evitar ao escrever o ebook;
4. como voce vai tratar RPE/RIR, sinais visuais de fadiga e qualidade tecnica sem transformar isso em comando automatico;
5. confirmacao de que nao vai usar outputs intermediarios antigos do NotebookLM como fonte principal.

Nao escreva capitulos ainda.
```

Formato esperado: checagem objetiva de hierarquia e riscos.

Salvar resultado em: `outputs/produtos-ebook/notebooklm-ebook-00-checagem-hierarquia.md`.

Trazer de volta ao Codex: apenas se a hierarquia sair desalinhada.

## Prompt 1 - Mapa consolidado do ebook

Onde usar: NotebookLM, na conversa.

Objetivo desta rodada: transformar o roteiro do ebook em um mapa de producao, sem escrever os capitulos finais ainda.

Prompt pronto:

```text
Agora crie o mapa consolidado do ebook mobile-first da aula "controle de carga no treino de forca".

Nao escreva os capitulos finais ainda. Use o roteiro ativo do ebook como estrutura mandataria.

Use esta hierarquia:
1. Briefing, arquitetura, roteiro mestre e fonte mestre validada definem publico, escopo, progressao didatica e conteudo tecnico validado.
2. O roteiro do ebook mobile-first define os 8 capitulos, a ordem, a funcao de cada capitulo, o conteudo essencial, os componentes mobile-first, os exemplos, checklists, cautelas, relacao com slides e ancoras de fonte.
3. A diretriz do ebook mobile-first define formato, estrutura interna dos capitulos, densidade textual, componentes obrigatorios e leitura em celular.
4. Os criterios de linguagem e o tema visual XSTEAM definem tom, nivel operacional, limites de tecnicismo e identidade visual futura.
5. Fontes secundarias servem apenas para apoio teorico e rastreabilidade.

Tarefa:
Crie um mapa de producao do ebook com 8 capitulos, preservando a ordem e a funcao didatica do roteiro.

Para cada capitulo, entregue:
1. titulo do capitulo;
2. funcao no ebook;
3. objetivo de estudo;
4. ideia central;
5. secoes internas sugeridas;
6. termos que precisam de definicao rapida;
7. exemplo operacional previsto;
8. checklist ou matriz mobile prevista;
9. frases profissionais previstas, quando relevantes;
10. cautela principal;
11. recapitulo esperado;
12. componentes visuais/mobile recomendados;
13. ancoras de fonte.

Regras:
- Nao altere a ordem dos 8 capitulos.
- Nao transforme o ebook em transcricao dos slides.
- Nao escreva os capitulos finais agora.
- Nao use tabelas largas.
- Use linguagem clara, operacional e adequada para trainees.
- Preserve o foco no ajuste agudo durante a sessao.
- Nao reintroduza registro de treino como etapa central.
- Nao trate sinais visuais como medicao objetiva.
```

Formato esperado: mapa de producao em Markdown, com secoes por capitulo.

Salvar resultado em: `outputs/produtos-ebook/notebooklm-ebook-01-mapa-consolidado.md`.

Trazer de volta ao Codex: resultado completo para auditoria antes de pedir os capitulos finais.

## Prompt 2 - Produzir capitulos 1 e 2

Onde usar: NotebookLM, na conversa, depois do mapa consolidado estar aprovado ou aceitavel.

Objetivo desta rodada: escrever os capitulos 1 e 2 do ebook, preservando o roteiro ativo.

Prompt pronto:

```text
Escreva apenas os Capitulos 1 e 2 do ebook mobile-first. Nao escreva os demais capitulos.

Use o mapa consolidado do ebook e siga obrigatoriamente o roteiro ativo `diretrizes/roteiro-ebook-mobile-first.md`.

Capitulos desta rodada:

Capitulo 1 - A carga e ajustada no atendimento real
- Funcao: mostrar por que o ajuste de carga acontece no atendimento real.
- Ideia central: A ficha orienta, mas a resposta do aluno calibra a decisao.
- Conteudo essencial: variabilidade do aluno no dia; plano versus sessao real; ajuste como competencia tecnica; postura do trainee diante da incerteza operacional.
- Componentes obrigatorios: card "plano x realidade"; mini lista "quando a ficha precisa ser recalibrada"; exemplo operacional; frases de abertura; cautela contra mudanca aleatoria.

Capitulo 2 - Carga, intensidade e resposta: o vocabulario minimo
- Funcao: construir vocabulario minimo de carga, intensidade e resposta.
- Ideia central: Controlar carga nao e controlar apenas peso; e ajustar a relacao entre proposta e resposta.
- Conteudo essencial: carga externa; carga interna/resposta; intensidade relativa; respostas diferentes ao mesmo peso; variaveis manipulaveis durante a sessao.
- Componentes obrigatorios: mini glossario; cards "externa = proposta" e "interna = resposta"; diagrama simples de variaveis manipulaveis; cautela contra periodizacao, volume semanal, 1RM e calculos cronicos.

Estrutura obrigatoria de cada capitulo:
1. Abertura.
2. Ideia central.
3. O que voce precisa entender.
4. Definicao rapida.
5. Observe antes de ajustar.
6. Exemplo operacional.
7. Checklist de estudo.
8. Frases profissionais.
9. Cautela.
10. Recapitulo.
11. Nota de producao.

Regras de escrita:
- Escreva para leitura em celular.
- Use paragrafos curtos.
- Use subtitulos escaneaveis.
- Nao use tabelas largas.
- Use cards, listas empilhadas e boxes quando precisar comparar ideias.
- O texto deve ser mais explicativo que slides, mas nao virar apostila academica.
- Nao invente fontes.
- Nao puxe para performance, clinica, periodizacao complexa ou registro de treino.
```

Formato esperado: capitulos 1 e 2 completos em Markdown.

Salvar resultado em: `outputs/produtos-ebook/notebooklm-ebook-02-capitulos-1-2.md`.

Trazer de volta ao Codex: resultado completo para auditoria de densidade e tom.

## Prompt 3 - Produzir capitulos 3 e 4

Onde usar: NotebookLM, na conversa.

Objetivo desta rodada: escrever os capitulos 3 e 4 do ebook, preservando o roteiro ativo.

Prompt pronto:

```text
Escreva apenas os Capitulos 3 e 4 do ebook mobile-first. Nao escreva os demais capitulos.

Use o mapa consolidado do ebook e siga obrigatoriamente o roteiro ativo `diretrizes/roteiro-ebook-mobile-first.md`.

Capitulos desta rodada:

Capitulo 3 - Leitura inicial: antes de mexer na carga
- Funcao: ensinar leitura inicial antes de mexer na carga.
- Ideia central: O ajuste bom comeca antes da troca de peso.
- Conteudo essencial: prontidao; perguntas breves; diferenca entre conversar e interrogar; aquecimento como validacao; sinais iniciais de inseguranca, cansaco ou limite tecnico.
- Componentes obrigatorios: checklist "antes da primeira serie efetiva"; card "pergunte sem transferir a decisao"; exemplo de aquecimento como leitura; perguntas curtas e seguras; cautela contra interrogatorio e diagnostico clinico.

Capitulo 4 - Intensidade na pratica: RPE, RIR e tecnica
- Funcao: integrar RPE, RIR, tecnica e contexto.
- Ideia central: Nenhum indicador isolado manda na decisao.
- Conteudo essencial: RPE; RIR; diferenca entre percepcao global e repeticoes de qualidade restantes; iniciantes estimam pior; conflito entre relato e execucao; triangulacao com tecnica e contexto.
- Componentes obrigatorios: definicao rapida de RPE e RIR; cards "relato", "tecnica" e "contexto"; matriz mobile de conflito entre indicadores; frases para perguntar esforco sem entregar a decisao ao aluno; cautela contra matematica precisa.

Estrutura obrigatoria de cada capitulo:
1. Abertura.
2. Ideia central.
3. O que voce precisa entender.
4. Definicao rapida.
5. Observe antes de ajustar.
6. Exemplo operacional.
7. Checklist de estudo.
8. Frases profissionais.
9. Cautela.
10. Recapitulo.
11. Nota de producao.

Regras de escrita:
- Escreva para leitura em celular.
- Use paragrafos curtos.
- Use subtitulos escaneaveis.
- Nao use tabelas largas.
- Explique termos de treino de forca quando aparecerem.
- Mantenha tom de capacitacao interna para trainees.
- Nao trate RPE/RIR como comandos automaticos.
- Nao trate o relato do aluno como perfeitamente preciso em iniciantes.
- Nao coloque a tecnica como desautorizacao automatica do aluno; use como criterio de julgamento integrado.
```

Formato esperado: capitulos 3 e 4 completos em Markdown.

Salvar resultado em: `outputs/produtos-ebook/notebooklm-ebook-03-capitulos-3-4.md`.

Trazer de volta ao Codex: resultado completo para auditoria de densidade, tom e cautelas.

## Prompt 4 - Produzir capitulo 5

Onde usar: NotebookLM, na conversa.

Objetivo desta rodada: escrever apenas o capitulo 5, que e o capitulo operacional mais denso.

Prompt pronto:

```text
Escreva apenas o Capitulo 5 do ebook mobile-first. Nao escreva os demais capitulos.

Use o mapa consolidado do ebook e siga obrigatoriamente o roteiro ativo `diretrizes/roteiro-ebook-mobile-first.md`.

Capitulo 5 - Da leitura ao ajuste: escolher a menor mudanca suficiente
- Funcao: transformar leitura em ajuste agudo proporcional.
- Ideia central: O bom ajuste resolve o problema dominante com a menor mudanca suficiente.
- Conteudo essencial: quando manter; quando progredir; quando reduzir; quando recuperar com intervalo; quando simplificar; quando modificar; peso, repeticoes, amplitude, ritmo, intervalo e variacao como botoes de ajuste.
- Componentes obrigatorios: matriz "se observar, considere"; cards por decisao; bloco "um botao por vez"; exemplos operacionais; frases para conduzir aumento, reducao, intervalo maior ou troca de variacao.
- Cautelas obrigatorias: evitar mudar muitas variaveis ao mesmo tempo; evitar trocar exercicio sempre que surge dificuldade; nao transformar matriz em algoritmo rigido.

Estrutura obrigatoria:
1. Abertura.
2. Ideia central.
3. O que voce precisa entender.
4. Definicao rapida.
5. Observe antes de ajustar.
6. Exemplo operacional.
7. Checklist de estudo.
8. Frases profissionais.
9. Cautela.
10. Recapitulo.
11. Nota de producao.

Regras de escrita:
- Escreva para leitura em celular.
- Use paragrafos curtos.
- Divida o capitulo em secoes bem escaneaveis.
- Evite tabela larga; se houver matriz, use cards empilhados.
- Mostre como escolher entre manter, progredir, reduzir, recuperar, simplificar e modificar.
- Preserve julgamento profissional: a matriz orienta, mas nao decide sozinha.
- Nao usar registro de treino como etapa da logica aguda.
- Nao usar 1RM, volume semanal ou periodizacao como eixo do capitulo.
```

Formato esperado: capitulo 5 completo em Markdown.

Salvar resultado em: `outputs/produtos-ebook/notebooklm-ebook-04-capitulo-5.md`.

Trazer de volta ao Codex: resultado completo para auditoria, porque este capitulo concentra a competencia operacional principal.

## Prompt 5 - Produzir capitulo 6

Onde usar: NotebookLM, na conversa.

Objetivo desta rodada: escrever apenas o capitulo 6, preservando as cautelas sobre sinais de fadiga.

Prompt pronto:

```text
Escreva apenas o Capitulo 6 do ebook mobile-first. Nao escreva os demais capitulos.

Use o mapa consolidado do ebook e siga obrigatoriamente o roteiro ativo `diretrizes/roteiro-ebook-mobile-first.md`.

Capitulo 6 - Sinais de fadiga durante a execucao
- Funcao: ensinar para onde olhar durante a serie para reconhecer pistas de fadiga.
- Ideia central: Sinais visuais sao pistas para decidir, nao medidas de precisao.
- Conteudo essencial: esforco esperado versus fadiga que muda qualidade; lentidao evidente; perda de fluidez; compensacoes; amplitude encurtando; perda de estabilidade; ritmo quebrado; expressao, respiracao e hesitacao como pistas contextuais.
- Componentes obrigatorios: guia "para onde olhar"; cards por categoria de sinal; cautela visual "nao somos sensores de precisao"; exemplo operacional; frases para encerrar, ajustar ou reduzir sem alarmismo.
- Cautelas obrigatorias: nao ensinar o olho a medir percentual de perda de velocidade; nao tratar respiracao ou hesitacao como prova isolada; nao transformar sinal visual em diagnostico.

Estrutura obrigatoria:
1. Abertura.
2. Ideia central.
3. O que voce precisa entender.
4. Definicao rapida.
5. Observe antes de ajustar.
6. Exemplo operacional.
7. Checklist de estudo.
8. Frases profissionais.
9. Cautela.
10. Recapitulo.
11. Nota de producao.

Regras de escrita:
- Escreva para leitura em celular.
- Use paragrafos curtos.
- Use linguagem operacional: "pistas", "alertas", "sugere", "merece revisar".
- Evite linguagem de medicao precisa: nao use percentuais visuais, sensores, VBT como requisito ou diagnosticos.
- Explique a diferenca entre observar fadiga e fingir medir fadiga.
- Mantenha o foco no ajuste agudo da sessao.
```

Formato esperado: capitulo 6 completo em Markdown.

Salvar resultado em: `outputs/produtos-ebook/notebooklm-ebook-05-capitulo-6.md`.

Trazer de volta ao Codex: resultado completo para auditoria, porque este capitulo tem maior risco de tecnicismo ou afirmacao forte demais.

## Prompt 6 - Produzir capitulos 7 e 8

Onde usar: NotebookLM, na conversa.

Objetivo desta rodada: escrever os capitulos finais, fechando comunicacao profissional e sintese.

Prompt pronto:

```text
Escreva apenas os Capitulos 7 e 8 do ebook mobile-first. Nao reescreva os capitulos anteriores.

Use o mapa consolidado do ebook e siga obrigatoriamente o roteiro ativo `diretrizes/roteiro-ebook-mobile-first.md`.

Capitulo 7 - Comunicacao profissional do ajuste
- Funcao: comunicar o ajuste com postura profissional.
- Ideia central: A comunicacao faz parte do controle de carga.
- Conteudo essencial: dizer o que foi observado; explicar motivo em linguagem simples; comandar a acao; educar brevemente; frases modelo; frases a evitar; tom calmo, direto e profissional.
- Componentes obrigatorios: estrutura em 3 passos "observei -> motivo -> acao"; cards "prefira/evite"; mini banco de frases; checklist "o que vi, por que ajustei, o que faremos agora".
- Cautela obrigatoria: ouvir o aluno nao significa terceirizar a decisao tecnica.

Capitulo 8 - Checklist final de raciocinio
- Funcao: consolidar o raciocinio completo em uma revisao final.
- Ideia central: O trainee deve saber perguntar: o que esta acontecendo agora e qual e a menor mudanca suficiente?
- Conteudo essencial: sintese dos capitulos; cadeia de decisao; limites do material; o que fica fora do escopo; reforco de postura profissional.
- Componentes obrigatorios: checklist final completo; fluxograma vertical mobile; bloco "erros comuns a evitar"; caso-sintese curto mostrando leitura, decisao e comunicacao.
- Cautela obrigatoria: nao transformar o checklist em protocolo rigido nem reintroduzir registro como etapa da aula.

Estrutura obrigatoria de cada capitulo:
1. Abertura.
2. Ideia central.
3. O que voce precisa entender.
4. Definicao rapida.
5. Observe antes de ajustar.
6. Exemplo operacional.
7. Checklist de estudo.
8. Frases profissionais.
9. Cautela.
10. Recapitulo.
11. Nota de producao.

Regras de escrita:
- Escreva para leitura em celular.
- Use paragrafos curtos.
- Use tom de lider e mentor de equipe com funcao professoral.
- O capitulo 7 pode ter mais frases profissionais que os demais.
- O capitulo 8 deve consolidar, nao abrir novos conceitos.
- Nao terminar com conteudo generico motivacional; terminar com raciocinio operacional.
```

Formato esperado: capitulos 7 e 8 completos em Markdown.

Salvar resultado em: `outputs/produtos-ebook/notebooklm-ebook-06-capitulos-7-8.md`.

Trazer de volta ao Codex: resultado completo para auditoria final de coerencia e fechamento.

## Prompt 7 - Revisao final do ebook consolidado

Onde usar: NotebookLM, depois de todos os capitulos terem sido escritos.

Objetivo desta rodada: auditar coerencia final antes de consolidar ou diagramar.

Prompt pronto:

```text
Revise o ebook mobile-first consolidado a partir dos capitulos produzidos.

Nao reescreva tudo. Audite a coerencia final e indique correcoes pontuais.

Compare contra:
1. fonte mestre validada;
2. briefing, arquitetura e roteiro mestre;
3. roteiro do ebook mobile-first;
4. diretriz do ebook mobile-first;
5. criterios de linguagem, densidade e nivel operacional;
6. tema visual XSTEAM;
7. diretriz de fontes para NotebookLM.

Verifique:
1. continuidade entre os 8 capitulos;
2. aderencia ao roteiro do ebook mobile-first;
3. progressao da pergunta-guia da aula ate o checklist final;
4. consistencia de tom para trainees de Educacao Fisica em capacitacao interna;
5. densidade mobile-first, com paragrafos curtos e sem tabelas largas;
6. equilibrio entre conceito, observacao, decisao, exemplo, checklist, comunicacao e cautela;
7. ausencia de desvio para performance esportiva, reabilitacao clinica, periodizacao complexa ou fisiologia excessiva;
8. ausencia de registro de treino como etapa central do ajuste agudo;
9. preservacao da fonte mestre validada;
10. uso de RPE, RIR, sinais visuais e qualidade tecnica como ferramentas de julgamento, nao comandos automaticos;
11. sinais visuais tratados como pistas, nao medicoes objetivas;
12. repeticoes desnecessarias entre capitulos;
13. lacunas que dificultam estudo autonomo pelo trainee;
14. respeito a hierarquia de fontes.

Entregue:
- aprovacao geral ou nao;
- problemas por capitulo;
- trechos que devem ser encurtados;
- trechos que precisam de mais aplicacao operacional;
- correcoes pontuais sugeridas;
- capitulos ou secoes que devem ser ajustados antes da diagramacao;
- riscos que ainda devem ser revisados pelo Codex;
- recomendacao final para consolidacao do ebook.

Nao reescreva o ebook inteiro. Gere apenas diagnostico e correcoes pontuais.
```

Formato esperado: auditoria objetiva do ebook consolidado.

Salvar resultado em: `outputs/produtos-ebook/notebooklm-ebook-07-revisao-final.md`.

Trazer de volta ao Codex: resposta completa para revisao e consolidacao final.

## Prompt opcional - Corrigir um lote especifico

Onde usar: NotebookLM, se um lote de capitulos vier desalinhado.

Objetivo desta rodada: corrigir uma parte sem regenerar todo o ebook.

Prompt pronto:

```text
Corrija apenas o trecho abaixo do ebook mobile-first. Nao reescreva os demais capitulos.

Trecho a corrigir:
[COLE AQUI O CAPITULO OU SECAO]

Problema a corrigir:
[DESCREVA O PROBLEMA: excesso de densidade, tecnicismo, desalinhamento com roteiro, falta de exemplo, falta de cautela, etc.]

Compare contra:
1. fonte mestre validada;
2. roteiro do ebook mobile-first;
3. diretriz do ebook mobile-first;
4. criterios de linguagem, densidade e nivel operacional.

Regras:
- Preserve o que estiver bom.
- Corrija apenas o necessario.
- Mantenha leitura mobile-first.
- Nao mude o escopo do capitulo.
- Nao acrescente fontes inventadas.
- Nao puxe para performance, clinica, periodizacao complexa ou registro de treino.
- Nao transforme RPE/RIR ou sinais visuais em comandos automaticos.

Entregue:
1. diagnostico curto;
2. lista do que foi corrigido;
3. versao corrigida apenas do trecho problemático.
```

Formato esperado: correcao pontual do trecho.

Salvar resultado em: `outputs/produtos-ebook/notebooklm-ebook-correcao-[IDENTIFICADOR].md`.
