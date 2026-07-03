# Phase 03: Slide Draft

This phase assembles a first working slide deck from the validated source, direction documents, and any available NotebookLM slide outputs. If NotebookLM outputs are not present yet, the agent must still produce a clearly labeled local draft grounded in the validated source so the project keeps moving and can be reviewed.

## Tasks

- [x] Inspect slide inputs and decide the source mode without asking the user:
  - Read `fluxo padrão/08_fonte-mestre-validada.md`, `fluxo padrão/04_roteiro-mestre-rascunho.md`, `diretrizes/diretriz-apresentacao-slides.md`, `diretrizes/criterios-linguagem-densidade-operacional.md`, and `prompts/notebooklm-slides-producao.md`.
  - Check whether `outputs/produtos-slides/` contains NotebookLM slide structure or block outputs.
  - If NotebookLM slide outputs exist, use them as the first source and correct them against `fluxo padrão/08_fonte-mestre-validada.md`.
  - If NotebookLM slide outputs do not exist, create a local draft from `fluxo padrão/08_fonte-mestre-validada.md` and label the audit status as "rascunho local aguardando rodada NotebookLM".
  - Completion note 2026-06-30: required inputs were inspected. `outputs/produtos-slides/` currently contains only `README.md`, so there are no NotebookLM slide structure or block outputs to use as first source. Source mode for the next slide-draft tasks is **local draft from `fluxo padrão/08_fonte-mestre-validada.md`**, with audit status **"rascunho local aguardando rodada NotebookLM"**.

- [x] Create `slides/roteiro-apresentacao.md` as a structured Markdown slide storyboard:
  - Include YAML front matter with `type: reference`, `title: Roteiro Apresentacao Controle de Carga`, `created` using the current local date, `tags: [slides, storyboard, controle-carga]`, and `related` wiki-links to `[[Diretriz Apresentacao Slides]]`, `[[Fonte Mestre Validada]]`, and `[[Roteiro Mestre]]`.
  - Organize the deck into the same 8 blocks from the master roteiro.
  - For each slide, include: slide number, title, objective, on-slide content, speaker-support note, and source anchor.
  - Keep the deck in the 60 to 90 minute training range and avoid dense text slides.
  - Completion note 2026-06-30: created `slides/roteiro-apresentacao.md` as a local 32-slide storyboard, marked with status **"rascunho local aguardando rodada NotebookLM"**. The file includes the requested YAML front matter, wiki-link relationships, all 8 master roteiro blocks, per-slide objective/content/speaker/source fields, and a 60 to 90 minute timing map with low-density slide text.

- [x] Create `slides/controle-carga-slides.html` as a dependency-free working slide deck:
  - Use semantic HTML, inline or local CSS, and no external build step.
  - Include a title slide, one or more slides for each of the 8 roteiro blocks, a decision-matrix slide, a fatigue-signs slide, a communication phrases slide, and a final synthesis slide.
  - Include speaker notes in a collapsible or visually secondary area so the file can support live teaching and review.
  - Make the deck readable on desktop and printable, with one slide-like section per screen/page.
  - Use restrained visual design appropriate for internal professional training, not a marketing landing page.
  - Completion note 2026-06-30: created `slides/controle-carga-slides.html` as a self-contained 32-slide HTML deck grounded in `slides/roteiro-apresentacao.md`, the slide directions, and the available NotebookLM slide-output chat as supplemental review context. The deck uses semantic slide sections, inline CSS, no external build step, XSTEAM-inspired restrained visual structures, secondary speaker notes, desktop/mobile responsive layout, and print page breaks. It includes the required title, eight-block coverage, decision matrix, fatigue-signs, communication phrases, and final synthesis slides.

- [x] Encode the core teaching logic explicitly in the slide deck:
  - Show that controlling load is not only choosing weight.
  - Contrast carga externa and carga interna/resposta.
  - Present RPE/RIR as practical conversation and calibration tools, not precise standalone measures.
  - Show how technique quality and fatigue signs can override or reframe the student's self-report.
  - Teach the principle of the "menor mudanca suficiente" for acute adjustment.
  - Completion note 2026-06-30: updated `slides/controle-carga-slides.html` with explicit on-slide principle callouts for the five required teaching points: load control beyond kg, external proposal vs internal response, RPE/RIR as calibration tools rather than standalone measures, technique and fatigue signs reframing self-report, and the acute-adjustment principle of the menor mudanca suficiente.

- [x] Create `revisoes/produtos/auditoria-slides-rascunho-01.md` as the first slide audit:
  - Include YAML front matter with `type: analysis`, `title: Auditoria Slides Rascunho 01`, `created` using the current local date, `tags: [slides, auditoria, controle-carga]`, and `related` wiki-links to `[[Roteiro Apresentacao Controle de Carga]]` and `[[Fonte Mestre Validada]]`.
  - Check alignment with audience, scope, 8-block progression, language density, source fidelity, exclusions, and operational usefulness.
  - List concrete corrections made during the phase and remaining items to verify after user or NotebookLM review.
  - Completion note 2026-06-30: created `revisoes/produtos/auditoria-slides-rascunho-01.md` with the requested YAML front matter and wiki-link relationships. The audit compares the storyboard and HTML deck against the validated source, master roteiro, slide direction, and language-density criteria; records the decision as **Aprovado com ajustes pequenos**; verifies audience/scope/progression/source fidelity/exclusions/operational usefulness; lists corrections already made during the phase; and flags the main remaining correction: reconcile the current 33-slide storyboard with the 32-slide HTML deck.

- [x] Correct the slide deck and storyboard based on the first audit:
  - Apply any fixes identified in `revisoes/produtos/auditoria-slides-rascunho-01.md`.
  - Remove any performance-sport, clinical, periodization-heavy, or registration/logging drift.
  - Reduce any slide that feels like a textbook paragraph into a shorter teaching point plus speaker note.
  - Preserve the complete 8-block progression after edits.
  - Completion note 2026-06-30: reconciled `slides/roteiro-apresentacao.md` with `slides/controle-carga-slides.html` as a 32-slide working deck, preserving the 8-block progression and 60 to 90 minute training range. Translated residual English kickers in the HTML, softened the technique-vs-self-report wording so it reopens the decision without sounding absolute, kept periodization/clinical/high-performance/logging topics only as exclusions, and maintained low-density on-slide text with detail moved to speaker notes.

- [x] Verify Phase 03 deliverables:
  - Confirm `slides/roteiro-apresentacao.md`, `slides/controle-carga-slides.html`, and `revisoes/produtos/auditoria-slides-rascunho-01.md` exist.
  - Open or inspect `slides/controle-carga-slides.html` and confirm the slide sections are visible, ordered, and readable without a build step.
  - Confirm every block from `fluxo padrão/04_roteiro-mestre-rascunho.md` appears in the storyboard and deck.
  - Confirm the deck states the acute-adjustment focus and does not treat registro de treino as part of the central decision logic.
  - Completion note 2026-06-30: verified the three Phase 03 deliverables exist. Inspected `slides/controle-carga-slides.html` statically and rendered it directly from a local `file://` URL in headless Chrome without any build step; the rendered first slide was visible and readable. Structured checks confirmed 32 ordered HTML slide sections, 32 ordered slide numbers, 32 speaker-note blocks, 32 source anchors, and all eight roteiro blocks in the deck. The storyboard also has 32 ordered slides and covers blocks 1-8. The deck and storyboard state the acute-adjustment focus through the "ajuste agudo" framing and "menor mudanca suficiente" principle, while `registro` appears only as an exclusion/context item outside the central decision logic.
