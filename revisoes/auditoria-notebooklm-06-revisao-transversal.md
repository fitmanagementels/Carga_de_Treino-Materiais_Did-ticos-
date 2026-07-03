# Auditoria - NotebookLM 06 - Revisao transversal

Status: Aprovado com ajustes moderados.

## Produto avaliado

Output externo:

- `outputs/notebooklm-06-revisao-transversal.md`

Prompt de origem:

- `prompts/notebooklm-sistema-e-fonte-mestre.md`
- Prompt 7 - Revisao transversal.

## Diagnostico

A revisao transversal e util e captou varias correcoes que ja apareciam nas auditorias anteriores: separar definicao de acao, evitar percentuais de 1RM, preservar sinais visuais como pistas, manter lacunas e evitar puxada para performance, hipertrofia ou fisiologia.

No entanto, algumas formulacoes precisam ser corrigidas antes de orientar a fonte mestre. O NotebookLM ainda usa tom absoluto em pontos importantes, especialmente sobre tecnica e iniciantes.

## Pontos aprovados

- Bloco 2 deve definir variaveis; Bloco 5 deve ensinar quando e como ajustar.
- Bloco 3 deve tratar prontidao/pre-serie; Bloco 6 deve tratar sinais durante a execucao.
- Remover percentuais de 1RM de exemplos praticos.
- Remover referencias a volume semanal/metas cronicas da fonte mestre.
- Manter a lacuna sobre quantificacao visual da perda de velocidade.
- Manter respiracao e hesitacao como pistas contextuais, nao marcadores validados.
- Reforcar que sinais visuais sao alertas/pistas, nao provas de fadiga.
- Reforcar comunicacao profissional como fechamento da competencia tecnica.

## Pontos que precisam de ajuste

- "Intensidade deve ser tratada exclusivamente pela triade peso na barra + esforco relatado + tecnica observada" esta incompleto. A fonte mestre deve incluir tambem contexto do aluno, proximidade da falha, fadiga e variaveis agudas como intervalo, ritmo, amplitude e variacao.
- "RPE 7 pode ser esforco maximo por falta de familiaridade com a dor muscular" deve ser reescrito. Melhor: iniciantes podem estimar mal esforco e RIR por falta de familiaridade com esforco, sensacoes corporais e proximidade da falha. Evitar centralizar "dor muscular".
- "Se a tecnica quebrar, a serie parou" e absoluto demais. Melhor: se a qualidade da execucao deixa de sustentar o objetivo da serie, o trainee deve considerar encerrar, reduzir demanda ou modificar a tarefa.
- "Sinais de falha intra-serie" deve virar "sinais de fadiga ou perda de qualidade durante a execucao", para nao transformar tudo em falha.
- "Notei que a velocidade caiu bastante" pode ser usado com cautela se vier junto de linguagem de pista. Nao precisa ser banido, mas deve evitar qualquer ideia de medicao precisa.

## Correcoes obrigatorias para o Prompt 8

Ao pedir a fonte mestre preliminar, adicionar ou respeitar estas regras:

```text
Ao montar a fonte mestre, incorpore a revisao transversal, mas corrija os pontos abaixo:

1. Nao trate intensidade apenas como peso + esforco relatado + tecnica. Inclua tambem contexto do aluno, proximidade da falha, fadiga e variaveis agudas como intervalo, ritmo, amplitude e variacao.
2. Nao diga que iniciante erra RPE/RIR por "dor muscular". Diga que iniciantes podem estimar mal esforco e repeticoes em reserva por baixa familiaridade com esforco, tecnica, sensacoes corporais e proximidade da falha.
3. Nao diga que "se a tecnica quebrar, a serie parou" como regra absoluta. Diga que, quando a qualidade da execucao deixa de sustentar o objetivo da serie, o trainee deve considerar encerrar, reduzir a demanda ou modificar a tarefa.
4. Troque "sinais de falha intra-serie" por "sinais de fadiga ou perda de qualidade durante a execucao".
5. Preserve sinais visuais como pistas operacionais, nunca como provas ou medidas objetivas.
```

## Decisao

Aprovado com ajustes moderados.

Pode seguir para:

- Prompt 8 - Fonte mestre preliminar.

## Proxima acao recomendada

Executar o Prompt 8 no NotebookLM com o adendo de correcoes obrigatorias acima e salvar a resposta em:

- `outputs/notebooklm-07-fonte-mestre-preliminar.md`
