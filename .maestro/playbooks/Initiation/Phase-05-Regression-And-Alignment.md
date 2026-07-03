# Phase 05: Regression and Alignment

This phase compares the slide deck and ebook against the validated source, roteiro, and direction documents. It exists to prevent polished drafts from becoming less accurate, less operational, or less aligned with the project scope.

## Tasks

- [ ] Inspect the current product drafts and control sources:
  - Read `fluxo padrão/08_fonte-mestre-validada.md`, `fluxo padrão/04_roteiro-mestre-rascunho.md`, `diretrizes/diretriz-apresentacao-slides.md`, `diretrizes/diretriz-ebook-mobile-first.md`, `diretrizes/criterios-linguagem-densidade-operacional.md`, `slides/roteiro-apresentacao.md`, `slides/controle-carga-slides.html`, `ebook/controle-carga-mobile.md`, and `ebook/controle-carga-mobile.html`.
  - Reuse findings from `revisoes/produtos/auditoria-slides-rascunho-01.md` and `revisoes/produtos/auditoria-ebook-rascunho-01.md`.
  - If any expected product draft is missing, recreate the missing draft from the validated source before continuing.

- [ ] Create `revisoes/produtos/matriz-cobertura-fonte-produtos.md` as a structured coverage matrix:
  - Include YAML front matter with `type: analysis`, `title: Matriz de Cobertura Fonte Produtos`, `created` using the current local date, `tags: [cobertura, regressao, slides, ebook]`, and `related` wiki-links to `[[Fonte Mestre Validada]]`, `[[Roteiro Apresentacao Controle de Carga]]`, and `[[Ebook Mobile Controle de Carga]]`.
  - Map each major section of `fluxo padrão/08_fonte-mestre-validada.md` to where it appears in the slides and ebook.
  - Mark each item as covered, partially covered, overemphasized, missing, or out of scope.
  - Pay special attention to the guiding question, acute decision matrix, fatigue signs, communication phrases, cautions, exclusions, and traceable references.

- [ ] Create `revisoes/produtos/relatorio-regressao-conteudo.md` as the regression report:
  - Include YAML front matter with `type: report`, `title: Relatorio de Regressao de Conteudo`, `created` using the current local date, `tags: [regressao, auditoria, controle-carga]`, and `related` wiki-links to `[[Matriz de Cobertura Fonte Produtos]]`, `[[Diretriz Apresentacao Slides]]`, and `[[Diretriz Ebook Mobile First]]`.
  - Identify content lost, oversimplified, distorted, duplicated, or introduced without source support.
  - Identify any language that sounds too uncertain, too clinical, too academic, too athlete-focused, or too generic.
  - Convert findings into specific correction instructions for the slide deck and ebook.

- [ ] Correct `slides/roteiro-apresentacao.md` and `slides/controle-carga-slides.html` using the coverage matrix and regression report:
  - Restore any missing core ideas from `fluxo padrão/08_fonte-mestre-validada.md`.
  - Remove or rewrite unsupported additions.
  - Improve operational decision language where the deck only states concepts without telling the trainee what to observe or do.
  - Keep slide bodies concise and move teaching detail into speaker-support notes.

- [ ] Correct `ebook/controle-carga-mobile.md` and `ebook/controle-carga-mobile.html` using the coverage matrix and regression report:
  - Restore any missing core ideas from `fluxo padrão/08_fonte-mestre-validada.md`.
  - Add or strengthen mini checklists where chapters are conceptual but not actionable.
  - Rewrite dense or academic paragraphs into mobile-friendly operational prose without losing rigor.
  - Preserve source traceability and avoid adding claims not supported by the validated project sources.

- [ ] Create `revisoes/produtos/auditoria-alinhamento-cruzado.md` as a final cross-product alignment audit:
  - Include YAML front matter with `type: analysis`, `title: Auditoria Alinhamento Cruzado`, `created` using the current local date, `tags: [slides, ebook, alinhamento, auditoria]`, and `related` wiki-links to `[[Relatorio de Regressao de Conteudo]]`, `[[Roteiro Apresentacao Controle de Carga]]`, and `[[Ebook Mobile Controle de Carga]]`.
  - Confirm the slide deck and ebook teach the same conceptual model, use compatible vocabulary, and preserve the same exclusions.
  - Note intentional differences between products: slides support live teaching; ebook supports independent study and consultation.
  - List any remaining issues that require user review rather than autonomous correction.

- [ ] Verify Phase 05 deliverables:
  - Confirm `revisoes/produtos/matriz-cobertura-fonte-produtos.md`, `revisoes/produtos/relatorio-regressao-conteudo.md`, and `revisoes/produtos/auditoria-alinhamento-cruzado.md` exist.
  - Confirm the slide and ebook files were corrected after the regression report, not merely audited.
  - Confirm all major inclusions and exclusions from `fluxo padrão/08_fonte-mestre-validada.md` are represented or explicitly marked out of scope.
  - Confirm no useful detailed content was replaced by a shorter generic version during corrections.
