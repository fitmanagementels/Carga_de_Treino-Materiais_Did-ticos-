# Auditoria - NotebookLM 07 - Fonte mestre preliminar

Status: Aprovado como esqueleto, com ajustes moderados antes de validar.

## Produto avaliado

Output externo:

- `outputs/notebooklm-07-fonte-mestre-preliminar.md`

Prompt de origem:

- `prompts/notebooklm-sistema-e-fonte-mestre.md`
- Prompt 8 - Fonte mestre preliminar.

## Diagnostico

A fonte mestre preliminar esta bem estruturada e cobre os itens obrigatorios do prompt: objetivo, publico, escopo, principios, conceitos, sintese por bloco, matriz de decisao, sinais de fadiga, frases operacionais, checklists, cautelas, exclusoes e referencias por tema.

Ela serve como um bom esqueleto para a fonte mestre. Porem ainda nao deve ser considerada versao validada, porque algumas formulacoes voltaram a ficar absolutas ou tecnicas demais, e algumas referencias ficaram pouco rastreaveis.

## Pontos aproveitaveis

- Objetivo do material ficou claro e alinhado ao roteiro.
- Escopo manteve foco em ajuste agudo da intensidade durante a sessao.
- Fora de escopo preserva performance de elite, reabilitacao clinica, periodizacao complexa e registro/acompanhamento cronico.
- Principio da menor mudanca suficiente foi incorporado.
- Conceitos essenciais estao organizados de forma simples.
- Sintese por bloco esta curta e usavel para orientar produtos posteriores.
- Sinais visuais aparecem acompanhados de nota metodologica.
- Cautelas excluem 1RM, bioquimica, VBT como requisito, periodizacao e volumes cronicos.

## Ajustes obrigatorios

### 1. Status da fonte

O texto abre dizendo que e "documento de referencia final". Isso precisa ser corrigido.

Usar:

```text
Esta e uma fonte mestre preliminar para auditoria. Ela orienta a criacao futura de slides e ebook somente depois de revisada e validada.
```

### 2. Evitar criterios absolutos

Trechos como "resposta real do aluno no dia e o criterio final" e "tecnica e a prioridade" podem ficar absolutos demais.

Preferir:

```text
A resposta real do aluno no dia tem peso central na decisao.
```

```text
Quando relato e execucao entram em conflito, a qualidade da execucao deve pesar muito na decisao.
```

### 3. Corrigir a matriz de decisao

A matriz usa faixas fixas de RIR:

- RIR alto (>4-5);
- RIR 1-3.

Essas faixas podem virar regra rigida. Melhor usar linguagem de alvo aproximado:

```text
RIR claramente acima do alvo planejado
```

```text
esforco proximo do alvo planejado
```

Tambem trocar "velocidade cai bruscamente" por:

```text
execucao perde velocidade de forma evidente junto com perda de qualidade
```

### 4. Ajustar Bloco 6

Trocar:

```text
perda de controle e fluidez que sinalizam a necessidade de encerrar ou ajustar a serie
```

Por:

```text
pistas de perda de qualidade que indicam necessidade de revisar a demanda, podendo manter, ajustar, encerrar ou modificar conforme o contexto.
```

### 5. Ajustar sinais visuais

Trocar "Evidencia Indireta Plausivel (O que o olho ve)" por:

```text
Pistas visuais plausiveis, sem validacao direta como medida objetiva
```

Isso preserva a cautela metodologica.

### 6. Ajustar frases operacionais

Evitar frases automaticas:

- "vamos parar aqui";
- "a tecnica diz que o peso esta alto".

Preferir:

```text
Notei que a execucao comecou a mudar. Vamos ajustar para manter a qualidade.
```

```text
A tecnica esta dando sinais de queda; vou revisar a demanda para manter o objetivo da serie.
```

### 7. Ajustar checklist

Trocar:

```text
O aluno dormiu bem? Tem dor?
```

Por:

```text
Ha algum sinal de baixa prontidao, desconforto incomum ou mudanca relevante no estado do aluno hoje?
```

Isso evita interrogatorio e reduz puxada clinica.

### 8. Referencias rastreaveis

A secao de referencias esta curta demais e inclui "Helms et al." sem identificacao completa. A fonte mestre validada deve usar referencias completas ou remeter aos outputs brutos.

Regra:

- nao usar "Autor et al." sem ano, titulo ou origem;
- nao inventar referencia;
- quando a referencia estiver resumida, marcar como "ver output bruto correspondente".

## Riscos de desalinhamento

- Tratar a fonte preliminar como final.
- Transformar faixas de RIR em regra fixa para todos os exercicios.
- Fazer a matriz parecer algoritmo rigido.
- Fazer sinais visuais parecerem criterio diagnostico.
- Usar linguagem clinica em dor/desconforto.
- Deixar referencias vagas entrarem na fonte validada.

## Decisao

Aprovado como esqueleto.

Nao validar ainda como fonte mestre final.

Pode seguir para:

- Prompt 9 - Autocritica da fonte mestre.

## Adendo obrigatorio para o Prompt 9

Ao executar o Prompt 9, adicionar:

```text
Na autocritica, considere tambem estes pontos obrigatorios:

1. Corrija a abertura: a fonte mestre ainda e preliminar, nao final.
2. Remova faixas fixas de RIR como regra geral. Use "acima do alvo planejado" e "proximo do alvo planejado".
3. Suavize frases absolutas sobre tecnica e resposta do aluno. A qualidade da execucao deve ter peso importante na decisao, especialmente em conflito com o relato, mas evite "sempre" e "criterio final".
4. Preserve sinais visuais como pistas operacionais, nunca como criterios diagnosticos ou medicoes.
5. Evite frases automaticas como "vamos parar aqui" para toda queda de velocidade.
6. Troque perguntas sobre dor por linguagem de desconforto incomum ou mudanca relevante no estado do aluno, sem puxar para triagem clinica.
7. Refaça a secao de referencias com nomes completos, ano, tema e origem, ou indique "ver output bruto correspondente" quando nao houver referencia completa.
8. Garanta que registro de treino, periodizacao, performance, reabilitacao e hipertrofia avancada continuem fora do escopo.
```

## Proxima acao recomendada

Executar o Prompt 9 no NotebookLM com o adendo acima e salvar a resposta em:

- `outputs/notebooklm-08-autocritica-fonte-mestre.md`
