# Estado do projeto: controle de carga no treino de forca

## Objetivo atual

Construir material didatico sobre controle de carga de treino no treino de forca, sob perspectiva de atuacao de personal trainer com publico geral.

## Publico do material

Estagiarios de Educacao Fisica em processo de formacao para atuarem como personal trainer. Neste projeto, eles serao chamados de trainees.

## Produtos finais previstos

- Apresentacao em slides.
- Ebook/apostila em formato de leitura, com potencial uso mobile.

## Ferramenta principal de producao

NotebookLM sera usado como principal ferramenta de construcao dos produtos finais.

## Etapa atual

12. Ebook interativo mobile-first em HTML.

Observacao: a apresentacao em slides esta em producao externa no NotebookLM. O conteudo textual canonico do ebook ja foi consolidado e agora esta sendo transformado em produto mobile interativo local.

## Decisoes ja assumidas

- O foco nao sera performance esportiva.
- O foco nao sera saude clinica ou reabilitacao.
- A abordagem sera pratica, aplicada ao cotidiano do personal trainer com publico geral.
- O processo de criacao podera ser feito em etapas, com prompts separados para diferentes partes do ebook e da apresentacao.
- A apresentacao tera duracao aproximada de 60 a 90 minutos.
- A profundidade sera intermediaria, com foco operacional para trainees atuando com alunos.
- O publico geral sera tratado de forma ampla; exemplos especificos poderao ser dados pelo professor durante a aula.
- O foco principal sera o controle da carga em uma sessao especifica e o ajuste agudo da intensidade do exercicio.
- Aspectos cronicos serao usados para dar contexto, mas nao serao o eixo principal.
- A base teorica sera organizada por curadoria hibrida: poucas fontes proprias, Open Evidence e consolidacao posterior em um RAG/fonte concisa.
- O ebook sera mobile-first, com capitulos medios, baixa densidade textual e mini checklists operacionais.
- A identidade didatica e de treinamento interno para estagiarios recem-chegados a equipe.
- A arquitetura logica foi validada sem nome formal para o metodo, para evitar excesso de termos novos para os trainees.
- A leitura de intensidade sera ensinada como combinacao pratica entre RPE/RIR, qualidade tecnica e sinais de fadiga.
- Casos e exemplos especificos serao inseridos oralmente pelo professor; o roteiro deve deixar pontos de entrada, mas nao depender de pratica guiada formal.
- O roteiro mestre foi validado com 8 blocos para 60 a 90 minutos.
- Registro foi removido da logica de ajuste agudo e nao sera trabalhado neste material neste momento.
- Sinais de fadiga durante a execucao ganharam bloco proprio no roteiro.
- A parte de frases modelo e frases a evitar foi mantida no bloco de comunicacao profissional.
- A Rodada 1 com `.COLETAR_BASE` sobre sinais de fadiga foi recebida e auditada.
- A Rodada 2 com `.COLETAR_BASE` sobre RPE/RIR, tecnica e iniciantes foi recebida e auditada.
- A Rodada 3 com `.COMPARAR_CONCEITOS` sobre falha, proximidade da falha e fadiga foi recebida e auditada.
- A Rodada 4 com `.COLETAR_BASE` sobre ajustes agudos de intensidade foi recebida e auditada.
- A Rodada 5 com `.MAPEAR_LACUNAS` sobre sinais visuais de fadiga sem equipamento foi recebida e auditada.
- A Rodada 6 com `.RESUMIR_PARA_FONTE` foi removida do fluxo deste projeto, porque as rodadas foram executadas em chats separados no OpenEvidence e nao ha contexto compartilhado para consolidacao automatica confiavel.
- `07_fontes-e-evidencias.md` passa a funcionar como mapa de contexto e hierarquia do projeto, nao como fonte mestre.
- A fonte mestre sera criada no NotebookLM a partir de roteiro, `07`, auditorias e outputs brutos, em etapas.
- Qualquer fonte mestre criada no NotebookLM deve voltar ao Codex para auditoria antes de orientar slides e ebook.
- A checagem de hierarquia do NotebookLM foi recebida, salva e aprovada para prosseguir.
- A sintese do NotebookLM para os Blocos 1 e 2 foi recebida, salva e aprovada com ajustes pequenos.
- A sintese do NotebookLM para os Blocos 3 e 4 foi recebida, salva e aprovada com ajustes pequenos.
- A sintese do NotebookLM para o Bloco 5 foi recebida, salva e aprovada com ajustes pequenos.
- A sintese do NotebookLM para o Bloco 6 foi recebida, salva e aprovada com ajustes moderados.
- A sintese do NotebookLM para os Blocos 7 e 8 foi recebida, salva e aprovada com ajustes pequenos.
- A revisao transversal do NotebookLM foi recebida, salva e aprovada com ajustes moderados.
- A fonte mestre preliminar do NotebookLM foi recebida, salva e aprovada como esqueleto, ainda nao validada como fonte mestre final.
- A autocritica da fonte mestre foi recebida, salva e aprovada como correcao intermediaria. Ela nao substitui a fonte mestre, mas autoriza uma rodada de fonte mestre revisada completa.
- A fonte mestre revisada do NotebookLM foi recebida, salva e aprovada com ajustes editoriais do Codex.
- A fonte mestre validada do projeto foi criada em `08_fonte-mestre-validada.md`.
- A diretriz de fontes para o NotebookLM de producao foi criada em `diretrizes/fontes-notebooklm-produtos.md`.
- O criterio de linguagem, densidade e nivel operacional foi criado em `diretrizes/criterios-linguagem-densidade-operacional.md`.
- O tema visual XSTEAM para materiais didaticos foi criado em `diretrizes/tema-visual-xsteam.md`.
- A diretriz da apresentacao em slides foi criada em `diretrizes/diretriz-apresentacao-slides.md`.
- A diretriz do ebook mobile-first foi criada em `diretrizes/diretriz-ebook-mobile-first.md`.
- Os documentos estruturantes `00` a `08` foram movidos da raiz para a pasta `fluxo padrão/`.
- Padrao de manutencao definido: ajustes em diretrizes, roteiros, formatacoes e prompts devem atualizar o proprio documento ativo, sem criar um novo arquivo para cada alteracao. Novos arquivos ficam reservados para novas categorias de artefato, outputs externos, auditorias ou produtos finais separados.
- Limpeza de redundancias realizada: criterios editoriais consolidados em `diretrizes/criterios-linguagem-densidade-operacional.md`; `diretrizes/00-indice-producao.md` e o criterio duplicado `diretrizes/criterios-linguagem-densidade-nivel-operacional.md` foram removidos; prompts antigos de OpenEvidence e fonte mestre foram movidos para `prompts/historico/`.
- A diretriz da apresentacao em slides foi refeita como contrato de producao para o NotebookLM: ela nao fixa o conteudo exato de cada slide, mas define campos obrigatorios, estrutura visual, organizacao dos elementos e regras de continuidade entre lotes.
- O prompt pack ativo `prompts/notebooklm-slides-producao.md` foi criado para gerar mapa geral, roteiro por lotes, apresentacao em partes e revisao final no NotebookLM.
- O prompt pack de slides foi corrigido para diferenciar Conversa e Studio do NotebookLM: a Conversa sera usada para mapa, roteiro e auditoria com memoria; o Studio recebera comandos unicos de geracao de artefato, com design lock XSTEAM e comandos separados para apresentacao unica ou partes 1/2/3.
- A secao de prompts da Conversa foi restaurada para a versao usada na conversa anterior do NotebookLM, preservando a sequencia antiga: confirmacao de hierarquia, mapa geral, roteiros dos lotes 1/2/3 e revisao transversal.
- O roteiro ativo para orientar o NotebookLM foi atualizado em `diretrizes/roteiro-apresentacao.md` para 27 slides, apos unir os pares 6+7, 11+12, 23+24 e 25+26, e remover o slide de escopo separado. O roteiro preserva os 8 blocos do roteiro mestre e mantem direcoes de elemento visual/organizacao visual para o Studio.
- O roteiro da apresentacao foi movido para `diretrizes/roteiro-apresentacao.md`, para ficar junto dos documentos-diretriz e evitar roteiro solto na pasta de produto.
- O roteiro ativo do ebook mobile-first foi criado em `diretrizes/roteiro-ebook-mobile-first.md`, seguindo a progressao dos 8 blocos e o padrao estrutural do roteiro da apresentacao.
- O prompt pack do ebook em `prompts/notebooklm-ebook-estrutura-e-capitulos.md` foi reformulado a partir de `diretrizes/roteiro-ebook-mobile-first.md`, com configuracao de sistema para o NotebookLM, checagem de hierarquia, mapa consolidado, producao por lotes de capitulos, capitulos 5 e 6 em rodadas proprias e revisao final.
- As respostas do NotebookLM aos Prompts 0 e 1 do ebook foram recebidas e salvas em `outputs/produtos-ebook/notebooklm-ebook-00-checagem-hierarquia.md` e `outputs/produtos-ebook/notebooklm-ebook-01-mapa-consolidado.md`.
- A auditoria do mapa consolidado foi criada em `revisoes/produtos/auditoria-ebook-00-mapa-consolidado.md`. O mapa foi aprovado com ajustes obrigatorios pequenos antes da escrita dos capitulos.
- O PDF textual do ebook foi recebido em `/home/elohimlima/Downloads/EBOOK_CONTEÚDO_CARGA_DE_TREINO.pdf`, extraido para `outputs/produtos-ebook/notebooklm-ebook-02-texto-completo-extraido.txt` e auditado em `revisoes/produtos/auditoria-ebook-09-texto-completo-pdf.md`.
- A revisao final do NotebookLM foi salva em `outputs/produtos-ebook/notebooklm-ebook-07-revisao-final.md`. O ebook esta aprovado como base textual, mas precisa de limpeza editorial antes da diagramacao final.
- O conteudo textual canonico do ebook foi criado em `outputs/ebook-conteudo.md`. A partir desta etapa, correcoes do conteudo do ebook devem atualizar esse unico arquivo, sem criar novas versoes paralelas.
- O ebook interativo mobile-first foi criado em `ebook/ebook-interativo-controle-carga.html`, usando `outputs/ebook-conteudo.md` como base canonica e mantendo `ebook/controle-carga-mobile.html` fora do fluxo atual.
- Revisao editorial de acentuacao, cedilha e escrita foi aplicada em `outputs/ebook-conteudo.md` e `ebook/ebook-interativo-controle-carga.html`, para adequar o texto ao padrao de produto entregue ao leitor.
- O ebook interativo foi atualizado com cards de explicação em pop-up/modal, checklist estático marcado por padrão, três perguntas por capítulo, menu customizado de capítulos, correção da navegação por índice, página final de síntese e capa com botões no final e mapa como navegação direta.
- `outputs/ebook-conteudo.md` recebeu uma seção de atualização da versão interativa HTML para preservar os novos aprofundamentos e regras sem criar documento paralelo.
- Bug de navegação no capítulo 5 diagnosticado e corrigido: o capítulo existia, mas não tinha bloco `observe`, o que quebrava a renderização ao avançar do capítulo 4. O capítulo 5 recebeu o bloco de observação e o renderizador passou a tolerar ausência desse bloco em capítulos futuros.
- A capa foi consolidada como capítulo inicial com instruções de uso do ebook, mantendo o mapa como navegação direta para capítulos e sem menu expansível na capa.
- O pop-up de explicação do ebook foi ajustado para caber melhor no padrão mobile sem barras internas de rolagem, e o menu expandido passou a incluir a opção `00 Introdução` para retorno à capa.
- O projeto foi consolidado para GitHub Pages com publicação pela pasta `/docs`: `docs/index.html` replica o ebook aprovado, `docs/.nojekyll` desativa Jekyll e `docs/README-publicacao-github-pages.md` documenta configuração, comandos e atualização. A pasta antiga de publicação Netlify foi removida para evitar duplicidade.
- O deck `slides/controle-carga-slides.html` ainda esta baseado na versao anterior de 32 slides e deve ser adaptado posteriormente ao roteiro ativo de 27 slides, caso continue sendo usado como produto HTML local.

## Proximo checkpoint

Auditar visualmente o ebook interativo em mobile e desktop estreito:

- confirmar leitura confortavel em tela pequena;
- confirmar navegacao por capitulos, progresso, checklists e quizzes;
- ajustar ritmo visual, espacamento e hierarquia se algum trecho ficar denso;
- decidir se havera uma versao exportavel/PDF derivada deste HTML.
