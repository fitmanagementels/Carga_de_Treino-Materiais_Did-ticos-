---
type: analysis
title: Auditoria Ebook - Mapa Consolidado
created: 2026-07-03
tags:
  - revisoes
  - notebooklm
  - ebook
  - mobile-first
  - controle-carga
related:
  - '[[Intake Outputs NotebookLM Ebook]]'
  - '[[Fonte Mestre Validada]]'
  - '[[Roteiro Ebook Mobile First Controle de Carga]]'
  - '[[Diretriz Ebook Mobile First]]'
---

# Auditoria Ebook - Mapa Consolidado

## Produto avaliado

- `outputs/produtos-ebook/notebooklm-ebook-00-checagem-hierarquia.md`
- `outputs/produtos-ebook/notebooklm-ebook-01-mapa-consolidado.md`

## Base de comparacao

- `fluxo padrão/08_fonte-mestre-validada.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `diretrizes/roteiro-ebook-mobile-first.md`
- `diretrizes/diretriz-ebook-mobile-first.md`
- `diretrizes/criterios-linguagem-densidade-operacional.md`
- `diretrizes/fontes-notebooklm-produtos.md`

## Diagnostico geral

O output esta adequado como mapa inicial do ebook. Ele preserva os 8 capitulos, mantem o foco no ajuste agudo da sessao e respeita a logica mobile-first. Ainda assim, precisa de pequenos ajustes antes de liberar a escrita dos capitulos, porque algumas palavras e escolhas de formato podem puxar o material para clinica, medicao objetiva ou tabela larga.

Decisao: **aprovado com ajustes obrigatorios pequenos**. Corrigir o mapa no NotebookLM antes de pedir os capitulos 1 e 2.

## Pontos aprovados

- A progressao em 8 capitulos foi preservada.
- O foco em ajuste agudo durante a sessao foi mantido.
- RPE/RIR aparecem como ferramentas de conversa e calibragem.
- Sinais visuais foram tratados majoritariamente como pistas, nao como medidas.
- A comunicacao profissional entrou como capitulo proprio.
- O mapa preve checklists, cards, boxes e matrizes mobile.

## Ajustes obrigatorios

1. **Remover linguagem clinica no Capitulo 6.**
   - Problema: o titulo "O Olhar Clinico" puxa o material para um enquadramento clinico, que esta fora do escopo.
   - Ajuste: usar "O olhar tecnico", "Sinais de fadiga durante a execucao" ou "Para onde olhar durante a serie".

2. **Corrigir higiene de fontes no Prompt 0.**
   - Problema: o output menciona "auditorias" como fontes secundarias. Para o notebook de producao, as auditorias nao devem comandar o produto.
   - Ajuste: fontes secundarias devem ser os outputs brutos/dotflows e `07_fontes-e-evidencias.md`, apenas como apoio teorico e rastreabilidade.

3. **Evitar formato de tabela larga no Capitulo 5.**
   - Problema: o mapa fala em "Tabela 'Se voce observar X -> Decisao provavel Y'".
   - Ajuste: trocar para cards empilhados ou matriz mobile em blocos curtos.

4. **Suavizar linguagem de medicao no Capitulo 4.**
   - Problema: "O Termometro do Treino" pode sugerir medicao precisa.
   - Ajuste: usar "Ferramentas de leitura" ou "RPE, RIR e tecnica na pratica".

5. **Trocar "dores" por "desconforto incomum" no Capitulo 3.**
   - Problema: "dores" pode aproximar o material de triagem clinica.
   - Ajuste: manter "desconforto incomum" e reforcar que nao e diagnostico.

6. **Evitar frase forte demais sobre tecnica no Capitulo 4.**
   - Problema: "se a tecnica contradiz o relato, priorize a seguranca tecnica" esta boa em intencao, mas pode soar como regra automatica.
   - Ajuste: "quando tecnica e relato apontam direcoes diferentes, reabra a decisao e use a qualidade tecnica como criterio central de seguranca".

7. **Ajustar frase do Capitulo 5 sobre velocidade.**
   - Problema: "Notei que a velocidade caiu" pode soar muito medido.
   - Ajuste: preferir "Notei que o ritmo e a fluidez mudaram".

## Lacunas toleraveis

- Os titulos dos capitulos mudaram em relacao ao roteiro canônico. Isso e aceitavel se os ajustes acima forem feitos e a funcao de cada capitulo for preservada.
- O exemplo do agachamento no Capitulo 6 pode ficar, desde que seja apresentado como exemplo pedagogico e nao como regra universal.
- "Variabilidade biologica" pode aparecer se for explicado em linguagem simples, mas "variacao do dia" e mais operacional.

## Prompt de correcao recomendado

Usar no NotebookLM antes de pedir os capitulos finais:

```text
Corrija apenas o mapa consolidado do ebook que voce acabou de produzir. Nao escreva os capitulos finais ainda.

Preserve a estrutura de 8 capitulos e mantenha tudo que estiver alinhado. Corrija somente os pontos abaixo:

1. No Capitulo 6, remova o titulo "O Olhar Clinico". Use um titulo operacional, como "Sinais de fadiga durante a execucao", "Para onde olhar durante a serie" ou "O olhar tecnico para a fadiga".
2. Na hierarquia de fontes, nao trate auditorias como fontes secundarias do notebook de producao. As fontes secundarias devem ser `fluxo padrão/07_fontes-e-evidencias.md` e os outputs brutos/dotflows, apenas como apoio teorico e rastreabilidade.
3. No Capitulo 5, nao use "tabela" como formato principal. Troque por cards empilhados ou matriz mobile em blocos curtos.
4. No Capitulo 4, evite o titulo "O Termometro do Treino", porque pode sugerir medicao precisa. Use um titulo mais operacional, como "RPE, RIR e tecnica na pratica" ou "Ferramentas de leitura da intensidade".
5. No Capitulo 3, troque "dores" por "desconforto incomum" e preserve a cautela de nao transformar isso em diagnostico clinico.
6. No Capitulo 4, troque a frase "se a tecnica contradiz o relato, priorize a seguranca tecnica" por uma formulacao menos automatica: "quando tecnica e relato apontam direcoes diferentes, reabra a decisao e use a qualidade tecnica como criterio central de seguranca".
7. No Capitulo 5, troque frases como "notei que a velocidade caiu" por "notei que o ritmo e a fluidez mudaram", para evitar linguagem de medicao objetiva a olho nu.

Entregue:
- lista curta do que foi corrigido;
- versao corrigida apenas dos capitulos/trechos afetados;
- confirmacao de que os 8 capitulos, o foco no ajuste agudo e o formato mobile-first foram preservados.
```

## Proxima acao

Rodar o prompt de correcao acima no NotebookLM. Se a resposta corrigida vier alinhada, liberar o Prompt 2 para producao dos capitulos 1 e 2.
