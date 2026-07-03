# Phase 02: NotebookLM Prompt Pack

This phase converts the validated source and Phase 01 direction documents into a structured set of prompts for NotebookLM. The goal is to make external generation repeatable, chunked by product and block, and easy to audit when the outputs return to the project.

## Tasks

- [x] Inspect the current prompt and direction context before writing new prompt files:
  - Completion note (2026-06-30): inspected the active prompt README, NotebookLM production/source hierarchy directions, slide and ebook product directions, language/density criteria, validated master source, and existing slide production prompt pack. Confirmed this phase should create copy-ready prompts for final product generation only, keep generation chunked by product/block/chapter, reuse the existing slide prompt-pack style, and avoid duplicating historic source-master creation prompts.
  - Read `prompts/README.md`, `diretrizes/notebooklm-fluxo-producao.md`, `diretrizes/fontes-notebooklm-produtos.md`, `diretrizes/diretriz-apresentacao-slides.md`, `diretrizes/diretriz-ebook-mobile-first.md`, `diretrizes/criterios-linguagem-densidade-operacional.md`, and `fluxo padrão/08_fonte-mestre-validada.md`.
  - Reuse the existing prompt style and do not duplicate prompts that already exist for source-master creation.
  - Treat this phase as prompt creation for final products, not as final product generation.

- [x] Create or maintain `prompts/notebooklm-slides-producao.md` as the slide production prompt pack:
  - Completion note (2026-06-29): created a single active slide prompt pack with setup prompt, map prompt, roteiro-by-lot prompts, final-presentation prompts in 10-15 slide parts, and final review prompt. The shared setup and slide review prompts are intentionally integrated into this one file to avoid scattering active prompts.
  - Require outputs to include slide title, visible slide text, visual element, layout, speaker note, caution, and source anchor.
  - Include slide-count guardrails for 60 to 90 minutes and continuity rules for multi-part generation.

- [x] Create `prompts/notebooklm-ebook-estrutura-e-capitulos.md` as the ebook production prompt pack:
  - Completion note (2026-06-30): created the active NotebookLM ebook prompt pack with required front matter, source hierarchy, one prompt for the full mobile-first ebook outline, and one reusable chapter-writing prompt template. The prompts require chapter goal, short sections, operational examples, mini checklist, communication phrases when relevant, recap, mobile-first formatting, no wide tables, and card/list alternatives for matrices.
  - Include YAML front matter with `type: reference`, `title: Prompt NotebookLM Ebook Estrutura e Capitulos`, `created` using the current local date, `tags: [notebooklm, ebook, mobile-first, prompts]`, and `related` wiki-links to `[[Diretriz Ebook Mobile First]]` and `[[Fonte Mestre Validada]]`.
  - Provide one prompt for the full ebook outline and one prompt template for writing each chapter separately.
  - Require outputs to include chapter goal, short sections, operational examples, mini checklist, communication phrases where relevant, and a short recap.
  - Require mobile-first formatting: short paragraphs, no wide tables, scannable headings, and card-style alternatives for matrices.

- [x] Create review/correction prompts only when needed:
  - Completion note (2026-06-30): confirmed slide review prompts already exist in `prompts/notebooklm-slides-producao.md`; added the needed ebook review/correction prompts directly to `prompts/notebooklm-ebook-estrutura-e-capitulos.md` to keep the active ebook workflow together. Added prompts for reviewing the ebook structure before chapter writing, reviewing/correcting each generated chapter, and reviewing the consolidated ebook before final assembly/diagramming.
  - Slide review prompts already live in `prompts/notebooklm-slides-producao.md`.
  - Ebook review prompts should be added to the future ebook prompt pack or to a separate review pack only if that becomes cleaner than keeping them with the ebook prompts.

- [x] Create output intake folders and index files for future external outputs:
  - Completion note (2026-06-30): created/updated the intake README files for NotebookLM product outputs and audits. Updated `outputs/produtos-slides/README.md` with structured front matter, source hierarchy, save sequence, raw-output header template, and audit routing. Created `outputs/produtos-ebook/README.md` with chapter-by-chapter intake instructions and mobile-first audit cautions. Created `revisoes/produtos/README.md` with audit naming conventions, product-specific checklists, review template, correction prompt area, and preservation rules. Added wiki-links among the three intake/review indexes and Phase 01 direction documents.
  - Create `outputs/produtos-slides/README.md` with front matter and instructions for saving NotebookLM slide outputs by block.
  - Create `outputs/produtos-ebook/README.md` with front matter and instructions for saving NotebookLM ebook outputs by chapter.
  - Create `revisoes/produtos/README.md` with front matter and instructions for audits of slide and ebook outputs.
  - Use wiki-links between the three README files and the Phase 01 direction documents.

- [x] Update `prompts/README.md` so the new product prompt files are discoverable:
  - Completion note (2026-06-30): added a concise product-generation prompt section that links both active NotebookLM product prompt packs. Updated the active-file list to include `prompts/notebooklm-ebook-estrutura-e-capitulos.md` and removed the stale "future ebook prompt pack" note while preserving the source-master/history guidance.
  - Add a concise section for product-generation prompts.
  - Link the active slide prompt pack and the future ebook prompt pack when created.
  - Preserve any existing README content and do not remove prior source-master prompt references.

- [x] Verify Phase 02 deliverables:
  - Completion note (2026-06-30): verified the active Phase 02 deliverables against the checklist. Confirmed `prompts/notebooklm-slides-producao.md` has 10 copy-ready NotebookLM prompts covering setup, map, three roteiro lots, three final slide parts, and final review; confirmed `prompts/notebooklm-ebook-estrutura-e-capitulos.md` has 5 copy-ready prompts covering structure, chapter-by-chapter writing, structure review, chapter correction, and consolidated review. Confirmed both packs enforce chunked generation and avoid uncontrolled full-product generation. Confirmed `outputs/produtos-slides/README.md`, `outputs/produtos-ebook/README.md`, and `revisoes/produtos/README.md` exist and explain output/audit routing. During verification, aligned ebook output filenames between the prompt pack and intake README, updated the NotebookLM source hierarchy to reference the active ebook prompt pack, and replaced stale "future prompt" wording in the NotebookLM flow direction. Confirmed active prompts preserve the validated source boundary: registro de treino remains outside the central acute-adjustment logic.
  - Confirm all new prompt files contain copy-ready prompts, not vague instructions to "ask NotebookLM".
  - Confirm the slide and ebook prompts generate products by structure/block/chapter, never the full final product in one uncontrolled response.
  - Confirm the intake folders and README files exist and explain where future outputs and audits should go.
  - Confirm no prompt contradicts `fluxo padrão/08_fonte-mestre-validada.md` or reintroduces registro as a central step of acute adjustment.
