# Phase 06: Final Package and QA

This phase prepares the slide deck, mobile ebook, and supporting documentation for review, export, and handoff. It does not add new theory; it stabilizes the materials, verifies renderability, and creates a clear final package index for the project.

## Tasks

- [ ] Inspect the corrected product set and final audit context:
  - Read `slides/controle-carga-slides.html`, `slides/roteiro-apresentacao.md`, `ebook/controle-carga-mobile.html`, `ebook/controle-carga-mobile.md`, `revisoes/produtos/auditoria-alinhamento-cruzado.md`, `revisoes/produtos/relatorio-regressao-conteudo.md`, `diretrizes/fontes-notebooklm-produtos.md`, and `diretrizes/README.md`.
  - Confirm this phase is packaging and QA only; do not introduce new conceptual claims unless they restore missing validated source content.

- [ ] Create `entregaveis/README.md` as the final package index:
  - Include YAML front matter with `type: reference`, `title: Indice de Entregaveis`, `created` using the current local date, `tags: [entregaveis, slides, ebook, controle-carga]`, and `related` wiki-links to `[[Roteiro Apresentacao Controle de Carga]]`, `[[Ebook Mobile Controle de Carga]]`, and `[[Auditoria Alinhamento Cruzado]]`.
  - List the current deliverables with paths: slide HTML, slide storyboard, ebook HTML, ebook Markdown, direction documents, prompt packs, and audits.
  - Explain which files are for teaching, which are for reading, which are for production traceability, and which are for future NotebookLM rounds.

- [ ] Create export-ready copies in `entregaveis/`:
  - Copy or regenerate the current slide deck as `entregaveis/slides-controle-carga.html`.
  - Copy or regenerate the current ebook HTML as `entregaveis/ebook-controle-carga-mobile.html`.
  - Copy or regenerate the current ebook Markdown as `entregaveis/ebook-controle-carga-mobile.md`.
  - Ensure copied files remain self-contained or use only relative local references that exist in the project.

- [ ] Add print and review affordances to the deliverable HTML files:
  - Ensure `entregaveis/slides-controle-carga.html` has print styles that separate slide sections cleanly.
  - Ensure `entregaveis/ebook-controle-carga-mobile.html` has print styles that hide navigation clutter and keep chapters readable.
  - Add a small unobtrusive metadata footer to each deliverable with project title, draft status, and source basis.
  - Do not add decorative elements that reduce readability or make the material feel like a marketing page.

- [ ] Create `revisoes/produtos/checklist-final-qa.md` as the final QA checklist:
  - Include YAML front matter with `type: report`, `title: Checklist Final QA`, `created` using the current local date, `tags: [qa, entregaveis, revisao-final]`, and `related` wiki-links to `[[Indice de Entregaveis]]`, `[[Fonte Mestre Validada]]`, and `[[Auditoria Alinhamento Cruzado]]`.
  - Check renderability, source alignment, scope exclusions, 8-block coverage, mobile readability, slide readability, communication tone, and export readiness.
  - Include a short "aprovado para revisao humana" or "bloqueado por pendencias" status with concrete reasons.

- [ ] Perform final corrections from the QA checklist:
  - If the checklist finds render or readability problems, fix the deliverable HTML and the source product files.
  - If the checklist finds scope drift, correct the slide or ebook text and note the correction in the checklist.
  - If the checklist finds missing core content from `fluxo padrão/08_fonte-mestre-validada.md`, restore it in the appropriate product without making the material denser than necessary.
  - If an issue genuinely requires user preference rather than autonomous correction, mark it clearly as a review question in `revisoes/produtos/checklist-final-qa.md`.

- [ ] Verify Phase 06 deliverables:
  - Confirm `entregaveis/README.md`, `entregaveis/slides-controle-carga.html`, `entregaveis/ebook-controle-carga-mobile.html`, `entregaveis/ebook-controle-carga-mobile.md`, and `revisoes/produtos/checklist-final-qa.md` exist.
  - Open or inspect both deliverable HTML files and confirm they render without a build step.
  - Confirm the deliverables still match the corrected source files in `slides/` and `ebook/`.
  - Confirm the final package index tells a future reviewer exactly which files to open first.
