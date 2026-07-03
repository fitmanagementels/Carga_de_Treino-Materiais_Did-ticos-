# Auditoria - NotebookLM 04 - Fonte Bloco 6

Status: Aprovado com ajustes moderados.

## Produto avaliado

Output externo:

- `outputs/notebooklm-04-fonte-bloco-6.md`

Prompt de origem:

- `prompts/notebooklm-sistema-e-fonte-mestre.md`
- Prompt 5 - Bloco 6.

## Diagnostico

A resposta captou a principal cautela metodologica do Bloco 6: sinais visuais devem ser tratados como pistas operacionais, nao como medidas objetivas. A classificacao por nivel de confianca esta bem alinhada ao fluxo de evidencias.

No entanto, este output precisa de ajustes moderados antes de entrar na fonte mestre, porque algumas frases ainda soam fortes demais para um bloco cuja principal funcao e ensinar observacao com cautela.

## Pontos aproveitaveis

- Sinais visuais como pistas operacionais, nao medicoes objetivas.
- Reducao de velocidade como indicador mais sustentado quando medida instrumentalmente.
- Visualmente, tratar velocidade como "lentidao evidente", nao como percentual.
- Separacao entre:
  - evidencia direta/instrumental;
  - evidencia indireta plausivel;
  - sinais uteis pedagogicamente;
  - sinais que nao devem virar afirmacao forte.
- Perguntas para guiar o olhar do trainee: velocidade, fluidez, amplitude, estabilidade e controle.
- Cautela de que em iniciantes a perda de tecnica pode refletir aprendizado motor, nao fadiga extrema.
- Frases a evitar estao bem calibradas e preservam a cautela metodologica.

## Usar com cautela ou ajustar

- "O que diferencia o personal trainer de um mero passador de treinos" e forte e pode soar julgador. Melhor: "ler a execucao e uma competencia central do personal trainer".
- "Qualidade tecnica observada e o criterio final para seguranca e eficacia" deve ser suavizado. Melhor: "qualidade tecnica observada deve ter peso importante na decisao, especialmente quando entra em conflito com o relato".
- "Perda de tecnica, compensacoes e encurtamento de amplitude indicam incapacidade de manter o padrao motor sob estresse" pode ser forte demais. Em iniciantes, tambem pode ser falta de aprendizado, inseguranca ou tarefa mal compreendida.
- "Perda de velocidade correlaciona-se fortemente com aumento do estresse metabolico, como lactato" nao deve entrar no material final; e tecnico, desnecessario e pode puxar para bioquimica que o proprio output manda evitar.
- "A fadiga se manifesta progressivamente atraves de alteracoes mecanicas e perceptivas mensuraveis" deve virar: "a fadiga pode aparecer como mudancas na execucao e na percepcao de esforco".
- "Vamos encerrar por aqui" pode ser adequado em algumas situacoes, mas nao deve aparecer como resposta automatica a toda queda de velocidade. Melhor: "vamos ajustar a proxima repeticao/serie" ou "vamos parar aqui se a qualidade cair mais".
- "O peso esta alto para hoje" e bom, mas deve manter abertura para tecnica, fadiga, inseguranca ou complexidade da tarefa.

## Riscos de desalinhamento

- Transformar sinais visuais em criterios diagnosticos.
- Dar a entender que toda queda de velocidade exige encerrar a serie.
- Fazer o trainee confundir fadiga com falta de aprendizagem tecnica.
- Reintroduzir bioquimica da fadiga no bloco.
- Tratar qualidade tecnica como criterio absoluto sem considerar objetivo, exercicio e grau da alteracao.

## Correcoes recomendadas para a fonte mestre

Formula central:

```text
Sinais visuais nao medem fadiga com precisao. Eles funcionam como pistas para o trainee revisar se a demanda ainda combina com a qualidade da execucao e com o objetivo da serie.
```

Classificacao recomendada:

| Nivel | Sinais | Como ensinar |
| --- | --- | --- |
| Mais sustentado quando medido objetivamente | reducao de velocidade | visualmente, tratar como lentidao evidente, nao percentual |
| Plausivel e operacional | perda de fluidez, encurtamento de amplitude, compensacoes, instabilidade, perda de controle | sinais de alerta para revisar a demanda |
| Contextual | respiracao desorganizada, hesitacao, expressao de esforco, queda de tolerancia | nao decide sozinho; usar junto com execucao, relato e contexto |
| Cuidado maximo | conflito relato-execucao | investigar sem desautorizar o aluno e ajustar com profissionalismo |

Perguntas preferidas:

- A repeticao ficou claramente mais lenta?
- O movimento perdeu fluidez?
- A amplitude encurtou sem intencao?
- A posicao ou estabilidade se perderam?
- Surgiram compensacoes que nao apareciam no inicio?
- A fase de descida ainda esta controlada?
- O que o aluno relata combina com a execucao que eu estou vendo?

Frases preferidas:

- "Notei que a velocidade caiu e a execucao comecou a mudar. Vamos ajustar para manter qualidade."
- "O movimento perdeu fluidez; isso e uma pista de que a demanda ja esta chegando perto do alvo."
- "A tecnica esta dando sinais de queda. Vou ajustar a demanda para manter o objetivo da serie."

Evitar:

- "criterio final" como regra absoluta;
- explicacoes sobre lactato, CK, amonia ou EMG;
- qualquer percentual visual de perda de velocidade;
- transformar hesitacao, respiracao ou expressao facial em prova de fadiga.

## Decisao

Aprovado com ajustes moderados.

Pode seguir para:

- Prompt 6 - Blocos 7 e 8.

## Proxima acao recomendada

Executar o Prompt 6 no NotebookLM e salvar a resposta em:

- `outputs/notebooklm-05-fonte-blocos-7-8.md`
