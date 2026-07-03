---
type: analysis
title: Auditoria Ebook - Texto Completo PDF
created: 2026-07-03
tags:
  - revisoes
  - notebooklm
  - ebook
  - pdf
  - mobile-first
  - controle-carga
related:
  - '[[Intake Outputs NotebookLM Ebook]]'
  - '[[Fonte Mestre Validada]]'
  - '[[Roteiro Ebook Mobile First Controle de Carga]]'
  - '[[Diretriz Ebook Mobile First]]'
---

# Auditoria Ebook - Texto Completo PDF

## Produto avaliado

- PDF original enviado: `/home/elohimlima/Downloads/EBOOK_CONTEÚDO_CARGA_DE_TREINO.pdf`
- Texto extraido: `outputs/produtos-ebook/notebooklm-ebook-02-texto-completo-extraido.txt`
- Revisao do NotebookLM: `outputs/produtos-ebook/notebooklm-ebook-07-revisao-final.md`

## Base de comparacao

- `fluxo padrão/08_fonte-mestre-validada.md`
- `fluxo padrão/04_roteiro-mestre-rascunho.md`
- `diretrizes/roteiro-ebook-mobile-first.md`
- `diretrizes/diretriz-ebook-mobile-first.md`
- `diretrizes/criterios-linguagem-densidade-operacional.md`
- `diretrizes/tema-visual-xsteam.md`

## Diagnostico geral

O ebook esta **aprovado como base textual**, mas ainda nao esta pronto para PDF final. A progressao dos 8 capitulos foi preservada, o foco operacional esta claro e o conteudo nao desviou para performance, reabilitacao ou periodizacao. O problema principal agora e editorial: o texto ainda carrega marcas de resposta do NotebookLM, notas de producao visiveis ao leitor e algumas expressoes que sugerem medicao/precisao maior do que queremos ensinar.

Decisao: **aprovado com ajustes editoriais obrigatorios antes da diagramacao final**.

## Pontos aprovados

- Os 8 capitulos estao presentes e seguem a progressao planejada.
- O foco em ajuste agudo durante a sessao foi mantido.
- A logica "ficha orienta, sessao calibra" esta bem estabelecida.
- RPE/RIR foram tratados como ferramentas de conversa e calibragem.
- O capitulo de fadiga usa a cautela "nao somos sensores de precisao".
- O capitulo 7 usa a estrutura profissional observacao -> motivo -> acao.
- O capitulo 8 fecha com checklist e pergunta-guia.

## Ajustes obrigatorios

### 1. Remover texto de bastidor do NotebookLM

Problema: o PDF ainda contem frases de producao, como:

- "Com base na hierarquia de fontes..."
- "Aqui estao os Capitulos 3 e 4..."
- "Conforme o mapa de producao..."

Acao: remover todas as frases que revelam que o texto foi gerado por rodada de IA. O ebook deve comecar direto na abertura do material e seguir pelos capitulos.

### 2. Remover ou separar "Nota de producao"

Problema: todos os capitulos terminam com "Nota de producao". Isso e util para diagramacao, mas nao deve aparecer no ebook final entregue ao trainee.

Acao: mover as notas de producao para um documento interno de diagramacao ou converter em orientacao visual fora do corpo do ebook. No PDF final do aluno, cada capitulo deve terminar no recapitulo ou em um bloco de revisao.

### 3. Suavizar linguagem de medicao e precisao

Problema: ainda aparecem formulacoes como "termometro", "ajustar com precisao", "velocidade cai", "velocidade constante" e "reduz 10% do peso". Isso pode sugerir um grau de medicao que nao queremos ensinar.

Acao recomendada:

- trocar "termometro" por "ferramenta de leitura";
- trocar "ajustar com precisao" por "ajustar com criterio";
- trocar "velocidade cai" por "ritmo e fluidez mudam";
- trocar "reduz 10% do peso" por "reduz um pouco a carga" ou "reduz a carga de forma proporcional";
- manter "lentidao evidente" apenas como pista visual, sem quantificacao.

### 4. Corrigir tom de performance no Capitulo 6

Problema: a frase "personal trainer de elite" puxa o texto para performance/status, fora do foco de publico geral.

Acao: trocar por "personal trainer atento", "personal trainer profissional" ou "personal trainer bem treinado".

### 5. Ajustar o Capitulo 5 para formato mobile

Problema: a secao "Para MANTER / PROGREDIR / REDUZIR..." aparece como lista unica longa. Para o ebook mobile-first, isso deve virar cards individuais.

Acao: reformatar como **Cards de Acao**:

- Card Manter
- Card Progredir
- Card Reduzir
- Card Recuperar
- Card Simplificar
- Card Modificar

Cada card deve ter: "Quando aparece", "Ajuste possivel" e "Cautela".

### 6. Evitar regra absoluta demais sobre tecnica

Problema: a revisao do NotebookLM sugeriu "a tecnica sempre decide o ajuste". A intencao e correta, mas a frase pode virar automatismo.

Acao: usar formulacao mais alinhada ao projeto:

```text
Quando relato e tecnica apontam direcoes diferentes, reabra a decisao. A qualidade tecnica deve ter prioridade quando a seguranca ou o objetivo da serie estiverem comprometidos.
```

### 7. Limpar excesso de marcas formais

Problema: varios itens aparecem com pontuacao estranha herdada da conversao/exportacao, como pergunta seguida de ponto: `?.`

Acao: revisar pontuacao final de checklists e frases para leitura fluida.

