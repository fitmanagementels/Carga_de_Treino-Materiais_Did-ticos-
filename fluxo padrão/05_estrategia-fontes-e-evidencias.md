# Estrategia de fontes e evidencias

Status: Atualizada em 2026-06-28 para uso com Dotflows do OpenEvidence e consolidacao local no Codex.

## Objetivo da etapa

Construir um pacote minimo de evidencias para sustentar a aula sobre controle de carga no treino de forca, com foco em ajuste agudo da intensidade durante a sessao.

O pacote deve servir como base para:

- diretriz didatica;
- diretriz de profundidade;
- prompts para NotebookLM;
- apresentacao em slides;
- ebook mobile-first com capitulos medios e mini checklists operacionais.

## Fonte piloto recebida

Arquivo externo usado como mapeamento inicial:

`/home/elohimlima/Downloads/VSCODE|ANTIGRAVITY/AULA_CARGA_DE_TREINO/projetos-didaticos/controle-carga-treino-forca/02-fonte-perplexity.md`

Origem: busca piloto no Perplexity, com organizacao de conceitos, referencias e cautelas.

Uso nesta etapa:

- aproveitar como mapa de termos, autores, conceitos e trilhas de busca;
- nao tratar ainda como fonte validada;
- auditar e complementar com Open Evidence e, depois, RAG/fonte consolidada.

## Diagnostico da fonte piloto

### Pontos fortes

- Boa separacao inicial entre carga externa e carga interna.
- Traz RPE, session-RPE, RPE baseado em RIR e limitacoes do RIR em iniciantes.
- Mapeia proximidade da falha, falha muscular, autorregulacao e progressao.
- Aponta autores e temas relevantes: Helms, Zourdos, Schoenfeld, ACSM, RPE/RIR, proximidade da falha e autorregulacao.
- Ja traz varias afirmacoes cautelosas uteis para trainees, especialmente sobre nao usar RIR como verdade absoluta em iniciantes.

### Pontos fracos para o nosso roteiro

- Fadiga aparece como conceito importante, mas ainda pouco desenvolvida como observacao didatica durante a execucao.
- Ha pouco material sobre "para onde olhar" durante uma serie: velocidade, fluidez, controle, amplitude, compensacoes, estabilidade e comportamento.
- A parte de comunicacao profissional aparece pouco sustentada, e talvez precise ser tratada mais como diretriz pedagogica/profissional do que como evidencia biometrica.
- Alguns trechos ainda puxam para progressao cronica, registro e monitoramento longitudinal; isso deve ser filtrado para nao reintroduzir registro como etapa da aula.

## Hierarquia de fontes

1. Evidencias revisadas e fontes rastreaveis obtidas via Open Evidence.
2. Outputs gerados pelos Dotflows do OpenEvidence, desde que auditados pelo Codex.
3. Artigos, revisoes e diretrizes identificadas na fonte piloto, quando confirmadas ou reaproveitadas no RAG.
4. Fonte piloto do Perplexity como mapa inicial e apoio de organizacao.
5. Fontes proprias do usuario, quando forem adicionadas.
6. Inferencias didaticas do professor/Codex, sempre marcadas como adaptacao pedagogica, nao como evidencia direta.

## Estrategia com Dotflows do OpenEvidence

A conversa com Perplexity sobre Dotflows foi recebida como insumo metodologico em:

`/home/elohimlima/Downloads/você sabe como funciona os dotflows do open eviden.md`

Decisao operacional:

- nao usar um prompt unico longo no OpenEvidence;
- usar Dotflows como modos reutilizaveis de resposta;
- fazer perguntas curtas, recortadas e auditaveis;
- salvar cada output bruto separadamente em `outputs/`;
- auditar no Codex antes de consolidar qualquer afirmacao no pacote final de evidencias.

Dotflows disponiveis/adicionados pelo usuario:

- `.COLETAR_BASE`: abre o tema e organiza o terreno conceitual.
- `.COLETAR_EVIDENCIA`: uso pontual para blindar afirmacoes cientificas sensiveis; nao sera o fluxo principal neste momento.
- `.COMPARAR_CONCEITOS`: compara conceitos, abordagens ou interpretacoes.
- `.MAPEAR_LACUNAS`: identifica incertezas, fragilidades e perguntas em aberto.
- `.RESUMIR_PARA_FONTE`: consolida os outputs em uma fonte-base limpa e reutilizavel.

Uso recomendado neste projeto:

1. Rodadas com `.COLETAR_BASE` para gerar material-fonte operacional e menos tecnico.
2. Rodadas com `.MAPEAR_LACUNAS` para evitar afirmacoes fortes demais.
3. Rodadas de comparacao apenas onde houver tensao didatica real.
4. Uso pontual de `.COLETAR_EVIDENCIA` somente quando uma afirmacao precisar de sustentacao tecnica mais rigorosa.
5. Consolidacao local no Codex, usando outputs brutos e auditorias.
6. Alimentacao do NotebookLM com fonte refinada, roteiro mestre e diretrizes dos produtos.

Observacao operacional: neste projeto, a etapa `.RESUMIR_PARA_FONTE` foi removida porque as rodadas foram feitas em chats separados no OpenEvidence. Como o Dotflow nao tera acesso simultaneo aos outputs anteriores, a consolidacao automatica ficaria fraca ou dependente de recortes colados manualmente. O Codex assumira a consolidacao refinada.

## Recortes de pesquisa

### Recorte 1 - Base conceitual minima

Perguntas:

- Como definir carga externa e carga interna no treino de forca de modo aplicavel ao personal trainer?
- Quais variaveis agudas compoem a carga externa em uma sessao de treino de forca?
- Quais indicadores de carga interna sao viaveis em contexto de academia e atendimento individual?

Uso no roteiro:

- Bloco 1;
- Bloco 2;
- abertura do ebook;
- glossario operacional.

### Recorte 2 - RPE/RIR e suas limitacoes

Perguntas:

- Qual a utilidade de RPE e RIR para autorregular intensidade no treino de forca?
- Quais sao as limitacoes de RIR em praticantes iniciantes ou pouco experientes?
- Como cruzar RPE/RIR com qualidade tecnica em vez de usar a escala isoladamente?

Uso no roteiro:

- Bloco 4;
- parte do Bloco 5;
- checklist de julgamento de esforco e tecnica.

### Recorte 3 - Proximidade da falha, fadiga e tecnica

Perguntas:

- O que a literatura permite afirmar sobre treinar ate a falha versus treinar proximo da falha?
- Como a fadiga durante series de forca se relaciona com perda de desempenho, velocidade, qualidade tecnica e tolerancia?
- Que cautelas devem ser ensinadas para publico geral e trainees iniciantes?

Uso no roteiro:

- Bloco 4;
- Bloco 5;
- Bloco 6.

### Recorte 4 - Sinais observaveis de fadiga durante a execucao

Perguntas:

- Quais sinais observaveis durante uma serie podem indicar fadiga relevante para ajuste de carga?
- Como velocidade de execucao, amplitude, estabilidade, compensacoes, ritmo e controle se alteram com fadiga?
- Quais sinais sao uteis pedagogicamente, mesmo quando a evidencia direta usa termos mais laboratoriais como velocity loss, repetition velocity, technique breakdown ou movement quality?

Uso no roteiro:

- Bloco 6, prioridade maxima;
- guia visual/verbal de sinais de fadiga;
- checklist "para onde olhar durante a serie".

### Recorte 5 - Ajustes agudos de intensidade

Perguntas:

- Quais variaveis podem ser manipuladas de forma aguda para adequar intensidade no treino de forca?
- Quando ajustar peso, repeticoes, amplitude, ritmo, intervalo ou variacao do exercicio?
- Como explicar que o melhor ajuste pode ser a menor mudanca suficiente?

Uso no roteiro:

- Bloco 5;
- mapa de decisao;
- mini checklist operacional.

### Recorte 6 - Comunicacao profissional do ajuste

Perguntas:

- Que principios de feedback e comunicacao breve podem ajudar o trainee a comunicar ajustes sem parecer inseguro?
- Como explicar ajustes de carga em linguagem simples, sem transformar a fala em aula longa durante a serie?

Uso no roteiro:

- Bloco 7;
- frases modelo;
- frases a evitar.

Observacao: este recorte pode exigir menos Open Evidence e mais diretriz didatica/profissional. Nao deve atrasar a curadoria biologica principal.

## Rodadas com Dotflows

Ferramenta: OpenEvidence usando Dotflows.

Motivo: o usuario tem acesso, a fonte piloto precisa de confirmacao e o tema envolve treino de forca, fadiga, esforco percebido e tomada de decisao baseada em evidencia.

Rodada 1 ja executada:

- Dotflow: `.COLETAR_BASE`.
- Tema: sinais observaveis de fadiga durante a execucao.
- Output salvo: `outputs/dotflow-01-fadiga-execucao-coletar-base.md`.
- Auditoria salva: `revisoes/auditoria-dotflow-01-fadiga-execucao.md`.

Rodada 2 ja executada:

- Dotflow: `.COLETAR_BASE`.
- Tema: RPE/RIR, tecnica e iniciantes.
- Output salvo: `outputs/dotflow-02-rpe-rir-tecnica.md`.
- Auditoria salva: `revisoes/auditoria-dotflow-02-rpe-rir-tecnica.md`.

Rodada 3 ja executada:

- Dotflow: `.COMPARAR_CONCEITOS`.
- Tema: falha, proximidade da falha e fadiga.
- Output salvo: `outputs/dotflow-03-falha-proximidade-fadiga.md`.
- Auditoria salva: `revisoes/auditoria-dotflow-03-falha-proximidade-fadiga.md`.

Rodada 4 ja executada:

- Dotflow: `.COLETAR_BASE`.
- Tema: ajustes agudos de intensidade.
- Output salvo: `outputs/dotflow-04-ajustes-agudos.md`.
- Auditoria salva: `revisoes/auditoria-dotflow-04-ajustes-agudos.md`.

Rodada 5 ja executada:

- Dotflow: `.MAPEAR_LACUNAS`.
- Tema: lacunas sobre sinais visuais observaveis sem equipamento.
- Output salvo: `outputs/dotflow-05-lacunas-fadiga.md`.
- Auditoria salva: `revisoes/auditoria-dotflow-05-lacunas-fadiga.md`.
- Objetivo cumprido: separar sinais com evidencia direta, evidencia indireta plausivel, uso pedagogico sem validacao direta e sinais que nao devem virar afirmacao forte.

Rodada 6 removida:

- Dotflow: `.RESUMIR_PARA_FONTE`.
- Motivo: inviavel como consolidacao automatica neste projeto, porque os outputs estao em chats separados.
- Substituto: consolidacao no Codex em `07_fontes-e-evidencias.md`.

## Output esperado da proxima etapa

A consolidacao local no Codex deve gerar uma fonte refinada, objetiva e rastreavel, com:

- conceitos essenciais;
- afirmacoes seguras;
- cautelas;
- implicacoes para cada bloco da aula;
- frases operacionais;
- checklists potenciais;
- referencias e origem de cada afirmacao importante.

## O que nao consolidar ainda

- Registro de treino como etapa da aula.
- Periodizacao complexa.
- Recomendacoes clinicas ou de reabilitacao.
- Foco em performance esportiva.
- Produto final em formato de slides ou ebook.

## Proximo checkpoint

Consolidar `07_fontes-e-evidencias.md`.

Outputs brutos ativos:

- `outputs/dotflow-01-fadiga-execucao-coletar-base.md`
- `outputs/dotflow-02-rpe-rir-tecnica.md`
- `outputs/dotflow-03-falha-proximidade-fadiga.md`
- `outputs/dotflow-04-ajustes-agudos.md`
- `outputs/dotflow-05-lacunas-fadiga.md`

Com os outputs ja auditados, o Codex deve consolidar `07_fontes-e-evidencias.md`. Esse arquivo sera a principal fonte refinada para o NotebookLM.
