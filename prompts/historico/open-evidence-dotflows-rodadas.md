# Rodadas curtas com Dotflows - OpenEvidence

Status: Rodadas 1 a 5 executadas; Rodada 6 removida neste projeto.

## Como usar

Execute uma rodada por vez no OpenEvidence usando o Dotflow indicado.

Depois de cada rodada:

1. salve o output bruto no arquivo indicado;
2. traga o output ao Codex para auditoria;
3. nao consolide nada no NotebookLM antes da auditoria.

## Rodada 1 - Sinais de fadiga durante a execucao

Dotflow recomendado: `.COLETAR_BASE`

Pergunta para colar:

```text
Em series de treino de forca para adultos saudaveis/público geral, quais sinais observaveis durante a execucao podem indicar fadiga relevante para ajuste agudo da carga?

Foque em: reducao de velocidade, perda de fluidez, compensacoes, encurtamento de amplitude, instabilidade, perda de posicao, dificuldade de manter ritmo, alteracao de respiracao, hesitacao e conflito entre relato do aluno e qualidade real da execucao.

Quero separar evidencia direta de inferencia pratica para personal trainer. Nao gere aula, slides ou prescricao individual.
```

Salvar em:

`outputs/dotflow-01-fadiga-execucao-coletar-base.md`

Trazer de volta:

Output completo, especialmente tabela/lista de sinais e referencias.

## Rodada 2 - RPE/RIR, tecnica e iniciantes

Dotflow recomendado: `.COLETAR_BASE`

Pergunta para colar:

```text
No treino de forca para adultos saudaveis/público geral, qual e a utilidade de RPE e RIR para ajustar intensidade durante a sessao, e quais sao suas limitacoes em iniciantes ou praticantes pouco experientes?

Inclua como cruzar RPE/RIR com qualidade tecnica e sinais observaveis de fadiga. Quero afirmacoes seguras, cautelas e referencias. Nao gere aula ou slides.
```

Salvar em:

`outputs/dotflow-02-rpe-rir-tecnica.md`

## Rodada 3 - Falha, proximidade da falha e fadiga

Dotflow recomendado: `.COMPARAR_CONCEITOS`

Pergunta para colar:

```text
Compare treinar ate a falha muscular versus treinar proximo da falha no treino de forca para adultos saudaveis/público geral.

Compare efeitos sobre força, hipertrofia, fadiga, qualidade tecnica, tolerancia e aplicabilidade para personal trainer. Quero conclusoes seguras, cautelas, limites da evidencia e referencias.
```

Salvar em:

`outputs/dotflow-03-falha-proximidade-fadiga.md`

## Rodada 4 - Ajustes agudos de intensidade

Dotflow recomendado: `.COLETAR_BASE`

Pergunta para colar:

```text
Quais variaveis podem ser manipuladas de forma aguda durante uma sessao de treino de forca para ajustar a intensidade ao aluno?

Considere peso, repeticoes, amplitude, ritmo, intervalo, execucao e variacao do exercicio. Quero fundamentos teoricos, aplicacoes praticas, cautelas e referencias. Nao inclua registro de treino como etapa central.
```

Salvar em:

`outputs/dotflow-04-ajustes-agudos.md`

## Rodada 5 - Lacunas especificas sobre sinais de fadiga

Dotflow recomendado: `.MAPEAR_LACUNAS`

Pergunta para colar:

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

## Rodada 6 - Removida neste projeto

A rodada `.RESUMIR_PARA_FONTE` nao sera usada neste projeto.

Motivo: as rodadas foram executadas em chats separados no OpenEvidence, entao o Dotflow nao tera acesso real ao conjunto completo de outputs. A consolidacao sera feita no Codex, a partir dos outputs brutos e auditorias salvos no projeto.

Arquivo substituto:

`fluxo padrão/07_fontes-e-evidencias.md`

## Prioridade pratica

Neste momento, as Rodadas 1 a 5 ja foram executadas e auditadas:

- Rodada 1: sinais de fadiga durante a execucao;
- Rodada 2: RPE/RIR, tecnica e iniciantes;
- Rodada 3: falha, proximidade da falha e fadiga;
- Rodada 4: ajustes agudos de intensidade;
- Rodada 5: lacunas sobre sinais visuais de fadiga sem equipamento.

Proxima acao: consolidar `fluxo padrão/07_fontes-e-evidencias.md` e preparar os prompts/diretrizes para NotebookLM.