## Ajustes por capitulo

### Capitulo 1

- Adicionar ao checklist uma pergunta sobre postura do treinador:
  - `[ ] Estou pronto para ajustar se o aquecimento contrariar a ficha?`
- Trocar "risco desnecessario" por "perda de qualidade tecnica" quando o foco for apenas ajuste de intensidade, evitando tom alarmista.

### Capitulo 2

- Encurtar a explicacao de carga interna para evitar fisiologia.
- Manter ritmo e amplitude como botoes de ajuste no mesmo nivel do peso.
- Trocar "velocidade constante" por "ritmo consistente".

### Capitulo 3

- Esta bem alinhado.
- Manter a cautela de que sono, energia e rotina recente servem para ajustar o treino, nao para diagnostico.
- Trocar "laboratorio de testes" por "ferramenta de validacao tecnica", se quiser tom mais profissional.

### Capitulo 4

- Trocar a abertura com "termometro" por "ferramenta de leitura".
- Trocar "ajustar com precisao" por "ajustar com criterio".
- Ajustar a conclusao para evitar automatismo: tecnica nao "cala" o aluno; ela orienta a decisao quando o relato nao combina com a execucao.

### Capitulo 5

- Reformatar decisao em cards.
- Trocar "cirurgia" por "decisao proporcional" ou manter apenas se o tom desejado for mais marcante.
- Trocar "velocidade cai drasticamente" por "ritmo e fluidez caem de forma evidente".
- Trocar "reduzir 10%" por "reduzir um pouco a carga".

### Capitulo 6

- Trocar "personal trainer de elite" por "personal trainer atento".
- Manter "nao somos sensores de precisao".
- Trocar "medir a perda de velocidade" por "identificar perda de fluidez ou lentidao evidente".
- Trocar "como voce sentiu o esforco para manter essa velocidade?" por "como voce sentiu o esforco para manter esse ritmo?".

### Capitulo 7

- Esta bem encaminhado.
- Trocar "velocidade do movimento caiu" por "ritmo do movimento mudou".
- A frase profissional deve soar como decisao tecnica, nao sugestao.

### Capitulo 8

- Remover percentual de 10%.
- Trocar "velocidade cai" por "fluidez cai".
- Encerrar com a pergunta-guia em destaque:
  - **O que esta acontecendo agora e qual e a menor mudanca suficiente?**
- Trocar "ajuste com precisao" por "ajuste com criterio".

## Prompt de correcao recomendado

Usar no NotebookLM ou em outro editor com o texto completo do ebook:

```text
Corrija o texto completo do ebook mobile-first "Ajuste de Carga na Pratica: O Guia de Decisao do Personal Trainer".

Nao reestruture os 8 capitulos. Preserve a progressao, a ordem, os exemplos principais, o foco operacional e a linguagem de capacitacao interna.

Tarefa:
Gere uma versao limpa e pronta para diagramacao textual, corrigindo apenas os pontos abaixo.

Correcoes obrigatorias:
1. Remova todas as frases de bastidor do NotebookLM, como "Com base na hierarquia...", "Aqui estao os capitulos..." e "Conforme o mapa de producao...".
2. Remova a secao "Nota de producao" do corpo final do ebook. Se houver orientacao visual util, mova para uma secao separada ao final chamada "Notas internas para diagramacao" ou simplesmente omita do texto do aluno.
3. Troque linguagem de medicao/precisao por linguagem de julgamento operacional:
   - "termometro" -> "ferramenta de leitura";
   - "ajustar com precisao" -> "ajustar com criterio";
   - "velocidade cai" -> "ritmo e fluidez mudam";
   - "reduzir 10%" -> "reduzir um pouco a carga" ou "reduzir a carga de forma proporcional".
4. No Capitulo 6, troque "personal trainer de elite" por "personal trainer atento" ou "personal trainer profissional".
5. No Capitulo 5, transforme a lista de decisoes em Cards de Acao individuais: Manter, Progredir, Reduzir, Recuperar, Simplificar e Modificar. Cada card deve ter "Quando aparece", "Ajuste possivel" e "Cautela".
6. Evite a regra absoluta "a tecnica sempre decide". Use: "Quando relato e tecnica apontam direcoes diferentes, reabra a decisao. A qualidade tecnica deve ter prioridade quando a seguranca ou o objetivo da serie estiverem comprometidos."
7. Revise pontuacao estranha dos checklists, removendo finais como "?."
8. No Capitulo 8, encerre obrigatoriamente com a pergunta-guia em destaque: "O que esta acontecendo agora e qual e a menor mudanca suficiente?"

Regras:
- Nao acrescente fisiologia profunda.
- Nao puxe para performance esportiva, reabilitacao clinica ou periodizacao complexa.
- Nao reintroduza registro de treino como etapa central.
- Nao transforme RPE/RIR ou sinais visuais em comandos automaticos.
- Preserve leitura mobile-first, com paragrafos curtos, secoes escaneaveis e checklists.

Entregue:
1. texto completo revisado do ebook;
2. lista curta das correcoes aplicadas;
3. aviso se algum ponto nao puder ser corrigido sem reescrever demais.
```

## Proxima acao

Rodar o prompt de correcao acima para gerar uma versao textual limpa. Depois disso, auditar rapidamente apenas:

- se as frases de bastidor sumiram;
- se as notas de producao sairam do corpo do aluno;
- se a linguagem de medicao foi suavizada;
- se o capitulo 5 virou cards;
- se o fechamento traz a pergunta-guia.
